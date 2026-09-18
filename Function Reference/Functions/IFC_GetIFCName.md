# IFC_GetIFCName

## Description
Returns the Object's IfcName of attached record or Mapped IfcEntity from IFC Data Mapping.

```pascal
FUNCTION IFC_GetIFCName(
				hObject           : HANDLE;
				VAR outStrIfcName : STRING): BOOLEAN;
```

```python
def vs.IFC_GetIFCName(hObject):
    return (BOOLEAN, outStrIfcName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|outStrIfcName|STRING|   |

## Examples
```pascal
resultOK := IFC_GetIFCName(hObject, 'Example');
```
```python
import vs

# Returns the Object's IfcName of attached record or Mapped IfcEntity from
# IFC Data Mapping.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, outStrIfcName = vs.IFC_GetIFCName(hObject)
vs.Message('IFC_GetIFCName returned: ' + str((ok, outStrIfcName)))
```

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
