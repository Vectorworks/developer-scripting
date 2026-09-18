# IFC_GetIFCEntity2

## Description
Gets the IFC entity type for an object by IFC record and IFC Data Mapping plus the type of the IFC record

```pascal
FUNCTION IFC_GetIFCEntity2(
				hObject           : HANDLE;
				VAR outType       : INTEGER;
				VAR outStrNameRec : STRING;
				VAR outStrNameMap : STRING): BOOLEAN;
```

```python
def vs.IFC_GetIFCEntity2(hObject):
    return (BOOLEAN, outType, outStrNameRec, outStrNameMap)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|outType|INTEGER|   |
|outStrNameRec|STRING|   |
|outStrNameMap|STRING|   |

## Examples
```pascal
resultOK := IFC_GetIFCEntity2(hObject, 1, 'Example', 'Example');
```
```python
import vs

# Gets the IFC entity type for an object by IFC record and IFC Data Mapping
# plus the type of the IFC record.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

ok, outType, outStrNameRec, outStrNameMap = vs.IFC_GetIFCEntity2(hObject)
vs.Message('IFC_GetIFCEntity2 returned: ' + str((ok, outType, outStrNameRec, outStrNameMap)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
