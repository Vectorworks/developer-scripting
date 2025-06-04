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

## Version
Availability: from Vectorworks 2021

## Category
* [IFC](../Categories/IFC.md)
