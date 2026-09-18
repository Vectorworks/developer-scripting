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

## Examples
```pascal
resultOK := IFC_GetZSGPSetField(1, 'Example', 'Example', 'MyRecord', 'MyRecord');
```
```python
import vs

# Gets Property Set field value which is attached to Zone, System or Group.
selector = 1
ZSGName = 'Example'
psetName = 'Example'
psetField = 'MyField'

ok, outPsetFieldValue = vs.IFC_GetZSGPSetField(selector, ZSGName, psetName, psetField)
vs.Message('IFC_GetZSGPSetField returned: ' + str((ok, outPsetFieldValue)))
```

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
