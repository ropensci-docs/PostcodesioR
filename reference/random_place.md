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
#>                   code    name_1 name_1_lang name_2 name_2_lang    local_type
#> 1 osgb4000000074548361 Manselton        NULL   NULL        NULL Suburban Area
#>   outcode     county_unitary county_unitary_type district_borough
#> 1     SA5 Abertawe - Swansea    UnitaryAuthority             NULL
#>   district_borough_type region country longitude latitude eastings northings
#> 1                  NULL  Wales   Wales -3.953319 51.64258   264937    195561
#>   min_eastings min_northings max_eastings max_northings
#> 1       264726        194801       265508        195716
# }
```
