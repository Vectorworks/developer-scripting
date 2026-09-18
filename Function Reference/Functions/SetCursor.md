# SetCursor

## Description
Procedure SetCursor changes the appearance of the screen cursor.

* Table - Cursor Styles

| Cursor Style | cursor parameter value |
|--------------|------------------------|
| Large Cross | 1307 |
| Small Cross | 1310 |
| Watch | 1311 |
| Text Bar | 1312 |
| Arrow | 1309 |
| Hand | 1308 |

```pascal
PROCEDURE SetCursor(cursor : INTEGER);
```

```python
def vs.SetCursor(cursor):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|cursor|INTEGER|Cursor style setting.|

## Examples
#### VectorScript ####
```pascal
SetCursor(LgCrossC);
```
#### Python ####
```python

```

```pascal
BEGIN
	SetCursor (WatchC);

MoveTo (originX, originY);
Relative;
AddVertex ((unitLen/2), 0, kSmooth, 0);
AddVertex (-(unitLen/2), thickness, kSmooth, 0);
SetCursor (WatchC);

SetCursor (WatchC);
{*/// None ///*}
IF folderName = GetPlugInString (3033) THEN traverseSymbolRoot
```
```python
vs.SetCursor(cursor)
```

## Version
Availability: from All Versions

## Category
* [User Interactive](../Categories/User%20Interactive.md)
