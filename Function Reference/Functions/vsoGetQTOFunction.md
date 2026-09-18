# vsoGetQTOFunction

## Description
Get the requested function during event 84 (kParametricGetQTOValue). The function and the option will determine what value needs to be returned during this event by calling vsoSetQTOValue.

```pascal
PROCEDURE vsoGetQTOFunction(
				hObject           : HANDLE;
				VAR functionIndex : INTEGER;
				VAR option        : DYNARRAY[] of CHAR);
```

```python
def vs.vsoGetQTOFunction(hObject):
    return (functionIndex, option)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|   |
|functionIndex|INTEGER|   |
|option|DYNARRAY[] of CHAR|   |

## Examples
```pascal
vsoGetQTOFunction(hObject, 1, option);
```
```python
import vs

# Get the requested function during event 84 (kParametricGetQTOValue).
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

functionIndex, option = vs.vsoGetQTOFunction(hObject)
vs.Message('vsoGetQTOFunction returned: ' + str((functionIndex, option)))
```

## Version
Availability: from Vectorworks 2022

## Category
* [Object Events](../Categories/Object%20Events.md)
