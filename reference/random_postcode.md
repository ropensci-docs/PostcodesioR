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
#> [1] "YO11 3DZ"
#> 
#> $quality
#> [1] 1
#> 
#> $eastings
#> [1] 505732
#> 
#> $northings
#> [1] 482918
#> 
#> $country
#> [1] "England"
#> 
#> $nhs_ha
#> [1] "Yorkshire and the Humber"
#> 
#> $longitude
#> [1] -0.379491
#> 
#> $latitude
#> [1] 54.23108
#> 
#> $european_electoral_region
#> [1] "Yorkshire and The Humber"
#> 
#> $primary_care_trust
#> [1] "North Yorkshire and York"
#> 
#> $region
#> [1] "Yorkshire and The Humber"
#> 
#> $lsoa
#> [1] "Scarborough 011B"
#> 
#> $msoa
#> [1] "Scarborough 011"
#> 
#> $incode
#> [1] "3DZ"
#> 
#> $outcode
#> [1] "YO11"
#> 
#> $parliamentary_constituency
#> [1] "Scarborough and Whitby"
#> 
#> $parliamentary_constituency_2024
#> [1] "Scarborough and Whitby"
#> 
#> $senedd_constituency
#> NULL
#> 
#> $senedd_constituency_no
#> NULL
#> 
#> $admin_district
#> [1] "North Yorkshire"
#> 
#> $parish
#> [1] "Cayton"
#> 
#> $admin_county
#> NULL
#> 
#> $date_of_introduction
#> [1] "201312"
#> 
#> $date_of_termination
#> NULL
#> 
#> $index_of_multiple_deprivation
#> [1] 23283
#> 
#> $admin_ward
#> [1] "Cayton"
#> 
#> $ced
#> NULL
#> 
#> $ccg
#> [1] "NHS Humber and North Yorkshire"
#> 
#> $nuts
#> [1] "North Yorkshire"
#> 
#> $pfa
#> [1] "North Yorkshire"
#> 
#> $nhs_region
#> [1] "North East and Yorkshire"
#> 
#> $ttwa
#> [1] "Scarborough"
#> 
#> $national_park
#> [1] "England (non-National Park)"
#> 
#> $bua
#> [1] "Scarborough"
#> 
#> $icb
#> [1] "NHS Humber and North Yorkshire Integrated Care Board"
#> 
#> $cancer_alliance
#> [1] "Humber and North Yorkshire"
#> 
#> $lsoa11
#> [1] "Scarborough 011B"
#> 
#> $msoa11
#> [1] "Scarborough 011"
#> 
#> $lsoa21
#> [1] "Scarborough 011B"
#> 
#> $msoa21
#> [1] "Scarborough 011"
#> 
#> $oa21
#> [1] "E00141651"
#> 
#> $ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> $ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> $lep1
#> [1] "York and North Yorkshire"
#> 
#> $lep2
#> NULL
#> 
#> $codes
#> $codes$admin_district
#> [1] "E06000065"
#> 
#> $codes$admin_county
#> [1] "E99999999"
#> 
#> $codes$admin_ward
#> [1] "E05014265"
#> 
#> $codes$parish
#> [1] "E04007663"
#> 
#> $codes$parliamentary_constituency
#> [1] "E14001461"
#> 
#> $codes$parliamentary_constituency_2024
#> [1] "E14001461"
#> 
#> $codes$ccg
#> [1] "E38000241"
#> 
#> $codes$ccg_id
#> [1] "42D"
#> 
#> $codes$ced
#> [1] "E99999999"
#> 
#> $codes$nuts
#> [1] "TLE22"
#> 
#> $codes$lsoa
#> [1] "E01027808"
#> 
#> $codes$msoa
#> [1] "E02005805"
#> 
#> $codes$lau2
#> [1] "E06000065"
#> 
#> $codes$pfa
#> [1] "E23000009"
#> 
#> $codes$nhs_region
#> [1] "E40000012"
#> 
#> $codes$ttwa
#> [1] "E30000259"
#> 
#> $codes$national_park
#> [1] "E65000001"
#> 
#> $codes$bua
#> [1] "E63007514"
#> 
#> $codes$icb
#> [1] "E54000051"
#> 
#> $codes$cancer_alliance
#> [1] "E56000026"
#> 
#> $codes$lsoa11
#> [1] "E01027808"
#> 
#> $codes$msoa11
#> [1] "E02005805"
#> 
#> $codes$lsoa21
#> [1] "E01027808"
#> 
#> $codes$msoa21
#> [1] "E02005805"
#> 
#> $codes$oa21
#> [1] "E00141651"
#> 
#> $codes$ruc11
#> [1] "C1"
#> 
#> $codes$ruc21
#> [1] "UF1"
#> 
#> $codes$lep1
#> [1] "E37000058"
#> 
#> $codes$lep2
#> NULL
#> 
#> 
random_postcode("N1")
#> $postcode
#> [1] "N1 2ZE"
#> 
#> $quality
#> [1] 1
#> 
#> $eastings
#> [1] 531708
#> 
#> $northings
#> [1] 184241
#> 
#> $country
#> [1] "England"
#> 
#> $nhs_ha
#> [1] "London"
#> 
#> $longitude
#> [1] -0.102149
#> 
#> $latitude
#> [1] 51.54171
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
#> [1] "Islington 016D"
#> 
#> $msoa
#> [1] "Islington 016"
#> 
#> $incode
#> [1] "2ZE"
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
#> [1] "200502"
#> 
#> $date_of_termination
#> NULL
#> 
#> $index_of_multiple_deprivation
#> [1] 3653
#> 
#> $admin_ward
#> [1] "St Mary's & St James'"
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
#> [1] "Islington 016D"
#> 
#> $msoa11
#> [1] "Islington 016"
#> 
#> $lsoa21
#> [1] "Islington 016D"
#> 
#> $msoa21
#> [1] "Islington 016"
#> 
#> $oa21
#> [1] "E00013953"
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
#> [1] "E05013710"
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
#> [1] "E01002790"
#> 
#> $codes$msoa
#> [1] "E02000569"
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
#> [1] "E01002790"
#> 
#> $codes$msoa11
#> [1] "E02000569"
#> 
#> $codes$lsoa21
#> [1] "E01002790"
#> 
#> $codes$msoa21
#> [1] "E02000569"
#> 
#> $codes$oa21
#> [1] "E00013953"
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
