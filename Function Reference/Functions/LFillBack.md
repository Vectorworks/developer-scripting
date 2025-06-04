# LFillBack

## Description
Procedure LFillBack sets the background fill color for the active layer. RGB values are in the range of 0~65535.

```pascal
PROCEDURE LFillBack(color : LONGINT);
```

```python
def vs.LFillBack(color):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|color|LONGINT|RGB color component value.|

## Remarks
Sets the background fill color for the active layer.

[sd 8/14/98]

## Examples
==== VectorScript ====
```pascal
LFillBack(65535,0,39321);
```
==== Python ====
```python

```

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
