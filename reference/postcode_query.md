# Postcode query

Submit a postcode query and receive a complete list of postcode matches
and all associated postcode data.

## Usage

``` r
postcode_query(postcode, limit = 10)
```

## Arguments

- postcode:

  A string. Valid UK postcode.

- limit:

  An integer. Limits the number of matches to return. Defaults to 10.
  Needs to be less than 100.

## Value

A list of geographic properties. To return a data frame use
[postcode_lookup](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md).

## Examples

``` r
# \donttest{
postcode_query("EC1Y8LX")
#> [[1]]
#> [[1]]$postcode
#> [1] "EC1Y 8LX"
#> 
#> [[1]]$quality
#> [1] 1
#> 
#> [[1]]$eastings
#> [1] 532544
#> 
#> [[1]]$northings
#> [1] 182128
#> 
#> [[1]]$country
#> [1] "England"
#> 
#> [[1]]$nhs_ha
#> [1] "London"
#> 
#> [[1]]$longitude
#> [1] -0.090896
#> 
#> [[1]]$latitude
#> [1] 51.52253
#> 
#> [[1]]$european_electoral_region
#> [1] "London"
#> 
#> [[1]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[1]]$region
#> [1] "London"
#> 
#> [[1]]$lsoa
#> [1] "Islington 023D"
#> 
#> [[1]]$msoa
#> [1] "Islington 023"
#> 
#> [[1]]$incode
#> [1] "8LX"
#> 
#> [[1]]$outcode
#> [1] "EC1Y"
#> 
#> [[1]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[1]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[1]]$senedd_constituency
#> NULL
#> 
#> [[1]]$senedd_constituency_no
#> NULL
#> 
#> [[1]]$admin_district
#> [1] "Islington"
#> 
#> [[1]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[1]]$admin_county
#> NULL
#> 
#> [[1]]$date_of_introduction
#> [1] "198001"
#> 
#> [[1]]$date_of_termination
#> NULL
#> 
#> [[1]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[1]]$admin_ward
#> [1] "Bunhill"
#> 
#> [[1]]$ced
#> NULL
#> 
#> [[1]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[1]]$nuts
#> [1] "Islington"
#> 
#> [[1]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[1]]$nhs_region
#> [1] "London"
#> 
#> [[1]]$ttwa
#> [1] "London"
#> 
#> [[1]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[1]]$bua
#> [1] "Islington"
#> 
#> [[1]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[1]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[1]]$lsoa11
#> [1] "Islington 023D"
#> 
#> [[1]]$msoa11
#> [1] "Islington 023"
#> 
#> [[1]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[1]]$msoa21
#> [1] "Islington 023"
#> 
#> [[1]]$oa21
#> [1] "E00013429"
#> 
#> [[1]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[1]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$lep1
#> [1] "London"
#> 
#> [[1]]$lep2
#> NULL
#> 
#> [[1]]$codes
#> [[1]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[1]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[1]]$codes$admin_ward
#> [1] "E05013699"
#> 
#> [[1]]$codes$parish
#> [1] "E43000209"
#> 
#> [[1]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[1]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[1]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[1]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[1]]$codes$ced
#> [1] "E99999999"
#> 
#> [[1]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[1]]$codes$lsoa
#> [1] "E01002704"
#> 
#> [[1]]$codes$msoa
#> [1] "E02000576"
#> 
#> [[1]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[1]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[1]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[1]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[1]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[1]]$codes$bua
#> [1] "E63011980"
#> 
#> [[1]]$codes$icb
#> [1] "E54000071"
#> 
#> [[1]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[1]]$codes$lsoa11
#> [1] "E01002704"
#> 
#> [[1]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[1]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[1]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[1]]$codes$oa21
#> [1] "E00013429"
#> 
#> [[1]]$codes$ruc11
#> [1] "A1"
#> 
#> [[1]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[1]]$codes$lep2
#> NULL
#> 
#> 
#> 
postcode_query("EC1", limit = 11)
#> [[1]]
#> [[1]]$postcode
#> [1] "EC1A 1AA"
#> 
#> [[1]]$quality
#> [1] 1
#> 
#> [[1]]$eastings
#> [1] 531131
#> 
#> [[1]]$northings
#> [1] 182382
#> 
#> [[1]]$country
#> [1] "England"
#> 
#> [[1]]$nhs_ha
#> [1] "London"
#> 
#> [[1]]$longitude
#> [1] -0.111157
#> 
#> [[1]]$latitude
#> [1] 51.52514
#> 
#> [[1]]$european_electoral_region
#> [1] "London"
#> 
#> [[1]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[1]]$region
#> [1] "London"
#> 
#> [[1]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[1]]$msoa
#> [1] "Islington 022"
#> 
#> [[1]]$incode
#> [1] "1AA"
#> 
#> [[1]]$outcode
#> [1] "EC1A"
#> 
#> [[1]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[1]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[1]]$senedd_constituency
#> NULL
#> 
#> [[1]]$senedd_constituency_no
#> NULL
#> 
#> [[1]]$admin_district
#> [1] "Islington"
#> 
#> [[1]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[1]]$admin_county
#> NULL
#> 
#> [[1]]$date_of_introduction
#> [1] "201307"
#> 
#> [[1]]$date_of_termination
#> NULL
#> 
#> [[1]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[1]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[1]]$ced
#> NULL
#> 
#> [[1]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[1]]$nuts
#> [1] "Islington"
#> 
#> [[1]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[1]]$nhs_region
#> [1] "London"
#> 
#> [[1]]$ttwa
#> [1] "London"
#> 
#> [[1]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[1]]$bua
#> [1] "Islington"
#> 
#> [[1]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[1]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[1]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[1]]$msoa11
#> [1] "Islington 022"
#> 
#> [[1]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[1]]$msoa21
#> [1] "Islington 022"
#> 
#> [[1]]$oa21
#> [1] "E00013578"
#> 
#> [[1]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[1]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[1]]$lep1
#> [1] "London"
#> 
#> [[1]]$lep2
#> NULL
#> 
#> [[1]]$codes
#> [[1]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[1]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[1]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[1]]$codes$parish
#> [1] "E43000209"
#> 
#> [[1]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[1]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[1]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[1]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[1]]$codes$ced
#> [1] "E99999999"
#> 
#> [[1]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[1]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[1]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[1]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[1]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[1]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[1]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[1]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[1]]$codes$bua
#> [1] "E63011980"
#> 
#> [[1]]$codes$icb
#> [1] "E54000071"
#> 
#> [[1]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[1]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[1]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[1]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[1]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[1]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[1]]$codes$ruc11
#> [1] "A1"
#> 
#> [[1]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[1]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[1]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[2]]
#> [[2]]$postcode
#> [1] "EC1A 1AH"
#> 
#> [[2]]$quality
#> [1] 1
#> 
#> [[2]]$eastings
#> [1] 531073
#> 
#> [[2]]$northings
#> [1] 182317
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$nhs_ha
#> [1] "London"
#> 
#> [[2]]$longitude
#> [1] -0.112017
#> 
#> [[2]]$latitude
#> [1] 51.52457
#> 
#> [[2]]$european_electoral_region
#> [1] "London"
#> 
#> [[2]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[2]]$region
#> [1] "London"
#> 
#> [[2]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[2]]$msoa
#> [1] "Islington 022"
#> 
#> [[2]]$incode
#> [1] "1AH"
#> 
#> [[2]]$outcode
#> [1] "EC1A"
#> 
#> [[2]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[2]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[2]]$senedd_constituency
#> NULL
#> 
#> [[2]]$senedd_constituency_no
#> NULL
#> 
#> [[2]]$admin_district
#> [1] "Islington"
#> 
#> [[2]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[2]]$admin_county
#> NULL
#> 
#> [[2]]$date_of_introduction
#> [1] "199501"
#> 
#> [[2]]$date_of_termination
#> NULL
#> 
#> [[2]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[2]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[2]]$ced
#> NULL
#> 
#> [[2]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[2]]$nuts
#> [1] "Islington"
#> 
#> [[2]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[2]]$nhs_region
#> [1] "London"
#> 
#> [[2]]$ttwa
#> [1] "London"
#> 
#> [[2]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$bua
#> [1] "Islington"
#> 
#> [[2]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[2]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[2]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[2]]$msoa11
#> [1] "Islington 022"
#> 
#> [[2]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[2]]$msoa21
#> [1] "Islington 022"
#> 
#> [[2]]$oa21
#> [1] "E00013578"
#> 
#> [[2]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[2]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[2]]$lep1
#> [1] "London"
#> 
#> [[2]]$lep2
#> NULL
#> 
#> [[2]]$codes
#> [[2]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[2]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[2]]$codes$parish
#> [1] "E43000209"
#> 
#> [[2]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[2]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[2]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[2]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[2]]$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[2]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[2]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[2]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[2]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[2]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[2]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[2]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$codes$bua
#> [1] "E63011980"
#> 
#> [[2]]$codes$icb
#> [1] "E54000071"
#> 
#> [[2]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[2]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[2]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[2]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[2]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[2]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[2]]$codes$ruc11
#> [1] "A1"
#> 
#> [[2]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[2]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[2]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[3]]
#> [[3]]$postcode
#> [1] "EC1A 1AZ"
#> 
#> [[3]]$quality
#> [1] 1
#> 
#> [[3]]$eastings
#> [1] 531070
#> 
#> [[3]]$northings
#> [1] 182310
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$nhs_ha
#> [1] "London"
#> 
#> [[3]]$longitude
#> [1] -0.112063
#> 
#> [[3]]$latitude
#> [1] 51.5245
#> 
#> [[3]]$european_electoral_region
#> [1] "London"
#> 
#> [[3]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[3]]$region
#> [1] "London"
#> 
#> [[3]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[3]]$msoa
#> [1] "Islington 022"
#> 
#> [[3]]$incode
#> [1] "1AZ"
#> 
#> [[3]]$outcode
#> [1] "EC1A"
#> 
#> [[3]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[3]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[3]]$senedd_constituency
#> NULL
#> 
#> [[3]]$senedd_constituency_no
#> NULL
#> 
#> [[3]]$admin_district
#> [1] "Islington"
#> 
#> [[3]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[3]]$admin_county
#> NULL
#> 
#> [[3]]$date_of_introduction
#> [1] "200207"
#> 
#> [[3]]$date_of_termination
#> NULL
#> 
#> [[3]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[3]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[3]]$ced
#> NULL
#> 
#> [[3]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[3]]$nuts
#> [1] "Islington"
#> 
#> [[3]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[3]]$nhs_region
#> [1] "London"
#> 
#> [[3]]$ttwa
#> [1] "London"
#> 
#> [[3]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[3]]$bua
#> [1] "Islington"
#> 
#> [[3]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[3]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[3]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[3]]$msoa11
#> [1] "Islington 022"
#> 
#> [[3]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[3]]$msoa21
#> [1] "Islington 022"
#> 
#> [[3]]$oa21
#> [1] "E00013578"
#> 
#> [[3]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[3]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[3]]$lep1
#> [1] "London"
#> 
#> [[3]]$lep2
#> NULL
#> 
#> [[3]]$codes
#> [[3]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[3]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[3]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[3]]$codes$parish
#> [1] "E43000209"
#> 
#> [[3]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[3]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[3]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[3]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[3]]$codes$ced
#> [1] "E99999999"
#> 
#> [[3]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[3]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[3]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[3]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[3]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[3]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[3]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[3]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[3]]$codes$bua
#> [1] "E63011980"
#> 
#> [[3]]$codes$icb
#> [1] "E54000071"
#> 
#> [[3]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[3]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[3]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[3]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[3]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[3]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[3]]$codes$ruc11
#> [1] "A1"
#> 
#> [[3]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[3]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[3]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[4]]
#> [[4]]$postcode
#> [1] "EC1A 1BB"
#> 
#> [[4]]$quality
#> [1] 1
#> 
#> [[4]]$eastings
#> [1] 531073
#> 
#> [[4]]$northings
#> [1] 182317
#> 
#> [[4]]$country
#> [1] "England"
#> 
#> [[4]]$nhs_ha
#> [1] "London"
#> 
#> [[4]]$longitude
#> [1] -0.112017
#> 
#> [[4]]$latitude
#> [1] 51.52457
#> 
#> [[4]]$european_electoral_region
#> [1] "London"
#> 
#> [[4]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[4]]$region
#> [1] "London"
#> 
#> [[4]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[4]]$msoa
#> [1] "Islington 022"
#> 
#> [[4]]$incode
#> [1] "1BB"
#> 
#> [[4]]$outcode
#> [1] "EC1A"
#> 
#> [[4]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[4]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[4]]$senedd_constituency
#> NULL
#> 
#> [[4]]$senedd_constituency_no
#> NULL
#> 
#> [[4]]$admin_district
#> [1] "Islington"
#> 
#> [[4]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[4]]$admin_county
#> NULL
#> 
#> [[4]]$date_of_introduction
#> [1] "198410"
#> 
#> [[4]]$date_of_termination
#> NULL
#> 
#> [[4]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[4]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[4]]$ced
#> NULL
#> 
#> [[4]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[4]]$nuts
#> [1] "Islington"
#> 
#> [[4]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[4]]$nhs_region
#> [1] "London"
#> 
#> [[4]]$ttwa
#> [1] "London"
#> 
#> [[4]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[4]]$bua
#> [1] "Islington"
#> 
#> [[4]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[4]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[4]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[4]]$msoa11
#> [1] "Islington 022"
#> 
#> [[4]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[4]]$msoa21
#> [1] "Islington 022"
#> 
#> [[4]]$oa21
#> [1] "E00013578"
#> 
#> [[4]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[4]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[4]]$lep1
#> [1] "London"
#> 
#> [[4]]$lep2
#> NULL
#> 
#> [[4]]$codes
#> [[4]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[4]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[4]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[4]]$codes$parish
#> [1] "E43000209"
#> 
#> [[4]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[4]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[4]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[4]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[4]]$codes$ced
#> [1] "E99999999"
#> 
#> [[4]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[4]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[4]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[4]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[4]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[4]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[4]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[4]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[4]]$codes$bua
#> [1] "E63011980"
#> 
#> [[4]]$codes$icb
#> [1] "E54000071"
#> 
#> [[4]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[4]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[4]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[4]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[4]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[4]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[4]]$codes$ruc11
#> [1] "A1"
#> 
#> [[4]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[4]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[4]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[5]]
#> [[5]]$postcode
#> [1] "EC1A 1DN"
#> 
#> [[5]]$quality
#> [1] 1
#> 
#> [[5]]$eastings
#> [1] 531073
#> 
#> [[5]]$northings
#> [1] 182317
#> 
#> [[5]]$country
#> [1] "England"
#> 
#> [[5]]$nhs_ha
#> [1] "London"
#> 
#> [[5]]$longitude
#> [1] -0.112017
#> 
#> [[5]]$latitude
#> [1] 51.52457
#> 
#> [[5]]$european_electoral_region
#> [1] "London"
#> 
#> [[5]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[5]]$region
#> [1] "London"
#> 
#> [[5]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[5]]$msoa
#> [1] "Islington 022"
#> 
#> [[5]]$incode
#> [1] "1DN"
#> 
#> [[5]]$outcode
#> [1] "EC1A"
#> 
#> [[5]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[5]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[5]]$senedd_constituency
#> NULL
#> 
#> [[5]]$senedd_constituency_no
#> NULL
#> 
#> [[5]]$admin_district
#> [1] "Islington"
#> 
#> [[5]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[5]]$admin_county
#> NULL
#> 
#> [[5]]$date_of_introduction
#> [1] "200006"
#> 
#> [[5]]$date_of_termination
#> NULL
#> 
#> [[5]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[5]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[5]]$ced
#> NULL
#> 
#> [[5]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[5]]$nuts
#> [1] "Islington"
#> 
#> [[5]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[5]]$nhs_region
#> [1] "London"
#> 
#> [[5]]$ttwa
#> [1] "London"
#> 
#> [[5]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[5]]$bua
#> [1] "Islington"
#> 
#> [[5]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[5]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[5]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[5]]$msoa11
#> [1] "Islington 022"
#> 
#> [[5]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[5]]$msoa21
#> [1] "Islington 022"
#> 
#> [[5]]$oa21
#> [1] "E00013578"
#> 
#> [[5]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[5]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[5]]$lep1
#> [1] "London"
#> 
#> [[5]]$lep2
#> NULL
#> 
#> [[5]]$codes
#> [[5]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[5]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[5]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[5]]$codes$parish
#> [1] "E43000209"
#> 
#> [[5]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[5]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[5]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[5]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[5]]$codes$ced
#> [1] "E99999999"
#> 
#> [[5]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[5]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[5]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[5]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[5]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[5]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[5]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[5]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[5]]$codes$bua
#> [1] "E63011980"
#> 
#> [[5]]$codes$icb
#> [1] "E54000071"
#> 
#> [[5]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[5]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[5]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[5]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[5]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[5]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[5]]$codes$ruc11
#> [1] "A1"
#> 
#> [[5]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[5]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[5]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[6]]
#> [[6]]$postcode
#> [1] "EC1A 1DU"
#> 
#> [[6]]$quality
#> [1] 1
#> 
#> [[6]]$eastings
#> [1] 531073
#> 
#> [[6]]$northings
#> [1] 182317
#> 
#> [[6]]$country
#> [1] "England"
#> 
#> [[6]]$nhs_ha
#> [1] "London"
#> 
#> [[6]]$longitude
#> [1] -0.112017
#> 
#> [[6]]$latitude
#> [1] 51.52457
#> 
#> [[6]]$european_electoral_region
#> [1] "London"
#> 
#> [[6]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[6]]$region
#> [1] "London"
#> 
#> [[6]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[6]]$msoa
#> [1] "Islington 022"
#> 
#> [[6]]$incode
#> [1] "1DU"
#> 
#> [[6]]$outcode
#> [1] "EC1A"
#> 
#> [[6]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[6]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[6]]$senedd_constituency
#> NULL
#> 
#> [[6]]$senedd_constituency_no
#> NULL
#> 
#> [[6]]$admin_district
#> [1] "Islington"
#> 
#> [[6]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[6]]$admin_county
#> NULL
#> 
#> [[6]]$date_of_introduction
#> [1] "200012"
#> 
#> [[6]]$date_of_termination
#> NULL
#> 
#> [[6]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[6]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[6]]$ced
#> NULL
#> 
#> [[6]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[6]]$nuts
#> [1] "Islington"
#> 
#> [[6]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[6]]$nhs_region
#> [1] "London"
#> 
#> [[6]]$ttwa
#> [1] "London"
#> 
#> [[6]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[6]]$bua
#> [1] "Islington"
#> 
#> [[6]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[6]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[6]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[6]]$msoa11
#> [1] "Islington 022"
#> 
#> [[6]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[6]]$msoa21
#> [1] "Islington 022"
#> 
#> [[6]]$oa21
#> [1] "E00013578"
#> 
#> [[6]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[6]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[6]]$lep1
#> [1] "London"
#> 
#> [[6]]$lep2
#> NULL
#> 
#> [[6]]$codes
#> [[6]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[6]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[6]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[6]]$codes$parish
#> [1] "E43000209"
#> 
#> [[6]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[6]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[6]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[6]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[6]]$codes$ced
#> [1] "E99999999"
#> 
#> [[6]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[6]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[6]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[6]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[6]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[6]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[6]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[6]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[6]]$codes$bua
#> [1] "E63011980"
#> 
#> [[6]]$codes$icb
#> [1] "E54000071"
#> 
#> [[6]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[6]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[6]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[6]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[6]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[6]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[6]]$codes$ruc11
#> [1] "A1"
#> 
#> [[6]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[6]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[6]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[7]]
#> [[7]]$postcode
#> [1] "EC1A 1HQ"
#> 
#> [[7]]$quality
#> [1] 1
#> 
#> [[7]]$eastings
#> [1] 532008
#> 
#> [[7]]$northings
#> [1] 181428
#> 
#> [[7]]$country
#> [1] "England"
#> 
#> [[7]]$nhs_ha
#> [1] "London"
#> 
#> [[7]]$longitude
#> [1] -0.09888
#> 
#> [[7]]$latitude
#> [1] 51.51636
#> 
#> [[7]]$european_electoral_region
#> [1] "London"
#> 
#> [[7]]$primary_care_trust
#> [1] "City and Hackney Teaching"
#> 
#> [[7]]$region
#> [1] "London"
#> 
#> [[7]]$lsoa
#> [1] "City of London 001F"
#> 
#> [[7]]$msoa
#> [1] "City of London 001"
#> 
#> [[7]]$incode
#> [1] "1HQ"
#> 
#> [[7]]$outcode
#> [1] "EC1A"
#> 
#> [[7]]$parliamentary_constituency
#> [1] "Cities of London and Westminster"
#> 
#> [[7]]$parliamentary_constituency_2024
#> [1] "Cities of London and Westminster"
#> 
#> [[7]]$senedd_constituency
#> NULL
#> 
#> [[7]]$senedd_constituency_no
#> NULL
#> 
#> [[7]]$admin_district
#> [1] "City of London"
#> 
#> [[7]]$parish
#> [1] "City of London, unparished area"
#> 
#> [[7]]$admin_county
#> NULL
#> 
#> [[7]]$date_of_introduction
#> [1] "200206"
#> 
#> [[7]]$date_of_termination
#> NULL
#> 
#> [[7]]$index_of_multiple_deprivation
#> [1] 20391
#> 
#> [[7]]$admin_ward
#> [1] "Farringdon Within"
#> 
#> [[7]]$ced
#> NULL
#> 
#> [[7]]$ccg
#> [1] "NHS North East London"
#> 
#> [[7]]$nuts
#> [1] "City of London"
#> 
#> [[7]]$pfa
#> [1] "London, City of"
#> 
#> [[7]]$nhs_region
#> [1] "London"
#> 
#> [[7]]$ttwa
#> [1] "London"
#> 
#> [[7]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[7]]$bua
#> [1] "City and County of the City of London"
#> 
#> [[7]]$icb
#> [1] "NHS North East London Integrated Care Board"
#> 
#> [[7]]$cancer_alliance
#> [1] "North East London"
#> 
#> [[7]]$lsoa11
#> [1] "City of London 001F"
#> 
#> [[7]]$msoa11
#> [1] "City of London 001"
#> 
#> [[7]]$lsoa21
#> [1] "City of London 001F"
#> 
#> [[7]]$msoa21
#> [1] "City of London 001"
#> 
#> [[7]]$oa21
#> [1] "E00000024"
#> 
#> [[7]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[7]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[7]]$lep1
#> [1] "London"
#> 
#> [[7]]$lep2
#> NULL
#> 
#> [[7]]$codes
#> [[7]]$codes$admin_district
#> [1] "E09000001"
#> 
#> [[7]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[7]]$codes$admin_ward
#> [1] "E05009304"
#> 
#> [[7]]$codes$parish
#> [1] "E43000191"
#> 
#> [[7]]$codes$parliamentary_constituency
#> [1] "E14001172"
#> 
#> [[7]]$codes$parliamentary_constituency_2024
#> [1] "E14001172"
#> 
#> [[7]]$codes$ccg
#> [1] "E38000255"
#> 
#> [[7]]$codes$ccg_id
#> [1] "A3A8R"
#> 
#> [[7]]$codes$ced
#> [1] "E99999999"
#> 
#> [[7]]$codes$nuts
#> [1] "TLI35"
#> 
#> [[7]]$codes$lsoa
#> [1] "E01032739"
#> 
#> [[7]]$codes$msoa
#> [1] "E02000001"
#> 
#> [[7]]$codes$lau2
#> [1] "E09000001"
#> 
#> [[7]]$codes$pfa
#> [1] "E23000034"
#> 
#> [[7]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[7]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[7]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[7]]$codes$bua
#> [1] "E63012025"
#> 
#> [[7]]$codes$icb
#> [1] "E54000029"
#> 
#> [[7]]$codes$cancer_alliance
#> [1] "E56000028"
#> 
#> [[7]]$codes$lsoa11
#> [1] "E01032739"
#> 
#> [[7]]$codes$msoa11
#> [1] "E02000001"
#> 
#> [[7]]$codes$lsoa21
#> [1] "E01032739"
#> 
#> [[7]]$codes$msoa21
#> [1] "E02000001"
#> 
#> [[7]]$codes$oa21
#> [1] "E00000024"
#> 
#> [[7]]$codes$ruc11
#> [1] "A1"
#> 
#> [[7]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[7]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[7]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[8]]
#> [[8]]$postcode
#> [1] "EC1A 1SS"
#> 
#> [[8]]$quality
#> [1] 1
#> 
#> [[8]]$eastings
#> [1] 531073
#> 
#> [[8]]$northings
#> [1] 182317
#> 
#> [[8]]$country
#> [1] "England"
#> 
#> [[8]]$nhs_ha
#> [1] "London"
#> 
#> [[8]]$longitude
#> [1] -0.112017
#> 
#> [[8]]$latitude
#> [1] 51.52457
#> 
#> [[8]]$european_electoral_region
#> [1] "London"
#> 
#> [[8]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[8]]$region
#> [1] "London"
#> 
#> [[8]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[8]]$msoa
#> [1] "Islington 022"
#> 
#> [[8]]$incode
#> [1] "1SS"
#> 
#> [[8]]$outcode
#> [1] "EC1A"
#> 
#> [[8]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[8]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[8]]$senedd_constituency
#> NULL
#> 
#> [[8]]$senedd_constituency_no
#> NULL
#> 
#> [[8]]$admin_district
#> [1] "Islington"
#> 
#> [[8]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[8]]$admin_county
#> NULL
#> 
#> [[8]]$date_of_introduction
#> [1] "202507"
#> 
#> [[8]]$date_of_termination
#> NULL
#> 
#> [[8]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[8]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[8]]$ced
#> NULL
#> 
#> [[8]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[8]]$nuts
#> [1] "Islington"
#> 
#> [[8]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[8]]$nhs_region
#> [1] "London"
#> 
#> [[8]]$ttwa
#> [1] "London"
#> 
#> [[8]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[8]]$bua
#> [1] "Islington"
#> 
#> [[8]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[8]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[8]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[8]]$msoa11
#> [1] "Islington 022"
#> 
#> [[8]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[8]]$msoa21
#> [1] "Islington 022"
#> 
#> [[8]]$oa21
#> [1] "E00013578"
#> 
#> [[8]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[8]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[8]]$lep1
#> [1] "London"
#> 
#> [[8]]$lep2
#> NULL
#> 
#> [[8]]$codes
#> [[8]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[8]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[8]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[8]]$codes$parish
#> [1] "E43000209"
#> 
#> [[8]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[8]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[8]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[8]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[8]]$codes$ced
#> [1] "E99999999"
#> 
#> [[8]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[8]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[8]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[8]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[8]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[8]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[8]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[8]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[8]]$codes$bua
#> [1] "E63011980"
#> 
#> [[8]]$codes$icb
#> [1] "E54000071"
#> 
#> [[8]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[8]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[8]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[8]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[8]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[8]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[8]]$codes$ruc11
#> [1] "A1"
#> 
#> [[8]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[8]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[8]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[9]]
#> [[9]]$postcode
#> [1] "EC1A 1TA"
#> 
#> [[9]]$quality
#> [1] 1
#> 
#> [[9]]$eastings
#> [1] 531073
#> 
#> [[9]]$northings
#> [1] 182317
#> 
#> [[9]]$country
#> [1] "England"
#> 
#> [[9]]$nhs_ha
#> [1] "London"
#> 
#> [[9]]$longitude
#> [1] -0.112017
#> 
#> [[9]]$latitude
#> [1] 51.52457
#> 
#> [[9]]$european_electoral_region
#> [1] "London"
#> 
#> [[9]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[9]]$region
#> [1] "London"
#> 
#> [[9]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[9]]$msoa
#> [1] "Islington 022"
#> 
#> [[9]]$incode
#> [1] "1TA"
#> 
#> [[9]]$outcode
#> [1] "EC1A"
#> 
#> [[9]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[9]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[9]]$senedd_constituency
#> NULL
#> 
#> [[9]]$senedd_constituency_no
#> NULL
#> 
#> [[9]]$admin_district
#> [1] "Islington"
#> 
#> [[9]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[9]]$admin_county
#> NULL
#> 
#> [[9]]$date_of_introduction
#> [1] "200303"
#> 
#> [[9]]$date_of_termination
#> NULL
#> 
#> [[9]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[9]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[9]]$ced
#> NULL
#> 
#> [[9]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[9]]$nuts
#> [1] "Islington"
#> 
#> [[9]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[9]]$nhs_region
#> [1] "London"
#> 
#> [[9]]$ttwa
#> [1] "London"
#> 
#> [[9]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[9]]$bua
#> [1] "Islington"
#> 
#> [[9]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[9]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[9]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[9]]$msoa11
#> [1] "Islington 022"
#> 
#> [[9]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[9]]$msoa21
#> [1] "Islington 022"
#> 
#> [[9]]$oa21
#> [1] "E00013578"
#> 
#> [[9]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[9]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[9]]$lep1
#> [1] "London"
#> 
#> [[9]]$lep2
#> NULL
#> 
#> [[9]]$codes
#> [[9]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[9]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[9]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[9]]$codes$parish
#> [1] "E43000209"
#> 
#> [[9]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[9]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[9]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[9]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[9]]$codes$ced
#> [1] "E99999999"
#> 
#> [[9]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[9]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[9]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[9]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[9]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[9]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[9]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[9]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[9]]$codes$bua
#> [1] "E63011980"
#> 
#> [[9]]$codes$icb
#> [1] "E54000071"
#> 
#> [[9]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[9]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[9]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[9]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[9]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[9]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[9]]$codes$ruc11
#> [1] "A1"
#> 
#> [[9]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[9]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[9]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[10]]
#> [[10]]$postcode
#> [1] "EC1A 1TB"
#> 
#> [[10]]$quality
#> [1] 1
#> 
#> [[10]]$eastings
#> [1] 531073
#> 
#> [[10]]$northings
#> [1] 182317
#> 
#> [[10]]$country
#> [1] "England"
#> 
#> [[10]]$nhs_ha
#> [1] "London"
#> 
#> [[10]]$longitude
#> [1] -0.112017
#> 
#> [[10]]$latitude
#> [1] 51.52457
#> 
#> [[10]]$european_electoral_region
#> [1] "London"
#> 
#> [[10]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[10]]$region
#> [1] "London"
#> 
#> [[10]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[10]]$msoa
#> [1] "Islington 022"
#> 
#> [[10]]$incode
#> [1] "1TB"
#> 
#> [[10]]$outcode
#> [1] "EC1A"
#> 
#> [[10]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[10]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[10]]$senedd_constituency
#> NULL
#> 
#> [[10]]$senedd_constituency_no
#> NULL
#> 
#> [[10]]$admin_district
#> [1] "Islington"
#> 
#> [[10]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[10]]$admin_county
#> NULL
#> 
#> [[10]]$date_of_introduction
#> [1] "200303"
#> 
#> [[10]]$date_of_termination
#> NULL
#> 
#> [[10]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[10]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[10]]$ced
#> NULL
#> 
#> [[10]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[10]]$nuts
#> [1] "Islington"
#> 
#> [[10]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[10]]$nhs_region
#> [1] "London"
#> 
#> [[10]]$ttwa
#> [1] "London"
#> 
#> [[10]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[10]]$bua
#> [1] "Islington"
#> 
#> [[10]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[10]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[10]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[10]]$msoa11
#> [1] "Islington 022"
#> 
#> [[10]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[10]]$msoa21
#> [1] "Islington 022"
#> 
#> [[10]]$oa21
#> [1] "E00013578"
#> 
#> [[10]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[10]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[10]]$lep1
#> [1] "London"
#> 
#> [[10]]$lep2
#> NULL
#> 
#> [[10]]$codes
#> [[10]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[10]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[10]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[10]]$codes$parish
#> [1] "E43000209"
#> 
#> [[10]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[10]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[10]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[10]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[10]]$codes$ced
#> [1] "E99999999"
#> 
#> [[10]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[10]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[10]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[10]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[10]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[10]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[10]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[10]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[10]]$codes$bua
#> [1] "E63011980"
#> 
#> [[10]]$codes$icb
#> [1] "E54000071"
#> 
#> [[10]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[10]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[10]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[10]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[10]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[10]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[10]]$codes$ruc11
#> [1] "A1"
#> 
#> [[10]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[10]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[10]]$codes$lep2
#> NULL
#> 
#> 
#> 
#> [[11]]
#> [[11]]$postcode
#> [1] "EC1A 1TF"
#> 
#> [[11]]$quality
#> [1] 1
#> 
#> [[11]]$eastings
#> [1] 531073
#> 
#> [[11]]$northings
#> [1] 182317
#> 
#> [[11]]$country
#> [1] "England"
#> 
#> [[11]]$nhs_ha
#> [1] "London"
#> 
#> [[11]]$longitude
#> [1] -0.112017
#> 
#> [[11]]$latitude
#> [1] 51.52457
#> 
#> [[11]]$european_electoral_region
#> [1] "London"
#> 
#> [[11]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[11]]$region
#> [1] "London"
#> 
#> [[11]]$lsoa
#> [1] "Islington 022F"
#> 
#> [[11]]$msoa
#> [1] "Islington 022"
#> 
#> [[11]]$incode
#> [1] "1TF"
#> 
#> [[11]]$outcode
#> [1] "EC1A"
#> 
#> [[11]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[11]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[11]]$senedd_constituency
#> NULL
#> 
#> [[11]]$senedd_constituency_no
#> NULL
#> 
#> [[11]]$admin_district
#> [1] "Islington"
#> 
#> [[11]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[11]]$admin_county
#> NULL
#> 
#> [[11]]$date_of_introduction
#> [1] "200303"
#> 
#> [[11]]$date_of_termination
#> NULL
#> 
#> [[11]]$index_of_multiple_deprivation
#> [1] 11070
#> 
#> [[11]]$admin_ward
#> [1] "Clerkenwell"
#> 
#> [[11]]$ced
#> NULL
#> 
#> [[11]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[11]]$nuts
#> [1] "Islington"
#> 
#> [[11]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[11]]$nhs_region
#> [1] "London"
#> 
#> [[11]]$ttwa
#> [1] "London"
#> 
#> [[11]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[11]]$bua
#> [1] "Islington"
#> 
#> [[11]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[11]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[11]]$lsoa11
#> [1] "Islington 022F"
#> 
#> [[11]]$msoa11
#> [1] "Islington 022"
#> 
#> [[11]]$lsoa21
#> [1] "Islington 022F"
#> 
#> [[11]]$msoa21
#> [1] "Islington 022"
#> 
#> [[11]]$oa21
#> [1] "E00013578"
#> 
#> [[11]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[11]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[11]]$lep1
#> [1] "London"
#> 
#> [[11]]$lep2
#> NULL
#> 
#> [[11]]$codes
#> [[11]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[11]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[11]]$codes$admin_ward
#> [1] "E05013702"
#> 
#> [[11]]$codes$parish
#> [1] "E43000209"
#> 
#> [[11]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[11]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[11]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[11]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[11]]$codes$ced
#> [1] "E99999999"
#> 
#> [[11]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[11]]$codes$lsoa
#> [1] "E01002726"
#> 
#> [[11]]$codes$msoa
#> [1] "E02000575"
#> 
#> [[11]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[11]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[11]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[11]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[11]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[11]]$codes$bua
#> [1] "E63011980"
#> 
#> [[11]]$codes$icb
#> [1] "E54000071"
#> 
#> [[11]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[11]]$codes$lsoa11
#> [1] "E01002726"
#> 
#> [[11]]$codes$msoa11
#> [1] "E02000575"
#> 
#> [[11]]$codes$lsoa21
#> [1] "E01002726"
#> 
#> [[11]]$codes$msoa21
#> [1] "E02000575"
#> 
#> [[11]]$codes$oa21
#> [1] "E00013578"
#> 
#> [[11]]$codes$ruc11
#> [1] "A1"
#> 
#> [[11]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[11]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[11]]$codes$lep2
#> NULL
#> 
#> 
#> 
# }
```
