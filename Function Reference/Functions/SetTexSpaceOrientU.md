# SetTexSpaceOrientU

## Description
Procedure SetTexSpaceOrientU specifies the vector that describes the u-axis of the referenced texture (from world space to texture space).

```pascal
PROCEDURE SetTexSpaceOrientU(
				textureSpace : HANDLE;
				uXAxis       : REAL;
				uYAxis       : REAL;
				uZAxis       : REAL);
```

```python
def vs.SetTexSpaceOrientU(textureSpace, uXAxis, uYAxis, uZAxis):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|uXAxis|REAL|Sets u-axis vector X component.|
|uYAxis|REAL|Sets u-axis vector Y component.|
|uZAxis|REAL|Sets u-axis vector Z component.|

## Remarks
Sets the u-axis for the texture space (from world space to texture space)

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
	xAxis := -xAxis;
	yAxis:= -yAxis;
	zAxis := -zAxis;
end;
SetTexSpaceOrientU( objTextureSpace, xAxis,  zAxis, yAxis );

	BEGIN
	AttachDefaultTextureSpace(h,0);
	TextSpaceHand := GetTextureSpace(h,0);
	SetTexSpaceKind(TextSpaceHand,0);
	SetTexSpaceOrientU(TextSpaceHand,0.420620787449235 ,-0.906811536331687 ,-0.0277667200322127);
	SetTexSpaceOrientV(TextSpaceHand,-0.703828946097636 ,0.703828946097624 ,0.0961749929565575);
	SetTexSpaceOrientW(TextSpaceHand,-0.19364703992807 ,-0.0598377431266686 ,-0.97924474388408);
	{U: X:0.420620787449235 Y:-0.906811536331687 Z:-0.0277667200322127
V: X:-0.703828946097636 Y:0.703828946097624 Z:0.0961749929565575

TextSpaceHand := GetTextureSpace( h, 0 ); { does it have a tex space ? }
IF ( TextSpaceHand = NIL ) THEN AttachDefaultTextureSpace( h, 0 ); { give it one. }
TextSpaceHand := GetTextureSpace( h, 0 ); { get handle to the tex space. }
SetTexSpaceKind( TextSpaceHand, 0 );
SetTexSpaceOrientU( TextSpaceHand, 0, -1, 0 );
SetTexSpaceOrientV( TextSpaceHand, 0, 0, -1 );
SetTexSpaceOrientW( TextSpaceHand, 1, 0, 0 );
END;
```
```python
import vs

# Procedure SetTexSpaceOrientU specifies the vector that describes the u-axis
# of the referenced texture (from world space to texture space).
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
uXAxis = 1.0
uYAxis = 2.0
uZAxis = 0.5

vs.SetTexSpaceOrientU(textureSpace, uXAxis, uYAxis, uZAxis)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
