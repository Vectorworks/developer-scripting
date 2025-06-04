# GetMouse

## Description
Procedure GetMouse tracks and returns the current location of the cursor within the active VectorWorks document, allowing the cursor coordinates to be returned dynamically while moving the cursor onscreen.

```pascal
PROCEDURE GetMouse(VAR pX,pY : REAL);
```

```python
def vs.GetMouse():
    return p
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Returns current mouse coordinates.|

## Remarks
This function does not return accurate position of the mouse on the current 2D plane when in a 3D view.

## Examples
#### VectorScript ####
```pascal
BEGIN
WHILE NOT KeyDown(aCode) DO
BEGIN
GetMouse(CursX,CursY);
Message('X : ',CursX,' Y : ',CursY);
END;
END;
{displays the cursor coordinates as it is moved around onscreen}
```
#### Python ####
```python
def Example():
	isKeyDown, alakiCode = vs.KeyDown()
	while not(isKeyDown):
		CursPt = vs.GetMouse()
		vs.Message('X : ',CursPt[0],' Y : ',CursPt[1])
		isKeyDown, alakiCode = vs.KeyDown()
Example()
```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
