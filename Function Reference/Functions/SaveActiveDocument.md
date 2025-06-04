# SaveActiveDocument

## Description
Saves a file with out presenting dialogs

```pascal
FUNCTION SaveActiveDocument(filePath : STRING): LONGINT;
```

```python
def vs.SaveActiveDocument(filePath):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|filePath|STRING|   |

## Remarks
([[User:CBM-c-|_c_]], 2014.09.20): Introduced by VW 10 (not 2010!), made public for VW 2014. This is predestinated to usage with Applescript, since it's dialog-free. Probably created for that precise usage, since I am not aware of a single command in the main application that could be using it.

It corresponds to "save as" but without dialog. Saving on the same file path name doesn't work (returns -1), only if the file path is different (returns 0).

## Examples
```pascal
PROCEDURE Test;
VAR
	temp_l	: LONGINT;
BEGIN
	{ save the current file in the application folder }
	temp_l := SaveActiveDocument(concat(getFolderPath(1), 'try.mcd'));
END;
Run(Test); { _c_ }
```

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
