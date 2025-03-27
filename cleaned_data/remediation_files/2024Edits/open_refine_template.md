# Open Refine Template Beauford Delaney Sketchbooks (2024 Edits - combined book/page)


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="pid">{{cells['PID'].value}}</identifier>
<identifier type="local">{{cells['Corrected Comp.UNIQID'].value}}</identifier>

{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}} 

<name valueURI="http://id.loc.gov/authorities/names/n85364216"><namePart>Delaney, Beauford, 1901-1979</namePart><role><roleTerm authority="marcrelator" valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm></role></name>

{{if(isBlank(cells['date'].value), '', '<originInfo><dateCreated>' + cells['date'].value + '</dateCreated>') + if(isBlank(cells['date_year'].value), '', '<dateCreated encoding="edtf">' + cells['date_year'].value + '</dateCreated>') + if(isBlank(cells['date_start'].value), '', '<dateCreated encoding="edtf" point="start">' + cells['date_start'].value + '</dateCreated><dateCreated encoding="edtf" point="end">' + cells['date_end'].value + '</dateCreated>') + '</originInfo>'}}

<abstract>{{cells['Description'].value}}</abstract>

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells['Size'].value}}</extent>
</physicalDescription>

{{if(isBlank(cells['subject'].value), '', '<subject valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject2'].value), '', '<subject valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject3'].value), '', '<subject valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject4'].value), '', '<subject valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject5'].value), '', '<subject valueURI="' + cells['subject5_URI'].value + '"><topic>' + cells['subject5'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject_geo'].value), '', '<subject valueURI="' + cells['subject_geo_URI'].value + '"><geographic>' + cells['subject_geo'].value + '</geographic></subject>')}}

{{if(isBlank(cells['subject_geo2'].value), '', '<subject valueURI="' + cells['subject_geo2_URI'].value + '"><geographic>' + cells['subject_geo2'].value + '</geographic></subject>')}}

<relatedItem displayLabel="Project" type="host"><titleInfo><title>Beauford Delaney Sketchbooks and Notebooks</title></titleInfo></relatedItem>

<relatedItem displayLabel="Collection" type="host"><titleInfo>
<title>Beauford Delaney Sketchbooks and Notebooks</title></titleInfo><identifier>MS-3967</identifier></relatedItem>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation><shelfLocator>{{cells['shelfLocator'].value}}</shelfLocator></location>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="http://rightsstatements.org/vocab/InC/1.0/">In Copyright</accessCondition>

</mods>

```

#### Suffix

```
</modsCollection>
```