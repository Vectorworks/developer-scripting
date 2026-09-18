# IFC_SetRecEnabled

## Description
Enables/disables the mapped Record.

```pascal
FUNCTION IFC_SetRecEnabled(
				objectName : STRING;
				recordName : STRING;
				bEnable    : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_SetRecEnabled(objectName, recordName, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|recordName|STRING|   |
|bEnable|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_SetRecEnabled('Example', 'MyRecord', TRUE);
```
```python
import vs

# Enables/disables the mapped Record.
objectName = 'Example'
recordName = 'MyRecord'
bEnable = True

ok = vs.IFC_SetRecEnabled(objectName, recordName, bEnable)
if ok:
    vs.Message('IFC_SetRecEnabled succeeded')
else:
    vs.Message('IFC_SetRecEnabled failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
