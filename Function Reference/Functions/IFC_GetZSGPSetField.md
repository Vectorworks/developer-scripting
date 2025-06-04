# IFC_GetZSGPSetField

## Description
Gets Property Set field value which is attached to Zone, System or Group.

```pascal
FUNCTION IFC_GetZSGPSetField(
				selector              : INTEGER;
				ZSGName               : STRING;
				psetName              : STRING;
				psetField             : STRING;
				VAR outPsetFieldValue : STRING): BOOLEAN;
```

```python
def vs.IFC_GetZSGPSetField(selector, ZSGName, psetName, psetField):
    return (BOOLEAN, outPsetFieldValue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|ZSGName|STRING|   |
|psetName|STRING|   |
|psetField|STRING|   |
|outPsetFieldValue|STRING|   |

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
