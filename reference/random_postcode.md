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
#> [1] "PE14 9JS"
#> 
#> $quality
#> [1] 1
#> 
#> $eastings
#> [1] 550832
#> 
#> $northings
#> [1] 299638
#> 
#> $country
#> [1] "England"
#> 
#> $nhs_ha
#> [1] "East of England"
#> 
#> $longitude
#> [1] 0.224325
#> 
#> $latitude
#> [1] 52.57367
#> 
#> $european_electoral_region
#> [1] "Eastern"
#> 
#> $primary_care_trust
#> [1] "Norfolk"
#> 
#> $region
#> [1] "East of England"
#> 
#> $lsoa
#> [1] "King's Lynn and West Norfolk 016E"
#> 
#> $msoa
#> [1] "King's Lynn and West Norfolk 016"
#> 
#> $incode
#> [1] "9JS"
#> 
#> $outcode
#> [1] "PE14"
#> 
#> $parliamentary_constituency
#> [1] "South West Norfolk"
#> 
#> $parliamentary_constituency_2024
#> [1] "South West Norfolk"
#> 
#> $senedd_constituency
#> NULL
#> 
#> $senedd_constituency_no
#> NULL
#> 
#> $admin_district
#> [1] "King's Lynn and West Norfolk"
#> 
#> $parish
#> [1] "Upwell"
#> 
#> $admin_county
#> [1] "Norfolk"
#> 
#> $date_of_introduction
#> [1] "198001"
#> 
#> $date_of_termination
#> NULL
#> 
#> $index_of_multiple_deprivation
#> [1] 4162
#> 
#> $admin_ward
#> [1] "Upwell & Delph"
#> 
#> $ced
#> [1] "Marshland South"
#> 
#> $ccg
#> [1] "NHS Norfolk and Suffolk"
#> 
#> $nuts
#> [1] "King's Lynn and West Norfolk"
#> 
#> $pfa
#> [1] "Norfolk"
#> 
#> $nhs_region
#> [1] "East of England"
#> 
#> $ttwa
#> [1] "Wisbech"
#> 
#> $national_park
#> [1] "England (non-National Park)"
#> 
#> $bua
#> NULL
#> 
#> $icb
#> [1] "NHS Norfolk and Suffolk Integrated Care Board"
#> 
#> $cancer_alliance
#> [1] "East of England"
#> 
#> $lsoa11
#> [1] "King's Lynn and West Norfolk 016E"
#> 
#> $msoa11
#> [1] "King's Lynn and West Norfolk 016"
#> 
#> $lsoa21
#> [1] "King's Lynn and West Norfolk 016E"
#> 
#> $msoa21
#> [1] "King's Lynn and West Norfolk 016"
#> 
#> $oa21
#> [1] "E00135786"
#> 
#> $ruc11
#> [1] "(England/Wales) Rural village"
#> 
#> $ruc21
#> [1] "Smaller rural: Further from a major town or city"
#> 
#> $lep1
#> [1] "New Anglia"
#> 
#> $lep2
#> NULL
#> 
#> $codes
#> $codes$admin_district
#> [1] "E07000146"
#> 
#> $codes$admin_county
#> [1] "E10000020"
#> 
#> $codes$admin_ward
#> [1] "E05012351"
#> 
#> $codes$parish
#> [1] "E04006366"
#> 
#> $codes$parliamentary_constituency
#> [1] "E14001497"
#> 
#> $codes$parliamentary_constituency_2024
#> [1] "E14001497"
#> 
#> $codes$ccg
#> [1] "E38000239"
#> 
#> $codes$ccg_id
#> [1] "26A"
#> 
#> $codes$ced
#> [1] "E58001005"
#> 
#> $codes$nuts
#> [1] "TLH52"
#> 
#> $codes$lsoa
#> [1] "E01026716"
#> 
#> $codes$msoa
#> [1] "E02005566"
#> 
#> $codes$lau2
#> [1] "E07000146"
#> 
#> $codes$pfa
#> [1] "E23000024"
#> 
#> $codes$nhs_region
#> [1] "E40000013"
#> 
#> $codes$ttwa
#> [1] "E30000287"
#> 
#> $codes$national_park
#> [1] "E65000001"
#> 
#> $codes$bua
#> NULL
#> 
#> $codes$icb
#> [1] "E54000068"
#> 
#> $codes$cancer_alliance
#> [1] "E56000035"
#> 
#> $codes$lsoa11
#> [1] "E01026716"
#> 
#> $codes$msoa11
#> [1] "E02005566"
#> 
#> $codes$lsoa21
#> [1] "E01026716"
#> 
#> $codes$msoa21
#> [1] "E02005566"
#> 
#> $codes$oa21
#> [1] "E00135786"
#> 
#> $codes$ruc11
#> [1] "E1"
#> 
#> $codes$ruc21
#> [1] "RSF1"
#> 
#> $codes$lep1
#> [1] "E37000052"
#> 
#> $codes$lep2
#> NULL
#> 
#> 
random_postcode("N1")
#> $postcode
#> [1] "N1 2BH"
#> 
#> $quality
#> [1] 1
#> 
#> $eastings
#> [1] 531854
#> 
#> $northings
#> [1] 183924
#> 
#> $country
#> [1] "England"
#> 
#> $nhs_ha
#> [1] "London"
#> 
#> $longitude
#> [1] -0.100164
#> 
#> $latitude
#> [1] 51.53883
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
#> [1] "Islington 016F"
#> 
#> $msoa
#> [1] "Islington 016"
#> 
#> $incode
#> [1] "2BH"
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
#> [1] 5450
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
#> [1] "Islington 016F"
#> 
#> $msoa11
#> [1] "Islington 016"
#> 
#> $lsoa21
#> [1] "Islington 016F"
#> 
#> $msoa21
#> [1] "Islington 016"
#> 
#> $oa21
#> [1] "E00013928"
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
#> [1] "E01002793"
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
#> [1] "E01002793"
#> 
#> $codes$msoa11
#> [1] "E02000569"
#> 
#> $codes$lsoa21
#> [1] "E01002793"
#> 
#> $codes$msoa21
#> [1] "E02000569"
#> 
#> $codes$oa21
#> [1] "E00013928"
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
