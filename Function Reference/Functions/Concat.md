# Concat

## Description
Function Concat combines, or concatenates, all the specified parameters in order and returns the resultant string.

```pascal
FUNCTION Concat(txt : DYNARRAY[] of CHAR): DYNARRAY[] of CHAR;
```

```python
def vs.Concat(txt):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|txt|DYNARRAY[] of CHAR|   |

## Remarks
[[User:CBM-c-|_c_]], 2015.05.23: You can use [[VS:Concat]] to convert numbers to strings, but it uses exclusively a dot "." as symbol for the decimal marker, it outputs the number as seen from inside VS. See the table below for a list of routines formatting according to your system's settings.
{| class="wikitable"
|+ Decimal marker symbol usage
! Metric: ',' !!  American '.'
|-
| 
: 100,123
|
: 100.123
|-
! Formatting routines: !!  Non formatting routines:
|-
| 
: [[VS:Num2Str]], [[VS:Num2StrF]], [[VS:Angle2Str]], [[VS:Area2Str]], [[VS:Volume2Str]]
: <code>Num2Str(3, 100.123) { --> 100,123 on metric systems } </code>
: <code>Num2Str(3, 100.123) { --> 100.123 on American systems } </code>
|
: [[VS:Concat]]
: <code>Concat(100.123) { --> 100.123 on any system } </code>
|}

## Examples
#### VectorScript ####
```pascal
AlrtDialog(Concat('A', 'sample', 'string'));
```
#### Python ####
```python
vs.AlrtDialog(vs.Concat('A', 'sample', 'string'))
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
