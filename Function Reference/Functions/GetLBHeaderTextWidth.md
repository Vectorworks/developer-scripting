# GetLBHeaderTextWidth

## Description
Produces the width in pixels that will show the given string without truncation in a listbrowser column header.  This will provide a guaranteed appropriate width for InsertLBColumn.

```pascal
FUNCTION GetLBHeaderTextWidth(
				className        : STRING;
				allowForSortIcon : BOOLEAN): INTEGER;
```

```python
def vs.GetLBHeaderTextWidth(className, allowForSortIcon):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|   |
|allowForSortIcon|BOOLEAN|   |

## Remarks
[[User:CBM-c-|_c_]] (2021.01.19): From [[User:Tui| Tui]], this routine crashes VW 2021 on Window, not on Mac (tested VW 2021 SP2)

## Version
Availability: from Vectorworks 14.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
