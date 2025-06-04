# GetScreen

## Description
Procedure GetScreen returns the top-left and bottom-right corners of the display screen. These values will change as different sized screens are used. This procedure can be utilized to aid in development of dialog boxes, or as a check of screen size for sizing or displaying custom dialogs.

```pascal
PROCEDURE GetScreen(
				VAR x1 : INTEGER;
				VAR y1 : INTEGER;
				VAR x2 : INTEGER;
				VAR y2 : INTEGER);
```

```python
def vs.GetScreen():
    return (x1, y1, x2, y2)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|x1|INTEGER|Returns X coordinate of top left of screen.|
|y1|INTEGER|Returns Y coordinate of top left of screen.|
|x2|INTEGER|Returns X coordinate of bottom right of screen.|
|y2|INTEGER|Returns Y coordinate of bottom right of screen.|

## Remarks
([[User:CBM-c-|_c_]], 2014.08.19): The values returned are pixels. For example my iMac returns "0, 0, 2560, 1440".


This seems to crash VW on Win98.

Works OK on 1000 8367 on XP.

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR 
x1, y1, x2, y2 :INTEGER;
BEGIN
GetScreen(x1, y1, x2, y2);
Message(x1,' ',y1,' ',x2,' ',y2);
END;
RUN(Example);
```
==== Python ====
```python
def Example():
	x1, y1, x2, y2 = vs.GetScreen()
	vs.Message(x1,' ',y1,' ',x2,' ',y2);
Example()
```

## Version
Availability: from All Versions

## Category
* [Utility](../Categories/Utility.md)
