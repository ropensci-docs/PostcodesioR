# Random place

Returns a random place and all associated data

## Usage

``` r
random_place()
```

## Value

A data frame describing a random place and all associated data.

## See also

[`place_lookup`](https://docs.ropensci.org/PostcodesioR/reference/place_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
random_place()
#>                   code     name_1 name_1_lang name_2 name_2_lang    local_type
#> 1 osgb4000000074541997 Woodbottom        NULL   NULL        NULL Suburban Area
#>   outcode county_unitary county_unitary_type district_borough
#> 1    WF14           NULL                NULL         Kirklees
#>   district_borough_type                   region country longitude latitude
#> 1  MetropolitanDistrict Yorkshire and the Humber England -1.682318 53.66268
#>   eastings northings min_eastings min_northings max_eastings max_northings
#> 1   421090    418513       420843        417987       421371        418971
# }
```
