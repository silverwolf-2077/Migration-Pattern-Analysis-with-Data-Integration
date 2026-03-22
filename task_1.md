Task 2
================
Ruihan Ding
2026-03-21

Import, clean and merge the datasets.

``` r
files = list.files(
  "migration",
  pattern = "\\.xls$",
  full.names = TRUE,
  ignore.case = TRUE
)

read_migration_file = function(file_path) {
  read_excel(
    file_path,
    skip = 8,
    col_names = c(
      "dest_state_fips",
      "dest_county_fips",
      "orig_state_fips",
      "orig_county_fips",
      "state_abbr",
      "flow_description",
      "returns",
      "exemptions",
      "income_thousands"
    ),
    col_types = rep("text", 9)
  ) |>
    mutate(
      returns = parse_number(returns),
      exemptions = parse_number(exemptions),
      income_thousands = parse_number(income_thousands)
    )
}

migration_raw = map_dfr(files, read_migration_file) |> 
  arrange(dest_state_fips, dest_county_fips, orig_state_fips, orig_county_fips)
```

## 1

Identify the county pairs with the most interactions (by number of
exemptions).

``` r
# get rid of the summary rows and non-migration rows
migration_df = migration_raw |> 
  filter(
    orig_state_fips <= 56,
    !(dest_state_fips == orig_state_fips & dest_county_fips == orig_county_fips)
  )

county_pairs = migration_df |>
  mutate(
    # create FIPS codes for each county
    dest_fips = paste0(dest_state_fips, dest_county_fips),
    orig_fips = paste0(orig_state_fips, orig_county_fips),
    # create county pairs
    pair_1 = pmin(orig_fips, dest_fips),
    pair_2 = pmax(orig_fips, dest_fips)
  ) |>
  # sum exemptions for each county pair
  group_by(pair_1, pair_2) |>
  summarise(
    total_exemptions = sum(exemptions, na.rm = TRUE),
    .groups = "drop"
  ) |>
  arrange(desc(total_exemptions))
```
