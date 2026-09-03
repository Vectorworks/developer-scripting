# IFC_SetDSFieldVis

## Description
Sets Data Sheet field visibility.

```pascal
FUNCTION IFC_SetDSFieldVis(
				objectName    : STRING;
				dataSheetName : STRING;
				fieldLabel    : STRING;
				isVisible     : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_SetDSFieldVis(objectName, dataSheetName, fieldLabel, isVisible):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|dataSheetName|STRING|   |
|fieldLabel|STRING|   |
|isVisible|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_SetDSFieldVis('Example', 'Example', 'MyRecord', TRUE);
```
```python
import vs

# Sets Data Sheet field visibility.
objectName = 'Example'
dataSheetName = 'Example'
fieldLabel = 'MyField'
isVisible = True

ok = vs.IFC_SetDSFieldVis(objectName, dataSheetName, fieldLabel, isVisible)
if ok:
    vs.Message('IFC_SetDSFieldVis succeeded')
else:
    vs.Message('IFC_SetDSFieldVis failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
