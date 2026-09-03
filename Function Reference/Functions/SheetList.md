# SheetList

## Description
Returns the name of the saved view specified by index.

```pascal
FUNCTION SheetList(sheetIndex : INTEGER): STRING;
```

```python
def vs.SheetList(sheetIndex):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|sheetIndex|INTEGER|Index of the sheet|

## Examples
```pascal
For TmpCnt := 1 to gNumSheets2 DO
	gSheetList2 [TmpCnt] := SheetList (TmpCnt);

Begin
CurSheetName := SheetList(CurSheetNum);

BEGIN
	oldSheetName := SheetList (i);
	instance := getSheetInstance (oldSheetName);
	index := getSheetListIndex (gOldSheetStd, Indiv2TYPE (oldSheetName), gNumSheets);
	IF index > 0 THEN
	BEGIN
```
```python
import vs

# Returns the name of the saved view specified by index.
sheetIndex = 1

text = vs.SheetList(sheetIndex)
vs.Message('SheetList returned: ' + str(text))
```

## See Also
VS Functions:
[SheetNum](SheetNum.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
