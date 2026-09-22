# IFC_DMAddCriteriaMap

## Description
Adds a criteria-based object to the Data Mapping settings.

```pascal
FUNCTION IFC_DMAddCriteriaMap(
				index           : INTEGER;
				critMappingName : STRING;
				criteria        : STRING;
				VAR outErr      : STRING) : BOOLEAN;
```

```python
def vs.IFC_DMAddCriteriaMap(index, critMappingName, criteria):
    return (BOOLEAN, outErr)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER||
|critMappingName|STRING||
|criteria|STRING||
|outErr|STRING||

## Version
Availability: from Vectorworks 2026.2

## Category
* [IFC](Categories/IFC.md)

