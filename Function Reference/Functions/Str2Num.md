# Str2Num

## Description
Function Str2Num returns the specified string as a numeric value.

```pascal
FUNCTION Str2Num(s : STRING): REAL;
```

```python
def vs.Str2Num(s):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s|STRING|Source string.|

## Remarks
\_c\_ (2017.11.18): Please be careful with overriding standard routines. I change the name of this routine into MyStr2Num. Thus it won't override the standard Str2Num.

Author unknown, changed so that it doesn't override the standard routine:
```pascal
FUNCTION MyStr2Num(str :STRING) :REAL;
{This is more robust than Str2Num because it handles unit marks in the string,
while the built-in FUNCTION does not. Returns zero
if it fails, which of course does not unambiguously
indicate failure, but it's the same thing that Str2Num 
returns on failure (without the warning). If you need
to know whether or not the FUNCTION succeeded, you
shouldn't be using Str2Num, but ValidNumStr instead.}
VAR
num :REAL;
BEGIN
MyStr2Num := 0;
IF ValidNumStr(str, num) THEN MyStr2Num := num;
END;
```

## Examples
#### VectorScript ####
```pascal
numValue:=Str2Num('235.44');
```
#### Python ####
```python

```

## See Also
VS Functions:
[ValidNumStr](ValidNumStr.md)

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
