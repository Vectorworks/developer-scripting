# SetTexSpaceOrientW

## Description
Procedure SetTexSpaceOrientW specifies the vector that describes the w-axis of the referenced texture (from world space to texture space).

```pascal
PROCEDURE SetTexSpaceOrientW(
				textureSpace : HANDLE;
				wXAxis       : REAL;
				wYAxis       : REAL;
				wZAxis       : REAL);
```

```python
def vs.SetTexSpaceOrientW(textureSpace, wXAxis, wYAxis, wZAxis):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|wXAxis|REAL|Sets w-axis vector X component.|
|wYAxis|REAL|Sets w-axis vector Y component.|
|wZAxis|REAL|Sets w-axis vector Z component.|

## Remarks
Sets the w-axis for the texture space (from world space to texture space)

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
GetTexSpaceOrientV( wallTextureSpace, xAxis, yAxis, zAxis );
SetTexSpaceOrientW( objTextureSpace, xAxis, yAxis, zAxis );

	TextSpaceHand := GetTextureSpace(h,0);
	SetTexSpaceKind(TextSpaceHand,0);
	SetTexSpaceOrientU(TextSpaceHand,0.420620787449235 ,-0.906811536331687 ,-0.0277667200322127);
	SetTexSpaceOrientV(TextSpaceHand,-0.703828946097636 ,0.703828946097624 ,0.0961749929565575);
	SetTexSpaceOrientW(TextSpaceHand,-0.19364703992807 ,-0.0598377431266686 ,-0.97924474388408);
	{U: X:0.420620787449235 Y:-0.906811536331687 Z:-0.0277667200322127
V: X:-0.703828946097636 Y:0.703828946097624 Z:0.0961749929565575
W: X:-0.19364703992807 Y:-0.0598377431266686 Z:-0.97924474388408}
	{SetTexSpace2DRot(TextSpaceHand,1.5707963267949);}

TextSpaceHand := GetTextureSpace( h, 0 ); { get handle to the tex space. }
SetTexSpaceKind( TextSpaceHand, 0 );
SetTexSpaceOrientU( TextSpaceHand, 0, -1, 0 );
SetTexSpaceOrientV( TextSpaceHand, 0, 0, -1 );
SetTexSpaceOrientW( TextSpaceHand, 1, 0, 0 );
END;
```
```python
import vs

# Procedure SetTexSpaceOrientW specifies the vector that describes the w-axis
# of the referenced texture (from world space to texture space).
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
wXAxis = 1.0
wYAxis = 2.0
wZAxis = 0.5

vs.SetTexSpaceOrientW(textureSpace, wXAxis, wYAxis, wZAxis)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
