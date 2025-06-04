# GetDrawingArea

## Description
Gets the drawing area of the active layer, as in Page Setup dialog. If Other is selected returns an empty string as outDrawingArea and true for outIsOther.If One Printer Page is Selected, returns empty string for outDrawingArea and true for outIsOnePrinterPage. Otherwise, returns the drawing area name (ISO A3, US ARCH A, etc.)

```pascal
PROCEDURE GetDrawingArea(
				VAR outDrawingArea      : STRING;
				VAR outIsOther          : BOOLEAN;
				VAR outIsOnePrintedPage : BOOLEAN);
```

```python
def vs.GetDrawingArea():
    return (STRING, outDrawingArea, outIsOther, outIsOnePrintedPage)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outDrawingArea|STRING|Returns the paper size name of the active layer, if it is found in the predefined paper sizes from DwgSizes-Universal.txt.|
|outIsOther|BOOLEAN|Returns true, if the paper size of the active layer is not one of the predefined sizes from DwgSizes-Universal.txt.|
|outIsOnePrintedPage|BOOLEAN|Returns true, if One Printer Page was selected in Page Setup dialog and the page area is the same as the selected from the printer page area.|

## Category
* [Layers](../Categories/Layers.md)
