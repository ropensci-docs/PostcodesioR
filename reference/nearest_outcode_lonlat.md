# Nearest outcodes given longitude and latitude

Returns nearest outward codes for a given longitude and latitude. The
search is based on the relative distance of the outcode centroid.

## Usage

``` r
nearest_outcode_lonlat(longitude, latitude)
```

## Arguments

- longitude:

  A string or numeric. Needs to have at least three decimal points.

- latitude:

  A string or numeric. Needs to have at least three decimal points.

## Value

A list with available data.

## See also

[`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
nearest_outcode_lonlat(0.127, 51.507)
#> [[1]]
#> [[1]]$outcode
#> [1] "DA18"
#> 
#> [[1]]$longitude
#> [1] 0.1362886
#> 
#> [[1]]$latitude
#> [1] 51.49428
#> 
#> [[1]]$northings
#> [1] 179423
#> 
#> [[1]]$eastings
#> [1] 548396
#> 
#> [[1]]$admin_district
#> [[1]]$admin_district[[1]]
#> [1] "Bexley"
#> 
#> 
#> [[1]]$parish
#> [[1]]$parish[[1]]
#> [1] "Bexley, unparished area"
#> 
#> 
#> [[1]]$admin_county
#> list()
#> 
#> [[1]]$admin_ward
#> [[1]]$admin_ward[[1]]
#> [1] "Slade Green & Northend"
#> 
#> [[1]]$admin_ward[[2]]
#> [1] "Thamesmead East"
#> 
#> 
#> [[1]]$country
#> [[1]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[1]]$parliamentary_constituency
#> [[1]]$parliamentary_constituency[[1]]
#> [1] "Bexleyheath and Crayford"
#> 
#> [[1]]$parliamentary_constituency[[2]]
#> [1] "Erith and Thamesmead"
#> 
#> 
#> 
#> [[2]]
#> [[2]]$outcode
#> [1] "SE28"
#> 
#> [[2]]$longitude
#> [1] 0.1036007
#> 
#> [[2]]$latitude
#> [1] 51.50198
#> 
#> [[2]]$northings
#> [1] 180213
#> 
#> [[2]]$eastings
#> [1] 546102
#> 
#> [[2]]$admin_district
#> [[2]]$admin_district[[1]]
#> [1] "Bexley"
#> 
#> [[2]]$admin_district[[2]]
#> [1] "Greenwich"
#> 
#> 
#> [[2]]$parish
#> [[2]]$parish[[1]]
#> [1] "Bexley, unparished area"
#> 
#> [[2]]$parish[[2]]
#> [1] "Greenwich, unparished area"
#> 
#> 
#> [[2]]$admin_county
#> list()
#> 
#> [[2]]$admin_ward
#> [[2]]$admin_ward[[1]]
#> [1] "Plumstead & Glyndon"
#> 
#> [[2]]$admin_ward[[2]]
#> [1] "Thamesmead East"
#> 
#> [[2]]$admin_ward[[3]]
#> [1] "Thamesmead Moorings"
#> 
#> [[2]]$admin_ward[[4]]
#> [1] "West Thamesmead"
#> 
#> 
#> [[2]]$country
#> [[2]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[2]]$parliamentary_constituency
#> [[2]]$parliamentary_constituency[[1]]
#> [1] "Erith and Thamesmead"
#> 
#> 
#> 
#> [[3]]
#> [[3]]$outcode
#> [1] "SE2"
#> 
#> [[3]]$longitude
#> [1] 0.1162492
#> 
#> [[3]]$latitude
#> [1] 51.48989
#> 
#> [[3]]$northings
#> [1] 178894
#> 
#> [[3]]$eastings
#> [1] 547019
#> 
#> [[3]]$admin_district
#> [[3]]$admin_district[[1]]
#> [1] "Bexley"
#> 
#> [[3]]$admin_district[[2]]
#> [1] "Greenwich"
#> 
#> 
#> [[3]]$parish
#> [[3]]$parish[[1]]
#> [1] "Bexley, unparished area"
#> 
#> [[3]]$parish[[2]]
#> [1] "Greenwich, unparished area"
#> 
#> 
#> [[3]]$admin_county
#> list()
#> 
#> [[3]]$admin_ward
#> [[3]]$admin_ward[[1]]
#> [1] "Abbey Wood"
#> 
#> [[3]]$admin_ward[[2]]
#> [1] "Belvedere"
#> 
#> [[3]]$admin_ward[[3]]
#> [1] "Plumstead Common"
#> 
#> [[3]]$admin_ward[[4]]
#> [1] "Plumstead & Glyndon"
#> 
#> [[3]]$admin_ward[[5]]
#> [1] "Thamesmead East"
#> 
#> [[3]]$admin_ward[[6]]
#> [1] "West Heath"
#> 
#> [[3]]$admin_ward[[7]]
#> [1] "West Thamesmead"
#> 
#> 
#> [[3]]$country
#> [[3]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[3]]$parliamentary_constituency
#> [[3]]$parliamentary_constituency[[1]]
#> [1] "Bexleyheath and Crayford"
#> 
#> [[3]]$parliamentary_constituency[[2]]
#> [1] "Erith and Thamesmead"
#> 
#> 
#> 
#> [[4]]
#> [[4]]$outcode
#> [1] "DA17"
#> 
#> [[4]]$longitude
#> [1] 0.1487898
#> 
#> [[4]]$latitude
#> [1] 51.4865
#> 
#> [[4]]$northings
#> [1] 178583
#> 
#> [[4]]$eastings
#> [1] 549289
#> 
#> [[4]]$admin_district
#> [[4]]$admin_district[[1]]
#> [1] "Bexley"
#> 
#> [[4]]$admin_district[[2]]
#> [1] "Dartford"
#> 
#> 
#> [[4]]$parish
#> [[4]]$parish[[1]]
#> [1] "Bexley, unparished area"
#> 
#> [[4]]$parish[[2]]
#> [1] "Dartford, unparished area"
#> 
#> 
#> [[4]]$admin_county
#> [[4]]$admin_county[[1]]
#> [1] "Kent"
#> 
#> 
#> [[4]]$admin_ward
#> [[4]]$admin_ward[[1]]
#> [1] "Belvedere"
#> 
#> [[4]]$admin_ward[[2]]
#> [1] "Erith"
#> 
#> [[4]]$admin_ward[[3]]
#> [1] "Northumberland Heath"
#> 
#> [[4]]$admin_ward[[4]]
#> [1] "West Heath"
#> 
#> [[4]]$admin_ward[[5]]
#> [1] "West Hill"
#> 
#> 
#> [[4]]$country
#> [[4]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[4]]$parliamentary_constituency
#> [[4]]$parliamentary_constituency[[1]]
#> [1] "Bexleyheath and Crayford"
#> 
#> [[4]]$parliamentary_constituency[[2]]
#> [1] "Dartford"
#> 
#> [[4]]$parliamentary_constituency[[3]]
#> [1] "Erith and Thamesmead"
#> 
#> 
#> 
#> [[5]]
#> [[5]]$outcode
#> [1] "RM9"
#> 
#> [[5]]$longitude
#> [1] 0.1346229
#> 
#> [[5]]$latitude
#> [1] 51.54023
#> 
#> [[5]]$northings
#> [1] 184529
#> 
#> [[5]]$eastings
#> [1] 548131
#> 
#> [[5]]$admin_district
#> [[5]]$admin_district[[1]]
#> [1] "Barking and Dagenham"
#> 
#> [[5]]$admin_district[[2]]
#> [1] "Havering"
#> 
#> 
#> [[5]]$parish
#> [[5]]$parish[[1]]
#> [1] "Barking and Dagenham, unparished area"
#> 
#> [[5]]$parish[[2]]
#> [1] "Havering, unparished area"
#> 
#> 
#> [[5]]$admin_county
#> list()
#> 
#> [[5]]$admin_ward
#> [[5]]$admin_ward[[1]]
#> [1] "Barking Riverside"
#> 
#> [[5]]$admin_ward[[2]]
#> [1] "Beam"
#> 
#> [[5]]$admin_ward[[3]]
#> [1] "Beam Park"
#> 
#> [[5]]$admin_ward[[4]]
#> [1] "Eastbury"
#> 
#> [[5]]$admin_ward[[5]]
#> [1] "Goresbrook"
#> 
#> [[5]]$admin_ward[[6]]
#> [1] "Heath"
#> 
#> [[5]]$admin_ward[[7]]
#> [1] "Mayesbrook"
#> 
#> [[5]]$admin_ward[[8]]
#> [1] "Parsloes"
#> 
#> 
#> [[5]]$country
#> [[5]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[5]]$parliamentary_constituency
#> [[5]]$parliamentary_constituency[[1]]
#> [1] "Barking"
#> 
#> [[5]]$parliamentary_constituency[[2]]
#> [1] "Dagenham and Rainham"
#> 
#> 
#> 
#> [[6]]
#> [[6]]$outcode
#> [1] "IG11"
#> 
#> [[6]]$longitude
#> [1] 0.09383749
#> 
#> [[6]]$latitude
#> [1] 51.53444
#> 
#> [[6]]$northings
#> [1] 183803
#> 
#> [[6]]$eastings
#> [1] 545321
#> 
#> [[6]]$admin_district
#> [[6]]$admin_district[[1]]
#> [1] "Barking and Dagenham"
#> 
#> [[6]]$admin_district[[2]]
#> [1] "Newham"
#> 
#> [[6]]$admin_district[[3]]
#> [1] "Redbridge"
#> 
#> 
#> [[6]]$parish
#> [[6]]$parish[[1]]
#> [1] "Barking and Dagenham, unparished area"
#> 
#> [[6]]$parish[[2]]
#> [1] "Newham, unparished area"
#> 
#> [[6]]$parish[[3]]
#> [1] "Redbridge, unparished area"
#> 
#> 
#> [[6]]$admin_county
#> list()
#> 
#> [[6]]$admin_ward
#> [[6]]$admin_ward[[1]]
#> [1] "Abbey"
#> 
#> [[6]]$admin_ward[[2]]
#> [1] "Barking Riverside"
#> 
#> [[6]]$admin_ward[[3]]
#> [1] "Beckton"
#> 
#> [[6]]$admin_ward[[4]]
#> [1] "Eastbury"
#> 
#> [[6]]$admin_ward[[5]]
#> [1] "East Ham South"
#> 
#> [[6]]$admin_ward[[6]]
#> [1] "Gascoigne"
#> 
#> [[6]]$admin_ward[[7]]
#> [1] "Longbridge"
#> 
#> [[6]]$admin_ward[[8]]
#> [1] "Mayesbrook"
#> 
#> [[6]]$admin_ward[[9]]
#> [1] "Mayfield"
#> 
#> [[6]]$admin_ward[[10]]
#> [1] "Northbury"
#> 
#> [[6]]$admin_ward[[11]]
#> [1] "Thames View"
#> 
#> 
#> [[6]]$country
#> [[6]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[6]]$parliamentary_constituency
#> [[6]]$parliamentary_constituency[[1]]
#> [1] "Barking"
#> 
#> [[6]]$parliamentary_constituency[[2]]
#> [1] "East Ham"
#> 
#> [[6]]$parliamentary_constituency[[3]]
#> [1] "Ilford South"
#> 
#> [[6]]$parliamentary_constituency[[4]]
#> [1] "West Ham and Beckton"
#> 
#> 
#> 
#> [[7]]
#> [[7]]$outcode
#> [1] "SE18"
#> 
#> [[7]]$longitude
#> [1] 0.07234797
#> 
#> [[7]]$latitude
#> [1] 51.48448
#> 
#> [[7]]$northings
#> [1] 178206
#> 
#> [[7]]$eastings
#> [1] 543988
#> 
#> [[7]]$admin_district
#> [[7]]$admin_district[[1]]
#> [1] "Greenwich"
#> 
#> 
#> [[7]]$parish
#> [[7]]$parish[[1]]
#> [1] "Greenwich, unparished area"
#> 
#> 
#> [[7]]$admin_county
#> list()
#> 
#> [[7]]$admin_ward
#> [[7]]$admin_ward[[1]]
#> [1] "Charlton Hornfair"
#> 
#> [[7]]$admin_ward[[2]]
#> [1] "Charlton Village & Riverside"
#> 
#> [[7]]$admin_ward[[3]]
#> [1] "Kidbrooke Park"
#> 
#> [[7]]$admin_ward[[4]]
#> [1] "Plumstead Common"
#> 
#> [[7]]$admin_ward[[5]]
#> [1] "Plumstead & Glyndon"
#> 
#> [[7]]$admin_ward[[6]]
#> [1] "Shooters Hill"
#> 
#> [[7]]$admin_ward[[7]]
#> [1] "West Thamesmead"
#> 
#> [[7]]$admin_ward[[8]]
#> [1] "Woolwich Arsenal"
#> 
#> [[7]]$admin_ward[[9]]
#> [1] "Woolwich Common"
#> 
#> [[7]]$admin_ward[[10]]
#> [1] "Woolwich Dockyard"
#> 
#> 
#> [[7]]$country
#> [[7]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[7]]$parliamentary_constituency
#> [[7]]$parliamentary_constituency[[1]]
#> [1] "Eltham and Chislehurst"
#> 
#> [[7]]$parliamentary_constituency[[2]]
#> [1] "Erith and Thamesmead"
#> 
#> [[7]]$parliamentary_constituency[[3]]
#> [1] "Greenwich and Woolwich"
#> 
#> 
#> 
#> [[8]]
#> [[8]]$outcode
#> [1] "RM10"
#> 
#> [[8]]$longitude
#> [1] 0.1579097
#> 
#> [[8]]$latitude
#> [1] 51.54489
#> 
#> [[8]]$northings
#> [1] 185095
#> 
#> [[8]]$eastings
#> [1] 549730
#> 
#> [[8]]$admin_district
#> [[8]]$admin_district[[1]]
#> [1] "Barking and Dagenham"
#> 
#> 
#> [[8]]$parish
#> [[8]]$parish[[1]]
#> [1] "Barking and Dagenham, unparished area"
#> 
#> 
#> [[8]]$admin_county
#> list()
#> 
#> [[8]]$admin_ward
#> [[8]]$admin_ward[[1]]
#> [1] "Alibon"
#> 
#> [[8]]$admin_ward[[2]]
#> [1] "Beam"
#> 
#> [[8]]$admin_ward[[3]]
#> [1] "Eastbrook & Rush Green"
#> 
#> [[8]]$admin_ward[[4]]
#> [1] "Heath"
#> 
#> [[8]]$admin_ward[[5]]
#> [1] "Parsloes"
#> 
#> [[8]]$admin_ward[[6]]
#> [1] "Village"
#> 
#> 
#> [[8]]$country
#> [[8]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[8]]$parliamentary_constituency
#> [[8]]$parliamentary_constituency[[1]]
#> [1] "Barking"
#> 
#> [[8]]$parliamentary_constituency[[2]]
#> [1] "Dagenham and Rainham"
#> 
#> 
#> 
#> [[9]]
#> [[9]]$outcode
#> [1] "DA7"
#> 
#> [[9]]$longitude
#> [1] 0.1461987
#> 
#> [[9]]$latitude
#> [1] 51.46566
#> 
#> [[9]]$northings
#> [1] 176260
#> 
#> [[9]]$eastings
#> [1] 549177
#> 
#> [[9]]$admin_district
#> [[9]]$admin_district[[1]]
#> [1] "Bexley"
#> 
#> 
#> [[9]]$parish
#> [[9]]$parish[[1]]
#> [1] "Bexley, unparished area"
#> 
#> 
#> [[9]]$admin_county
#> list()
#> 
#> [[9]]$admin_ward
#> [[9]]$admin_ward[[1]]
#> [1] "Barnehurst"
#> 
#> [[9]]$admin_ward[[2]]
#> [1] "Bexleyheath"
#> 
#> [[9]]$admin_ward[[3]]
#> [1] "Crayford"
#> 
#> [[9]]$admin_ward[[4]]
#> [1] "Crook Log"
#> 
#> [[9]]$admin_ward[[5]]
#> [1] "Northumberland Heath"
#> 
#> [[9]]$admin_ward[[6]]
#> [1] "West Heath"
#> 
#> 
#> [[9]]$country
#> [[9]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[9]]$parliamentary_constituency
#> [[9]]$parliamentary_constituency[[1]]
#> [1] "Bexleyheath and Crayford"
#> 
#> 
#> 
#> [[10]]
#> [[10]]$outcode
#> [1] "DA8"
#> 
#> [[10]]$longitude
#> [1] 0.1755844
#> 
#> [[10]]$latitude
#> [1] 51.47576
#> 
#> [[10]]$northings
#> [1] 177444
#> 
#> [[10]]$eastings
#> [1] 551184
#> 
#> [[10]]$admin_district
#> [[10]]$admin_district[[1]]
#> [1] "Bexley"
#> 
#> 
#> [[10]]$parish
#> [[10]]$parish[[1]]
#> [1] "Bexley, unparished area"
#> 
#> 
#> [[10]]$admin_county
#> list()
#> 
#> [[10]]$admin_ward
#> [[10]]$admin_ward[[1]]
#> [1] "Barnehurst"
#> 
#> [[10]]$admin_ward[[2]]
#> [1] "Belvedere"
#> 
#> [[10]]$admin_ward[[3]]
#> [1] "Erith"
#> 
#> [[10]]$admin_ward[[4]]
#> [1] "Northumberland Heath"
#> 
#> [[10]]$admin_ward[[5]]
#> [1] "Slade Green & Northend"
#> 
#> 
#> [[10]]$country
#> [[10]]$country[[1]]
#> [1] "England"
#> 
#> 
#> [[10]]$parliamentary_constituency
#> [[10]]$parliamentary_constituency[[1]]
#> [1] "Bexleyheath and Crayford"
#> 
#> [[10]]$parliamentary_constituency[[2]]
#> [1] "Erith and Thamesmead"
#> 
#> 
#> 
# }
```
