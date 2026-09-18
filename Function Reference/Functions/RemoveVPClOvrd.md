# RemoveVPClOvrd

## Description
Removes a class override from the specified viewport.

```pascal
PROCEDURE RemoveVPClOvrd(
				viewportHandle : HANDLE;
				className      : STRING);
```

```python
def vs.RemoveVPClOvrd(viewportHandle, className):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|The name of the class.|

## Examples
```pascal
RemoveVPClOvrd(viewportHandle, 'Wall');
```
```python
import vs

# Removes a class override from the specified viewport.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

vs.RemoveVPClOvrd(viewportHandle, className)
```

## See Also
VS Functions:
[CreateVPClOvrd](CreateVPClOvrd.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
