# vstSetPtBehavior

```pascal
PROCEDURE vstSetPtBehavior(inStatusType : LONGINT);
```

```python
def vs.vstSetPtBehavior(inStatusType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inStatusType|LONGINT|   |

## Remarks
0 -  the tool will collect two points using click drag gesture

1 - the tool will collect one point

2 -  the tool will collect two points using user click-click/drag pref setting

3 -  the tool will collect three points

4 -  the tool will collect multiple points - double-click completes

101 - the tool will draw a box

102 - the tool will draw an Ellipse

## Examples
```pascal
BEGIN
	CASE inMode OF
		1: VSTSetPtBehavior (kEllipseDraw);
		2: VSTSetPtBehavior (kBoxDraw);
		3: VSTSetPtBehavior (kPolyPointTool);
		4: VSTSetPtBehavior (103);
	END;

BEGIN
	VSTSetPtBehavior( kTwoPointTool );
	vstGetDataLong( kModeDataID, modeValue, result );
	IF NOT result THEN
	BEGIN
		modeValue := 2;

	AddButtonMode('VWMiscSmallImages/11016.png');
	BeginModeButtonsText;
	SetModeButtonText( GetPluginString( 6000 ), 2 );
	EndModeButtonsText;
	vstSetPtBehavior(kPolyPointTool);
	vstSetModeHelpBase( -2322 );
END;
```
```python
import vs

inStatusType = 0

vs.vstSetPtBehavior(inStatusType)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
