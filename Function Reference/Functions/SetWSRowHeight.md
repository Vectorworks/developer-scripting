# SetWSRowHeight

## Description
Sets the height of a row in the referenced worksheet.

SetWSRowHeight allows height to be set for a range of rows. To set the height of a single worksheet row, specify identical values for the top/bottom row range boundaries.

SetWSRowHeight also allows the lock state of a row to be set. Set 'TRUE' to lock or 'FALSE' to unlock the row height. If the height is locked, the row will not automatically resize to fit the contents of the cells when text is entered.

If the &quot;updatePalette'&quot; parameter is set to FALSE, the applied changes will not automatically be updated in the worksheet palette.

```pascal
PROCEDURE SetWSRowHeight(
				worksheet     : HANDLE;
				fromRow       : INTEGER;
				toRow         : INTEGER;
				height        : INTEGER;
				updatePalette : BOOLEAN;
				lockHeight    : BOOLEAN);
```

```python
def vs.SetWSRowHeight(worksheet, fromRow, toRow, height, updatePalette, lockHeight):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet|
|fromRow|INTEGER|Top row of row range|
|toRow|INTEGER|Bottom row of row range|
|height|INTEGER|Row height to be set (in pixels)|
|updatePalette|BOOLEAN|Worksheet palette update flag|
|lockHeight|BOOLEAN|Row height lock state to be set|

## Remarks
Note:
updatePalette - input - specifies whether or not to update the worksheet palette

lockHeight  - input - specifies whether or not to lock the height for the specified rows. If 'true' the height will be locked and the row will not automatically be resized when text is entered in a cell.

## Examples
#### VectorScript ####
```pascal
{Sets and locks the height of all rows from row 3 to row 9 to 22 pixels and update the changes in the worksheet palette }
SetWSRowHeight(sheet,3,9,22,TRUE,TRUE);
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks12.0

## Category
* [Worksheets](../Categories/Worksheets.md)
