# UprString

## Description
Procedure UprString converts all characters in the specified string to upper case.

```pascal
PROCEDURE UprString(VAR str : DYNARRAY[] of CHAR);
```

```python
def vs.UprString(str):
    return str
```

## Parameters
|Name|Type|Description|
|---|---|---|
|str|DYNARRAY[] of CHAR|Source string.|

## Examples
#### VectorScript ####
```pascal
revisedString := 'vectorworks';
UprString(revisedString);
{Sets revisedString equal to 'VECTORWORKS'}
```
#### Python ####
```python

```

```pascal
BEGIN
	GetResourceString( gLocTrue, 2103, 6 );
	GetResourceString( glocFalse, 2103, 7 );
	UprString( gLocTrue  );
	UprString( gLocFalse );
END;

lenFind := Len(FStr);
tempstr := str;
IF ((lenFind > 0) & (lenStr > 0)) THEN BEGIN
	IF NOT(caseSens) THEN BEGIN
		UprString(tempstr);UprString(FStr);
		END;

IF (recHandle <> NIL) THEN
	FOR i := 1 TO numfields(recHandle) DO BEGIN
	tmpinput := fldname;
	tmpstr := getfldname(recHandle, i);
	Uprstring(tmpstr);
	Uprstring(tmpinput);
	IF (tmpstr = tmpinput) THEN GoodFldName := TRUE;
END;
```
```python
def UCase( str ):
	result = vs.UprString( str )
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
