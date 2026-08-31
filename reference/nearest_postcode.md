# Nearest postcode

Returns nearest postcodes for a given postcode. The search is based on
the relative distance of the postcode centroid.

## Usage

``` r
nearest_postcode(postcode, limit = 10, radius = 100)
```

## Arguments

- postcode:

  A string. Valid UK postcode.

- limit:

  A string or integer. Limits number of postcodes matches to return.
  Defaults to 10. Needs to be lower than 100.

- radius:

  Limits number of postcodes matches to return. Defaults to 100m. Needs
  to be less than 2,000m.

## Value

A list of geographic properties of the nearest postcode.

## Examples

``` r
# \donttest{
nearest_postcode("EC1Y 8LX")
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
#> [[1]]$distance
#> [1] 0
#> 
#> 
#> [[2]]
#> [[2]]$postcode
#> [1] "EC1Y 8LD"
#> 
#> [[2]]$quality
#> [1] 1
#> 
#> [[2]]$eastings
#> [1] 532565
#> 
#> [[2]]$northings
#> [1] 182142
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$nhs_ha
#> [1] "London"
#> 
#> [[2]]$longitude
#> [1] -0.090589
#> 
#> [[2]]$latitude
#> [1] 51.52265
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
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa
#> [1] "Islington 023"
#> 
#> [[2]]$incode
#> [1] "8LD"
#> 
#> [[2]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[2]]$date_of_termination
#> NULL
#> 
#> [[2]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[2]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa11
#> [1] "Islington 023"
#> 
#> [[2]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa21
#> [1] "Islington 023"
#> 
#> [[2]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[2]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[2]]$codes$oa21
#> [1] "E00013462"
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
#> [[2]]$distance
#> [1] 25.14302
#> 
#> 
#> [[3]]
#> [[3]]$postcode
#> [1] "EC1Y 8LE"
#> 
#> [[3]]$quality
#> [1] 1
#> 
#> [[3]]$eastings
#> [1] 532563
#> 
#> [[3]]$northings
#> [1] 182101
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$nhs_ha
#> [1] "London"
#> 
#> [[3]]$longitude
#> [1] -0.090633
#> 
#> [[3]]$latitude
#> [1] 51.52228
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
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa
#> [1] "Islington 023"
#> 
#> [[3]]$incode
#> [1] "8LE"
#> 
#> [[3]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[3]]$date_of_termination
#> NULL
#> 
#> [[3]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[3]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa11
#> [1] "Islington 023"
#> 
#> [[3]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa21
#> [1] "Islington 023"
#> 
#> [[3]]$oa21
#> [1] "E00013428"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[3]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[3]]$codes$oa21
#> [1] "E00013428"
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
#> [[3]]$distance
#> [1] 32.94591
#> 
#> 
#> [[4]]
#> [[4]]$postcode
#> [1] "EC1Y 8SE"
#> 
#> [[4]]$quality
#> [1] 1
#> 
#> [[4]]$eastings
#> [1] 532508
#> 
#> [[4]]$northings
#> [1] 182130
#> 
#> [[4]]$country
#> [1] "England"
#> 
#> [[4]]$nhs_ha
#> [1] "London"
#> 
#> [[4]]$longitude
#> [1] -0.091414
#> 
#> [[4]]$latitude
#> [1] 51.52255
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
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa
#> [1] "Islington 023"
#> 
#> [[4]]$incode
#> [1] "8SE"
#> 
#> [[4]]$outcode
#> [1] "EC1Y"
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
#> [1] "201802"
#> 
#> [[4]]$date_of_termination
#> NULL
#> 
#> [[4]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[4]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa11
#> [1] "Islington 023"
#> 
#> [[4]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa21
#> [1] "Islington 023"
#> 
#> [[4]]$oa21
#> [1] "E00013429"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[4]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[4]]$codes$oa21
#> [1] "E00013429"
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
#> [[4]]$distance
#> [1] 35.96405
#> 
#> 
#> [[5]]
#> [[5]]$postcode
#> [1] "EC1Y 8LS"
#> 
#> [[5]]$quality
#> [1] 1
#> 
#> [[5]]$eastings
#> [1] 532524
#> 
#> [[5]]$northings
#> [1] 182170
#> 
#> [[5]]$country
#> [1] "England"
#> 
#> [[5]]$nhs_ha
#> [1] "London"
#> 
#> [[5]]$longitude
#> [1] -0.091169
#> 
#> [[5]]$latitude
#> [1] 51.52291
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
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa
#> [1] "Islington 023"
#> 
#> [[5]]$incode
#> [1] "8LS"
#> 
#> [[5]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[5]]$date_of_termination
#> NULL
#> 
#> [[5]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[5]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa11
#> [1] "Islington 023"
#> 
#> [[5]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa21
#> [1] "Islington 023"
#> 
#> [[5]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[5]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[5]]$codes$oa21
#> [1] "E00013462"
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
#> [[5]]$distance
#> [1] 46.58822
#> 
#> 
#> [[6]]
#> [[6]]$postcode
#> [1] "EC1Y 8AL"
#> 
#> [[6]]$quality
#> [1] 1
#> 
#> [[6]]$eastings
#> [1] 532596
#> 
#> [[6]]$northings
#> [1] 182120
#> 
#> [[6]]$country
#> [1] "England"
#> 
#> [[6]]$nhs_ha
#> [1] "London"
#> 
#> [[6]]$longitude
#> [1] -0.09015
#> 
#> [[6]]$latitude
#> [1] 51.52244
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
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa
#> [1] "Islington 023"
#> 
#> [[6]]$incode
#> [1] "8AL"
#> 
#> [[6]]$outcode
#> [1] "EC1Y"
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
#> [1] "202506"
#> 
#> [[6]]$date_of_termination
#> NULL
#> 
#> [[6]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[6]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa11
#> [1] "Islington 023"
#> 
#> [[6]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa21
#> [1] "Islington 023"
#> 
#> [[6]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[6]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[6]]$codes$oa21
#> [1] "E00013462"
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
#> [[6]]$distance
#> [1] 52.45142
#> 
#> 
#> [[7]]
#> [[7]]$postcode
#> [1] "EC1Y 8LT"
#> 
#> [[7]]$quality
#> [1] 1
#> 
#> [[7]]$eastings
#> [1] 532502
#> 
#> [[7]]$northings
#> [1] 182162
#> 
#> [[7]]$country
#> [1] "England"
#> 
#> [[7]]$nhs_ha
#> [1] "London"
#> 
#> [[7]]$longitude
#> [1] -0.091489
#> 
#> [[7]]$latitude
#> [1] 51.52284
#> 
#> [[7]]$european_electoral_region
#> [1] "London"
#> 
#> [[7]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[7]]$region
#> [1] "London"
#> 
#> [[7]]$lsoa
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa
#> [1] "Islington 023"
#> 
#> [[7]]$incode
#> [1] "8LT"
#> 
#> [[7]]$outcode
#> [1] "EC1Y"
#> 
#> [[7]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[7]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[7]]$senedd_constituency
#> NULL
#> 
#> [[7]]$senedd_constituency_no
#> NULL
#> 
#> [[7]]$admin_district
#> [1] "Islington"
#> 
#> [[7]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[7]]$admin_county
#> NULL
#> 
#> [[7]]$date_of_introduction
#> [1] "198001"
#> 
#> [[7]]$date_of_termination
#> NULL
#> 
#> [[7]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[7]]$admin_ward
#> [1] "Bunhill"
#> 
#> [[7]]$ced
#> NULL
#> 
#> [[7]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[7]]$nuts
#> [1] "Islington"
#> 
#> [[7]]$pfa
#> [1] "Metropolitan Police"
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
#> [1] "Islington"
#> 
#> [[7]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[7]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[7]]$lsoa11
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa11
#> [1] "Islington 023"
#> 
#> [[7]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa21
#> [1] "Islington 023"
#> 
#> [[7]]$oa21
#> [1] "E00013462"
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
#> [1] "E09000019"
#> 
#> [[7]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[7]]$codes$admin_ward
#> [1] "E05013699"
#> 
#> [[7]]$codes$parish
#> [1] "E43000209"
#> 
#> [[7]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[7]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[7]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[7]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[7]]$codes$ced
#> [1] "E99999999"
#> 
#> [[7]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[7]]$codes$lsoa
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa
#> [1] "E02000576"
#> 
#> [[7]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[7]]$codes$pfa
#> [1] "E23000001"
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
#> [1] "E63011980"
#> 
#> [[7]]$codes$icb
#> [1] "E54000071"
#> 
#> [[7]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[7]]$codes$lsoa11
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[7]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[7]]$codes$oa21
#> [1] "E00013462"
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
#> [[7]]$distance
#> [1] 54.01758
#> 
#> 
#> [[8]]
#> [[8]]$postcode
#> [1] "EC1Y 8NJ"
#> 
#> [[8]]$quality
#> [1] 1
#> 
#> [[8]]$eastings
#> [1] 532564
#> 
#> [[8]]$northings
#> [1] 182184
#> 
#> [[8]]$country
#> [1] "England"
#> 
#> [[8]]$nhs_ha
#> [1] "London"
#> 
#> [[8]]$longitude
#> [1] -0.090587
#> 
#> [[8]]$latitude
#> [1] 51.52302
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
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa
#> [1] "Islington 023"
#> 
#> [[8]]$incode
#> [1] "8NJ"
#> 
#> [[8]]$outcode
#> [1] "EC1Y"
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
#> [1] "199301"
#> 
#> [[8]]$date_of_termination
#> NULL
#> 
#> [[8]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[8]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa11
#> [1] "Islington 023"
#> 
#> [[8]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa21
#> [1] "Islington 023"
#> 
#> [[8]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[8]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[8]]$codes$oa21
#> [1] "E00013462"
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
#> [[8]]$distance
#> [1] 59.46237
#> 
#> 
#> [[9]]
#> [[9]]$postcode
#> [1] "EC1Y 8NH"
#> 
#> [[9]]$quality
#> [1] 1
#> 
#> [[9]]$eastings
#> [1] 532564
#> 
#> [[9]]$northings
#> [1] 182184
#> 
#> [[9]]$country
#> [1] "England"
#> 
#> [[9]]$nhs_ha
#> [1] "London"
#> 
#> [[9]]$longitude
#> [1] -0.090587
#> 
#> [[9]]$latitude
#> [1] 51.52302
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
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa
#> [1] "Islington 023"
#> 
#> [[9]]$incode
#> [1] "8NH"
#> 
#> [[9]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[9]]$date_of_termination
#> NULL
#> 
#> [[9]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[9]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa11
#> [1] "Islington 023"
#> 
#> [[9]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa21
#> [1] "Islington 023"
#> 
#> [[9]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[9]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[9]]$codes$oa21
#> [1] "E00013462"
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
#> [[9]]$distance
#> [1] 59.46237
#> 
#> 
#> [[10]]
#> [[10]]$postcode
#> [1] "EC1Y 8TZ"
#> 
#> [[10]]$quality
#> [1] 1
#> 
#> [[10]]$eastings
#> [1] 532580
#> 
#> [[10]]$northings
#> [1] 182080
#> 
#> [[10]]$country
#> [1] "England"
#> 
#> [[10]]$nhs_ha
#> [1] "London"
#> 
#> [[10]]$longitude
#> [1] -0.090396
#> 
#> [[10]]$latitude
#> [1] 51.52209
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
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa
#> [1] "Islington 023"
#> 
#> [[10]]$incode
#> [1] "8TZ"
#> 
#> [[10]]$outcode
#> [1] "EC1Y"
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
#> [1] "200205"
#> 
#> [[10]]$date_of_termination
#> NULL
#> 
#> [[10]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[10]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa11
#> [1] "Islington 023"
#> 
#> [[10]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa21
#> [1] "Islington 023"
#> 
#> [[10]]$oa21
#> [1] "E00013428"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[10]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[10]]$codes$oa21
#> [1] "E00013428"
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
#> [[10]]$distance
#> [1] 59.82949
#> 
#> 
nearest_postcode("EC1Y 8LX", limit = 11)
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
#> [[1]]$distance
#> [1] 0
#> 
#> 
#> [[2]]
#> [[2]]$postcode
#> [1] "EC1Y 8LD"
#> 
#> [[2]]$quality
#> [1] 1
#> 
#> [[2]]$eastings
#> [1] 532565
#> 
#> [[2]]$northings
#> [1] 182142
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$nhs_ha
#> [1] "London"
#> 
#> [[2]]$longitude
#> [1] -0.090589
#> 
#> [[2]]$latitude
#> [1] 51.52265
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
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa
#> [1] "Islington 023"
#> 
#> [[2]]$incode
#> [1] "8LD"
#> 
#> [[2]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[2]]$date_of_termination
#> NULL
#> 
#> [[2]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[2]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa11
#> [1] "Islington 023"
#> 
#> [[2]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa21
#> [1] "Islington 023"
#> 
#> [[2]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[2]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[2]]$codes$oa21
#> [1] "E00013462"
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
#> [[2]]$distance
#> [1] 25.14302
#> 
#> 
#> [[3]]
#> [[3]]$postcode
#> [1] "EC1Y 8LE"
#> 
#> [[3]]$quality
#> [1] 1
#> 
#> [[3]]$eastings
#> [1] 532563
#> 
#> [[3]]$northings
#> [1] 182101
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$nhs_ha
#> [1] "London"
#> 
#> [[3]]$longitude
#> [1] -0.090633
#> 
#> [[3]]$latitude
#> [1] 51.52228
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
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa
#> [1] "Islington 023"
#> 
#> [[3]]$incode
#> [1] "8LE"
#> 
#> [[3]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[3]]$date_of_termination
#> NULL
#> 
#> [[3]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[3]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa11
#> [1] "Islington 023"
#> 
#> [[3]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa21
#> [1] "Islington 023"
#> 
#> [[3]]$oa21
#> [1] "E00013428"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[3]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[3]]$codes$oa21
#> [1] "E00013428"
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
#> [[3]]$distance
#> [1] 32.94591
#> 
#> 
#> [[4]]
#> [[4]]$postcode
#> [1] "EC1Y 8SE"
#> 
#> [[4]]$quality
#> [1] 1
#> 
#> [[4]]$eastings
#> [1] 532508
#> 
#> [[4]]$northings
#> [1] 182130
#> 
#> [[4]]$country
#> [1] "England"
#> 
#> [[4]]$nhs_ha
#> [1] "London"
#> 
#> [[4]]$longitude
#> [1] -0.091414
#> 
#> [[4]]$latitude
#> [1] 51.52255
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
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa
#> [1] "Islington 023"
#> 
#> [[4]]$incode
#> [1] "8SE"
#> 
#> [[4]]$outcode
#> [1] "EC1Y"
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
#> [1] "201802"
#> 
#> [[4]]$date_of_termination
#> NULL
#> 
#> [[4]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[4]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa11
#> [1] "Islington 023"
#> 
#> [[4]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa21
#> [1] "Islington 023"
#> 
#> [[4]]$oa21
#> [1] "E00013429"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[4]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[4]]$codes$oa21
#> [1] "E00013429"
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
#> [[4]]$distance
#> [1] 35.96405
#> 
#> 
#> [[5]]
#> [[5]]$postcode
#> [1] "EC1Y 8LS"
#> 
#> [[5]]$quality
#> [1] 1
#> 
#> [[5]]$eastings
#> [1] 532524
#> 
#> [[5]]$northings
#> [1] 182170
#> 
#> [[5]]$country
#> [1] "England"
#> 
#> [[5]]$nhs_ha
#> [1] "London"
#> 
#> [[5]]$longitude
#> [1] -0.091169
#> 
#> [[5]]$latitude
#> [1] 51.52291
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
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa
#> [1] "Islington 023"
#> 
#> [[5]]$incode
#> [1] "8LS"
#> 
#> [[5]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[5]]$date_of_termination
#> NULL
#> 
#> [[5]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[5]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa11
#> [1] "Islington 023"
#> 
#> [[5]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa21
#> [1] "Islington 023"
#> 
#> [[5]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[5]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[5]]$codes$oa21
#> [1] "E00013462"
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
#> [[5]]$distance
#> [1] 46.58822
#> 
#> 
#> [[6]]
#> [[6]]$postcode
#> [1] "EC1Y 8AL"
#> 
#> [[6]]$quality
#> [1] 1
#> 
#> [[6]]$eastings
#> [1] 532596
#> 
#> [[6]]$northings
#> [1] 182120
#> 
#> [[6]]$country
#> [1] "England"
#> 
#> [[6]]$nhs_ha
#> [1] "London"
#> 
#> [[6]]$longitude
#> [1] -0.09015
#> 
#> [[6]]$latitude
#> [1] 51.52244
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
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa
#> [1] "Islington 023"
#> 
#> [[6]]$incode
#> [1] "8AL"
#> 
#> [[6]]$outcode
#> [1] "EC1Y"
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
#> [1] "202506"
#> 
#> [[6]]$date_of_termination
#> NULL
#> 
#> [[6]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[6]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa11
#> [1] "Islington 023"
#> 
#> [[6]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa21
#> [1] "Islington 023"
#> 
#> [[6]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[6]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[6]]$codes$oa21
#> [1] "E00013462"
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
#> [[6]]$distance
#> [1] 52.45142
#> 
#> 
#> [[7]]
#> [[7]]$postcode
#> [1] "EC1Y 8LT"
#> 
#> [[7]]$quality
#> [1] 1
#> 
#> [[7]]$eastings
#> [1] 532502
#> 
#> [[7]]$northings
#> [1] 182162
#> 
#> [[7]]$country
#> [1] "England"
#> 
#> [[7]]$nhs_ha
#> [1] "London"
#> 
#> [[7]]$longitude
#> [1] -0.091489
#> 
#> [[7]]$latitude
#> [1] 51.52284
#> 
#> [[7]]$european_electoral_region
#> [1] "London"
#> 
#> [[7]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[7]]$region
#> [1] "London"
#> 
#> [[7]]$lsoa
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa
#> [1] "Islington 023"
#> 
#> [[7]]$incode
#> [1] "8LT"
#> 
#> [[7]]$outcode
#> [1] "EC1Y"
#> 
#> [[7]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[7]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[7]]$senedd_constituency
#> NULL
#> 
#> [[7]]$senedd_constituency_no
#> NULL
#> 
#> [[7]]$admin_district
#> [1] "Islington"
#> 
#> [[7]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[7]]$admin_county
#> NULL
#> 
#> [[7]]$date_of_introduction
#> [1] "198001"
#> 
#> [[7]]$date_of_termination
#> NULL
#> 
#> [[7]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[7]]$admin_ward
#> [1] "Bunhill"
#> 
#> [[7]]$ced
#> NULL
#> 
#> [[7]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[7]]$nuts
#> [1] "Islington"
#> 
#> [[7]]$pfa
#> [1] "Metropolitan Police"
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
#> [1] "Islington"
#> 
#> [[7]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[7]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[7]]$lsoa11
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa11
#> [1] "Islington 023"
#> 
#> [[7]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa21
#> [1] "Islington 023"
#> 
#> [[7]]$oa21
#> [1] "E00013462"
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
#> [1] "E09000019"
#> 
#> [[7]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[7]]$codes$admin_ward
#> [1] "E05013699"
#> 
#> [[7]]$codes$parish
#> [1] "E43000209"
#> 
#> [[7]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[7]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[7]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[7]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[7]]$codes$ced
#> [1] "E99999999"
#> 
#> [[7]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[7]]$codes$lsoa
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa
#> [1] "E02000576"
#> 
#> [[7]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[7]]$codes$pfa
#> [1] "E23000001"
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
#> [1] "E63011980"
#> 
#> [[7]]$codes$icb
#> [1] "E54000071"
#> 
#> [[7]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[7]]$codes$lsoa11
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[7]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[7]]$codes$oa21
#> [1] "E00013462"
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
#> [[7]]$distance
#> [1] 54.01758
#> 
#> 
#> [[8]]
#> [[8]]$postcode
#> [1] "EC1Y 8NH"
#> 
#> [[8]]$quality
#> [1] 1
#> 
#> [[8]]$eastings
#> [1] 532564
#> 
#> [[8]]$northings
#> [1] 182184
#> 
#> [[8]]$country
#> [1] "England"
#> 
#> [[8]]$nhs_ha
#> [1] "London"
#> 
#> [[8]]$longitude
#> [1] -0.090587
#> 
#> [[8]]$latitude
#> [1] 51.52302
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
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa
#> [1] "Islington 023"
#> 
#> [[8]]$incode
#> [1] "8NH"
#> 
#> [[8]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[8]]$date_of_termination
#> NULL
#> 
#> [[8]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[8]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa11
#> [1] "Islington 023"
#> 
#> [[8]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa21
#> [1] "Islington 023"
#> 
#> [[8]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[8]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[8]]$codes$oa21
#> [1] "E00013462"
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
#> [[8]]$distance
#> [1] 59.46237
#> 
#> 
#> [[9]]
#> [[9]]$postcode
#> [1] "EC1Y 8NJ"
#> 
#> [[9]]$quality
#> [1] 1
#> 
#> [[9]]$eastings
#> [1] 532564
#> 
#> [[9]]$northings
#> [1] 182184
#> 
#> [[9]]$country
#> [1] "England"
#> 
#> [[9]]$nhs_ha
#> [1] "London"
#> 
#> [[9]]$longitude
#> [1] -0.090587
#> 
#> [[9]]$latitude
#> [1] 51.52302
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
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa
#> [1] "Islington 023"
#> 
#> [[9]]$incode
#> [1] "8NJ"
#> 
#> [[9]]$outcode
#> [1] "EC1Y"
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
#> [1] "199301"
#> 
#> [[9]]$date_of_termination
#> NULL
#> 
#> [[9]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[9]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa11
#> [1] "Islington 023"
#> 
#> [[9]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa21
#> [1] "Islington 023"
#> 
#> [[9]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[9]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[9]]$codes$oa21
#> [1] "E00013462"
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
#> [[9]]$distance
#> [1] 59.46237
#> 
#> 
#> [[10]]
#> [[10]]$postcode
#> [1] "EC1Y 8TZ"
#> 
#> [[10]]$quality
#> [1] 1
#> 
#> [[10]]$eastings
#> [1] 532580
#> 
#> [[10]]$northings
#> [1] 182080
#> 
#> [[10]]$country
#> [1] "England"
#> 
#> [[10]]$nhs_ha
#> [1] "London"
#> 
#> [[10]]$longitude
#> [1] -0.090396
#> 
#> [[10]]$latitude
#> [1] 51.52209
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
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa
#> [1] "Islington 023"
#> 
#> [[10]]$incode
#> [1] "8TZ"
#> 
#> [[10]]$outcode
#> [1] "EC1Y"
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
#> [1] "200205"
#> 
#> [[10]]$date_of_termination
#> NULL
#> 
#> [[10]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[10]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa11
#> [1] "Islington 023"
#> 
#> [[10]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa21
#> [1] "Islington 023"
#> 
#> [[10]]$oa21
#> [1] "E00013428"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[10]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[10]]$codes$oa21
#> [1] "E00013428"
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
#> [[10]]$distance
#> [1] 59.82949
#> 
#> 
#> [[11]]
#> [[11]]$postcode
#> [1] "EC1Y 8LZ"
#> 
#> [[11]]$quality
#> [1] 1
#> 
#> [[11]]$eastings
#> [1] 532600
#> 
#> [[11]]$northings
#> [1] 182163
#> 
#> [[11]]$country
#> [1] "England"
#> 
#> [[11]]$nhs_ha
#> [1] "London"
#> 
#> [[11]]$longitude
#> [1] -0.090076
#> 
#> [[11]]$latitude
#> [1] 51.52283
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
#> [1] "Islington 023D"
#> 
#> [[11]]$msoa
#> [1] "Islington 023"
#> 
#> [[11]]$incode
#> [1] "8LZ"
#> 
#> [[11]]$outcode
#> [1] "EC1Y"
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
#> [1] "202211"
#> 
#> [[11]]$date_of_termination
#> NULL
#> 
#> [[11]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[11]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[11]]$msoa11
#> [1] "Islington 023"
#> 
#> [[11]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[11]]$msoa21
#> [1] "Islington 023"
#> 
#> [[11]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[11]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[11]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[11]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[11]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[11]]$codes$oa21
#> [1] "E00013462"
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
#> [[11]]$distance
#> [1] 65.92623
#> 
#> 
nearest_postcode("EC1Y 8LX", limit = 12, radius = 200)
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
#> [[1]]$distance
#> [1] 0
#> 
#> 
#> [[2]]
#> [[2]]$postcode
#> [1] "EC1Y 8LD"
#> 
#> [[2]]$quality
#> [1] 1
#> 
#> [[2]]$eastings
#> [1] 532565
#> 
#> [[2]]$northings
#> [1] 182142
#> 
#> [[2]]$country
#> [1] "England"
#> 
#> [[2]]$nhs_ha
#> [1] "London"
#> 
#> [[2]]$longitude
#> [1] -0.090589
#> 
#> [[2]]$latitude
#> [1] 51.52265
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
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa
#> [1] "Islington 023"
#> 
#> [[2]]$incode
#> [1] "8LD"
#> 
#> [[2]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[2]]$date_of_termination
#> NULL
#> 
#> [[2]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[2]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa11
#> [1] "Islington 023"
#> 
#> [[2]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[2]]$msoa21
#> [1] "Islington 023"
#> 
#> [[2]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[2]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[2]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[2]]$codes$oa21
#> [1] "E00013462"
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
#> [[2]]$distance
#> [1] 25.14302
#> 
#> 
#> [[3]]
#> [[3]]$postcode
#> [1] "EC1Y 8LE"
#> 
#> [[3]]$quality
#> [1] 1
#> 
#> [[3]]$eastings
#> [1] 532563
#> 
#> [[3]]$northings
#> [1] 182101
#> 
#> [[3]]$country
#> [1] "England"
#> 
#> [[3]]$nhs_ha
#> [1] "London"
#> 
#> [[3]]$longitude
#> [1] -0.090633
#> 
#> [[3]]$latitude
#> [1] 51.52228
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
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa
#> [1] "Islington 023"
#> 
#> [[3]]$incode
#> [1] "8LE"
#> 
#> [[3]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[3]]$date_of_termination
#> NULL
#> 
#> [[3]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[3]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa11
#> [1] "Islington 023"
#> 
#> [[3]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[3]]$msoa21
#> [1] "Islington 023"
#> 
#> [[3]]$oa21
#> [1] "E00013428"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[3]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[3]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[3]]$codes$oa21
#> [1] "E00013428"
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
#> [[3]]$distance
#> [1] 32.94591
#> 
#> 
#> [[4]]
#> [[4]]$postcode
#> [1] "EC1Y 8SE"
#> 
#> [[4]]$quality
#> [1] 1
#> 
#> [[4]]$eastings
#> [1] 532508
#> 
#> [[4]]$northings
#> [1] 182130
#> 
#> [[4]]$country
#> [1] "England"
#> 
#> [[4]]$nhs_ha
#> [1] "London"
#> 
#> [[4]]$longitude
#> [1] -0.091414
#> 
#> [[4]]$latitude
#> [1] 51.52255
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
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa
#> [1] "Islington 023"
#> 
#> [[4]]$incode
#> [1] "8SE"
#> 
#> [[4]]$outcode
#> [1] "EC1Y"
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
#> [1] "201802"
#> 
#> [[4]]$date_of_termination
#> NULL
#> 
#> [[4]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[4]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa11
#> [1] "Islington 023"
#> 
#> [[4]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[4]]$msoa21
#> [1] "Islington 023"
#> 
#> [[4]]$oa21
#> [1] "E00013429"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[4]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[4]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[4]]$codes$oa21
#> [1] "E00013429"
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
#> [[4]]$distance
#> [1] 35.96405
#> 
#> 
#> [[5]]
#> [[5]]$postcode
#> [1] "EC1Y 8LS"
#> 
#> [[5]]$quality
#> [1] 1
#> 
#> [[5]]$eastings
#> [1] 532524
#> 
#> [[5]]$northings
#> [1] 182170
#> 
#> [[5]]$country
#> [1] "England"
#> 
#> [[5]]$nhs_ha
#> [1] "London"
#> 
#> [[5]]$longitude
#> [1] -0.091169
#> 
#> [[5]]$latitude
#> [1] 51.52291
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
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa
#> [1] "Islington 023"
#> 
#> [[5]]$incode
#> [1] "8LS"
#> 
#> [[5]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[5]]$date_of_termination
#> NULL
#> 
#> [[5]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[5]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa11
#> [1] "Islington 023"
#> 
#> [[5]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[5]]$msoa21
#> [1] "Islington 023"
#> 
#> [[5]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[5]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[5]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[5]]$codes$oa21
#> [1] "E00013462"
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
#> [[5]]$distance
#> [1] 46.58822
#> 
#> 
#> [[6]]
#> [[6]]$postcode
#> [1] "EC1Y 8AL"
#> 
#> [[6]]$quality
#> [1] 1
#> 
#> [[6]]$eastings
#> [1] 532596
#> 
#> [[6]]$northings
#> [1] 182120
#> 
#> [[6]]$country
#> [1] "England"
#> 
#> [[6]]$nhs_ha
#> [1] "London"
#> 
#> [[6]]$longitude
#> [1] -0.09015
#> 
#> [[6]]$latitude
#> [1] 51.52244
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
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa
#> [1] "Islington 023"
#> 
#> [[6]]$incode
#> [1] "8AL"
#> 
#> [[6]]$outcode
#> [1] "EC1Y"
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
#> [1] "202506"
#> 
#> [[6]]$date_of_termination
#> NULL
#> 
#> [[6]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[6]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa11
#> [1] "Islington 023"
#> 
#> [[6]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[6]]$msoa21
#> [1] "Islington 023"
#> 
#> [[6]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[6]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[6]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[6]]$codes$oa21
#> [1] "E00013462"
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
#> [[6]]$distance
#> [1] 52.45142
#> 
#> 
#> [[7]]
#> [[7]]$postcode
#> [1] "EC1Y 8LT"
#> 
#> [[7]]$quality
#> [1] 1
#> 
#> [[7]]$eastings
#> [1] 532502
#> 
#> [[7]]$northings
#> [1] 182162
#> 
#> [[7]]$country
#> [1] "England"
#> 
#> [[7]]$nhs_ha
#> [1] "London"
#> 
#> [[7]]$longitude
#> [1] -0.091489
#> 
#> [[7]]$latitude
#> [1] 51.52284
#> 
#> [[7]]$european_electoral_region
#> [1] "London"
#> 
#> [[7]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[7]]$region
#> [1] "London"
#> 
#> [[7]]$lsoa
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa
#> [1] "Islington 023"
#> 
#> [[7]]$incode
#> [1] "8LT"
#> 
#> [[7]]$outcode
#> [1] "EC1Y"
#> 
#> [[7]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[7]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[7]]$senedd_constituency
#> NULL
#> 
#> [[7]]$senedd_constituency_no
#> NULL
#> 
#> [[7]]$admin_district
#> [1] "Islington"
#> 
#> [[7]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[7]]$admin_county
#> NULL
#> 
#> [[7]]$date_of_introduction
#> [1] "198001"
#> 
#> [[7]]$date_of_termination
#> NULL
#> 
#> [[7]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[7]]$admin_ward
#> [1] "Bunhill"
#> 
#> [[7]]$ced
#> NULL
#> 
#> [[7]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[7]]$nuts
#> [1] "Islington"
#> 
#> [[7]]$pfa
#> [1] "Metropolitan Police"
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
#> [1] "Islington"
#> 
#> [[7]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[7]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[7]]$lsoa11
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa11
#> [1] "Islington 023"
#> 
#> [[7]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[7]]$msoa21
#> [1] "Islington 023"
#> 
#> [[7]]$oa21
#> [1] "E00013462"
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
#> [1] "E09000019"
#> 
#> [[7]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[7]]$codes$admin_ward
#> [1] "E05013699"
#> 
#> [[7]]$codes$parish
#> [1] "E43000209"
#> 
#> [[7]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[7]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[7]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[7]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[7]]$codes$ced
#> [1] "E99999999"
#> 
#> [[7]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[7]]$codes$lsoa
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa
#> [1] "E02000576"
#> 
#> [[7]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[7]]$codes$pfa
#> [1] "E23000001"
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
#> [1] "E63011980"
#> 
#> [[7]]$codes$icb
#> [1] "E54000071"
#> 
#> [[7]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[7]]$codes$lsoa11
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[7]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[7]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[7]]$codes$oa21
#> [1] "E00013462"
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
#> [[7]]$distance
#> [1] 54.01758
#> 
#> 
#> [[8]]
#> [[8]]$postcode
#> [1] "EC1Y 8NJ"
#> 
#> [[8]]$quality
#> [1] 1
#> 
#> [[8]]$eastings
#> [1] 532564
#> 
#> [[8]]$northings
#> [1] 182184
#> 
#> [[8]]$country
#> [1] "England"
#> 
#> [[8]]$nhs_ha
#> [1] "London"
#> 
#> [[8]]$longitude
#> [1] -0.090587
#> 
#> [[8]]$latitude
#> [1] 51.52302
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
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa
#> [1] "Islington 023"
#> 
#> [[8]]$incode
#> [1] "8NJ"
#> 
#> [[8]]$outcode
#> [1] "EC1Y"
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
#> [1] "199301"
#> 
#> [[8]]$date_of_termination
#> NULL
#> 
#> [[8]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[8]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa11
#> [1] "Islington 023"
#> 
#> [[8]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[8]]$msoa21
#> [1] "Islington 023"
#> 
#> [[8]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[8]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[8]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[8]]$codes$oa21
#> [1] "E00013462"
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
#> [[8]]$distance
#> [1] 59.46237
#> 
#> 
#> [[9]]
#> [[9]]$postcode
#> [1] "EC1Y 8NH"
#> 
#> [[9]]$quality
#> [1] 1
#> 
#> [[9]]$eastings
#> [1] 532564
#> 
#> [[9]]$northings
#> [1] 182184
#> 
#> [[9]]$country
#> [1] "England"
#> 
#> [[9]]$nhs_ha
#> [1] "London"
#> 
#> [[9]]$longitude
#> [1] -0.090587
#> 
#> [[9]]$latitude
#> [1] 51.52302
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
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa
#> [1] "Islington 023"
#> 
#> [[9]]$incode
#> [1] "8NH"
#> 
#> [[9]]$outcode
#> [1] "EC1Y"
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
#> [1] "198001"
#> 
#> [[9]]$date_of_termination
#> NULL
#> 
#> [[9]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[9]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa11
#> [1] "Islington 023"
#> 
#> [[9]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[9]]$msoa21
#> [1] "Islington 023"
#> 
#> [[9]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[9]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[9]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[9]]$codes$oa21
#> [1] "E00013462"
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
#> [[9]]$distance
#> [1] 59.46237
#> 
#> 
#> [[10]]
#> [[10]]$postcode
#> [1] "EC1Y 8TZ"
#> 
#> [[10]]$quality
#> [1] 1
#> 
#> [[10]]$eastings
#> [1] 532580
#> 
#> [[10]]$northings
#> [1] 182080
#> 
#> [[10]]$country
#> [1] "England"
#> 
#> [[10]]$nhs_ha
#> [1] "London"
#> 
#> [[10]]$longitude
#> [1] -0.090396
#> 
#> [[10]]$latitude
#> [1] 51.52209
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
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa
#> [1] "Islington 023"
#> 
#> [[10]]$incode
#> [1] "8TZ"
#> 
#> [[10]]$outcode
#> [1] "EC1Y"
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
#> [1] "200205"
#> 
#> [[10]]$date_of_termination
#> NULL
#> 
#> [[10]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[10]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa11
#> [1] "Islington 023"
#> 
#> [[10]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[10]]$msoa21
#> [1] "Islington 023"
#> 
#> [[10]]$oa21
#> [1] "E00013428"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[10]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[10]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[10]]$codes$oa21
#> [1] "E00013428"
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
#> [[10]]$distance
#> [1] 59.82949
#> 
#> 
#> [[11]]
#> [[11]]$postcode
#> [1] "EC1Y 8LZ"
#> 
#> [[11]]$quality
#> [1] 1
#> 
#> [[11]]$eastings
#> [1] 532600
#> 
#> [[11]]$northings
#> [1] 182163
#> 
#> [[11]]$country
#> [1] "England"
#> 
#> [[11]]$nhs_ha
#> [1] "London"
#> 
#> [[11]]$longitude
#> [1] -0.090076
#> 
#> [[11]]$latitude
#> [1] 51.52283
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
#> [1] "Islington 023D"
#> 
#> [[11]]$msoa
#> [1] "Islington 023"
#> 
#> [[11]]$incode
#> [1] "8LZ"
#> 
#> [[11]]$outcode
#> [1] "EC1Y"
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
#> [1] "202211"
#> 
#> [[11]]$date_of_termination
#> NULL
#> 
#> [[11]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[11]]$admin_ward
#> [1] "Bunhill"
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
#> [1] "Islington 023D"
#> 
#> [[11]]$msoa11
#> [1] "Islington 023"
#> 
#> [[11]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[11]]$msoa21
#> [1] "Islington 023"
#> 
#> [[11]]$oa21
#> [1] "E00013462"
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
#> [1] "E05013699"
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
#> [1] "E01002704"
#> 
#> [[11]]$codes$msoa
#> [1] "E02000576"
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
#> [1] "E01002704"
#> 
#> [[11]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[11]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[11]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[11]]$codes$oa21
#> [1] "E00013462"
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
#> [[11]]$distance
#> [1] 65.92623
#> 
#> 
#> [[12]]
#> [[12]]$postcode
#> [1] "EC1Y 8TE"
#> 
#> [[12]]$quality
#> [1] 1
#> 
#> [[12]]$eastings
#> [1] 532505
#> 
#> [[12]]$northings
#> [1] 182072
#> 
#> [[12]]$country
#> [1] "England"
#> 
#> [[12]]$nhs_ha
#> [1] "London"
#> 
#> [[12]]$longitude
#> [1] -0.091479
#> 
#> [[12]]$latitude
#> [1] 51.52203
#> 
#> [[12]]$european_electoral_region
#> [1] "London"
#> 
#> [[12]]$primary_care_trust
#> [1] "Islington"
#> 
#> [[12]]$region
#> [1] "London"
#> 
#> [[12]]$lsoa
#> [1] "Islington 023D"
#> 
#> [[12]]$msoa
#> [1] "Islington 023"
#> 
#> [[12]]$incode
#> [1] "8TE"
#> 
#> [[12]]$outcode
#> [1] "EC1Y"
#> 
#> [[12]]$parliamentary_constituency
#> [1] "Islington South and Finsbury"
#> 
#> [[12]]$parliamentary_constituency_2024
#> [1] "Islington South and Finsbury"
#> 
#> [[12]]$senedd_constituency
#> NULL
#> 
#> [[12]]$senedd_constituency_no
#> NULL
#> 
#> [[12]]$admin_district
#> [1] "Islington"
#> 
#> [[12]]$parish
#> [1] "Islington, unparished area"
#> 
#> [[12]]$admin_county
#> NULL
#> 
#> [[12]]$date_of_introduction
#> [1] "198402"
#> 
#> [[12]]$date_of_termination
#> NULL
#> 
#> [[12]]$index_of_multiple_deprivation
#> [1] 12549
#> 
#> [[12]]$admin_ward
#> [1] "Bunhill"
#> 
#> [[12]]$ced
#> NULL
#> 
#> [[12]]$ccg
#> [1] "NHS West and North London"
#> 
#> [[12]]$nuts
#> [1] "Islington"
#> 
#> [[12]]$pfa
#> [1] "Metropolitan Police"
#> 
#> [[12]]$nhs_region
#> [1] "London"
#> 
#> [[12]]$ttwa
#> [1] "London"
#> 
#> [[12]]$national_park
#> [1] "England (non-National Park)"
#> 
#> [[12]]$bua
#> [1] "Islington"
#> 
#> [[12]]$icb
#> [1] "NHS West and North London Integrated Care Board"
#> 
#> [[12]]$cancer_alliance
#> [1] "North Central London"
#> 
#> [[12]]$lsoa11
#> [1] "Islington 023D"
#> 
#> [[12]]$msoa11
#> [1] "Islington 023"
#> 
#> [[12]]$lsoa21
#> [1] "Islington 023D"
#> 
#> [[12]]$msoa21
#> [1] "Islington 023"
#> 
#> [[12]]$oa21
#> [1] "E00013428"
#> 
#> [[12]]$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[12]]$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[12]]$lep1
#> [1] "London"
#> 
#> [[12]]$lep2
#> NULL
#> 
#> [[12]]$codes
#> [[12]]$codes$admin_district
#> [1] "E09000019"
#> 
#> [[12]]$codes$admin_county
#> [1] "E99999999"
#> 
#> [[12]]$codes$admin_ward
#> [1] "E05013699"
#> 
#> [[12]]$codes$parish
#> [1] "E43000209"
#> 
#> [[12]]$codes$parliamentary_constituency
#> [1] "E14001306"
#> 
#> [[12]]$codes$parliamentary_constituency_2024
#> [1] "E14001306"
#> 
#> [[12]]$codes$ccg
#> [1] "E38000240"
#> 
#> [[12]]$codes$ccg_id
#> [1] "93C"
#> 
#> [[12]]$codes$ced
#> [1] "E99999999"
#> 
#> [[12]]$codes$nuts
#> [1] "TLI43"
#> 
#> [[12]]$codes$lsoa
#> [1] "E01002704"
#> 
#> [[12]]$codes$msoa
#> [1] "E02000576"
#> 
#> [[12]]$codes$lau2
#> [1] "E09000019"
#> 
#> [[12]]$codes$pfa
#> [1] "E23000001"
#> 
#> [[12]]$codes$nhs_region
#> [1] "E40000003"
#> 
#> [[12]]$codes$ttwa
#> [1] "E30000234"
#> 
#> [[12]]$codes$national_park
#> [1] "E65000001"
#> 
#> [[12]]$codes$bua
#> [1] "E63011980"
#> 
#> [[12]]$codes$icb
#> [1] "E54000071"
#> 
#> [[12]]$codes$cancer_alliance
#> [1] "E56000027"
#> 
#> [[12]]$codes$lsoa11
#> [1] "E01002704"
#> 
#> [[12]]$codes$msoa11
#> [1] "E02000576"
#> 
#> [[12]]$codes$lsoa21
#> [1] "E01002704"
#> 
#> [[12]]$codes$msoa21
#> [1] "E02000576"
#> 
#> [[12]]$codes$oa21
#> [1] "E00013428"
#> 
#> [[12]]$codes$ruc11
#> [1] "A1"
#> 
#> [[12]]$codes$ruc21
#> [1] "UN1"
#> 
#> [[12]]$codes$lep1
#> [1] "E37000051"
#> 
#> [[12]]$codes$lep2
#> NULL
#> 
#> 
#> [[12]]$distance
#> [1] 68.1493
#> 
#> 
# }
```
