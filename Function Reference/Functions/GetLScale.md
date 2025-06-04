# GetLScale

## Description
Function GetLScale returns the scale of the referenced layer.

```pascal
FUNCTION GetLScale(h : HANDLE): REAL;
```

```python
def vs.GetLScale(h):
    return REAL
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|

## Remarks
''Joel Sciamma 2006.02.20'': Returns 200 for 1:200, 1 for 1:1 and 0.5 for 2x

## Examples
==== VectorScript ====
```pascal
LayerScale := GetLScale(LayerHandle);
```
==== Python ====
```python
LayerScale  = vs.GetLScale(vs.ActLayer())
```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
