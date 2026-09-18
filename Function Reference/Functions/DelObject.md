# DelObject

## Description
Procedure DelObject deletes the referenced object from the document.

```pascal
PROCEDURE DelObject(h : HANDLE);
```

```python
def vs.DelObject(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
Note that DelObject doesn't work when called from inside a PIO to delete something that is not also inside the PIO. I don't have an explanation for this one -- just know it's so. Anyway, there's a workaround. 

SetCustomObjectProfileGroup is a call that was implemented so that a script could move an object in the drawing into the profile group of a PIO. This even works if the PIO getting the new profile group is the currently executing script. So a PIO can redefine its own profile group using this call.

When a new profile group gets assigned, the existing profile group simply goes bye-bye, and the new profile group is not copied from the main drawing list -- it is MOVED from the main drawing list. 

To think of this behavior in another way (that was certainly not intended originally), we can think of the profile group as a sort of bottomless trash can. You throw things in there, and you never see them again, and you don't even have to empty the trash can. When something is moved from the drawing list into the profile group of a PIO, it disappears from the drawing (effectively deleted), and even during the same script execution, another object can be assigned to the same profile group. Then, the first object is actually gone forever, and the second object is effectively deleted. Hence SetCustomObjectProfileGroup can be used as a substitute for DelObject when an object wants to delete peer objects.

## Examples
```pascal
BEGIN
	DelObject(LNewObj);
	DrawDrawer(gDrawerHandleHeight, gDrawerStyle,gDrawerPanelStyle,-gLeftLength+gSideReveal,-gBottomReveal-gDepth-gKickHeight-gDoorHeight-gMidReveal,gLeftDoorLength+gFaceThick,gDrawerHeight,gRailWidth,gRailWidth,gMulWidth,gDoorThick,gThinPanel,gInsideTap,gOutsideTap,gDoorsClass,gGlassClass,DrawerHandSymName,1,0);
	SET3DRot(LNewObj, -90, 0, 0, 0,-gDepth, 0);
	IF NOT bFlush THEN Move3DObj(LNewObj,0,-gDoorThick,0);
END;

		END;
	EndGroup;
	groupHand := LNewObj;
	MXTrd_NURBS := CreateLoftSurfaces(groupHand, kRule, kClose, kSolid);
	DelObject(groupHand);
{
message (' solidHand = ',solidHand ,'   curveHand [2] = ',curveHand [2]);
}
	{IF (ProjectionI <> 6) & ((xAngle <> 0) | (yAngle <> 0) | (zAngle <> 0)) THEN

			SetTextFont( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextFont( textFoundH, 0 ) );
			SetTextSize( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextSize( textFoundH, 0 ) );
			SetTextStyle( LNewObj, 0, GetTextLength( LNewObj )-1 , GetTextStyle( textFoundH, 0 ) );
			AddNumberWidth := GetTextWidth( LNewObj );
			DelObject(LNewObj);
		end ELSE AddNumberWidth := 0;
	END ELSE AddNumberWidth := 0;
	KNprefix := Concat( KNprefix, ' ' );
END ELSE AddNumberWidth := 0;
```
```python
if hTempSymDef != None:
	vs.DelObject( hTempSymDef )
```
See also in tutorials: [21. Hello Worksheet — Create and Populate](ai%20examples/21_WorksheetBasic.md), [22. Selected Objects → Worksheet Rows](ai%20examples/22_WorksheetSelectedObjects.md), [23. Count Objects by Criteria (Formula-Driven)](ai%20examples/23_WorksheetCountByCriteria.md), [24. Auto-Populating Database Row](ai%20examples/24_WorksheetDBRowAutoPopulate.md)

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
