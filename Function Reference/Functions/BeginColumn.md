# BeginColumn

## Description
Procedure BeginColumn creates a column object in a VectorWorks document using 2D object creation procedure calls to define the &quot;template&quot; for the column object. 

After specifying object procedure calls to define the column, you should call EndGroup to complete the column definition and create the actual object.

```pascal
PROCEDURE BeginColumn(columnDistance : REAL);
```

```python
def vs.BeginColumn(columnDistance):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|columnDistance|REAL|Height of column.|

## Remarks
BeginColumn takes the group of objects that follow, until there is an EndGroup, and converts them into a column with height equal to column distance.

[sd 8/17/98]

## Examples
==== VectorScript ====
```pascal
BeginColumn(12');
Oval(2',2',6',6');
EndGroup;
```
==== Python ====
```python
vs.BeginColumn(12*12)
vs.Oval(2*12,2*12,6*12,6*12)
vs.EndGroup()
```

## Version
Availability: from MiniCAD7.0

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
