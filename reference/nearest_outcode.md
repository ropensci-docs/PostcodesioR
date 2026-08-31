# Nearest outcode

Returns nearest outcodes for a given outcode. The search is based on the
relative distance of the outcode centroid.

## Usage

``` r
nearest_outcode(outcode, limit = 10, radius = 5000)
```

## Arguments

- outcode:

  A string with a UK postcode.

- limit:

  An integer. Optional parameter. Limits number of postcodes matches to
  return. Defaults to 10. Needs to be less than 100.

- radius:

  An integer. Optional parameter. Limits number of postcodes matches to
  return. Defaults to 5,000m. Needs to be less than 25,000m.

## Value

A list of geographical properties.

## See also

[`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
nearest_outcode("EC1Y")
#> [[1]]
#> [[1]]$outcode
#> [1] "EC1Y"
#> 
#> [[1]]$longitude
#> [1] -0.0923844
#> 
#> [[1]]$latitude
#> [1] 51.52309
#> 
#> [[1]]$northings
#> [1] 182188
#> 
#> [[1]]$eastings
#> [1] 532439
#> 
#> [[1]]$admin_district
#> [[1]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[1]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[1]]$parish
#> [[1]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[1]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[1]]$admin_county
#> list()
#> 
#> [[1]]$admin_ward
#> [[1]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[1]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[1]]$admin_ward[[3]]
#> [1] "Coleman Street"
#> 
#> [[1]]$admin_ward[[4]]
#> [1] "Cripplegate"
#> 
#> 
#> [[1]]$country
#> [[1]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[1]]$parliamentary_constituency
#> [[1]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[1]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[2]]
#> [[2]]$outcode
#> [1] "EC2Y"
#> 
#> [[2]]$longitude
#> [1] -0.09354922
#> 
#> [[2]]$latitude
#> [1] 51.51947
#> 
#> [[2]]$northings
#> [1] 181783
#> 
#> [[2]]$eastings
#> [1] 532369
#> 
#> [[2]]$admin_district
#> [[2]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[2]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[2]]$parish
#> [[2]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[2]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[2]]$admin_county
#> list()
#> 
#> [[2]]$admin_ward
#> [[2]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[2]]$admin_ward[[2]]
#> [1] "Bassishaw"
#> 
#> [[2]]$admin_ward[[3]]
#> [1] "Bunhill"
#> 
#> [[2]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[2]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[2]]$admin_ward[[6]]
#> [1] "Cripplegate"
#> 
#> 
#> [[2]]$country
#> [[2]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[2]]$parliamentary_constituency
#> [[2]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[2]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[3]]
#> [[3]]$outcode
#> [1] "EC2A"
#> 
#> [[3]]$longitude
#> [1] -0.08542688
#> 
#> [[3]]$latitude
#> [1] 51.52367
#> 
#> [[3]]$northings
#> [1] 182265
#> 
#> [[3]]$eastings
#> [1] 532920
#> 
#> [[3]]$admin_district
#> [[3]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[3]]$admin_district[[2]]
#> [1] "Hackney"
#> 
#> [[3]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> 
#> [[3]]$parish
#> [[3]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[3]]$parish[[2]]
#> [1] "Hackney, unparished area"
#> 
#> [[3]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[3]]$admin_county
#> list()
#> 
#> [[3]]$admin_ward
#> [[3]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[3]]$admin_ward[[2]]
#> [1] "Bunhill"
#> 
#> [[3]]$admin_ward[[3]]
#> [1] "Clerkenwell"
#> 
#> [[3]]$admin_ward[[4]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> 
#> [[3]]$country
#> [[3]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[3]]$parliamentary_constituency
#> [[3]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[3]]$parliamentary_constituency[[2]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[3]]$parliamentary_constituency[[3]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[4]]
#> [[4]]$outcode
#> [1] "EC1V"
#> 
#> [[4]]$longitude
#> [1] -0.09777263
#> 
#> [[4]]$latitude
#> [1] 51.5268
#> 
#> [[4]]$northings
#> [1] 182590
#> 
#> [[4]]$eastings
#> [1] 532055
#> 
#> [[4]]$admin_district
#> [[4]]$admin_district[[1]]
#> [1] "Hackney"
#> 
#> [[4]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[4]]$parish
#> [[4]]$parish[[1]]
#> [1] "Hackney, unparished area"
#> 
#> [[4]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[4]]$admin_county
#> list()
#> 
#> [[4]]$admin_ward
#> [[4]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[4]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[4]]$admin_ward[[3]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> [[4]]$admin_ward[[4]]
#> [1] "Hoxton West"
#> 
#> [[4]]$admin_ward[[5]]
#> [1] "St Peter's & Canalside"
#> 
#> 
#> [[4]]$country
#> [[4]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[4]]$parliamentary_constituency
#> [[4]]$parliamentary_constituency[[1]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[4]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[5]]
#> [[5]]$outcode
#> [1] "EC2M"
#> 
#> [[5]]$longitude
#> [1] -0.0861603
#> 
#> [[5]]$latitude
#> [1] 51.51857
#> 
#> [[5]]$northings
#> [1] 181697
#> 
#> [[5]]$eastings
#> [1] 532884
#> 
#> [[5]]$admin_district
#> [[5]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[5]]$admin_district[[2]]
#> [1] "Hackney"
#> 
#> [[5]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> [[5]]$admin_district[[4]]
#> [1] "Tower Hamlets"
#> 
#> 
#> [[5]]$parish
#> [[5]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[5]]$parish[[2]]
#> [1] "Hackney, unparished area"
#> 
#> [[5]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> [[5]]$parish[[4]]
#> [1] "Tower Hamlets, unparished area"
#> 
#> 
#> [[5]]$admin_county
#> list()
#> 
#> [[5]]$admin_ward
#> [[5]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[5]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[5]]$admin_ward[[3]]
#> [1] "Bunhill"
#> 
#> [[5]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[5]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[5]]$admin_ward[[6]]
#> [1] "Cornhill"
#> 
#> [[5]]$admin_ward[[7]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> [[5]]$admin_ward[[8]]
#> [1] "Spitalfields & Banglatown"
#> 
#> 
#> [[5]]$country
#> [[5]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[5]]$parliamentary_constituency
#> [[5]]$parliamentary_constituency[[1]]
#> [1] "Bethnal Green and Stepney"
#> 
#> [[5]]$parliamentary_constituency[[2]]
#> [1] "Cities of London and Westminster"
#> 
#> [[5]]$parliamentary_constituency[[3]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[5]]$parliamentary_constituency[[4]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[6]]
#> [[6]]$outcode
#> [1] "EC1M"
#> 
#> [[6]]$longitude
#> [1] -0.1023023
#> 
#> [[6]]$latitude
#> [1] 51.52129
#> 
#> [[6]]$northings
#> [1] 181970
#> 
#> [[6]]$eastings
#> [1] 531756
#> 
#> [[6]]$admin_district
#> [[6]]$admin_district[[1]]
#> [1] "Camden"
#> 
#> [[6]]$admin_district[[2]]
#> [1] "City of London"
#> 
#> [[6]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> 
#> [[6]]$parish
#> [[6]]$parish[[1]]
#> [1] "Camden, unparished area"
#> 
#> [[6]]$parish[[2]]
#> [1] "City of London, unparished area"
#> 
#> [[6]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[6]]$admin_county
#> list()
#> 
#> [[6]]$admin_ward
#> [[6]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[6]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[6]]$admin_ward[[3]]
#> [1] "Cripplegate"
#> 
#> [[6]]$admin_ward[[4]]
#> [1] "Farringdon Within"
#> 
#> [[6]]$admin_ward[[5]]
#> [1] "Farringdon Without"
#> 
#> [[6]]$admin_ward[[6]]
#> [1] "Holborn & Covent Garden"
#> 
#> 
#> [[6]]$country
#> [[6]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[6]]$parliamentary_constituency
#> [[6]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[6]]$parliamentary_constituency[[2]]
#> [1] "Holborn and St Pancras"
#> 
#> [[6]]$parliamentary_constituency[[3]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[7]]
#> [[7]]$outcode
#> [1] "EC2R"
#> 
#> [[7]]$longitude
#> [1] -0.09108468
#> 
#> [[7]]$latitude
#> [1] 51.51629
#> 
#> [[7]]$northings
#> [1] 181434
#> 
#> [[7]]$eastings
#> [1] 532549
#> 
#> [[7]]$admin_district
#> [[7]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[7]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[7]]$parish
#> [[7]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[7]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[7]]$admin_county
#> list()
#> 
#> [[7]]$admin_ward
#> [[7]]$admin_ward[[1]]
#> [1] "Bassishaw"
#> 
#> [[7]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[7]]$admin_ward[[3]]
#> [1] "Cheap"
#> 
#> [[7]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[7]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[7]]$admin_ward[[6]]
#> [1] "Cordwainer"
#> 
#> [[7]]$admin_ward[[7]]
#> [1] "Cornhill"
#> 
#> [[7]]$admin_ward[[8]]
#> [1] "Walbrook"
#> 
#> 
#> [[7]]$country
#> [[7]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[7]]$parliamentary_constituency
#> [[7]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[7]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[8]]
#> [[8]]$outcode
#> [1] "EC2V"
#> 
#> [[8]]$longitude
#> [1] -0.09365719
#> 
#> [[8]]$latitude
#> [1] 51.51546
#> 
#> [[8]]$northings
#> [1] 181337
#> 
#> [[8]]$eastings
#> [1] 532373
#> 
#> [[8]]$admin_district
#> [[8]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[8]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[8]]$parish
#> [[8]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[8]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[8]]$admin_county
#> list()
#> 
#> [[8]]$admin_ward
#> [[8]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[8]]$admin_ward[[2]]
#> [1] "Bassishaw"
#> 
#> [[8]]$admin_ward[[3]]
#> [1] "Bread Street"
#> 
#> [[8]]$admin_ward[[4]]
#> [1] "Cheap"
#> 
#> [[8]]$admin_ward[[5]]
#> [1] "Clerkenwell"
#> 
#> [[8]]$admin_ward[[6]]
#> [1] "Coleman Street"
#> 
#> [[8]]$admin_ward[[7]]
#> [1] "Cordwainer"
#> 
#> [[8]]$admin_ward[[8]]
#> [1] "Walbrook"
#> 
#> 
#> [[8]]$country
#> [[8]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[8]]$parliamentary_constituency
#> [[8]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[8]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[9]]
#> [[9]]$outcode
#> [1] "EC1A"
#> 
#> [[9]]$longitude
#> [1] -0.1041297
#> 
#> [[9]]$latitude
#> [1] 51.52053
#> 
#> [[9]]$northings
#> [1] 181882
#> 
#> [[9]]$eastings
#> [1] 531632
#> 
#> [[9]]$admin_district
#> [[9]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[9]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[9]]$parish
#> [[9]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[9]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[9]]$admin_county
#> list()
#> 
#> [[9]]$admin_ward
#> [[9]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[9]]$admin_ward[[2]]
#> [1] "Bunhill"
#> 
#> [[9]]$admin_ward[[3]]
#> [1] "Cheap"
#> 
#> [[9]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[9]]$admin_ward[[5]]
#> [1] "Farringdon Within"
#> 
#> [[9]]$admin_ward[[6]]
#> [1] "Farringdon Without"
#> 
#> 
#> [[9]]$country
#> [[9]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[9]]$parliamentary_constituency
#> [[9]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[9]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[10]]
#> [[10]]$outcode
#> [1] "EC2N"
#> 
#> [[10]]$longitude
#> [1] -0.08581437
#> 
#> [[10]]$latitude
#> [1] 51.51579
#> 
#> [[10]]$northings
#> [1] 181388
#> 
#> [[10]]$eastings
#> [1] 532916
#> 
#> [[10]]$admin_district
#> [[10]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[10]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[10]]$parish
#> [[10]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[10]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[10]]$admin_county
#> list()
#> 
#> [[10]]$admin_ward
#> [[10]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[10]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[10]]$admin_ward[[3]]
#> [1] "Clerkenwell"
#> 
#> [[10]]$admin_ward[[4]]
#> [1] "Cornhill"
#> 
#> [[10]]$admin_ward[[5]]
#> [1] "Lime Street"
#> 
#> [[10]]$admin_ward[[6]]
#> [1] "Walbrook"
#> 
#> 
#> [[10]]$country
#> [[10]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[10]]$parliamentary_constituency
#> [[10]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[10]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
nearest_outcode("EC1Y", limit = 11)
#> [[1]]
#> [[1]]$outcode
#> [1] "EC1Y"
#> 
#> [[1]]$longitude
#> [1] -0.0923844
#> 
#> [[1]]$latitude
#> [1] 51.52309
#> 
#> [[1]]$northings
#> [1] 182188
#> 
#> [[1]]$eastings
#> [1] 532439
#> 
#> [[1]]$admin_district
#> [[1]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[1]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[1]]$parish
#> [[1]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[1]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[1]]$admin_county
#> list()
#> 
#> [[1]]$admin_ward
#> [[1]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[1]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[1]]$admin_ward[[3]]
#> [1] "Coleman Street"
#> 
#> [[1]]$admin_ward[[4]]
#> [1] "Cripplegate"
#> 
#> 
#> [[1]]$country
#> [[1]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[1]]$parliamentary_constituency
#> [[1]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[1]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[2]]
#> [[2]]$outcode
#> [1] "EC2Y"
#> 
#> [[2]]$longitude
#> [1] -0.09354922
#> 
#> [[2]]$latitude
#> [1] 51.51947
#> 
#> [[2]]$northings
#> [1] 181783
#> 
#> [[2]]$eastings
#> [1] 532369
#> 
#> [[2]]$admin_district
#> [[2]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[2]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[2]]$parish
#> [[2]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[2]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[2]]$admin_county
#> list()
#> 
#> [[2]]$admin_ward
#> [[2]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[2]]$admin_ward[[2]]
#> [1] "Bassishaw"
#> 
#> [[2]]$admin_ward[[3]]
#> [1] "Bunhill"
#> 
#> [[2]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[2]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[2]]$admin_ward[[6]]
#> [1] "Cripplegate"
#> 
#> 
#> [[2]]$country
#> [[2]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[2]]$parliamentary_constituency
#> [[2]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[2]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[3]]
#> [[3]]$outcode
#> [1] "EC2A"
#> 
#> [[3]]$longitude
#> [1] -0.08542688
#> 
#> [[3]]$latitude
#> [1] 51.52367
#> 
#> [[3]]$northings
#> [1] 182265
#> 
#> [[3]]$eastings
#> [1] 532920
#> 
#> [[3]]$admin_district
#> [[3]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[3]]$admin_district[[2]]
#> [1] "Hackney"
#> 
#> [[3]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> 
#> [[3]]$parish
#> [[3]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[3]]$parish[[2]]
#> [1] "Hackney, unparished area"
#> 
#> [[3]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[3]]$admin_county
#> list()
#> 
#> [[3]]$admin_ward
#> [[3]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[3]]$admin_ward[[2]]
#> [1] "Bunhill"
#> 
#> [[3]]$admin_ward[[3]]
#> [1] "Clerkenwell"
#> 
#> [[3]]$admin_ward[[4]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> 
#> [[3]]$country
#> [[3]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[3]]$parliamentary_constituency
#> [[3]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[3]]$parliamentary_constituency[[2]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[3]]$parliamentary_constituency[[3]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[4]]
#> [[4]]$outcode
#> [1] "EC1V"
#> 
#> [[4]]$longitude
#> [1] -0.09777263
#> 
#> [[4]]$latitude
#> [1] 51.5268
#> 
#> [[4]]$northings
#> [1] 182590
#> 
#> [[4]]$eastings
#> [1] 532055
#> 
#> [[4]]$admin_district
#> [[4]]$admin_district[[1]]
#> [1] "Hackney"
#> 
#> [[4]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[4]]$parish
#> [[4]]$parish[[1]]
#> [1] "Hackney, unparished area"
#> 
#> [[4]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[4]]$admin_county
#> list()
#> 
#> [[4]]$admin_ward
#> [[4]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[4]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[4]]$admin_ward[[3]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> [[4]]$admin_ward[[4]]
#> [1] "Hoxton West"
#> 
#> [[4]]$admin_ward[[5]]
#> [1] "St Peter's & Canalside"
#> 
#> 
#> [[4]]$country
#> [[4]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[4]]$parliamentary_constituency
#> [[4]]$parliamentary_constituency[[1]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[4]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[5]]
#> [[5]]$outcode
#> [1] "EC2M"
#> 
#> [[5]]$longitude
#> [1] -0.0861603
#> 
#> [[5]]$latitude
#> [1] 51.51857
#> 
#> [[5]]$northings
#> [1] 181697
#> 
#> [[5]]$eastings
#> [1] 532884
#> 
#> [[5]]$admin_district
#> [[5]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[5]]$admin_district[[2]]
#> [1] "Hackney"
#> 
#> [[5]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> [[5]]$admin_district[[4]]
#> [1] "Tower Hamlets"
#> 
#> 
#> [[5]]$parish
#> [[5]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[5]]$parish[[2]]
#> [1] "Hackney, unparished area"
#> 
#> [[5]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> [[5]]$parish[[4]]
#> [1] "Tower Hamlets, unparished area"
#> 
#> 
#> [[5]]$admin_county
#> list()
#> 
#> [[5]]$admin_ward
#> [[5]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[5]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[5]]$admin_ward[[3]]
#> [1] "Bunhill"
#> 
#> [[5]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[5]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[5]]$admin_ward[[6]]
#> [1] "Cornhill"
#> 
#> [[5]]$admin_ward[[7]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> [[5]]$admin_ward[[8]]
#> [1] "Spitalfields & Banglatown"
#> 
#> 
#> [[5]]$country
#> [[5]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[5]]$parliamentary_constituency
#> [[5]]$parliamentary_constituency[[1]]
#> [1] "Bethnal Green and Stepney"
#> 
#> [[5]]$parliamentary_constituency[[2]]
#> [1] "Cities of London and Westminster"
#> 
#> [[5]]$parliamentary_constituency[[3]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[5]]$parliamentary_constituency[[4]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[6]]
#> [[6]]$outcode
#> [1] "EC1M"
#> 
#> [[6]]$longitude
#> [1] -0.1023023
#> 
#> [[6]]$latitude
#> [1] 51.52129
#> 
#> [[6]]$northings
#> [1] 181970
#> 
#> [[6]]$eastings
#> [1] 531756
#> 
#> [[6]]$admin_district
#> [[6]]$admin_district[[1]]
#> [1] "Camden"
#> 
#> [[6]]$admin_district[[2]]
#> [1] "City of London"
#> 
#> [[6]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> 
#> [[6]]$parish
#> [[6]]$parish[[1]]
#> [1] "Camden, unparished area"
#> 
#> [[6]]$parish[[2]]
#> [1] "City of London, unparished area"
#> 
#> [[6]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[6]]$admin_county
#> list()
#> 
#> [[6]]$admin_ward
#> [[6]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[6]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[6]]$admin_ward[[3]]
#> [1] "Cripplegate"
#> 
#> [[6]]$admin_ward[[4]]
#> [1] "Farringdon Within"
#> 
#> [[6]]$admin_ward[[5]]
#> [1] "Farringdon Without"
#> 
#> [[6]]$admin_ward[[6]]
#> [1] "Holborn & Covent Garden"
#> 
#> 
#> [[6]]$country
#> [[6]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[6]]$parliamentary_constituency
#> [[6]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[6]]$parliamentary_constituency[[2]]
#> [1] "Holborn and St Pancras"
#> 
#> [[6]]$parliamentary_constituency[[3]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[7]]
#> [[7]]$outcode
#> [1] "EC2R"
#> 
#> [[7]]$longitude
#> [1] -0.09108468
#> 
#> [[7]]$latitude
#> [1] 51.51629
#> 
#> [[7]]$northings
#> [1] 181434
#> 
#> [[7]]$eastings
#> [1] 532549
#> 
#> [[7]]$admin_district
#> [[7]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[7]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[7]]$parish
#> [[7]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[7]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[7]]$admin_county
#> list()
#> 
#> [[7]]$admin_ward
#> [[7]]$admin_ward[[1]]
#> [1] "Bassishaw"
#> 
#> [[7]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[7]]$admin_ward[[3]]
#> [1] "Cheap"
#> 
#> [[7]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[7]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[7]]$admin_ward[[6]]
#> [1] "Cordwainer"
#> 
#> [[7]]$admin_ward[[7]]
#> [1] "Cornhill"
#> 
#> [[7]]$admin_ward[[8]]
#> [1] "Walbrook"
#> 
#> 
#> [[7]]$country
#> [[7]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[7]]$parliamentary_constituency
#> [[7]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[7]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[8]]
#> [[8]]$outcode
#> [1] "EC2V"
#> 
#> [[8]]$longitude
#> [1] -0.09365719
#> 
#> [[8]]$latitude
#> [1] 51.51546
#> 
#> [[8]]$northings
#> [1] 181337
#> 
#> [[8]]$eastings
#> [1] 532373
#> 
#> [[8]]$admin_district
#> [[8]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[8]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[8]]$parish
#> [[8]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[8]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[8]]$admin_county
#> list()
#> 
#> [[8]]$admin_ward
#> [[8]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[8]]$admin_ward[[2]]
#> [1] "Bassishaw"
#> 
#> [[8]]$admin_ward[[3]]
#> [1] "Bread Street"
#> 
#> [[8]]$admin_ward[[4]]
#> [1] "Cheap"
#> 
#> [[8]]$admin_ward[[5]]
#> [1] "Clerkenwell"
#> 
#> [[8]]$admin_ward[[6]]
#> [1] "Coleman Street"
#> 
#> [[8]]$admin_ward[[7]]
#> [1] "Cordwainer"
#> 
#> [[8]]$admin_ward[[8]]
#> [1] "Walbrook"
#> 
#> 
#> [[8]]$country
#> [[8]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[8]]$parliamentary_constituency
#> [[8]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[8]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[9]]
#> [[9]]$outcode
#> [1] "EC1A"
#> 
#> [[9]]$longitude
#> [1] -0.1041297
#> 
#> [[9]]$latitude
#> [1] 51.52053
#> 
#> [[9]]$northings
#> [1] 181882
#> 
#> [[9]]$eastings
#> [1] 531632
#> 
#> [[9]]$admin_district
#> [[9]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[9]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[9]]$parish
#> [[9]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[9]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[9]]$admin_county
#> list()
#> 
#> [[9]]$admin_ward
#> [[9]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[9]]$admin_ward[[2]]
#> [1] "Bunhill"
#> 
#> [[9]]$admin_ward[[3]]
#> [1] "Cheap"
#> 
#> [[9]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[9]]$admin_ward[[5]]
#> [1] "Farringdon Within"
#> 
#> [[9]]$admin_ward[[6]]
#> [1] "Farringdon Without"
#> 
#> 
#> [[9]]$country
#> [[9]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[9]]$parliamentary_constituency
#> [[9]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[9]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[10]]
#> [[10]]$outcode
#> [1] "EC2N"
#> 
#> [[10]]$longitude
#> [1] -0.08581437
#> 
#> [[10]]$latitude
#> [1] 51.51579
#> 
#> [[10]]$northings
#> [1] 181388
#> 
#> [[10]]$eastings
#> [1] 532916
#> 
#> [[10]]$admin_district
#> [[10]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[10]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[10]]$parish
#> [[10]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[10]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[10]]$admin_county
#> list()
#> 
#> [[10]]$admin_ward
#> [[10]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[10]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[10]]$admin_ward[[3]]
#> [1] "Clerkenwell"
#> 
#> [[10]]$admin_ward[[4]]
#> [1] "Cornhill"
#> 
#> [[10]]$admin_ward[[5]]
#> [1] "Lime Street"
#> 
#> [[10]]$admin_ward[[6]]
#> [1] "Walbrook"
#> 
#> 
#> [[10]]$country
#> [[10]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[10]]$parliamentary_constituency
#> [[10]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[10]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[11]]
#> [[11]]$outcode
#> [1] "EC4M"
#> 
#> [[11]]$longitude
#> [1] -0.0995088
#> 
#> [[11]]$latitude
#> [1] 51.51432
#> 
#> [[11]]$northings
#> [1] 181200
#> 
#> [[11]]$eastings
#> [1] 531970
#> 
#> [[11]]$admin_district
#> [[11]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[11]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[11]]$parish
#> [[11]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[11]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[11]]$admin_county
#> list()
#> 
#> [[11]]$admin_ward
#> [[11]]$admin_ward[[1]]
#> [1] "Bread Street"
#> 
#> [[11]]$admin_ward[[2]]
#> [1] "Castle Baynard"
#> 
#> [[11]]$admin_ward[[3]]
#> [1] "Clerkenwell"
#> 
#> [[11]]$admin_ward[[4]]
#> [1] "Cordwainer"
#> 
#> [[11]]$admin_ward[[5]]
#> [1] "Farringdon Within"
#> 
#> [[11]]$admin_ward[[6]]
#> [1] "Vintry"
#> 
#> 
#> [[11]]$country
#> [[11]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[11]]$parliamentary_constituency
#> [[11]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[11]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
nearest_outcode("EC1Y", limit = 11, radius = 6000)
#> [[1]]
#> [[1]]$outcode
#> [1] "EC1Y"
#> 
#> [[1]]$longitude
#> [1] -0.0923844
#> 
#> [[1]]$latitude
#> [1] 51.52309
#> 
#> [[1]]$northings
#> [1] 182188
#> 
#> [[1]]$eastings
#> [1] 532439
#> 
#> [[1]]$admin_district
#> [[1]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[1]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[1]]$parish
#> [[1]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[1]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[1]]$admin_county
#> list()
#> 
#> [[1]]$admin_ward
#> [[1]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[1]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[1]]$admin_ward[[3]]
#> [1] "Coleman Street"
#> 
#> [[1]]$admin_ward[[4]]
#> [1] "Cripplegate"
#> 
#> 
#> [[1]]$country
#> [[1]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[1]]$parliamentary_constituency
#> [[1]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[1]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[2]]
#> [[2]]$outcode
#> [1] "EC2Y"
#> 
#> [[2]]$longitude
#> [1] -0.09354922
#> 
#> [[2]]$latitude
#> [1] 51.51947
#> 
#> [[2]]$northings
#> [1] 181783
#> 
#> [[2]]$eastings
#> [1] 532369
#> 
#> [[2]]$admin_district
#> [[2]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[2]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[2]]$parish
#> [[2]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[2]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[2]]$admin_county
#> list()
#> 
#> [[2]]$admin_ward
#> [[2]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[2]]$admin_ward[[2]]
#> [1] "Bassishaw"
#> 
#> [[2]]$admin_ward[[3]]
#> [1] "Bunhill"
#> 
#> [[2]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[2]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[2]]$admin_ward[[6]]
#> [1] "Cripplegate"
#> 
#> 
#> [[2]]$country
#> [[2]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[2]]$parliamentary_constituency
#> [[2]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[2]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[3]]
#> [[3]]$outcode
#> [1] "EC2A"
#> 
#> [[3]]$longitude
#> [1] -0.08542688
#> 
#> [[3]]$latitude
#> [1] 51.52367
#> 
#> [[3]]$northings
#> [1] 182265
#> 
#> [[3]]$eastings
#> [1] 532920
#> 
#> [[3]]$admin_district
#> [[3]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[3]]$admin_district[[2]]
#> [1] "Hackney"
#> 
#> [[3]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> 
#> [[3]]$parish
#> [[3]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[3]]$parish[[2]]
#> [1] "Hackney, unparished area"
#> 
#> [[3]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[3]]$admin_county
#> list()
#> 
#> [[3]]$admin_ward
#> [[3]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[3]]$admin_ward[[2]]
#> [1] "Bunhill"
#> 
#> [[3]]$admin_ward[[3]]
#> [1] "Clerkenwell"
#> 
#> [[3]]$admin_ward[[4]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> 
#> [[3]]$country
#> [[3]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[3]]$parliamentary_constituency
#> [[3]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[3]]$parliamentary_constituency[[2]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[3]]$parliamentary_constituency[[3]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[4]]
#> [[4]]$outcode
#> [1] "EC1V"
#> 
#> [[4]]$longitude
#> [1] -0.09777263
#> 
#> [[4]]$latitude
#> [1] 51.5268
#> 
#> [[4]]$northings
#> [1] 182590
#> 
#> [[4]]$eastings
#> [1] 532055
#> 
#> [[4]]$admin_district
#> [[4]]$admin_district[[1]]
#> [1] "Hackney"
#> 
#> [[4]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[4]]$parish
#> [[4]]$parish[[1]]
#> [1] "Hackney, unparished area"
#> 
#> [[4]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[4]]$admin_county
#> list()
#> 
#> [[4]]$admin_ward
#> [[4]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[4]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[4]]$admin_ward[[3]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> [[4]]$admin_ward[[4]]
#> [1] "Hoxton West"
#> 
#> [[4]]$admin_ward[[5]]
#> [1] "St Peter's & Canalside"
#> 
#> 
#> [[4]]$country
#> [[4]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[4]]$parliamentary_constituency
#> [[4]]$parliamentary_constituency[[1]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[4]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[5]]
#> [[5]]$outcode
#> [1] "EC2M"
#> 
#> [[5]]$longitude
#> [1] -0.0861603
#> 
#> [[5]]$latitude
#> [1] 51.51857
#> 
#> [[5]]$northings
#> [1] 181697
#> 
#> [[5]]$eastings
#> [1] 532884
#> 
#> [[5]]$admin_district
#> [[5]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[5]]$admin_district[[2]]
#> [1] "Hackney"
#> 
#> [[5]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> [[5]]$admin_district[[4]]
#> [1] "Tower Hamlets"
#> 
#> 
#> [[5]]$parish
#> [[5]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[5]]$parish[[2]]
#> [1] "Hackney, unparished area"
#> 
#> [[5]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> [[5]]$parish[[4]]
#> [1] "Tower Hamlets, unparished area"
#> 
#> 
#> [[5]]$admin_county
#> list()
#> 
#> [[5]]$admin_ward
#> [[5]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[5]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[5]]$admin_ward[[3]]
#> [1] "Bunhill"
#> 
#> [[5]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[5]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[5]]$admin_ward[[6]]
#> [1] "Cornhill"
#> 
#> [[5]]$admin_ward[[7]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> [[5]]$admin_ward[[8]]
#> [1] "Spitalfields & Banglatown"
#> 
#> 
#> [[5]]$country
#> [[5]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[5]]$parliamentary_constituency
#> [[5]]$parliamentary_constituency[[1]]
#> [1] "Bethnal Green and Stepney"
#> 
#> [[5]]$parliamentary_constituency[[2]]
#> [1] "Cities of London and Westminster"
#> 
#> [[5]]$parliamentary_constituency[[3]]
#> [1] "Hackney South and Shoreditch"
#> 
#> [[5]]$parliamentary_constituency[[4]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[6]]
#> [[6]]$outcode
#> [1] "EC1M"
#> 
#> [[6]]$longitude
#> [1] -0.1023023
#> 
#> [[6]]$latitude
#> [1] 51.52129
#> 
#> [[6]]$northings
#> [1] 181970
#> 
#> [[6]]$eastings
#> [1] 531756
#> 
#> [[6]]$admin_district
#> [[6]]$admin_district[[1]]
#> [1] "Camden"
#> 
#> [[6]]$admin_district[[2]]
#> [1] "City of London"
#> 
#> [[6]]$admin_district[[3]]
#> [1] "Islington"
#> 
#> 
#> [[6]]$parish
#> [[6]]$parish[[1]]
#> [1] "Camden, unparished area"
#> 
#> [[6]]$parish[[2]]
#> [1] "City of London, unparished area"
#> 
#> [[6]]$parish[[3]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[6]]$admin_county
#> list()
#> 
#> [[6]]$admin_ward
#> [[6]]$admin_ward[[1]]
#> [1] "Bunhill"
#> 
#> [[6]]$admin_ward[[2]]
#> [1] "Clerkenwell"
#> 
#> [[6]]$admin_ward[[3]]
#> [1] "Cripplegate"
#> 
#> [[6]]$admin_ward[[4]]
#> [1] "Farringdon Within"
#> 
#> [[6]]$admin_ward[[5]]
#> [1] "Farringdon Without"
#> 
#> [[6]]$admin_ward[[6]]
#> [1] "Holborn & Covent Garden"
#> 
#> 
#> [[6]]$country
#> [[6]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[6]]$parliamentary_constituency
#> [[6]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[6]]$parliamentary_constituency[[2]]
#> [1] "Holborn and St Pancras"
#> 
#> [[6]]$parliamentary_constituency[[3]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[7]]
#> [[7]]$outcode
#> [1] "EC2R"
#> 
#> [[7]]$longitude
#> [1] -0.09108468
#> 
#> [[7]]$latitude
#> [1] 51.51629
#> 
#> [[7]]$northings
#> [1] 181434
#> 
#> [[7]]$eastings
#> [1] 532549
#> 
#> [[7]]$admin_district
#> [[7]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[7]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[7]]$parish
#> [[7]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[7]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[7]]$admin_county
#> list()
#> 
#> [[7]]$admin_ward
#> [[7]]$admin_ward[[1]]
#> [1] "Bassishaw"
#> 
#> [[7]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[7]]$admin_ward[[3]]
#> [1] "Cheap"
#> 
#> [[7]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[7]]$admin_ward[[5]]
#> [1] "Coleman Street"
#> 
#> [[7]]$admin_ward[[6]]
#> [1] "Cordwainer"
#> 
#> [[7]]$admin_ward[[7]]
#> [1] "Cornhill"
#> 
#> [[7]]$admin_ward[[8]]
#> [1] "Walbrook"
#> 
#> 
#> [[7]]$country
#> [[7]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[7]]$parliamentary_constituency
#> [[7]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[7]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[8]]
#> [[8]]$outcode
#> [1] "EC2V"
#> 
#> [[8]]$longitude
#> [1] -0.09365719
#> 
#> [[8]]$latitude
#> [1] 51.51546
#> 
#> [[8]]$northings
#> [1] 181337
#> 
#> [[8]]$eastings
#> [1] 532373
#> 
#> [[8]]$admin_district
#> [[8]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[8]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[8]]$parish
#> [[8]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[8]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[8]]$admin_county
#> list()
#> 
#> [[8]]$admin_ward
#> [[8]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[8]]$admin_ward[[2]]
#> [1] "Bassishaw"
#> 
#> [[8]]$admin_ward[[3]]
#> [1] "Bread Street"
#> 
#> [[8]]$admin_ward[[4]]
#> [1] "Cheap"
#> 
#> [[8]]$admin_ward[[5]]
#> [1] "Clerkenwell"
#> 
#> [[8]]$admin_ward[[6]]
#> [1] "Coleman Street"
#> 
#> [[8]]$admin_ward[[7]]
#> [1] "Cordwainer"
#> 
#> [[8]]$admin_ward[[8]]
#> [1] "Walbrook"
#> 
#> 
#> [[8]]$country
#> [[8]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[8]]$parliamentary_constituency
#> [[8]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[8]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[9]]
#> [[9]]$outcode
#> [1] "EC1A"
#> 
#> [[9]]$longitude
#> [1] -0.1041297
#> 
#> [[9]]$latitude
#> [1] 51.52053
#> 
#> [[9]]$northings
#> [1] 181882
#> 
#> [[9]]$eastings
#> [1] 531632
#> 
#> [[9]]$admin_district
#> [[9]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[9]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[9]]$parish
#> [[9]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[9]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[9]]$admin_county
#> list()
#> 
#> [[9]]$admin_ward
#> [[9]]$admin_ward[[1]]
#> [1] "Aldersgate"
#> 
#> [[9]]$admin_ward[[2]]
#> [1] "Bunhill"
#> 
#> [[9]]$admin_ward[[3]]
#> [1] "Cheap"
#> 
#> [[9]]$admin_ward[[4]]
#> [1] "Clerkenwell"
#> 
#> [[9]]$admin_ward[[5]]
#> [1] "Farringdon Within"
#> 
#> [[9]]$admin_ward[[6]]
#> [1] "Farringdon Without"
#> 
#> 
#> [[9]]$country
#> [[9]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[9]]$parliamentary_constituency
#> [[9]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[9]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[10]]
#> [[10]]$outcode
#> [1] "EC2N"
#> 
#> [[10]]$longitude
#> [1] -0.08581437
#> 
#> [[10]]$latitude
#> [1] 51.51579
#> 
#> [[10]]$northings
#> [1] 181388
#> 
#> [[10]]$eastings
#> [1] 532916
#> 
#> [[10]]$admin_district
#> [[10]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[10]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[10]]$parish
#> [[10]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[10]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[10]]$admin_county
#> list()
#> 
#> [[10]]$admin_ward
#> [[10]]$admin_ward[[1]]
#> [1] "Bishopsgate"
#> 
#> [[10]]$admin_ward[[2]]
#> [1] "Broad Street"
#> 
#> [[10]]$admin_ward[[3]]
#> [1] "Clerkenwell"
#> 
#> [[10]]$admin_ward[[4]]
#> [1] "Cornhill"
#> 
#> [[10]]$admin_ward[[5]]
#> [1] "Lime Street"
#> 
#> [[10]]$admin_ward[[6]]
#> [1] "Walbrook"
#> 
#> 
#> [[10]]$country
#> [[10]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[10]]$parliamentary_constituency
#> [[10]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[10]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
#> [[11]]
#> [[11]]$outcode
#> [1] "EC4M"
#> 
#> [[11]]$longitude
#> [1] -0.0995088
#> 
#> [[11]]$latitude
#> [1] 51.51432
#> 
#> [[11]]$northings
#> [1] 181200
#> 
#> [[11]]$eastings
#> [1] 531970
#> 
#> [[11]]$admin_district
#> [[11]]$admin_district[[1]]
#> [1] "City of London"
#> 
#> [[11]]$admin_district[[2]]
#> [1] "Islington"
#> 
#> 
#> [[11]]$parish
#> [[11]]$parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> [[11]]$parish[[2]]
#> [1] "Islington, unparished area"
#> 
#> 
#> [[11]]$admin_county
#> list()
#> 
#> [[11]]$admin_ward
#> [[11]]$admin_ward[[1]]
#> [1] "Bread Street"
#> 
#> [[11]]$admin_ward[[2]]
#> [1] "Castle Baynard"
#> 
#> [[11]]$admin_ward[[3]]
#> [1] "Clerkenwell"
#> 
#> [[11]]$admin_ward[[4]]
#> [1] "Cordwainer"
#> 
#> [[11]]$admin_ward[[5]]
#> [1] "Farringdon Within"
#> 
#> [[11]]$admin_ward[[6]]
#> [1] "Vintry"
#> 
#> 
#> [[11]]$country
#> [[11]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[11]]$parliamentary_constituency
#> [[11]]$parliamentary_constituency[[1]]
#> [1] "Cities of London and Westminster"
#> 
#> [[11]]$parliamentary_constituency[[2]]
#> [1] "Islington South and Finsbury"
#> 
#> 
#> 
# }
```
