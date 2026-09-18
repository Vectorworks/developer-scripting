# IFC_SetZSGPSetField

## Description
Sets Property Set field value which is attached to Zone, System or Group.

```pascal
FUNCTION IFC_SetZSGPSetField(
				selector       : INTEGER;
				ZSGName        : STRING;
				psetName       : STRING;
				psetField      : STRING;
				psetFieldValue : STRING): BOOLEAN;
```

```python
def vs.IFC_SetZSGPSetField(selector, ZSGName, psetName, psetField, psetFieldValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|ZSGName|STRING|   |
|psetName|STRING|   |
|psetField|STRING|   |
|psetFieldValue|STRING|   |

## Examples
```pascal
resultOK := IFC_SetZSGPSetField(1, 'Example', 'Example', 'MyRecord', 'MyRecord');
```
```python
import vs

# Sets Property Set field value which is attached to Zone, System or Group.
selector = 1
ZSGName = 'Example'
psetName = 'Example'
psetField = 'MyField'
psetFieldValue = 'MyField'

ok = vs.IFC_SetZSGPSetField(selector, ZSGName, psetName, psetField, psetFieldValue)
if ok:
    vs.Message('IFC_SetZSGPSetField succeeded')
else:
    vs.Message('IFC_SetZSGPSetField failed')
```

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
