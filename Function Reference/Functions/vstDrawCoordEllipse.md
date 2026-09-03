# vstDrawCoordEllipse

```pascal
PROCEDURE vstDrawCoordEllipse(
				ptLeftTopX,ptLeftTopY : REAL;
				ptRghtBotX,ptRghtBotY : REAL);
```

```python
def vs.vstDrawCoordEllipse(ptLeftTopX, ptLeftTopY, ptRghtBotX, ptRghtBotY):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ptLeftTop, ptLeftTop|REAL|   |
|ptRghtBotX, ptRghtBotY|REAL|   |

## Examples
```pascal
vstDrawCoordEllipse(1.0, 2.0, 0.5, 1.5);
```
```python
import vs

ptLeftTopX = 1.0
ptLeftTopY = 2.0
ptRghtBotX = 0.5
ptRghtBotY = 3.0

vs.vstDrawCoordEllipse(ptLeftTopX, ptLeftTopY, ptRghtBotX, ptRghtBotY)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Tool Events](../Categories/Tool%20Events.md)
