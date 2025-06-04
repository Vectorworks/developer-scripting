# Centroid

## Description
Returns the centroid of the object. Returns false if an unsupported object type is supplied.

```pascal
FUNCTION Centroid(
				h     : HANDLE;
				VAR x : REAL;
				VAR y : REAL): BOOLEAN;
```

```python
def vs.Centroid(h):
    return (BOOLEAN, x, y)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|x|REAL|   |
|y|REAL|   |

## Remarks
([[User:CBM-c-|_c_]] 2016.04.18): This returns mm, so convert the values into current units:
<code lang="vss">
IF Centroid(h, c.x, c.y) THEN BEGIN
        { centroid returns mm }
        c.x := c.x * GetPrefReal(152) / 25.4;
	c.y := c.y * GetPrefReal(152) / 25.4;
END;

## Version
Availability: from Vectorworks 2014

## Category
* [Graphic Calculation](../Categories/Graphic%20Calculation.md)
