# GetCWPanelFromPt

## Description
Returns information about a panel in a curtain wall from a given point.<BR>
<BR>
Used for placing objects inside a panel in a curtain wall. When passing the center point of the object in the wall, it will find the panel in the curtain wall and return a new center point and the height and width of the panel.

```pascal
FUNCTION GetCWPanelFromPt(
				hWall              : HANDLE;
				testPt             : POINT;
				includeBottomFrame : BOOLEAN;
				VAR centerPt       : POINT;
				VAR width          : REAL;
				VAR height         : REAL): BOOLEAN;
```

```python
def vs.GetCWPanelFromPt(hWall, testPt, includeBottomFrame):
    return (BOOLEAN, centerPt, width, height)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hWall|HANDLE|Handle to the curtain wall|
|testPt|POINT|Point to test on the curtain wall. Typically the center point of the object to be placed in the curtain wall panel.|
|includeBottomFrame|BOOLEAN|Include the bottom frame in the return height.|
|centerPt|POINT|Returns the center point of the rectangle in witch to place the object.|
|width|REAL|The width of the rectangle in which to place the object.|
|height|REAL|The height of the rectangle in which to place the object.|

## Examples
```pascal
resultOK := GetCWPanelFromPt(hWall, 1, TRUE, 2, 1.0, 2.0);
```
```python
import vs

# Returns information about a panel in a curtain wall from a given point.
hWall = vs.FSActLayer()  # handle to the first selected object on the active layer
testPt = (0, 0)
includeBottomFrame = True

ok, centerPt, width, height = vs.GetCWPanelFromPt(hWall, testPt, includeBottomFrame)
vs.Message('GetCWPanelFromPt returned: ' + str((ok, centerPt, width, height)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Objects - Walls](../Categories/Objects%20-%20Walls.md)
