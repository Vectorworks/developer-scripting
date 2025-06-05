# CreateLB

## Description
Creates a layout manager list browser control.

```pascal
PROCEDURE CreateLB(
				dialogID           : LONGINT;
				componentID        : LONGINT;
				widthInCharacters  : INTEGER;
				heightInCharacters : INTEGER);
```

```python
def vs.CreateLB(dialogID, componentID, widthInCharacters, heightInCharacters):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|id of the dialog that contains the list browser|
|componentID|LONGINT|id of the list browser control|
|widthInCharacters|INTEGER|the width of the control in characters|
|heightInCharacters|INTEGER|the height of the control in characters|

## Remarks
(*_c_*, 2022.01.22) : Here the former Vectorlab article: [[User:CBM-c-/VS-List_Browsers_part_1| List Browsers]]

## Examples
[ComplexDialogLayout4](examples/ComplexDialogLayout4.md)

## Version
Availability: from VectorWorks 11.0

## Category
* [Dialogs - Modern - Browser](../Categories/Dialogs%20-%20Modern%20-%20Browser.md)
