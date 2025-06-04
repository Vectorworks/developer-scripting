# Duplicate

## Description
Procedure Duplicate copies the currently selected objects and moves them the specified offset distance.

```pascal
PROCEDURE Duplicate(offset : REAL);
```

```python
def vs.Duplicate(offset):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|offset|REAL|Offset value.|

## Remarks
If user has "Offset Duplications" turned off, Duplicate ignores the x/y.

## Examples
#### VectorScript ####
```pascal
Rect(0,1,1,0);
Duplicate(2,0);
{duplicates the rectangle 2 units right of the original}
```
#### Python ####
```python
vs.Rect(0,1,1,0)
vs.Duplicate(2,0)
#{duplicates the rectangle 2 units right of the original}
```

## Version
Availability: from All Versions

## Category
* [Object Editing](../Categories/Object%20Editing.md)
