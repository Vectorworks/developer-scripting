# GetStoryLayerInfo

## Description
Returns information on the given story layer template

```pascal
FUNCTION GetStoryLayerInfo(
				index                 : INTEGER;
				VAR name              : STRING;
				VAR scaleFactor       : REAL;
				VAR layerLevelType    : STRING;
				VAR eleveationOffset  : REAL;
				VAR defaultWallHeight : REAL): Boolean;
```

```python
def vs.GetStoryLayerInfo(index):
    return (Boolean, name, scaleFactor, layerLevelType, eleveationOffset, defaultWallHeight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|index|INTEGER|Index of story.|
|name|STRING|Returns with Name of story layer template|
|scaleFactor|REAL|Returns with Scale Factor of story layer template|
|layerLevelType|STRING|Returns with Level Type of story layer template|
|eleveationOffset|REAL|Returns with the Elevation Offset of story layer template|
|defaultWallHeight|REAL|Returns with the Default Wall Height of story layer template|

## Version
Availability: from Vectorworks 2012

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
