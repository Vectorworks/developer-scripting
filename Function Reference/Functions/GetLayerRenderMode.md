# GetLayerRenderMode

## Description
Returns the render mode for the referenced layer.

**Table - Render Modes**

| Render Mode                   | Constant |
|-------------------------------|----------|
| Wireframe                     | 0        |
| Unshaded Polygon              | 2        |
| Shaded Polygon                | 3        |
| Shaded Polygon No Lines       | 4        |
| Final Shaded Polygon          | 5        |
| Hidden Line                   | 6        |
| Dashed Hidden Line            | 7        |
| OpenGL                        | 11       |
| Fast RenderWorks              | 12       |
| Fast RenderWorks with Shadows | 13       |
| Final Quality Renderworks     | 14       |
| Custom Renderworks            | 15       |

```pascal
FUNCTION GetLayerRenderMode(theLayer : HANDLE): INTEGER;
```

```python
def vs.GetLayerRenderMode(theLayer):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theLayer|HANDLE|   |

## Examples
```pascal
BEGIN
	boo := ResourceIsOK;
	VSave( 'TempView' );	{ save current view. }
	nObjRender := GetLayerRenderMode( hObjLayer );

	7: pioVPBackRenderMode := kRWModeHiddenDash;		{ dashed hidden line }
	8: pioVPBackRenderMode := kRWModeSketch;			{ sketch }
	9: ;												{ divider }
	10:	CASE pioLocation OF								{ use current mode }
			kpioInDesignLayer:	pioVPBackRenderMode := GetLayerRenderMode( GetLayer(pioHand) );
			kpioInVPAnnotation:	pioVPBackRenderMode := GetObjectVariableInt( pioParentVPHand, 1001 );
		END; {CASE}
END; {CASE}
{

{Set to Top view because of convert to 3D poly}
hActLayer := GetLayer (parmHand);
IF hActLayer <> NIL THEN ProjectionI := GetProjection(hActLayer) ELSE ProjectionI := GetProjection(ActLayer);
LyrRendModeIndex := GetLayerRenderMode(hActLayer);
getview(rx,ry,rz,vx,vy,vz);
```
```python
import vs

# Returns the render mode for the referenced layer.
theLayer = vs.ActLayer()  # handle to the active design layer

resultN = vs.GetLayerRenderMode(theLayer)
vs.Message('GetLayerRenderMode returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks 10.0

## Category
* [Layers](../Categories/Layers.md)
