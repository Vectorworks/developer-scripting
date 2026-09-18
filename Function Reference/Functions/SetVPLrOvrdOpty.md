# SetVPLrOvrdOpty

## Description
Sets the opacity for a layer override.

```pascal
PROCEDURE SetVPLrOvrdOpty(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE;
				opacity        : INTEGER);
```

```python
def vs.SetVPLrOvrdOpty(viewportHandle, layerHandle, opacity):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|layerHandle|HANDLE|The layer handle.|
|opacity|INTEGER|Opacity (0-100)|

## Examples
```pascal
SetVPLrOvrdOpty(viewportHandle, layerHandle, 1);
```
```python
import vs

# Sets the opacity for a layer override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer
opacity = 1

vs.SetVPLrOvrdOpty(viewportHandle, layerHandle, opacity)
```

## See Also
VS Functions:
[GetVPLrOvrdOpty](GetVPLrOvrdOpty.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
