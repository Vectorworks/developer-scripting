# CreateSymDispCtrlN

## Description
Creates a new symbol display control in the dialog layout.  The control displays the specified symbol in the specified rendering mode and view. Specified image component is used.  The actual size of the symbol is not relevant; it is shown as large as possible in the given height and width (the height to width ratio of the symbol is always preserved).  To show a blank SymbolDisplay control, use an empty string as the symbolName parameter.<BR>

**Table - Render Modes**

| Render Mode                      | Constant |
|----------------------------------|----------|
| Wireframe                        | 0        |
| Unshaded Polygon                 | 2        |
| Shaded Polygon                   | 3        |
| Shaded Polygon No Lines          | 4        |
| Final Shaded Polygon             | 5        |
| Hidden Line                      | 6        |
| Dashed Hidden Line               | 7        |
| OpenGL                           | 11       |
| Fast RenderWorks                 | 12       |
| Fast RenderWorks with Shadows    | 13       |
| Final Quality RenderWorks        | 14       |
| Custom RenderWorks               | 15       |
| Artistic RenderWorks             | 17       |
| Sketch                           | 18       |

**Table - Views**

| View                      | Constant |
|---------------------------|----------|
| Top/Plan                  | 2        |
| Front                     | 3        |
| Back                      | 4        |
| Left                      | 5        |
| Right                     | 6        |
| Top                       | 7        |
| Bottom                    | 8        |
| Right Isometric           | 9        |
| Left Isometric            | 10       |
| Right Rear Isometric      | 11       |
| Left Rear Isometric       | 12       |
| Bottom Right Isometric    | 13       |
| Bottom Left Isometric     | 14       |
| Bottom Right Rear Isometric | 15     |
| Bottom Left Rear Isometric  | 16     |

**Table - Components**

| Component   | Constant |
|-------------|----------|
| "3D"        | 0        |
| "2D"        | 1        |
| "2D Cut"    | 2        |
| "Not set"   | 4        |

```pascal
PROCEDURE CreateSymDispCtrlN(
				dialogID    : LONGINT;
				itemID      : LONGINT;
				symbolName  : STRING;
				width       : INTEGER;
				height      : INTEGER;
				margin      : INTEGER;
				view        : INTEGER;
				renderMode  : INTEGER;
				component   : INTEGER;
				scaleByZoom : BOOLEAN);
```

```python
def vs.CreateSymDispCtrlN(dialogID, itemID, symbolName, width, height, margin, view, renderMode, component, scaleByZoom):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog in which to create the control.|
|itemID|LONGINT|The item ID of the control.|
|symbolName|STRING|The name of the symbol to display.|
|width|INTEGER|The width of the control in pixels.|
|height|INTEGER|The height of the control in pixels.|
|margin|INTEGER|The margin between the border of the control and the symbol in pixels.|
|view|INTEGER|The view in which to display the symbol.|
|renderMode|INTEGER|The render mode in which to display the symbol.|
|component|INTEGER|The image component.|
|scaleByZoom|BOOLEAN|Whether the sizing is done by zoom or layer scale.|

## See Also
VS Functions:
[UpdateSymDispCtrlN](UpdateSymDispCtrlN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
