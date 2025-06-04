# UpdateSymbolDisplayControl

## Description
Updates a pre-existing symbol display control in the dialog with a new symbol, rendering mode, or view.  The dialog ID and item ID must refer to symbol display control created with CreateSymbolDisplayControl.  To show a blank SymbolDisplay control, use an empty string as the symbolName parameter.

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
PROCEDURE UpdateSymbolDisplayControl(
				dialogID   : LONGINT;
				itemID     : LONGINT;
				symbolName : STRING;
				renderMode : INTEGER;
				view       : INTEGER);
```

```python
def vs.UpdateSymbolDisplayControl(dialogID, itemID, symbolName, renderMode, view):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog in which to create the control.|
|itemID|LONGINT|The item ID of the control.|
|symbolName|STRING|The name of the symbol to display.|
|renderMode|INTEGER|The render mode in which to display the symbol.|
|view|INTEGER|The standard view in which to display the symbol.|

## Examples
#### VectorScript ####
```pascal
CreateSymbolDisplayControl( 5, 6, 'Chair', 350, 200, 5, 11, 9 );
{Other code}
UpdateSymbolDisplayControl( 5, 6, 'Chair', 0, 3 );

This creates a dialog control that displays the symbol called &quot;Chair.&quot;  The control is 350 pixels high and 200 pixels wide, with a margin of 5 pixels.  The symbol is rendered in OpenGL mode and displayed in a right isometric view.  It then later updates the control to display the same symbol rendered in Wireframe in a front view.
```
#### Python ####
```python

```

## See Also
VS Functions:
[CreateSymbolDisplayControl](CreateSymbolDisplayControl.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
