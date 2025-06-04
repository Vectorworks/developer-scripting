# HasDim

## Description
Function HasDim returns TRUE if a line or arc object has dimension text associated with it, otherwise it returns FALSE.

```pascal
FUNCTION HasDim(h : HANDLE): BOOLEAN;
```

```python
def vs.HasDim(h):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
==== VectorScript ====
```pascal
isDimension:=HasDim(HandleToObject);
```
==== Python ====
```python
vs.Message(vs.HasDim(vs.FSActLayer()))
```

## Version
Availability: from All Versions

## Category
* [Dimensions](../Categories/Dimensions.md)
