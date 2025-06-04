# SetObjectWallOffset

## Description
Sets an object's offset value in it's  break record. <BR>
<BR>
The object (objH) must be contained in wall (wallH) for the setting to succeed.

```pascal
FUNCTION SetObjectWallOffset(
				objH   : HANDLE;
				wallH  : HANDLE;
				offset : REAL): BOOLEAN;
```

```python
def vs.SetObjectWallOffset(objH, wallH, offset):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objH|HANDLE|Handle of object to set a new offset value for.|
|wallH|HANDLE|Handle of wall containing the object references in objH.|
|offset|REAL|Value of new offset for object within wall.|

## Remarks
Julian: [2009/08/30] The offset value is to the centre of the object.

## Version
Availability: from Vectorworks 2010

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
