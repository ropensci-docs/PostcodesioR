# Place query

Submit a place query and receive a complete list of places matches and
associated data. This function is similar to
[`place_lookup`](https://docs.ropensci.org/PostcodesioR/reference/place_lookup.md)
but it returns a list and allows limiting the results.

## Usage

``` r
place_query(place, limit = 10)
```

## Arguments

- place:

  A string. Name of a place to search for.

- limit:

  An integer. Limits the number of matches to return. Defaults to 10.
  Needs to be less than 100.

## Value

A list with available places.

## See also

[`place_lookup`](https://docs.ropensci.org/PostcodesioR/reference/place_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
place_query("Hills")
#> [[1]]
#> [[1]]$code
#> [1] "osgb4000000074555222"
#> 
#> [[1]]$name_1
#> [1] "Tan Hills"
#> 
#> [[1]]$name_1_lang
#> NULL
#> 
#> [[1]]$name_2
#> NULL
#> 
#> [[1]]$name_2_lang
#> NULL
#> 
#> [[1]]$local_type
#> [1] "Village"
#> 
#> [[1]]$outcode
#> [1] "DH2"
#> 
#> [[1]]$county_unitary
#> [1] "County Durham"
#> 
#> [[1]]$county_unitary_type
#> [1] "UnitaryAuthority"
#> 
#> [[1]]$district_borough
#> NULL
#> 
#> [[1]]$district_borough_type
#> NULL
#> 
#> [[1]]$region
#> [1] "North East"
#> 
#> [[1]]$country
#> [1] "England"
#> 
#> [[1]]$longitude
#> [1] -1.597868
#> 
#> [[1]]$latitude
#> [1] 54.82239
#> 
#> [[1]]$eastings
#> [1] 425936
#> 
#> [[1]]$northings
#> [1] 547579
#> 
#> [[1]]$min_eastings
#> [1] 425721
#> 
#> [[1]]$min_northings
#> [1] 547375
#> 
#> [[1]]$max_eastings
#> [1] 426221
#> 
#> [[1]]$max_northings
#> [1] 547875
#> 
#> 
#> [[2]]
#> [[2]]$code
#> [1] "osgb4000000074574731"
#> 
#> [[2]]$name_1
#> [1] "Berwick Hills"
#> 
#> [[2]]$name_1_lang
#> NULL
#> 
#> [[2]]$name_2
#> NULL
#> 
#> [[2]]$name_2_lang
#> NULL
#> 
#> [[2]]$local_type
#> [1] "Suburban Area"
#> 
#> [[2]]$outcode
#> [1] "TS3"
#> 
#> [[2]]$county_unitary
#> [1] "Middlesbrough"
#> 
#> [[2]]$county_unitary_type
#> [1] "UnitaryAuthority"
#> 
#> [[2]]$district_borough
#> NULL
#> 
#> [[2]]$district_borough_type
#> NULL
#> 
#> [[2]]$region
#> [1] "North East"
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$longitude
#> [1] -1.20577
#> 
#> [[2]]$latitude
#> [1] 54.56005
#> 
#> [[2]]$eastings
#> [1] 451459
#> 
#> [[2]]$northings
#> [1] 518602
#> 
#> [[2]]$min_eastings
#> [1] 450839
#> 
#> [[2]]$min_northings
#> [1] 517640
#> 
#> [[2]]$max_eastings
#> [1] 451963
#> 
#> [[2]]$max_northings
#> [1] 519361
#> 
#> 
#> [[3]]
#> [[3]]$code
#> [1] "osgb4000000074568110"
#> 
#> [[3]]$name_1
#> [1] "Nun Hills"
#> 
#> [[3]]$name_1_lang
#> NULL
#> 
#> [[3]]$name_2
#> NULL
#> 
#> [[3]]$name_2_lang
#> NULL
#> 
#> [[3]]$local_type
#> [1] "Suburban Area"
#> 
#> [[3]]$outcode
#> [1] "OL13"
#> 
#> [[3]]$county_unitary
#> [1] "Lancashire"
#> 
#> [[3]]$county_unitary_type
#> [1] "County"
#> 
#> [[3]]$district_borough
#> [1] "Rossendale"
#> 
#> [[3]]$district_borough_type
#> [1] "District"
#> 
#> [[3]]$region
#> [1] "North West"
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$longitude
#> [1] -2.224568
#> 
#> [[3]]$latitude
#> [1] 53.69104
#> 
#> [[3]]$eastings
#> [1] 385268
#> 
#> [[3]]$northings
#> [1] 421645
#> 
#> [[3]]$min_eastings
#> [1] 384958
#> 
#> [[3]]$min_northings
#> [1] 421437
#> 
#> [[3]]$max_eastings
#> [1] 385465
#> 
#> [[3]]$max_northings
#> [1] 421937
#> 
#> 
#> [[4]]
#> [[4]]$code
#> [1] "osgb4000000074571332"
#> 
#> [[4]]$name_1
#> [1] "Bailey Hills"
#> 
#> [[4]]$name_1_lang
#> NULL
#> 
#> [[4]]$name_2
#> NULL
#> 
#> [[4]]$name_2_lang
#> NULL
#> 
#> [[4]]$local_type
#> [1] "Suburban Area"
#> 
#> [[4]]$outcode
#> [1] "BD16"
#> 
#> [[4]]$county_unitary
#> NULL
#> 
#> [[4]]$county_unitary_type
#> NULL
#> 
#> [[4]]$district_borough
#> [1] "Bradford"
#> 
#> [[4]]$district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> [[4]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[4]]$country
#> [1] "England"
#> 
#> [[4]]$longitude
#> [1] -1.841124
#> 
#> [[4]]$latitude
#> [1] 53.85212
#> 
#> [[4]]$eastings
#> [1] 410549
#> 
#> [[4]]$northings
#> [1] 439555
#> 
#> [[4]]$min_eastings
#> [1] 410241
#> 
#> [[4]]$min_northings
#> [1] 439253
#> 
#> [[4]]$max_eastings
#> [1] 410741
#> 
#> [[4]]$max_northings
#> [1] 439863
#> 
#> 
#> [[5]]
#> [[5]]$code
#> [1] "osgb4000000074572024"
#> 
#> [[5]]$name_1
#> [1] "Lister Hills"
#> 
#> [[5]]$name_1_lang
#> NULL
#> 
#> [[5]]$name_2
#> NULL
#> 
#> [[5]]$name_2_lang
#> NULL
#> 
#> [[5]]$local_type
#> [1] "Suburban Area"
#> 
#> [[5]]$outcode
#> [1] "BD7"
#> 
#> [[5]]$county_unitary
#> NULL
#> 
#> [[5]]$county_unitary_type
#> NULL
#> 
#> [[5]]$district_borough
#> [1] "Bradford"
#> 
#> [[5]]$district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> [[5]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[5]]$country
#> [1] "England"
#> 
#> [[5]]$longitude
#> [1] -1.770226
#> 
#> [[5]]$latitude
#> [1] 53.79351
#> 
#> [[5]]$eastings
#> [1] 415234
#> 
#> [[5]]$northings
#> [1] 433046
#> 
#> [[5]]$min_eastings
#> [1] 414935
#> 
#> [[5]]$min_northings
#> [1] 432878
#> 
#> [[5]]$max_eastings
#> [1] 415497
#> 
#> [[5]]$max_northings
#> [1] 433534
#> 
#> 
#> [[6]]
#> [[6]]$code
#> [1] "osgb4000000074569230"
#> 
#> [[6]]$name_1
#> [1] "Cross Hills"
#> 
#> [[6]]$name_1_lang
#> NULL
#> 
#> [[6]]$name_2
#> NULL
#> 
#> [[6]]$name_2_lang
#> NULL
#> 
#> [[6]]$local_type
#> [1] "Village"
#> 
#> [[6]]$outcode
#> [1] "BD20"
#> 
#> [[6]]$county_unitary
#> [1] "North Yorkshire"
#> 
#> [[6]]$county_unitary_type
#> [1] "UnitaryAuthority"
#> 
#> [[6]]$district_borough
#> NULL
#> 
#> [[6]]$district_borough_type
#> NULL
#> 
#> [[6]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[6]]$country
#> [1] "England"
#> 
#> [[6]]$longitude
#> [1] -1.989919
#> 
#> [[6]]$latitude
#> [1] 53.90184
#> 
#> [[6]]$eastings
#> [1] 400760
#> 
#> [[6]]$northings
#> [1] 445075
#> 
#> [[6]]$min_eastings
#> [1] 398551
#> 
#> [[6]]$min_northings
#> [1] 444126
#> 
#> [[6]]$max_eastings
#> [1] 401868
#> 
#> [[6]]$max_northings
#> [1] 445644
#> 
#> 
#> [[7]]
#> [[7]]$code
#> [1] "osgb4000000074570252"
#> 
#> [[7]]$name_1
#> [1] "Old Hills"
#> 
#> [[7]]$name_1_lang
#> NULL
#> 
#> [[7]]$name_2
#> NULL
#> 
#> [[7]]$name_2_lang
#> NULL
#> 
#> [[7]]$local_type
#> [1] "Suburban Area"
#> 
#> [[7]]$outcode
#> [1] "BD16"
#> 
#> [[7]]$county_unitary
#> NULL
#> 
#> [[7]]$county_unitary_type
#> NULL
#> 
#> [[7]]$district_borough
#> [1] "Bradford"
#> 
#> [[7]]$district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> [[7]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[7]]$country
#> [1] "England"
#> 
#> [[7]]$longitude
#> [1] -1.830166
#> 
#> [[7]]$latitude
#> [1] 53.84416
#> 
#> [[7]]$eastings
#> [1] 411272
#> 
#> [[7]]$northings
#> [1] 438671
#> 
#> [[7]]$min_eastings
#> [1] 411081
#> 
#> [[7]]$min_northings
#> [1] 438457
#> 
#> [[7]]$max_eastings
#> [1] 411581
#> 
#> [[7]]$max_northings
#> [1] 438957
#> 
#> 
#> [[8]]
#> [[8]]$code
#> [1] "osgb4000000074544460"
#> 
#> [[8]]$name_1
#> [1] "Wheatley Hills"
#> 
#> [[8]]$name_1_lang
#> NULL
#> 
#> [[8]]$name_2
#> NULL
#> 
#> [[8]]$name_2_lang
#> NULL
#> 
#> [[8]]$local_type
#> [1] "Suburban Area"
#> 
#> [[8]]$outcode
#> [1] "DN2"
#> 
#> [[8]]$county_unitary
#> NULL
#> 
#> [[8]]$county_unitary_type
#> NULL
#> 
#> [[8]]$district_borough
#> [1] "Doncaster"
#> 
#> [[8]]$district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> [[8]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[8]]$country
#> [1] "England"
#> 
#> [[8]]$longitude
#> [1] -1.100679
#> 
#> [[8]]$latitude
#> [1] 53.53897
#> 
#> [[8]]$eastings
#> [1] 459698
#> 
#> [[8]]$northings
#> [1] 405078
#> 
#> [[8]]$min_eastings
#> [1] 458941
#> 
#> [[8]]$min_northings
#> [1] 404220
#> 
#> [[8]]$max_eastings
#> [1] 460614
#> 
#> [[8]]$max_northings
#> [1] 405620
#> 
#> 
#> [[9]]
#> [[9]]$code
#> [1] "osgb4000000074561319"
#> 
#> [[9]]$name_1
#> [1] "Stanford Hills"
#> 
#> [[9]]$name_1_lang
#> NULL
#> 
#> [[9]]$name_2
#> NULL
#> 
#> [[9]]$name_2_lang
#> NULL
#> 
#> [[9]]$local_type
#> [1] "Hamlet"
#> 
#> [[9]]$outcode
#> [1] "LE12"
#> 
#> [[9]]$county_unitary
#> [1] "Nottinghamshire"
#> 
#> [[9]]$county_unitary_type
#> [1] "County"
#> 
#> [[9]]$district_borough
#> [1] "Rushcliffe"
#> 
#> [[9]]$district_borough_type
#> [1] "District"
#> 
#> [[9]]$region
#> [1] "East Midlands"
#> 
#> [[9]]$country
#> [1] "England"
#> 
#> [[9]]$longitude
#> [1] -1.186273
#> 
#> [[9]]$latitude
#> [1] 52.80939
#> 
#> [[9]]$eastings
#> [1] 454948
#> 
#> [[9]]$northings
#> [1] 323848
#> 
#> [[9]]$min_eastings
#> [1] 454696
#> 
#> [[9]]$min_northings
#> [1] 323502
#> 
#> [[9]]$max_eastings
#> [1] 455196
#> 
#> [[9]]$max_northings
#> [1] 324002
#> 
#> 
#> [[10]]
#> [[10]]$code
#> [1] "osgb4000000074547803"
#> 
#> [[10]]$name_1
#> [1] "Red Hills"
#> 
#> [[10]]$name_1_lang
#> NULL
#> 
#> [[10]]$name_2
#> NULL
#> 
#> [[10]]$name_2_lang
#> NULL
#> 
#> [[10]]$local_type
#> [1] "Hamlet"
#> 
#> [[10]]$outcode
#> [1] "CA11"
#> 
#> [[10]]$county_unitary
#> [1] "Westmorland and Furness"
#> 
#> [[10]]$county_unitary_type
#> [1] "UnitaryAuthority"
#> 
#> [[10]]$district_borough
#> NULL
#> 
#> [[10]]$district_borough_type
#> NULL
#> 
#> [[10]]$region
#> [1] "North West"
#> 
#> [[10]]$country
#> [1] "England"
#> 
#> [[10]]$longitude
#> [1] -2.769232
#> 
#> [[10]]$latitude
#> [1] 54.6501
#> 
#> [[10]]$eastings
#> [1] 350463
#> 
#> [[10]]$northings
#> [1] 528605
#> 
#> [[10]]$min_eastings
#> [1] 349916
#> 
#> [[10]]$min_northings
#> [1] 528349
#> 
#> [[10]]$max_eastings
#> [1] 350584
#> 
#> [[10]]$max_northings
#> [1] 528849
#> 
#> 
place_query("Hills", limit = 12)
#> [[1]]
#> [[1]]$code
#> [1] "osgb4000000074555222"
#> 
#> [[1]]$name_1
#> [1] "Tan Hills"
#> 
#> [[1]]$name_1_lang
#> NULL
#> 
#> [[1]]$name_2
#> NULL
#> 
#> [[1]]$name_2_lang
#> NULL
#> 
#> [[1]]$local_type
#> [1] "Village"
#> 
#> [[1]]$outcode
#> [1] "DH2"
#> 
#> [[1]]$county_unitary
#> [1] "County Durham"
#> 
#> [[1]]$county_unitary_type
#> [1] "UnitaryAuthority"
#> 
#> [[1]]$district_borough
#> NULL
#> 
#> [[1]]$district_borough_type
#> NULL
#> 
#> [[1]]$region
#> [1] "North East"
#> 
#> [[1]]$country
#> [1] "England"
#> 
#> [[1]]$longitude
#> [1] -1.597868
#> 
#> [[1]]$latitude
#> [1] 54.82239
#> 
#> [[1]]$eastings
#> [1] 425936
#> 
#> [[1]]$northings
#> [1] 547579
#> 
#> [[1]]$min_eastings
#> [1] 425721
#> 
#> [[1]]$min_northings
#> [1] 547375
#> 
#> [[1]]$max_eastings
#> [1] 426221
#> 
#> [[1]]$max_northings
#> [1] 547875
#> 
#> 
#> [[2]]
#> [[2]]$code
#> [1] "osgb4000000074574731"
#> 
#> [[2]]$name_1
#> [1] "Berwick Hills"
#> 
#> [[2]]$name_1_lang
#> NULL
#> 
#> [[2]]$name_2
#> NULL
#> 
#> [[2]]$name_2_lang
#> NULL
#> 
#> [[2]]$local_type
#> [1] "Suburban Area"
#> 
#> [[2]]$outcode
#> [1] "TS3"
#> 
#> [[2]]$county_unitary
#> [1] "Middlesbrough"
#> 
#> [[2]]$county_unitary_type
#> [1] "UnitaryAuthority"
#> 
#> [[2]]$district_borough
#> NULL
#> 
#> [[2]]$district_borough_type
#> NULL
#> 
#> [[2]]$region
#> [1] "North East"
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$longitude
#> [1] -1.20577
#> 
#> [[2]]$latitude
#> [1] 54.56005
#> 
#> [[2]]$eastings
#> [1] 451459
#> 
#> [[2]]$northings
#> [1] 518602
#> 
#> [[2]]$min_eastings
#> [1] 450839
#> 
#> [[2]]$min_northings
#> [1] 517640
#> 
#> [[2]]$max_eastings
#> [1] 451963
#> 
#> [[2]]$max_northings
#> [1] 519361
#> 
#> 
#> [[3]]
#> [[3]]$code
#> [1] "osgb4000000074568110"
#> 
#> [[3]]$name_1
#> [1] "Nun Hills"
#> 
#> [[3]]$name_1_lang
#> NULL
#> 
#> [[3]]$name_2
#> NULL
#> 
#> [[3]]$name_2_lang
#> NULL
#> 
#> [[3]]$local_type
#> [1] "Suburban Area"
#> 
#> [[3]]$outcode
#> [1] "OL13"
#> 
#> [[3]]$county_unitary
#> [1] "Lancashire"
#> 
#> [[3]]$county_unitary_type
#> [1] "County"
#> 
#> [[3]]$district_borough
#> [1] "Rossendale"
#> 
#> [[3]]$district_borough_type
#> [1] "District"
#> 
#> [[3]]$region
#> [1] "North West"
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$longitude
#> [1] -2.224568
#> 
#> [[3]]$latitude
#> [1] 53.69104
#> 
#> [[3]]$eastings
#> [1] 385268
#> 
#> [[3]]$northings
#> [1] 421645
#> 
#> [[3]]$min_eastings
#> [1] 384958
#> 
#> [[3]]$min_northings
#> [1] 421437
#> 
#> [[3]]$max_eastings
#> [1] 385465
#> 
#> [[3]]$max_northings
#> [1] 421937
#> 
#> 
#> [[4]]
#> [[4]]$code
#> [1] "osgb4000000074571332"
#> 
#> [[4]]$name_1
#> [1] "Bailey Hills"
#> 
#> [[4]]$name_1_lang
#> NULL
#> 
#> [[4]]$name_2
#> NULL
#> 
#> [[4]]$name_2_lang
#> NULL
#> 
#> [[4]]$local_type
#> [1] "Suburban Area"
#> 
#> [[4]]$outcode
#> [1] "BD16"
#> 
#> [[4]]$county_unitary
#> NULL
#> 
#> [[4]]$county_unitary_type
#> NULL
#> 
#> [[4]]$district_borough
#> [1] "Bradford"
#> 
#> [[4]]$district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> [[4]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[4]]$country
#> [1] "England"
#> 
#> [[4]]$longitude
#> [1] -1.841124
#> 
#> [[4]]$latitude
#> [1] 53.85212
#> 
#> [[4]]$eastings
#> [1] 410549
#> 
#> [[4]]$northings
#> [1] 439555
#> 
#> [[4]]$min_eastings
#> [1] 410241
#> 
#> [[4]]$min_northings
#> [1] 439253
#> 
#> [[4]]$max_eastings
#> [1] 410741
#> 
#> [[4]]$max_northings
#> [1] 439863
#> 
#> 
#> [[5]]
#> [[5]]$code
#> [1] "osgb4000000074572024"
#> 
#> [[5]]$name_1
#> [1] "Lister Hills"
#> 
#> [[5]]$name_1_lang
#> NULL
#> 
#> [[5]]$name_2
#> NULL
#> 
#> [[5]]$name_2_lang
#> NULL
#> 
#> [[5]]$local_type
#> [1] "Suburban Area"
#> 
#> [[5]]$outcode
#> [1] "BD7"
#> 
#> [[5]]$county_unitary
#> NULL
#> 
#> [[5]]$county_unitary_type
#> NULL
#> 
#> [[5]]$district_borough
#> [1] "Bradford"
#> 
#> [[5]]$district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> [[5]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[5]]$country
#> [1] "England"
#> 
#> [[5]]$longitude
#> [1] -1.770226
#> 
#> [[5]]$latitude
#> [1] 53.79351
#> 
#> [[5]]$eastings
#> [1] 415234
#> 
#> [[5]]$northings
#> [1] 433046
#> 
#> [[5]]$min_eastings
#> [1] 414935
#> 
#> [[5]]$min_northings
#> [1] 432878
#> 
#> [[5]]$max_eastings
#> [1] 415497
#> 
#> [[5]]$max_northings
#> [1] 433534
#> 
#> 
#> [[6]]
#> [[6]]$code
#> [1] "osgb4000000074569230"
#> 
#> [[6]]$name_1
#> [1] "Cross Hills"
#> 
#> [[6]]$name_1_lang
#> NULL
#> 
#> [[6]]$name_2
#> NULL
#> 
#> [[6]]$name_2_lang
#> NULL
#> 
#> [[6]]$local_type
#> [1] "Village"
#> 
#> [[6]]$outcode
#> [1] "BD20"
#> 
#> [[6]]$county_unitary
#> [1] "North Yorkshire"
#> 
#> [[6]]$county_unitary_type
#> [1] "UnitaryAuthority"
#> 
#> [[6]]$district_borough
#> NULL
#> 
#> [[6]]$district_borough_type
#> NULL
#> 
#> [[6]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[6]]$country
#> [1] "England"
#> 
#> [[6]]$longitude
#> [1] -1.989919
#> 
#> [[6]]$latitude
#> [1] 53.90184
#> 
#> [[6]]$eastings
#> [1] 400760
#> 
#> [[6]]$northings
#> [1] 445075
#> 
#> [[6]]$min_eastings
#> [1] 398551
#> 
#> [[6]]$min_northings
#> [1] 444126
#> 
#> [[6]]$max_eastings
#> [1] 401868
#> 
#> [[6]]$max_northings
#> [1] 445644
#> 
#> 
#> [[7]]
#> [[7]]$code
#> [1] "osgb4000000074570252"
#> 
#> [[7]]$name_1
#> [1] "Old Hills"
#> 
#> [[7]]$name_1_lang
#> NULL
#> 
#> [[7]]$name_2
#> NULL
#> 
#> [[7]]$name_2_lang
#> NULL
#> 
#> [[7]]$local_type
#> [1] "Suburban Area"
#> 
#> [[7]]$outcode
#> [1] "BD16"
#> 
#> [[7]]$county_unitary
#> NULL
#> 
#> [[7]]$county_unitary_type
#> NULL
#> 
#> [[7]]$district_borough
#> [1] "Bradford"
#> 
#> [[7]]$district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> [[7]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[7]]$country
#> [1] "England"
#> 
#> [[7]]$longitude
#> [1] -1.830166
#> 
#> [[7]]$latitude
#> [1] 53.84416
#> 
#> [[7]]$eastings
#> [1] 411272
#> 
#> [[7]]$northings
#> [1] 438671
#> 
#> [[7]]$min_eastings
#> [1] 411081
#> 
#> [[7]]$min_northings
#> [1] 438457
#> 
#> [[7]]$max_eastings
#> [1] 411581
#> 
#> [[7]]$max_northings
#> [1] 438957
#> 
#> 
#> [[8]]
#> [[8]]$code
#> [1] "osgb4000000074544460"
#> 
#> [[8]]$name_1
#> [1] "Wheatley Hills"
#> 
#> [[8]]$name_1_lang
#> NULL
#> 
#> [[8]]$name_2
#> NULL
#> 
#> [[8]]$name_2_lang
#> NULL
#> 
#> [[8]]$local_type
#> [1] "Suburban Area"
#> 
#> [[8]]$outcode
#> [1] "DN2"
#> 
#> [[8]]$county_unitary
#> NULL
#> 
#> [[8]]$county_unitary_type
#> NULL
#> 
#> [[8]]$district_borough
#> [1] "Doncaster"
#> 
#> [[8]]$district_borough_type
#> [1] "MetropolitanDistrict"
#> 
#> [[8]]$region
#> [1] "Yorkshire and the Humber"
#> 
#> [[8]]$country
#> [1] "England"
#> 
#> [[8]]$longitude
#> [1] -1.100679
#> 
#> [[8]]$latitude
#> [1] 53.53897
#> 
#> [[8]]$eastings
#> [1] 459698
#> 
#> [[8]]$northings
#> [1] 405078
#> 
#> [[8]]$min_eastings
#> [1] 458941
#> 
#> [[8]]$min_northings
#> [1] 404220
#> 
#> [[8]]$max_eastings
#> [1] 460614
#> 
#> [[8]]$max_northings
#> [1] 405620
#> 
#> 
#> [[9]]
#> [[9]]$code
#> [1] "osgb4000000074561319"
#> 
#> [[9]]$name_1
#> [1] "Stanford Hills"
#> 
#> [[9]]$name_1_lang
#> NULL
#> 
#> [[9]]$name_2
#> NULL
#> 
#> [[9]]$name_2_lang
#> NULL
#> 
#> [[9]]$local_type
#> [1] "Hamlet"
#> 
#> [[9]]$outcode
#> [1] "LE12"
#> 
#> [[9]]$county_unitary
#> [1] "Nottinghamshire"
#> 
#> [[9]]$county_unitary_type
#> [1] "County"
#> 
#> [[9]]$district_borough
#> [1] "Rushcliffe"
#> 
#> [[9]]$district_borough_type
#> [1] "District"
#> 
#> [[9]]$region
#> [1] "East Midlands"
#> 
#> [[9]]$country
#> [1] "England"
#> 
#> [[9]]$longitude
#> [1] -1.186273
#> 
#> [[9]]$latitude
#> [1] 52.80939
#> 
#> [[9]]$eastings
#> [1] 454948
#> 
#> [[9]]$northings
#> [1] 323848
#> 
#> [[9]]$min_eastings
#> [1] 454696
#> 
#> [[9]]$min_northings
#> [1] 323502
#> 
#> [[9]]$max_eastings
#> [1] 455196
#> 
#> [[9]]$max_northings
#> [1] 324002
#> 
#> 
#> [[10]]
#> [[10]]$code
#> [1] "osgb4000000074575417"
#> 
#> [[10]]$name_1
#> [1] "Bleak Hills"
#> 
#> [[10]]$name_1_lang
#> NULL
#> 
#> [[10]]$name_2
#> NULL
#> 
#> [[10]]$name_2_lang
#> NULL
#> 
#> [[10]]$local_type
#> [1] "Suburban Area"
#> 
#> [[10]]$outcode
#> [1] "NG18"
#> 
#> [[10]]$county_unitary
#> [1] "Nottinghamshire"
#> 
#> [[10]]$county_unitary_type
#> [1] "County"
#> 
#> [[10]]$district_borough
#> [1] "Mansfield"
#> 
#> [[10]]$district_borough_type
#> [1] "District"
#> 
#> [[10]]$region
#> [1] "East Midlands"
#> 
#> [[10]]$country
#> [1] "England"
#> 
#> [[10]]$longitude
#> [1] -1.216838
#> 
#> [[10]]$latitude
#> [1] 53.13223
#> 
#> [[10]]$eastings
#> [1] 452496
#> 
#> [[10]]$northings
#> [1] 359738
#> 
#> [[10]]$min_eastings
#> [1] 451939
#> 
#> [[10]]$min_northings
#> [1] 359026
#> 
#> [[10]]$max_eastings
#> [1] 453287
#> 
#> [[10]]$max_northings
#> [1] 360090
#> 
#> 
#> [[11]]
#> [[11]]$code
#> [1] "osgb4000000074561106"
#> 
#> [[11]]$name_1
#> [1] "Hoton Hills"
#> 
#> [[11]]$name_1_lang
#> NULL
#> 
#> [[11]]$name_2
#> NULL
#> 
#> [[11]]$name_2_lang
#> NULL
#> 
#> [[11]]$local_type
#> [1] "Hamlet"
#> 
#> [[11]]$outcode
#> [1] "LE12"
#> 
#> [[11]]$county_unitary
#> [1] "Leicestershire"
#> 
#> [[11]]$county_unitary_type
#> [1] "County"
#> 
#> [[11]]$district_borough
#> [1] "Charnwood"
#> 
#> [[11]]$district_borough_type
#> [1] "District"
#> 
#> [[11]]$region
#> [1] "East Midlands"
#> 
#> [[11]]$country
#> [1] "England"
#> 
#> [[11]]$longitude
#> [1] -1.171086
#> 
#> [[11]]$latitude
#> [1] 52.79511
#> 
#> [[11]]$eastings
#> [1] 455990
#> 
#> [[11]]$northings
#> [1] 322271
#> 
#> [[11]]$min_eastings
#> [1] 455722
#> 
#> [[11]]$min_northings
#> [1] 322037
#> 
#> [[11]]$max_eastings
#> [1] 456222
#> 
#> [[11]]$max_northings
#> [1] 322537
#> 
#> 
#> [[12]]
#> [[12]]$code
#> [1] "osgb4000000074547803"
#> 
#> [[12]]$name_1
#> [1] "Red Hills"
#> 
#> [[12]]$name_1_lang
#> NULL
#> 
#> [[12]]$name_2
#> NULL
#> 
#> [[12]]$name_2_lang
#> NULL
#> 
#> [[12]]$local_type
#> [1] "Hamlet"
#> 
#> [[12]]$outcode
#> [1] "CA11"
#> 
#> [[12]]$county_unitary
#> [1] "Westmorland and Furness"
#> 
#> [[12]]$county_unitary_type
#> [1] "UnitaryAuthority"
#> 
#> [[12]]$district_borough
#> NULL
#> 
#> [[12]]$district_borough_type
#> NULL
#> 
#> [[12]]$region
#> [1] "North West"
#> 
#> [[12]]$country
#> [1] "England"
#> 
#> [[12]]$longitude
#> [1] -2.769232
#> 
#> [[12]]$latitude
#> [1] 54.6501
#> 
#> [[12]]$eastings
#> [1] 350463
#> 
#> [[12]]$northings
#> [1] 528605
#> 
#> [[12]]$min_eastings
#> [1] 349916
#> 
#> [[12]]$min_northings
#> [1] 528349
#> 
#> [[12]]$max_eastings
#> [1] 350584
#> 
#> [[12]]$max_northings
#> [1] 528849
#> 
#> 
# }
```
