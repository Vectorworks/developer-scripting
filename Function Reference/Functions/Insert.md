# Insert

## Description
Procedure Insert will insert the specified string into a destination string.

```pascal
PROCEDURE Insert(
				source   : DYNARRAY[] of CHAR;
				VAR dest : DYNARRAY[] of CHAR;
				index    : INTEGER);
```

```python
def vs.Insert(source, index):
    return dest
```

## Parameters
|Name|Type|Description|
|---|---|---|
|source|DYNARRAY[] of CHAR|String to be inserted.|
|dest|DYNARRAY[] of CHAR|Destination string.|
|index|INTEGER|Position where string is to be inserted.|

## Examples
#### VectorScript ####
```pascal
theStr:='sample';
originalStr:='A string';
Insert(theStr,originalStr,3);
{inserts 'sample' into the target string}
```
#### Python ####
```python

```

```pascal
BEGIN
	Delete (newString, i, 1);
	Insert (CR, newString, i);
	j := k1 - i;
END

strtemp:=Num2Str(decPlace,labtemp);
nOfChars2:=Len(strtemp);
IF NOT(nOfChars2>=nOfChars) THEN BEGIN {pad leading zeros}
	WHILE (not(nOfChars2>=nOfChars)) DO BEGIN
		Insert(kZero,strtemp,1);
		nOfChars2:=Len(strtemp);
		END;

BEGIN
	Delete (gNutSize, i, 1);
	Insert (',', gNutSize, i);
END;
```
```python
result = vs.Insert(source, 1)
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
