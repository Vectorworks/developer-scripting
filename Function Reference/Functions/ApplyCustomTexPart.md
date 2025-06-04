# ApplyCustomTexPart

## Description
Applies the src object’s custom texture part partID to dest Overall part.  For example apply PIO texture partID 100 to extrude’s Overall part.  If the dest object does not support the src map type then a default mapping is used.

```pascal
PROCEDURE ApplyCustomTexPart(
				srcObj  : HANDLE;
				destObj : HANDLE;
				partID  : LONGINT);
```

```python
def vs.ApplyCustomTexPart(srcObj, destObj, partID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|srcObj|HANDLE|The source object from which to get the texture assignment and mapping.|
|destObj|HANDLE|The dest object to apply the texture and mapping to.  The texture and mapping are applied to destObj’s Overall texture part.|
|partID|LONGINT|The custom texture part ID to apply from the src to the dest object.|

## Examples
```python
ApplyCustomTexPart(parentPIO, pioSubObj, 100);
```

## Version
Availability: from Vectorworks 2017

## Category
* [Textures](../Categories/Textures.md)
