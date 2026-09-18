# vstDrawCoordArcN

```pascal
PROCEDURE vstDrawCoordArcN(
				ptLeftTopX,ptLeftTopY : REAL;
				ptRghtBotX,ptRghtBotY : REAL;
				startAngle            : REAL;
				sweepAngle            : REAL);
```

```python
def vs.vstDrawCoordArcN(ptLeftTopX, ptLeftTopY, ptRghtBotX, ptRghtBotY, startAngle, sweepAngle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ptLeftTopX, ptLeftTopY|REAL|   |
|ptRghtBotX, ptRghtBotY|REAL|   |
|startAngle|REAL|   |
|sweepAngle|REAL|   |

## Examples
```pascal
vstDrawCoordArcN(1.0, 2.0, 0.5, 1.5, 3.0, 1.0);
```
```python
import vs

ptLeftTopX = 1.0
ptLeftTopY = 2.0
ptRghtBotX = 0.5
ptRghtBotY = 3.0
startAngle = 45.0
sweepAngle = 90.0

vs.vstDrawCoordArcN(ptLeftTopX, ptLeftTopY, ptRghtBotX, ptRghtBotY, startAngle, sweepAngle)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Tool Events](../Categories/Tool%20Events.md)
