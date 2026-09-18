# GetLocus3D

## Description
Procedure GetLocus3D returns the coordinates of the referenced 3D locus object.

```pascal
PROCEDURE GetLocus3D(
				h            : HANDLE;
				VAR pX,pY,pZ : REAL);
```

```python
def vs.GetLocus3D(h):
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to 3D locus.|
|p|REAL|Returns 3D coordinates of locus.|

## Examples
```pascal
{ get elevation of the locus object. }
GetLocus3D( locHandle, locusX, locusY, locusZ );

		foundInterval := TRUE;
		END;
	END;
IF (GetType(targetHandle) = kLocus3DID) THEN BEGIN
	GetLocus3D(targetHandle,targetX,targetY,targetZ);
	setLocusBtn := TRUE;
	startElev := targetZ;
	compareZ := targetZ;
	foundStartElev := TRUE;

	GetLocus3D( FInGroup( LNewObj ), pX, pY, pZ );
	DelObject( LNewObj );
END;
```
```python
import vs

# Procedure GetLocus3D returns the coordinates of the referenced 3D locus object.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

result = vs.GetLocus3D(h)
```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - 3D](../Categories/Objects%20-%203D.md)
