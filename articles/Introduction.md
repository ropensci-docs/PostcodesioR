# Introduction

PostcodesioR is an API wrapper for postcodes.io. It allows acquiring
geographic information about the UK postcodes and geographic
coordinates.

## Installation

``` r

if (!require("devtools")) install.packages("devtools")
devtools::install_github("ropensci/PostcodesioR")
```

## Lookup postcodes and outcodes

### Single postcode

Provide a postcode to obtain all available information

``` r

library(PostcodesioR)

lookup_result <- postcode_lookup("EC1Y8LX")

#overview
str(lookup_result)
```

    ## 'data.frame':    1 obs. of  73 variables:
    ##  $ postcode                            : chr "EC1Y 8LX"
    ##  $ quality                             : int 1
    ##  $ eastings                            : int 532544
    ##  $ northings                           : int 182128
    ##  $ country                             : chr "England"
    ##  $ nhs_ha                              : chr "London"
    ##  $ longitude                           : num -0.0909
    ##  $ latitude                            : num 51.5
    ##  $ european_electoral_region           : chr "London"
    ##  $ primary_care_trust                  : chr "Islington"
    ##  $ region                              : chr "London"
    ##  $ lsoa                                : chr "Islington 023D"
    ##  $ msoa                                : chr "Islington 023"
    ##  $ incode                              : chr "8LX"
    ##  $ outcode                             : chr "EC1Y"
    ##  $ parliamentary_constituency          : chr "Islington South and Finsbury"
    ##  $ parliamentary_constituency_2024     : chr "Islington South and Finsbury"
    ##  $ senedd_constituency                 : logi NA
    ##  $ senedd_constituency_no              : logi NA
    ##  $ admin_district                      : chr "Islington"
    ##  $ parish                              : chr "Islington, unparished area"
    ##  $ admin_county                        : logi NA
    ##  $ date_of_introduction                : chr "198001"
    ##  $ date_of_termination                 : logi NA
    ##  $ index_of_multiple_deprivation       : int 12549
    ##  $ admin_ward                          : chr "Bunhill"
    ##  $ ced                                 : logi NA
    ##  $ ccg                                 : chr "NHS West and North London"
    ##  $ nuts                                : chr "Islington"
    ##  $ pfa                                 : chr "Metropolitan Police"
    ##  $ nhs_region                          : chr "London"
    ##  $ ttwa                                : chr "London"
    ##  $ national_park                       : chr "England (non-National Park)"
    ##  $ bua                                 : chr "Islington"
    ##  $ icb                                 : chr "NHS West and North London Integrated Care Board"
    ##  $ cancer_alliance                     : chr "North Central London"
    ##  $ lsoa11                              : chr "Islington 023D"
    ##  $ msoa11                              : chr "Islington 023"
    ##  $ lsoa21                              : chr "Islington 023D"
    ##  $ msoa21                              : chr "Islington 023"
    ##  $ oa21                                : chr "E00013429"
    ##  $ ruc11                               : chr "(England/Wales) Urban major conurbation"
    ##  $ ruc21                               : chr "Urban: Nearer to a major town or city"
    ##  $ lep1                                : chr "London"
    ##  $ lep2                                : logi NA
    ##  $ admin_district_code                 : chr "E09000019"
    ##  $ admin_county_code                   : chr "E99999999"
    ##  $ admin_ward_code                     : chr "E05013699"
    ##  $ parish_code                         : chr "E43000209"
    ##  $ parliamentary_constituency_code     : chr "E14001306"
    ##  $ parliamentary_constituency_2024_code: chr "E14001306"
    ##  $ ccg_code                            : chr "E38000240"
    ##  $ ccg_id_code                         : chr "93C"
    ##  $ ced_code                            : chr "E99999999"
    ##  $ nuts_code                           : chr "TLI43"
    ##  $ lsoa_code                           : chr "E01002704"
    ##  $ msoa_code                           : chr "E02000576"
    ##  $ lau2_code                           : chr "E09000019"
    ##  $ pfa_code                            : chr "E23000001"
    ##  $ nhs_region_code                     : chr "E40000003"
    ##  $ ttwa_code                           : chr "E30000234"
    ##  $ national_park_code                  : chr "E65000001"
    ##  $ bua_code                            : chr "E63011980"
    ##  $ icb_code                            : chr "E54000071"
    ##  $ cancer_alliance_code                : chr "E56000027"
    ##  $ lsoa11_code                         : chr "E01002704"
    ##  $ msoa11_code                         : chr "E02000576"
    ##  $ lsoa21_code                         : chr "E01002704"
    ##  $ msoa21_code                         : chr "E02000576"
    ##  $ oa21_code                           : chr "E00013429"
    ##  $ ruc11_code                          : chr "A1"
    ##  $ ruc21_code                          : chr "UN1"
    ##  $ lep1_code                           : chr "E37000051"

There is another function that returns the same data points but returns
a list and allows optional parameters

``` r

query_result <- postcode_query("EC1Y8LX")

#overview
str(query_result)
```

    ## List of 1
    ##  $ :List of 46
    ##   ..$ postcode                       : chr "EC1Y 8LX"
    ##   ..$ quality                        : int 1
    ##   ..$ eastings                       : int 532544
    ##   ..$ northings                      : int 182128
    ##   ..$ country                        : chr "England"
    ##   ..$ nhs_ha                         : chr "London"
    ##   ..$ longitude                      : num -0.0909
    ##   ..$ latitude                       : num 51.5
    ##   ..$ european_electoral_region      : chr "London"
    ##   ..$ primary_care_trust             : chr "Islington"
    ##   ..$ region                         : chr "London"
    ##   ..$ lsoa                           : chr "Islington 023D"
    ##   ..$ msoa                           : chr "Islington 023"
    ##   ..$ incode                         : chr "8LX"
    ##   ..$ outcode                        : chr "EC1Y"
    ##   ..$ parliamentary_constituency     : chr "Islington South and Finsbury"
    ##   ..$ parliamentary_constituency_2024: chr "Islington South and Finsbury"
    ##   ..$ senedd_constituency            : NULL
    ##   ..$ senedd_constituency_no         : NULL
    ##   ..$ admin_district                 : chr "Islington"
    ##   ..$ parish                         : chr "Islington, unparished area"
    ##   ..$ admin_county                   : NULL
    ##   ..$ date_of_introduction           : chr "198001"
    ##   ..$ date_of_termination            : NULL
    ##   ..$ index_of_multiple_deprivation  : int 12549
    ##   ..$ admin_ward                     : chr "Bunhill"
    ##   ..$ ced                            : NULL
    ##   ..$ ccg                            : chr "NHS West and North London"
    ##   ..$ nuts                           : chr "Islington"
    ##   ..$ pfa                            : chr "Metropolitan Police"
    ##   ..$ nhs_region                     : chr "London"
    ##   ..$ ttwa                           : chr "London"
    ##   ..$ national_park                  : chr "England (non-National Park)"
    ##   ..$ bua                            : chr "Islington"
    ##   ..$ icb                            : chr "NHS West and North London Integrated Care Board"
    ##   ..$ cancer_alliance                : chr "North Central London"
    ##   ..$ lsoa11                         : chr "Islington 023D"
    ##   ..$ msoa11                         : chr "Islington 023"
    ##   ..$ lsoa21                         : chr "Islington 023D"
    ##   ..$ msoa21                         : chr "Islington 023"
    ##   ..$ oa21                           : chr "E00013429"
    ##   ..$ ruc11                          : chr "(England/Wales) Urban major conurbation"
    ##   ..$ ruc21                          : chr "Urban: Nearer to a major town or city"
    ##   ..$ lep1                           : chr "London"
    ##   ..$ lep2                           : NULL
    ##   ..$ codes                          :List of 29
    ##   .. ..$ admin_district                 : chr "E09000019"
    ##   .. ..$ admin_county                   : chr "E99999999"
    ##   .. ..$ admin_ward                     : chr "E05013699"
    ##   .. ..$ parish                         : chr "E43000209"
    ##   .. ..$ parliamentary_constituency     : chr "E14001306"
    ##   .. ..$ parliamentary_constituency_2024: chr "E14001306"
    ##   .. ..$ ccg                            : chr "E38000240"
    ##   .. ..$ ccg_id                         : chr "93C"
    ##   .. ..$ ced                            : chr "E99999999"
    ##   .. ..$ nuts                           : chr "TLI43"
    ##   .. ..$ lsoa                           : chr "E01002704"
    ##   .. ..$ msoa                           : chr "E02000576"
    ##   .. ..$ lau2                           : chr "E09000019"
    ##   .. ..$ pfa                            : chr "E23000001"
    ##   .. ..$ nhs_region                     : chr "E40000003"
    ##   .. ..$ ttwa                           : chr "E30000234"
    ##   .. ..$ national_park                  : chr "E65000001"
    ##   .. ..$ bua                            : chr "E63011980"
    ##   .. ..$ icb                            : chr "E54000071"
    ##   .. ..$ cancer_alliance                : chr "E56000027"
    ##   .. ..$ lsoa11                         : chr "E01002704"
    ##   .. ..$ msoa11                         : chr "E02000576"
    ##   .. ..$ lsoa21                         : chr "E01002704"
    ##   .. ..$ msoa21                         : chr "E02000576"
    ##   .. ..$ oa21                           : chr "E00013429"
    ##   .. ..$ ruc11                          : chr "A1"
    ##   .. ..$ ruc21                          : chr "UN1"
    ##   .. ..$ lep1                           : chr "E37000051"
    ##   .. ..$ lep2                           : NULL

This function creates a nested list with the codes for administrative
district, county, ward, parish, parliamentary constituency, CCG, and
NUTS.

### Multiple postcodes

To query two or more postcodes, use `bulk_` functions.

``` r

# You can provide a character vector:
bulk_lookup_result <- bulk_postcode_lookup(c("PR3 0SG", "M45 6GN", "EX165BL"))

# Or provide multiple arguments:
bulk_lookup_result <- bulk_postcode_lookup("PR3 0SG", "M45 6GN", "EX165BL")

# The old list form is still supported:
pc_list <- list(postcodes = c("PR3 0SG", "M45 6GN", "EX165BL"))
bulk_lookup_result <- bulk_postcode_lookup(pc_list)

# Note: whitespace in input postcodes is ignored (e.g. "S7 1FL" -> "S71FL")

#overview
str(bulk_lookup_result[1])
```

    ## List of 1
    ##  $ :List of 2
    ##   ..$ query : chr "PR30SG"
    ##   ..$ result:List of 46
    ##   .. ..$ postcode                       : chr "PR3 0SG"
    ##   .. ..$ quality                        : int 1
    ##   .. ..$ eastings                       : int 351012
    ##   .. ..$ northings                      : int 440302
    ##   .. ..$ country                        : chr "England"
    ##   .. ..$ nhs_ha                         : chr "North West"
    ##   .. ..$ longitude                      : num -2.75
    ##   .. ..$ latitude                       : num 53.9
    ##   .. ..$ european_electoral_region      : chr "North West"
    ##   .. ..$ primary_care_trust             : chr "North Lancashire Teaching"
    ##   .. ..$ region                         : chr "North West"
    ##   .. ..$ lsoa                           : chr "Wyre 006A"
    ##   .. ..$ msoa                           : chr "Wyre 006"
    ##   .. ..$ incode                         : chr "0SG"
    ##   .. ..$ outcode                        : chr "PR3"
    ##   .. ..$ parliamentary_constituency     : chr "Lancaster and Wyre"
    ##   .. ..$ parliamentary_constituency_2024: chr "Lancaster and Wyre"
    ##   .. ..$ senedd_constituency            : NULL
    ##   .. ..$ senedd_constituency_no         : NULL
    ##   .. ..$ admin_district                 : chr "Wyre"
    ##   .. ..$ parish                         : chr "Myerscough and Bilsborrow"
    ##   .. ..$ admin_county                   : chr "Lancashire"
    ##   .. ..$ date_of_introduction           : chr "200705"
    ##   .. ..$ date_of_termination            : NULL
    ##   .. ..$ index_of_multiple_deprivation  : int 23736
    ##   .. ..$ admin_ward                     : chr "Brock with Catterall"
    ##   .. ..$ ced                            : chr "Wyre Rural East"
    ##   .. ..$ ccg                            : chr "NHS Lancashire and South Cumbria"
    ##   .. ..$ nuts                           : chr "Wyre"
    ##   .. ..$ pfa                            : chr "Lancashire"
    ##   .. ..$ nhs_region                     : chr "North West"
    ##   .. ..$ ttwa                           : chr "Preston"
    ##   .. ..$ national_park                  : chr "England (non-National Park)"
    ##   .. ..$ bua                            : chr "Bilsborrow"
    ##   .. ..$ icb                            : chr "NHS Lancashire and South Cumbria Integrated Care Board"
    ##   .. ..$ cancer_alliance                : chr "Lancashire and South Cumbria"
    ##   .. ..$ lsoa11                         : chr "Wyre 006A"
    ##   .. ..$ msoa11                         : chr "Wyre 006"
    ##   .. ..$ lsoa21                         : chr "Wyre 006A"
    ##   .. ..$ msoa21                         : chr "Wyre 006"
    ##   .. ..$ oa21                           : chr "E00185591"
    ##   .. ..$ ruc11                          : chr "(England/Wales) Rural village"
    ##   .. ..$ ruc21                          : chr "Smaller rural: Nearer to a major town or city"
    ##   .. ..$ lep1                           : chr "Lancashire"
    ##   .. ..$ lep2                           : NULL
    ##   .. ..$ codes                          :List of 29
    ##   .. .. ..$ admin_district                 : chr "E07000128"
    ##   .. .. ..$ admin_county                   : chr "E10000017"
    ##   .. .. ..$ admin_ward                     : chr "E05009934"
    ##   .. .. ..$ parish                         : chr "E04005340"
    ##   .. .. ..$ parliamentary_constituency     : chr "E14001318"
    ##   .. .. ..$ parliamentary_constituency_2024: chr "E14001318"
    ##   .. .. ..$ ccg                            : chr "E38000226"
    ##   .. .. ..$ ccg_id                         : chr "02M"
    ##   .. .. ..$ ced                            : chr "E58000832"
    ##   .. .. ..$ nuts                           : chr "TLD44"
    ##   .. .. ..$ lsoa                           : chr "E01025547"
    ##   .. .. ..$ msoa                           : chr "E02005324"
    ##   .. .. ..$ lau2                           : chr "E07000128"
    ##   .. .. ..$ pfa                            : chr "E23000003"
    ##   .. .. ..$ nhs_region                     : chr "E40000014"
    ##   .. .. ..$ ttwa                           : chr "E30000255"
    ##   .. .. ..$ national_park                  : chr "E65000001"
    ##   .. .. ..$ bua                            : chr "E63007815"
    ##   .. .. ..$ icb                            : chr "E54000048"
    ##   .. .. ..$ cancer_alliance                : chr "E56000018"
    ##   .. .. ..$ lsoa11                         : chr "E01025547"
    ##   .. .. ..$ msoa11                         : chr "E02005324"
    ##   .. .. ..$ lsoa21                         : chr "E01025547"
    ##   .. .. ..$ msoa21                         : chr "E02005324"
    ##   .. .. ..$ oa21                           : chr "E00185591"
    ##   .. .. ..$ ruc11                          : chr "E1"
    ##   .. .. ..$ ruc21                          : chr "RSN1"
    ##   .. .. ..$ lep1                           : chr "E37000019"
    ##   .. .. ..$ lep2                           : NULL

If you want to work with data frame then the nested list created above
can be turned into a data frame

``` r

library(purrr)

bulk_list <- lapply(bulk_lookup_result, "[[", 2)

bulk_df <-
  map_dfr(bulk_list,
          `[`,
          c("postcode", "longitude", "latitude"))
```

Querying Scottish postcodes requires a separate function:

``` r

scottish_lookup <- scottish_postcode_lookup("EH12NG")

str(scottish_lookup)
```

    ## 'data.frame':    1 obs. of  101 variables:
    ##  $ postcode                                     : chr "EH1 2NG"
    ##  $ pc_compact                                   : chr "EH12NG"
    ##  $ postcode_district                            : chr "EH1"
    ##  $ postcode_sector                              : chr "EH1 2"
    ##  $ incode                                       : chr "2NG"
    ##  $ outcode                                      : chr "EH1"
    ##  $ user_type                                    : chr "small"
    ##  $ date_of_introduction                         : chr "1/8/1973 00:00:00"
    ##  $ date_of_deletion                             : logi NA
    ##  $ linked_small_user_postcode                   : logi NA
    ##  $ longitude                                    : num -3.2
    ##  $ latitude                                     : num 55.9
    ##  $ eastings                                     : int 325066
    ##  $ northings                                    : int 673533
    ##  $ split_indicator                              : chr "N"
    ##  $ grid_link_indicator                          : chr "Y"
    ##  $ grid_link_positional_accuracy                : chr "1"
    ##  $ council_area                                 : chr "City of Edinburgh"
    ##  $ electoral_ward                               : chr "City Centre"
    ##  $ registration_district                        : chr "S12000036"
    ##  $ enterprise_region                            : chr "East of Scotland"
    ##  $ strategic_development_planning_area          : chr "S11000003"
    ##  $ local_government_district                    : chr "Edinburgh City"
    ##  $ local_government_district_1991               : chr "Edinburgh City"
    ##  $ uk_parliamentary_constituency                : chr "Edinburgh East and Musselburgh"
    ##  $ scottish_parliamentary_region                : chr "Edinburgh and Lothians East"
    ##  $ scottish_parliamentary_region_2021           : chr "Lothian"
    ##  $ scottish_parliamentary_constituency          : chr "Edinburgh Central"
    ##  $ scottish_parliamentary_constituency_2021     : chr "Edinburgh Central"
    ##  $ health_board_area                            : chr "Lothian"
    ##  $ health_board_area_2006                       : chr "Lothian"
    ##  $ health_board_area_1995                       : chr "Lothian"
    ##  $ integration_authority                        : chr "Edinburgh"
    ##  $ output_area                                  : chr "S00143095"
    ##  $ output_area_2011                             : chr "S00103329"
    ##  $ output_area_2001                             : chr "S00013295"
    ##  $ output_area_1991                             : chr "6229AB03B"
    ##  $ data_zone                                    : chr "Old Town, Princes Street and Leith Street - 02"
    ##  $ data_zone_2011                               : chr "S01008675"
    ##  $ data_zone_2001                               : chr "S01002117"
    ##  $ intermediate_zone                            : chr "Old Town, Princes Street and Leith Street"
    ##  $ intermediate_zone_2011                       : chr "S02001622"
    ##  $ intermediate_zone_2001                       : chr "S02000393"
    ##  $ locality                                     : chr "Edinburgh"
    ##  $ locality_2020                                : chr "Edinburgh"
    ##  $ locality_2001                                : chr "Edinburgh"
    ##  $ locality_1991                                : chr "Edinburgh"
    ##  $ settlement                                   : chr "Edinburgh"
    ##  $ settlement_2020                              : logi NA
    ##  $ settlement_2001                              : chr "Edinburgh"
    ##  $ civil_parish                                 : chr "Edinburgh"
    ##  $ island                                       : chr "Mainland of Scotland"
    ##  $ national_park                                : logi NA
    ##  $ travel_to_work_area                          : chr "Edinburgh"
    ##  $ lau_level_1                                  : chr "City of Edinburgh"
    ##  $ itl_level_2                                  : chr "East Central Scotland"
    ##  $ itl_level_3                                  : chr "City of Edinburgh"
    ##  $ urban_rural_6_fold                           : chr "1"
    ##  $ urban_rural_8_fold                           : chr "1"
    ##  $ scottish_index_of_multiple_deprivation       : int 2592
    ##  $ roa_community_planning_partnership           : logi NA
    ##  $ roa_local                                    : logi NA
    ##  $ census_household_count                       : int 2
    ##  $ census_household_count_2011                  : int 0
    ##  $ census_household_count_2001                  : int 0
    ##  $ census_household_count_1991                  : int 2
    ##  $ census_population_count                      : int 7
    ##  $ census_population_count_2011                 : int 8
    ##  $ census_population_count_2001                 : int 23
    ##  $ census_population_count_1991                 : int 24
    ##  $ never_digitised                              : logi NA
    ##  $ council_area_code                            : chr "S12000036"
    ##  $ electoral_ward_code                          : chr "S13002929"
    ##  $ enterprise_region_code                       : chr "S09000002"
    ##  $ local_government_district_code               : chr "29"
    ##  $ local_government_district_1991_code          : chr "29"
    ##  $ uk_parliamentary_constituency_code           : chr "S14000078"
    ##  $ scottish_parliamentary_region_code           : chr "S17000022"
    ##  $ scottish_parliamentary_region_2021_code      : chr "S17000012"
    ##  $ scottish_parliamentary_constituency_code     : chr "S16000182"
    ##  $ scottish_parliamentary_constituency_2021_code: chr "S16000104"
    ##  $ health_board_area_code                       : chr "S08000024"
    ##  $ health_board_area_2006_code                  : chr "S08000010"
    ##  $ health_board_area_1995_code                  : chr "05"
    ##  $ integration_authority_code                   : chr "S37000012"
    ##  $ data_zone_code                               : chr "S01014711"
    ##  $ data_zone_2011_code                          : chr "S01008675"
    ##  $ data_zone_2001_code                          : chr "S01002117"
    ##  $ intermediate_zone_code                       : chr "S02002727"
    ##  $ intermediate_zone_2011_code                  : chr "S02001622"
    ##  $ intermediate_zone_2001_code                  : chr "S02000393"
    ##  $ locality_code                                : chr "S52000233"
    ##  $ settlement_code                              : chr "S53000178"
    ##  $ civil_parish_code                            : chr "S35000287"
    ##  $ island_code                                  : chr "000"
    ##  $ travel_to_work_area_code                     : chr "S22000059"
    ##  $ lau_level_1_code                             : chr "S30000008"
    ##  $ itl_level_2_code                             : chr "TLM1"
    ##  $ itl_level_3_code                             : chr "TLM13"
    ##   [list output truncated]

### Outward code lookup

Provide an outcode to obtain geolocation data for the centroid of the
specified outcode:

``` r

ocl <- outward_code_lookup("E1")

#overview
str(ocl)
```

    ## List of 11
    ##  $ outcode                   : chr "E1"
    ##  $ longitude                 : num -0.0594
    ##  $ latitude                  : num 51.5
    ##  $ northings                 : int 181614
    ##  $ eastings                  : int 534746
    ##  $ admin_district            :List of 3
    ##   ..$ : chr "City of London"
    ##   ..$ : chr "Hackney"
    ##   ..$ : chr "Tower Hamlets"
    ##  $ parish                    :List of 3
    ##   ..$ : chr "City of London, unparished area"
    ##   ..$ : chr "Hackney, unparished area"
    ##   ..$ : chr "Tower Hamlets, unparished area"
    ##  $ admin_county              : list()
    ##  $ admin_ward                :List of 14
    ##   ..$ : chr "Aldgate"
    ##   ..$ : chr "Bethnal Green East"
    ##   ..$ : chr "Bethnal Green West"
    ##   ..$ : chr "Bishopsgate"
    ##   ..$ : chr "Bow West"
    ##   ..$ : chr "Hoxton East & Shoreditch"
    ##   ..$ : chr "Portsoken"
    ##   ..$ : chr "Shadwell"
    ##   ..$ : chr "Spitalfields & Banglatown"
    ##   ..$ : chr "St Dunstan's"
    ##   ..$ : chr "Stepney Green"
    ##   ..$ : chr "Tower"
    ##   ..$ : chr "Weavers"
    ##   ..$ : chr "Whitechapel"
    ##  $ country                   :List of 1
    ##   ..$ : chr "England"
    ##  $ parliamentary_constituency:List of 4
    ##   ..$ : chr "Bethnal Green and Stepney"
    ##   ..$ : chr "Cities of London and Westminster"
    ##   ..$ : chr "Hackney South and Shoreditch"
    ##   ..$ : chr "Stratford and Bow"

## Reverse geocoding

Provide latitude and longitude to obtain geographic information.
Different levels of aggregation are available, i.e. postcode or outcode.

### Single postcode

``` r

rev_geo <- reverse_geocoding(0.127, 51.507)

# overview
str(rev_geo[1])
```

    ## List of 1
    ##  $ :List of 47
    ##   ..$ postcode                       : chr "SE28 8NH"
    ##   ..$ quality                        : int 1
    ##   ..$ eastings                       : int 547715
    ##   ..$ northings                      : int 180780
    ##   ..$ country                        : chr "England"
    ##   ..$ nhs_ha                         : chr "London"
    ##   ..$ longitude                      : num 0.127
    ##   ..$ latitude                       : num 51.5
    ##   ..$ european_electoral_region      : chr "London"
    ##   ..$ primary_care_trust             : chr "Bexley"
    ##   ..$ region                         : chr "London"
    ##   ..$ lsoa                           : chr "Bexley 001D"
    ##   ..$ msoa                           : chr "Bexley 001"
    ##   ..$ incode                         : chr "8NH"
    ##   ..$ outcode                        : chr "SE28"
    ##   ..$ parliamentary_constituency     : chr "Erith and Thamesmead"
    ##   ..$ parliamentary_constituency_2024: chr "Erith and Thamesmead"
    ##   ..$ senedd_constituency            : NULL
    ##   ..$ senedd_constituency_no         : NULL
    ##   ..$ admin_district                 : chr "Bexley"
    ##   ..$ parish                         : chr "Bexley, unparished area"
    ##   ..$ admin_county                   : NULL
    ##   ..$ date_of_introduction           : chr "198410"
    ##   ..$ date_of_termination            : NULL
    ##   ..$ index_of_multiple_deprivation  : int 14434
    ##   ..$ admin_ward                     : chr "Thamesmead East"
    ##   ..$ ced                            : NULL
    ##   ..$ ccg                            : chr "NHS South East London"
    ##   ..$ nuts                           : chr "Bexley"
    ##   ..$ pfa                            : chr "Metropolitan Police"
    ##   ..$ nhs_region                     : chr "London"
    ##   ..$ ttwa                           : chr "London"
    ##   ..$ national_park                  : chr "England (non-National Park)"
    ##   ..$ bua                            : chr "Bexley"
    ##   ..$ icb                            : chr "NHS South East London Integrated Care Board"
    ##   ..$ cancer_alliance                : chr "South East London"
    ##   ..$ lsoa11                         : chr "Bexley 001D"
    ##   ..$ msoa11                         : chr "Bexley 001"
    ##   ..$ lsoa21                         : chr "Bexley 001D"
    ##   ..$ msoa21                         : chr "Bexley 001"
    ##   ..$ oa21                           : chr "E00002294"
    ##   ..$ ruc11                          : chr "(England/Wales) Urban major conurbation"
    ##   ..$ ruc21                          : chr "Urban: Nearer to a major town or city"
    ##   ..$ lep1                           : chr "London"
    ##   ..$ lep2                           : NULL
    ##   ..$ codes                          :List of 29
    ##   .. ..$ admin_district                 : chr "E09000004"
    ##   .. ..$ admin_county                   : chr "E99999999"
    ##   .. ..$ admin_ward                     : chr "E05011232"
    ##   .. ..$ parish                         : chr "E43000194"
    ##   .. ..$ parliamentary_constituency     : chr "E14001229"
    ##   .. ..$ parliamentary_constituency_2024: chr "E14001229"
    ##   .. ..$ ccg                            : chr "E38000244"
    ##   .. ..$ ccg_id                         : chr "72Q"
    ##   .. ..$ ced                            : chr "E99999999"
    ##   .. ..$ nuts                           : chr "TLI51"
    ##   .. ..$ lsoa                           : chr "E01000469"
    ##   .. ..$ msoa                           : chr "E02000065"
    ##   .. ..$ lau2                           : chr "E09000004"
    ##   .. ..$ pfa                            : chr "E23000001"
    ##   .. ..$ nhs_region                     : chr "E40000003"
    ##   .. ..$ ttwa                           : chr "E30000234"
    ##   .. ..$ national_park                  : chr "E65000001"
    ##   .. ..$ bua                            : chr "E63012138"
    ##   .. ..$ icb                            : chr "E54000030"
    ##   .. ..$ cancer_alliance                : chr "E56000010"
    ##   .. ..$ lsoa11                         : chr "E01000469"
    ##   .. ..$ msoa11                         : chr "E02000065"
    ##   .. ..$ lsoa21                         : chr "E01000469"
    ##   .. ..$ msoa21                         : chr "E02000065"
    ##   .. ..$ oa21                           : chr "E00002294"
    ##   .. ..$ ruc11                          : chr "A1"
    ##   .. ..$ ruc21                          : chr "UN1"
    ##   .. ..$ lep1                           : chr "E37000051"
    ##   .. ..$ lep2                           : NULL
    ##   ..$ distance                       : num 39

### Multiple postcodes

To reverse geocode multiple values use the function underneath. The
result is a nested list, which might be a bit intimidating, but it
allows storing unequal number of elements.

``` r

# create a list with the coordinates
geolocations_list <- structure(
 list(
 geolocations = structure(
 list(
 longitude = c(-3.15807731271522, -1.12935802905177),
 latitude = c(51.4799900627036, 50.7186356978817),
 limit = c(NA, 100L),
 radius = c(NA, 500L)),
 .Names = c("longitude", "latitude", "limit", "radius"),
 class = "data.frame",
 row.names = 1:2)),
 .Names = "geolocations")

bulk_rev_geo <- bulk_reverse_geocoding(geolocations_list)

bulk_rev_geo[[1]]$result[[1]]
```

    ## $postcode
    ## [1] "CF24 2BT"
    ## 
    ## $quality
    ## [1] 1
    ## 
    ## $eastings
    ## [1] 319675
    ## 
    ## $northings
    ## [1] 176305
    ## 
    ## $country
    ## [1] "Wales"
    ## 
    ## $nhs_ha
    ## [1] "Cardiff and Vale University Health Board"
    ## 
    ## $longitude
    ## [1] -3.158085
    ## 
    ## $latitude
    ## [1] 51.47998
    ## 
    ## $european_electoral_region
    ## [1] "Wales"
    ## 
    ## $primary_care_trust
    ## [1] "Cardiff and Vale University Health Board"
    ## 
    ## $region
    ## NULL
    ## 
    ## $lsoa
    ## [1] "Cardiff 038D"
    ## 
    ## $msoa
    ## [1] "Cardiff 038"
    ## 
    ## $incode
    ## [1] "2BT"
    ## 
    ## $outcode
    ## [1] "CF24"
    ## 
    ## $parliamentary_constituency
    ## [1] "Cardiff South and Penarth"
    ## 
    ## $parliamentary_constituency_2024
    ## [1] "Cardiff South and Penarth"
    ## 
    ## $senedd_constituency
    ## [1] "Caerdydd Penarth"
    ## 
    ## $senedd_constituency_no
    ## [1] 14
    ## 
    ## $admin_district
    ## [1] "Cardiff"
    ## 
    ## $parish
    ## [1] "Splott"
    ## 
    ## $admin_county
    ## NULL
    ## 
    ## $date_of_introduction
    ## [1] "199906"
    ## 
    ## $date_of_termination
    ## NULL
    ## 
    ## $index_of_multiple_deprivation
    ## [1] 12
    ## 
    ## $admin_ward
    ## [1] "Splott"
    ## 
    ## $ced
    ## NULL
    ## 
    ## $ccg
    ## [1] "Cardiff and Vale University"
    ## 
    ## $nuts
    ## [1] "Cardiff"
    ## 
    ## $pfa
    ## [1] "South Wales"
    ## 
    ## $nhs_region
    ## NULL
    ## 
    ## $ttwa
    ## [1] "Cardiff"
    ## 
    ## $national_park
    ## [1] "Wales (non-National Park)"
    ## 
    ## $bua
    ## [1] "Cardiff"
    ## 
    ## $icb
    ## [1] "Wales"
    ## 
    ## $cancer_alliance
    ## NULL
    ## 
    ## $lsoa11
    ## [1] "Cardiff 038D"
    ## 
    ## $msoa11
    ## [1] "Cardiff 038"
    ## 
    ## $lsoa21
    ## [1] "Cardiff 038D"
    ## 
    ## $msoa21
    ## [1] "Cardiff 038"
    ## 
    ## $oa21
    ## [1] "W00009646"
    ## 
    ## $ruc11
    ## [1] "(England/Wales) Urban city and town"
    ## 
    ## $ruc21
    ## [1] "Urban: Nearer to a major town or city"
    ## 
    ## $lep1
    ## NULL
    ## 
    ## $lep2
    ## NULL
    ## 
    ## $codes
    ## $codes$admin_district
    ## [1] "W06000015"
    ## 
    ## $codes$admin_county
    ## [1] "W99999999"
    ## 
    ## $codes$admin_ward
    ## [1] "W05001295"
    ## 
    ## $codes$parish
    ## [1] "W04001005"
    ## 
    ## $codes$parliamentary_constituency
    ## [1] "W07000091"
    ## 
    ## $codes$parliamentary_constituency_2024
    ## [1] "W07000091"
    ## 
    ## $codes$ccg
    ## [1] "W11000029"
    ## 
    ## $codes$ccg_id
    ## [1] "7A4"
    ## 
    ## $codes$ced
    ## [1] "W99999999"
    ## 
    ## $codes$nuts
    ## [1] "TLL52"
    ## 
    ## $codes$lsoa
    ## [1] "W01001874"
    ## 
    ## $codes$msoa
    ## [1] "W02000404"
    ## 
    ## $codes$lau2
    ## [1] "W06000015"
    ## 
    ## $codes$pfa
    ## [1] "W15000003"
    ## 
    ## $codes$nhs_region
    ## [1] "W99999999"
    ## 
    ## $codes$ttwa
    ## [1] "W22000024"
    ## 
    ## $codes$national_park
    ## [1] "W31000001"
    ## 
    ## $codes$bua
    ## [1] "W45001208"
    ## 
    ## $codes$icb
    ## [1] "W99999999"
    ## 
    ## $codes$cancer_alliance
    ## [1] "W99999999"
    ## 
    ## $codes$lsoa11
    ## [1] "W01001874"
    ## 
    ## $codes$msoa11
    ## [1] "W02000404"
    ## 
    ## $codes$lsoa21
    ## [1] "W01001874"
    ## 
    ## $codes$msoa21
    ## [1] "W02000404"
    ## 
    ## $codes$oa21
    ## [1] "W00009646"
    ## 
    ## $codes$ruc11
    ## [1] "C1"
    ## 
    ## $codes$ruc21
    ## [1] "UN1"
    ## 
    ## $codes$lep1
    ## [1] "W99999999"
    ## 
    ## $codes$lep2
    ## NULL
    ## 
    ## 
    ## $distance
    ## [1] 1.54699

The list above is not the most common way of storing files. It’s more
likely that a data frame will be used to store the geodata. In that
case, it has to be turned into a list of a specific forma\[…\]

``` r

geolocations_df <- structure(
  list(
    longitude = c(-3.15807731271522, -1.12935802905177),
    latitude = c(51.4799900627036, 50.7186356978817),
    limit = c(NA, 100L),
    radius = c(NA, 500L)),
  .Names = c("longitude", "latitude", "limit", "radius"),
  row.names = 1:2,
  class = "data.frame")

geolocations_df
```

    ##   longitude latitude limit radius
    ## 1 -3.158077 51.47999    NA     NA
    ## 2 -1.129358 50.71864   100    500

``` r

# turn a data frame into a list
geolocations_df2list <- list(geolocations_df)

# add a list name
names(geolocations_df2list) <- "geolocations"

# display correct input for the function
geolocations_df2list
```

    ## $geolocations
    ##   longitude latitude limit radius
    ## 1 -3.158077 51.47999    NA     NA
    ## 2 -1.129358 50.71864   100    500

Common usage of this function might be extracting particular variables.
You can extract one variable like this:

``` r

# extract one postcode
bulk_rev_geo[[1]]$result[[8]]$postcode
```

    ## [1] "CF24 2AB"

But more likely you will want more than one result. After all, that’s
the point of using a bulk function:

``` r

# function to extract variables of interest
extract_bulk_geo_variable <- function(x) {
  bulk_results <- lapply(bulk_rev_geo, `[[`, "result")
  sapply(unlist(bulk_results, recursive = FALSE), `[[`, x)
}

# define the variables you need
variables_of_interest <- c("postcode", "latitude", "longitude")

# return a data frame with the variables
data.frame(
  sapply(variables_of_interest, extract_bulk_geo_variable))
```

    ##    postcode  latitude longitude
    ## 1  CF24 2BT 51.479977 -3.158085
    ## 2  CF24 2ED 51.479719 -3.158712
    ## 3  CF24 2AA  51.48021  -3.15907
    ## 4  CF24 5NW 51.479361 -3.158487
    ## 5  CF24 2AJ 51.480683 -3.158535
    ## 6  CF24 2AH 51.480553 -3.158921
    ## 7  CF24 2DZ 51.480106 -3.156807
    ## 8  CF24 2AB 51.480615 -3.157223
    ## 9  CF24 2AL  51.48083  -3.15815
    ## 10 PO33 1PS 50.718856 -1.129272
    ## 11 PO33 1PT 50.718562 -1.128455
    ## 12 PO33 1PX 50.717878 -1.127137
    ## 13 PO33 1QB 50.717034 -1.129815
    ## 14 PO33 1QD 50.717191 -1.127843
    ## 15 PO33 1PU 50.718454 -1.126021
    ## 16 PO33 1PZ 50.716247 -1.127932
    ## 17 PO33 1FS 50.717691 -1.123882
    ## 18 PO33 1QR 50.715729 -1.125987
    ## 19 PO33 1PB 50.721101 -1.133735
    ## 20 PO33 1PR 50.721475 -1.133175
    ## 21 PO33 1QP 50.715694 -1.124911
    ## 22 PO33 1GL 50.716031 -1.124296
    ## 23 PO34 5AP 50.721536 -1.124476
    ## 24 PO33 1PY 50.715218 -1.125104

### Single outcode

``` r

out_rev_geocode <- outcode_reverse_geocoding("-3.15", "51.47")
# overview
str(out_rev_geocode[1])
```

    ## List of 1
    ##  $ :List of 11
    ##   ..$ outcode                   : chr "CF99"
    ##   ..$ longitude                 : num -3.16
    ##   ..$ latitude                  : num 51.5
    ##   ..$ northings                 : int 174506
    ##   ..$ eastings                  : int 319353
    ##   ..$ admin_district            :List of 1
    ##   .. ..$ : chr "Cardiff"
    ##   ..$ parish                    :List of 1
    ##   .. ..$ : chr "Butetown"
    ##   ..$ admin_county              : list()
    ##   ..$ admin_ward                :List of 1
    ##   .. ..$ : chr "Butetown"
    ##   ..$ country                   :List of 1
    ##   .. ..$ : chr "Wales"
    ##   ..$ parliamentary_constituency:List of 1
    ##   .. ..$ : chr "Cardiff South and Penarth"

## Generate random entries

### Postcodes

Generates a list with a random UK postcode and corresponding geographic
information:

``` r

# without restrictions
random_postcode()
```

    ## $postcode
    ## [1] "AB15 8EX"
    ## 
    ## $quality
    ## [1] 1
    ## 
    ## $eastings
    ## [1] 389928
    ## 
    ## $northings
    ## [1] 805827
    ## 
    ## $country
    ## [1] "Scotland"
    ## 
    ## $nhs_ha
    ## [1] "Grampian"
    ## 
    ## $longitude
    ## [1] -2.168077
    ## 
    ## $latitude
    ## [1] 57.14321
    ## 
    ## $european_electoral_region
    ## [1] "Scotland"
    ## 
    ## $primary_care_trust
    ## [1] "Aberdeen City Community Health Partnership"
    ## 
    ## $region
    ## NULL
    ## 
    ## $lsoa
    ## [1] "Hazlehead - 07"
    ## 
    ## $msoa
    ## [1] "Hazlehead"
    ## 
    ## $incode
    ## [1] "8EX"
    ## 
    ## $outcode
    ## [1] "AB15"
    ## 
    ## $parliamentary_constituency
    ## [1] "Aberdeen South"
    ## 
    ## $parliamentary_constituency_2024
    ## [1] "Aberdeen South"
    ## 
    ## $senedd_constituency
    ## NULL
    ## 
    ## $senedd_constituency_no
    ## NULL
    ## 
    ## $admin_district
    ## [1] "Aberdeen City"
    ## 
    ## $parish
    ## NULL
    ## 
    ## $admin_county
    ## NULL
    ## 
    ## $date_of_introduction
    ## [1] "199606"
    ## 
    ## $date_of_termination
    ## NULL
    ## 
    ## $index_of_multiple_deprivation
    ## [1] 1474
    ## 
    ## $admin_ward
    ## [1] "Hazlehead/Queens Cross/Countesswells"
    ## 
    ## $ced
    ## NULL
    ## 
    ## $ccg
    ## [1] "Aberdeen City Community Health Partnership"
    ## 
    ## $nuts
    ## [1] "Aberdeen City"
    ## 
    ## $pfa
    ## [1] "Scotland"
    ## 
    ## $nhs_region
    ## NULL
    ## 
    ## $ttwa
    ## [1] "Aberdeen"
    ## 
    ## $national_park
    ## [1] "(pseudo) Scotland (non-National Park)"
    ## 
    ## $bua
    ## NULL
    ## 
    ## $icb
    ## [1] "Scotland"
    ## 
    ## $cancer_alliance
    ## NULL
    ## 
    ## $lsoa11
    ## [1] "Hazlehead - 05"
    ## 
    ## $msoa11
    ## [1] "Hazlehead"
    ## 
    ## $lsoa21
    ## [1] "Hazlehead - 07"
    ## 
    ## $msoa21
    ## [1] "Hazlehead"
    ## 
    ## $oa21
    ## [1] "S00136553"
    ## 
    ## $ruc11
    ## [1] "(Scotland) Large Urban Area"
    ## 
    ## $ruc21
    ## [1] "Large Urban Areas"
    ## 
    ## $lep1
    ## NULL
    ## 
    ## $lep2
    ## NULL
    ## 
    ## $codes
    ## $codes$admin_district
    ## [1] "S12000033"
    ## 
    ## $codes$admin_county
    ## [1] "S99999999"
    ## 
    ## $codes$admin_ward
    ## [1] "S13002844"
    ## 
    ## $codes$parish
    ## [1] "S99999999"
    ## 
    ## $codes$parliamentary_constituency
    ## [1] "S14000061"
    ## 
    ## $codes$parliamentary_constituency_2024
    ## [1] "S14000061"
    ## 
    ## $codes$ccg
    ## [1] "S03000012"
    ## 
    ## $codes$ccg_id
    ## [1] "012"
    ## 
    ## $codes$ced
    ## [1] "S99999999"
    ## 
    ## $codes$nuts
    ## [1] "TLM50"
    ## 
    ## $codes$lsoa
    ## [1] "S01013530"
    ## 
    ## $codes$msoa
    ## [1] "S02002523"
    ## 
    ## $codes$lau2
    ## [1] "S30000026"
    ## 
    ## $codes$pfa
    ## [1] "S23000009"
    ## 
    ## $codes$nhs_region
    ## [1] "S99999999"
    ## 
    ## $codes$ttwa
    ## [1] "S22000047"
    ## 
    ## $codes$national_park
    ## [1] "S99999999"
    ## 
    ## $codes$bua
    ## [1] "S99999999"
    ## 
    ## $codes$icb
    ## [1] "S99999999"
    ## 
    ## $codes$cancer_alliance
    ## [1] "S99999999"
    ## 
    ## $codes$lsoa11
    ## [1] "S01006551"
    ## 
    ## $codes$msoa11
    ## [1] "S02001243"
    ## 
    ## $codes$lsoa21
    ## [1] "S01013530"
    ## 
    ## $codes$msoa21
    ## [1] "S02002523"
    ## 
    ## $codes$oa21
    ## [1] "S00136553"
    ## 
    ## $codes$ruc11
    ## [1] "1"
    ## 
    ## $codes$ruc21
    ## [1] "1"
    ## 
    ## $codes$lep1
    ## [1] "S99999999"
    ## 
    ## $codes$lep2
    ## NULL

A randomly generated postcode can also belong to a particular outcode:

``` r

# restrict to an outcode
random_postcode("N1")
```

    ## $postcode
    ## [1] "N1 6BN"
    ## 
    ## $quality
    ## [1] 1
    ## 
    ## $eastings
    ## [1] 532965
    ## 
    ## $northings
    ## [1] 182932
    ## 
    ## $country
    ## [1] "England"
    ## 
    ## $nhs_ha
    ## [1] "London"
    ## 
    ## $longitude
    ## [1] -0.084528
    ## 
    ## $latitude
    ## [1] 51.52965
    ## 
    ## $european_electoral_region
    ## [1] "London"
    ## 
    ## $primary_care_trust
    ## [1] "City and Hackney Teaching"
    ## 
    ## $region
    ## [1] "London"
    ## 
    ## $lsoa
    ## [1] "Hackney 032C"
    ## 
    ## $msoa
    ## [1] "Hackney 032"
    ## 
    ## $incode
    ## [1] "6BN"
    ## 
    ## $outcode
    ## [1] "N1"
    ## 
    ## $parliamentary_constituency
    ## [1] "Hackney South and Shoreditch"
    ## 
    ## $parliamentary_constituency_2024
    ## [1] "Hackney South and Shoreditch"
    ## 
    ## $senedd_constituency
    ## NULL
    ## 
    ## $senedd_constituency_no
    ## NULL
    ## 
    ## $admin_district
    ## [1] "Hackney"
    ## 
    ## $parish
    ## [1] "Hackney, unparished area"
    ## 
    ## $admin_county
    ## NULL
    ## 
    ## $date_of_introduction
    ## [1] "198001"
    ## 
    ## $date_of_termination
    ## NULL
    ## 
    ## $index_of_multiple_deprivation
    ## [1] 12611
    ## 
    ## $admin_ward
    ## [1] "Hoxton West"
    ## 
    ## $ced
    ## NULL
    ## 
    ## $ccg
    ## [1] "NHS North East London"
    ## 
    ## $nuts
    ## [1] "Hackney"
    ## 
    ## $pfa
    ## [1] "Metropolitan Police"
    ## 
    ## $nhs_region
    ## [1] "London"
    ## 
    ## $ttwa
    ## [1] "London"
    ## 
    ## $national_park
    ## [1] "England (non-National Park)"
    ## 
    ## $bua
    ## [1] "Hackney"
    ## 
    ## $icb
    ## [1] "NHS North East London Integrated Care Board"
    ## 
    ## $cancer_alliance
    ## [1] "North East London"
    ## 
    ## $lsoa11
    ## [1] "Hackney 027I"
    ## 
    ## $msoa11
    ## [1] "Hackney 027"
    ## 
    ## $lsoa21
    ## [1] "Hackney 032C"
    ## 
    ## $msoa21
    ## [1] "Hackney 032"
    ## 
    ## $oa21
    ## [1] "E00008874"
    ## 
    ## $ruc11
    ## [1] "(England/Wales) Urban major conurbation"
    ## 
    ## $ruc21
    ## [1] "Urban: Nearer to a major town or city"
    ## 
    ## $lep1
    ## [1] "London"
    ## 
    ## $lep2
    ## NULL
    ## 
    ## $codes
    ## $codes$admin_district
    ## [1] "E09000012"
    ## 
    ## $codes$admin_county
    ## [1] "E99999999"
    ## 
    ## $codes$admin_ward
    ## [1] "E05009378"
    ## 
    ## $codes$parish
    ## [1] "E43000202"
    ## 
    ## $codes$parliamentary_constituency
    ## [1] "E14001260"
    ## 
    ## $codes$parliamentary_constituency_2024
    ## [1] "E14001260"
    ## 
    ## $codes$ccg
    ## [1] "E38000255"
    ## 
    ## $codes$ccg_id
    ## [1] "A3A8R"
    ## 
    ## $codes$ced
    ## [1] "E99999999"
    ## 
    ## $codes$nuts
    ## [1] "TLI41"
    ## 
    ## $codes$lsoa
    ## [1] "E01033711"
    ## 
    ## $codes$msoa
    ## [1] "E02007110"
    ## 
    ## $codes$lau2
    ## [1] "E09000012"
    ## 
    ## $codes$pfa
    ## [1] "E23000001"
    ## 
    ## $codes$nhs_region
    ## [1] "E40000003"
    ## 
    ## $codes$ttwa
    ## [1] "E30000234"
    ## 
    ## $codes$national_park
    ## [1] "E65000001"
    ## 
    ## $codes$bua
    ## [1] "E63011969"
    ## 
    ## $codes$icb
    ## [1] "E54000029"
    ## 
    ## $codes$cancer_alliance
    ## [1] "E56000028"
    ## 
    ## $codes$lsoa11
    ## [1] "E01033711"
    ## 
    ## $codes$msoa11
    ## [1] "E02000371"
    ## 
    ## $codes$lsoa21
    ## [1] "E01033711"
    ## 
    ## $codes$msoa21
    ## [1] "E02007110"
    ## 
    ## $codes$oa21
    ## [1] "E00008874"
    ## 
    ## $codes$ruc11
    ## [1] "A1"
    ## 
    ## $codes$ruc21
    ## [1] "UN1"
    ## 
    ## $codes$lep1
    ## [1] "E37000051"
    ## 
    ## $codes$lep2
    ## NULL

## Places

You can also generate a random place, specified by an OSGB code, with
corresponding geographic information:

``` r

random_place()
```

    ##                   code  name_1 name_1_lang name_2 name_2_lang local_type
    ## 1 osgb4000000074573308 Neenton        NULL   NULL        NULL    Village
    ##   outcode county_unitary county_unitary_type district_borough
    ## 1    WV16     Shropshire    UnitaryAuthority             NULL
    ##   district_borough_type        region country longitude latitude eastings
    ## 1                  NULL West Midlands England -2.532604 52.48747   363931
    ##   northings min_eastings min_northings max_eastings max_northings
    ## 1    287862       363403        287580       364212        288304

## Postcode validation

This function can validate a UK postcode:

``` r

postcode_validation("EC1Y8LX") # actual UK postcode
```

    ## [1] TRUE

``` r

postcode_validation("XYZ") # incorrect UK postcode
```

    ## [1] FALSE

## Autocomplete postcodes

Find the potential candidates for a postcode if you only know the
beginning characters

``` r

postcode_autocomplete("EC1")
```

    ##    postcode
    ## 1  EC1A 1AA
    ## 2  EC1A 1AH
    ## 3  EC1A 1AZ
    ## 4  EC1A 1BB
    ## 5  EC1A 1DN
    ## 6  EC1A 1DU
    ## 7  EC1A 1HQ
    ## 8  EC1A 1SS
    ## 9  EC1A 1TA
    ## 10 EC1A 1TB

It defaults to 10 candidates, but can be changed by specifying the
`limit` argument.

## Find nearest postcodes or outcodes

Provide a postcode to get a list of the nearest postcodes:

``` r

near_pc <- nearest_postcode("EC1Y8LX")

#overview
str(near_pc[1])
```

    ## List of 1
    ##  $ :List of 47
    ##   ..$ postcode                       : chr "EC1Y 8LX"
    ##   ..$ quality                        : int 1
    ##   ..$ eastings                       : int 532544
    ##   ..$ northings                      : int 182128
    ##   ..$ country                        : chr "England"
    ##   ..$ nhs_ha                         : chr "London"
    ##   ..$ longitude                      : num -0.0909
    ##   ..$ latitude                       : num 51.5
    ##   ..$ european_electoral_region      : chr "London"
    ##   ..$ primary_care_trust             : chr "Islington"
    ##   ..$ region                         : chr "London"
    ##   ..$ lsoa                           : chr "Islington 023D"
    ##   ..$ msoa                           : chr "Islington 023"
    ##   ..$ incode                         : chr "8LX"
    ##   ..$ outcode                        : chr "EC1Y"
    ##   ..$ parliamentary_constituency     : chr "Islington South and Finsbury"
    ##   ..$ parliamentary_constituency_2024: chr "Islington South and Finsbury"
    ##   ..$ senedd_constituency            : NULL
    ##   ..$ senedd_constituency_no         : NULL
    ##   ..$ admin_district                 : chr "Islington"
    ##   ..$ parish                         : chr "Islington, unparished area"
    ##   ..$ admin_county                   : NULL
    ##   ..$ date_of_introduction           : chr "198001"
    ##   ..$ date_of_termination            : NULL
    ##   ..$ index_of_multiple_deprivation  : int 12549
    ##   ..$ admin_ward                     : chr "Bunhill"
    ##   ..$ ced                            : NULL
    ##   ..$ ccg                            : chr "NHS West and North London"
    ##   ..$ nuts                           : chr "Islington"
    ##   ..$ pfa                            : chr "Metropolitan Police"
    ##   ..$ nhs_region                     : chr "London"
    ##   ..$ ttwa                           : chr "London"
    ##   ..$ national_park                  : chr "England (non-National Park)"
    ##   ..$ bua                            : chr "Islington"
    ##   ..$ icb                            : chr "NHS West and North London Integrated Care Board"
    ##   ..$ cancer_alliance                : chr "North Central London"
    ##   ..$ lsoa11                         : chr "Islington 023D"
    ##   ..$ msoa11                         : chr "Islington 023"
    ##   ..$ lsoa21                         : chr "Islington 023D"
    ##   ..$ msoa21                         : chr "Islington 023"
    ##   ..$ oa21                           : chr "E00013429"
    ##   ..$ ruc11                          : chr "(England/Wales) Urban major conurbation"
    ##   ..$ ruc21                          : chr "Urban: Nearer to a major town or city"
    ##   ..$ lep1                           : chr "London"
    ##   ..$ lep2                           : NULL
    ##   ..$ codes                          :List of 29
    ##   .. ..$ admin_district                 : chr "E09000019"
    ##   .. ..$ admin_county                   : chr "E99999999"
    ##   .. ..$ admin_ward                     : chr "E05013699"
    ##   .. ..$ parish                         : chr "E43000209"
    ##   .. ..$ parliamentary_constituency     : chr "E14001306"
    ##   .. ..$ parliamentary_constituency_2024: chr "E14001306"
    ##   .. ..$ ccg                            : chr "E38000240"
    ##   .. ..$ ccg_id                         : chr "93C"
    ##   .. ..$ ced                            : chr "E99999999"
    ##   .. ..$ nuts                           : chr "TLI43"
    ##   .. ..$ lsoa                           : chr "E01002704"
    ##   .. ..$ msoa                           : chr "E02000576"
    ##   .. ..$ lau2                           : chr "E09000019"
    ##   .. ..$ pfa                            : chr "E23000001"
    ##   .. ..$ nhs_region                     : chr "E40000003"
    ##   .. ..$ ttwa                           : chr "E30000234"
    ##   .. ..$ national_park                  : chr "E65000001"
    ##   .. ..$ bua                            : chr "E63011980"
    ##   .. ..$ icb                            : chr "E54000071"
    ##   .. ..$ cancer_alliance                : chr "E56000027"
    ##   .. ..$ lsoa11                         : chr "E01002704"
    ##   .. ..$ msoa11                         : chr "E02000576"
    ##   .. ..$ lsoa21                         : chr "E01002704"
    ##   .. ..$ msoa21                         : chr "E02000576"
    ##   .. ..$ oa21                           : chr "E00013429"
    ##   .. ..$ ruc11                          : chr "A1"
    ##   .. ..$ ruc21                          : chr "UN1"
    ##   .. ..$ lep1                           : chr "E37000051"
    ##   .. ..$ lep2                           : NULL
    ##   ..$ distance                       : int 0

You can also use outcodes:

``` r

near_outcode <- nearest_outcode("EC1Y")

# overview
str(near_outcode[2])
```

    ## List of 1
    ##  $ :List of 11
    ##   ..$ outcode                   : chr "EC2Y"
    ##   ..$ longitude                 : num -0.0935
    ##   ..$ latitude                  : num 51.5
    ##   ..$ northings                 : int 181783
    ##   ..$ eastings                  : int 532369
    ##   ..$ admin_district            :List of 2
    ##   .. ..$ : chr "City of London"
    ##   .. ..$ : chr "Islington"
    ##   ..$ parish                    :List of 2
    ##   .. ..$ : chr "City of London, unparished area"
    ##   .. ..$ : chr "Islington, unparished area"
    ##   ..$ admin_county              : list()
    ##   ..$ admin_ward                :List of 6
    ##   .. ..$ : chr "Aldersgate"
    ##   .. ..$ : chr "Bassishaw"
    ##   .. ..$ : chr "Bunhill"
    ##   .. ..$ : chr "Clerkenwell"
    ##   .. ..$ : chr "Coleman Street"
    ##   .. ..$ : chr "Cripplegate"
    ##   ..$ country                   :List of 1
    ##   .. ..$ : chr "England"
    ##   ..$ parliamentary_constituency:List of 2
    ##   .. ..$ : chr "Cities of London and Westminster"
    ##   .. ..$ : chr "Islington South and Finsbury"

Or longitude and latitude

``` r

near_ll <- nearest_outcode_lonlat(0.127, 51.507)

#overview
str(near_ll[1])
```

    ## List of 1
    ##  $ :List of 11
    ##   ..$ outcode                   : chr "DA18"
    ##   ..$ longitude                 : num 0.136
    ##   ..$ latitude                  : num 51.5
    ##   ..$ northings                 : int 179423
    ##   ..$ eastings                  : int 548396
    ##   ..$ admin_district            :List of 1
    ##   .. ..$ : chr "Bexley"
    ##   ..$ parish                    :List of 1
    ##   .. ..$ : chr "Bexley, unparished area"
    ##   ..$ admin_county              : list()
    ##   ..$ admin_ward                :List of 2
    ##   .. ..$ : chr "Slade Green & Northend"
    ##   .. ..$ : chr "Thamesmead East"
    ##   ..$ country                   :List of 1
    ##   .. ..$ : chr "England"
    ##   ..$ parliamentary_constituency:List of 2
    ##   .. ..$ : chr "Bexleyheath and Crayford"
    ##   .. ..$ : chr "Erith and Thamesmead"

## Find places

Provide a name of a place of interest. You can specify the number of
results (default is 10):

``` r

place_query_result <- place_query("Hills", limit = 11)

# overview
str(place_query_result[1])
```

    ## List of 1
    ##  $ :List of 21
    ##   ..$ code                 : chr "osgb4000000074555222"
    ##   ..$ name_1               : chr "Tan Hills"
    ##   ..$ name_1_lang          : NULL
    ##   ..$ name_2               : NULL
    ##   ..$ name_2_lang          : NULL
    ##   ..$ local_type           : chr "Village"
    ##   ..$ outcode              : chr "DH2"
    ##   ..$ county_unitary       : chr "County Durham"
    ##   ..$ county_unitary_type  : chr "UnitaryAuthority"
    ##   ..$ district_borough     : NULL
    ##   ..$ district_borough_type: NULL
    ##   ..$ region               : chr "North East"
    ##   ..$ country              : chr "England"
    ##   ..$ longitude            : num -1.6
    ##   ..$ latitude             : num 54.8
    ##   ..$ eastings             : int 425936
    ##   ..$ northings            : int 547579
    ##   ..$ min_eastings         : int 425721
    ##   ..$ min_northings        : int 547375
    ##   ..$ max_eastings         : int 426221
    ##   ..$ max_northings        : int 547875

You can also find a place using an OSGB code:

``` r

place_lookup_result <- place_lookup("osgb4000000074544700")

# overview
str(place_lookup_result)
```

    ## List of 21
    ##  $ code                 : chr "osgb4000000074544700"
    ##  $ name_1               : chr "Cutler Heights"
    ##  $ name_1_lang          : NULL
    ##  $ name_2               : NULL
    ##  $ name_2_lang          : NULL
    ##  $ local_type           : chr "Suburban Area"
    ##  $ outcode              : chr "BD4"
    ##  $ county_unitary       : NULL
    ##  $ county_unitary_type  : NULL
    ##  $ district_borough     : chr "Bradford"
    ##  $ district_borough_type: chr "MetropolitanDistrict"
    ##  $ region               : chr "Yorkshire and the Humber"
    ##  $ country              : chr "England"
    ##  $ longitude            : num -1.72
    ##  $ latitude             : num 53.8
    ##  $ eastings             : int 418830
    ##  $ northings            : int 431785
    ##  $ min_eastings         : int 418449
    ##  $ min_northings        : int 431455
    ##  $ max_eastings         : int 419076
    ##  $ max_northings        : int 432106

## Terminated postcodes

You might end up having terminated postcodes in your data set. These are
postcodes that are no longer active. UK postcodes can change so it’s
worth checking whether used postcodes are still activ\[…\]

``` r

terminated_postcode("E1W 1UU")
```

    ##   postcode year_terminated month_terminated eastings northings longitude
    ## 1  E1W 1UU            2015                2   533779    180545 -0.073706
    ##   latitude
    ## 1 51.50801
