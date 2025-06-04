# FPenColorByClass

## Description
Function FPenColorByClass returns whether the global attributes are set to use the pen colors of the default class.

```pascal
FUNCTION FPenColorByClass : BOOLEAN;
```

```python
def vs.FPenColorByClass():
    return BOOLEAN
```

## Remarks
Returns whether the global attributes are set to use the pen colors of the default class.
[sd 8/19/98]

## Examples
==== VectorScript ====
```pascal
useClassPenColor:=FPenColorByClass;
```
==== Python ====
```python
useClassPenColor = vs.FPenColorByClass()
```

## Version
Availability: from VectorWorks8.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
