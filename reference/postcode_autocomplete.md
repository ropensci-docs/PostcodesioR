# Postcode autocomplete

Returns a data frame of matching postcodes.

## Usage

``` r
postcode_autocomplete(postcode, limit = 10)
```

## Arguments

- postcode:

  A string. Valid UK postcode.

- limit:

  An integer. Limits number of postcodes matches to return. Defaults
  to 10. Needs to be less than 100.

## Value

A data frame with suggested postcodes.

## Examples

``` r
# \donttest{
postcode_autocomplete("E1")
#>    postcode
#> 1   E10 5AB
#> 2   E10 5AD
#> 3   E10 5AH
#> 4   E10 5AJ
#> 5   E10 5AL
#> 6   E10 5AN
#> 7   E10 5AP
#> 8   E10 5AR
#> 9   E10 5AS
#> 10  E10 5AT
postcode_autocomplete("E1", limit = 11)
#>    postcode
#> 1   E10 5AB
#> 2   E10 5AD
#> 3   E10 5AH
#> 4   E10 5AJ
#> 5   E10 5AL
#> 6   E10 5AN
#> 7   E10 5AP
#> 8   E10 5AR
#> 9   E10 5AS
#> 10  E10 5AT
#> 11  E10 5AU
# }
```
