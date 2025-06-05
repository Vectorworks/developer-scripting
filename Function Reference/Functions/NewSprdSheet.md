# NewSprdSheet

## Description
Procedure NewSprdSheet creates a new worksheet in a VectorWorks document.

```pascal
PROCEDURE NewSprdSheet(
				name                : STRING;
				locationX,locationY : REAL;
				rows                : INTEGER;
				columns             : INTEGER;
				showOnDrawing       : BOOLEAN;
				openAfterCreate     : BOOLEAN);
```

```python
def vs.NewSprdSheet(name, location, rows, columns, showOnDrawing, openAfterCreate):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|Name of new worksheet.|
|location|REAL|Insertion point of worksheet.|
|rows|INTEGER|Number of rows.|
|columns|INTEGER|Number of columns.|
|showOnDrawing|BOOLEAN|Display worksheet in document.|
|openAfterCreate|BOOLEAN|Open worksheet after creation.|

## Examples
#### VectorScript ####
```pascal
NewSprdSheet('Window Schedule', 12, 24, 5, 8, TRUE, FALSE);
```
#### Python ####
```python

```

## See Also
[CreateWS | CreateWS](CreateWS%20| CreateWS.md)

## Version
NewSprdSheet is obsolete as of VectorWorks 9.0, see new [ CreateWS](CreateWS.md)

Availability: from VectorWorks 8.0

## Category
* [Worksheets](../Categories/Worksheets.md)
