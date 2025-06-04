# GetMarkerPopupSelectedItem

## Description
This is a deprecated function.  Use GetMarkerChoice instead.

Returns the 1-based index number of the selected item in the specified marker popup menu item.  If return value is 8, a custom marker is selected.

```pascal
FUNCTION GetMarkerPopupSelectedItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				VAR style   : INTEGER;
				VAR angle   : INTEGER;
				VAR size    : INTEGER): INTEGER;
```

```python
def vs.GetMarkerPopupSelectedItem(dialogID, componentID):
    return (INTEGER, style, angle, size)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog|
|componentID|LONGINT|ID of the marker popup item|
|style|INTEGER|On return, indicates the style of the selected marker.  Valid styles:|0 - kFilledArrowMarker|1 - kEmptyArrowMarker|2 - kOpenArrowMarker|3 - kFilledBallMarker|4 - kEmptyBallMarker|5 - kSlashMarker|6 - kCrossMarker|
|angle|INTEGER|On return, indicates the angle of the selected marker, for arrow markers|
|size|INTEGER|On return, indicates the size of the selected marker|

## Version
Availability: from VectorWorks10.5

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
