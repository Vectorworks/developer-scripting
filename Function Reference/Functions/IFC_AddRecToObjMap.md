# IFC_AddRecToObjMap

## Description
Adds Record to the mapping for an Object.

```pascal
FUNCTION IFC_AddRecToObjMap(
				objectName : STRING;
				recordName : STRING;
				condition  : STRING;
				bEnable    : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_AddRecToObjMap(objectName, recordName, condition, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectName|STRING|   |
|recordName|STRING|   |
|condition|STRING|   |
|bEnable|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_AddRecToObjMap('Example', 'MyRecord', 'Example', TRUE);
```
```python
import vs

# Adds Record to the mapping for an Object.
objectName = 'Example'
recordName = 'MyRecord'
condition = 'Example'
bEnable = True

ok = vs.IFC_AddRecToObjMap(objectName, recordName, condition, bEnable)
if ok:
    vs.Message('IFC_AddRecToObjMap succeeded')
else:
    vs.Message('IFC_AddRecToObjMap failed')
```

## Version
Availability: from Vectorworks 2023.4

## Category
* [IFC](../Categories/IFC.md)
