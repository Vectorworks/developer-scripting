# Ln

## Description
Function Ln returns the natural logarithm of the specified value.

```pascal
FUNCTION Ln(v : REAL): REAL;
```

```python
def vs.Ln(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Numeric value for which to find the natural logarithm.|

## Examples
```pascal
		n := Ln (expR) / Ln (10);
{
writeln (' s2 = ',s1,'    nDigits+1-Len (s3) = ',nDigits+1-Len (s3),'    expR = ',expR,'    n = ',n);
}
```
```python
import vs

# Function Ln returns the natural logarithm of the specified value.
v = 1.0

value = vs.Ln(v)
vs.Message('Ln returned: ' + str(value))
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
