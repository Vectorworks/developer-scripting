# OvalN

## Description
Creates an oval with the specified bounds.

```pascal
PROCEDURE OvalN(
				orginX,orginY         : REAL;
				directionX,directionY : REAL;
				width                 : REAL;
				height                : REAL);
```

```python
def vs.OvalN(orgin, direction, width, height):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|orgin|REAL|   |
|direction|REAL|   |
|width|REAL|   |
|height|REAL|   |

## Examples
==== VectorScript ====
```pascal
PROCEDURE Example;
BEGIN
OvalN(0, 0, 1, 0, 1, 1);
END;
RUN(Example);
```
==== Python ====
```python

```

## Version
Availability: from VectorWorks13.0

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
