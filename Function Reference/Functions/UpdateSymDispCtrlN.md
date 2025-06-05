# UpdateSymDispCtrlN

## Description
Updates a pre-existing symbol display control in the dialog with a new symbol, rendering mode, view or image component.  The dialog ID and item ID must refer to symbol display control created with CreateSymDispCtrlN.  To show a blank SymbolDisplay control, use an empty string as the symbolName parameter.

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
| 3D          | 0        |
| 2D          | 1        |
| 2D Cut      | 2        |
| Not set     | 4        |

```pascal
PROCEDURE UpdateSymDispCtrlN(
				dialogID    : LONGINT;
				itemID      : LONGINT;
				symbolName  : STRING;
				view        : INTEGER;
				renderMode  : INTEGER;
				component   : INTEGER;
				scaleByZoom : BOOLEAN);
```

```python
def vs.UpdateSymDispCtrlN(dialogID, itemID, symbolName, view, renderMode, component, scaleByZoom):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|The ID of the dialog in which to create the control.|
|itemID|LONGINT|The item ID of the control.|
|symbolName|STRING|The name of the symbol to display.|
|view|INTEGER|The view in which to display the symbol.|
|renderMode|INTEGER|The render mode in which to display the symbol.|
|component|INTEGER|The image component.|
|scaleByZoom|BOOLEAN|Whether the sizing is done by zoom or layer scale.|

## See Also
VS Functions:
[CreateSymDispCtrlN](CreateSymDispCtrlN.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
