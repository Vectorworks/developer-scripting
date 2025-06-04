# TextFace

## Description
Procedure TextFace sets the active text style of a VectorWorks document.

The text style may be one or a combination of the available styles, and should be enclosed in brackets. To specify multiple styles, each style should be separated by a comma.

```pascal
PROCEDURE TextFace(s : TEXTSTYLE);
```

```python
def vs.TextFace(s):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|s|TEXTSTYLE|Style setting for document.|

## Remarks
Make sure the docs indicate that the face must appear in set notation - check it out [PCP]

## Examples
==== VectorScript ====
```pascal
TextFace([Italic]);
{set the active text style to Italic}

TextFace([Bold,Outline]);
{set the active text style to bold outline}
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
