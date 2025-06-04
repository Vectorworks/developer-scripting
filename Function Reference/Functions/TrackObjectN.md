# TrackObjectN

## Description
Interactively, including highlighting, allows the user to select one object meeting the specified criteria.

The callback function is used to let the user filter the object that can be returned from the function. Any of these below, depending on what info is needed :
* FUNCTION Callback(h : HANDLE): BOOLEAN;
* FUNCTION CheckObjCallback(h : HANDLE; px, py : REAL) : BOOLEAN;
* FUNCTION CheckObjCallback(h : HANDLE; px, py, pz : REAL) : BOOLEAN;

The parameters ''px, py, pz'' pass into the function information about current cursor position in document units.
This callback function is called when tracking over an object; also when click happens over an object.

```pascal
PROCEDURE TrackObjectN(
				traverseType : INTEGER;
				callback     : PROCEDURE;
				VAR outObj   : HANDLE;
				VAR p        : REAL);
```

```python
def vs.TrackObjectN(traverseType, callback):
    return (outObj, p)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|traverseType|INTEGER|Specify how to traverse the drawing.|0 - traverses only the high-level objects (the same as the TrakcObject function);|1 - traverses the objects deep (uses GetPickObjectInfo, the 'subH' parameter).|2 - traverses the objects shallow (uses GetPickObjectInfo|
|callback|PROCEDURE|The callback that will be called to check if an object meets the requrements to be tracked. See remarks.|
|outObj|HANDLE|Returns handle of the object for which the callback returned TRUE.|
|p|REAL|Returns coordinates of mouse click.|

## Remarks
[[User:CBM-c-| _c_]] (2021.01.22) Traverse Options:
* 0 = Shallow
* 1 = Groups (Traverse inside groups)
* 2 = Deep (Traverse all containers: walls, extrudes, sweeps, etc)

## Examples
```python
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
	TrackObjectN( 0, CheckObjCallback, h, x, y, z );
	SetSelect( h );
END;
RUN( Test );
```

## See Also
VS Functions:
[TrackObject](TrackObject.md) 
| [GetPickObjectInfo](GetPickObjectInfo.md)

## Version
Availability: from Vectorworks 2014

## Category
* [User Interactive](../Categories/User%20Interactive.md)
