# UniChr

## Description
Returns the UTF-8 character corresponding to the specified Unicode code point.

```pascal
FUNCTION UniChr(v : LONGINT): STRING;
```

```python
def vs.UniChr(v):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|LONGINT|A Unicode code point. The code point value must be in decimal (base ten).|

## Examples
```pascal
BEGIN
CASE (ord(inStr)) OF
		65..89:		GetNextChar := UniChr(ord(inStr)+1);
		90:			GetNextChar := UniChr(65);
		97..121:	GetNextChar := UniChr(ord(inStr)+1);
		122:		GetNextChar := UniChr(97);
		OTHERWISE GetNextChar := inStr;

crChar := Chr (kCRChar);
degreeC := UniChr (kDegreeUniChar);

crChar := Chr (kCRChar);
degreeC := UniChr (kDegreeUniChar);
diaC := Chr (kDiaChar);
```
```python
import vs

# Returns the UTF-8 character corresponding to the specified Unicode code point.
v = 1

text = vs.UniChr(v)
vs.Message('UniChr returned: ' + str(text))
```

## See Also
VS Functions:
[Chr](Chr.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Strings](../Categories/Strings.md)
