# DBShowDBTableDlg

## Description
Show the specified database table dialog.

```pascal
FUNCTION DBShowDBTableDlg(
				database : STRING;
				table    : STRING): BOOLEAN;
```

```python
def vs.DBShowDBTableDlg(database, table):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|database|STRING|   |
|table|STRING|   |

## Remarks
([[User:Orso.b.schmid| Orso]], 2010 Sep. 27): It silently fails -returns FALSE- if the database or table names are invalid. If it succeeds a list of all available records (= entries, not to be confused with the term "record" in VW, often used instead of "format") in the chosen table is displayed for viewing, but you can't edit them. You can select a record, but there is no way to retrieve the selection. Is really view only.

## Version
Availability: from Vectorworks 2011

## Category
* [ODBC](../Categories/ODBC.md)
