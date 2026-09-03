# SetVPClOvrdRoofTxt

```pascal
PROCEDURE SetVPClOvrdRoofTxt(
				viewportHandle : HANDLE;
				className      : STRING;
				topMaterial    : LONGINT;
				dormerMaterial : LONGINT);
```

```python
def vs.SetVPClOvrdRoofTxt(viewportHandle, className, topMaterial, dormerMaterial):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle|
|className|STRING|The name of the class override|
|topMaterial|LONGINT|The material of the top|
|dormerMaterial|LONGINT|The material of the dormer|

## Examples
```pascal
SetVPClOvrdRoofTxt(viewportHandle, 'Wall', 1, 2);
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
topMaterial = 1
dormerMaterial = 2

vs.SetVPClOvrdRoofTxt(viewportHandle, className, topMaterial, dormerMaterial)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
