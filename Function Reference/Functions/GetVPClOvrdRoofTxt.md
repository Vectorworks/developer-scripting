# GetVPClOvrdRoofTxt

```pascal
PROCEDURE GetVPClOvrdRoofTxt(
				viewportHandle     : HANDLE;
				className          : STRING;
				VAR topMaterial    : LONGINT;
				VAR dormerMaterial : LONGINT);
```

```python
def vs.GetVPClOvrdRoofTxt(viewportHandle, className):
    return (topMaterial, dormerMaterial)
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
GetVPClOvrdRoofTxt(viewportHandle, 'Wall', 1, 2);
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

topMaterial, dormerMaterial = vs.GetVPClOvrdRoofTxt(viewportHandle, className)
vs.Message('GetVPClOvrdRoofTxt returned: ' + str((topMaterial, dormerMaterial)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
