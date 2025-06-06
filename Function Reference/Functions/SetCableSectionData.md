# SetCableSectionData

## Description
Set cable section data. Data selectors - 'Name', 'Parts Ordered', 'Length', 'Start Slack', 'End Slack', 'Swag', 'Total Vertical Drop'. 'Parts Ordered', 'Length' and 'Total Vertical Drop' are read only. If the function is called on a cable section subpart the section index is ignored. If the function is called on a cable object you have to specify the section index.

```pascal
PROCEDURE SetCableSectionData(
				hObj         : HANDLE;
				DataSelector : STRING;
				SectionIndex : INTEGER;
				Value        : STRING);
```

```python

def vs.SetCableSectionData(hObj, DataSelector, SectionIndex, Value):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObj|HANDLE||
|DataSelector|STRING||
|SectionIndex|INTEGER||
|Value|STRING||

## Version
Availability: from Vectorworks 2025.4

## Category
* [Objects - Cables](../Categories/Objects%20-%20Cables.md)

