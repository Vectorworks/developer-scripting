# Delete

## Description
Procedure Delete removes a substring from the specified source string.

```pascal
PROCEDURE Delete(
				VAR source : DYNARRAY[] of CHAR;
				index      : INTEGER;
				count      : INTEGER);
```

```python
def vs.Delete(source, index, count):
    return source
```

## Parameters
|Name|Type|Description|
|---|---|---|
|source|DYNARRAY[] of CHAR|Source string.|
|index|INTEGER|Start position in text string.|
|count|INTEGER|Length of substring.|

## Remarks
Per Raymond Mullin, on the VS list, there is a bug in Delete that prevents it from getting the last character if the string is a dynarray of char. The following test script should leave T = '', but it leaves T = '7'.

```pascal
PROCEDURE DeleteTest;
VAR
T :DYNARRAY [] of CHAR;
BEGIN
T := '1234567';
Delete(T, 1, 7);
Message('T: ', T);
END;
RUN(DeleteTest);
```

## Examples
#### VectorScript ####
```pascal
theStr:='A sample string';
Delete(theStr,3,7);
{deletes 'sample' from the string value}
```
#### Python ####
```python
def DeleteTest():
	T = '1234567'
	T = vs.Delete(T, 1, 7)
	vs.Message('T: ', T)

DeleteTest()
```

```pascal
prefix := '';
while (not ValidNumStr(Copy(inBearingStr, 1, 1), num)) & (Len(inBearingStr) > 0) do BEGIN
	prefix := Concat(prefix, Copy(inBearingStr, 1, 1));
	Delete(inBearingStr, 1, 1);
	format := 'bearing';
END;

BEGIN
	IF bConvKeyNote & GetKeyNoteData( textFoundH ) then BEGIN
		if Copy( KNprefix, Len(KNprefix), 1) = ' ' then BEGIN
			Delete(KNprefix, Len(KNprefix), 1);
			if ( KNsuffix = '' ) & ( KNprefix = GetText( textFoundH ) ) then BEGIN
				IF not ValidNumStr( GetText( textFoundH ), t_real ) THEN BEGIN
					TextOrigin(0,0);
					CreateText(Concat(' ', KNNoteNo));

BEGIN
{Returns the date string up to the third space character}
pos1 := Pos (' ', input);
dummy1 := Copy(input, 1, pos1);
Delete(input, 1, pos1);
pos1 := Pos (' ', input);
dummy1 := concat(dummy1, Copy(input, 1, pos1));
Delete(input, 1, pos1);
pos1 := Pos (' ', input);
```
```python
import vs

# Procedure Delete removes a substring from the specified source string.
source = 'Example'
index = 1
count = 5

result = vs.Delete(source, index, count)
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
