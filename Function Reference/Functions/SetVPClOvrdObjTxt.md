# SetVPClOvrdObjTxt

```pascal
PROCEDURE SetVPClOvrdObjTxt(
				viewportHandle : HANDLE;
				className      : STRING;
				objectTexture  : INTEGER);
```

```python
def vs.SetVPClOvrdObjTxt(viewportHandle, className, objectTexture):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle|
|className|STRING|The name of the class override|
|objectTexture|INTEGER|The object texture to be set|

## Examples
```pascal
SetVPClOvrdObjTxt(viewportHandle, 'Wall', 1);
```
```python
import vs

viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
className = 'None'
objectTexture = 1

vs.SetVPClOvrdObjTxt(viewportHandle, className, objectTexture)
```

## Version
Availability: from Vectorworks 2018

## Category
* [Viewports](../Categories/Viewports.md)
