# SetGISLayer

## Description
Set layer context.

```pascal
FUNCTION SetGISLayer(hLayer : HANDLE): BOOLEAN;
```

```python
def vs.SetGISLayer(hLayer):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|   |

## Examples
```pascal
{set georef data}
if IsGeoreferenced( ActLayer ) then begin
	isOK	:= SetGISLayer( ActLayer );
	if isOK then begin
		gPageNorthStr	:= Num2StrF( GetAngleToNorth );

if IsGeoreferenced( layerH ) then BEGIN
	isOK	:= SetGISLayer( layerH );
	IF isOK THEN
		BEGIN
```
```python
import vs

# Set layer context.
hLayer = vs.ActLayer()  # handle to the active design layer

ok = vs.SetGISLayer(hLayer)
if ok:
    vs.Message('SetGISLayer succeeded')
else:
    vs.Message('SetGISLayer failed')
```

## Version
Availability: from Vectorworks 2012

## Category
* [GIS](../Categories/GIS.md)
