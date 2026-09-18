# SetVPClOvrdWallTxt

```pascal
PROCEDURE SetVPClOvrdWallTxt(
				viewportHandle : HANDLE;
				className      : STRING;
				leftTexture    : LONGINT;
				centerTexture  : LONGINT;
				rightTexture   : LONGINT);
```

```python
def vs.SetVPClOvrdWallTxt(viewportHandle, className, leftTexture, centerTexture, rightTexture):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The handle of the viewport|
|className|STRING|The name of the class override|
|leftTexture|LONGINT|The left side texture to be set|
|centerTexture|LONGINT|Thecenter texture to be set|
|rightTexture|LONGINT|The right side texture to be set|

## Examples
```pascal
SetVPClOvrdWallTxt(viewportHandle, 'Wall', 1, 2, 3);
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
leftTexture = 1
centerTexture = 2
rightTexture = 3

vs.SetVPClOvrdWallTxt(viewportHandle, className, leftTexture, centerTexture, rightTexture)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
