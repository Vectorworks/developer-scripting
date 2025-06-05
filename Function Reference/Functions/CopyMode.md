# CopyMode

## Description
Procedure CopyMode sets the transfer mode for the active design layer.  If a sheet layer is active, the procedure has no effect.

*Transfer Modes*

**Table - Transfer Modes**

| Transfer Mode   | Index Value |
|-----------------|-------------|
| Copy            | 8           |
| OR              | 9           |
| XOR             | 10          |
| BIC             | 11          |
| Inverse Copy    | 12          |
| Inverse OR      | 13          |
| Inverse XOR     | 14          |
| Inverse BIC     | 15          |

The design layer will only be imaged with the transfer mode on systems which support it, like Windows.  Setting the transfer mode to a mode other than Copy (i.e. 8, Paint mode), when the current layer transparency percentage is 0, will also automatically change the layer transparency percentage to 50.  Similarly, setting the transfer mode to Copy, when the current layer transparency percentage is greater than 0, will also automatically change the layer transparency percentage to 0.  This is to approximately preserve the appearance of the layer on systems that don't support transfer modes, like Quartz on the Mac.

```pascal
PROCEDURE CopyMode(mode : INTEGER);
```

```python
def vs.CopyMode(mode):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|mode|INTEGER|Mode index value.|

## Remarks
Sets the layer transfer mode for the actlve layer.

Valid mode values are:
8 - Copy
9 - OR
10 - XOR
11 - BIC
12 - Inverse Copy
13 - Inverse OR
14 - Inverse XOR
15 - Inverse BIC

This procedure may also set the layer transparency to approximate the given transfer mode on systems that don't support transfer modes.

## See Also
VS Functions:
[SetLayerTransparency](SetLayerTransparency.md)

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
