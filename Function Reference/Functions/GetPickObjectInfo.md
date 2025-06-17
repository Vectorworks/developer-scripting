# GetPickObjectInfo

## Description
Function GetPickObjectInfo returns a handle to an object found at a user selected point. 

Parameter subH returns a handle to a sub-selectable object (e.g., a symbol in a wall) if such an object exists. Parameter message is currently unused, and always returns 0.

```pascal
FUNCTION GetPickObjectInfo(
				pX,pY       : REAL;
				VAR h       : HANDLE;
				VAR subH    : HANDLE;
				VAR message : INTEGER): BOOLEAN;
```

```python
def vs.GetPickObjectInfo(p):
    return (BOOLEAN, h, subH, message)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinate location to test for object.|
|h|HANDLE|Returns handle to object.|
|subH|HANDLE|Returns handle to sub selectable object.|
|message|INTEGER|Resereved for future use. Specify a dummy INTEGER variable.|

## Remarks
same as PickObject except it return the sub-selected object, if any, and a message.  See Rich D. for more details.


Only picks objects on the active class & layer, or on other classes/layers if the class/layer options are set to Show/Snap/Modify (respectively). Essentially, it will only pick an object that you could have picked manually with the Selection Tool. Same goes for the PickObject function.

The parameter "message" should be changed to something else, since there is a built-in call by this name.

with the following, able to get a handle on objects within a group- group can be in a design layer, seen through a viewport, or within a symbol.  handle is hx.  opens the door to make edits without entering containers through groups/vps or symbols, if objects are inside group.
```pascal
GetPt(X,Y);
h:=PickObject(x,y);
if GetPickObjectInfo(x, y, h, hx, message) then begin
```

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
    pX : REAL;
    pY : REAL;
    hObject : HANDLE;
    hSymbol : HANDLE;
    dummyVar : INTEGER;
BEGIN
    WHILE NOT GetPickObjectInfo(pX, pY, foundObj, subObj, dummyVar) DO BEGIN
        GetPt(pX, pY);
        Message( 'X: ', pX,'Y: ', pY );
    END;
END;
RUN(Example);
```
#### Python ####
```python
def PickPointCallback( pt ):
    vs.Message( 'X: ', pt[0], 'Y: ', pt[1] )
    success, foundObj, subObj, dummyVar = vs.GetPickObjectInfo( pt[0], pt[1] )

    if foundObj != vs.Handle():
        vs.SetSelect( foundObj )
	
	
vs.GetPt( PickPointCallback )
```

## See Also
VS Functions:
[PickObject](PickObject.md) 
| [ForEachObjectAtPoint](ForEachObjectAtPoint.md)

## Version
Availability: from VectorWorks8.0

## Category
* [Utility](../Categories/Utility.md)
