# Chr

## Description
Function Chr returns the ASCII character corresponding to the specified numeric code. The ASCII code value must be between 1 and 255.

```pascal
FUNCTION Chr(v : INTEGER): CHAR;
```

```python
def vs.Chr(v):
    return CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|INTEGER|ASCII numeric identifier code.|

## Remarks
Here;s the ASCII table for the lower 128...

[[Image:ascii_lower.gif]]

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
cnt :INTEGER;
str :STRING;
BEGIN
FOR cnt := 128 TO 255 DO BEGIN
str := Concat(str, Chr(cnt));
IF cnt MOD 32 = 0 THEN str := Concat(str, Chr(13));
END;
AlrtDialog(str);
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	str = ""
	for cnt in range(128, 255):
		str = str + vs.Chr(cnt)
		if cnt % 32 == 0:
			str = str + vs.Chr(13)
	vs.AlrtDialog(str)
Example()
```

## See Also
VS Functions:
[Ord](Ord.md)

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
