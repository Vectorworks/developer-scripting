# IFC_GetDSFieldsCount

## Description
Gets Data Sheet's fields count.

```pascal
FUNCTION IFC_GetDSFieldsCount(
				objectName         : STRING;
				dataSheetName      : STRING;
				VAR outFieldsCount : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetDSFieldsCount(objectName, dataSheetName):
    return (BOOLEAN, outFieldsCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|dataSheetName|STRING|   |
|outFieldsCount|INTEGER|   |

## Examples
```pascal
resultOK := IFC_GetDSFieldsCount('Example', 'Example', 1);
```
```python
import vs

# Gets Data Sheet's fields count.
objectName = 'Example'
dataSheetName = 'Example'

ok, outFieldsCount = vs.IFC_GetDSFieldsCount(objectName, dataSheetName)
vs.Message('IFC_GetDSFieldsCount returned: ' + str((ok, outFieldsCount)))
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
