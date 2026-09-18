# SetVPClOvrdPenOpty

## Description
Sets the pen opacity for a class override.

```pascal
PROCEDURE SetVPClOvrdPenOpty(
				viewportHandle : HANDLE;
				className      : STRING;
				penOpacity     : INTEGER);
```

```python
def vs.SetVPClOvrdPenOpty(viewportHandle, className, penOpacity):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|Name of the class.|
|penOpacity|INTEGER|The pen opacity as a percentage (0-100).|

## Examples
```pascal
SetVPClOvrdPenOpty(viewportHandle, 'Wall', 1);
```
```python
import vs

# Sets the pen opacity for a class override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
penOpacity = 1

vs.SetVPClOvrdPenOpty(viewportHandle, className, penOpacity)
```

## See Also
VS Functions:
[GetVPClOvrdPenOpty](GetVPClOvrdPenOpty.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
