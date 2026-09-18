# Layer

## Description
Procedure Layer creates a new layer in a VectorWorks document. After creation, the new layer becomes the active layer of the document.

Layer can also be used to switch the active layer of the document. If the layer name passed to the procedure already exists, the procedure switches the active layer to the specified layer.

Single quotes should be avoided in layer names, as they will be treated as a mismatched string specifier, and will cause an error to be generated.

```pascal
PROCEDURE Layer(name : STRING);
```

```python
def vs.Layer(name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of new or existing layer.|

## Examples
[IsolateLayer](examples/IsolateLayer.md)

```pascal
actLayerH := actLayer;
IF GetLayer (h) <> NIL THEN Layer (GetLName (GetLayer (h)));
{Layer (GetLName (GetLayer (h)));}
getArcProps (objH, method, r, theta1, theta2, maxSegLength, x, y);

{store the active Layer}
actLH := ActLayer;
{change the active Layer}
Layer( GetLName( GetLayer( textFoundH ) ) );

if layerOptions = 1 then BEGIN
	SetLayerOptions(5);
	temp_h := FLayer;
	while temp_h <> nil do BEGIN
		Layer(GetLName(temp_h));
		ShowLayer;
		temp_h := NextObj(temp_h);
	END;
```
```python
if ( objectLayerName != '' ) and ( objectLayerName != activeLayerName ):
	vs.Layer( objectLayerName )
	bRestoreLayer = True
```
See also in tutorials: [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md), [29. Cross-Layer Summary](ai%20examples/29_WorksheetCrossLayerSummary.md), [30. Publish Worksheet Image on a Sheet Layer](ai%20examples/30_WorksheetPublishOnSheet.md)

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
