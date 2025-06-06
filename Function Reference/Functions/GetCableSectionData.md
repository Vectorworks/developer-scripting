# GetCableSectionData

## Description
Get cable section data. Data selectors - 'Name', 'Parts Ordered', 'Length', 'Start Slack', 'End Slack', 'Swag', 'Total Vertical Drop'. 'Parts Ordered', 'Length' and 'Total Vertical Drop' are read only. If the function is called on a cable section subpart the section index is ignored. If the function is called on a cable object you have to specify the section index. Optionally, for 'Parts Ordered' you can specify part index which to display, or 0 to ignore this argument.

```pascal
FUNCTION GetCableSectionData(
				hObj         : HANDLE;
				DataSelector : STRING;
				SectionIndex : INTEGER;
				PartIndex    : INTEGER) : STRING;
```

```python

def vs.GetCableSectionData(hObj, DataSelector, SectionIndex, PartIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE||
|DataSelector|STRING||
|SectionIndex|INTEGER||
|PartIndex|INTEGER||

## Version
Availability: from Vectorworks 2025.4

## Category
* [Objects - Cables](../Categories/Objects%20-%20Cables.md)

