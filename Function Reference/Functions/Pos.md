# Pos

## Description
Function Pos searches for a specified substring contained within in a target string.

Pos returns the position of the substring. If the string is not found, 0 is returned.

```pascal
FUNCTION Pos(
				subStr : DYNARRAY[] of CHAR;
				str    : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.Pos(subStr, str):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|subStr|DYNARRAY[] of CHAR|Substring to be located.|
|str|DYNARRAY[] of CHAR|Target string.|

## Remarks
(Joel Sciamma, 2006.09.08): Pos returns the position of the ''first character'' of the ''first occurrence'' of the sub-string. The function is case-sensitive.

## Examples
==== VectorScript ====
```pascal
Loc:=Pos('samp','A sample string');
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
