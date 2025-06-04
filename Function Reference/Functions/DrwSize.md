# DrwSize

## Description
Procedure DrwSize sets the drawing area of the document.

```pascal
PROCEDURE DrwSize(
				rows    : INTEGER;
				columns : INTEGER);
```

```python
def vs.DrwSize(rows, columns):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|rows|INTEGER|Number of sheet rows comprising total document area.|
|columns|INTEGER|Number of sheet columns comprising total document area.|

## Examples
==== VectorScript ====
```pascal
DrwSize(2,3);
{sets the drawing size to 2 x 3 sheets}
```
==== Python ====
```python
vs.DrwSize(2,3)
```

## Version
Availability: from All Versions

## Category
* [Document Settings](../Categories/Document%20Settings.md)
