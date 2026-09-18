# ReplaceText

## Description
Procedure ReplaceText replace the oldText with the newText of the referenced text object.

```pascal
PROCEDURE ReplaceText(
				objectHd   : HANDLE;
				oldText    : STRING;
				newText    : STRING;
				replaceAll : BOOLEAN;
				isCaseSens : BOOLEAN);
```

```python
def vs.ReplaceText(objectHd, oldText, newText, replaceAll, isCaseSens):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|oldText|STRING|Old text string value.|
|newText|STRING|New text string value.|
|replaceAll|BOOLEAN|Flag whether to replace all oldTexts or first found text.|
|isCaseSens|BOOLEAN|Flag whether to be case sensitive.|

## Examples
```python
ReplaceText(hText,'Old text', 'New', TRUE, FALSE);
```

```pascal
2:	BEGIN
	SearchTxtObj := TRUE;
	gStop := TRUE;
	ReplaceStr(FldStr,gFindString,gReplString,gCase);
	ReplaceText(HObj, gFindString, gReplString, FALSE, gCase);
	GOTO 97;
	END;
```
```python
import vs

# Procedure ReplaceText replace the oldText with the newText of the
# referenced text object.
objectHd = vs.FSActLayer()  # handle to the first selected object on the active layer
oldText = 'Example text'
newText = 'Example text'
replaceAll = True
isCaseSens = True

vs.ReplaceText(objectHd, oldText, newText, replaceAll, isCaseSens)
```

## Version
Availability: from Vectorworks 2025

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
