# GetFontID

## Description
Function GetFontID converts the string name of an available font to a font ID which can be passed to other VectorScript routines.

```pascal
FUNCTION GetFontID(fontName : STRING): INTEGER;
```

```python
def vs.GetFontID(fontName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fontName|STRING|Name of installed font.|

## Remarks
returns -1 if the requested font is not available

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
VAR
str :STRING;
BEGIN
str := StrDialog('Enter the font name:', 'Arial');
AlrtDialog(Concat('The font ID is: ', GetFontID(str)));
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	str = vs.StrDialog('Enter the font name:', 'Arial')
	vs.AlrtDialog(vs.Concat('The font ID is: ', vs.GetFontID(str)))

Example()
```

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
