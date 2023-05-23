# Open Refine Commencement Programs 2015-2022


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
{{if(isBlank(cells['Title'].value), '', '<titleInfo supplied="yes"><title>' + cells["Title"].value + '</title></titleInfo>')}}
<abstract>{{cells["abstract"].value}}</abstract>
{{if(isBlank(cells['date_created_year'].value), '', '<originInfo><dateCreated>' + cells['date_created_year'].value + '</dateCreated><dateCreated encoding="edtf" keyDate="yes">' + cells['date_created_season'].value + '</dateCreated></originInfo>')}}
<physicalDescription><form authority="aat" valueURI="{{cells['form_URI'].value}}">{{cells['form'].value}}</form><extent>{{cells["Extent"].value}}</extent></physicalDescription>
{{if(isBlank(cells['subject1'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject1_URI'].value + '"><topic>' + cells['subject1'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject2'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject2_URI'].value + '"><topic>' + cells['subject2'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject3'].value), '', '<subject authority="lcsh" valueURI="' + cells['subject3_URI'].value + '"><topic>' + cells['subject3'].value + '</topic></subject>')}}
{{if(isBlank(cells['subject4'].value), '', '<subject authority="naf" valueURI="' + cells['subject4_URI'].value + '"><name><namePart>' + cells['subject4'].value + '</namePart></name></subject>')}}
{{if(isBlank(cells['subject5'].value), '', '<subject authority="naf" valueURI="' + cells['subject5_URI'].value + '"><name><namePart>' + cells['subject5'].value + '</namePart></name></subject>')}}
<classification authority="lcc">LD5297 .U55</classification>
<language>
<languageTerm type="text" authority="iso639-2b">English</languageTerm>
</language>
{{if(isBlank(cells['note'].value), '', '<note>' + cells['note'].value + '</note>')}}
<typeOfResource>text</typeOfResource>
<relatedItem displayLabel="Project" type="host"><titleInfo><title>University of Tennessee Commencement Programs</title></titleInfo></relatedItem>
<location><physicalLocation valueURI="http://id.loc.gov/authorities/names/no2014027633">University of Tennessee, Knoxville. Special Collections</physicalLocation></location>
<recordInfo><recordContentSource valueURI="http://id.loc.gov/authorities/names/n87808088">University of Tennessee, Knoxville. Libraries</recordContentSource></recordInfo>
<accessCondition type="use and reproduction" xlink:href="{{cells['rights_URI'].value}}">{{cells['rights'].value}}</accessCondition>
</mods>

```

#### Suffix

```
</modsCollection>
```