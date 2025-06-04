# Locus

## Description
Procedure Locus creates a 2D locus object at the specified coordinate location.

```pascal
PROCEDURE Locus(pX,pY : REAL);
```

```python
def vs.Locus(p):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|p|REAL|Coordinate location of new locus.|

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
VAR
x, y :REAL;
BEGIN
HCenter(FSActLayer, x, y);
Locus(x, y);
END;
RUN(Example);
```
==== Python ====
```python
x = 100
y = 0
vs.Locus (x, y)
```

## Version
Availability: from All Versions

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
