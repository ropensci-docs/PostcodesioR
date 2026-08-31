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
#>                   code name_1 name_1_lang name_2 name_2_lang local_type outcode
#> 1 osgb4000000074566282 Lupton        NULL   NULL        NULL    Village     LA6
#>            county_unitary county_unitary_type district_borough
#> 1 Westmorland and Furness    UnitaryAuthority             NULL
#>   district_borough_type     region country longitude latitude eastings
#> 1                  NULL North West England -2.675273 54.21943   356066
#>   northings min_eastings min_northings max_eastings max_northings
#> 1    480622       354942        480295       357304        481625
# }
```
