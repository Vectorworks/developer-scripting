# GetTextSpace

## Description
Procedure GetTextSpace returns the line spacing of the referenced text object.

{| class="wikitable_c"
|+ Table - Text Spacing
! Leading !! Constant
|-
| Single space
| 2
|-
| 1 1/2 space
| 3
|-
| Double space
| 4
|}

```pascal
FUNCTION GetTextSpace(theText : HANDLE): INTEGER;
```

```python
def vs.GetTextSpace(theText):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|

## Version
Availability: from VectorWorks 8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
