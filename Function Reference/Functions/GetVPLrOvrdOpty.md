# GetVPLrOvrdOpty

## Description
Gets the opacity for a layer override.

```pascal
FUNCTION GetVPLrOvrdOpty(
				viewportHandle : HANDLE;
				layerHandle    : HANDLE): INTEGER;
```

```python
def vs.GetVPLrOvrdOpty(viewportHandle, layerHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|viewportHandle|HANDLE|The viewport handle.|
|layerHandle|HANDLE|The layer handle.|

## Examples
```pascal
resultN := GetVPLrOvrdOpty(viewportHandle, layerHandle);
```
```python
import vs

# Gets the opacity for a layer override.
viewportHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
layerHandle = vs.ActLayer()  # handle to the active design layer

resultN = vs.GetVPLrOvrdOpty(viewportHandle, layerHandle)
vs.Message('GetVPLrOvrdOpty returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetVPLrOvrdOpty](SetVPLrOvrdOpty.md)

## Version
Availability: from Vectorworks 2014

## Category
* [Viewports](../Categories/Viewports.md)
