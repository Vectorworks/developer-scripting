# GetWSCellNumberFormat

## Description
Returns the numeric formatting of a cell in the referenced worksheet.

Specific index values for numeric formats and accuracy are listed in the [Script Appendix](../Appendix/pages/Appendix%20E%20-%20Miscellaneous%20Selectors.md#record---worksheet-field-types).

```pascal
PROCEDURE GetWSCellNumberFormat(
				worksheet         : HANDLE;
				row               : INTEGER;
				column            : INTEGER;
				VAR style         : INTEGER;
				VAR accuracy      : INTEGER;
				VAR leaderString  : STRING;
				VAR trailerString : STRING);
```

```python
def vs.GetWSCellNumberFormat(worksheet, row, column):
    return (style, accuracy, leaderString, trailerString)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|row|INTEGER|Row of cell to be queried.|
|column|INTEGER|Column of cell to be queried.|
|style|INTEGER|Numeric format style index.|
|accuracy|INTEGER|Numeric accuracy / secondary format index.|
|leaderString|STRING|Leader string (where applicable).|
|trailerString|STRING|Trailer string (where applicable).|

## Remarks
([[User:CBM-c-|_c_]] 2022.05.09):

Number Format constants:

| Flag | Style                |
|------|----------------------|
| 0    | general              |
| 1    | decimal              |
| 2    | decimal with commas  |
| 3    | scientific           |
| 4    | fractional           |
| 5    | dimension            |
| 6    | angle                |
|      | For angle, the accuracy displays the angle format as in the pull-down menu list, whereby the choices 1 to 3 are degrees, the rest decimal. |
| 7    | date                 |
|      | For date, the accuracy displays the date format as in the pull-down menu. |
|      | Warning: the returned flags don't correspond to the pull-down indexes. See list below. The format depends on the system settings.<br>Example: flag 33 shows as dd/mm/yy in the pull-down menu, but resolves as dd.mm.yy in my German system.<br>Example: all (AM/PM) flags don't resolve in the German system and stay as 24h. |

| Flag | Date Format                | Example (sys dependent)         |
|------|---------------------------|---------------------------------|
| 9    | mmm-yy                    | Jan-04                          |
| 1    | m/d/yy                    | 1.24.04                         |
| 30   | mm/dd/yyyy                | 01.24.1904                      |
| 2    | m/d/yy hmm                | 1.24.04 21:34                   |
| 14   | m/d/yy hms (AM/PM)        | 1.24.04  21:34:14               |
| 8    | d-mmm                     | 24-Jan                          |
| 3    | d/m/yy                    | 24.1.04                         |
| 7    | d-mmm-yy                  | 24-Jan-04                       |
| 33   | dd/mm/yy                  | 24.01.04                        |
| 35   | dd/mm/yyyy                | 24.01.1904                      |
| 4    | d/m/yy hm                 | 24.1.04 21:34                   |
| 23   | d/m/yy hms (AM/PM)        | 24.1.04  21:34:14               |
| 34   | dd/mm/yy hms (AM/PM)      | 24.01.04  21:34:14              |
| 36   | dd/mm/yyyy hms (AM/PM)    | 24.01.1904  21:34:14            |
| 5    | yy/m/d                    | 04.1.24                         |
| 29   | yyyymmdd                  | 19040124                        |
| 31   | yyyy-mm-dd                | 1904-01-24                      |
| 6    | yy/m/d hm                 | 04.1.24 21:34                   |
| 28   | yy/m/d hms (AM/PM)        | 04.1.24  21:34:14               |
| 32   | yyyymmddhhmmss            | 19040124213414                  |
| 10   | h mm                      | 21:34                           |
| 11   | h mm ss                   | 21:34:14                        |
| 12   | h mm (AM/PM)              | 21:34                           |
| 13   | h mm ss (AM/PM)           | 21:34:14                        |
| 15   | day, month d, yyyy        | Sunday, January 24, 1904        |
| 16   | day, month d, yyyy hms (AM/PM) | Sunday, January 24, 1904  21:34:14 |
| 17   | dow, mmm d, yyyy          | Sun, Jan 24, 1904               |
| 18   | dow, mmm d, yyyy hms (AM/PM) | Sun, Jan 24, 1904  21:34:14   |
| 19   | day, d month yyyy         | Sunday, 24 January 1904         |
| 20   | day, d month yyyy hms (AM/PM) | Sunday, 24 January 1904  21:34:14 |
| 21   | dow, d mmm yyyy           | Sun, 24 Jan 1904                |
| 22   | dow, d mmm yyyy hms (AM/PM) | Sun, 24 Jan 1904  21:34:14    |
| 24   | day, yyyy month d         | Sunday, 1904 January 24         |
| 25   | day, yyyy month d hms (AM/PM) | Sunday, 1904 January 24  21:34:14 |
| 26   | dow, yyyy mmm d           | Sun, 1904 Jan 24                |
| 27   | dow, yyyy mmm d hms (AM/PM) | Sun, 1904 Jan 24  21:34:14    |

| Flag | Style            |
|------|------------------|
| 8    | boolean          |
| 11   | dimension area   |
| 12   | dimension volume |
| 13   | text             |
| 14   | percentage       |

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
