# Reverse geocoding

Returns nearest postcodes for a given longitude and latitude.

## Usage

``` r
reverse_geocoding(
  longitude,
  latitude,
  limit = 10,
  radius = 100,
  wideSearch = NULL
)
```

## Arguments

- longitude:

  A string or numeric. Needs to have at least three decimal points.

- latitude:

  A string or numeric. Needs to have at least three decimal points.

- limit:

  An integer. Limits number of postcodes matches to return. Defaults
  to 10. Needs to be less than 100.

- radius:

  An integer. Limits number of postcodes matches to return. Defaults to
  100m. Needs to be less than 2,000m.

- wideSearch:

  TRUE or FALSE. Search up to 20km radius, but subject to a maximum of
  10 results. Since lookups over a wide area can be very expensive,
  we've created this method to allow you choose to make the trade off
  between search radius and number of results. Defaults to false. When
  enabled, radius and limits over 10 are ignored.

## Value

A list with available data.

## See also

[`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
reverse_geocoding(0.127, 51.507)
#> [[1]]
#> [[1]]$postcode
#> [1] "SE28 8NH"
#> 
#> [[1]]$quality
#> [1] 1
#> 
#> [[1]]$eastings
#> [1] 547715
#> 
#> [[1]]$northings
#> [1] 180780
#> 
#> [[1]]$country
#> [1] "England"
#> 
#> [[1]]$nhs_ha
#> [1] "London"
#> 
#> [[1]]$longitude
#> [1] 0.12706
#> 
#> [[1]]$latitude
#> [1] 51.50665
#> 
#> [[1]]$european_electoral_region
#> [1] "London"
#> 
#> [[1]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[1]]$region
#> [1] "London"
#> 
#> [[1]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[1]]$msoa
#> [1] "Bexley 001"
#> 
#> [[1]]$incode
#> [1] "8NH"
#> 
#> [[1]]$outcode
#> [1] "SE28"
#> 
#> [[1]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[1]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[1]]$senedd_constituency
#> NULL
#> 
#> [[1]]$senedd_constituency_no
#> NULL
#> 
#> [[1]]$admin_district
#> [1] "Bexley"
#> 
#> [[1]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[1]]$admin_county
#> NULL
#> 
#> [[1]]$date_of_introduction
#> [1] "198410"
#> 
#> [[1]]$date_of_termination
#> NULL
#> 
#> [[1]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[1]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[1]]$ced
#> NULL
#> 
#> [[1]]$ccg
#> [1] "NHS South East London"
#> 
#> [[1]]$nuts
#> [1] "Bexley"
#> 
#> [[1]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[1]]$nhs_region
#> [1] "London"
#> 
#> [[1]]$ttwa
#> [1] "London"
#> 
#> [[1]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[1]]$bua
#> [1] "Bexley"
#> 
#> [[1]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[1]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[1]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[1]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[1]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[1]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[1]]$oa21
#> [1] "E00002294"
#> 
#> [[1]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[1]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$lep1
#> [1] "London"
#> 
#> [[1]]$lep2
#> NULL
#> 
#> [[1]]$codes
#> [[1]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[1]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[1]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[1]]$codes$parish
#> [1] "E43000194"
#> 
#> [[1]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[1]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[1]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[1]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[1]]$codes$ced
#> [1] "E99999999"
#> 
#> [[1]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[1]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[1]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[1]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[1]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[1]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[1]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[1]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[1]]$codes$bua
#> [1] "E63012138"
#> 
#> [[1]]$codes$icb
#> [1] "E54000030"
#> 
#> [[1]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[1]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[1]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[1]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[1]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[1]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[1]]$codes$ruc11
#> [1] "A1"
#> 
#> [[1]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[1]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$distance
#> [1] 39.02863
#> 
#> 
#> [[2]]
#> [[2]]$postcode
#> [1] "SE28 8NA"
#> 
#> [[2]]$quality
#> [1] 1
#> 
#> [[2]]$eastings
#> [1] 547680
#> 
#> [[2]]$northings
#> [1] 180848
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$nhs_ha
#> [1] "London"
#> 
#> [[2]]$longitude
#> [1] 0.126585
#> 
#> [[2]]$latitude
#> [1] 51.50727
#> 
#> [[2]]$european_electoral_region
#> [1] "London"
#> 
#> [[2]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[2]]$region
#> [1] "London"
#> 
#> [[2]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[2]]$msoa
#> [1] "Bexley 001"
#> 
#> [[2]]$incode
#> [1] "8NA"
#> 
#> [[2]]$outcode
#> [1] "SE28"
#> 
#> [[2]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[2]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[2]]$senedd_constituency
#> NULL
#> 
#> [[2]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$admin_district
#> [1] "Bexley"
#> 
#> [[2]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[2]]$admin_county
#> NULL
#> 
#> [[2]]$date_of_introduction
#> [1] "198402"
#> 
#> [[2]]$date_of_termination
#> NULL
#> 
#> [[2]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[2]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[2]]$ced
#> NULL
#> 
#> [[2]]$ccg
#> [1] "NHS South East London"
#> 
#> [[2]]$nuts
#> [1] "Bexley"
#> 
#> [[2]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[2]]$nhs_region
#> [1] "London"
#> 
#> [[2]]$ttwa
#> [1] "London"
#> 
#> [[2]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$bua
#> [1] "Bexley"
#> 
#> [[2]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[2]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[2]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[2]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[2]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[2]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[2]]$oa21
#> [1] "E00002294"
#> 
#> [[2]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[2]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[2]]$lep1
#> [1] "London"
#> 
#> [[2]]$lep2
#> NULL
#> 
#> [[2]]$codes
#> [[2]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[2]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[2]]$codes$parish
#> [1] "E43000194"
#> 
#> [[2]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[2]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[2]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[2]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[2]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[2]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[2]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[2]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[2]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[2]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[2]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[2]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$codes$bua
#> [1] "E63012138"
#> 
#> [[2]]$codes$icb
#> [1] "E54000030"
#> 
#> [[2]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[2]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[2]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[2]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[2]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[2]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[2]]$codes$ruc11
#> [1] "A1"
#> 
#> [[2]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[2]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[2]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$distance
#> [1] 41.70994
#> 
#> 
#> [[3]]
#> [[3]]$postcode
#> [1] "SE28 8NN"
#> 
#> [[3]]$quality
#> [1] 1
#> 
#> [[3]]$eastings
#> [1] 547685
#> 
#> [[3]]$northings
#> [1] 180759
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$nhs_ha
#> [1] "London"
#> 
#> [[3]]$longitude
#> [1] 0.12662
#> 
#> [[3]]$latitude
#> [1] 51.50647
#> 
#> [[3]]$european_electoral_region
#> [1] "London"
#> 
#> [[3]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[3]]$region
#> [1] "London"
#> 
#> [[3]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa
#> [1] "Bexley 001"
#> 
#> [[3]]$incode
#> [1] "8NN"
#> 
#> [[3]]$outcode
#> [1] "SE28"
#> 
#> [[3]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[3]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[3]]$senedd_constituency
#> NULL
#> 
#> [[3]]$senedd_constituency_no
#> NULL
#> 
#> [[3]]$admin_district
#> [1] "Bexley"
#> 
#> [[3]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[3]]$admin_county
#> NULL
#> 
#> [[3]]$date_of_introduction
#> [1] "198410"
#> 
#> [[3]]$date_of_termination
#> NULL
#> 
#> [[3]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[3]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[3]]$ced
#> NULL
#> 
#> [[3]]$ccg
#> [1] "NHS South East London"
#> 
#> [[3]]$nuts
#> [1] "Bexley"
#> 
#> [[3]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[3]]$nhs_region
#> [1] "London"
#> 
#> [[3]]$ttwa
#> [1] "London"
#> 
#> [[3]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[3]]$bua
#> [1] "Bexley"
#> 
#> [[3]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[3]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[3]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[3]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[3]]$oa21
#> [1] "E00002294"
#> 
#> [[3]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[3]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[3]]$lep1
#> [1] "London"
#> 
#> [[3]]$lep2
#> NULL
#> 
#> [[3]]$codes
#> [[3]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[3]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[3]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[3]]$codes$parish
#> [1] "E43000194"
#> 
#> [[3]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[3]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[3]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[3]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[3]]$codes$ced
#> [1] "E99999999"
#> 
#> [[3]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[3]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[3]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[3]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[3]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[3]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[3]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[3]]$codes$bua
#> [1] "E63012138"
#> 
#> [[3]]$codes$icb
#> [1] "E54000030"
#> 
#> [[3]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[3]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[3]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[3]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[3]]$codes$ruc11
#> [1] "A1"
#> 
#> [[3]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[3]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[3]]$codes$lep2
#> NULL
#> 
#> 
#> [[3]]$distance
#> [1] 64.43397
#> 
#> 
#> [[4]]
#> [[4]]$postcode
#> [1] "SE28 8NP"
#> 
#> [[4]]$quality
#> [1] 1
#> 
#> [[4]]$eastings
#> [1] 547780
#> 
#> [[4]]$northings
#> [1] 180840
#> 
#> [[4]]$country
#> [1] "England"
#> 
#> [[4]]$nhs_ha
#> [1] "London"
#> 
#> [[4]]$longitude
#> [1] 0.128021
#> 
#> [[4]]$latitude
#> [1] 51.50717
#> 
#> [[4]]$european_electoral_region
#> [1] "London"
#> 
#> [[4]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[4]]$region
#> [1] "London"
#> 
#> [[4]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[4]]$msoa
#> [1] "Bexley 001"
#> 
#> [[4]]$incode
#> [1] "8NP"
#> 
#> [[4]]$outcode
#> [1] "SE28"
#> 
#> [[4]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[4]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[4]]$senedd_constituency
#> NULL
#> 
#> [[4]]$senedd_constituency_no
#> NULL
#> 
#> [[4]]$admin_district
#> [1] "Bexley"
#> 
#> [[4]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[4]]$admin_county
#> NULL
#> 
#> [[4]]$date_of_introduction
#> [1] "198504"
#> 
#> [[4]]$date_of_termination
#> NULL
#> 
#> [[4]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[4]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[4]]$ced
#> NULL
#> 
#> [[4]]$ccg
#> [1] "NHS South East London"
#> 
#> [[4]]$nuts
#> [1] "Bexley"
#> 
#> [[4]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[4]]$nhs_region
#> [1] "London"
#> 
#> [[4]]$ttwa
#> [1] "London"
#> 
#> [[4]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[4]]$bua
#> [1] "Bexley"
#> 
#> [[4]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[4]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[4]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[4]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[4]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[4]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[4]]$oa21
#> [1] "E00002291"
#> 
#> [[4]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[4]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[4]]$lep1
#> [1] "London"
#> 
#> [[4]]$lep2
#> NULL
#> 
#> [[4]]$codes
#> [[4]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[4]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[4]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[4]]$codes$parish
#> [1] "E43000194"
#> 
#> [[4]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[4]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[4]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[4]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[4]]$codes$ced
#> [1] "E99999999"
#> 
#> [[4]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[4]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[4]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[4]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[4]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[4]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[4]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[4]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[4]]$codes$bua
#> [1] "E63012138"
#> 
#> [[4]]$codes$icb
#> [1] "E54000030"
#> 
#> [[4]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[4]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[4]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[4]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[4]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[4]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[4]]$codes$ruc11
#> [1] "A1"
#> 
#> [[4]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[4]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[4]]$codes$lep2
#> NULL
#> 
#> 
#> [[4]]$distance
#> [1] 73.26412
#> 
#> 
#> [[5]]
#> [[5]]$postcode
#> [1] "SE28 8NR"
#> 
#> [[5]]$quality
#> [1] 1
#> 
#> [[5]]$eastings
#> [1] 547760
#> 
#> [[5]]$northings
#> [1] 180897
#> 
#> [[5]]$country
#> [1] "England"
#> 
#> [[5]]$nhs_ha
#> [1] "London"
#> 
#> [[5]]$longitude
#> [1] 0.127757
#> 
#> [[5]]$latitude
#> [1] 51.50769
#> 
#> [[5]]$european_electoral_region
#> [1] "London"
#> 
#> [[5]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[5]]$region
#> [1] "London"
#> 
#> [[5]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[5]]$msoa
#> [1] "Bexley 001"
#> 
#> [[5]]$incode
#> [1] "8NR"
#> 
#> [[5]]$outcode
#> [1] "SE28"
#> 
#> [[5]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[5]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[5]]$senedd_constituency
#> NULL
#> 
#> [[5]]$senedd_constituency_no
#> NULL
#> 
#> [[5]]$admin_district
#> [1] "Bexley"
#> 
#> [[5]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[5]]$admin_county
#> NULL
#> 
#> [[5]]$date_of_introduction
#> [1] "198504"
#> 
#> [[5]]$date_of_termination
#> NULL
#> 
#> [[5]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[5]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[5]]$ced
#> NULL
#> 
#> [[5]]$ccg
#> [1] "NHS South East London"
#> 
#> [[5]]$nuts
#> [1] "Bexley"
#> 
#> [[5]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[5]]$nhs_region
#> [1] "London"
#> 
#> [[5]]$ttwa
#> [1] "London"
#> 
#> [[5]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[5]]$bua
#> [1] "Bexley"
#> 
#> [[5]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[5]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[5]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[5]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[5]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[5]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[5]]$oa21
#> [1] "E00002291"
#> 
#> [[5]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[5]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[5]]$lep1
#> [1] "London"
#> 
#> [[5]]$lep2
#> NULL
#> 
#> [[5]]$codes
#> [[5]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[5]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[5]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[5]]$codes$parish
#> [1] "E43000194"
#> 
#> [[5]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[5]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[5]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[5]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[5]]$codes$ced
#> [1] "E99999999"
#> 
#> [[5]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[5]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[5]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[5]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[5]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[5]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[5]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[5]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[5]]$codes$bua
#> [1] "E63012138"
#> 
#> [[5]]$codes$icb
#> [1] "E54000030"
#> 
#> [[5]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[5]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[5]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[5]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[5]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[5]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[5]]$codes$ruc11
#> [1] "A1"
#> 
#> [[5]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[5]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[5]]$codes$lep2
#> NULL
#> 
#> 
#> [[5]]$distance
#> [1] 92.99791
#> 
#> 
#> [[6]]
#> [[6]]$postcode
#> [1] "SE28 8NQ"
#> 
#> [[6]]$quality
#> [1] 1
#> 
#> [[6]]$eastings
#> [1] 547676
#> 
#> [[6]]$northings
#> [1] 180726
#> 
#> [[6]]$country
#> [1] "England"
#> 
#> [[6]]$nhs_ha
#> [1] "London"
#> 
#> [[6]]$longitude
#> [1] 0.126476
#> 
#> [[6]]$latitude
#> [1] 51.50618
#> 
#> [[6]]$european_electoral_region
#> [1] "London"
#> 
#> [[6]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[6]]$region
#> [1] "London"
#> 
#> [[6]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[6]]$msoa
#> [1] "Bexley 001"
#> 
#> [[6]]$incode
#> [1] "8NQ"
#> 
#> [[6]]$outcode
#> [1] "SE28"
#> 
#> [[6]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[6]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[6]]$senedd_constituency
#> NULL
#> 
#> [[6]]$senedd_constituency_no
#> NULL
#> 
#> [[6]]$admin_district
#> [1] "Bexley"
#> 
#> [[6]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[6]]$admin_county
#> NULL
#> 
#> [[6]]$date_of_introduction
#> [1] "198410"
#> 
#> [[6]]$date_of_termination
#> NULL
#> 
#> [[6]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[6]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[6]]$ced
#> NULL
#> 
#> [[6]]$ccg
#> [1] "NHS South East London"
#> 
#> [[6]]$nuts
#> [1] "Bexley"
#> 
#> [[6]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[6]]$nhs_region
#> [1] "London"
#> 
#> [[6]]$ttwa
#> [1] "London"
#> 
#> [[6]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[6]]$bua
#> [1] "Bexley"
#> 
#> [[6]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[6]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[6]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[6]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[6]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[6]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[6]]$oa21
#> [1] "E00002294"
#> 
#> [[6]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[6]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[6]]$lep1
#> [1] "London"
#> 
#> [[6]]$lep2
#> NULL
#> 
#> [[6]]$codes
#> [[6]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[6]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[6]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[6]]$codes$parish
#> [1] "E43000194"
#> 
#> [[6]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[6]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[6]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[6]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[6]]$codes$ced
#> [1] "E99999999"
#> 
#> [[6]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[6]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[6]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[6]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[6]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[6]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[6]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[6]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[6]]$codes$bua
#> [1] "E63012138"
#> 
#> [[6]]$codes$icb
#> [1] "E54000030"
#> 
#> [[6]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[6]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[6]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[6]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[6]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[6]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[6]]$codes$ruc11
#> [1] "A1"
#> 
#> [[6]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[6]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[6]]$codes$lep2
#> NULL
#> 
#> 
#> [[6]]$distance
#> [1] 98.54106
#> 
#> 
reverse_geocoding("0.1275", "51.5073", limit = 3)
#> [[1]]
#> [[1]]$postcode
#> [1] "SE28 8NP"
#> 
#> [[1]]$quality
#> [1] 1
#> 
#> [[1]]$eastings
#> [1] 547780
#> 
#> [[1]]$northings
#> [1] 180840
#> 
#> [[1]]$country
#> [1] "England"
#> 
#> [[1]]$nhs_ha
#> [1] "London"
#> 
#> [[1]]$longitude
#> [1] 0.128021
#> 
#> [[1]]$latitude
#> [1] 51.50717
#> 
#> [[1]]$european_electoral_region
#> [1] "London"
#> 
#> [[1]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[1]]$region
#> [1] "London"
#> 
#> [[1]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[1]]$msoa
#> [1] "Bexley 001"
#> 
#> [[1]]$incode
#> [1] "8NP"
#> 
#> [[1]]$outcode
#> [1] "SE28"
#> 
#> [[1]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[1]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[1]]$senedd_constituency
#> NULL
#> 
#> [[1]]$senedd_constituency_no
#> NULL
#> 
#> [[1]]$admin_district
#> [1] "Bexley"
#> 
#> [[1]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[1]]$admin_county
#> NULL
#> 
#> [[1]]$date_of_introduction
#> [1] "198504"
#> 
#> [[1]]$date_of_termination
#> NULL
#> 
#> [[1]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[1]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[1]]$ced
#> NULL
#> 
#> [[1]]$ccg
#> [1] "NHS South East London"
#> 
#> [[1]]$nuts
#> [1] "Bexley"
#> 
#> [[1]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[1]]$nhs_region
#> [1] "London"
#> 
#> [[1]]$ttwa
#> [1] "London"
#> 
#> [[1]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[1]]$bua
#> [1] "Bexley"
#> 
#> [[1]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[1]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[1]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[1]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[1]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[1]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[1]]$oa21
#> [1] "E00002291"
#> 
#> [[1]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[1]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$lep1
#> [1] "London"
#> 
#> [[1]]$lep2
#> NULL
#> 
#> [[1]]$codes
#> [[1]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[1]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[1]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[1]]$codes$parish
#> [1] "E43000194"
#> 
#> [[1]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[1]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[1]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[1]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[1]]$codes$ced
#> [1] "E99999999"
#> 
#> [[1]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[1]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[1]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[1]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[1]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[1]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[1]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[1]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[1]]$codes$bua
#> [1] "E63012138"
#> 
#> [[1]]$codes$icb
#> [1] "E54000030"
#> 
#> [[1]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[1]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[1]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[1]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[1]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[1]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[1]]$codes$ruc11
#> [1] "A1"
#> 
#> [[1]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[1]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$distance
#> [1] 38.68448
#> 
#> 
#> [[2]]
#> [[2]]$postcode
#> [1] "SE28 8NR"
#> 
#> [[2]]$quality
#> [1] 1
#> 
#> [[2]]$eastings
#> [1] 547760
#> 
#> [[2]]$northings
#> [1] 180897
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$nhs_ha
#> [1] "London"
#> 
#> [[2]]$longitude
#> [1] 0.127757
#> 
#> [[2]]$latitude
#> [1] 51.50769
#> 
#> [[2]]$european_electoral_region
#> [1] "London"
#> 
#> [[2]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[2]]$region
#> [1] "London"
#> 
#> [[2]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[2]]$msoa
#> [1] "Bexley 001"
#> 
#> [[2]]$incode
#> [1] "8NR"
#> 
#> [[2]]$outcode
#> [1] "SE28"
#> 
#> [[2]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[2]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[2]]$senedd_constituency
#> NULL
#> 
#> [[2]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$admin_district
#> [1] "Bexley"
#> 
#> [[2]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[2]]$admin_county
#> NULL
#> 
#> [[2]]$date_of_introduction
#> [1] "198504"
#> 
#> [[2]]$date_of_termination
#> NULL
#> 
#> [[2]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[2]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[2]]$ced
#> NULL
#> 
#> [[2]]$ccg
#> [1] "NHS South East London"
#> 
#> [[2]]$nuts
#> [1] "Bexley"
#> 
#> [[2]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[2]]$nhs_region
#> [1] "London"
#> 
#> [[2]]$ttwa
#> [1] "London"
#> 
#> [[2]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$bua
#> [1] "Bexley"
#> 
#> [[2]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[2]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[2]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[2]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[2]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[2]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[2]]$oa21
#> [1] "E00002291"
#> 
#> [[2]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[2]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[2]]$lep1
#> [1] "London"
#> 
#> [[2]]$lep2
#> NULL
#> 
#> [[2]]$codes
#> [[2]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[2]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[2]]$codes$parish
#> [1] "E43000194"
#> 
#> [[2]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[2]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[2]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[2]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[2]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[2]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[2]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[2]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[2]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[2]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[2]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[2]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$codes$bua
#> [1] "E63012138"
#> 
#> [[2]]$codes$icb
#> [1] "E54000030"
#> 
#> [[2]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[2]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[2]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[2]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[2]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[2]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[2]]$codes$ruc11
#> [1] "A1"
#> 
#> [[2]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[2]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[2]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$distance
#> [1] 46.97491
#> 
#> 
#> [[3]]
#> [[3]]$postcode
#> [1] "SE28 8NA"
#> 
#> [[3]]$quality
#> [1] 1
#> 
#> [[3]]$eastings
#> [1] 547680
#> 
#> [[3]]$northings
#> [1] 180848
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$nhs_ha
#> [1] "London"
#> 
#> [[3]]$longitude
#> [1] 0.126585
#> 
#> [[3]]$latitude
#> [1] 51.50727
#> 
#> [[3]]$european_electoral_region
#> [1] "London"
#> 
#> [[3]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[3]]$region
#> [1] "London"
#> 
#> [[3]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa
#> [1] "Bexley 001"
#> 
#> [[3]]$incode
#> [1] "8NA"
#> 
#> [[3]]$outcode
#> [1] "SE28"
#> 
#> [[3]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[3]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[3]]$senedd_constituency
#> NULL
#> 
#> [[3]]$senedd_constituency_no
#> NULL
#> 
#> [[3]]$admin_district
#> [1] "Bexley"
#> 
#> [[3]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[3]]$admin_county
#> NULL
#> 
#> [[3]]$date_of_introduction
#> [1] "198402"
#> 
#> [[3]]$date_of_termination
#> NULL
#> 
#> [[3]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[3]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[3]]$ced
#> NULL
#> 
#> [[3]]$ccg
#> [1] "NHS South East London"
#> 
#> [[3]]$nuts
#> [1] "Bexley"
#> 
#> [[3]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[3]]$nhs_region
#> [1] "London"
#> 
#> [[3]]$ttwa
#> [1] "London"
#> 
#> [[3]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[3]]$bua
#> [1] "Bexley"
#> 
#> [[3]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[3]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[3]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[3]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[3]]$oa21
#> [1] "E00002294"
#> 
#> [[3]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[3]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[3]]$lep1
#> [1] "London"
#> 
#> [[3]]$lep2
#> NULL
#> 
#> [[3]]$codes
#> [[3]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[3]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[3]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[3]]$codes$parish
#> [1] "E43000194"
#> 
#> [[3]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[3]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[3]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[3]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[3]]$codes$ced
#> [1] "E99999999"
#> 
#> [[3]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[3]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[3]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[3]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[3]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[3]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[3]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[3]]$codes$bua
#> [1] "E63012138"
#> 
#> [[3]]$codes$icb
#> [1] "E54000030"
#> 
#> [[3]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[3]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[3]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[3]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[3]]$codes$ruc11
#> [1] "A1"
#> 
#> [[3]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[3]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[3]]$codes$lep2
#> NULL
#> 
#> 
#> [[3]]$distance
#> [1] 63.40318
#> 
#> 
reverse_geocoding("0.1275", "51.5073", limit = 11, radius = 200)
#> [[1]]
#> [[1]]$postcode
#> [1] "SE28 8NP"
#> 
#> [[1]]$quality
#> [1] 1
#> 
#> [[1]]$eastings
#> [1] 547780
#> 
#> [[1]]$northings
#> [1] 180840
#> 
#> [[1]]$country
#> [1] "England"
#> 
#> [[1]]$nhs_ha
#> [1] "London"
#> 
#> [[1]]$longitude
#> [1] 0.128021
#> 
#> [[1]]$latitude
#> [1] 51.50717
#> 
#> [[1]]$european_electoral_region
#> [1] "London"
#> 
#> [[1]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[1]]$region
#> [1] "London"
#> 
#> [[1]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[1]]$msoa
#> [1] "Bexley 001"
#> 
#> [[1]]$incode
#> [1] "8NP"
#> 
#> [[1]]$outcode
#> [1] "SE28"
#> 
#> [[1]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[1]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[1]]$senedd_constituency
#> NULL
#> 
#> [[1]]$senedd_constituency_no
#> NULL
#> 
#> [[1]]$admin_district
#> [1] "Bexley"
#> 
#> [[1]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[1]]$admin_county
#> NULL
#> 
#> [[1]]$date_of_introduction
#> [1] "198504"
#> 
#> [[1]]$date_of_termination
#> NULL
#> 
#> [[1]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[1]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[1]]$ced
#> NULL
#> 
#> [[1]]$ccg
#> [1] "NHS South East London"
#> 
#> [[1]]$nuts
#> [1] "Bexley"
#> 
#> [[1]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[1]]$nhs_region
#> [1] "London"
#> 
#> [[1]]$ttwa
#> [1] "London"
#> 
#> [[1]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[1]]$bua
#> [1] "Bexley"
#> 
#> [[1]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[1]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[1]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[1]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[1]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[1]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[1]]$oa21
#> [1] "E00002291"
#> 
#> [[1]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[1]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$lep1
#> [1] "London"
#> 
#> [[1]]$lep2
#> NULL
#> 
#> [[1]]$codes
#> [[1]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[1]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[1]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[1]]$codes$parish
#> [1] "E43000194"
#> 
#> [[1]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[1]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[1]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[1]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[1]]$codes$ced
#> [1] "E99999999"
#> 
#> [[1]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[1]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[1]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[1]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[1]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[1]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[1]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[1]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[1]]$codes$bua
#> [1] "E63012138"
#> 
#> [[1]]$codes$icb
#> [1] "E54000030"
#> 
#> [[1]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[1]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[1]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[1]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[1]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[1]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[1]]$codes$ruc11
#> [1] "A1"
#> 
#> [[1]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[1]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$distance
#> [1] 38.68448
#> 
#> 
#> [[2]]
#> [[2]]$postcode
#> [1] "SE28 8NR"
#> 
#> [[2]]$quality
#> [1] 1
#> 
#> [[2]]$eastings
#> [1] 547760
#> 
#> [[2]]$northings
#> [1] 180897
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$nhs_ha
#> [1] "London"
#> 
#> [[2]]$longitude
#> [1] 0.127757
#> 
#> [[2]]$latitude
#> [1] 51.50769
#> 
#> [[2]]$european_electoral_region
#> [1] "London"
#> 
#> [[2]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[2]]$region
#> [1] "London"
#> 
#> [[2]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[2]]$msoa
#> [1] "Bexley 001"
#> 
#> [[2]]$incode
#> [1] "8NR"
#> 
#> [[2]]$outcode
#> [1] "SE28"
#> 
#> [[2]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[2]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[2]]$senedd_constituency
#> NULL
#> 
#> [[2]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$admin_district
#> [1] "Bexley"
#> 
#> [[2]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[2]]$admin_county
#> NULL
#> 
#> [[2]]$date_of_introduction
#> [1] "198504"
#> 
#> [[2]]$date_of_termination
#> NULL
#> 
#> [[2]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[2]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[2]]$ced
#> NULL
#> 
#> [[2]]$ccg
#> [1] "NHS South East London"
#> 
#> [[2]]$nuts
#> [1] "Bexley"
#> 
#> [[2]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[2]]$nhs_region
#> [1] "London"
#> 
#> [[2]]$ttwa
#> [1] "London"
#> 
#> [[2]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$bua
#> [1] "Bexley"
#> 
#> [[2]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[2]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[2]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[2]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[2]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[2]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[2]]$oa21
#> [1] "E00002291"
#> 
#> [[2]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[2]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[2]]$lep1
#> [1] "London"
#> 
#> [[2]]$lep2
#> NULL
#> 
#> [[2]]$codes
#> [[2]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[2]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[2]]$codes$parish
#> [1] "E43000194"
#> 
#> [[2]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[2]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[2]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[2]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[2]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[2]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[2]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[2]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[2]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[2]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[2]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[2]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$codes$bua
#> [1] "E63012138"
#> 
#> [[2]]$codes$icb
#> [1] "E54000030"
#> 
#> [[2]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[2]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[2]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[2]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[2]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[2]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[2]]$codes$ruc11
#> [1] "A1"
#> 
#> [[2]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[2]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[2]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$distance
#> [1] 46.97491
#> 
#> 
#> [[3]]
#> [[3]]$postcode
#> [1] "SE28 8NA"
#> 
#> [[3]]$quality
#> [1] 1
#> 
#> [[3]]$eastings
#> [1] 547680
#> 
#> [[3]]$northings
#> [1] 180848
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$nhs_ha
#> [1] "London"
#> 
#> [[3]]$longitude
#> [1] 0.126585
#> 
#> [[3]]$latitude
#> [1] 51.50727
#> 
#> [[3]]$european_electoral_region
#> [1] "London"
#> 
#> [[3]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[3]]$region
#> [1] "London"
#> 
#> [[3]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa
#> [1] "Bexley 001"
#> 
#> [[3]]$incode
#> [1] "8NA"
#> 
#> [[3]]$outcode
#> [1] "SE28"
#> 
#> [[3]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[3]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[3]]$senedd_constituency
#> NULL
#> 
#> [[3]]$senedd_constituency_no
#> NULL
#> 
#> [[3]]$admin_district
#> [1] "Bexley"
#> 
#> [[3]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[3]]$admin_county
#> NULL
#> 
#> [[3]]$date_of_introduction
#> [1] "198402"
#> 
#> [[3]]$date_of_termination
#> NULL
#> 
#> [[3]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[3]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[3]]$ced
#> NULL
#> 
#> [[3]]$ccg
#> [1] "NHS South East London"
#> 
#> [[3]]$nuts
#> [1] "Bexley"
#> 
#> [[3]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[3]]$nhs_region
#> [1] "London"
#> 
#> [[3]]$ttwa
#> [1] "London"
#> 
#> [[3]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[3]]$bua
#> [1] "Bexley"
#> 
#> [[3]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[3]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[3]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[3]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[3]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[3]]$oa21
#> [1] "E00002294"
#> 
#> [[3]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[3]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[3]]$lep1
#> [1] "London"
#> 
#> [[3]]$lep2
#> NULL
#> 
#> [[3]]$codes
#> [[3]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[3]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[3]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[3]]$codes$parish
#> [1] "E43000194"
#> 
#> [[3]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[3]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[3]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[3]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[3]]$codes$ced
#> [1] "E99999999"
#> 
#> [[3]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[3]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[3]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[3]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[3]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[3]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[3]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[3]]$codes$bua
#> [1] "E63012138"
#> 
#> [[3]]$codes$icb
#> [1] "E54000030"
#> 
#> [[3]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[3]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[3]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[3]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[3]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[3]]$codes$ruc11
#> [1] "A1"
#> 
#> [[3]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[3]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[3]]$codes$lep2
#> NULL
#> 
#> 
#> [[3]]$distance
#> [1] 63.40318
#> 
#> 
#> [[4]]
#> [[4]]$postcode
#> [1] "SE28 8NH"
#> 
#> [[4]]$quality
#> [1] 1
#> 
#> [[4]]$eastings
#> [1] 547715
#> 
#> [[4]]$northings
#> [1] 180780
#> 
#> [[4]]$country
#> [1] "England"
#> 
#> [[4]]$nhs_ha
#> [1] "London"
#> 
#> [[4]]$longitude
#> [1] 0.12706
#> 
#> [[4]]$latitude
#> [1] 51.50665
#> 
#> [[4]]$european_electoral_region
#> [1] "London"
#> 
#> [[4]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[4]]$region
#> [1] "London"
#> 
#> [[4]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[4]]$msoa
#> [1] "Bexley 001"
#> 
#> [[4]]$incode
#> [1] "8NH"
#> 
#> [[4]]$outcode
#> [1] "SE28"
#> 
#> [[4]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[4]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[4]]$senedd_constituency
#> NULL
#> 
#> [[4]]$senedd_constituency_no
#> NULL
#> 
#> [[4]]$admin_district
#> [1] "Bexley"
#> 
#> [[4]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[4]]$admin_county
#> NULL
#> 
#> [[4]]$date_of_introduction
#> [1] "198410"
#> 
#> [[4]]$date_of_termination
#> NULL
#> 
#> [[4]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[4]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[4]]$ced
#> NULL
#> 
#> [[4]]$ccg
#> [1] "NHS South East London"
#> 
#> [[4]]$nuts
#> [1] "Bexley"
#> 
#> [[4]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[4]]$nhs_region
#> [1] "London"
#> 
#> [[4]]$ttwa
#> [1] "London"
#> 
#> [[4]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[4]]$bua
#> [1] "Bexley"
#> 
#> [[4]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[4]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[4]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[4]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[4]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[4]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[4]]$oa21
#> [1] "E00002294"
#> 
#> [[4]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[4]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[4]]$lep1
#> [1] "London"
#> 
#> [[4]]$lep2
#> NULL
#> 
#> [[4]]$codes
#> [[4]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[4]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[4]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[4]]$codes$parish
#> [1] "E43000194"
#> 
#> [[4]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[4]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[4]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[4]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[4]]$codes$ced
#> [1] "E99999999"
#> 
#> [[4]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[4]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[4]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[4]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[4]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[4]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[4]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[4]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[4]]$codes$bua
#> [1] "E63012138"
#> 
#> [[4]]$codes$icb
#> [1] "E54000030"
#> 
#> [[4]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[4]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[4]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[4]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[4]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[4]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[4]]$codes$ruc11
#> [1] "A1"
#> 
#> [[4]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[4]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[4]]$codes$lep2
#> NULL
#> 
#> 
#> [[4]]$distance
#> [1] 78.32766
#> 
#> 
#> [[5]]
#> [[5]]$postcode
#> [1] "SE28 8NS"
#> 
#> [[5]]$quality
#> [1] 1
#> 
#> [[5]]$eastings
#> [1] 547826
#> 
#> [[5]]$northings
#> [1] 180872
#> 
#> [[5]]$country
#> [1] "England"
#> 
#> [[5]]$nhs_ha
#> [1] "London"
#> 
#> [[5]]$longitude
#> [1] 0.128697
#> 
#> [[5]]$latitude
#> [1] 51.50745
#> 
#> [[5]]$european_electoral_region
#> [1] "London"
#> 
#> [[5]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[5]]$region
#> [1] "London"
#> 
#> [[5]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[5]]$msoa
#> [1] "Bexley 001"
#> 
#> [[5]]$incode
#> [1] "8NS"
#> 
#> [[5]]$outcode
#> [1] "SE28"
#> 
#> [[5]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[5]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[5]]$senedd_constituency
#> NULL
#> 
#> [[5]]$senedd_constituency_no
#> NULL
#> 
#> [[5]]$admin_district
#> [1] "Bexley"
#> 
#> [[5]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[5]]$admin_county
#> NULL
#> 
#> [[5]]$date_of_introduction
#> [1] "198504"
#> 
#> [[5]]$date_of_termination
#> NULL
#> 
#> [[5]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[5]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[5]]$ced
#> NULL
#> 
#> [[5]]$ccg
#> [1] "NHS South East London"
#> 
#> [[5]]$nuts
#> [1] "Bexley"
#> 
#> [[5]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[5]]$nhs_region
#> [1] "London"
#> 
#> [[5]]$ttwa
#> [1] "London"
#> 
#> [[5]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[5]]$bua
#> [1] "Bexley"
#> 
#> [[5]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[5]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[5]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[5]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[5]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[5]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[5]]$oa21
#> [1] "E00002291"
#> 
#> [[5]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[5]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[5]]$lep1
#> [1] "London"
#> 
#> [[5]]$lep2
#> NULL
#> 
#> [[5]]$codes
#> [[5]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[5]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[5]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[5]]$codes$parish
#> [1] "E43000194"
#> 
#> [[5]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[5]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[5]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[5]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[5]]$codes$ced
#> [1] "E99999999"
#> 
#> [[5]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[5]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[5]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[5]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[5]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[5]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[5]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[5]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[5]]$codes$bua
#> [1] "E63012138"
#> 
#> [[5]]$codes$icb
#> [1] "E54000030"
#> 
#> [[5]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[5]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[5]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[5]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[5]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[5]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[5]]$codes$ruc11
#> [1] "A1"
#> 
#> [[5]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[5]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[5]]$codes$lep2
#> NULL
#> 
#> 
#> [[5]]$distance
#> [1] 84.48411
#> 
#> 
#> [[6]]
#> [[6]]$postcode
#> [1] "SE28 8NJ"
#> 
#> [[6]]$quality
#> [1] 1
#> 
#> [[6]]$eastings
#> [1] 547816
#> 
#> [[6]]$northings
#> [1] 180807
#> 
#> [[6]]$country
#> [1] "England"
#> 
#> [[6]]$nhs_ha
#> [1] "London"
#> 
#> [[6]]$longitude
#> [1] 0.128526
#> 
#> [[6]]$latitude
#> [1] 51.50687
#> 
#> [[6]]$european_electoral_region
#> [1] "London"
#> 
#> [[6]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[6]]$region
#> [1] "London"
#> 
#> [[6]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[6]]$msoa
#> [1] "Bexley 001"
#> 
#> [[6]]$incode
#> [1] "8NJ"
#> 
#> [[6]]$outcode
#> [1] "SE28"
#> 
#> [[6]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[6]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[6]]$senedd_constituency
#> NULL
#> 
#> [[6]]$senedd_constituency_no
#> NULL
#> 
#> [[6]]$admin_district
#> [1] "Bexley"
#> 
#> [[6]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[6]]$admin_county
#> NULL
#> 
#> [[6]]$date_of_introduction
#> [1] "198410"
#> 
#> [[6]]$date_of_termination
#> NULL
#> 
#> [[6]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[6]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[6]]$ced
#> NULL
#> 
#> [[6]]$ccg
#> [1] "NHS South East London"
#> 
#> [[6]]$nuts
#> [1] "Bexley"
#> 
#> [[6]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[6]]$nhs_region
#> [1] "London"
#> 
#> [[6]]$ttwa
#> [1] "London"
#> 
#> [[6]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[6]]$bua
#> [1] "Bexley"
#> 
#> [[6]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[6]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[6]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[6]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[6]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[6]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[6]]$oa21
#> [1] "E00002291"
#> 
#> [[6]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[6]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[6]]$lep1
#> [1] "London"
#> 
#> [[6]]$lep2
#> NULL
#> 
#> [[6]]$codes
#> [[6]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[6]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[6]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[6]]$codes$parish
#> [1] "E43000194"
#> 
#> [[6]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[6]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[6]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[6]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[6]]$codes$ced
#> [1] "E99999999"
#> 
#> [[6]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[6]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[6]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[6]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[6]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[6]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[6]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[6]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[6]]$codes$bua
#> [1] "E63012138"
#> 
#> [[6]]$codes$icb
#> [1] "E54000030"
#> 
#> [[6]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[6]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[6]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[6]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[6]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[6]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[6]]$codes$ruc11
#> [1] "A1"
#> 
#> [[6]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[6]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[6]]$codes$lep2
#> NULL
#> 
#> 
#> [[6]]$distance
#> [1] 85.73097
#> 
#> 
#> [[7]]
#> [[7]]$postcode
#> [1] "SE28 8NB"
#> 
#> [[7]]$quality
#> [1] 1
#> 
#> [[7]]$eastings
#> [1] 547676
#> 
#> [[7]]$northings
#> [1] 180923
#> 
#> [[7]]$country
#> [1] "England"
#> 
#> [[7]]$nhs_ha
#> [1] "London"
#> 
#> [[7]]$longitude
#> [1] 0.126559
#> 
#> [[7]]$latitude
#> [1] 51.50795
#> 
#> [[7]]$european_electoral_region
#> [1] "London"
#> 
#> [[7]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[7]]$region
#> [1] "London"
#> 
#> [[7]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[7]]$msoa
#> [1] "Bexley 001"
#> 
#> [[7]]$incode
#> [1] "8NB"
#> 
#> [[7]]$outcode
#> [1] "SE28"
#> 
#> [[7]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[7]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[7]]$senedd_constituency
#> NULL
#> 
#> [[7]]$senedd_constituency_no
#> NULL
#> 
#> [[7]]$admin_district
#> [1] "Bexley"
#> 
#> [[7]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[7]]$admin_county
#> NULL
#> 
#> [[7]]$date_of_introduction
#> [1] "198402"
#> 
#> [[7]]$date_of_termination
#> NULL
#> 
#> [[7]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[7]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[7]]$ced
#> NULL
#> 
#> [[7]]$ccg
#> [1] "NHS South East London"
#> 
#> [[7]]$nuts
#> [1] "Bexley"
#> 
#> [[7]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[7]]$nhs_region
#> [1] "London"
#> 
#> [[7]]$ttwa
#> [1] "London"
#> 
#> [[7]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[7]]$bua
#> [1] "Bexley"
#> 
#> [[7]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[7]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[7]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[7]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[7]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[7]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[7]]$oa21
#> [1] "E00002290"
#> 
#> [[7]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[7]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[7]]$lep1
#> [1] "London"
#> 
#> [[7]]$lep2
#> NULL
#> 
#> [[7]]$codes
#> [[7]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[7]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[7]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[7]]$codes$parish
#> [1] "E43000194"
#> 
#> [[7]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[7]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[7]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[7]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[7]]$codes$ced
#> [1] "E99999999"
#> 
#> [[7]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[7]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[7]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[7]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[7]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[7]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[7]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[7]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[7]]$codes$bua
#> [1] "E63012138"
#> 
#> [[7]]$codes$icb
#> [1] "E54000030"
#> 
#> [[7]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[7]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[7]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[7]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[7]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[7]]$codes$oa21
#> [1] "E00002290"
#> 
#> [[7]]$codes$ruc11
#> [1] "A1"
#> 
#> [[7]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[7]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[7]]$codes$lep2
#> NULL
#> 
#> 
#> [[7]]$distance
#> [1] 96.95974
#> 
#> 
#> [[8]]
#> [[8]]$postcode
#> [1] "SE28 8NN"
#> 
#> [[8]]$quality
#> [1] 1
#> 
#> [[8]]$eastings
#> [1] 547685
#> 
#> [[8]]$northings
#> [1] 180759
#> 
#> [[8]]$country
#> [1] "England"
#> 
#> [[8]]$nhs_ha
#> [1] "London"
#> 
#> [[8]]$longitude
#> [1] 0.12662
#> 
#> [[8]]$latitude
#> [1] 51.50647
#> 
#> [[8]]$european_electoral_region
#> [1] "London"
#> 
#> [[8]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[8]]$region
#> [1] "London"
#> 
#> [[8]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[8]]$msoa
#> [1] "Bexley 001"
#> 
#> [[8]]$incode
#> [1] "8NN"
#> 
#> [[8]]$outcode
#> [1] "SE28"
#> 
#> [[8]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[8]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[8]]$senedd_constituency
#> NULL
#> 
#> [[8]]$senedd_constituency_no
#> NULL
#> 
#> [[8]]$admin_district
#> [1] "Bexley"
#> 
#> [[8]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[8]]$admin_county
#> NULL
#> 
#> [[8]]$date_of_introduction
#> [1] "198410"
#> 
#> [[8]]$date_of_termination
#> NULL
#> 
#> [[8]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[8]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[8]]$ced
#> NULL
#> 
#> [[8]]$ccg
#> [1] "NHS South East London"
#> 
#> [[8]]$nuts
#> [1] "Bexley"
#> 
#> [[8]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[8]]$nhs_region
#> [1] "London"
#> 
#> [[8]]$ttwa
#> [1] "London"
#> 
#> [[8]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[8]]$bua
#> [1] "Bexley"
#> 
#> [[8]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[8]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[8]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[8]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[8]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[8]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[8]]$oa21
#> [1] "E00002294"
#> 
#> [[8]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[8]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[8]]$lep1
#> [1] "London"
#> 
#> [[8]]$lep2
#> NULL
#> 
#> [[8]]$codes
#> [[8]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[8]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[8]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[8]]$codes$parish
#> [1] "E43000194"
#> 
#> [[8]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[8]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[8]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[8]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[8]]$codes$ced
#> [1] "E99999999"
#> 
#> [[8]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[8]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[8]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[8]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[8]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[8]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[8]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[8]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[8]]$codes$bua
#> [1] "E63012138"
#> 
#> [[8]]$codes$icb
#> [1] "E54000030"
#> 
#> [[8]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[8]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[8]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[8]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[8]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[8]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[8]]$codes$ruc11
#> [1] "A1"
#> 
#> [[8]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[8]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[8]]$codes$lep2
#> NULL
#> 
#> 
#> [[8]]$distance
#> [1] 110.4839
#> 
#> 
#> [[9]]
#> [[9]]$postcode
#> [1] "SE28 8NF"
#> 
#> [[9]]$quality
#> [1] 1
#> 
#> [[9]]$eastings
#> [1] 547711
#> 
#> [[9]]$northings
#> [1] 180960
#> 
#> [[9]]$country
#> [1] "England"
#> 
#> [[9]]$nhs_ha
#> [1] "London"
#> 
#> [[9]]$longitude
#> [1] 0.127078
#> 
#> [[9]]$latitude
#> [1] 51.50827
#> 
#> [[9]]$european_electoral_region
#> [1] "London"
#> 
#> [[9]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[9]]$region
#> [1] "London"
#> 
#> [[9]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[9]]$msoa
#> [1] "Bexley 001"
#> 
#> [[9]]$incode
#> [1] "8NF"
#> 
#> [[9]]$outcode
#> [1] "SE28"
#> 
#> [[9]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[9]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[9]]$senedd_constituency
#> NULL
#> 
#> [[9]]$senedd_constituency_no
#> NULL
#> 
#> [[9]]$admin_district
#> [1] "Bexley"
#> 
#> [[9]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[9]]$admin_county
#> NULL
#> 
#> [[9]]$date_of_introduction
#> [1] "198402"
#> 
#> [[9]]$date_of_termination
#> NULL
#> 
#> [[9]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[9]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[9]]$ced
#> NULL
#> 
#> [[9]]$ccg
#> [1] "NHS South East London"
#> 
#> [[9]]$nuts
#> [1] "Bexley"
#> 
#> [[9]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[9]]$nhs_region
#> [1] "London"
#> 
#> [[9]]$ttwa
#> [1] "London"
#> 
#> [[9]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[9]]$bua
#> [1] "Bexley"
#> 
#> [[9]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[9]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[9]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[9]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[9]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[9]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[9]]$oa21
#> [1] "E00002290"
#> 
#> [[9]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[9]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[9]]$lep1
#> [1] "London"
#> 
#> [[9]]$lep2
#> NULL
#> 
#> [[9]]$codes
#> [[9]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[9]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[9]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[9]]$codes$parish
#> [1] "E43000194"
#> 
#> [[9]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[9]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[9]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[9]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[9]]$codes$ced
#> [1] "E99999999"
#> 
#> [[9]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[9]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[9]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[9]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[9]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[9]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[9]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[9]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[9]]$codes$bua
#> [1] "E63012138"
#> 
#> [[9]]$codes$icb
#> [1] "E54000030"
#> 
#> [[9]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[9]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[9]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[9]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[9]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[9]]$codes$oa21
#> [1] "E00002290"
#> 
#> [[9]]$codes$ruc11
#> [1] "A1"
#> 
#> [[9]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[9]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[9]]$codes$lep2
#> NULL
#> 
#> 
#> [[9]]$distance
#> [1] 111.7435
#> 
#> 
#> [[10]]
#> [[10]]$postcode
#> [1] "SE28 8NT"
#> 
#> [[10]]$quality
#> [1] 1
#> 
#> [[10]]$eastings
#> [1] 547852
#> 
#> [[10]]$northings
#> [1] 180890
#> 
#> [[10]]$country
#> [1] "England"
#> 
#> [[10]]$nhs_ha
#> [1] "London"
#> 
#> [[10]]$longitude
#> [1] 0.129079
#> 
#> [[10]]$latitude
#> [1] 51.5076
#> 
#> [[10]]$european_electoral_region
#> [1] "London"
#> 
#> [[10]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[10]]$region
#> [1] "London"
#> 
#> [[10]]$lsoa
#> [1] "Bexley 001C"
#> 
#> [[10]]$msoa
#> [1] "Bexley 001"
#> 
#> [[10]]$incode
#> [1] "8NT"
#> 
#> [[10]]$outcode
#> [1] "SE28"
#> 
#> [[10]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[10]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[10]]$senedd_constituency
#> NULL
#> 
#> [[10]]$senedd_constituency_no
#> NULL
#> 
#> [[10]]$admin_district
#> [1] "Bexley"
#> 
#> [[10]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[10]]$admin_county
#> NULL
#> 
#> [[10]]$date_of_introduction
#> [1] "198504"
#> 
#> [[10]]$date_of_termination
#> NULL
#> 
#> [[10]]$index_of_multiple_deprivation
#> [1] 13661
#> 
#> [[10]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[10]]$ced
#> NULL
#> 
#> [[10]]$ccg
#> [1] "NHS South East London"
#> 
#> [[10]]$nuts
#> [1] "Bexley"
#> 
#> [[10]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[10]]$nhs_region
#> [1] "London"
#> 
#> [[10]]$ttwa
#> [1] "London"
#> 
#> [[10]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[10]]$bua
#> [1] "Bexley"
#> 
#> [[10]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[10]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[10]]$lsoa11
#> [1] "Bexley 001C"
#> 
#> [[10]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[10]]$lsoa21
#> [1] "Bexley 001C"
#> 
#> [[10]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[10]]$oa21
#> [1] "E00002291"
#> 
#> [[10]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[10]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[10]]$lep1
#> [1] "London"
#> 
#> [[10]]$lep2
#> NULL
#> 
#> [[10]]$codes
#> [[10]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[10]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[10]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[10]]$codes$parish
#> [1] "E43000194"
#> 
#> [[10]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[10]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[10]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[10]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[10]]$codes$ced
#> [1] "E99999999"
#> 
#> [[10]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[10]]$codes$lsoa
#> [1] "E01000468"
#> 
#> [[10]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[10]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[10]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[10]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[10]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[10]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[10]]$codes$bua
#> [1] "E63012138"
#> 
#> [[10]]$codes$icb
#> [1] "E54000030"
#> 
#> [[10]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[10]]$codes$lsoa11
#> [1] "E01000468"
#> 
#> [[10]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[10]]$codes$lsoa21
#> [1] "E01000468"
#> 
#> [[10]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[10]]$codes$oa21
#> [1] "E00002291"
#> 
#> [[10]]$codes$ruc11
#> [1] "A1"
#> 
#> [[10]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[10]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[10]]$codes$lep2
#> NULL
#> 
#> 
#> [[10]]$distance
#> [1] 114.3901
#> 
#> 
#> [[11]]
#> [[11]]$postcode
#> [1] "SE28 8NL"
#> 
#> [[11]]$quality
#> [1] 1
#> 
#> [[11]]$eastings
#> [1] 547792
#> 
#> [[11]]$northings
#> [1] 180749
#> 
#> [[11]]$country
#> [1] "England"
#> 
#> [[11]]$nhs_ha
#> [1] "London"
#> 
#> [[11]]$longitude
#> [1] 0.128156
#> 
#> [[11]]$latitude
#> [1] 51.50635
#> 
#> [[11]]$european_electoral_region
#> [1] "London"
#> 
#> [[11]]$primary_care_trust
#> [1] "Bexley"
#> 
#> [[11]]$region
#> [1] "London"
#> 
#> [[11]]$lsoa
#> [1] "Bexley 001D"
#> 
#> [[11]]$msoa
#> [1] "Bexley 001"
#> 
#> [[11]]$incode
#> [1] "8NL"
#> 
#> [[11]]$outcode
#> [1] "SE28"
#> 
#> [[11]]$parliamentary_constituency
#> [1] "Erith and Thamesmead"
#> 
#> [[11]]$parliamentary_constituency_2024
#> [1] "Erith and Thamesmead"
#> 
#> [[11]]$senedd_constituency
#> NULL
#> 
#> [[11]]$senedd_constituency_no
#> NULL
#> 
#> [[11]]$admin_district
#> [1] "Bexley"
#> 
#> [[11]]$parish
#> [1] "Bexley, unparished area"
#> 
#> [[11]]$admin_county
#> NULL
#> 
#> [[11]]$date_of_introduction
#> [1] "198410"
#> 
#> [[11]]$date_of_termination
#> NULL
#> 
#> [[11]]$index_of_multiple_deprivation
#> [1] 14434
#> 
#> [[11]]$admin_ward
#> [1] "Thamesmead East"
#> 
#> [[11]]$ced
#> NULL
#> 
#> [[11]]$ccg
#> [1] "NHS South East London"
#> 
#> [[11]]$nuts
#> [1] "Bexley"
#> 
#> [[11]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[11]]$nhs_region
#> [1] "London"
#> 
#> [[11]]$ttwa
#> [1] "London"
#> 
#> [[11]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[11]]$bua
#> [1] "Bexley"
#> 
#> [[11]]$icb
#> [1] "NHS South East London Integrated Care Board"
#> 
#> [[11]]$cancer_alliance
#> [1] "South East London"
#> 
#> [[11]]$lsoa11
#> [1] "Bexley 001D"
#> 
#> [[11]]$msoa11
#> [1] "Bexley 001"
#> 
#> [[11]]$lsoa21
#> [1] "Bexley 001D"
#> 
#> [[11]]$msoa21
#> [1] "Bexley 001"
#> 
#> [[11]]$oa21
#> [1] "E00002294"
#> 
#> [[11]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[11]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[11]]$lep1
#> [1] "London"
#> 
#> [[11]]$lep2
#> NULL
#> 
#> [[11]]$codes
#> [[11]]$codes$admin_district
#> [1] "E09000004"
#> 
#> [[11]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[11]]$codes$admin_ward
#> [1] "E05011232"
#> 
#> [[11]]$codes$parish
#> [1] "E43000194"
#> 
#> [[11]]$codes$parliamentary_constituency
#> [1] "E14001229"
#> 
#> [[11]]$codes$parliamentary_constituency_2024
#> [1] "E14001229"
#> 
#> [[11]]$codes$ccg
#> [1] "E38000244"
#> 
#> [[11]]$codes$ccg_id
#> [1] "72Q"
#> 
#> [[11]]$codes$ced
#> [1] "E99999999"
#> 
#> [[11]]$codes$nuts
#> [1] "TLI51"
#> 
#> [[11]]$codes$lsoa
#> [1] "E01000469"
#> 
#> [[11]]$codes$msoa
#> [1] "E02000065"
#> 
#> [[11]]$codes$lau2
#> [1] "E09000004"
#> 
#> [[11]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[11]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[11]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[11]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[11]]$codes$bua
#> [1] "E63012138"
#> 
#> [[11]]$codes$icb
#> [1] "E54000030"
#> 
#> [[11]]$codes$cancer_alliance
#> [1] "E56000010"
#> 
#> [[11]]$codes$lsoa11
#> [1] "E01000469"
#> 
#> [[11]]$codes$msoa11
#> [1] "E02000065"
#> 
#> [[11]]$codes$lsoa21
#> [1] "E01000469"
#> 
#> [[11]]$codes$msoa21
#> [1] "E02000065"
#> 
#> [[11]]$codes$oa21
#> [1] "E00002294"
#> 
#> [[11]]$codes$ruc11
#> [1] "A1"
#> 
#> [[11]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[11]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[11]]$codes$lep2
#> NULL
#> 
#> 
#> [[11]]$distance
#> [1] 114.6725
#> 
#> 
# }
```
