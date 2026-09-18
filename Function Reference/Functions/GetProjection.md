# GetProjection

## Description
Returns the projection index from the specified layer.

```pascal
FUNCTION GetProjection(theyLayer : HANDLE): INTEGER;
```

```python
def vs.GetProjection(theyLayer):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theyLayer|HANDLE|Layer which the projection is returned for.|

## Examples
```pascal
AlertInformDontShowAgain(GetPlugInString(3010),'', FALSE, Options);
PenFore(45000, 45000, 45000);
SetPref(9871, TRUE);
GetOrigin(OriginX,OriginY);
Is3dView := GetProjection(ActLayer)<>6;
RunTempTool(TempToolCallback, TRUE);

{ 3D or plan rotation }
IF (( NOT ( ( GetProjection( GetLayerByName( pluginLayer ) ) ) = 6 ) ) |  GetPref(92)) &  (GetObjectVariableInt(GetLayer(gPluginH), 154) = 1 ) THEN
BEGIN
	Move3DObj( gPluginH, (CenterX - CurX), (CenterY - CurY), -Zval );
END

begin
	LayerHandle:=GetLayer(LNewObj);
	If LayerHandle <> NIL THEN ProjectionI := GetProjection(LayerHandle) ELSE ProjectionI := GetProjection(FActLayer);
	planeRef := GetCurrentPlanarRefID;
	IF (ProjectionI <> 6)  THEN
		SetPlanarRef(LNewObj,kUseLayerPlaneForText)
	else
```
```python
import vs

# Returns the projection index from the specified layer.
theyLayer = vs.ActLayer()  # handle to the active design layer

resultN = vs.GetProjection(theyLayer)
vs.Message('GetProjection returned: ' + str(resultN))
```

## See Also
[ActLayer](ActLayer.md)

## Version
Availability: from VectorWorks 13.0

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
