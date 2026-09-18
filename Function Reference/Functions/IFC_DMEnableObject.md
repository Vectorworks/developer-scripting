# IFC_DMEnableObject

## Description
Enables/Disables the indicated object from current IFC Data Mapping.

```pascal
FUNCTION IFC_DMEnableObject(
				inStrObjName : STRING;
				bEnable      : BOOLEAN): BOOLEAN;
```

```python
def vs.IFC_DMEnableObject(inStrObjName, bEnable):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStrObjName|STRING|   |
|bEnable|BOOLEAN|   |

## Examples
```pascal
resultOK := IFC_DMEnableObject('Example', TRUE);
```
```python
import vs

# Enables/Disables the indicated object from current IFC Data Mapping.
inStrObjName = 'Example'
bEnable = True

ok = vs.IFC_DMEnableObject(inStrObjName, bEnable)
if ok:
    vs.Message('IFC_DMEnableObject succeeded')
else:
    vs.Message('IFC_DMEnableObject failed')
```

## Version
Available from: Vectorworks 2017

## Category
* [IFC](../Categories/IFC.md)
