# SetFPat

## Description
Procedure SetFPat sets the fill pattern of the referenced object.

To apply a bitmap fill pattern, use positive value corresponding to the index  of the bitmap pattern.  To apply a vector fill pattern, use the negative of the vector fill index (index * -1).

Fill patterns and their associated constants can be found in the [[VS:Function Reference Appendix#Fill Patterns|VectorScript Appendix]].

```pascal
PROCEDURE SetFPat(
				h           : HANDLE;
				fillPattern : LONGINT);
```

```python
def vs.SetFPat(h, fillPattern):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|
|fillPattern|LONGINT|Fill index value.|

## Examples
dSurface}}

## Version
Availability: from All Versions

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
