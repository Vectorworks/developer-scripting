# SubString

## Description
Function SubString splits the Text string using characters specified in the var "Delimiter" and returns the token located at the Index position. <BR>
The first token is located at index 1. <BR>
If there is an error the function returns ''(empty string).<BR>
If index is less than 1 or greater than max number of tokens the function returns ''(empty string).

```pascal
FUNCTION SubString(
				text      : DYNARRAY[] of CHAR;
				delimiter : STRING;
				index     : INTEGER): DYNARRAY[] of CHAR;
```

```python
def vs.SubString(text, delimiter, index):
    return DYNARRAY[] of CHAR
```

## Parameters
|Name|Type|Description|
|---|---|---|
|text|DYNARRAY[] of CHAR|   |
|delimiter|STRING|   |
|index|INTEGER|   |

## Examples
```python
middleStr := SubString('Left;Middle;Right', ';', 2);
```

```pascal
BEGIN
	flString := SubString(lString, ';', j);
	selObjsflStrings[selObjsOffsets[i] + j] := flString;

BEGIN
	paramOrderString := GetRField(legenHandle, kLegendRec, kParamsStackOrderFld);
	orderNum := 1;
	stringNum := 1;
	paramUniName := SubString(paramOrderString, kOrderDelimiter, stringNum);
	WHILE paramUniName <> '' DO
		BEGIN
		index := FindParmListID(paramUniName,1);
		IF index <> 0 THEN

i := 1;
tempStr := SubString(choiceStr, kSep, i);
WHILE ( tempStr <> '' ) DO BEGIN
	IF NOT ValidNumStr(tempStr, choiceReal) THEN EnableItem(dialogIDCSO, kOK, FALSE);
	i := i+1;
	tempStr:=SubString(choiceStr, kSep, i);
```
```python
import vs

# Function SubString splits the Text string using characters specified in the
# var "Delimiter" and returns the token located at the Index position.
text = 'Example text'
delimiter = 'Example'
index = 1

text = vs.SubString(text, delimiter, index)
vs.Message('SubString returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Strings](../Categories/Strings.md)
