# Ord

## Description
Function Ord returns the corresponding ASCII number of the specified character value. Parameter Ord specifies the character.

```pascal
FUNCTION Ord(v : CHAR): INTEGER;
```

```python
def vs.Ord(v):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|CHAR|ASCII character.|

## Remarks
The encoding used is Apple MacRoman. This leads to a number of troubles if you are on Windows and use characters above ASCII 128.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Main;
VAR
str :STRING;
cnt :INTEGER;
BEGIN
str := GetText(FSActLayer);
FOR cnt := 1 TO Len(str) DO
AlrtDialog(Concat(Ord(Copy(str, cnt, 1))));
END;
RUN(Main);
```
#### Python ####
```python

```

```pascal
		  ( fulltext[ ps ] = '/' ) |
		  ( fulltext[ ps ] = '\' ) |
		  ( fulltext[ ps ] = ':' ) |
		  ( fulltext[ ps ] = '-' ) |
		  ( Ord(fulltext[ ps ]) = 32 ) |
	      ( Ord(fulltext[ ps ]) = 9 )
		) THEN
BEGIN
	IF ( Ord(fulltext[ ps ]) = 32 ) | ( Ord(fulltext[ ps ]) = 9 ) THEN BEGIN
		noteIDend := TRUE;
		{save the indent size and font}
		while ( ps <= fulltextLen ) & (( Ord(fulltext[ ps ]) = 32 ) | ( Ord(fulltext[ ps ]) = 9 ) ) do BEGIN

BEGIN
CASE (ord(inStr)) OF
		65..89:		GetNextChar := UniChr(ord(inStr)+1);
		90:			GetNextChar := UniChr(65);
		97..121:	GetNextChar := UniChr(ord(inStr)+1);
		122:		GetNextChar := UniChr(97);
		OTHERWISE GetNextChar := inStr;

isLiteral := FALSE;
str := kEmpty;
WHILE (pos <= len(specStr)) DO BEGIN
	chr := copy(specStr, pos, 1);
	CASE ord(chr) OF
		kAmperAscii:BEGIN {stuff the string on the stack and increment}
				IF isLiteral THEN BEGIN {it's a literal string}
					TempStr[j] := str;
					IsLiteral := FALSE;
					END ELSE IF GoodFldName(hrec, str) THEN TempStr[j] := GetRField(hObj, recname, str) ELSE TempStr[j] := kFldErrStr;
				str := '';
				j := j+1;
```
```python
result = vs.Ord(v)
```

## See Also
VS Functions:
[Chr](Chr.md)

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
