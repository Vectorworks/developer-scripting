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

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
