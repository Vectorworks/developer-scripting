# SetVPClOvrdLnWeight

```pascal
PROCEDURE SetVPClOvrdLnWeight(
				viewportHandle : HANDLE;
				className      : STRING;
				LineWeight     : INTEGER);
```

```python
def vs.SetVPClOvrdLnWeight(viewportHandle, className, LineWeight):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle|
|className|STRING|The name of the class override|
|LineWeight|INTEGER|The lineWeight to be set|

## Examples
```pascal
SetVPClOvrdLnWeight(viewportHandle, 'Wall', 1);
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
LineWeight = 1

vs.SetVPClOvrdLnWeight(viewportHandle, className, LineWeight)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
