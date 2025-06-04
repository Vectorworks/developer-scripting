# FillPat

## Description
Procedure FillPat sets the active fill pattern for the document. Any objects created after a calling this procedure will use the specified fill pattern.

Fill patterns and their associated constants can be found in the [[VS:Function Reference Appendix#Fill Patterns|VectorScript Appendix]].

```pascal
PROCEDURE FillPat(patNumber : LONGINT);
```

```python
def vs.FillPat(patNumber):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|patNumber|LONGINT|Index of fill pattern to be set as document default.|

## Examples
#### VectorScript ####
```pascal
Rect(0,0,2,2);
FillPat(21);
Rect(2,2,4,4);
```
#### Python ####
```python
vs.Rect(0,0,2,2)
vs.FillPat(21)
vs.Rect(2,2,4,4)
```

## Version
Availability: from All Versions

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
