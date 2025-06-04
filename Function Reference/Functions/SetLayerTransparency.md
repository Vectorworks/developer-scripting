# SetLayerTransparency

## Description
Procedure SetLayerTransparency assigns a transparency percentage value to the active design layer.  If a sheet layer is active, the procedure has no effect.  The transparency value must be between 0.0 and 100.0, inclusive.

The design layer will only be imaged with transparency on systems which support it, like Quartz on the Mac.  Setting the transparency to a value greater than 0, when the current transfer mode is Copy (i.e. 8, Paint mode), will also automatically change the layer transfer mode to OR (i.e. 9, Overlay).  Similarly, setting the transparency to 0, when the current transfer mode is not set to Copy, will also automatically change the layer transfer mode to Copy.  This is to approximately preserve the appearance of the drawing when imaging on systems that don't support transparency, like Windows.

```pascal
PROCEDURE SetLayerTransparency(transparency : REAL);
```

```python
def vs.SetLayerTransparency(transparency):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|transparency|REAL|   |

## Remarks
Sets the transparency percentage of the active design layer
Valid transparency values are between 0.0 and 100.0, inclusive.
This procedure may also set the layer transfer mode to approximate the given transparency on systems that don't support transparency.

## See Also
VS Functions:
[CopyMode](CopyMode.md)

## Version
Availability: from VectorWorks12.0

## Category
* [Layers](../Categories/Layers.md)
