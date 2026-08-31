# Scottish postcode lookup

Lookup a Scottish postcode.

## Usage

``` r
scottish_postcode_lookup(postcode)
```

## Arguments

- postcode:

  A string. One valid Scottish postcode. This function is case- and
  space-insensitive. For non-Scottish postcodes use
  [`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md).
  For more than one non-Scottish postcode use
  [`bulk_postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/bulk_postcode_lookup.md).

## Value

A data frame. Returns all available data if found. Returns NAs if
postcode does not exist (404).

- `postcode` Postcode. Royal Mail postcode.

- `scottish_parliamentary_constituency` Scottish Parliamentary
  Constituency 2014 Scottish Parliamentary Constituency.

- `scottish_parliamentary_constituency` Scottish Parliamentary
  Constituency GSS Code. A code that identifies a 2014 Scottish
  Parliamentary Constituency.

See <https://postcodes.io/docs> for more details.

## Examples

``` r
# \donttest{
scottish_postcode_lookup("EH12NG")
#>   postcode pc_compact postcode_district postcode_sector incode outcode
#> 1  EH1 2NG     EH12NG               EH1           EH1 2    2NG     EH1
#>   user_type date_of_introduction date_of_deletion linked_small_user_postcode
#> 1     small    1/8/1973 00:00:00               NA                         NA
#>   longitude latitude eastings northings split_indicator grid_link_indicator
#> 1 -3.201479 55.94896   325066    673533               N                   Y
#>   grid_link_positional_accuracy      council_area electoral_ward
#> 1                             1 City of Edinburgh    City Centre
#>   registration_district enterprise_region strategic_development_planning_area
#> 1             S12000036  East of Scotland                           S11000003
#>   local_government_district local_government_district_1991
#> 1            Edinburgh City                 Edinburgh City
#>    uk_parliamentary_constituency scottish_parliamentary_region
#> 1 Edinburgh East and Musselburgh   Edinburgh and Lothians East
#>   scottish_parliamentary_region_2021 scottish_parliamentary_constituency
#> 1                            Lothian                   Edinburgh Central
#>   scottish_parliamentary_constituency_2021 health_board_area
#> 1                        Edinburgh Central           Lothian
#>   health_board_area_2006 health_board_area_1995 integration_authority
#> 1                Lothian                Lothian             Edinburgh
#>   output_area output_area_2011 output_area_2001 output_area_1991
#> 1   S00143095        S00103329        S00013295        6229AB03B
#>                                        data_zone data_zone_2011 data_zone_2001
#> 1 Old Town, Princes Street and Leith Street - 02      S01008675      S01002117
#>                           intermediate_zone intermediate_zone_2011
#> 1 Old Town, Princes Street and Leith Street              S02001622
#>   intermediate_zone_2001  locality locality_2020 locality_2001 locality_1991
#> 1              S02000393 Edinburgh     Edinburgh     Edinburgh     Edinburgh
#>   settlement settlement_2020 settlement_2001 civil_parish               island
#> 1  Edinburgh              NA       Edinburgh    Edinburgh Mainland of Scotland
#>   national_park travel_to_work_area       lau_level_1           itl_level_2
#> 1            NA           Edinburgh City of Edinburgh East Central Scotland
#>         itl_level_3 urban_rural_6_fold urban_rural_8_fold
#> 1 City of Edinburgh                  1                  1
#>   scottish_index_of_multiple_deprivation roa_community_planning_partnership
#> 1                                   2592                                 NA
#>   roa_local census_household_count census_household_count_2011
#> 1        NA                      2                           0
#>   census_household_count_2001 census_household_count_1991
#> 1                           0                           2
#>   census_population_count census_population_count_2011
#> 1                       7                            8
#>   census_population_count_2001 census_population_count_1991 never_digitised
#> 1                           23                           24              NA
#>   council_area_code electoral_ward_code enterprise_region_code
#> 1         S12000036           S13002929              S09000002
#>   local_government_district_code local_government_district_1991_code
#> 1                             29                                  29
#>   uk_parliamentary_constituency_code scottish_parliamentary_region_code
#> 1                          S14000078                          S17000022
#>   scottish_parliamentary_region_2021_code
#> 1                               S17000012
#>   scottish_parliamentary_constituency_code
#> 1                                S16000182
#>   scottish_parliamentary_constituency_2021_code health_board_area_code
#> 1                                     S16000104              S08000024
#>   health_board_area_2006_code health_board_area_1995_code
#> 1                   S08000010                          05
#>   integration_authority_code data_zone_code data_zone_2011_code
#> 1                  S37000012      S01014711           S01008675
#>   data_zone_2001_code intermediate_zone_code intermediate_zone_2011_code
#> 1           S01002117              S02002727                   S02001622
#>   intermediate_zone_2001_code locality_code settlement_code civil_parish_code
#> 1                   S02000393     S52000233       S53000178         S35000287
#>   island_code travel_to_work_area_code lau_level_1_code itl_level_2_code
#> 1         000                S22000059        S30000008             TLM1
#>   itl_level_3_code registration_district_code
#> 1            TLM13                  S12000036
#>   strategic_development_planning_area_code
#> 1                                S11000003
# }
```
