# Bulk postcode lookup

Returns a list of matching postcodes and respective available data.

## Usage

``` r
bulk_postcode_lookup(postcodes)
```

## Arguments

- postcodes:

  Accepts a list of postcodes. Accepts up to 100 postcodes. For only one
  postcode use
  [`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md).

## Value

A list of length one.

## See also

[`postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/postcode_lookup.md)
for documentation.

## Examples

``` r
# \donttest{
pc_list <- list(
postcodes = c("PR3 0SG", "M45 6GN", "EX165BL")) # spaces are ignored
bulk_postcode_lookup(pc_list)
#> [[1]]
#> [[1]]$query
#> [1] "PR30SG"
#> 
#> [[1]]$result
#> [[1]]$result$postcode
#> [1] "PR3 0SG"
#> 
#> [[1]]$result$quality
#> [1] 1
#> 
#> [[1]]$result$eastings
#> [1] 351012
#> 
#> [[1]]$result$northings
#> [1] 440302
#> 
#> [[1]]$result$country
#> [1] "England"
#> 
#> [[1]]$result$nhs_ha
#> [1] "North West"
#> 
#> [[1]]$result$longitude
#> [1] -2.746251
#> 
#> [[1]]$result$latitude
#> [1] 53.85663
#> 
#> [[1]]$result$european_electoral_region
#> [1] "North West"
#> 
#> [[1]]$result$primary_care_trust
#> [1] "North Lancashire Teaching"
#> 
#> [[1]]$result$region
#> [1] "North West"
#> 
#> [[1]]$result$lsoa
#> [1] "Wyre 006A"
#> 
#> [[1]]$result$msoa
#> [1] "Wyre 006"
#> 
#> [[1]]$result$incode
#> [1] "0SG"
#> 
#> [[1]]$result$outcode
#> [1] "PR3"
#> 
#> [[1]]$result$parliamentary_constituency
#> [1] "Lancaster and Wyre"
#> 
#> [[1]]$result$parliamentary_constituency_2024
#> [1] "Lancaster and Wyre"
#> 
#> [[1]]$result$senedd_constituency
#> NULL
#> 
#> [[1]]$result$senedd_constituency_no
#> NULL
#> 
#> [[1]]$result$admin_district
#> [1] "Wyre"
#> 
#> [[1]]$result$parish
#> [1] "Myerscough and Bilsborrow"
#> 
#> [[1]]$result$admin_county
#> [1] "Lancashire"
#> 
#> [[1]]$result$date_of_introduction
#> [1] "200705"
#> 
#> [[1]]$result$date_of_termination
#> NULL
#> 
#> [[1]]$result$index_of_multiple_deprivation
#> [1] 23736
#> 
#> [[1]]$result$admin_ward
#> [1] "Brock with Catterall"
#> 
#> [[1]]$result$ced
#> [1] "Wyre Rural East"
#> 
#> [[1]]$result$ccg
#> [1] "NHS Lancashire and South Cumbria"
#> 
#> [[1]]$result$nuts
#> [1] "Wyre"
#> 
#> [[1]]$result$pfa
#> [1] "Lancashire"
#> 
#> [[1]]$result$nhs_region
#> [1] "North West"
#> 
#> [[1]]$result$ttwa
#> [1] "Preston"
#> 
#> [[1]]$result$national_park
#> [1] "England (non-National Park)"
#> 
#> [[1]]$result$bua
#> [1] "Bilsborrow"
#> 
#> [[1]]$result$icb
#> [1] "NHS Lancashire and South Cumbria Integrated Care Board"
#> 
#> [[1]]$result$cancer_alliance
#> [1] "Lancashire and South Cumbria"
#> 
#> [[1]]$result$lsoa11
#> [1] "Wyre 006A"
#> 
#> [[1]]$result$msoa11
#> [1] "Wyre 006"
#> 
#> [[1]]$result$lsoa21
#> [1] "Wyre 006A"
#> 
#> [[1]]$result$msoa21
#> [1] "Wyre 006"
#> 
#> [[1]]$result$oa21
#> [1] "E00185591"
#> 
#> [[1]]$result$ruc11
#> [1] "(England/Wales) Rural village"
#> 
#> [[1]]$result$ruc21
#> [1] "Smaller rural: Nearer to a major town or city"
#> 
#> [[1]]$result$lep1
#> [1] "Lancashire"
#> 
#> [[1]]$result$lep2
#> NULL
#> 
#> [[1]]$result$codes
#> [[1]]$result$codes$admin_district
#> [1] "E07000128"
#> 
#> [[1]]$result$codes$admin_county
#> [1] "E10000017"
#> 
#> [[1]]$result$codes$admin_ward
#> [1] "E05009934"
#> 
#> [[1]]$result$codes$parish
#> [1] "E04005340"
#> 
#> [[1]]$result$codes$parliamentary_constituency
#> [1] "E14001318"
#> 
#> [[1]]$result$codes$parliamentary_constituency_2024
#> [1] "E14001318"
#> 
#> [[1]]$result$codes$ccg
#> [1] "E38000226"
#> 
#> [[1]]$result$codes$ccg_id
#> [1] "02M"
#> 
#> [[1]]$result$codes$ced
#> [1] "E58000832"
#> 
#> [[1]]$result$codes$nuts
#> [1] "TLD44"
#> 
#> [[1]]$result$codes$lsoa
#> [1] "E01025547"
#> 
#> [[1]]$result$codes$msoa
#> [1] "E02005324"
#> 
#> [[1]]$result$codes$lau2
#> [1] "E07000128"
#> 
#> [[1]]$result$codes$pfa
#> [1] "E23000003"
#> 
#> [[1]]$result$codes$nhs_region
#> [1] "E40000014"
#> 
#> [[1]]$result$codes$ttwa
#> [1] "E30000255"
#> 
#> [[1]]$result$codes$national_park
#> [1] "E65000001"
#> 
#> [[1]]$result$codes$bua
#> [1] "E63007815"
#> 
#> [[1]]$result$codes$icb
#> [1] "E54000048"
#> 
#> [[1]]$result$codes$cancer_alliance
#> [1] "E56000018"
#> 
#> [[1]]$result$codes$lsoa11
#> [1] "E01025547"
#> 
#> [[1]]$result$codes$msoa11
#> [1] "E02005324"
#> 
#> [[1]]$result$codes$lsoa21
#> [1] "E01025547"
#> 
#> [[1]]$result$codes$msoa21
#> [1] "E02005324"
#> 
#> [[1]]$result$codes$oa21
#> [1] "E00185591"
#> 
#> [[1]]$result$codes$ruc11
#> [1] "E1"
#> 
#> [[1]]$result$codes$ruc21
#> [1] "RSN1"
#> 
#> [[1]]$result$codes$lep1
#> [1] "E37000019"
#> 
#> [[1]]$result$codes$lep2
#> NULL
#> 
#> 
#> 
#> 
#> [[2]]
#> [[2]]$query
#> [1] "M456GN"
#> 
#> [[2]]$result
#> [[2]]$result$postcode
#> [1] "M45 6GN"
#> 
#> [[2]]$result$quality
#> [1] 1
#> 
#> [[2]]$result$eastings
#> [1] 380402
#> 
#> [[2]]$result$northings
#> [1] 406021
#> 
#> [[2]]$result$country
#> [1] "England"
#> 
#> [[2]]$result$nhs_ha
#> [1] "North West"
#> 
#> [[2]]$result$longitude
#> [1] -2.297263
#> 
#> [[2]]$result$latitude
#> [1] 53.55047
#> 
#> [[2]]$result$european_electoral_region
#> [1] "North West"
#> 
#> [[2]]$result$primary_care_trust
#> [1] "Bury"
#> 
#> [[2]]$result$region
#> [1] "North West"
#> 
#> [[2]]$result$lsoa
#> [1] "Bury 019C"
#> 
#> [[2]]$result$msoa
#> [1] "Bury 019"
#> 
#> [[2]]$result$incode
#> [1] "6GN"
#> 
#> [[2]]$result$outcode
#> [1] "M45"
#> 
#> [[2]]$result$parliamentary_constituency
#> [1] "Bury South"
#> 
#> [[2]]$result$parliamentary_constituency_2024
#> [1] "Bury South"
#> 
#> [[2]]$result$senedd_constituency
#> NULL
#> 
#> [[2]]$result$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result$admin_district
#> [1] "Bury"
#> 
#> [[2]]$result$parish
#> [1] "Bury, unparished area"
#> 
#> [[2]]$result$admin_county
#> NULL
#> 
#> [[2]]$result$date_of_introduction
#> [1] "199405"
#> 
#> [[2]]$result$date_of_termination
#> NULL
#> 
#> [[2]]$result$index_of_multiple_deprivation
#> [1] 26575
#> 
#> [[2]]$result$admin_ward
#> [1] "Pilkington Park"
#> 
#> [[2]]$result$ced
#> NULL
#> 
#> [[2]]$result$ccg
#> [1] "NHS Greater Manchester"
#> 
#> [[2]]$result$nuts
#> [1] "Bury"
#> 
#> [[2]]$result$pfa
#> [1] "Greater Manchester"
#> 
#> [[2]]$result$nhs_region
#> [1] "North West"
#> 
#> [[2]]$result$ttwa
#> [1] "Manchester"
#> 
#> [[2]]$result$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result$bua
#> [1] "Whitefield"
#> 
#> [[2]]$result$icb
#> [1] "NHS Greater Manchester Integrated Care Board"
#> 
#> [[2]]$result$cancer_alliance
#> [1] "Greater Manchester"
#> 
#> [[2]]$result$lsoa11
#> [1] "Bury 019C"
#> 
#> [[2]]$result$msoa11
#> [1] "Bury 019"
#> 
#> [[2]]$result$lsoa21
#> [1] "Bury 019C"
#> 
#> [[2]]$result$msoa21
#> [1] "Bury 019"
#> 
#> [[2]]$result$oa21
#> [1] "E00025239"
#> 
#> [[2]]$result$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[2]]$result$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[2]]$result$lep1
#> [1] "Greater Manchester"
#> 
#> [[2]]$result$lep2
#> NULL
#> 
#> [[2]]$result$codes
#> [[2]]$result$codes$admin_district
#> [1] "E08000002"
#> 
#> [[2]]$result$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result$codes$admin_ward
#> [1] "E05014159"
#> 
#> [[2]]$result$codes$parish
#> [1] "E43000156"
#> 
#> [[2]]$result$codes$parliamentary_constituency
#> [1] "E14001145"
#> 
#> [[2]]$result$codes$parliamentary_constituency_2024
#> [1] "E14001145"
#> 
#> [[2]]$result$codes$ccg
#> [1] "E38000024"
#> 
#> [[2]]$result$codes$ccg_id
#> [1] "00V"
#> 
#> [[2]]$result$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result$codes$nuts
#> [1] "TLD37"
#> 
#> [[2]]$result$codes$lsoa
#> [1] "E01004989"
#> 
#> [[2]]$result$codes$msoa
#> [1] "E02001037"
#> 
#> [[2]]$result$codes$lau2
#> [1] "E08000002"
#> 
#> [[2]]$result$codes$pfa
#> [1] "E23000005"
#> 
#> [[2]]$result$codes$nhs_region
#> [1] "E40000014"
#> 
#> [[2]]$result$codes$ttwa
#> [1] "E30000239"
#> 
#> [[2]]$result$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result$codes$bua
#> [1] "E63008275"
#> 
#> [[2]]$result$codes$icb
#> [1] "E54000057"
#> 
#> [[2]]$result$codes$cancer_alliance
#> [1] "E56000032"
#> 
#> [[2]]$result$codes$lsoa11
#> [1] "E01004989"
#> 
#> [[2]]$result$codes$msoa11
#> [1] "E02001037"
#> 
#> [[2]]$result$codes$lsoa21
#> [1] "E01004989"
#> 
#> [[2]]$result$codes$msoa21
#> [1] "E02001037"
#> 
#> [[2]]$result$codes$oa21
#> [1] "E00025239"
#> 
#> [[2]]$result$codes$ruc11
#> [1] "A1"
#> 
#> [[2]]$result$codes$ruc21
#> [1] "UN1"
#> 
#> [[2]]$result$codes$lep1
#> [1] "E37000015"
#> 
#> [[2]]$result$codes$lep2
#> NULL
#> 
#> 
#> 
#> 
#> [[3]]
#> [[3]]$query
#> [1] "EX165BL"
#> 
#> [[3]]$result
#> [[3]]$result$postcode
#> [1] "EX16 5BL"
#> 
#> [[3]]$result$quality
#> [1] 1
#> 
#> [[3]]$result$eastings
#> [1] 294478
#> 
#> [[3]]$result$northings
#> [1] 112252
#> 
#> [[3]]$result$country
#> [1] "England"
#> 
#> [[3]]$result$nhs_ha
#> [1] "South West"
#> 
#> [[3]]$result$longitude
#> [1] -3.50197
#> 
#> [[3]]$result$latitude
#> [1] 50.90006
#> 
#> [[3]]$result$european_electoral_region
#> [1] "South West"
#> 
#> [[3]]$result$primary_care_trust
#> [1] "Devon"
#> 
#> [[3]]$result$region
#> [1] "South West"
#> 
#> [[3]]$result$lsoa
#> [1] "Mid Devon 005C"
#> 
#> [[3]]$result$msoa
#> [1] "Mid Devon 005"
#> 
#> [[3]]$result$incode
#> [1] "5BL"
#> 
#> [[3]]$result$outcode
#> [1] "EX16"
#> 
#> [[3]]$result$parliamentary_constituency
#> [1] "Tiverton and Minehead"
#> 
#> [[3]]$result$parliamentary_constituency_2024
#> [1] "Tiverton and Minehead"
#> 
#> [[3]]$result$senedd_constituency
#> NULL
#> 
#> [[3]]$result$senedd_constituency_no
#> NULL
#> 
#> [[3]]$result$admin_district
#> [1] "Mid Devon"
#> 
#> [[3]]$result$parish
#> [1] "Tiverton"
#> 
#> [[3]]$result$admin_county
#> [1] "Devon"
#> 
#> [[3]]$result$date_of_introduction
#> [1] "198001"
#> 
#> [[3]]$result$date_of_termination
#> NULL
#> 
#> [[3]]$result$index_of_multiple_deprivation
#> [1] 7072
#> 
#> [[3]]$result$admin_ward
#> [1] "Tiverton Westexe"
#> 
#> [[3]]$result$ced
#> [1] "Tiverton West"
#> 
#> [[3]]$result$ccg
#> [1] "NHS Devon"
#> 
#> [[3]]$result$nuts
#> [1] "Mid Devon"
#> 
#> [[3]]$result$pfa
#> [1] "Devon & Cornwall"
#> 
#> [[3]]$result$nhs_region
#> [1] "South West"
#> 
#> [[3]]$result$ttwa
#> [1] "Exeter"
#> 
#> [[3]]$result$national_park
#> [1] "England (non-National Park)"
#> 
#> [[3]]$result$bua
#> [1] "Tiverton (Mid Devon)"
#> 
#> [[3]]$result$icb
#> [1] "NHS Devon Integrated Care Board"
#> 
#> [[3]]$result$cancer_alliance
#> [1] "Peninsula"
#> 
#> [[3]]$result$lsoa11
#> [1] "Mid Devon 005C"
#> 
#> [[3]]$result$msoa11
#> [1] "Mid Devon 005"
#> 
#> [[3]]$result$lsoa21
#> [1] "Mid Devon 005C"
#> 
#> [[3]]$result$msoa21
#> [1] "Mid Devon 005"
#> 
#> [[3]]$result$oa21
#> [1] "E00101678"
#> 
#> [[3]]$result$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[3]]$result$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[3]]$result$lep1
#> [1] "Heart of the South West"
#> 
#> [[3]]$result$lep2
#> NULL
#> 
#> [[3]]$result$codes
#> [[3]]$result$codes$admin_district
#> [1] "E07000042"
#> 
#> [[3]]$result$codes$admin_county
#> [1] "E10000008"
#> 
#> [[3]]$result$codes$admin_ward
#> [1] "E05014813"
#> 
#> [[3]]$result$codes$parish
#> [1] "E04003055"
#> 
#> [[3]]$result$codes$parliamentary_constituency
#> [1] "E14001548"
#> 
#> [[3]]$result$codes$parliamentary_constituency_2024
#> [1] "E14001548"
#> 
#> [[3]]$result$codes$ccg
#> [1] "E38000230"
#> 
#> [[3]]$result$codes$ccg_id
#> [1] "15N"
#> 
#> [[3]]$result$codes$ced
#> [1] "E58000304"
#> 
#> [[3]]$result$codes$nuts
#> [1] "TLK43"
#> 
#> [[3]]$result$codes$lsoa
#> [1] "E01020079"
#> 
#> [[3]]$result$codes$msoa
#> [1] "E02004168"
#> 
#> [[3]]$result$codes$lau2
#> [1] "E07000042"
#> 
#> [[3]]$result$codes$pfa
#> [1] "E23000035"
#> 
#> [[3]]$result$codes$nhs_region
#> [1] "E40000006"
#> 
#> [[3]]$result$codes$ttwa
#> [1] "E30000206"
#> 
#> [[3]]$result$codes$national_park
#> [1] "E65000001"
#> 
#> [[3]]$result$codes$bua
#> [1] "E63013547"
#> 
#> [[3]]$result$codes$icb
#> [1] "E54000037"
#> 
#> [[3]]$result$codes$cancer_alliance
#> [1] "E56000014"
#> 
#> [[3]]$result$codes$lsoa11
#> [1] "E01020079"
#> 
#> [[3]]$result$codes$msoa11
#> [1] "E02004168"
#> 
#> [[3]]$result$codes$lsoa21
#> [1] "E01020079"
#> 
#> [[3]]$result$codes$msoa21
#> [1] "E02004168"
#> 
#> [[3]]$result$codes$oa21
#> [1] "E00101678"
#> 
#> [[3]]$result$codes$ruc11
#> [1] "C1"
#> 
#> [[3]]$result$codes$ruc21
#> [1] "UN1"
#> 
#> [[3]]$result$codes$lep1
#> [1] "E37000016"
#> 
#> [[3]]$result$codes$lep2
#> NULL
#> 
#> 
#> 
#> 
# The function needs a list of length one. This won't work:
bulk_postcode_lookup(list("PR3 0SG", "M45 6GN", "EX165BL"))
#> [[1]]
#> [[1]]$query
#> [1] "PR30SG"
#> 
#> [[1]]$result
#> [[1]]$result$postcode
#> [1] "PR3 0SG"
#> 
#> [[1]]$result$quality
#> [1] 1
#> 
#> [[1]]$result$eastings
#> [1] 351012
#> 
#> [[1]]$result$northings
#> [1] 440302
#> 
#> [[1]]$result$country
#> [1] "England"
#> 
#> [[1]]$result$nhs_ha
#> [1] "North West"
#> 
#> [[1]]$result$longitude
#> [1] -2.746251
#> 
#> [[1]]$result$latitude
#> [1] 53.85663
#> 
#> [[1]]$result$european_electoral_region
#> [1] "North West"
#> 
#> [[1]]$result$primary_care_trust
#> [1] "North Lancashire Teaching"
#> 
#> [[1]]$result$region
#> [1] "North West"
#> 
#> [[1]]$result$lsoa
#> [1] "Wyre 006A"
#> 
#> [[1]]$result$msoa
#> [1] "Wyre 006"
#> 
#> [[1]]$result$incode
#> [1] "0SG"
#> 
#> [[1]]$result$outcode
#> [1] "PR3"
#> 
#> [[1]]$result$parliamentary_constituency
#> [1] "Lancaster and Wyre"
#> 
#> [[1]]$result$parliamentary_constituency_2024
#> [1] "Lancaster and Wyre"
#> 
#> [[1]]$result$senedd_constituency
#> NULL
#> 
#> [[1]]$result$senedd_constituency_no
#> NULL
#> 
#> [[1]]$result$admin_district
#> [1] "Wyre"
#> 
#> [[1]]$result$parish
#> [1] "Myerscough and Bilsborrow"
#> 
#> [[1]]$result$admin_county
#> [1] "Lancashire"
#> 
#> [[1]]$result$date_of_introduction
#> [1] "200705"
#> 
#> [[1]]$result$date_of_termination
#> NULL
#> 
#> [[1]]$result$index_of_multiple_deprivation
#> [1] 23736
#> 
#> [[1]]$result$admin_ward
#> [1] "Brock with Catterall"
#> 
#> [[1]]$result$ced
#> [1] "Wyre Rural East"
#> 
#> [[1]]$result$ccg
#> [1] "NHS Lancashire and South Cumbria"
#> 
#> [[1]]$result$nuts
#> [1] "Wyre"
#> 
#> [[1]]$result$pfa
#> [1] "Lancashire"
#> 
#> [[1]]$result$nhs_region
#> [1] "North West"
#> 
#> [[1]]$result$ttwa
#> [1] "Preston"
#> 
#> [[1]]$result$national_park
#> [1] "England (non-National Park)"
#> 
#> [[1]]$result$bua
#> [1] "Bilsborrow"
#> 
#> [[1]]$result$icb
#> [1] "NHS Lancashire and South Cumbria Integrated Care Board"
#> 
#> [[1]]$result$cancer_alliance
#> [1] "Lancashire and South Cumbria"
#> 
#> [[1]]$result$lsoa11
#> [1] "Wyre 006A"
#> 
#> [[1]]$result$msoa11
#> [1] "Wyre 006"
#> 
#> [[1]]$result$lsoa21
#> [1] "Wyre 006A"
#> 
#> [[1]]$result$msoa21
#> [1] "Wyre 006"
#> 
#> [[1]]$result$oa21
#> [1] "E00185591"
#> 
#> [[1]]$result$ruc11
#> [1] "(England/Wales) Rural village"
#> 
#> [[1]]$result$ruc21
#> [1] "Smaller rural: Nearer to a major town or city"
#> 
#> [[1]]$result$lep1
#> [1] "Lancashire"
#> 
#> [[1]]$result$lep2
#> NULL
#> 
#> [[1]]$result$codes
#> [[1]]$result$codes$admin_district
#> [1] "E07000128"
#> 
#> [[1]]$result$codes$admin_county
#> [1] "E10000017"
#> 
#> [[1]]$result$codes$admin_ward
#> [1] "E05009934"
#> 
#> [[1]]$result$codes$parish
#> [1] "E04005340"
#> 
#> [[1]]$result$codes$parliamentary_constituency
#> [1] "E14001318"
#> 
#> [[1]]$result$codes$parliamentary_constituency_2024
#> [1] "E14001318"
#> 
#> [[1]]$result$codes$ccg
#> [1] "E38000226"
#> 
#> [[1]]$result$codes$ccg_id
#> [1] "02M"
#> 
#> [[1]]$result$codes$ced
#> [1] "E58000832"
#> 
#> [[1]]$result$codes$nuts
#> [1] "TLD44"
#> 
#> [[1]]$result$codes$lsoa
#> [1] "E01025547"
#> 
#> [[1]]$result$codes$msoa
#> [1] "E02005324"
#> 
#> [[1]]$result$codes$lau2
#> [1] "E07000128"
#> 
#> [[1]]$result$codes$pfa
#> [1] "E23000003"
#> 
#> [[1]]$result$codes$nhs_region
#> [1] "E40000014"
#> 
#> [[1]]$result$codes$ttwa
#> [1] "E30000255"
#> 
#> [[1]]$result$codes$national_park
#> [1] "E65000001"
#> 
#> [[1]]$result$codes$bua
#> [1] "E63007815"
#> 
#> [[1]]$result$codes$icb
#> [1] "E54000048"
#> 
#> [[1]]$result$codes$cancer_alliance
#> [1] "E56000018"
#> 
#> [[1]]$result$codes$lsoa11
#> [1] "E01025547"
#> 
#> [[1]]$result$codes$msoa11
#> [1] "E02005324"
#> 
#> [[1]]$result$codes$lsoa21
#> [1] "E01025547"
#> 
#> [[1]]$result$codes$msoa21
#> [1] "E02005324"
#> 
#> [[1]]$result$codes$oa21
#> [1] "E00185591"
#> 
#> [[1]]$result$codes$ruc11
#> [1] "E1"
#> 
#> [[1]]$result$codes$ruc21
#> [1] "RSN1"
#> 
#> [[1]]$result$codes$lep1
#> [1] "E37000019"
#> 
#> [[1]]$result$codes$lep2
#> NULL
#> 
#> 
#> 
#> 
#> [[2]]
#> [[2]]$query
#> [1] "M456GN"
#> 
#> [[2]]$result
#> [[2]]$result$postcode
#> [1] "M45 6GN"
#> 
#> [[2]]$result$quality
#> [1] 1
#> 
#> [[2]]$result$eastings
#> [1] 380402
#> 
#> [[2]]$result$northings
#> [1] 406021
#> 
#> [[2]]$result$country
#> [1] "England"
#> 
#> [[2]]$result$nhs_ha
#> [1] "North West"
#> 
#> [[2]]$result$longitude
#> [1] -2.297263
#> 
#> [[2]]$result$latitude
#> [1] 53.55047
#> 
#> [[2]]$result$european_electoral_region
#> [1] "North West"
#> 
#> [[2]]$result$primary_care_trust
#> [1] "Bury"
#> 
#> [[2]]$result$region
#> [1] "North West"
#> 
#> [[2]]$result$lsoa
#> [1] "Bury 019C"
#> 
#> [[2]]$result$msoa
#> [1] "Bury 019"
#> 
#> [[2]]$result$incode
#> [1] "6GN"
#> 
#> [[2]]$result$outcode
#> [1] "M45"
#> 
#> [[2]]$result$parliamentary_constituency
#> [1] "Bury South"
#> 
#> [[2]]$result$parliamentary_constituency_2024
#> [1] "Bury South"
#> 
#> [[2]]$result$senedd_constituency
#> NULL
#> 
#> [[2]]$result$senedd_constituency_no
#> NULL
#> 
#> [[2]]$result$admin_district
#> [1] "Bury"
#> 
#> [[2]]$result$parish
#> [1] "Bury, unparished area"
#> 
#> [[2]]$result$admin_county
#> NULL
#> 
#> [[2]]$result$date_of_introduction
#> [1] "199405"
#> 
#> [[2]]$result$date_of_termination
#> NULL
#> 
#> [[2]]$result$index_of_multiple_deprivation
#> [1] 26575
#> 
#> [[2]]$result$admin_ward
#> [1] "Pilkington Park"
#> 
#> [[2]]$result$ced
#> NULL
#> 
#> [[2]]$result$ccg
#> [1] "NHS Greater Manchester"
#> 
#> [[2]]$result$nuts
#> [1] "Bury"
#> 
#> [[2]]$result$pfa
#> [1] "Greater Manchester"
#> 
#> [[2]]$result$nhs_region
#> [1] "North West"
#> 
#> [[2]]$result$ttwa
#> [1] "Manchester"
#> 
#> [[2]]$result$national_park
#> [1] "England (non-National Park)"
#> 
#> [[2]]$result$bua
#> [1] "Whitefield"
#> 
#> [[2]]$result$icb
#> [1] "NHS Greater Manchester Integrated Care Board"
#> 
#> [[2]]$result$cancer_alliance
#> [1] "Greater Manchester"
#> 
#> [[2]]$result$lsoa11
#> [1] "Bury 019C"
#> 
#> [[2]]$result$msoa11
#> [1] "Bury 019"
#> 
#> [[2]]$result$lsoa21
#> [1] "Bury 019C"
#> 
#> [[2]]$result$msoa21
#> [1] "Bury 019"
#> 
#> [[2]]$result$oa21
#> [1] "E00025239"
#> 
#> [[2]]$result$ruc11
#> [1] "(England/Wales) Urban major conurbation"
#> 
#> [[2]]$result$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[2]]$result$lep1
#> [1] "Greater Manchester"
#> 
#> [[2]]$result$lep2
#> NULL
#> 
#> [[2]]$result$codes
#> [[2]]$result$codes$admin_district
#> [1] "E08000002"
#> 
#> [[2]]$result$codes$admin_county
#> [1] "E99999999"
#> 
#> [[2]]$result$codes$admin_ward
#> [1] "E05014159"
#> 
#> [[2]]$result$codes$parish
#> [1] "E43000156"
#> 
#> [[2]]$result$codes$parliamentary_constituency
#> [1] "E14001145"
#> 
#> [[2]]$result$codes$parliamentary_constituency_2024
#> [1] "E14001145"
#> 
#> [[2]]$result$codes$ccg
#> [1] "E38000024"
#> 
#> [[2]]$result$codes$ccg_id
#> [1] "00V"
#> 
#> [[2]]$result$codes$ced
#> [1] "E99999999"
#> 
#> [[2]]$result$codes$nuts
#> [1] "TLD37"
#> 
#> [[2]]$result$codes$lsoa
#> [1] "E01004989"
#> 
#> [[2]]$result$codes$msoa
#> [1] "E02001037"
#> 
#> [[2]]$result$codes$lau2
#> [1] "E08000002"
#> 
#> [[2]]$result$codes$pfa
#> [1] "E23000005"
#> 
#> [[2]]$result$codes$nhs_region
#> [1] "E40000014"
#> 
#> [[2]]$result$codes$ttwa
#> [1] "E30000239"
#> 
#> [[2]]$result$codes$national_park
#> [1] "E65000001"
#> 
#> [[2]]$result$codes$bua
#> [1] "E63008275"
#> 
#> [[2]]$result$codes$icb
#> [1] "E54000057"
#> 
#> [[2]]$result$codes$cancer_alliance
#> [1] "E56000032"
#> 
#> [[2]]$result$codes$lsoa11
#> [1] "E01004989"
#> 
#> [[2]]$result$codes$msoa11
#> [1] "E02001037"
#> 
#> [[2]]$result$codes$lsoa21
#> [1] "E01004989"
#> 
#> [[2]]$result$codes$msoa21
#> [1] "E02001037"
#> 
#> [[2]]$result$codes$oa21
#> [1] "E00025239"
#> 
#> [[2]]$result$codes$ruc11
#> [1] "A1"
#> 
#> [[2]]$result$codes$ruc21
#> [1] "UN1"
#> 
#> [[2]]$result$codes$lep1
#> [1] "E37000015"
#> 
#> [[2]]$result$codes$lep2
#> NULL
#> 
#> 
#> 
#> 
#> [[3]]
#> [[3]]$query
#> [1] "EX165BL"
#> 
#> [[3]]$result
#> [[3]]$result$postcode
#> [1] "EX16 5BL"
#> 
#> [[3]]$result$quality
#> [1] 1
#> 
#> [[3]]$result$eastings
#> [1] 294478
#> 
#> [[3]]$result$northings
#> [1] 112252
#> 
#> [[3]]$result$country
#> [1] "England"
#> 
#> [[3]]$result$nhs_ha
#> [1] "South West"
#> 
#> [[3]]$result$longitude
#> [1] -3.50197
#> 
#> [[3]]$result$latitude
#> [1] 50.90006
#> 
#> [[3]]$result$european_electoral_region
#> [1] "South West"
#> 
#> [[3]]$result$primary_care_trust
#> [1] "Devon"
#> 
#> [[3]]$result$region
#> [1] "South West"
#> 
#> [[3]]$result$lsoa
#> [1] "Mid Devon 005C"
#> 
#> [[3]]$result$msoa
#> [1] "Mid Devon 005"
#> 
#> [[3]]$result$incode
#> [1] "5BL"
#> 
#> [[3]]$result$outcode
#> [1] "EX16"
#> 
#> [[3]]$result$parliamentary_constituency
#> [1] "Tiverton and Minehead"
#> 
#> [[3]]$result$parliamentary_constituency_2024
#> [1] "Tiverton and Minehead"
#> 
#> [[3]]$result$senedd_constituency
#> NULL
#> 
#> [[3]]$result$senedd_constituency_no
#> NULL
#> 
#> [[3]]$result$admin_district
#> [1] "Mid Devon"
#> 
#> [[3]]$result$parish
#> [1] "Tiverton"
#> 
#> [[3]]$result$admin_county
#> [1] "Devon"
#> 
#> [[3]]$result$date_of_introduction
#> [1] "198001"
#> 
#> [[3]]$result$date_of_termination
#> NULL
#> 
#> [[3]]$result$index_of_multiple_deprivation
#> [1] 7072
#> 
#> [[3]]$result$admin_ward
#> [1] "Tiverton Westexe"
#> 
#> [[3]]$result$ced
#> [1] "Tiverton West"
#> 
#> [[3]]$result$ccg
#> [1] "NHS Devon"
#> 
#> [[3]]$result$nuts
#> [1] "Mid Devon"
#> 
#> [[3]]$result$pfa
#> [1] "Devon & Cornwall"
#> 
#> [[3]]$result$nhs_region
#> [1] "South West"
#> 
#> [[3]]$result$ttwa
#> [1] "Exeter"
#> 
#> [[3]]$result$national_park
#> [1] "England (non-National Park)"
#> 
#> [[3]]$result$bua
#> [1] "Tiverton (Mid Devon)"
#> 
#> [[3]]$result$icb
#> [1] "NHS Devon Integrated Care Board"
#> 
#> [[3]]$result$cancer_alliance
#> [1] "Peninsula"
#> 
#> [[3]]$result$lsoa11
#> [1] "Mid Devon 005C"
#> 
#> [[3]]$result$msoa11
#> [1] "Mid Devon 005"
#> 
#> [[3]]$result$lsoa21
#> [1] "Mid Devon 005C"
#> 
#> [[3]]$result$msoa21
#> [1] "Mid Devon 005"
#> 
#> [[3]]$result$oa21
#> [1] "E00101678"
#> 
#> [[3]]$result$ruc11
#> [1] "(England/Wales) Urban city and town"
#> 
#> [[3]]$result$ruc21
#> [1] "Urban: Nearer to a major town or city"
#> 
#> [[3]]$result$lep1
#> [1] "Heart of the South West"
#> 
#> [[3]]$result$lep2
#> NULL
#> 
#> [[3]]$result$codes
#> [[3]]$result$codes$admin_district
#> [1] "E07000042"
#> 
#> [[3]]$result$codes$admin_county
#> [1] "E10000008"
#> 
#> [[3]]$result$codes$admin_ward
#> [1] "E05014813"
#> 
#> [[3]]$result$codes$parish
#> [1] "E04003055"
#> 
#> [[3]]$result$codes$parliamentary_constituency
#> [1] "E14001548"
#> 
#> [[3]]$result$codes$parliamentary_constituency_2024
#> [1] "E14001548"
#> 
#> [[3]]$result$codes$ccg
#> [1] "E38000230"
#> 
#> [[3]]$result$codes$ccg_id
#> [1] "15N"
#> 
#> [[3]]$result$codes$ced
#> [1] "E58000304"
#> 
#> [[3]]$result$codes$nuts
#> [1] "TLK43"
#> 
#> [[3]]$result$codes$lsoa
#> [1] "E01020079"
#> 
#> [[3]]$result$codes$msoa
#> [1] "E02004168"
#> 
#> [[3]]$result$codes$lau2
#> [1] "E07000042"
#> 
#> [[3]]$result$codes$pfa
#> [1] "E23000035"
#> 
#> [[3]]$result$codes$nhs_region
#> [1] "E40000006"
#> 
#> [[3]]$result$codes$ttwa
#> [1] "E30000206"
#> 
#> [[3]]$result$codes$national_park
#> [1] "E65000001"
#> 
#> [[3]]$result$codes$bua
#> [1] "E63013547"
#> 
#> [[3]]$result$codes$icb
#> [1] "E54000037"
#> 
#> [[3]]$result$codes$cancer_alliance
#> [1] "E56000014"
#> 
#> [[3]]$result$codes$lsoa11
#> [1] "E01020079"
#> 
#> [[3]]$result$codes$msoa11
#> [1] "E02004168"
#> 
#> [[3]]$result$codes$lsoa21
#> [1] "E01020079"
#> 
#> [[3]]$result$codes$msoa21
#> [1] "E02004168"
#> 
#> [[3]]$result$codes$oa21
#> [1] "E00101678"
#> 
#> [[3]]$result$codes$ruc11
#> [1] "C1"
#> 
#> [[3]]$result$codes$ruc21
#> [1] "UN1"
#> 
#> [[3]]$result$codes$lep1
#> [1] "E37000016"
#> 
#> [[3]]$result$codes$lep2
#> NULL
#> 
#> 
#> 
#> 
# }
```
