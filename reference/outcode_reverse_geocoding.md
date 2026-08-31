# Outcode reverse geocoding

Returns nearest outcodes for a given longitude and latitude.

## Usage

``` r
outcode_reverse_geocoding(longitude, latitude, limit = 10, radius = 5000)
```

## Arguments

- longitude:

  A string, integer or float. Needs to have at least two decimal points.

- latitude:

  A string, integer or float. Needs to have at least two decimal points.

- limit:

  A string, integer or float. Limits number of postcodes matches to
  return. Defaults to 10. Needs to be less than 100.

- radius:

  A string, integer or float. Limits number of postcodes matches to
  return. Defaults to 5,000m. Needs to be less than 25,000m.

## Value

A list of geographical properties.

## See also

[`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
outcode_reverse_geocoding("-3.15", "51.47")
#> [[1]]
#> [[1]]$outcode
#> [1] "CF99"
#> 
#> [[1]]$longitude
#> [1] -3.16231
#> 
#> [[1]]$latitude
#> [1] 51.46376
#> 
#> [[1]]$northings
#> [1] 174506
#> 
#> [[1]]$eastings
#> [1] 319353
#> 
#> [[1]]$admin_district
#> [[1]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[1]]$parish
#> [[1]]$parish[[1]]
#> [1] "Butetown"
#> 
#> 
#> [[1]]$admin_county
#> list()
#> 
#> [[1]]$admin_ward
#> [[1]]$admin_ward[[1]]
#> [1] "Butetown"
#> 
#> 
#> [[1]]$country
#> [[1]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[1]]$parliamentary_constituency
#> [[1]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[2]]
#> [[2]]$outcode
#> [1] "CF10"
#> 
#> [[2]]$longitude
#> [1] -3.17314
#> 
#> [[2]]$latitude
#> [1] 51.47473
#> 
#> [[2]]$northings
#> [1] 175738
#> 
#> [[2]]$eastings
#> [1] 318620
#> 
#> [[2]]$admin_district
#> [[2]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[2]]$parish
#> [[2]]$parish[[1]]
#> [1] "Adamsdown"
#> 
#> [[2]]$parish[[2]]
#> [1] "Butetown"
#> 
#> [[2]]$parish[[3]]
#> [1] "Castle"
#> 
#> [[2]]$parish[[4]]
#> [1] "Cathays"
#> 
#> [[2]]$parish[[5]]
#> [1] "Grangetown"
#> 
#> [[2]]$parish[[6]]
#> [1] "Splott"
#> 
#> 
#> [[2]]$admin_county
#> list()
#> 
#> [[2]]$admin_ward
#> [[2]]$admin_ward[[1]]
#> [1] "Adamsdown"
#> 
#> [[2]]$admin_ward[[2]]
#> [1] "Butetown"
#> 
#> [[2]]$admin_ward[[3]]
#> [1] "Cathays"
#> 
#> [[2]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[2]]$admin_ward[[5]]
#> [1] "Splott"
#> 
#> 
#> [[2]]$country
#> [[2]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[2]]$parliamentary_constituency
#> [[2]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[2]]$parliamentary_constituency[[2]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[3]]
#> [[3]]$outcode
#> [1] "CF95"
#> 
#> [[3]]$longitude
#> [1] -3.171048
#> 
#> [[3]]$latitude
#> [1] 51.4812
#> 
#> [[3]]$northings
#> [1] 176455
#> 
#> [[3]]$eastings
#> [1] 318777
#> 
#> [[3]]$admin_district
#> [[3]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[3]]$parish
#> [[3]]$parish[[1]]
#> [1] "Castle"
#> 
#> 
#> [[3]]$admin_county
#> list()
#> 
#> [[3]]$admin_ward
#> [[3]]$admin_ward[[1]]
#> [1] "Cathays"
#> 
#> 
#> [[3]]$country
#> [[3]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[3]]$parliamentary_constituency
#> [[3]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[4]]
#> [[4]]$outcode
#> [1] "CF24"
#> 
#> [[4]]$longitude
#> [1] -3.161936
#> 
#> [[4]]$latitude
#> [1] 51.48813
#> 
#> [[4]]$northings
#> [1] 177216
#> 
#> [[4]]$eastings
#> [1] 319422
#> 
#> [[4]]$admin_district
#> [[4]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[4]]$parish
#> [[4]]$parish[[1]]
#> [1] "Adamsdown"
#> 
#> [[4]]$parish[[2]]
#> [1] "Butetown"
#> 
#> [[4]]$parish[[3]]
#> [1] "Cathays"
#> 
#> [[4]]$parish[[4]]
#> [1] "Grangetown"
#> 
#> [[4]]$parish[[5]]
#> [1] "Penylan"
#> 
#> [[4]]$parish[[6]]
#> [1] "Roath"
#> 
#> [[4]]$parish[[7]]
#> [1] "Splott"
#> 
#> [[4]]$parish[[8]]
#> [1] "Tremorfa"
#> 
#> 
#> [[4]]$admin_county
#> list()
#> 
#> [[4]]$admin_ward
#> [[4]]$admin_ward[[1]]
#> [1] "Adamsdown"
#> 
#> [[4]]$admin_ward[[2]]
#> [1] "Butetown"
#> 
#> [[4]]$admin_ward[[3]]
#> [1] "Cathays"
#> 
#> [[4]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[4]]$admin_ward[[5]]
#> [1] "Penylan"
#> 
#> [[4]]$admin_ward[[6]]
#> [1] "Plasnewydd"
#> 
#> [[4]]$admin_ward[[7]]
#> [1] "Splott"
#> 
#> 
#> [[4]]$country
#> [[4]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[4]]$parliamentary_constituency
#> [[4]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[4]]$parliamentary_constituency[[2]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[5]]
#> [[5]]$outcode
#> [1] "CF11"
#> 
#> [[5]]$longitude
#> [1] -3.19249
#> 
#> [[5]]$latitude
#> [1] 51.47288
#> 
#> [[5]]$northings
#> [1] 175554
#> 
#> [[5]]$eastings
#> [1] 317273
#> 
#> [[5]]$admin_district
#> [[5]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> [[5]]$admin_district[[2]]
#> [1] "Vale of Glamorgan"
#> 
#> 
#> [[5]]$parish
#> [[5]]$parish[[1]]
#> [1] "Butetown"
#> 
#> [[5]]$parish[[2]]
#> [1] "Canton"
#> 
#> [[5]]$parish[[3]]
#> [1] "Grangetown"
#> 
#> [[5]]$parish[[4]]
#> [1] "Llandaff"
#> 
#> [[5]]$parish[[5]]
#> [1] "Llandough"
#> 
#> [[5]]$parish[[6]]
#> [1] "Michaelston-le-Pit and Leckwith"
#> 
#> [[5]]$parish[[7]]
#> [1] "Pontcanna"
#> 
#> [[5]]$parish[[8]]
#> [1] "Riverside"
#> 
#> 
#> [[5]]$admin_county
#> list()
#> 
#> [[5]]$admin_ward
#> [[5]]$admin_ward[[1]]
#> [1] "Butetown"
#> 
#> [[5]]$admin_ward[[2]]
#> [1] "Canton"
#> 
#> [[5]]$admin_ward[[3]]
#> [1] "Dinas Powys"
#> 
#> [[5]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[5]]$admin_ward[[5]]
#> [1] "Llandaff"
#> 
#> [[5]]$admin_ward[[6]]
#> [1] "Llandough"
#> 
#> [[5]]$admin_ward[[7]]
#> [1] "Riverside"
#> 
#> 
#> [[5]]$country
#> [[5]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[5]]$parliamentary_constituency
#> [[5]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> [[5]]$parliamentary_constituency[[2]]
#> [1] "Cardiff West"
#> 
#> 
#> 
#> [[6]]
#> [[6]]$outcode
#> [1] "CF91"
#> 
#> [[6]]$longitude
#> [1] -3.194049
#> 
#> [[6]]$latitude
#> [1] 51.46554
#> 
#> [[6]]$northings
#> [1] 174740
#> 
#> [[6]]$eastings
#> [1] 317151
#> 
#> [[6]]$admin_district
#> [[6]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[6]]$parish
#> [[6]]$parish[[1]]
#> [1] "Grangetown"
#> 
#> 
#> [[6]]$admin_county
#> list()
#> 
#> [[6]]$admin_ward
#> [[6]]$admin_ward[[1]]
#> [1] "Grangetown"
#> 
#> 
#> [[6]]$country
#> [[6]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[6]]$parliamentary_constituency
#> [[6]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[7]]
#> [[7]]$outcode
#> [1] "CF23"
#> 
#> [[7]]$longitude
#> [1] -3.155483
#> 
#> [[7]]$latitude
#> [1] 51.51448
#> 
#> [[7]]$northings
#> [1] 180140
#> 
#> [[7]]$eastings
#> [1] 319916
#> 
#> [[7]]$admin_district
#> [[7]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[7]]$parish
#> [[7]]$parish[[1]]
#> [1] "Cyncoed"
#> 
#> [[7]]$parish[[2]]
#> [1] "Heath"
#> 
#> [[7]]$parish[[3]]
#> [1] "Lisvane"
#> 
#> [[7]]$parish[[4]]
#> [1] "Llanedeyrn"
#> 
#> [[7]]$parish[[5]]
#> [1] "Pentwyn"
#> 
#> [[7]]$parish[[6]]
#> [1] "Penylan"
#> 
#> [[7]]$parish[[7]]
#> [1] "Pontprennau"
#> 
#> [[7]]$parish[[8]]
#> [1] "Roath"
#> 
#> [[7]]$parish[[9]]
#> [1] "Trowbridge"
#> 
#> 
#> [[7]]$admin_county
#> list()
#> 
#> [[7]]$admin_ward
#> [[7]]$admin_ward[[1]]
#> [1] "Cyncoed"
#> 
#> [[7]]$admin_ward[[2]]
#> [1] "Heath"
#> 
#> [[7]]$admin_ward[[3]]
#> [1] "Lisvane and Thornhill"
#> 
#> [[7]]$admin_ward[[4]]
#> [1] "Pentwyn"
#> 
#> [[7]]$admin_ward[[5]]
#> [1] "Penylan"
#> 
#> [[7]]$admin_ward[[6]]
#> [1] "Plasnewydd"
#> 
#> [[7]]$admin_ward[[7]]
#> [1] "Pontprennau and Old St Mellons"
#> 
#> [[7]]$admin_ward[[8]]
#> [1] "Trowbridge"
#> 
#> 
#> [[7]]$country
#> [[7]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[7]]$parliamentary_constituency
#> [[7]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[7]]$parliamentary_constituency[[2]]
#> [1] "Cardiff North"
#> 
#> 
#> 
outcode_reverse_geocoding(-3.15, 51.47)
#> [[1]]
#> [[1]]$outcode
#> [1] "CF99"
#> 
#> [[1]]$longitude
#> [1] -3.16231
#> 
#> [[1]]$latitude
#> [1] 51.46376
#> 
#> [[1]]$northings
#> [1] 174506
#> 
#> [[1]]$eastings
#> [1] 319353
#> 
#> [[1]]$admin_district
#> [[1]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[1]]$parish
#> [[1]]$parish[[1]]
#> [1] "Butetown"
#> 
#> 
#> [[1]]$admin_county
#> list()
#> 
#> [[1]]$admin_ward
#> [[1]]$admin_ward[[1]]
#> [1] "Butetown"
#> 
#> 
#> [[1]]$country
#> [[1]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[1]]$parliamentary_constituency
#> [[1]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[2]]
#> [[2]]$outcode
#> [1] "CF10"
#> 
#> [[2]]$longitude
#> [1] -3.17314
#> 
#> [[2]]$latitude
#> [1] 51.47473
#> 
#> [[2]]$northings
#> [1] 175738
#> 
#> [[2]]$eastings
#> [1] 318620
#> 
#> [[2]]$admin_district
#> [[2]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[2]]$parish
#> [[2]]$parish[[1]]
#> [1] "Adamsdown"
#> 
#> [[2]]$parish[[2]]
#> [1] "Butetown"
#> 
#> [[2]]$parish[[3]]
#> [1] "Castle"
#> 
#> [[2]]$parish[[4]]
#> [1] "Cathays"
#> 
#> [[2]]$parish[[5]]
#> [1] "Grangetown"
#> 
#> [[2]]$parish[[6]]
#> [1] "Splott"
#> 
#> 
#> [[2]]$admin_county
#> list()
#> 
#> [[2]]$admin_ward
#> [[2]]$admin_ward[[1]]
#> [1] "Adamsdown"
#> 
#> [[2]]$admin_ward[[2]]
#> [1] "Butetown"
#> 
#> [[2]]$admin_ward[[3]]
#> [1] "Cathays"
#> 
#> [[2]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[2]]$admin_ward[[5]]
#> [1] "Splott"
#> 
#> 
#> [[2]]$country
#> [[2]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[2]]$parliamentary_constituency
#> [[2]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[2]]$parliamentary_constituency[[2]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[3]]
#> [[3]]$outcode
#> [1] "CF95"
#> 
#> [[3]]$longitude
#> [1] -3.171048
#> 
#> [[3]]$latitude
#> [1] 51.4812
#> 
#> [[3]]$northings
#> [1] 176455
#> 
#> [[3]]$eastings
#> [1] 318777
#> 
#> [[3]]$admin_district
#> [[3]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[3]]$parish
#> [[3]]$parish[[1]]
#> [1] "Castle"
#> 
#> 
#> [[3]]$admin_county
#> list()
#> 
#> [[3]]$admin_ward
#> [[3]]$admin_ward[[1]]
#> [1] "Cathays"
#> 
#> 
#> [[3]]$country
#> [[3]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[3]]$parliamentary_constituency
#> [[3]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[4]]
#> [[4]]$outcode
#> [1] "CF24"
#> 
#> [[4]]$longitude
#> [1] -3.161936
#> 
#> [[4]]$latitude
#> [1] 51.48813
#> 
#> [[4]]$northings
#> [1] 177216
#> 
#> [[4]]$eastings
#> [1] 319422
#> 
#> [[4]]$admin_district
#> [[4]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[4]]$parish
#> [[4]]$parish[[1]]
#> [1] "Adamsdown"
#> 
#> [[4]]$parish[[2]]
#> [1] "Butetown"
#> 
#> [[4]]$parish[[3]]
#> [1] "Cathays"
#> 
#> [[4]]$parish[[4]]
#> [1] "Grangetown"
#> 
#> [[4]]$parish[[5]]
#> [1] "Penylan"
#> 
#> [[4]]$parish[[6]]
#> [1] "Roath"
#> 
#> [[4]]$parish[[7]]
#> [1] "Splott"
#> 
#> [[4]]$parish[[8]]
#> [1] "Tremorfa"
#> 
#> 
#> [[4]]$admin_county
#> list()
#> 
#> [[4]]$admin_ward
#> [[4]]$admin_ward[[1]]
#> [1] "Adamsdown"
#> 
#> [[4]]$admin_ward[[2]]
#> [1] "Butetown"
#> 
#> [[4]]$admin_ward[[3]]
#> [1] "Cathays"
#> 
#> [[4]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[4]]$admin_ward[[5]]
#> [1] "Penylan"
#> 
#> [[4]]$admin_ward[[6]]
#> [1] "Plasnewydd"
#> 
#> [[4]]$admin_ward[[7]]
#> [1] "Splott"
#> 
#> 
#> [[4]]$country
#> [[4]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[4]]$parliamentary_constituency
#> [[4]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[4]]$parliamentary_constituency[[2]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[5]]
#> [[5]]$outcode
#> [1] "CF11"
#> 
#> [[5]]$longitude
#> [1] -3.19249
#> 
#> [[5]]$latitude
#> [1] 51.47288
#> 
#> [[5]]$northings
#> [1] 175554
#> 
#> [[5]]$eastings
#> [1] 317273
#> 
#> [[5]]$admin_district
#> [[5]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> [[5]]$admin_district[[2]]
#> [1] "Vale of Glamorgan"
#> 
#> 
#> [[5]]$parish
#> [[5]]$parish[[1]]
#> [1] "Butetown"
#> 
#> [[5]]$parish[[2]]
#> [1] "Canton"
#> 
#> [[5]]$parish[[3]]
#> [1] "Grangetown"
#> 
#> [[5]]$parish[[4]]
#> [1] "Llandaff"
#> 
#> [[5]]$parish[[5]]
#> [1] "Llandough"
#> 
#> [[5]]$parish[[6]]
#> [1] "Michaelston-le-Pit and Leckwith"
#> 
#> [[5]]$parish[[7]]
#> [1] "Pontcanna"
#> 
#> [[5]]$parish[[8]]
#> [1] "Riverside"
#> 
#> 
#> [[5]]$admin_county
#> list()
#> 
#> [[5]]$admin_ward
#> [[5]]$admin_ward[[1]]
#> [1] "Butetown"
#> 
#> [[5]]$admin_ward[[2]]
#> [1] "Canton"
#> 
#> [[5]]$admin_ward[[3]]
#> [1] "Dinas Powys"
#> 
#> [[5]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[5]]$admin_ward[[5]]
#> [1] "Llandaff"
#> 
#> [[5]]$admin_ward[[6]]
#> [1] "Llandough"
#> 
#> [[5]]$admin_ward[[7]]
#> [1] "Riverside"
#> 
#> 
#> [[5]]$country
#> [[5]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[5]]$parliamentary_constituency
#> [[5]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> [[5]]$parliamentary_constituency[[2]]
#> [1] "Cardiff West"
#> 
#> 
#> 
#> [[6]]
#> [[6]]$outcode
#> [1] "CF91"
#> 
#> [[6]]$longitude
#> [1] -3.194049
#> 
#> [[6]]$latitude
#> [1] 51.46554
#> 
#> [[6]]$northings
#> [1] 174740
#> 
#> [[6]]$eastings
#> [1] 317151
#> 
#> [[6]]$admin_district
#> [[6]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[6]]$parish
#> [[6]]$parish[[1]]
#> [1] "Grangetown"
#> 
#> 
#> [[6]]$admin_county
#> list()
#> 
#> [[6]]$admin_ward
#> [[6]]$admin_ward[[1]]
#> [1] "Grangetown"
#> 
#> 
#> [[6]]$country
#> [[6]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[6]]$parliamentary_constituency
#> [[6]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[7]]
#> [[7]]$outcode
#> [1] "CF23"
#> 
#> [[7]]$longitude
#> [1] -3.155483
#> 
#> [[7]]$latitude
#> [1] 51.51448
#> 
#> [[7]]$northings
#> [1] 180140
#> 
#> [[7]]$eastings
#> [1] 319916
#> 
#> [[7]]$admin_district
#> [[7]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[7]]$parish
#> [[7]]$parish[[1]]
#> [1] "Cyncoed"
#> 
#> [[7]]$parish[[2]]
#> [1] "Heath"
#> 
#> [[7]]$parish[[3]]
#> [1] "Lisvane"
#> 
#> [[7]]$parish[[4]]
#> [1] "Llanedeyrn"
#> 
#> [[7]]$parish[[5]]
#> [1] "Pentwyn"
#> 
#> [[7]]$parish[[6]]
#> [1] "Penylan"
#> 
#> [[7]]$parish[[7]]
#> [1] "Pontprennau"
#> 
#> [[7]]$parish[[8]]
#> [1] "Roath"
#> 
#> [[7]]$parish[[9]]
#> [1] "Trowbridge"
#> 
#> 
#> [[7]]$admin_county
#> list()
#> 
#> [[7]]$admin_ward
#> [[7]]$admin_ward[[1]]
#> [1] "Cyncoed"
#> 
#> [[7]]$admin_ward[[2]]
#> [1] "Heath"
#> 
#> [[7]]$admin_ward[[3]]
#> [1] "Lisvane and Thornhill"
#> 
#> [[7]]$admin_ward[[4]]
#> [1] "Pentwyn"
#> 
#> [[7]]$admin_ward[[5]]
#> [1] "Penylan"
#> 
#> [[7]]$admin_ward[[6]]
#> [1] "Plasnewydd"
#> 
#> [[7]]$admin_ward[[7]]
#> [1] "Pontprennau and Old St Mellons"
#> 
#> [[7]]$admin_ward[[8]]
#> [1] "Trowbridge"
#> 
#> 
#> [[7]]$country
#> [[7]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[7]]$parliamentary_constituency
#> [[7]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[7]]$parliamentary_constituency[[2]]
#> [1] "Cardiff North"
#> 
#> 
#> 
outcode_reverse_geocoding("-3.15807731271522", "51.4799900627036")
#> [[1]]
#> [[1]]$outcode
#> [1] "CF95"
#> 
#> [[1]]$longitude
#> [1] -3.171048
#> 
#> [[1]]$latitude
#> [1] 51.4812
#> 
#> [[1]]$northings
#> [1] 176455
#> 
#> [[1]]$eastings
#> [1] 318777
#> 
#> [[1]]$admin_district
#> [[1]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[1]]$parish
#> [[1]]$parish[[1]]
#> [1] "Castle"
#> 
#> 
#> [[1]]$admin_county
#> list()
#> 
#> [[1]]$admin_ward
#> [[1]]$admin_ward[[1]]
#> [1] "Cathays"
#> 
#> 
#> [[1]]$country
#> [[1]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[1]]$parliamentary_constituency
#> [[1]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[2]]
#> [[2]]$outcode
#> [1] "CF24"
#> 
#> [[2]]$longitude
#> [1] -3.161936
#> 
#> [[2]]$latitude
#> [1] 51.48813
#> 
#> [[2]]$northings
#> [1] 177216
#> 
#> [[2]]$eastings
#> [1] 319422
#> 
#> [[2]]$admin_district
#> [[2]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[2]]$parish
#> [[2]]$parish[[1]]
#> [1] "Adamsdown"
#> 
#> [[2]]$parish[[2]]
#> [1] "Butetown"
#> 
#> [[2]]$parish[[3]]
#> [1] "Cathays"
#> 
#> [[2]]$parish[[4]]
#> [1] "Grangetown"
#> 
#> [[2]]$parish[[5]]
#> [1] "Penylan"
#> 
#> [[2]]$parish[[6]]
#> [1] "Roath"
#> 
#> [[2]]$parish[[7]]
#> [1] "Splott"
#> 
#> [[2]]$parish[[8]]
#> [1] "Tremorfa"
#> 
#> 
#> [[2]]$admin_county
#> list()
#> 
#> [[2]]$admin_ward
#> [[2]]$admin_ward[[1]]
#> [1] "Adamsdown"
#> 
#> [[2]]$admin_ward[[2]]
#> [1] "Butetown"
#> 
#> [[2]]$admin_ward[[3]]
#> [1] "Cathays"
#> 
#> [[2]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[2]]$admin_ward[[5]]
#> [1] "Penylan"
#> 
#> [[2]]$admin_ward[[6]]
#> [1] "Plasnewydd"
#> 
#> [[2]]$admin_ward[[7]]
#> [1] "Splott"
#> 
#> 
#> [[2]]$country
#> [[2]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[2]]$parliamentary_constituency
#> [[2]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[2]]$parliamentary_constituency[[2]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[3]]
#> [[3]]$outcode
#> [1] "CF10"
#> 
#> [[3]]$longitude
#> [1] -3.17314
#> 
#> [[3]]$latitude
#> [1] 51.47473
#> 
#> [[3]]$northings
#> [1] 175738
#> 
#> [[3]]$eastings
#> [1] 318620
#> 
#> [[3]]$admin_district
#> [[3]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[3]]$parish
#> [[3]]$parish[[1]]
#> [1] "Adamsdown"
#> 
#> [[3]]$parish[[2]]
#> [1] "Butetown"
#> 
#> [[3]]$parish[[3]]
#> [1] "Castle"
#> 
#> [[3]]$parish[[4]]
#> [1] "Cathays"
#> 
#> [[3]]$parish[[5]]
#> [1] "Grangetown"
#> 
#> [[3]]$parish[[6]]
#> [1] "Splott"
#> 
#> 
#> [[3]]$admin_county
#> list()
#> 
#> [[3]]$admin_ward
#> [[3]]$admin_ward[[1]]
#> [1] "Adamsdown"
#> 
#> [[3]]$admin_ward[[2]]
#> [1] "Butetown"
#> 
#> [[3]]$admin_ward[[3]]
#> [1] "Cathays"
#> 
#> [[3]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[3]]$admin_ward[[5]]
#> [1] "Splott"
#> 
#> 
#> [[3]]$country
#> [[3]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[3]]$parliamentary_constituency
#> [[3]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[3]]$parliamentary_constituency[[2]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[4]]
#> [[4]]$outcode
#> [1] "CF99"
#> 
#> [[4]]$longitude
#> [1] -3.16231
#> 
#> [[4]]$latitude
#> [1] 51.46376
#> 
#> [[4]]$northings
#> [1] 174506
#> 
#> [[4]]$eastings
#> [1] 319353
#> 
#> [[4]]$admin_district
#> [[4]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[4]]$parish
#> [[4]]$parish[[1]]
#> [1] "Butetown"
#> 
#> 
#> [[4]]$admin_county
#> list()
#> 
#> [[4]]$admin_ward
#> [[4]]$admin_ward[[1]]
#> [1] "Butetown"
#> 
#> 
#> [[4]]$country
#> [[4]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[4]]$parliamentary_constituency
#> [[4]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[5]]
#> [[5]]$outcode
#> [1] "CF11"
#> 
#> [[5]]$longitude
#> [1] -3.19249
#> 
#> [[5]]$latitude
#> [1] 51.47288
#> 
#> [[5]]$northings
#> [1] 175554
#> 
#> [[5]]$eastings
#> [1] 317273
#> 
#> [[5]]$admin_district
#> [[5]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> [[5]]$admin_district[[2]]
#> [1] "Vale of Glamorgan"
#> 
#> 
#> [[5]]$parish
#> [[5]]$parish[[1]]
#> [1] "Butetown"
#> 
#> [[5]]$parish[[2]]
#> [1] "Canton"
#> 
#> [[5]]$parish[[3]]
#> [1] "Grangetown"
#> 
#> [[5]]$parish[[4]]
#> [1] "Llandaff"
#> 
#> [[5]]$parish[[5]]
#> [1] "Llandough"
#> 
#> [[5]]$parish[[6]]
#> [1] "Michaelston-le-Pit and Leckwith"
#> 
#> [[5]]$parish[[7]]
#> [1] "Pontcanna"
#> 
#> [[5]]$parish[[8]]
#> [1] "Riverside"
#> 
#> 
#> [[5]]$admin_county
#> list()
#> 
#> [[5]]$admin_ward
#> [[5]]$admin_ward[[1]]
#> [1] "Butetown"
#> 
#> [[5]]$admin_ward[[2]]
#> [1] "Canton"
#> 
#> [[5]]$admin_ward[[3]]
#> [1] "Dinas Powys"
#> 
#> [[5]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[5]]$admin_ward[[5]]
#> [1] "Llandaff"
#> 
#> [[5]]$admin_ward[[6]]
#> [1] "Llandough"
#> 
#> [[5]]$admin_ward[[7]]
#> [1] "Riverside"
#> 
#> 
#> [[5]]$country
#> [[5]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[5]]$parliamentary_constituency
#> [[5]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> [[5]]$parliamentary_constituency[[2]]
#> [1] "Cardiff West"
#> 
#> 
#> 
#> [[6]]
#> [[6]]$outcode
#> [1] "CF91"
#> 
#> [[6]]$longitude
#> [1] -3.194049
#> 
#> [[6]]$latitude
#> [1] 51.46554
#> 
#> [[6]]$northings
#> [1] 174740
#> 
#> [[6]]$eastings
#> [1] 317151
#> 
#> [[6]]$admin_district
#> [[6]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[6]]$parish
#> [[6]]$parish[[1]]
#> [1] "Grangetown"
#> 
#> 
#> [[6]]$admin_county
#> list()
#> 
#> [[6]]$admin_ward
#> [[6]]$admin_ward[[1]]
#> [1] "Grangetown"
#> 
#> 
#> [[6]]$country
#> [[6]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[6]]$parliamentary_constituency
#> [[6]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[7]]
#> [[7]]$outcode
#> [1] "CF23"
#> 
#> [[7]]$longitude
#> [1] -3.155483
#> 
#> [[7]]$latitude
#> [1] 51.51448
#> 
#> [[7]]$northings
#> [1] 180140
#> 
#> [[7]]$eastings
#> [1] 319916
#> 
#> [[7]]$admin_district
#> [[7]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[7]]$parish
#> [[7]]$parish[[1]]
#> [1] "Cyncoed"
#> 
#> [[7]]$parish[[2]]
#> [1] "Heath"
#> 
#> [[7]]$parish[[3]]
#> [1] "Lisvane"
#> 
#> [[7]]$parish[[4]]
#> [1] "Llanedeyrn"
#> 
#> [[7]]$parish[[5]]
#> [1] "Pentwyn"
#> 
#> [[7]]$parish[[6]]
#> [1] "Penylan"
#> 
#> [[7]]$parish[[7]]
#> [1] "Pontprennau"
#> 
#> [[7]]$parish[[8]]
#> [1] "Roath"
#> 
#> [[7]]$parish[[9]]
#> [1] "Trowbridge"
#> 
#> 
#> [[7]]$admin_county
#> list()
#> 
#> [[7]]$admin_ward
#> [[7]]$admin_ward[[1]]
#> [1] "Cyncoed"
#> 
#> [[7]]$admin_ward[[2]]
#> [1] "Heath"
#> 
#> [[7]]$admin_ward[[3]]
#> [1] "Lisvane and Thornhill"
#> 
#> [[7]]$admin_ward[[4]]
#> [1] "Pentwyn"
#> 
#> [[7]]$admin_ward[[5]]
#> [1] "Penylan"
#> 
#> [[7]]$admin_ward[[6]]
#> [1] "Plasnewydd"
#> 
#> [[7]]$admin_ward[[7]]
#> [1] "Pontprennau and Old St Mellons"
#> 
#> [[7]]$admin_ward[[8]]
#> [1] "Trowbridge"
#> 
#> 
#> [[7]]$country
#> [[7]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[7]]$parliamentary_constituency
#> [[7]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[7]]$parliamentary_constituency[[2]]
#> [1] "Cardiff North"
#> 
#> 
#> 
outcode_reverse_geocoding(-3.15, 51.47, limit = 11, radius = 20000)
#> [[1]]
#> [[1]]$outcode
#> [1] "CF99"
#> 
#> [[1]]$longitude
#> [1] -3.16231
#> 
#> [[1]]$latitude
#> [1] 51.46376
#> 
#> [[1]]$northings
#> [1] 174506
#> 
#> [[1]]$eastings
#> [1] 319353
#> 
#> [[1]]$admin_district
#> [[1]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[1]]$parish
#> [[1]]$parish[[1]]
#> [1] "Butetown"
#> 
#> 
#> [[1]]$admin_county
#> list()
#> 
#> [[1]]$admin_ward
#> [[1]]$admin_ward[[1]]
#> [1] "Butetown"
#> 
#> 
#> [[1]]$country
#> [[1]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[1]]$parliamentary_constituency
#> [[1]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[2]]
#> [[2]]$outcode
#> [1] "CF10"
#> 
#> [[2]]$longitude
#> [1] -3.17314
#> 
#> [[2]]$latitude
#> [1] 51.47473
#> 
#> [[2]]$northings
#> [1] 175738
#> 
#> [[2]]$eastings
#> [1] 318620
#> 
#> [[2]]$admin_district
#> [[2]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[2]]$parish
#> [[2]]$parish[[1]]
#> [1] "Adamsdown"
#> 
#> [[2]]$parish[[2]]
#> [1] "Butetown"
#> 
#> [[2]]$parish[[3]]
#> [1] "Castle"
#> 
#> [[2]]$parish[[4]]
#> [1] "Cathays"
#> 
#> [[2]]$parish[[5]]
#> [1] "Grangetown"
#> 
#> [[2]]$parish[[6]]
#> [1] "Splott"
#> 
#> 
#> [[2]]$admin_county
#> list()
#> 
#> [[2]]$admin_ward
#> [[2]]$admin_ward[[1]]
#> [1] "Adamsdown"
#> 
#> [[2]]$admin_ward[[2]]
#> [1] "Butetown"
#> 
#> [[2]]$admin_ward[[3]]
#> [1] "Cathays"
#> 
#> [[2]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[2]]$admin_ward[[5]]
#> [1] "Splott"
#> 
#> 
#> [[2]]$country
#> [[2]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[2]]$parliamentary_constituency
#> [[2]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[2]]$parliamentary_constituency[[2]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[3]]
#> [[3]]$outcode
#> [1] "CF95"
#> 
#> [[3]]$longitude
#> [1] -3.171048
#> 
#> [[3]]$latitude
#> [1] 51.4812
#> 
#> [[3]]$northings
#> [1] 176455
#> 
#> [[3]]$eastings
#> [1] 318777
#> 
#> [[3]]$admin_district
#> [[3]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[3]]$parish
#> [[3]]$parish[[1]]
#> [1] "Castle"
#> 
#> 
#> [[3]]$admin_county
#> list()
#> 
#> [[3]]$admin_ward
#> [[3]]$admin_ward[[1]]
#> [1] "Cathays"
#> 
#> 
#> [[3]]$country
#> [[3]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[3]]$parliamentary_constituency
#> [[3]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[4]]
#> [[4]]$outcode
#> [1] "CF24"
#> 
#> [[4]]$longitude
#> [1] -3.161936
#> 
#> [[4]]$latitude
#> [1] 51.48813
#> 
#> [[4]]$northings
#> [1] 177216
#> 
#> [[4]]$eastings
#> [1] 319422
#> 
#> [[4]]$admin_district
#> [[4]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[4]]$parish
#> [[4]]$parish[[1]]
#> [1] "Adamsdown"
#> 
#> [[4]]$parish[[2]]
#> [1] "Butetown"
#> 
#> [[4]]$parish[[3]]
#> [1] "Cathays"
#> 
#> [[4]]$parish[[4]]
#> [1] "Grangetown"
#> 
#> [[4]]$parish[[5]]
#> [1] "Penylan"
#> 
#> [[4]]$parish[[6]]
#> [1] "Roath"
#> 
#> [[4]]$parish[[7]]
#> [1] "Splott"
#> 
#> [[4]]$parish[[8]]
#> [1] "Tremorfa"
#> 
#> 
#> [[4]]$admin_county
#> list()
#> 
#> [[4]]$admin_ward
#> [[4]]$admin_ward[[1]]
#> [1] "Adamsdown"
#> 
#> [[4]]$admin_ward[[2]]
#> [1] "Butetown"
#> 
#> [[4]]$admin_ward[[3]]
#> [1] "Cathays"
#> 
#> [[4]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[4]]$admin_ward[[5]]
#> [1] "Penylan"
#> 
#> [[4]]$admin_ward[[6]]
#> [1] "Plasnewydd"
#> 
#> [[4]]$admin_ward[[7]]
#> [1] "Splott"
#> 
#> 
#> [[4]]$country
#> [[4]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[4]]$parliamentary_constituency
#> [[4]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[4]]$parliamentary_constituency[[2]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[5]]
#> [[5]]$outcode
#> [1] "CF11"
#> 
#> [[5]]$longitude
#> [1] -3.19249
#> 
#> [[5]]$latitude
#> [1] 51.47288
#> 
#> [[5]]$northings
#> [1] 175554
#> 
#> [[5]]$eastings
#> [1] 317273
#> 
#> [[5]]$admin_district
#> [[5]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> [[5]]$admin_district[[2]]
#> [1] "Vale of Glamorgan"
#> 
#> 
#> [[5]]$parish
#> [[5]]$parish[[1]]
#> [1] "Butetown"
#> 
#> [[5]]$parish[[2]]
#> [1] "Canton"
#> 
#> [[5]]$parish[[3]]
#> [1] "Grangetown"
#> 
#> [[5]]$parish[[4]]
#> [1] "Llandaff"
#> 
#> [[5]]$parish[[5]]
#> [1] "Llandough"
#> 
#> [[5]]$parish[[6]]
#> [1] "Michaelston-le-Pit and Leckwith"
#> 
#> [[5]]$parish[[7]]
#> [1] "Pontcanna"
#> 
#> [[5]]$parish[[8]]
#> [1] "Riverside"
#> 
#> 
#> [[5]]$admin_county
#> list()
#> 
#> [[5]]$admin_ward
#> [[5]]$admin_ward[[1]]
#> [1] "Butetown"
#> 
#> [[5]]$admin_ward[[2]]
#> [1] "Canton"
#> 
#> [[5]]$admin_ward[[3]]
#> [1] "Dinas Powys"
#> 
#> [[5]]$admin_ward[[4]]
#> [1] "Grangetown"
#> 
#> [[5]]$admin_ward[[5]]
#> [1] "Llandaff"
#> 
#> [[5]]$admin_ward[[6]]
#> [1] "Llandough"
#> 
#> [[5]]$admin_ward[[7]]
#> [1] "Riverside"
#> 
#> 
#> [[5]]$country
#> [[5]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[5]]$parliamentary_constituency
#> [[5]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> [[5]]$parliamentary_constituency[[2]]
#> [1] "Cardiff West"
#> 
#> 
#> 
#> [[6]]
#> [[6]]$outcode
#> [1] "CF91"
#> 
#> [[6]]$longitude
#> [1] -3.194049
#> 
#> [[6]]$latitude
#> [1] 51.46554
#> 
#> [[6]]$northings
#> [1] 174740
#> 
#> [[6]]$eastings
#> [1] 317151
#> 
#> [[6]]$admin_district
#> [[6]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[6]]$parish
#> [[6]]$parish[[1]]
#> [1] "Grangetown"
#> 
#> 
#> [[6]]$admin_county
#> list()
#> 
#> [[6]]$admin_ward
#> [[6]]$admin_ward[[1]]
#> [1] "Grangetown"
#> 
#> 
#> [[6]]$country
#> [[6]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[6]]$parliamentary_constituency
#> [[6]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
#> [[7]]
#> [[7]]$outcode
#> [1] "CF23"
#> 
#> [[7]]$longitude
#> [1] -3.155483
#> 
#> [[7]]$latitude
#> [1] 51.51448
#> 
#> [[7]]$northings
#> [1] 180140
#> 
#> [[7]]$eastings
#> [1] 319916
#> 
#> [[7]]$admin_district
#> [[7]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[7]]$parish
#> [[7]]$parish[[1]]
#> [1] "Cyncoed"
#> 
#> [[7]]$parish[[2]]
#> [1] "Heath"
#> 
#> [[7]]$parish[[3]]
#> [1] "Lisvane"
#> 
#> [[7]]$parish[[4]]
#> [1] "Llanedeyrn"
#> 
#> [[7]]$parish[[5]]
#> [1] "Pentwyn"
#> 
#> [[7]]$parish[[6]]
#> [1] "Penylan"
#> 
#> [[7]]$parish[[7]]
#> [1] "Pontprennau"
#> 
#> [[7]]$parish[[8]]
#> [1] "Roath"
#> 
#> [[7]]$parish[[9]]
#> [1] "Trowbridge"
#> 
#> 
#> [[7]]$admin_county
#> list()
#> 
#> [[7]]$admin_ward
#> [[7]]$admin_ward[[1]]
#> [1] "Cyncoed"
#> 
#> [[7]]$admin_ward[[2]]
#> [1] "Heath"
#> 
#> [[7]]$admin_ward[[3]]
#> [1] "Lisvane and Thornhill"
#> 
#> [[7]]$admin_ward[[4]]
#> [1] "Pentwyn"
#> 
#> [[7]]$admin_ward[[5]]
#> [1] "Penylan"
#> 
#> [[7]]$admin_ward[[6]]
#> [1] "Plasnewydd"
#> 
#> [[7]]$admin_ward[[7]]
#> [1] "Pontprennau and Old St Mellons"
#> 
#> [[7]]$admin_ward[[8]]
#> [1] "Trowbridge"
#> 
#> 
#> [[7]]$country
#> [[7]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[7]]$parliamentary_constituency
#> [[7]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> [[7]]$parliamentary_constituency[[2]]
#> [1] "Cardiff North"
#> 
#> 
#> 
#> [[8]]
#> [[8]]$outcode
#> [1] "CF64"
#> 
#> [[8]]$longitude
#> [1] -3.192439
#> 
#> [[8]]$latitude
#> [1] 51.43277
#> 
#> [[8]]$northings
#> [1] 171093
#> 
#> [[8]]$eastings
#> [1] 317204
#> 
#> [[8]]$admin_district
#> [[8]]$admin_district[[1]]
#> [1] "Vale of Glamorgan"
#> 
#> 
#> [[8]]$parish
#> [[8]]$parish[[1]]
#> [1] "Barry"
#> 
#> [[8]]$parish[[2]]
#> [1] "Dinas Powys"
#> 
#> [[8]]$parish[[3]]
#> [1] "Llandough"
#> 
#> [[8]]$parish[[4]]
#> [1] "Michaelston-le-Pit and Leckwith"
#> 
#> [[8]]$parish[[5]]
#> [1] "Penarth"
#> 
#> [[8]]$parish[[6]]
#> [1] "Sully and Lavernock"
#> 
#> 
#> [[8]]$admin_county
#> list()
#> 
#> [[8]]$admin_ward
#> [[8]]$admin_ward[[1]]
#> [1] "Castleland"
#> 
#> [[8]]$admin_ward[[2]]
#> [1] "Cornerswell"
#> 
#> [[8]]$admin_ward[[3]]
#> [1] "Dinas Powys"
#> 
#> [[8]]$admin_ward[[4]]
#> [1] "Llandough"
#> 
#> [[8]]$admin_ward[[5]]
#> [1] "Plymouth"
#> 
#> [[8]]$admin_ward[[6]]
#> [1] "Stanwell"
#> 
#> [[8]]$admin_ward[[7]]
#> [1] "St Augustine's"
#> 
#> [[8]]$admin_ward[[8]]
#> [1] "Sully"
#> 
#> 
#> [[8]]$country
#> [[8]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[8]]$parliamentary_constituency
#> [[8]]$parliamentary_constituency[[1]]
#> [1] "Cardiff South and Penarth"
#> 
#> [[8]]$parliamentary_constituency[[2]]
#> [1] "Vale of Glamorgan"
#> 
#> 
#> 
#> [[9]]
#> [[9]]$outcode
#> [1] "CF30"
#> 
#> [[9]]$longitude
#> [1] -3.1196
#> 
#> [[9]]$latitude
#> [1] 51.51964
#> 
#> [[9]]$northings
#> [1] 180675
#> 
#> [[9]]$eastings
#> [1] 322415
#> 
#> [[9]]$admin_district
#> [[9]]$admin_district[[1]]
#> [1] "Cardiff"
#> 
#> 
#> [[9]]$parish
#> [[9]]$parish[[1]]
#> [1] "Llanrumney"
#> 
#> 
#> [[9]]$admin_county
#> list()
#> 
#> [[9]]$admin_ward
#> [[9]]$admin_ward[[1]]
#> [1] "Llanrumney"
#> 
#> 
#> [[9]]$country
#> [[9]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[9]]$parliamentary_constituency
#> [[9]]$parliamentary_constituency[[1]]
#> [1] "Cardiff East"
#> 
#> 
#> 
#> [[10]]
#> [[10]]$outcode
#> [1] "CF3"
#> 
#> [[10]]$longitude
#> [1] -3.111304
#> 
#> [[10]]$latitude
#> [1] 51.52062
#> 
#> [[10]]$northings
#> [1] 180775
#> 
#> [[10]]$eastings
#> [1] 322992
#> 
#> [[10]]$admin_district
#> [[10]]$admin_district[[1]]
#> [1] "Caerphilly"
#> 
#> [[10]]$admin_district[[2]]
#> [1] "Cardiff"
#> 
#> [[10]]$admin_district[[3]]
#> [1] "Newport"
#> 
#> 
#> [[10]]$parish
#> [[10]]$parish[[1]]
#> [1] "Llanrumney"
#> 
#> [[10]]$parish[[2]]
#> [1] "Marshfield"
#> 
#> [[10]]$parish[[3]]
#> [1] "Michaelstone-y-Fedw"
#> 
#> [[10]]$parish[[4]]
#> [1] "Old St. Mellons"
#> 
#> [[10]]$parish[[5]]
#> [1] "Rudry"
#> 
#> [[10]]$parish[[6]]
#> [1] "Rumney"
#> 
#> [[10]]$parish[[7]]
#> [1] "Trowbridge"
#> 
#> [[10]]$parish[[8]]
#> [1] "Wentlooge"
#> 
#> 
#> [[10]]$admin_county
#> list()
#> 
#> [[10]]$admin_ward
#> [[10]]$admin_ward[[1]]
#> [1] "Llanrumney"
#> 
#> [[10]]$admin_ward[[2]]
#> [1] "Machen and Rudry"
#> 
#> [[10]]$admin_ward[[3]]
#> [1] "Pontprennau and Old St Mellons"
#> 
#> [[10]]$admin_ward[[4]]
#> [1] "Rumney"
#> 
#> [[10]]$admin_ward[[5]]
#> [1] "Tredegar Park and Marshfield"
#> 
#> [[10]]$admin_ward[[6]]
#> [1] "Trowbridge"
#> 
#> 
#> [[10]]$country
#> [[10]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[10]]$parliamentary_constituency
#> [[10]]$parliamentary_constituency[[1]]
#> [1] "Caerphilly"
#> 
#> [[10]]$parliamentary_constituency[[2]]
#> [1] "Cardiff East"
#> 
#> [[10]]$parliamentary_constituency[[3]]
#> [1] "Cardiff North"
#> 
#> [[10]]$parliamentary_constituency[[4]]
#> [1] "Newport West and Islwyn"
#> 
#> 
#> 
#> [[11]]
#> [[11]]$outcode
#> [1] "CF14"
#> 
#> [[11]]$longitude
#> [1] -3.20372
#> 
#> [[11]]$latitude
#> [1] 51.52008
#> 
#> [[11]]$northings
#> [1] 180816
#> 
#> [[11]]$eastings
#> [1] 316579
#> 
#> [[11]]$admin_district
#> [[11]]$admin_district[[1]]
#> [1] "Caerphilly"
#> 
#> [[11]]$admin_district[[2]]
#> [1] "Cardiff"
#> 
#> 
#> [[11]]$parish
#> [[11]]$parish[[1]]
#> [1] "Cathays"
#> 
#> [[11]]$parish[[2]]
#> [1] "Cyncoed"
#> 
#> [[11]]$parish[[3]]
#> [1] "Gabalfa"
#> 
#> [[11]]$parish[[4]]
#> [1] "Heath"
#> 
#> [[11]]$parish[[5]]
#> [1] "Lisvane"
#> 
#> [[11]]$parish[[6]]
#> [1] "Llandaff North"
#> 
#> [[11]]$parish[[7]]
#> [1] "Llanishen"
#> 
#> [[11]]$parish[[8]]
#> [1] "Pontprennau"
#> 
#> [[11]]$parish[[9]]
#> [1] "Rhiwbina"
#> 
#> [[11]]$parish[[10]]
#> [1] "Rudry"
#> 
#> [[11]]$parish[[11]]
#> [1] "Thornhill"
#> 
#> [[11]]$parish[[12]]
#> [1] "Tongwynlais"
#> 
#> [[11]]$parish[[13]]
#> [1] "Whitchurch"
#> 
#> 
#> [[11]]$admin_county
#> list()
#> 
#> [[11]]$admin_ward
#> [[11]]$admin_ward[[1]]
#> [1] "Cathays"
#> 
#> [[11]]$admin_ward[[2]]
#> [1] "Cyncoed"
#> 
#> [[11]]$admin_ward[[3]]
#> [1] "Gabalfa"
#> 
#> [[11]]$admin_ward[[4]]
#> [1] "Heath"
#> 
#> [[11]]$admin_ward[[5]]
#> [1] "Lisvane and Thornhill"
#> 
#> [[11]]$admin_ward[[6]]
#> [1] "Llandaff North"
#> 
#> [[11]]$admin_ward[[7]]
#> [1] "Llanishen"
#> 
#> [[11]]$admin_ward[[8]]
#> [1] "Machen and Rudry"
#> 
#> [[11]]$admin_ward[[9]]
#> [1] "Pontprennau and Old St Mellons"
#> 
#> [[11]]$admin_ward[[10]]
#> [1] "Rhiwbina"
#> 
#> [[11]]$admin_ward[[11]]
#> [1] "Whitchurch and Tongwynlais"
#> 
#> 
#> [[11]]$country
#> [[11]]$country[[1]]
#> [1] "Wales"
#> 
#> 
#> [[11]]$parliamentary_constituency
#> [[11]]$parliamentary_constituency[[1]]
#> [1] "Caerphilly"
#> 
#> [[11]]$parliamentary_constituency[[2]]
#> [1] "Cardiff East"
#> 
#> [[11]]$parliamentary_constituency[[3]]
#> [1] "Cardiff North"
#> 
#> [[11]]$parliamentary_constituency[[4]]
#> [1] "Cardiff South and Penarth"
#> 
#> 
#> 
# }
```
