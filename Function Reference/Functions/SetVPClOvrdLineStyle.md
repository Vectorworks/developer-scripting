# SetVPClOvrdLineStyle

```pascal
PROCEDURE SetVPClOvrdLineStyle(
				viewportHandle : HANDLE;
				className      : STRING;
				lineStyle      : LONGINT);
```

```python
def vs.SetVPClOvrdLineStyle(viewportHandle, className, lineStyle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The handle of the viewport.|
|className|STRING|The name of the class|
|lineStyle|LONGINT|The line style to be set to the class override|

## Examples
```pascal
SetVPClOvrdLineStyle(viewportHandle, 'Wall', 1);
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
lineStyle = 0

vs.SetVPClOvrdLineStyle(viewportHandle, className, lineStyle)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
