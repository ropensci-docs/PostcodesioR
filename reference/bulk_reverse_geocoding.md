# Bulk reverse geocoding

Returns nearest postcodes for a given longitude and latitude. Accepts up
to 100 geolocations.

## Usage

``` r
bulk_reverse_geocoding(geolocations)
```

## Arguments

- geolocations:

  A list containing an array of objects to geolocate. At least two
  elements needed.

## Value

A list with the geocoded data.

## Details

This method requires a JSON object containing an array of geolocation
objects to be POSTed. Each geolocation object accepts an optional radius
(meters) and limit argument. Both default to 100m and 10 respectively.
It also accepts a wideSearch argument.

## See also

[`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md)
for documentation.

## Examples

``` r

# \donttest{
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

bulk_reverse_geocoding(geolocations_list)
#> [[1]]
#> [[1]]$query
#> [[1]]$query$longitude
#> [1] -3.158077
#> 
#> [[1]]$query$latitude
#> [1] 51.47999
#> 
#> 
#> [[1]]$result
#> [[1]]$result[[1]]
#> [[1]]$result[[1]]$postcode
#> [1] "CF24 2BT"
#> 
#> [[1]]$result[[1]]$quality
#> [1] 1
#> 
#> [[1]]$result[[1]]$eastings
#> [1] 319675
#> 
#> [[1]]$result[[1]]$northings
#> [1] 176305
#> 
#> [[1]]$result[[1]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[1]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[1]]$longitude
#> [1] -3.158085
#> 
#> [[1]]$result[[1]]$latitude
#> [1] 51.47998
#> 
#> [[1]]$result[[1]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[1]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[1]]$region
#> NULL
#> 
#> [[1]]$result[[1]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[1]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[1]]$incode
#> [1] "2BT"
#> 
#> [[1]]$result[[1]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[1]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[1]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[1]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[1]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[1]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[1]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[1]]$admin_county
#> NULL
#> 
#> [[1]]$result[[1]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[1]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[1]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[1]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[1]]$ced
#> NULL
#> 
#> [[1]]$result[[1]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[1]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[1]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[1]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[1]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[1]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[1]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[1]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[1]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[1]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[1]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[1]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[1]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[1]]$oa21
#> [1] "W00009646"
#> 
#> [[1]]$result[[1]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[1]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[1]]$lep1
#> NULL
#> 
#> [[1]]$result[[1]]$lep2
#> NULL
#> 
#> [[1]]$result[[1]]$codes
#> [[1]]$result[[1]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[1]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[1]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[1]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[1]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[1]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[1]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[1]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[1]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[1]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[1]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[1]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[1]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[1]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[1]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[1]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[1]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[1]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[1]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[1]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[1]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[1]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[1]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[1]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[1]]$codes$oa21
#> [1] "W00009646"
#> 
#> [[1]]$result[[1]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[1]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[1]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[1]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[1]]$distance
#> [1] 1.54699
#> 
#> 
#> [[1]]$result[[2]]
#> [[1]]$result[[2]]$postcode
#> [1] "CF24 2ED"
#> 
#> [[1]]$result[[2]]$quality
#> [1] 1
#> 
#> [[1]]$result[[2]]$eastings
#> [1] 319631
#> 
#> [[1]]$result[[2]]$northings
#> [1] 176277
#> 
#> [[1]]$result[[2]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[2]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[2]]$longitude
#> [1] -3.158712
#> 
#> [[1]]$result[[2]]$latitude
#> [1] 51.47972
#> 
#> [[1]]$result[[2]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[2]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[2]]$region
#> NULL
#> 
#> [[1]]$result[[2]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[2]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[2]]$incode
#> [1] "2ED"
#> 
#> [[1]]$result[[2]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[2]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[2]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[2]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[2]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[2]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[2]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[2]]$admin_county
#> NULL
#> 
#> [[1]]$result[[2]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[2]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[2]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[2]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[2]]$ced
#> NULL
#> 
#> [[1]]$result[[2]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[2]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[2]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[2]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[2]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[2]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[2]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[2]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[2]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[2]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[2]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[2]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[2]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[2]]$oa21
#> [1] "W00009646"
#> 
#> [[1]]$result[[2]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[2]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[2]]$lep1
#> NULL
#> 
#> [[1]]$result[[2]]$lep2
#> NULL
#> 
#> [[1]]$result[[2]]$codes
#> [[1]]$result[[2]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[2]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[2]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[2]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[2]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[2]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[2]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[2]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[2]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[2]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[2]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[2]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[2]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[2]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[2]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[2]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[2]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[2]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[2]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[2]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[2]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[2]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[2]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[2]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[2]]$codes$oa21
#> [1] "W00009646"
#> 
#> [[1]]$result[[2]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[2]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[2]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[2]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[2]]$distance
#> [1] 53.29467
#> 
#> 
#> [[1]]$result[[3]]
#> [[1]]$result[[3]]$postcode
#> [1] "CF24 2AA"
#> 
#> [[1]]$result[[3]]$quality
#> [1] 1
#> 
#> [[1]]$result[[3]]$eastings
#> [1] 319607
#> 
#> [[1]]$result[[3]]$northings
#> [1] 176332
#> 
#> [[1]]$result[[3]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[3]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[3]]$longitude
#> [1] -3.15907
#> 
#> [[1]]$result[[3]]$latitude
#> [1] 51.48021
#> 
#> [[1]]$result[[3]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[3]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[3]]$region
#> NULL
#> 
#> [[1]]$result[[3]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[3]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[3]]$incode
#> [1] "2AA"
#> 
#> [[1]]$result[[3]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[3]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[3]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[3]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[3]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[3]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[3]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[3]]$admin_county
#> NULL
#> 
#> [[1]]$result[[3]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[3]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[3]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[3]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[3]]$ced
#> NULL
#> 
#> [[1]]$result[[3]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[3]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[3]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[3]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[3]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[3]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[3]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[3]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[3]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[3]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[3]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[3]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[3]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[3]]$oa21
#> [1] "W00009644"
#> 
#> [[1]]$result[[3]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[3]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[3]]$lep1
#> NULL
#> 
#> [[1]]$result[[3]]$lep2
#> NULL
#> 
#> [[1]]$result[[3]]$codes
#> [[1]]$result[[3]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[3]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[3]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[3]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[3]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[3]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[3]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[3]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[3]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[3]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[3]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[3]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[3]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[3]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[3]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[3]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[3]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[3]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[3]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[3]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[3]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[3]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[3]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[3]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[3]]$codes$oa21
#> [1] "W00009644"
#> 
#> [[1]]$result[[3]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[3]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[3]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[3]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[3]]$distance
#> [1] 72.96494
#> 
#> 
#> [[1]]$result[[4]]
#> [[1]]$result[[4]]$postcode
#> [1] "CF24 5NW"
#> 
#> [[1]]$result[[4]]$quality
#> [1] 1
#> 
#> [[1]]$result[[4]]$eastings
#> [1] 319646
#> 
#> [[1]]$result[[4]]$northings
#> [1] 176237
#> 
#> [[1]]$result[[4]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[4]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[4]]$longitude
#> [1] -3.158487
#> 
#> [[1]]$result[[4]]$latitude
#> [1] 51.47936
#> 
#> [[1]]$result[[4]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[4]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[4]]$region
#> NULL
#> 
#> [[1]]$result[[4]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[4]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[4]]$incode
#> [1] "5NW"
#> 
#> [[1]]$result[[4]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[4]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[4]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[4]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[4]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[4]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[4]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[4]]$admin_county
#> NULL
#> 
#> [[1]]$result[[4]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[4]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[4]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[4]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[4]]$ced
#> NULL
#> 
#> [[1]]$result[[4]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[4]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[4]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[4]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[4]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[4]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[4]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[4]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[4]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[4]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[4]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[4]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[4]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[4]]$oa21
#> [1] "W00009646"
#> 
#> [[1]]$result[[4]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[4]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[4]]$lep1
#> NULL
#> 
#> [[1]]$result[[4]]$lep2
#> NULL
#> 
#> [[1]]$result[[4]]$codes
#> [[1]]$result[[4]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[4]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[4]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[4]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[4]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[4]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[4]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[4]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[4]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[4]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[4]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[4]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[4]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[4]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[4]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[4]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[4]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[4]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[4]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[4]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[4]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[4]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[4]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[4]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[4]]$codes$oa21
#> [1] "W00009646"
#> 
#> [[1]]$result[[4]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[4]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[4]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[4]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[4]]$distance
#> [1] 75.48348
#> 
#> 
#> [[1]]$result[[5]]
#> [[1]]$result[[5]]$postcode
#> [1] "CF24 2AJ"
#> 
#> [[1]]$result[[5]]$quality
#> [1] 1
#> 
#> [[1]]$result[[5]]$eastings
#> [1] 319645
#> 
#> [[1]]$result[[5]]$northings
#> [1] 176384
#> 
#> [[1]]$result[[5]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[5]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[5]]$longitude
#> [1] -3.158535
#> 
#> [[1]]$result[[5]]$latitude
#> [1] 51.48068
#> 
#> [[1]]$result[[5]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[5]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[5]]$region
#> NULL
#> 
#> [[1]]$result[[5]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[5]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[5]]$incode
#> [1] "2AJ"
#> 
#> [[1]]$result[[5]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[5]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[5]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[5]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[5]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[5]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[5]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[5]]$admin_county
#> NULL
#> 
#> [[1]]$result[[5]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[5]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[5]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[5]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[5]]$ced
#> NULL
#> 
#> [[1]]$result[[5]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[5]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[5]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[5]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[5]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[5]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[5]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[5]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[5]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[5]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[5]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[5]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[5]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[5]]$oa21
#> [1] "W00009644"
#> 
#> [[1]]$result[[5]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[5]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[5]]$lep1
#> NULL
#> 
#> [[1]]$result[[5]]$lep2
#> NULL
#> 
#> [[1]]$result[[5]]$codes
#> [[1]]$result[[5]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[5]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[5]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[5]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[5]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[5]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[5]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[5]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[5]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[5]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[5]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[5]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[5]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[5]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[5]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[5]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[5]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[5]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[5]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[5]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[5]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[5]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[5]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[5]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[5]]$codes$oa21
#> [1] "W00009644"
#> 
#> [[1]]$result[[5]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[5]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[5]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[5]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[5]]$distance
#> [1] 83.31546
#> 
#> 
#> [[1]]$result[[6]]
#> [[1]]$result[[6]]$postcode
#> [1] "CF24 2AH"
#> 
#> [[1]]$result[[6]]$quality
#> [1] 1
#> 
#> [[1]]$result[[6]]$eastings
#> [1] 319618
#> 
#> [[1]]$result[[6]]$northings
#> [1] 176370
#> 
#> [[1]]$result[[6]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[6]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[6]]$longitude
#> [1] -3.158921
#> 
#> [[1]]$result[[6]]$latitude
#> [1] 51.48055
#> 
#> [[1]]$result[[6]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[6]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[6]]$region
#> NULL
#> 
#> [[1]]$result[[6]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[6]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[6]]$incode
#> [1] "2AH"
#> 
#> [[1]]$result[[6]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[6]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[6]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[6]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[6]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[6]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[6]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[6]]$admin_county
#> NULL
#> 
#> [[1]]$result[[6]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[6]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[6]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[6]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[6]]$ced
#> NULL
#> 
#> [[1]]$result[[6]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[6]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[6]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[6]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[6]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[6]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[6]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[6]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[6]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[6]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[6]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[6]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[6]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[6]]$oa21
#> [1] "W00009644"
#> 
#> [[1]]$result[[6]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[6]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[6]]$lep1
#> NULL
#> 
#> [[1]]$result[[6]]$lep2
#> NULL
#> 
#> [[1]]$result[[6]]$codes
#> [[1]]$result[[6]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[6]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[6]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[6]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[6]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[6]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[6]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[6]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[6]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[6]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[6]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[6]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[6]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[6]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[6]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[6]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[6]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[6]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[6]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[6]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[6]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[6]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[6]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[6]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[6]]$codes$oa21
#> [1] "W00009644"
#> 
#> [[1]]$result[[6]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[6]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[6]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[6]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[6]]$distance
#> [1] 85.62601
#> 
#> 
#> [[1]]$result[[7]]
#> [[1]]$result[[7]]$postcode
#> [1] "CF24 2DZ"
#> 
#> [[1]]$result[[7]]$quality
#> [1] 1
#> 
#> [[1]]$result[[7]]$eastings
#> [1] 319764
#> 
#> [[1]]$result[[7]]$northings
#> [1] 176318
#> 
#> [[1]]$result[[7]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[7]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[7]]$longitude
#> [1] -3.156807
#> 
#> [[1]]$result[[7]]$latitude
#> [1] 51.48011
#> 
#> [[1]]$result[[7]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[7]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[7]]$region
#> NULL
#> 
#> [[1]]$result[[7]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[7]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[7]]$incode
#> [1] "2DZ"
#> 
#> [[1]]$result[[7]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[7]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[7]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[7]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[7]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[7]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[7]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[7]]$admin_county
#> NULL
#> 
#> [[1]]$result[[7]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[7]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[7]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[7]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[7]]$ced
#> NULL
#> 
#> [[1]]$result[[7]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[7]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[7]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[7]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[7]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[7]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[7]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[7]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[7]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[7]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[7]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[7]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[7]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[7]]$oa21
#> [1] "W00009646"
#> 
#> [[1]]$result[[7]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[7]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[7]]$lep1
#> NULL
#> 
#> [[1]]$result[[7]]$lep2
#> NULL
#> 
#> [[1]]$result[[7]]$codes
#> [[1]]$result[[7]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[7]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[7]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[7]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[7]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[7]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[7]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[7]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[7]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[7]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[7]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[7]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[7]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[7]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[7]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[7]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[7]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[7]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[7]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[7]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[7]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[7]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[7]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[7]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[7]]$codes$oa21
#> [1] "W00009646"
#> 
#> [[1]]$result[[7]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[7]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[7]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[7]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[7]]$distance
#> [1] 88.90984
#> 
#> 
#> [[1]]$result[[8]]
#> [[1]]$result[[8]]$postcode
#> [1] "CF24 2AB"
#> 
#> [[1]]$result[[8]]$quality
#> [1] 1
#> 
#> [[1]]$result[[8]]$eastings
#> [1] 319736
#> 
#> [[1]]$result[[8]]$northings
#> [1] 176375
#> 
#> [[1]]$result[[8]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[8]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[8]]$longitude
#> [1] -3.157223
#> 
#> [[1]]$result[[8]]$latitude
#> [1] 51.48062
#> 
#> [[1]]$result[[8]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[8]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[8]]$region
#> NULL
#> 
#> [[1]]$result[[8]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[8]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[8]]$incode
#> [1] "2AB"
#> 
#> [[1]]$result[[8]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[8]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[8]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[8]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[8]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[8]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[8]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[8]]$admin_county
#> NULL
#> 
#> [[1]]$result[[8]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[8]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[8]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[8]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[8]]$ced
#> NULL
#> 
#> [[1]]$result[[8]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[8]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[8]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[8]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[8]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[8]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[8]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[8]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[8]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[8]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[8]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[8]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[8]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[8]]$oa21
#> [1] "W00009643"
#> 
#> [[1]]$result[[8]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[8]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[8]]$lep1
#> NULL
#> 
#> [[1]]$result[[8]]$lep2
#> NULL
#> 
#> [[1]]$result[[8]]$codes
#> [[1]]$result[[8]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[8]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[8]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[8]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[8]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[8]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[8]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[8]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[8]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[8]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[8]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[8]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[8]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[8]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[8]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[8]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[8]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[8]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[8]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[8]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[8]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[8]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[8]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[8]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[8]]$codes$oa21
#> [1] "W00009643"
#> 
#> [[1]]$result[[8]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[8]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[8]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[8]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[8]]$distance
#> [1] 91.26305
#> 
#> 
#> [[1]]$result[[9]]
#> [[1]]$result[[9]]$postcode
#> [1] "CF24 2AL"
#> 
#> [[1]]$result[[9]]$quality
#> [1] 1
#> 
#> [[1]]$result[[9]]$eastings
#> [1] 319672
#> 
#> [[1]]$result[[9]]$northings
#> [1] 176400
#> 
#> [[1]]$result[[9]]$country
#> [1] "Wales"
#> 
#> [[1]]$result[[9]]$nhs_ha
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[9]]$longitude
#> [1] -3.15815
#> 
#> [[1]]$result[[9]]$latitude
#> [1] 51.48083
#> 
#> [[1]]$result[[9]]$european_electoral_region
#> [1] "Wales"
#> 
#> [[1]]$result[[9]]$primary_care_trust
#> [1] "Cardiff and Vale University Health Board"
#> 
#> [[1]]$result[[9]]$region
#> NULL
#> 
#> [[1]]$result[[9]]$lsoa
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[9]]$msoa
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[9]]$incode
#> [1] "2AL"
#> 
#> [[1]]$result[[9]]$outcode
#> [1] "CF24"
#> 
#> [[1]]$result[[9]]$parliamentary_constituency
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[9]]$parliamentary_constituency_2024
#> [1] "Cardiff South and Penarth"
#> 
#> [[1]]$result[[9]]$senedd_constituency
#> [1] "Caerdydd Penarth"
#> 
#> [[1]]$result[[9]]$senedd_constituency_no
#> [1] 14
#> 
#> [[1]]$result[[9]]$admin_district
#> [1] "Cardiff"
#> 
#> [[1]]$result[[9]]$parish
#> [1] "Splott"
#> 
#> [[1]]$result[[9]]$admin_county
#> NULL
#> 
#> [[1]]$result[[9]]$date_of_introduction
#> [1] "199906"
#> 
#> [[1]]$result[[9]]$date_of_termination
#> NULL
#> 
#> [[1]]$result[[9]]$index_of_multiple_deprivation
#> [1] 12
#> 
#> [[1]]$result[[9]]$admin_ward
#> [1] "Splott"
#> 
#> [[1]]$result[[9]]$ced
#> NULL
#> 
#> [[1]]$result[[9]]$ccg
#> [1] "Cardiff and Vale University"
#> 
#> [[1]]$result[[9]]$nuts
#> [1] "Cardiff"
#> 
#> [[1]]$result[[9]]$pfa
#> [1] "South Wales"
#> 
#> [[1]]$result[[9]]$nhs_region
#> NULL
#> 
#> [[1]]$result[[9]]$ttwa
#> [1] "Cardiff"
#> 
#> [[1]]$result[[9]]$national_park
#> [1] "Wales (non-National Park)"
#> 
#> [[1]]$result[[9]]$bua
#> [1] "Cardiff"
#> 
#> [[1]]$result[[9]]$icb
#> [1] "Wales"
#> 
#> [[1]]$result[[9]]$cancer_alliance
#> NULL
#> 
#> [[1]]$result[[9]]$lsoa11
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[9]]$msoa11
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[9]]$lsoa21
#> [1] "Cardiff 038D"
#> 
#> [[1]]$result[[9]]$msoa21
#> [1] "Cardiff 038"
#> 
#> [[1]]$result[[9]]$oa21
#> [1] "W00009644"
#> 
#> [[1]]$result[[9]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[1]]$result[[9]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$result[[9]]$lep1
#> NULL
#> 
#> [[1]]$result[[9]]$lep2
#> NULL
#> 
#> [[1]]$result[[9]]$codes
#> [[1]]$result[[9]]$codes$admin_district
#> [1] "W06000015"
#> 
#> [[1]]$result[[9]]$codes$admin_county
#> [1] "W99999999"
#> 
#> [[1]]$result[[9]]$codes$admin_ward
#> [1] "W05001295"
#> 
#> [[1]]$result[[9]]$codes$parish
#> [1] "W04001005"
#> 
#> [[1]]$result[[9]]$codes$parliamentary_constituency
#> [1] "W07000091"
#> 
#> [[1]]$result[[9]]$codes$parliamentary_constituency_2024
#> [1] "W07000091"
#> 
#> [[1]]$result[[9]]$codes$ccg
#> [1] "W11000029"
#> 
#> [[1]]$result[[9]]$codes$ccg_id
#> [1] "7A4"
#> 
#> [[1]]$result[[9]]$codes$ced
#> [1] "W99999999"
#> 
#> [[1]]$result[[9]]$codes$nuts
#> [1] "TLL52"
#> 
#> [[1]]$result[[9]]$codes$lsoa
#> [1] "W01001874"
#> 
#> [[1]]$result[[9]]$codes$msoa
#> [1] "W02000404"
#> 
#> [[1]]$result[[9]]$codes$lau2
#> [1] "W06000015"
#> 
#> [[1]]$result[[9]]$codes$pfa
#> [1] "W15000003"
#> 
#> [[1]]$result[[9]]$codes$nhs_region
#> [1] "W99999999"
#> 
#> [[1]]$result[[9]]$codes$ttwa
#> [1] "W22000024"
#> 
#> [[1]]$result[[9]]$codes$national_park
#> [1] "W31000001"
#> 
#> [[1]]$result[[9]]$codes$bua
#> [1] "W45001208"
#> 
#> [[1]]$result[[9]]$codes$icb
#> [1] "W99999999"
#> 
#> [[1]]$result[[9]]$codes$cancer_alliance
#> [1] "W99999999"
#> 
#> [[1]]$result[[9]]$codes$lsoa11
#> [1] "W01001874"
#> 
#> [[1]]$result[[9]]$codes$msoa11
#> [1] "W02000404"
#> 
#> [[1]]$result[[9]]$codes$lsoa21
#> [1] "W01001874"
#> 
#> [[1]]$result[[9]]$codes$msoa21
#> [1] "W02000404"
#> 
#> [[1]]$result[[9]]$codes$oa21
#> [1] "W00009644"
#> 
#> [[1]]$result[[9]]$codes$ruc11
#> [1] "C1"
#> 
#> [[1]]$result[[9]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$result[[9]]$codes$lep1
#> [1] "W99999999"
#> 
#> [[1]]$result[[9]]$codes$lep2
#> NULL
#> 
#> 
#> [[1]]$result[[9]]$distance
#> [1] 93.53244
#> 
#> 
#> 
#> 
#> [[2]]
#> [[2]]$query
#> [[2]]$query$longitude
#> [1] -1.129358
#> 
#> [[2]]$query$latitude
#> [1] 50.71864
#> 
#> [[2]]$query$limit
#> [1] 100
#> 
#> [[2]]$query$radius
#> [1] 500
#> 
#> 
#> [[2]]$result
#> [[2]]$result[[1]]
#> [[2]]$result[[1]]$postcode
#> [1] "PO33 1PS"
#> 
#> [[2]]$result[[1]]$quality
#> [1] 1
#> 
#> [[2]]$result[[1]]$eastings
#> [1] 461564
#> 
#> [[2]]$result[[1]]$northings
#> [1] 91388
#> 
#> [[2]]$result[[1]]$country
#> [1] "England"
#> 
#> [[2]]$result[[1]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[1]]$longitude
#> [1] -1.129272
#> 
#> [[2]]$result[[1]]$latitude
#> [1] 50.71886
#> 
#> [[2]]$result[[1]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[1]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[1]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[1]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[1]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[1]]$incode
#> [1] "1PS"
#> 
#> [[2]]$result[[1]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[1]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[1]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[1]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[1]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[1]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[1]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[1]]$admin_county
#> NULL
#> 
#> [[2]]$result[[1]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[1]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[1]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[1]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[1]]$ced
#> NULL
#> 
#> [[2]]$result[[1]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[1]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[1]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[1]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[1]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[1]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[1]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[1]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[1]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[1]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[1]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[1]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[1]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[1]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[1]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[1]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[1]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[1]]$lep2
#> NULL
#> 
#> [[2]]$result[[1]]$codes
#> [[2]]$result[[1]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[1]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[1]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[1]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[1]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[1]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[1]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[1]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[1]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[1]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[1]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[1]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[1]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[1]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[1]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[1]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[1]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[1]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[1]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[1]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[1]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[1]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[1]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[1]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[1]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[1]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[1]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[1]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[1]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[1]]$distance
#> [1] 25.23411
#> 
#> 
#> [[2]]$result[[2]]
#> [[2]]$result[[2]]$postcode
#> [1] "PO33 1PT"
#> 
#> [[2]]$result[[2]]$quality
#> [1] 1
#> 
#> [[2]]$result[[2]]$eastings
#> [1] 461622
#> 
#> [[2]]$result[[2]]$northings
#> [1] 91356
#> 
#> [[2]]$result[[2]]$country
#> [1] "England"
#> 
#> [[2]]$result[[2]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[2]]$longitude
#> [1] -1.128455
#> 
#> [[2]]$result[[2]]$latitude
#> [1] 50.71856
#> 
#> [[2]]$result[[2]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[2]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[2]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[2]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[2]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[2]]$incode
#> [1] "1PT"
#> 
#> [[2]]$result[[2]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[2]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[2]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[2]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[2]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[2]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[2]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[2]]$admin_county
#> NULL
#> 
#> [[2]]$result[[2]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[2]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[2]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[2]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[2]]$ced
#> NULL
#> 
#> [[2]]$result[[2]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[2]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[2]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[2]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[2]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[2]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[2]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[2]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[2]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[2]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[2]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[2]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[2]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[2]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[2]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[2]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[2]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[2]]$lep2
#> NULL
#> 
#> [[2]]$result[[2]]$codes
#> [[2]]$result[[2]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[2]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[2]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[2]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[2]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[2]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[2]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[2]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[2]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[2]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[2]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[2]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[2]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[2]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[2]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[2]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[2]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[2]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[2]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[2]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[2]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[2]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[2]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[2]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[2]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[2]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[2]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[2]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[2]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[2]]$distance
#> [1] 64.10005
#> 
#> 
#> [[2]]$result[[3]]
#> [[2]]$result[[3]]$postcode
#> [1] "PO33 1PX"
#> 
#> [[2]]$result[[3]]$quality
#> [1] 1
#> 
#> [[2]]$result[[3]]$eastings
#> [1] 461716
#> 
#> [[2]]$result[[3]]$northings
#> [1] 91281
#> 
#> [[2]]$result[[3]]$country
#> [1] "England"
#> 
#> [[2]]$result[[3]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[3]]$longitude
#> [1] -1.127137
#> 
#> [[2]]$result[[3]]$latitude
#> [1] 50.71788
#> 
#> [[2]]$result[[3]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[3]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[3]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[3]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[3]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[3]]$incode
#> [1] "1PX"
#> 
#> [[2]]$result[[3]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[3]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[3]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[3]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[3]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[3]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[3]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[3]]$admin_county
#> NULL
#> 
#> [[2]]$result[[3]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[3]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[3]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[3]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[3]]$ced
#> NULL
#> 
#> [[2]]$result[[3]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[3]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[3]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[3]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[3]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[3]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[3]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[3]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[3]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[3]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[3]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[3]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[3]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[3]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[3]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[3]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[3]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[3]]$lep2
#> NULL
#> 
#> [[2]]$result[[3]]$codes
#> [[2]]$result[[3]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[3]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[3]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[3]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[3]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[3]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[3]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[3]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[3]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[3]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[3]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[3]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[3]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[3]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[3]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[3]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[3]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[3]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[3]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[3]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[3]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[3]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[3]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[3]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[3]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[3]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[3]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[3]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[3]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[3]]$distance
#> [1] 177.6176
#> 
#> 
#> [[2]]$result[[4]]
#> [[2]]$result[[4]]$postcode
#> [1] "PO33 1QB"
#> 
#> [[2]]$result[[4]]$quality
#> [1] 1
#> 
#> [[2]]$result[[4]]$eastings
#> [1] 461528
#> 
#> [[2]]$result[[4]]$northings
#> [1] 91185
#> 
#> [[2]]$result[[4]]$country
#> [1] "England"
#> 
#> [[2]]$result[[4]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[4]]$longitude
#> [1] -1.129815
#> 
#> [[2]]$result[[4]]$latitude
#> [1] 50.71703
#> 
#> [[2]]$result[[4]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[4]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[4]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[4]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[4]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[4]]$incode
#> [1] "1QB"
#> 
#> [[2]]$result[[4]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[4]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[4]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[4]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[4]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[4]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[4]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[4]]$admin_county
#> NULL
#> 
#> [[2]]$result[[4]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[4]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[4]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[4]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[4]]$ced
#> NULL
#> 
#> [[2]]$result[[4]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[4]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[4]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[4]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[4]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[4]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[4]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[4]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[4]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[4]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[4]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[4]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[4]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[4]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[4]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[4]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[4]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[4]]$lep2
#> NULL
#> 
#> [[2]]$result[[4]]$codes
#> [[2]]$result[[4]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[4]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[4]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[4]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[4]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[4]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[4]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[4]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[4]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[4]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[4]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[4]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[4]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[4]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[4]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[4]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[4]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[4]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[4]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[4]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[4]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[4]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[4]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[4]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[4]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[4]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[4]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[4]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[4]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[4]]$distance
#> [1] 180.9833
#> 
#> 
#> [[2]]$result[[5]]
#> [[2]]$result[[5]]$postcode
#> [1] "PO33 1QD"
#> 
#> [[2]]$result[[5]]$quality
#> [1] 1
#> 
#> [[2]]$result[[5]]$eastings
#> [1] 461667
#> 
#> [[2]]$result[[5]]$northings
#> [1] 91204
#> 
#> [[2]]$result[[5]]$country
#> [1] "England"
#> 
#> [[2]]$result[[5]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[5]]$longitude
#> [1] -1.127843
#> 
#> [[2]]$result[[5]]$latitude
#> [1] 50.71719
#> 
#> [[2]]$result[[5]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[5]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[5]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[5]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[5]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[5]]$incode
#> [1] "1QD"
#> 
#> [[2]]$result[[5]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[5]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[5]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[5]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[5]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[5]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[5]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[5]]$admin_county
#> NULL
#> 
#> [[2]]$result[[5]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[5]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[5]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[5]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[5]]$ced
#> NULL
#> 
#> [[2]]$result[[5]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[5]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[5]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[5]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[5]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[5]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[5]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[5]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[5]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[5]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[5]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[5]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[5]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[5]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[5]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[5]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[5]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[5]]$lep2
#> NULL
#> 
#> [[2]]$result[[5]]$codes
#> [[2]]$result[[5]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[5]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[5]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[5]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[5]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[5]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[5]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[5]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[5]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[5]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[5]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[5]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[5]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[5]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[5]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[5]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[5]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[5]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[5]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[5]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[5]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[5]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[5]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[5]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[5]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[5]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[5]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[5]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[5]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[5]]$distance
#> [1] 192.8285
#> 
#> 
#> [[2]]$result[[6]]
#> [[2]]$result[[6]]$postcode
#> [1] "PO33 1PU"
#> 
#> [[2]]$result[[6]]$quality
#> [1] 1
#> 
#> [[2]]$result[[6]]$eastings
#> [1] 461794
#> 
#> [[2]]$result[[6]]$northings
#> [1] 91346
#> 
#> [[2]]$result[[6]]$country
#> [1] "England"
#> 
#> [[2]]$result[[6]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[6]]$longitude
#> [1] -1.126021
#> 
#> [[2]]$result[[6]]$latitude
#> [1] 50.71845
#> 
#> [[2]]$result[[6]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[6]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[6]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[6]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[6]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[6]]$incode
#> [1] "1PU"
#> 
#> [[2]]$result[[6]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[6]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[6]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[6]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[6]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[6]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[6]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[6]]$admin_county
#> NULL
#> 
#> [[2]]$result[[6]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[6]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[6]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[6]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[6]]$ced
#> NULL
#> 
#> [[2]]$result[[6]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[6]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[6]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[6]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[6]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[6]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[6]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[6]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[6]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[6]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[6]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[6]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[6]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[6]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[6]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[6]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[6]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[6]]$lep2
#> NULL
#> 
#> [[2]]$result[[6]]$codes
#> [[2]]$result[[6]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[6]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[6]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[6]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[6]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[6]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[6]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[6]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[6]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[6]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[6]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[6]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[6]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[6]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[6]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[6]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[6]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[6]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[6]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[6]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[6]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[6]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[6]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[6]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[6]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[6]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[6]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[6]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[6]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[6]]$distance
#> [1] 235.7973
#> 
#> 
#> [[2]]$result[[7]]
#> [[2]]$result[[7]]$postcode
#> [1] "PO33 1PZ"
#> 
#> [[2]]$result[[7]]$quality
#> [1] 1
#> 
#> [[2]]$result[[7]]$eastings
#> [1] 461662
#> 
#> [[2]]$result[[7]]$northings
#> [1] 91099
#> 
#> [[2]]$result[[7]]$country
#> [1] "England"
#> 
#> [[2]]$result[[7]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[7]]$longitude
#> [1] -1.127932
#> 
#> [[2]]$result[[7]]$latitude
#> [1] 50.71625
#> 
#> [[2]]$result[[7]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[7]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[7]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[7]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[7]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[7]]$incode
#> [1] "1PZ"
#> 
#> [[2]]$result[[7]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[7]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[7]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[7]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[7]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[7]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[7]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[7]]$admin_county
#> NULL
#> 
#> [[2]]$result[[7]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[7]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[7]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[7]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[7]]$ced
#> NULL
#> 
#> [[2]]$result[[7]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[7]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[7]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[7]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[7]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[7]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[7]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[7]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[7]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[7]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[7]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[7]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[7]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[7]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[7]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[7]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[7]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[7]]$lep2
#> NULL
#> 
#> [[2]]$result[[7]]$codes
#> [[2]]$result[[7]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[7]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[7]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[7]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[7]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[7]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[7]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[7]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[7]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[7]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[7]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[7]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[7]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[7]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[7]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[7]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[7]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[7]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[7]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[7]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[7]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[7]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[7]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[7]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[7]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[7]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[7]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[7]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[7]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[7]]$distance
#> [1] 283.9522
#> 
#> 
#> [[2]]$result[[8]]
#> [[2]]$result[[8]]$postcode
#> [1] "PO33 1FS"
#> 
#> [[2]]$result[[8]]$quality
#> [1] 1
#> 
#> [[2]]$result[[8]]$eastings
#> [1] 461946
#> 
#> [[2]]$result[[8]]$northings
#> [1] 91263
#> 
#> [[2]]$result[[8]]$country
#> [1] "England"
#> 
#> [[2]]$result[[8]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[8]]$longitude
#> [1] -1.123882
#> 
#> [[2]]$result[[8]]$latitude
#> [1] 50.71769
#> 
#> [[2]]$result[[8]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[8]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[8]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[8]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[8]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[8]]$incode
#> [1] "1FS"
#> 
#> [[2]]$result[[8]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[8]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[8]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[8]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[8]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[8]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[8]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[8]]$admin_county
#> NULL
#> 
#> [[2]]$result[[8]]$date_of_introduction
#> [1] "201810"
#> 
#> [[2]]$result[[8]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[8]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[8]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[8]]$ced
#> NULL
#> 
#> [[2]]$result[[8]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[8]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[8]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[8]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[8]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[8]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[8]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[8]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[8]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[8]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[8]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[8]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[8]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[8]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[8]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[8]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[8]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[8]]$lep2
#> NULL
#> 
#> [[2]]$result[[8]]$codes
#> [[2]]$result[[8]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[8]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[8]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[8]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[8]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[8]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[8]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[8]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[8]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[8]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[8]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[8]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[8]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[8]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[8]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[8]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[8]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[8]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[8]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[8]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[8]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[8]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[8]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[8]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[8]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[8]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[8]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[8]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[8]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[8]]$distance
#> [1] 399.5761
#> 
#> 
#> [[2]]$result[[9]]
#> [[2]]$result[[9]]$postcode
#> [1] "PO33 1QR"
#> 
#> [[2]]$result[[9]]$quality
#> [1] 1
#> 
#> [[2]]$result[[9]]$eastings
#> [1] 461800
#> 
#> [[2]]$result[[9]]$northings
#> [1] 91043
#> 
#> [[2]]$result[[9]]$country
#> [1] "England"
#> 
#> [[2]]$result[[9]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[9]]$longitude
#> [1] -1.125987
#> 
#> [[2]]$result[[9]]$latitude
#> [1] 50.71573
#> 
#> [[2]]$result[[9]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[9]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[9]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[9]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[9]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[9]]$incode
#> [1] "1QR"
#> 
#> [[2]]$result[[9]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[9]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[9]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[9]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[9]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[9]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[9]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[9]]$admin_county
#> NULL
#> 
#> [[2]]$result[[9]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[9]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[9]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[9]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[9]]$ced
#> NULL
#> 
#> [[2]]$result[[9]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[9]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[9]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[9]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[9]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[9]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[9]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[9]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[9]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[9]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[9]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[9]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[9]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[9]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[9]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[9]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[9]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[9]]$lep2
#> NULL
#> 
#> [[2]]$result[[9]]$codes
#> [[2]]$result[[9]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[9]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[9]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[9]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[9]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[9]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[9]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[9]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[9]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[9]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[9]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[9]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[9]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[9]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[9]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[9]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[9]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[9]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[9]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[9]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[9]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[9]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[9]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[9]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[9]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[9]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[9]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[9]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[9]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[9]]$distance
#> [1] 400.9874
#> 
#> 
#> [[2]]$result[[10]]
#> [[2]]$result[[10]]$postcode
#> [1] "PO33 1PB"
#> 
#> [[2]]$result[[10]]$quality
#> [1] 1
#> 
#> [[2]]$result[[10]]$eastings
#> [1] 461246
#> 
#> [[2]]$result[[10]]$northings
#> [1] 91634
#> 
#> [[2]]$result[[10]]$country
#> [1] "England"
#> 
#> [[2]]$result[[10]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[10]]$longitude
#> [1] -1.133735
#> 
#> [[2]]$result[[10]]$latitude
#> [1] 50.7211
#> 
#> [[2]]$result[[10]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[10]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[10]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[10]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[10]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[10]]$incode
#> [1] "1PB"
#> 
#> [[2]]$result[[10]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[10]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[10]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[10]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[10]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[10]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[10]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[10]]$admin_county
#> NULL
#> 
#> [[2]]$result[[10]]$date_of_introduction
#> [1] "198504"
#> 
#> [[2]]$result[[10]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[10]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[10]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[10]]$ced
#> NULL
#> 
#> [[2]]$result[[10]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[10]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[10]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[10]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[10]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[10]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[10]]$bua
#> NULL
#> 
#> [[2]]$result[[10]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[10]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[10]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[10]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[10]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[10]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[10]]$oa21
#> [1] "E00087635"
#> 
#> [[2]]$result[[10]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[2]]$result[[10]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[10]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[10]]$lep2
#> NULL
#> 
#> [[2]]$result[[10]]$codes
#> [[2]]$result[[10]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[10]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[10]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[10]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[10]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[10]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[10]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[10]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[10]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[10]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[10]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[10]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[10]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[10]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[10]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[10]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[10]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[10]]$codes$bua
#> NULL
#> 
#> [[2]]$result[[10]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[10]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[10]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[10]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[10]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[10]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[10]]$codes$oa21
#> [1] "E00087635"
#> 
#> [[2]]$result[[10]]$codes$ruc11
#> [1] "C1"
#> 
#> [[2]]$result[[10]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[10]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[10]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[10]]$distance
#> [1] 412.4242
#> 
#> 
#> [[2]]$result[[11]]
#> [[2]]$result[[11]]$postcode
#> [1] "PO33 1PR"
#> 
#> [[2]]$result[[11]]$quality
#> [1] 1
#> 
#> [[2]]$result[[11]]$eastings
#> [1] 461285
#> 
#> [[2]]$result[[11]]$northings
#> [1] 91676
#> 
#> [[2]]$result[[11]]$country
#> [1] "England"
#> 
#> [[2]]$result[[11]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[11]]$longitude
#> [1] -1.133175
#> 
#> [[2]]$result[[11]]$latitude
#> [1] 50.72147
#> 
#> [[2]]$result[[11]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[11]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[11]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[11]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[11]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[11]]$incode
#> [1] "1PR"
#> 
#> [[2]]$result[[11]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[11]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[11]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[11]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[11]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[11]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[11]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[11]]$admin_county
#> NULL
#> 
#> [[2]]$result[[11]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[11]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[11]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[11]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[11]]$ced
#> NULL
#> 
#> [[2]]$result[[11]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[11]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[11]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[11]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[11]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[11]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[11]]$bua
#> NULL
#> 
#> [[2]]$result[[11]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[11]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[11]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[11]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[11]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[11]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[11]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[11]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[11]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[11]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[11]]$lep2
#> NULL
#> 
#> [[2]]$result[[11]]$codes
#> [[2]]$result[[11]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[11]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[11]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[11]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[11]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[11]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[11]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[11]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[11]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[11]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[11]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[11]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[11]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[11]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[11]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[11]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[11]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[11]]$codes$bua
#> NULL
#> 
#> [[2]]$result[[11]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[11]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[11]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[11]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[11]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[11]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[11]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[11]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[11]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[11]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[11]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[11]]$distance
#> [1] 414.5863
#> 
#> 
#> [[2]]$result[[12]]
#> [[2]]$result[[12]]$postcode
#> [1] "PO33 1QP"
#> 
#> [[2]]$result[[12]]$quality
#> [1] 1
#> 
#> [[2]]$result[[12]]$eastings
#> [1] 461876
#> 
#> [[2]]$result[[12]]$northings
#> [1] 91040
#> 
#> [[2]]$result[[12]]$country
#> [1] "England"
#> 
#> [[2]]$result[[12]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[12]]$longitude
#> [1] -1.124911
#> 
#> [[2]]$result[[12]]$latitude
#> [1] 50.71569
#> 
#> [[2]]$result[[12]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[12]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[12]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[12]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[12]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[12]]$incode
#> [1] "1QP"
#> 
#> [[2]]$result[[12]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[12]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[12]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[12]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[12]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[12]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[12]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[12]]$admin_county
#> NULL
#> 
#> [[2]]$result[[12]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[12]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[12]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[12]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[12]]$ced
#> NULL
#> 
#> [[2]]$result[[12]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[12]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[12]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[12]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[12]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[12]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[12]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[12]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[12]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[12]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[12]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[12]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[12]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[12]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[12]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[12]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[12]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[12]]$lep2
#> NULL
#> 
#> [[2]]$result[[12]]$codes
#> [[2]]$result[[12]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[12]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[12]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[12]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[12]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[12]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[12]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[12]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[12]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[12]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[12]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[12]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[12]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[12]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[12]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[12]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[12]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[12]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[12]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[12]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[12]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[12]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[12]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[12]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[12]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[12]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[12]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[12]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[12]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[12]]$distance
#> [1] 452.7889
#> 
#> 
#> [[2]]$result[[13]]
#> [[2]]$result[[13]]$postcode
#> [1] "PO33 1GL"
#> 
#> [[2]]$result[[13]]$quality
#> [1] 1
#> 
#> [[2]]$result[[13]]$eastings
#> [1] 461919
#> 
#> [[2]]$result[[13]]$northings
#> [1] 91078
#> 
#> [[2]]$result[[13]]$country
#> [1] "England"
#> 
#> [[2]]$result[[13]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[13]]$longitude
#> [1] -1.124296
#> 
#> [[2]]$result[[13]]$latitude
#> [1] 50.71603
#> 
#> [[2]]$result[[13]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[13]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[13]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[13]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[13]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[13]]$incode
#> [1] "1GL"
#> 
#> [[2]]$result[[13]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[13]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[13]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[13]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[13]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[13]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[13]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[13]]$admin_county
#> NULL
#> 
#> [[2]]$result[[13]]$date_of_introduction
#> [1] "202209"
#> 
#> [[2]]$result[[13]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[13]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[13]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[13]]$ced
#> NULL
#> 
#> [[2]]$result[[13]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[13]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[13]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[13]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[13]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[13]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[13]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[13]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[13]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[13]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[13]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[13]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[13]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[13]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[13]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[13]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[13]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[13]]$lep2
#> NULL
#> 
#> [[2]]$result[[13]]$codes
#> [[2]]$result[[13]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[13]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[13]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[13]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[13]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[13]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[13]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[13]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[13]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[13]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[13]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[13]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[13]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[13]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[13]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[13]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[13]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[13]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[13]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[13]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[13]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[13]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[13]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[13]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[13]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[13]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[13]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[13]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[13]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[13]]$distance
#> [1] 459.2306
#> 
#> 
#> [[2]]$result[[14]]
#> [[2]]$result[[14]]$postcode
#> [1] "PO34 5AP"
#> 
#> [[2]]$result[[14]]$quality
#> [1] 1
#> 
#> [[2]]$result[[14]]$eastings
#> [1] 461899
#> 
#> [[2]]$result[[14]]$northings
#> [1] 91690
#> 
#> [[2]]$result[[14]]$country
#> [1] "England"
#> 
#> [[2]]$result[[14]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[14]]$longitude
#> [1] -1.124476
#> 
#> [[2]]$result[[14]]$latitude
#> [1] 50.72154
#> 
#> [[2]]$result[[14]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[14]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[14]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[14]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[14]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[14]]$incode
#> [1] "5AP"
#> 
#> [[2]]$result[[14]]$outcode
#> [1] "PO34"
#> 
#> [[2]]$result[[14]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[14]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[14]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[14]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[14]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[14]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[14]]$admin_county
#> NULL
#> 
#> [[2]]$result[[14]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[14]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[14]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[14]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[14]]$ced
#> NULL
#> 
#> [[2]]$result[[14]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[14]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[14]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[14]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[14]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[14]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[14]]$bua
#> [1] "Seaview and Nettlestone"
#> 
#> [[2]]$result[[14]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[14]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[14]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[14]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[14]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[14]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[14]]$oa21
#> [1] "E00087635"
#> 
#> [[2]]$result[[14]]$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[2]]$result[[14]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[14]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[14]]$lep2
#> NULL
#> 
#> [[2]]$result[[14]]$codes
#> [[2]]$result[[14]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[14]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[14]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[14]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[14]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[14]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[14]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[14]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[14]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[14]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[14]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[14]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[14]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[14]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[14]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[14]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[14]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[14]]$codes$bua
#> [1] "E63013869"
#> 
#> [[2]]$result[[14]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[14]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[14]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[14]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[14]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[14]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[14]]$codes$oa21
#> [1] "E00087635"
#> 
#> [[2]]$result[[14]]$codes$ruc11
#> [1] "C1"
#> 
#> [[2]]$result[[14]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[14]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[14]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[14]]$distance
#> [1] 471.304
#> 
#> 
#> [[2]]$result[[15]]
#> [[2]]$result[[15]]$postcode
#> [1] "PO33 1PY"
#> 
#> [[2]]$result[[15]]$quality
#> [1] 1
#> 
#> [[2]]$result[[15]]$eastings
#> [1] 461863
#> 
#> [[2]]$result[[15]]$northings
#> [1] 90987
#> 
#> [[2]]$result[[15]]$country
#> [1] "England"
#> 
#> [[2]]$result[[15]]$nhs_ha
#> [1] "South Central"
#> 
#> [[2]]$result[[15]]$longitude
#> [1] -1.125104
#> 
#> [[2]]$result[[15]]$latitude
#> [1] 50.71522
#> 
#> [[2]]$result[[15]]$european_electoral_region
#> [1] "South East"
#> 
#> [[2]]$result[[15]]$primary_care_trust
#> [1] "Isle of Wight National Health Service"
#> 
#> [[2]]$result[[15]]$region
#> [1] "South East"
#> 
#> [[2]]$result[[15]]$lsoa
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[15]]$msoa
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[15]]$incode
#> [1] "1PY"
#> 
#> [[2]]$result[[15]]$outcode
#> [1] "PO33"
#> 
#> [[2]]$result[[15]]$parliamentary_constituency
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[15]]$parliamentary_constituency_2024
#> [1] "Isle of Wight East"
#> 
#> [[2]]$result[[15]]$senedd_constituency
#> NULL
#> 
#> [[2]]$result[[15]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result[[15]]$admin_district
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[15]]$parish
#> [1] "Nettlestone and Seaview"
#> 
#> [[2]]$result[[15]]$admin_county
#> NULL
#> 
#> [[2]]$result[[15]]$date_of_introduction
#> [1] "198001"
#> 
#> [[2]]$result[[15]]$date_of_termination
#> NULL
#> 
#> [[2]]$result[[15]]$index_of_multiple_deprivation
#> [1] 20794
#> 
#> [[2]]$result[[15]]$admin_ward
#> [1] "Nettlestone & Seaview"
#> 
#> [[2]]$result[[15]]$ced
#> NULL
#> 
#> [[2]]$result[[15]]$ccg
#> [1] "NHS Hampshire and Isle of Wight"
#> 
#> [[2]]$result[[15]]$nuts
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[15]]$pfa
#> [1] "Hampshire"
#> 
#> [[2]]$result[[15]]$nhs_region
#> [1] "South East"
#> 
#> [[2]]$result[[15]]$ttwa
#> [1] "Isle of Wight"
#> 
#> [[2]]$result[[15]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result[[15]]$bua
#> [1] "Pondwell"
#> 
#> [[2]]$result[[15]]$icb
#> [1] "NHS Hampshire and Isle of Wight Integrated Care Board"
#> 
#> [[2]]$result[[15]]$cancer_alliance
#> [1] "Wessex"
#> 
#> [[2]]$result[[15]]$lsoa11
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[15]]$msoa11
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[15]]$lsoa21
#> [1] "Isle of Wight 010D"
#> 
#> [[2]]$result[[15]]$msoa21
#> [1] "Isle of Wight 010"
#> 
#> [[2]]$result[[15]]$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[15]]$ruc11
#> [1] "(England/Wales) Rural hamlet and isolated dwellings"
#> 
#> [[2]]$result[[15]]$ruc21
#> [1] "Urban: Further from a major town or city"
#> 
#> [[2]]$result[[15]]$lep1
#> [1] "Solent"
#> 
#> [[2]]$result[[15]]$lep2
#> NULL
#> 
#> [[2]]$result[[15]]$codes
#> [[2]]$result[[15]]$codes$admin_district
#> [1] "E06000046"
#> 
#> [[2]]$result[[15]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result[[15]]$codes$admin_ward
#> [1] "E05013378"
#> 
#> [[2]]$result[[15]]$codes$parish
#> [1] "E04001306"
#> 
#> [[2]]$result[[15]]$codes$parliamentary_constituency
#> [1] "E14001303"
#> 
#> [[2]]$result[[15]]$codes$parliamentary_constituency_2024
#> [1] "E14001303"
#> 
#> [[2]]$result[[15]]$codes$ccg
#> [1] "E38000266"
#> 
#> [[2]]$result[[15]]$codes$ccg_id
#> [1] "D9Y0V"
#> 
#> [[2]]$result[[15]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result[[15]]$codes$nuts
#> [1] "TLJ34"
#> 
#> [[2]]$result[[15]]$codes$lsoa
#> [1] "E01017351"
#> 
#> [[2]]$result[[15]]$codes$msoa
#> [1] "E02003590"
#> 
#> [[2]]$result[[15]]$codes$lau2
#> [1] "E06000046"
#> 
#> [[2]]$result[[15]]$codes$pfa
#> [1] "E23000030"
#> 
#> [[2]]$result[[15]]$codes$nhs_region
#> [1] "E40000005"
#> 
#> [[2]]$result[[15]]$codes$ttwa
#> [1] "E30000070"
#> 
#> [[2]]$result[[15]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result[[15]]$codes$bua
#> [1] "E63013866"
#> 
#> [[2]]$result[[15]]$codes$icb
#> [1] "E54000067"
#> 
#> [[2]]$result[[15]]$codes$cancer_alliance
#> [1] "E56000038"
#> 
#> [[2]]$result[[15]]$codes$lsoa11
#> [1] "E01017351"
#> 
#> [[2]]$result[[15]]$codes$msoa11
#> [1] "E02003590"
#> 
#> [[2]]$result[[15]]$codes$lsoa21
#> [1] "E01017351"
#> 
#> [[2]]$result[[15]]$codes$msoa21
#> [1] "E02003590"
#> 
#> [[2]]$result[[15]]$codes$oa21
#> [1] "E00087636"
#> 
#> [[2]]$result[[15]]$codes$ruc11
#> [1] "F1"
#> 
#> [[2]]$result[[15]]$codes$ruc21
#> [1] "UF1"
#> 
#> [[2]]$result[[15]]$codes$lep1
#> [1] "E37000055"
#> 
#> [[2]]$result[[15]]$codes$lep2
#> NULL
#> 
#> 
#> [[2]]$result[[15]]$distance
#> [1] 483.8624
#> 
#> 
#> 
#> 
# }
```
