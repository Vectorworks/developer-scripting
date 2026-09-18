# GetVPClOvrdWallTxt

```pascal
PROCEDURE GetVPClOvrdWallTxt(
				viewportHandle    : HANDLE;
				className         : STRING;
				VAR leftTexture   : LONGINT;
				VAR centerTexture : LONGINT;
				VAR rightTexture  : LONGINT);
```

```python
def vs.GetVPClOvrdWallTxt(viewportHandle, className):
    return (leftTexture, centerTexture, rightTexture)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle|
|className|STRING|The name of the class override|
|leftTexture|LONGINT|The material of the left side|
|centerTexture|LONGINT|The material of the center|
|rightTexture|LONGINT|The material of the right side|

## Examples
```pascal
GetVPClOvrdWallTxt(viewportHandle, 'Wall', 1, 2, 3);
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'

leftTexture, centerTexture, rightTexture = vs.GetVPClOvrdWallTxt(viewportHandle, className)
vs.Message('GetVPClOvrdWallTxt returned: ' + str((leftTexture, centerTexture, rightTexture)))
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
