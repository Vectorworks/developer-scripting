# ForEachObjectAtPoint

## Description
Performs an action for each object at the specified point in the drawing. This call was implemented to get past the practical limitations of PickObject, which only finds the topmost object. This call will find all of the objects at a given point.

&quot;actionFunc&quot; should actually be a function, not a procedure as the declaration indicates.

If the callback function returns FALSE, ForEachObjectAtPoint will not process any more objects at the specified point.

{| class="wikitable"
|+ Table - ForEachObjectAtPoint Selectors
! Option !! Selector !! Description
|-
! Colspan="3" | Object Options
|-
| All objects
| style="text-align:center"| 0
| 
|-
| Visible Objects only
| style="text-align:center"| 1
|  
|-
| Selected Objects only
| style="text-align:center"| 2
| 
|-
| Unlocked objects only
| style="text-align:center"| 4
| 
|-
! Colspan="3" | Traversal Options
|-
| Traverse Shallow
| style="text-align:center"| 0
|  
|-
| Traverse Groups
| style="text-align:center"| 1
| Traverse inside groups
|}

```pascal
PROCEDURE ForEachObjectAtPoint(
				actionFunc  : PROCEDURE;
				objOptions  : INTEGER;
				travOptions : INTEGER;
				locX,locY   : REAL;
				pickRadius  : REAL);
```

```python
def vs.ForEachObjectAtPoint(actionFunc, objOptions, travOptions, loc, pickRadius):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|actionFunc|PROCEDURE|   |
|objOptions|INTEGER|   |
|travOptions|INTEGER|   |
|loc|REAL|   |
|pickRadius|REAL|   |

## Remarks
([[User:CBM-c-|_c_]], 2011 Oct. 06): This function only finds objects within the same parent, so it won't work from inside PIOs for finding something which is on drawing, nor does it work for finding objects on other layers, unregarded their visibility options. 

<b>NOTE</b> This function is very specific and have some problems:
* doesn't go inside groups. The callback pointer is being set to NIL when going inside groups;
* doesn't pick groups;

You can use [[VS:FindObjAtPt_Create]], [[VS:FindObjAtPt_GetCount]], or [[VS:FindObjAtPt_GetObj]] instead.

## Examples
```pascal
PROCEDURE Example;
VAR
	gx1, gy1 : REAL;

FUNCTION DoIt(h1 :HANDLE) :BOOLEAN;
BEGIN
	DSelectAll;
	SetSelect(h1);
	Redraw;
	Wait(1);
END;

BEGIN
	GetPt(gx1, gy1);
	ForEachObjectAtPoint(DoIt, 0, 0, gx1, gy1, 5);
END;
RUN(Example);
```
Python:
```python
import vs;

def DoIt(h1):
	vs.AlrtDialog( "we're in", h1 )

def PickPointCallback(pt):
	vs.ForEachObjectAtPoint(DoIt, 0, 0, pt[0], pt[1], 5)

vs.AlrtDialog( "show let you pick a point, and then show a dialog with the object's handle" )
vs.GetPt( PickPointCallback )
```

## See Also
VS Functions:
[PickObject](PickObject.md) 
| [GetPickObjectInfo](GetPickObjectInfo.md) 
| [FindObjAtPt_Create](FindObjAtPt_Create.md) 
| [FindObjAtPt_GetCount](FindObjAtPt_GetCount.md) 
| [FindObjAtPt_GetObj](FindObjAtPt_GetObj.md)

## Version
Availability: from VectorWorks 13.0

## Category
* [Utility](../Categories/Utility.md)
