# SetObjectAsCornerBreak

## Description
Sets an object's corner break flag in it's corner break record. <BR>
<BR>
Setting the flag to TRUE will force the object into the closest end of the wall and set the offset position of the break record to reflect this.<BR>
<BR>
Setting the flag to FALSE will unset the corner flag, but no further updating to the object will occur.<BR>
<BR>
The object (objH) must be contained in wall (wallH) for the setting to succeed.

```pascal
FUNCTION SetObjectAsCornerBreak(
				objH        : HANDLE;
				wallH       : HANDLE;
				cornerBreak : BOOLEAN): BOOLEAN;
```

```python
def vs.SetObjectAsCornerBreak(objH, wallH, cornerBreak):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|The handle of the object to update.|
|wallH|HANDLE|The handle of the wall containing the object referenced in objH.|
|cornerBreak|BOOLEAN|Boolean value to set or unset the cornerBreak flag for the object.|

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
