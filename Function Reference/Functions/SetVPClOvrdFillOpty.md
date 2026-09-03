# SetVPClOvrdFillOpty

## Description
Sets the fill opacity for a viewport class override.

```pascal
PROCEDURE SetVPClOvrdFillOpty(
				viewportHandle : HANDLE;
				className      : STRING;
				fillOpacity    : INTEGER);
```

```python
def vs.SetVPClOvrdFillOpty(viewportHandle, className, fillOpacity):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|className|STRING|Name of the class.|
|fillOpacity|INTEGER|The fill opacity as a percentage (0-100).|

## Examples
```pascal
SetVPClOvrdFillOpty(viewportHandle, 'Wall', 1);
```
```python
import vs

# Sets the fill opacity for a viewport class override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
fillOpacity = 1

vs.SetVPClOvrdFillOpty(viewportHandle, className, fillOpacity)
```

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
