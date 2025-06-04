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

## Version
Availability: from Vectorworks 2025

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
