# SetObjectAsSpanBreak

## Description
Sets an object's span wall flag in it's break record.<BR>
<BR>
Setting the flag to TRUE will force the object the center of the wall and set the offset position of the break record to reflect this.<BR>
<BR>
Setting the flag to FALSE will unset the span wall flag, but no further updating to the object will occur.<BR>
<BR>
The oject (objH) must be contained in wall (wallH) for the setting to succeed.

```pascal
FUNCTION SetObjectAsSpanBreak(
				objH          : HANDLE;
				wallH         : HANDLE;
				spanWallBreak : BOOLEAN): BOOLEAN;
```

```python
def vs.SetObjectAsSpanBreak(objH, wallH, spanWallBreak):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|The handle of the object to update.|
|wallH|HANDLE|The handle of the wall cotainting the object referenced in objH.|
|spanWallBreak|BOOLEAN|Boolean value to set or unset the span wall  flag for the object.|

## Examples
```pascal
resultOK := SetObjectAsSpanBreak(objH, wallH, TRUE);
```
```python
import vs

# Sets an object's span wall flag in it's break record.
objH = vs.FSActLayer()  # handle to the first selected object on the active layer
wallH = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
spanWallBreak = True

ok = vs.SetObjectAsSpanBreak(objH, wallH, spanWallBreak)
if ok:
    vs.Message('SetObjectAsSpanBreak succeeded')
else:
    vs.Message('SetObjectAsSpanBreak failed')
```

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
