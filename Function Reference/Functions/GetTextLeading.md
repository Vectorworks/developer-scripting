# GetTextLeading

## Description
Procedure GetTextLeading returns the custom leading value(in points) of the referenced text object.

```pascal
FUNCTION GetTextLeading(theText : HANDLE): REAL;
```

```python
def vs.GetTextLeading(theText):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theText|HANDLE|Handle to text object.|

## Remarks
If a custom value was not set, this returns -1.0.

## Version
Availability: from VectorWorks8.0

## Category
* [Objects - Text](../Categories/Objects%20-%20Text.md)
