# CreateVPClOvrd

## Description
Creates a new override for the specified class in the specified viewport. The override is initially populated with the class's current properties.

```pascal
PROCEDURE CreateVPClOvrd(
				viewportHandle : HANDLE;
				className      : STRING);
```

```python
def vs.CreateVPClOvrd(viewportHandle, className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|The name of the class.|

## Examples
```pascal
CreateVPClOvrd(viewportHandle, 'Wall');
```
```python
import vs

# Creates a new override for the specified class in the specified viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

vs.CreateVPClOvrd(viewportHandle, className)
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[RemoveVPClOvrd](RemoveVPClOvrd.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
