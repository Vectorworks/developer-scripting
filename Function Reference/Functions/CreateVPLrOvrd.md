# CreateVPLrOvrd

## Description
Creates a new layer override, initially set to the layer's current properties.

```pascal
PROCEDURE CreateVPLrOvrd(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE);
```

```python
def vs.CreateVPLrOvrd(viewportHandle, layerHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|layerHandle|HANDLE|The layer to override.|

## Examples
```pascal
CreateVPLrOvrd(viewportHandle, layerHandle);
```
```python
import vs

# Creates a new layer override, initially set to the layer's current properties.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer

vs.CreateVPLrOvrd(viewportHandle, layerHandle)
newObj = vs.LNewObj()  # handle to the newly created object
```

## See Also
VS Functions:
[RemoveVPLrOvrd](RemoveVPLrOvrd.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
