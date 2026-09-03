# GetLayer

## Description
Function GetLayer returns a handle to the layer of the referenced object.

```pascal
FUNCTION GetLayer(h : HANDLE): HANDLE;
```

```python
def vs.GetLayer(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Care should be taken when using this call in the code for an object. If an object is cut-n-pasted or inserted from the object browser, it has to regenerate before it is actually in a layer, in which case GetLayer(h) will return a nil handle. So always check that you have a valid handle before proceeding. (This may have been fixed -- ask Jeff Koppi about this.)

## Examples
#### VectorScript ####
```pascal
LayerHandle:=GetLayer(ObjHd);
```
#### Python ####
```python
LayerHandle = vs.GetLayer(ObjHd)
```

```pascal
actLayerH := actLayer;
IF GetLayer (h) <> NIL THEN Layer (GetLName (GetLayer (h)));
{Layer (GetLName (GetLayer (h)));}
getArcProps (objH, method, r, theta1, theta2, maxSegLength, x, y);

		ELSE Scaler := GetLScale(ActLayer);
	END
	ELSE Scaler := GetLScale(ActLayer);
}
	IF GetLayer(parmHand) <> NIL THEN
		Scaler := GetLScale(GetLayer(parmHand))
	ELSE Scaler := GetLScale(ActLayer);

IF ( NOT p__IsPilaster ) & ( gPluginH <> NIL ) & ( gOAHeight < 0 ) & ( GetLayer( gPluginH ) <> NIL ) THEN
BEGIN
	UpdateBound( gPluginH, gPluginH, kOldTopBoundArchitID, kTopBoundArchitID, pOA_Height );
	UpdateBound( gPluginH, gPluginH, kOldBotBoundArchitID, kBotBoundArchitID, 0 );
	CalculateBoundHeight( kTopBoundArchitID, kBotBoundArchitID, topArchitHeight, botArchitHeight );
END;
```
```python
import vs

# Function GetLayer returns a handle to the layer of the referenced object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

objHandle = vs.GetLayer(h)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```
See also in tutorials: [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md)

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
