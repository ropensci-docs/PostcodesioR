# Postcode validation

Convenience method to validate a postcode.

## Usage

``` r
postcode_validation(postcode)
```

## Arguments

- postcode:

  A string. Valid UK postcode.

## Value

A logical vector: True or False (meaning respectively valid or invalid
postcode).

## Examples

``` r
# \donttest{
postcode_validation("EC1Y 8LX") # returns TRUE
#> [1] TRUE
postcode_validation("XYZ") # returns FALSE
#> [1] FALSE
# }
```
