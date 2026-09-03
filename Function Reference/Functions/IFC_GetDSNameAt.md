# IFC_GetDSNameAt

## Description
Gets Data Sheets name for object at specified index.

```pascal
FUNCTION IFC_GetDSNameAt(
				objectName           : STRING;
				iDataSheet           : INTEGER;
				VAR outDataSheetName : STRING): BOOLEAN;
```

```python
def vs.IFC_GetDSNameAt(objectName, iDataSheet):
    return (BOOLEAN, outDataSheetName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|iDataSheet|INTEGER|   |
|outDataSheetName|STRING|   |

## Examples
```pascal
resultOK := IFC_GetDSNameAt('Example', 1, 'Example');
```
```python
import vs

# Gets Data Sheets name for object at specified index.
objectName = 'Example'
iDataSheet = 1

ok, outDataSheetName = vs.IFC_GetDSNameAt(objectName, iDataSheet)
vs.Message('IFC_GetDSNameAt returned: ' + str((ok, outDataSheetName)))
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
