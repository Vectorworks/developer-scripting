# Mirror

## Description
Reflect an object across an axis.<BR>
<BR>
For a 2D reflection, the axis is a line containing arbitrary point p and extending along vector v.

```pascal
FUNCTION Mirror(
				h   : HANDLE;
				dup : BOOLEAN;
				p1  : POINT;
				p2  : POINT): HANDLE;
```

```python
def vs.Mirror(h, dup, p1, p2):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The object to reflect|
|dup|BOOLEAN|If false, transform the original object to the new position. If true, create a new object|
|p1|POINT|An arbitrary point on the mirror axis|
|p2|POINT|A second arbitrary point on the mirror axis|

## Remarks
([[User:CBM-c-|_c_]], 2019.11.09) This doesn't support Groups and is unpredictable on 3D objects

## Version
Availability: from Vectorworks 2017

## Category
* [Object Editing](../Categories/Object%20Editing.md)
