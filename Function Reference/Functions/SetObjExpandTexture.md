# SetObjExpandTexture

## Description
Procedure SetObjExpandTexture sets the &quot;expanded&quot; state of the referenced objects' texture. When a texture is expanded, different components of an object can have different textures.

```pascal
PROCEDURE SetObjExpandTexture(
				obj      : HANDLE;
				expanded : BOOLEAN);
```

```python
def vs.SetObjExpandTexture(obj, expanded):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Handle to object.|
|expanded|BOOLEAN|Use expanded textures setting.|

## Remarks
Sets whether three or just a single texture is applied to this object (can be up to three for walls or two for roofs).

## Examples
```pascal
Wall(-(cWidth/2-3*upi),(cWidth/2-3*upi),(cWidth/2-3*upi),(cWidth/2-3*upi));
SetObjExpandTexture(lNewObj,FALSE);
SetTextureRef(lNewObj,-1,7);
WallCap(FALSE,FALSE,FALSE,-3*upi,3*upi);
WallCap(TRUE,FALSE,FALSE,3*upi,-3*upi);
result := SetWallOverallHeights(lnewobj,0,0,'',cHeight,0,0,'',cHeight);

	BEGIN
	AttachDefaultTextureSpace(h, 0); { Give it one}
	TexSpaceHan := GetTextureSpace(h, 0); {Get a handle to the Tex Space}
	END;
SetObjExpandTexture(h,FALSE);
SetTextureRef(h, TexIndex, 0);
END;
```
```python
import vs

# Procedure SetObjExpandTexture sets the &quot;expanded&quot; state of the
# referenced objects' texture.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
expanded = True

vs.SetObjExpandTexture(obj, expanded)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
