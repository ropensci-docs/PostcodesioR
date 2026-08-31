# Outward code lookup

Geolocation data for the centroid of the outward code specified.

## Usage

``` r
outward_code_lookup(outcode)
```

## Arguments

- outcode:

  A string. The outward code representing the first half of any postcode
  (separated by a space).

## Value

The list of geographical properties.

## See also

[`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
outward_code_lookup("E1")
#> $outcode
#> [1] "E1"
#> 
#> $longitude
#> [1] -0.059378
#> 
#> $latitude
#> [1] 51.51738
#> 
#> $northings
#> [1] 181614
#> 
#> $eastings
#> [1] 534746
#> 
#> $admin_district
#> $admin_district[[1]]
#> [1] "City of London"
#> 
#> $admin_district[[2]]
#> [1] "Hackney"
#> 
#> $admin_district[[3]]
#> [1] "Tower Hamlets"
#> 
#> 
#> $parish
#> $parish[[1]]
#> [1] "City of London, unparished area"
#> 
#> $parish[[2]]
#> [1] "Hackney, unparished area"
#> 
#> $parish[[3]]
#> [1] "Tower Hamlets, unparished area"
#> 
#> 
#> $admin_county
#> list()
#> 
#> $admin_ward
#> $admin_ward[[1]]
#> [1] "Aldgate"
#> 
#> $admin_ward[[2]]
#> [1] "Bethnal Green East"
#> 
#> $admin_ward[[3]]
#> [1] "Bethnal Green West"
#> 
#> $admin_ward[[4]]
#> [1] "Bishopsgate"
#> 
#> $admin_ward[[5]]
#> [1] "Bow West"
#> 
#> $admin_ward[[6]]
#> [1] "Hoxton East & Shoreditch"
#> 
#> $admin_ward[[7]]
#> [1] "Portsoken"
#> 
#> $admin_ward[[8]]
#> [1] "Shadwell"
#> 
#> $admin_ward[[9]]
#> [1] "Spitalfields & Banglatown"
#> 
#> $admin_ward[[10]]
#> [1] "St Dunstan's"
#> 
#> $admin_ward[[11]]
#> [1] "Stepney Green"
#> 
#> $admin_ward[[12]]
#> [1] "Tower"
#> 
#> $admin_ward[[13]]
#> [1] "Weavers"
#> 
#> $admin_ward[[14]]
#> [1] "Whitechapel"
#> 
#> 
#> $country
#> $country[[1]]
#> [1] "England"
#> 
#> 
#> $parliamentary_constituency
#> $parliamentary_constituency[[1]]
#> [1] "Bethnal Green and Stepney"
#> 
#> $parliamentary_constituency[[2]]
#> [1] "Cities of London and Westminster"
#> 
#> $parliamentary_constituency[[3]]
#> [1] "Hackney South and Shoreditch"
#> 
#> $parliamentary_constituency[[4]]
#> [1] "Stratford and Bow"
#> 
#> 
# }
```
