# SetMarkerChoice

## Description
_OBSOLETE procedure for VW2008_

Set current choice for Marker popup dialog control.  Index  is the standing position of marker; it is -1 for customized, otherwise 1-based index.
Style is the chosen shape of arrow head . Style is zero-based. The angle parameter must be in range 0 to 90 degrees, depending on the style. Size is per Inches.  Style, angle and size may be changed by user in VW preferences.
Further, the function can find a specific Index , given the right Style, Angle &amp; Size. In such case index should be set to -1. If the given properties correspond to one of indecies, then -1 is replaced with that specific index.
When using pre-defined arrow heads, style &amp; angle &amp; size may be passed zero and just fill in the proper index to set the current.

```pascal
PROCEDURE SetMarkerChoice(
				dialogID : LONGINT;
				itemID   : LONGINT;
				index    : INTEGER;
				style    : INTEGER;
				angle    : INTEGER;
				size     : REAL);
```

```python
def vs.SetMarkerChoice(dialogID, itemID, index, style, angle, size):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|itemID|LONGINT|   |
|index|INTEGER|   |
|style|INTEGER|   |
|angle|INTEGER|   |
|size|REAL|   |

## Remarks
OBSOLETE procedure for VW2008, use SetMarkerValue instead.
Set current choice for Marker popup dialog control.

## Examples
#### VectorScript ####
```pascal
PROCEDURE dialog1_Main;
VAR
int, dialog1   :INTEGER;
index, style, angle, size :INTEGER;

PROCEDURE dialog1_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
CASE item OF
SetupDialogC:
BEGIN
index := 1;
style := 2;
angle := 3;
size  := 4;
SetMarkerChoice(dialog1, 4, index, style, angle, size);
END;
5: 
BEGIN
GetMarkerChoice(dialog1, 4, index, style, angle, size);
AlrtDialog(Concat('index: ', index, Chr(13), 'style: ', style, Chr(13), 'angle: ', angle, Chr(13), 'size: ', size));
END;
END;
END;

BEGIN
dialog1 := CreateLayout('Test', False, 'OK', '');
CreateMarkerPopup(dialog1, 4);
CreatePushButton(dialog1, 5, '  Display Values  ');
SetFirstLayoutItem(dialog1, 4);
SetBelowItem(dialog1, 4, 5, 0, 2);
int := RunLayoutDialog(dialog1, dialog1_Handler);
END;
RUN(dialog1_Main);
```
#### Python ####
```python

```

## See Also
VS Functions:
[GetMarkerChoice](GetMarkerChoice.md)

## Version
SetMarkerChoice is obsolete as of VectorWorks13.0<P>


Availability: from VectorWorks12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
