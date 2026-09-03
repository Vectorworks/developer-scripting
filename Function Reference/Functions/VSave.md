# VSave

## Description
Procedure VSave saves the current VectorWorks document view.

```pascal
PROCEDURE VSave(name : STRING);
```

```python
def vs.VSave(name):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of view to save.|

## Examples
```pascal
BEGIN
	VSave ('myTempView00000001');
	SetView (0,0,0,0,0,0);
END;

BEGIN
{	VSave('UpdateObjectsTempView');
	DoMenuTextByName(GetLocStr(11050,32), 1);{Standard Views}

BEGIN
	VSave ('__SeatingLayoutTempView');
	SetView (0, 0, 0, 0, 0, 0);
	Symbol(symName, 0, 0, 0);
	h := LNewObj;
	GetBBox(h, p1x, p1y, p2x, p2y);
```
```python
import vs

# Procedure VSave saves the current VectorWorks document view.
name = 'Example'

vs.VSave(name)
```

## Version
Availability: from All Versions

## Category
* [View @ Zoom](../Categories/View%20-%20Zoom.md)
