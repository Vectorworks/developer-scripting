# IFC_AttachPSetToZSG

## Description
Attaches Property Set to Zone, System or Group.

```pascal
FUNCTION IFC_AttachPSetToZSG(
				selector : INTEGER;
				ZSGName  : STRING;
				psetName : STRING): BOOLEAN;
```

```python
def vs.IFC_AttachPSetToZSG(selector, ZSGName, psetName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|selector|INTEGER|   |
|ZSGName|STRING|   |
|psetName|STRING|   |

## Examples
```pascal
resultOK := IFC_AttachPSetToZSG(1, 'Example', 'Example');
```
```python
import vs

# Attaches Property Set to Zone, System or Group.
selector = 1
ZSGName = 'Example'
psetName = 'Example'

ok = vs.IFC_AttachPSetToZSG(selector, ZSGName, psetName)
if ok:
    vs.Message('IFC_AttachPSetToZSG succeeded')
else:
    vs.Message('IFC_AttachPSetToZSG failed')
```

## Version
Availability: from Vectorworks 2022.1

## Category
* [IFC](../Categories/IFC.md)
