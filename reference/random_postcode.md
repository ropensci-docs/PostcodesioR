# Random postcode

Returns a random postcode and all available data for that postcode.

## Usage

``` r
random_postcode(outcode = NULL)
```

## Arguments

- outcode:

  A string. Filters random postcodes by outcode. Returns null if invalid
  outcode. Optional.

## Value

A list with a random postcode with corresponding characteristics.

## See also

[`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
random_postcode()
#> $postcode
#> [1] "SY13 3DU"
#> 
#> $quality
#> [1] 1
#> 
#> $eastings
#> [1] 343520
#> 
#> $northings
#> [1] 341209
#> 
#> $country
#> [1] "Wales"
#> 
#> $nhs_ha
#> [1] "Betsi Cadwaladr University Health Board"
#> 
#> $longitude
#> [1] -2.842354
#> 
#> $latitude
#> [1] 52.96527
#> 
#> $european_electoral_region
#> [1] "Wales"
#> 
#> $primary_care_trust
#> [1] "Betsi Cadwaladr University Health Board"
#> 
#> $region
#> NULL
#> 
#> $lsoa
#> [1] "Wrexham 018C"
#> 
#> $msoa
#> [1] "Wrexham 018"
#> 
#> $incode
#> [1] "3DU"
#> 
#> $outcode
#> [1] "SY13"
#> 
#> $parliamentary_constituency
#> [1] "Wrexham"
#> 
#> $parliamentary_constituency_2024
#> [1] "Wrexham"
#> 
#> $senedd_constituency
#> [1] "Fflint Wrecsam"
#> 
#> $senedd_constituency_no
#> [1] 3
#> 
#> $admin_district
#> [1] "Wrexham"
#> 
#> $parish
#> [1] "Hanmer"
#> 
#> $admin_county
#> NULL
#> 
#> $date_of_introduction
#> [1] "198001"
#> 
#> $date_of_termination
#> NULL
#> 
#> $index_of_multiple_deprivation
#> [1] 1465
#> 
#> $admin_ward
#> [1] "Bronington and Hanmer"
#> 
#> $ced
#> NULL
#> 
#> $ccg
#> [1] "Betsi Cadwaladr University"
#> 
#> $nuts
#> [1] "Wrexham"
#> 
#> $pfa
#> [1] "North Wales"
#> 
#> $nhs_region
#> NULL
#> 
#> $ttwa
#> [1] "Wrexham"
#> 
#> $national_park
#> [1] "Wales (non-National Park)"
#> 
#> $bua
#> NULL
#> 
#> $icb
#> [1] "Wales"
#> 
#> $cancer_alliance
#> NULL
#> 
#> $lsoa11
#> [1] "Wrexham 018C"
#> 
#> $msoa11
#> [1] "Wrexham 018"
#> 
#> $lsoa21
#> [1] "Wrexham 018C"
#> 
#> $msoa21
#> [1] "Wrexham 018"
#> 
#> $oa21
#> [1] "W00002142"
#> 
#> $ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> $ruc21
#> [1] "Smaller rural: Further from a major town or city"
#> 
#> $lep1
#> NULL
#> 
#> $lep2
#> NULL
#> 
#> $codes
#> $codes$admin_district
#> [1] "W06000006"
#> 
#> $codes$admin_county
#> [1] "W99999999"
#> 
#> $codes$admin_ward
#> [1] "W05001717"
#> 
#> $codes$parish
#> [1] "W04000229"
#> 
#> $codes$parliamentary_constituency
#> [1] "W07000111"
#> 
#> $codes$parliamentary_constituency_2024
#> [1] "W07000111"
#> 
#> $codes$ccg
#> [1] "W11000023"
#> 
#> $codes$ccg_id
#> [1] "7A1"
#> 
#> $codes$ced
#> [1] "W99999999"
#> 
#> $codes$nuts
#> [1] "TLL34"
#> 
#> $codes$lsoa
#> [1] "W01000403"
#> 
#> $codes$msoa
#> [1] "W02000095"
#> 
#> $codes$lau2
#> [1] "W06000006"
#> 
#> $codes$pfa
#> [1] "W15000001"
#> 
#> $codes$nhs_region
#> [1] "W99999999"
#> 
#> $codes$ttwa
#> [1] "W22000034"
#> 
#> $codes$national_park
#> [1] "W31000001"
#> 
#> $codes$bua
#> NULL
#> 
#> $codes$icb
#> [1] "W99999999"
#> 
#> $codes$cancer_alliance
#> [1] "W99999999"
#> 
#> $codes$lsoa11
#> [1] "W01000403"
#> 
#> $codes$msoa11
#> [1] "W02000095"
#> 
#> $codes$lsoa21
#> [1] "W01000403"
#> 
#> $codes$msoa21
#> [1] "W02000095"
#> 
#> $codes$oa21
#> [1] "W00002142"
#> 
#> $codes$ruc11
#> [1] "F1"
#> 
#> $codes$ruc21
#> [1] "RSF1"
#> 
#> $codes$lep1
#> [1] "W99999999"
#> 
#> $codes$lep2
#> NULL
#> 
#> 
random_postcode("N1")
#> $postcode
#> [1] "N1 3BH"
#> 
#> $quality
#> [1] 1
#> 
#> $eastings
#> [1] 532686
#> 
#> $northings
#> [1] 184202
#> 
#> $country
#> [1] "England"
#> 
#> $nhs_ha
#> [1] "London"
#> 
#> $longitude
#> [1] -0.08807
#> 
#> $latitude
#> [1] 51.54113
#> 
#> $european_electoral_region
#> [1] "London"
#> 
#> $primary_care_trust
#> [1] "Islington"
#> 
#> $region
#> [1] "London"
#> 
#> $lsoa
#> [1] "Islington 014C"
#> 
#> $msoa
#> [1] "Islington 014"
#> 
#> $incode
#> [1] "3BH"
#> 
#> $outcode
#> [1] "N1"
#> 
#> $parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> $parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> $senedd_constituency
#> NULL
#> 
#> $senedd_constituency_no
#> NULL
#> 
#> $admin_district
#> [1] "Islington"
#> 
#> $parish
#> [1] "Islington, unparished area"
#> 
#> $admin_county
#> NULL
#> 
#> $date_of_introduction
#> [1] "198001"
#> 
#> $date_of_termination
#> NULL
#> 
#> $index_of_multiple_deprivation
#> [1] 8938
#> 
#> $admin_ward
#> [1] "Canonbury"
#> 
#> $ced
#> NULL
#> 
#> $ccg
#> [1] "NHS West and North London"
#> 
#> $nuts
#> [1] "Islington"
#> 
#> $pfa
#> [1] "Metropolitan Police"
#> 
#> $nhs_region
#> [1] "London"
#> 
#> $ttwa
#> [1] "London"
#> 
#> $national_park
#> [1] "England (non-National Park)"
#> 
#> $bua
#> [1] "Islington"
#> 
#> $icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> $cancer_alliance
#> [1] "North Central London"
#> 
#> $lsoa11
#> [1] "Islington 014C"
#> 
#> $msoa11
#> [1] "Islington 014"
#> 
#> $lsoa21
#> [1] "Islington 014C"
#> 
#> $msoa21
#> [1] "Islington 014"
#> 
#> $oa21
#> [1] "E00013517"
#> 
#> $ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> $ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> $lep1
#> [1] "London"
#> 
#> $lep2
#> NULL
#> 
#> $codes
#> $codes$admin_district
#> [1] "E09000019"
#> 
#> $codes$admin_county
#> [1] "E99999999"
#> 
#> $codes$admin_ward
#> [1] "E05013701"
#> 
#> $codes$parish
#> [1] "E43000209"
#> 
#> $codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> $codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> $codes$ccg
#> [1] "E38000240"
#> 
#> $codes$ccg_id
#> [1] "93C"
#> 
#> $codes$ced
#> [1] "E99999999"
#> 
#> $codes$nuts
#> [1] "TLI43"
#> 
#> $codes$lsoa
#> [1] "E01002721"
#> 
#> $codes$msoa
#> [1] "E02000567"
#> 
#> $codes$lau2
#> [1] "E09000019"
#> 
#> $codes$pfa
#> [1] "E23000001"
#> 
#> $codes$nhs_region
#> [1] "E40000003"
#> 
#> $codes$ttwa
#> [1] "E30000234"
#> 
#> $codes$national_park
#> [1] "E65000001"
#> 
#> $codes$bua
#> [1] "E63011980"
#> 
#> $codes$icb
#> [1] "E54000071"
#> 
#> $codes$cancer_alliance
#> [1] "E56000027"
#> 
#> $codes$lsoa11
#> [1] "E01002721"
#> 
#> $codes$msoa11
#> [1] "E02000567"
#> 
#> $codes$lsoa21
#> [1] "E01002721"
#> 
#> $codes$msoa21
#> [1] "E02000567"
#> 
#> $codes$oa21
#> [1] "E00013517"
#> 
#> $codes$ruc11
#> [1] "A1"
#> 
#> $codes$ruc21
#> [1] "UN1"
#> 
#> $codes$lep1
#> [1] "E37000051"
#> 
#> $codes$lep2
#> NULL
#> 
#> 
# }
```
