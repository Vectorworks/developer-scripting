# IFC_GetDSFieldInfoAt

## Description
Gets label, visibility state, by formula state for Data Sheet field.

```pascal
FUNCTION IFC_GetDSFieldInfoAt(
				objectName         : STRING;
				dataSheetName      : STRING;
				iField             : INTEGER;
				VAR outFieldLabel  : STRING;
				VAR outIsVisible   : BOOLEAN;
				VAR outIsByFormula : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_GetDSFieldInfoAt(objectName, dataSheetName, iField):
    return (BOOLEAN, outFieldLabel, outIsVisible, outIsByFormula)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|dataSheetName|STRING|   |
|iField|INTEGER|   |
|outFieldLabel|STRING|   |
|outIsVisible|BOOLEAN|   |
|outIsByFormula|BOOLEAN|   |

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
