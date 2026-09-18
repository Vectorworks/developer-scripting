# SetTexSpaceOrientV

## Description
Procedure SetTexSpaceOrientV specifies the vector that describes the v-axis of the referenced texture (from world space to texture space).

```pascal
PROCEDURE SetTexSpaceOrientV(
				textureSpace : HANDLE;
				vXAxis       : REAL;
				vYAxis       : REAL;
				vZAxis       : REAL);
```

```python
def vs.SetTexSpaceOrientV(textureSpace, vXAxis, vYAxis, vZAxis):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|textureSpace|HANDLE|Handle to texture space.|
|vXAxis|REAL|Sets v-axis vector X component.|
|vYAxis|REAL|Sets v-axis vector Y component.|
|vZAxis|REAL|Sets v-axis vector Z component.|

## Remarks
Sets the v-axis for the texture space (from world space to texture space)

Note: SetTexMapXXX routines replace the older SetTexSpaceXXX routines.  It is recommended that all developers transition to the newer versions.

## Examples
```pascal
		xAxis := -xAxis;
		yAxis:= -yAxis;
		zAxis := -zAxis;
	end;
	SetTexSpaceOrientV( objTextureSpace, xAxis, yAxis, zAxis );
End;

	AttachDefaultTextureSpace(h,0);
	TextSpaceHand := GetTextureSpace(h,0);
	SetTexSpaceKind(TextSpaceHand,0);
	SetTexSpaceOrientU(TextSpaceHand,0.420620787449235 ,-0.906811536331687 ,-0.0277667200322127);
	SetTexSpaceOrientV(TextSpaceHand,-0.703828946097636 ,0.703828946097624 ,0.0961749929565575);
	SetTexSpaceOrientW(TextSpaceHand,-0.19364703992807 ,-0.0598377431266686 ,-0.97924474388408);
	{U: X:0.420620787449235 Y:-0.906811536331687 Z:-0.0277667200322127
V: X:-0.703828946097636 Y:0.703828946097624 Z:0.0961749929565575
W: X:-0.19364703992807 Y:-0.0598377431266686 Z:-0.97924474388408}

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

# Procedure SetTexSpaceOrientV specifies the vector that describes the v-axis
# of the referenced texture (from world space to texture space).
textureSpace = vs.FSActLayer()  # handle to the first selected object on the active layer
vXAxis = 1.0
vYAxis = 2.0
vZAxis = 0.5

vs.SetTexSpaceOrientV(textureSpace, vXAxis, vYAxis, vZAxis)
```

## Version
Availability: from VectorWorks8.0

## Category
* [Textures](../Categories/Textures.md)
