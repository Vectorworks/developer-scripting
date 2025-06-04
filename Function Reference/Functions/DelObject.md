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

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
