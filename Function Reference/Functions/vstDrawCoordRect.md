# vstDrawCoordRect

```pascal
PROCEDURE vstDrawCoordRect(
				ptLeftTopX, ptLeftTopY : REAL;
				ptRghtBotX, ptRghtBotY : REAL);
```

```python
def vs.vstDrawCoordRect(ptLeftTopX, ptLeftTopY, ptRghtBotX, ptRghtBotY):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|ptLeftTopX, ptLeftTopY|REAL|   |
|ptRghtBotX, ptRghtBotY|REAL|   |

## Examples
```pascal
vstDrawCoordRect(1.0, 2.0, 0.5, 1.5);
```
```python
import vs

ptLeftTopX = 1.0
ptLeftTopY = 2.0
ptRghtBotX = 0.5
ptRghtBotY = 3.0

vs.vstDrawCoordRect(ptLeftTopX, ptLeftTopY, ptRghtBotX, ptRghtBotY)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Tool Events](../Categories/Tool%20Events.md)
