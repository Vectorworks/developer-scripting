# IFC_SetProperty

## Description
Sets the specified property value.

```pascal
FUNCTION IFC_SetProperty(
				hObject      : HANDLE;
				pSetName     : STRING;
				propertyName : STRING;
				propValue    : STRING): BOOLEAN;
```

```python
def vs.IFC_SetProperty(hObject, pSetName, propertyName, propValue):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|pSetName|STRING|   |
|propertyName|STRING|   |
|propValue|STRING|   |

## Examples
```pascal
resultOK := IFC_SetProperty(hObject, 'Example', 'Example', 'Example');
```
```python
import vs

# Sets the specified property value.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
pSetName = 'Example'
propertyName = 'Example'
propValue = 'Example'

ok = vs.IFC_SetProperty(hObject, pSetName, propertyName, propValue)
if ok:
    vs.Message('IFC_SetProperty succeeded')
else:
    vs.Message('IFC_SetProperty failed')
```

## Version
Availability: from Vectorworks 2018

## Category
* [IFC](../Categories/IFC.md)
