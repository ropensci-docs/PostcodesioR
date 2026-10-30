# Postcode lookup

Lookup a postcode.

## Usage

``` r
postcode_lookup(postcode)
```

## Arguments

- postcode:

  A string. One valid UK postcode. This function is case- and
  space-insensitive. For more than one postcode use
  [`bulk_postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/bulk_postcode_lookup.md).
  For Scottish postcodes use
  [`scottish_postcode_lookup`](https://docs.ropensci.org/PostcodesioR/reference/scottish_postcode_lookup.md).

## Value

A data frame. Returns all available data if found. Returns NAs if
postcode does not exist (404).

- `postcode` Postcode. All current ('live') postcodes within the United
  Kingdom, the Channel Islands and the Isle of Man, received monthly
  from Royal Mail. 2, 3 or 4-character outward code, single space and
  3-character inward code.

- `quality` Positional Quality. Shows the status of the assigned grid
  reference.

  - 1 - within the building of the matched address closest to the
    postcode mean

  - 2 - as for status value 1, except by visual inspection of Landline
    maps (Scotland only)

  - 3 - approximate to within 50m

  - 4 - postcode unit mean (mean of matched addresses with the same
    postcode, but not snapped to a building)

  - 5 - imputed by ONS, by reference to surrounding postcode grid
    references

  - 6 - postcode sector mean, (mainly PO Boxes)

  - 8 - postcode terminated prior to Gridlink(R) initiative, last known
    ONS postcode grid reference1

  - 9 - no grid reference available

- `eastings` Eastings. The Ordnance Survey postcode grid reference
  Easting to 1 metre resolution; blank for postcodes in the Channel
  Islands and the Isle of Man. Grid references for postcodes in Northern
  Ireland relate to the Irish Grid system.

- `northings` Northings. The Ordnance Survey postcode grid reference
  Easting to 1 metre resolution; blank for postcodes in the Channel
  Islands and the Isle of Man. Grid references for postcodes in Northern
  Ireland relate to the Irish Grid system.

- `country` Country. The country (i.e. one of the four constituent
  countries of the United Kingdom or the Channel Islands or the Isle of
  Man) to which each postcode is assigned.

- `nhs_ha` Strategic Health Authority. The health area code for the
  postcode.

- `longitude` Longitude. The WGS84 longitude given the Postcode's
  national grid reference.

- `latitude` Latitude. The WGS84 latitude given the Postcode's national
  grid reference.

- `european_electoral_region` European Electoral Region (EER). The
  European Electoral Region code for each postcode.

- `primary_care_trust` Primary Care Trust (PCT). The code for the
  Primary Care areas in England, LHBs in Wales, CHPs in Scotland, LCG in
  Northern Ireland and PHD in the Isle of Man; there are no equivalent
  areas in the Channel Islands. Care Trust/ Care Trust Plus (CT) / local
  health board (LHB) / community health partnership (CHP) / local
  commissioning group (LCG) / primary healthcare directorate (PHD).

- `region` Region (formerly GOR). The Region code for each postcode. The
  nine GORs were abolished on 1 April 2011 and are now known as
  'Regions'. They were the primary statistical subdivisions of England
  and also the areas in which the Government Offices for the Regions
  fulfilled their role. Each GOR covered a number of local authorities.

- `lsoa` 2011 Census lower layer super output area (LSOA). The 2011
  Census lower layer SOA code for England and Wales, SOA code for
  Northern Ireland and data zone code for Scotland.

- `msoa` 2011 Census middle layer super output area (MSOA). The 2011
  Census middle layer SOA (MSOA) code for England and Wales and
  intermediate zone for Scotland.

- `incode` Incode. 3-character inward code that is following the space
  in the full postcode.

- `outcode` Outcode. 2, 3 or 4-character outward code. The part of
  postcode before the space.

- `parliamentary_constituency` Westminster Parliamentary Constituency.
  The Westminster Parliamentary Constituency code for each postcode.

- `admin_district` District. The current district/unitary authority to
  which the postcode has been assigned.

- `parish` Parish (England)/ community (Wales). The smallest type of
  administrative area in England is the parish (also known as 'civil
  parish'); the equivalent units in Wales are communities.

- `admin_county` County. The current county to which the postcode has
  been assigned.

- `admin_ward` Ward. The current administrative/electoral area to which
  the postcode has been assigned.

- `ccg` Clinical Commissioning Group. Clinical commissioning groups
  (CCGs) are NHS organisations set up by the Health and Social Care Act
  2012 to organise the delivery of NHS services in England.

- `nuts` Nomenclature of Units for Territorial Statistics (NUTS) / Local
  Administrative Units (LAU) areas. The LAU2 code for each postcode.
  NUTS is a hierarchical classification of spatial units that provides a
  breakdown of the European Union's territory for producing regional
  statistics which are comparable across the Union. The NUTS area
  classification in the United Kingdom comprises current national
  administrative and electoral areas, except in Scotland where some NUTS
  areas comprise whole and/or part Local Enterprise Regions. NUTS levels
  1-3 are frozen for a minimum of three years and NUTS levels 4 and 5
  are now Local Administrative Units (LAU) levels 1 and 2 respectively.

- `_code` Returns an ID or Code associated with the postcode. Typically
  these are a 9 character code known as an ONS Code or GSS Code. This is
  currently only available for districts, parishes, counties, CCGs, NUTS
  and wards.

See <https://postcodes.io/docs> for more details.

## Examples

``` r
# \donttest{
postcode_lookup("EC1Y8LX")
#>   postcode quality eastings northings country nhs_ha longitude latitude
#> 1 EC1Y 8LX       1   532544    182128 England London -0.090896 51.52253
#>   european_electoral_region primary_care_trust region           lsoa
#> 1                    London          Islington London Islington 023D
#>            msoa incode outcode   parliamentary_constituency
#> 1 Islington 023    8LX    EC1Y Islington South and Finsbury
#>   parliamentary_constituency_2024 senedd_constituency senedd_constituency_no
#> 1    Islington South and Finsbury                  NA                     NA
#>   admin_district                     parish admin_county date_of_introduction
#> 1      Islington Islington, unparished area           NA               198001
#>   date_of_termination index_of_multiple_deprivation admin_ward ced
#> 1                  NA                         12549    Bunhill  NA
#>                         ccg      nuts                 pfa nhs_region   ttwa
#> 1 NHS West and North London Islington Metropolitan Police     London London
#>                 national_park       bua
#> 1 England (non-National Park) Islington
#>                                               icb      cancer_alliance
#> 1 NHS West and North London Integrated Care Board North Central London
#>           lsoa11        msoa11         lsoa21        msoa21      oa21
#> 1 Islington 023D Islington 023 Islington 023D Islington 023 E00013429
#>                                     ruc11                                 ruc21
#> 1 (England/Wales) Urban major conurbation Urban: Nearer to a major town or city
#>     lep1 lep2 admin_district_code admin_county_code admin_ward_code parish_code
#> 1 London   NA           E09000019         E99999999       E05013699   E43000209
#>   parliamentary_constituency_code parliamentary_constituency_2024_code
#> 1                       E14001306                            E14001306
#>    ccg_code ccg_id_code  ced_code nuts_code lsoa_code msoa_code lau2_code
#> 1 E38000240         93C E99999999     TLI43 E01002704 E02000576 E09000019
#>    pfa_code nhs_region_code ttwa_code national_park_code  bua_code  icb_code
#> 1 E23000001       E40000003 E30000234          E65000001 E63011980 E54000071
#>   cancer_alliance_code lsoa11_code msoa11_code lsoa21_code msoa21_code
#> 1            E56000027   E01002704   E02000576   E01002704   E02000576
#>   oa21_code ruc11_code ruc21_code lep1_code
#> 1 E00013429         A1        UN1 E37000051
postcode_lookup("EC1Y 8LX") # spaces are ignored
#>   postcode quality eastings northings country nhs_ha longitude latitude
#> 1 EC1Y 8LX       1   532544    182128 England London -0.090896 51.52253
#>   european_electoral_region primary_care_trust region           lsoa
#> 1                    London          Islington London Islington 023D
#>            msoa incode outcode   parliamentary_constituency
#> 1 Islington 023    8LX    EC1Y Islington South and Finsbury
#>   parliamentary_constituency_2024 senedd_constituency senedd_constituency_no
#> 1    Islington South and Finsbury                  NA                     NA
#>   admin_district                     parish admin_county date_of_introduction
#> 1      Islington Islington, unparished area           NA               198001
#>   date_of_termination index_of_multiple_deprivation admin_ward ced
#> 1                  NA                         12549    Bunhill  NA
#>                         ccg      nuts                 pfa nhs_region   ttwa
#> 1 NHS West and North London Islington Metropolitan Police     London London
#>                 national_park       bua
#> 1 England (non-National Park) Islington
#>                                               icb      cancer_alliance
#> 1 NHS West and North London Integrated Care Board North Central London
#>           lsoa11        msoa11         lsoa21        msoa21      oa21
#> 1 Islington 023D Islington 023 Islington 023D Islington 023 E00013429
#>                                     ruc11                                 ruc21
#> 1 (England/Wales) Urban major conurbation Urban: Nearer to a major town or city
#>     lep1 lep2 admin_district_code admin_county_code admin_ward_code parish_code
#> 1 London   NA           E09000019         E99999999       E05013699   E43000209
#>   parliamentary_constituency_code parliamentary_constituency_2024_code
#> 1                       E14001306                            E14001306
#>    ccg_code ccg_id_code  ced_code nuts_code lsoa_code msoa_code lau2_code
#> 1 E38000240         93C E99999999     TLI43 E01002704 E02000576 E09000019
#>    pfa_code nhs_region_code ttwa_code national_park_code  bua_code  icb_code
#> 1 E23000001       E40000003 E30000234          E65000001 E63011980 E54000071
#>   cancer_alliance_code lsoa11_code msoa11_code lsoa21_code msoa21_code
#> 1            E56000027   E01002704   E02000576   E01002704   E02000576
#>   oa21_code ruc11_code ruc21_code lep1_code
#> 1 E00013429         A1        UN1 E37000051
postcode_lookup("DE3 5LF") # terminated postcode returns NAs
#> Warning: Not Found (HTTP 404).
#> [1] "Postcode DE3%205LF is incorrect or expired."
#>    postcode quality eastings northings country nhs_ha longitude latitude
#> 1 DE3%205LF      NA       NA        NA      NA     NA        NA       NA
#>   european_electoral_region primary_care_trust region lsoa msoa incode outcode
#> 1                        NA                 NA     NA   NA   NA     NA      NA
#>   parliamentary_constituency admin_district parish admin_county admin_ward ced
#> 1                         NA             NA     NA           NA         NA  NA
#>   ccg nuts admin_district_code admin_county_code admin_ward_code parish_code
#> 1  NA   NA                  NA                NA              NA          NA
#>   parliamentary_constituency_code ccg_code ccg_id_code ced_code nuts_code
#> 1                              NA       NA          NA       NA        NA
#>   lsoa_code msoa_code lau2_code
#> 1        NA        NA        NA
# }
```
