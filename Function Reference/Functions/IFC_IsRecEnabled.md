# IFC_IsRecEnabled

## Description
Checks if the mapped Record is enabled.

```pascal
FUNCTION IFC_IsRecEnabled(
				objectName       : STRING;
				recordName       : STRING;
				VAR outIsEnabled : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_IsRecEnabled(objectName, recordName):
    return (BOOLEAN, outIsEnabled)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|recordName|STRING|   |
|outIsEnabled|BOOLEAN|   |

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
