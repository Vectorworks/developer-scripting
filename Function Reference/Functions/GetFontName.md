# GetFontName

## Description
Function GetFontName converts a system font ID to a font name.

An integer ID with a value representing a font in the current operating system.

```pascal
FUNCTION GetFontName(fontID : INTEGER): STRING;
```

```python
def vs.GetFontName(fontID):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fontID|INTEGER|Font ID value.|

## Remarks
[[User:CBM-c-|_c_]] (2016.03.05): Upon passing an illegal font index it returns:
* before VW 2015: an empty string
* after VW 2015: the string "System font regular".
After VW 2015 you can use [[VS:GetFontListSize]] to fetch the count of installed fonts. Before that you had to check in both negative and positive direction the whole integer limit: from -32767 to +32767.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
str :STRING;
cnt :INTEGER;
BEGIN
FOR cnt := 0 to 10 DO str := Concat(str, Chr(13), GetFontName(cnt));
AlrtDialog(str);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	str = ''
	for cnt in range(0,10):
		str = vs.Concat(str, vs.Chr(13), vs.GetFontName(cnt))
	vs.AlrtDialog(str)
Example()
```

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
