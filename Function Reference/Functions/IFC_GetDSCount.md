# IFC_GetDSCount

## Description
Gets Data Sheets count for object.

```pascal
FUNCTION IFC_GetDSCount(
				objectName     : STRING;
				VAR outDSCount : INTEGER): BOOLEAN;
```

```python
def vs.IFC_GetDSCount(objectName):
    return (BOOLEAN, outDSCount)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|outDSCount|INTEGER|   |

## Examples
```pascal
resultOK := IFC_GetDSCount('Example', 1);
```
```python
import vs

# Gets Data Sheets count for object.
objectName = 'Example'

ok, outDSCount = vs.IFC_GetDSCount(objectName)
vs.Message('IFC_GetDSCount returned: ' + str((ok, outDSCount)))
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
