# Num2Str

## Description
Function Num2Str converts a REAL value to a string and returns the value.

Parameter decPlace has a range of -1 to 9; if -1 is specified, the value will be returned in scientific notation.

```pascal
FUNCTION Num2Str(
				decPlace : INTEGER;
				v        : REAL): STRING;
```

```python
def vs.Num2Str(decPlace, v):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|decPlace|INTEGER|Number of decimal places.|
|v|REAL|Numeric value.|

## Remarks
[[User:CBM-c-|_c_]], 2015.05.23: You can also use [Concat](Concat.md) to convert numbers to strings, but it uses exclusively a dot "." as symbol for the decimal marker, because it outputs the number as seen from inside VS, I suppose. See further comments on the page [Concat](Concat.md).

The parameter *decPlace* can be the following values:

| Value    | Meaning                              | Sample                                 |
|----------|--------------------------------------|----------------------------------------|
| positive | round-up the value                   | 10.56 -> 10.6 (1 decimal place)        |
| 0        | round-up the value                   | 10.56 -> 11                            |
| -1       | Use scientific notation (9 decimals) | 10.56 -> 1.056000000e+001              |
| -2       | Use scientific notation (15 decimals)| 10.56 -> 1.056000000000000e+001        |

## Examples
#### VectorScript ####
```pascal
oldnumValue := 232.5148;
newStrValue := Num2Str(3, oldnumValue);
{ --> '232.515' if your system is american }
{ --> '232,515' if your system is metric }
```
#### Python ####
```python

```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
