# Sqrt

## Description
Function Sqrt returns the square root of the specified value.

```pascal
FUNCTION Sqrt(v : REAL): REAL;
```

```python
def vs.Sqrt(v):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|REAL|Value for which to find the square root.|

## Remarks
Be aware that in VS, a number can be less than zero, even if it is equal to zero. The following script generates a "square root of a negative number" error...
```pascal
PROCEDURE GenerateError;
VAR
temp_r :REAL;
BEGIN
temp_r := -.00000000000000000000000000000000000001;
IF temp_r = 0 THEN Message(sqrt(temp_r));
END;
RUN(GenerateError);
```

## Version
Availability: from All Versions

## Category
* [Math - General](../Categories/Math%20-%20General.md)
