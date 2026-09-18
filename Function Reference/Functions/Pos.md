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
#### VectorScript ####
```pascal
Loc:=Pos('samp','A sample string');
```
#### Python ####
```python

```

```pascal
if Pos(' ', inBearingStr) > 0 then BEGIN {space delimited}
	while (ValidNumStr(Copy(inBearingStr, 1, 1), num)) & (Len(inBearingStr) > 0) do BEGIN
		prefix := Concat(prefix, Copy(inBearingStr, 1, 1));
		Delete(inBearingStr, 1, 1);
	END;

{parse the hole txtFoundH string in order to separate the KN No. from the rest and thus get its full prefix and suffix}
if ok then BEGIN
	{find the start and end position of the prefix-No.-suffix string in  the text.}
	temppos := Pos( noteNostr, GetText( H ) );
	{check whether the temppos is not 0, i.e. whether the keynote pref-num-suff is not in the text's object text at all}
	{if so - use the text's object text as a prefix! followed by ' '}
	if ( tempPos = 0 ) THEN BEGIN
		KNprefix := Concat( GetText( H ), ' ', KNprefix);

	IF recordOp = '='
		THEN tmpStr := '&((R in ['
		ELSE tmpStr := Concat('&(NOT(R in [');
	tmpStr := Concat(tmpStr, QStr(recordVa), ']))');
	IF Pos(tmpStr, SQL) = 0 THEN SQL := Concat(SQL, tmpStr);
END;
```
```python
result = vs.Pos('Example', 'Example')
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
