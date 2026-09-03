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

## Examples
```pascal
resultOK := IFC_IsRecEnabled('Example', 'MyRecord', TRUE);
```
```python
import vs

# Checks if the mapped Record is enabled.
objectName = 'Example'
recordName = 'MyRecord'

ok, outIsEnabled = vs.IFC_IsRecEnabled(objectName, recordName)
vs.Message('IFC_IsRecEnabled returned: ' + str((ok, outIsEnabled)))
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
