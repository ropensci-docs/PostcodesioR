# Terminated postcode lookup

Returns month and year if a postcode was terminated or is no longer
active.

## Usage

``` r
terminated_postcode(postcode)
```

## Arguments

- postcode:

  A string. Terminated UK postcode.

## Value

A data frame with data about terminated postcode. NULL if postcode is
active.

- `postcode` Postcode. All currently terminated postcodes within the
  United Kingdom, the Channel Islands and the Isle of Man, received
  every 3 months from Royal Mail. 2, 3 or 4-character outward code,
  single space and 3-character inward code.

- `year_terminated` Termination year. Year of termination of a postcode.

- `month_terminated` Termination month. Month of termination of a
  postcode. 1-January, 2-February, ..., 12-December.

- `longitude` Longitude. The WGS84 longitude given the Postcode's
  national grid reference.

- `latitude` Latitude. The WGS84 latitude given the Postcode's national
  grid reference.

See <https://postcodes.io/docs> for more details.

## Examples

``` r
# \donttest{
terminated_postcode("EC1Y 8LX") # existing postcode
#> Warning: Not Found (HTTP 404).
terminated_postcode("E1W 1UU") # terminated postcode
#>   postcode year_terminated month_terminated eastings northings longitude
#> 1  E1W 1UU            2015                2   533779    180545 -0.073706
#>   latitude
#> 1 51.50801
# }
```
