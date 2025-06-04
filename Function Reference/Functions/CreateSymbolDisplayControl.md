# CreateSymbolDisplayControl

## Description
Creates a new symbol display control in the dialog layout.  The control displays the specified symbol in the specified rendering mode and view.  The actual size of the symbol is not relevant; it is shown as large as possible in the given height and width (the height to width ratio of the symbol is always preserved).  To show a blank SymbolDisplay control, use an empty string as the symbolName parameter.

{| class="wikitable_c"
|+ Table - Render Modes
! Render Mode !! Constant
|-
| Wireframe
| 0
|-
| Unshaded Polygon
| 2
|-
| Shaded Polygon
| 3
|-
| Shaded Polygon No Lines
| 4
|-
| Final Shaded Polygon
| 5
|-
| Hidden Line
| 6
|-
| Dashed Hidden Line
| 7
|-
| OpenGL
| 11
|-
| Fast RenderWorks
| 12
|-
| Fast RenderWorks with Shadows
| 13
|-
| Final Quality RenderWorks
| 14
|-
| Custom RenderWorks
| 15
|-
| Artistic RenderWorks
| 17
|-
| Sketch
| 18
|}

{| class="wikitable_c"
|+ Table - Views
! View !! Constant
|-
| Top/Plan
| 2
|-
| Front
| 3
|-
| Back
| 4
|-
| Left
| 5
|-
| Right
| 6
|-
| Top
| 7
|-
| Bottom
| 8
|-
| Right Isometric
| 9
|-
| Left Isometric
| 10
|-
| Right Rear Isometric
| 11
|-
| Left Rear Isometric
| 12
|-
| Bottom Right Isometric
| 13
|-
| Bottom Left Isometric
| 14
|-
| Bottom Right Rear Isometric
| 15
|-
| Bottom Left Rear Isometric
| 16
|}

```pascal
PROCEDURE CreateSymbolDisplayControl(
				dialogID   : LONGINT;
				itemID     : LONGINT;
				symbolName : STRING;
				height     : INTEGER;
				width      : INTEGER;
				margin     : INTEGER;
				renderMode : INTEGER;
				view       : INTEGER);
```

```python
def vs.CreateSymbolDisplayControl(dialogID, itemID, symbolName, height, width, margin, renderMode, view):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog in which to create the control.|
|itemID|LONGINT|The item ID of the control.|
|symbolName|STRING|The name of the symbol to display.|
|height|INTEGER|The height of the control in pixels.|
|width|INTEGER|The width of the control in pixels.|
|margin|INTEGER|The margin bewteen the border of the control and the symbol in pixels.|
|renderMode|INTEGER|The render mode in which to display the symbol.|
|view|INTEGER|The view in which to display the symbol.|

## Examples
==== VectorScript ====
```pascal
CreateSymbolDisplayControl( 5, 6, 'Chair', 350, 200, 5, 11, 9 );
```
This creates a dialog control that displays the symbol called &quot;Chair.&quot;  The control is 350 pixels high and 200 pixels wide, with a margin of 5 pixels.  The symbol is rendered in OpenGL mode and displayed in a right isometric view.
```pascal
PROCEDURE Example;
VAR
dialog1 :INTEGER;
int     :INTEGER;

PROCEDURE dialog1_Handler(VAR item :LONGINT; data :LONGINT);
BEGIN
END;

BEGIN
dialog1 := CreateLayout('Example', TRUE, 'OK', 'Cancel');
CreateSymbolDisplayControl(dialog1,  4,  'Symbol-1', 128, 128, 0, 11, 9);
SetFirstLayoutItem(dialog1,  4);
int := RunLayoutDialog(dialog1, dialog1_Handler);
END;
RUN(Example);
```
==== Python ====
```python
def dialog1_Handler( item , data ):
	pass

def Example():
	dialog1 = vs.CreateLayout('Example', True, 'OK', 'Cancel')
	vs.CreateSymbolDisplayControl(dialog1,  4,  'Symbol-1', 128, 128, 0, 11, 9)
	vs.SetFirstLayoutItem(dialog1,  4)
	int = vs.RunLayoutDialog(dialog1, dialog1_Handler)
Example()
```

## See Also
VS Functions:
[UpdateSymbolDisplayControl](UpdateSymbolDisplayControl.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
