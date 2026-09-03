# SetVPClOvrdFillStyle

```pascal
PROCEDURE SetVPClOvrdFillStyle(
				viewportHandle : HANDLE;
				className      : STRING;
				fillStyle      : LONGINT);
```

```python
def vs.SetVPClOvrdFillStyle(viewportHandle, className, fillStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle|
|className|STRING|The name of the class|
|fillStyle|LONGINT|The fill style to be set|

## Examples
```pascal
SetVPClOvrdFillStyle(viewportHandle, 'Wall', 1);
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
fillStyle = 0

vs.SetVPClOvrdFillStyle(viewportHandle, className, fillStyle)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
