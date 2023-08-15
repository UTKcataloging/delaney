# Open Refine Template Beauford Delaney Sketchbooks (book level)


## Template

#### Prefix

```
<?xml version="1.0" encoding="UTF-8"?>
<modsCollection xmlns="http://www.loc.gov/mods/v3" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xlink="http://www.w3.org/1999/xlink" xsi:schemaLocation="http://www.loc.gov/mods/v3 http://www.loc.gov/standards/mods/v3/mods-3-5.xsd">
```
####Body

```
<mods>
<identifier type="local">{{cells["Identifier"].value}}</identifier>

{{if(isBlank(cells['title'].value), '', '<titleInfo><title>' + cells["title"].value + '</title></titleInfo>')}} 

{{if(isBlank(cells['creator'].value), '', '<name valueURI="' + cells['creator_URI'].value + '"><namePart>' + cells['creator'].value + '</namePart><role><roleTerm valueURI="http://id.loc.gov/vocabulary/relators/cre">Creator</roleTerm></role></name>')}}

{{if(isBlank(cells['Year (circa)'].value), '', '<originInfo><dateCreated>' + cells['Year (circa)'].value + '</dateCreated>') + if(isBlank(cells['year_edtf'].value), '', '<dateCreated encoding="edtf">' + cells['year_edtf'].value + '</dateCreated>') + if(isBlank(cells['start_date'].value), '', '<dateCreated encoding="edtf" point="start">' + cells['start_date'].value + '</dateCreated><dateCreated encoding="edtf" point="end">' + cells['end_date'].value + '</dateCreated>') + '</originInfo>'}}

<abstract>{{cells['Content Description'].value}}</abstract>

{{if(isBlank(cells['Physical Description'].value), '', '<note>' + cells['Physical Description'].value + '</note>')}}

{{if(isBlank(cells['Media/Detail'].value), '', '<note>' + cells['Media/Detail'].value + '</note>')}}

<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form>
</physicalDescription>

{{if(isBlank(cells['subject'].value), '', '<subject valueURI="' + cells['subject_URI'].value + '"><topic>' + cells['subject'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject2'].value), '', '<subject valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject3'].value), '', '<subject valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}

{{if(isBlank(cells['subject4'].value), '', '<subject valueURI="' + cells['subject4_URI'].value + '"><topic>' + cells['subject4'].value + '</topic></subject>')}}

<relatedItem displayLabel="Project" type="host"><titleInfo><title>Beauford Delaney Sketchbooks and Notebooks</title></titleInfo></relatedItem>

<relatedItem displayLabel="Collection" type="host"><titleInfo>
<title>Beauford Delaney Sketchbooks and Notebooks</title></titleInfo><identifier>MS-3967</identifier></relatedItem>

<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>

<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>

<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```