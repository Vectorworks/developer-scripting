# IFC_SetIFCEntity2

## Description
Sets IFC entity type and its default Psets and values from IFC Data Mapping.

```pascal
FUNCTION IFC_SetIFCEntity2(
				hObject      : HANDLE;
				inStrIfcType : STRING): BOOLEAN;
```

```python
def vs.IFC_SetIFCEntity2(hObject, inStrIfcType):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|inStrIfcType|STRING|   |

## Examples
```pascal
resultOK := IFC_SetIFCEntity2(hObject, 'Example');
```
```python
import vs

# Sets IFC entity type and its default Psets and values from IFC Data Mapping.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
inStrIfcType = 'Example'

ok = vs.IFC_SetIFCEntity2(hObject, inStrIfcType)
if ok:
    vs.Message('IFC_SetIFCEntity2 succeeded')
else:
    vs.Message('IFC_SetIFCEntity2 failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
