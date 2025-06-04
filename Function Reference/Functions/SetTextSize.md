# SetTextSize

## Description
Procedure SetTextSize sets the text size of a specified substring in the referenced text object. Parameters Start and Count specify the substring start position and substring length. Parameter Size specifies the size (in points) to be assigned to the substring.

```pascal
PROCEDURE SetTextSize(
				objectHd : HANDLE;
				Start    : INTEGER;
				Count    : INTEGER;
				Size     : REAL);
```

```python
def vs.SetTextSize(objectHd, Start, Count, Size):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHd|HANDLE|Handle to text object.|
|Start|INTEGER|Start position in text string.|
|Count|INTEGER|Length of substring.|
|Size|REAL|Text size setting for substring.|

## Remarks
The size parameter was previously an integer, but is now a floating point value. [9/14/98 - PCP]

## Examples
==== VectorScript ====
```pascal
SetTextSize(HandleToText,0,5,24);
{set the first five characters of the referenced text string to 24 point text}
```
==== Python ====
```python

```

## Version
Availability: from MiniCAD6.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
