# TrackObject

## Description
Interactively, including highlighting, allows the user to select one object meeting the specified criteria.

The callback function (any of these depending on what info is needed):

<code lang="pas">
FUNCTION Callback(h : HANDLE): BOOLEAN;
FUNCTION CheckObjCallback(h : HANDLE; px, py : REAL) : BOOLEAN;
FUNCTION CheckObjCallback(h : HANDLE; px, py, pz : REAL) : BOOLEAN;
</code>

is used to let the user filter the object that can be returned from the function.

The parameter px, py, pz pass into the function information about current cursor position in document units.

This callback function is called when tracking over an object; also when click happens over an object.
Returns true if the passed handle can be returned.

```pascal
PROCEDURE TrackObject(
				callback       : PROCEDURE;
				VAR outObj     : HANDLE;
				VAR px, py, pz : REAL);
```

```python
def vs.TrackObject(callback):
    return (outObj, p)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|callback|PROCEDURE|The callback that will be called to check if an object meets the requirements to be tracked. See remarks.|
|outObj|HANDLE|Returns handle to the selected from the temp tool object.|
|p|REAL|Returns coordinates of mouse click.|

## Remarks
[[User:CBM-c-|_c_]], (2011 Oct. 03): The user is always prompted to select a point, similar to using [[VS:GetPt| GetPt]], and this point seems to be the required criteria. So the description is a bit misleading, since you might believe that the routine takes care of the point all by itself, which doesn't happen.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Test;
VAR
  h : HANDLE;
  x, y, z : REAL;
  
  FUNCTION CheckObjCallback(h : HANDLE) : BOOLEAN;
  {or FUNCTION CheckObjCallback(h : HANDLE; px, py : REAL) : BOOLEAN;}
  {or FUNCTION CheckObjCallback(h : HANDLE; px, py, pz : REAL) : BOOLEAN;}
  BEGIN
     {any object is ok}
     CheckObjCallback := true;
  END;

BEGIN
     TrackObject( CheckObjCallback, h, x, y, z );
     IF h <> NIL THEN
          SetSelect( h );
END;
RUN( Test );
```
#### Python ####
```python

```

## See Also
VS Functions:
[GetPt](GetPt.md) |
[GetPtL](GetPtL.md) |
[GetPt3D](GetPt3D.md) |
[GetPtL3D](GetPtL3D.md) |
[GetLine](GetLine.md) |
[GetLine3D](GetLine3D.md) |
[GetRect](GetRect.md) |
[GetRect3D](GetRect3D.md) |
[TrackObject](TrackObject.md)

## Version
Availability: from Vectorworks 2010

## Category
* [User Interactive](../Categories/User%20Interactive.md)
