# Place lookup

Lookup a place by code. Returns all available data if found. Returns 404
if a place does not exist.

## Usage

``` r
place_lookup(code)
```

## Arguments

- code:

  A string. The unique identifier for places - Ordnance Survey (OSGB)
  code.

## Value

A list with available places.

- `code` A unique identifier that enables records to be identified
  easily. The identifier will be persistent for all LocalTypes except
  Section of Named Road and Section of Numbered Road.

- `name_1` Name. The proper noun that applies to the real world entity.
  Names that are prefixed by the definite article are not formatted for
  alphabetical sorting, that is, 'The Pennines' not 'Pennines, The'.

- `name_1_lang` Language of Name. The language type is only set where
  more than one name exists E.g. cym (Welsh), eng (English), gla
  (Scottish Gaelic).

- `name_2` Name (in case of multiple languages). The proper noun that
  applies to the real world entity. Names that are prefixed by the
  definite article are not formatted for alphabetical sorting, that is,
  'The Pennines' not 'Pennines, The'.

- `name_2_lang` Language of Name. The language type is only set where
  more than one name exists E.g. cym (Welsh), eng (English), gla
  (Scottish Gaelic).

- `local_type` The Ordnance Survey classification for the named place
  being represented by the specific feature. E.g. City, Town, Village,
  Hamlet, Other Settlement, Suburban Area

- `outcode` The postcode district, for example, SO15.

- `county_unitary` Administrative Area. The name of the County
  (non-metropolitan or Metropolitan), Unitary Authority or Greater
  London Authority administrative area that the point geometry for
  feature is within or nearest to.

- `county_unitary_type` Administrative Area Type. Classifies the type of
  administrative unit.

- `district_borough` District or Borough. The name of the District,
  Metropolitan District or London Borough administrative unit that the
  point geometry for the feature is within.

- `district_borough_type` Borough Type. Classifies the type of
  administrative unit.

- `region` The name of the European Region (was Government O ice Region)
  that the point geometry for the feature is within or nearest to.

- `country` The country (i.e. one of the four constituent countries of
  the United Kingdom or the Channel Islands or the Isle of Man) to which
  each place is assigned.

- `longitude` The WGS84 longitude given the Place's national grid
  reference.

- `latitude` The WGS84 latitude given the Place's national grid
  reference.

- `eastings` The Ordnance Survey postcode grid reference Easting to 1
  metre resolution; blank for postcodes in the Channel Islands and the
  Isle of Man.

- `northings` The Ordnance Survey postcode grid reference Northing to 1
  metre resolution; blank for postcodes in the Channel Islands and the
  Isle of Man.

- `min/max northings/eastings` Minimum and Maximum, Northings and
  Eastings. Bounding box or Minimum Bounding Rectangle (MBR) for roads
  and settlements. For Settlements and Sections of Named and Numbered
  Roads, the MBR gives a representation of the extent of these features
  and is not snapped to the real world extent.

See <https://postcodes.io/docs> for more details.

## Examples

``` r
# \donttest{
place_lookup("osgb4000000074544700")
#> $code
#> [1] "osgb4000000074544700"
#> 
#> $name_1
#> [1] "Cutler Heights"
#> 
#> $name_1_lang
#> NULL
#> 
#> $name_2
#> NULL
#> 
#> $name_2_lang
#> NULL
#> 
#> $local_type
#> [1] "Suburban Area"
#> 
#> $outcode
#> [1] "BD4"
#> 
#> $county_unitary
#> NULL
#> 
#> $county_unitary_type
#> NULL
#> 
#> $district_borough
#> [1] "Bradford"
#> 
#> $district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> $region
#> [1] "Yorkshire and the Humber"
#> 
#> $country
#> [1] "England"
#> 
#> $longitude
#> [1] -1.715716
#> 
#> $latitude
#> [1] 53.78206
#> 
#> $eastings
#> [1] 418830
#> 
#> $northings
#> [1] 431785
#> 
#> $min_eastings
#> [1] 418449
#> 
#> $min_northings
#> [1] 431455
#> 
#> $max_eastings
#> [1] 419076
#> 
#> $max_northings
#> [1] 432106
#> 
# }
```
