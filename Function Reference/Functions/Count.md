# Count

## Description
Counts all of the objects which match the search criteria.

```pascal
FUNCTION Count(c : CRITERIA): LONGINT;
```

```python
def vs.Count(c):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|c|CRITERIA|Search criteria.|

## Remarks
Undocumented is that criteria also accept the object type flag as parameter. The example above can also be written:

<code lang="pas">
CountValue := Count((FP=4)and(T=3)); { 3 is object type flag for 'Rectangle&amp' }
</code>

This is valid for all object types being assigned a name in the [[VS:Function Reference Appendix#Object Types|VectorScript Appendix]].

## Examples
==== VectorScript ====
```pascal
CountValue := Count((FP=4)and(T='Rect'));
{counts all rectangles with a fillpat index of 4}
```
==== Python ====
```python
CountValue = vs.Count("(FP=4)AND(T='Rect')")
# counts all rectangles with a fillpat index of 4
```

## Version
Availability: from All Versions

## Category
* [Criteria](../Categories/Criteria.md)
