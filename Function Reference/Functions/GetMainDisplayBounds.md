# GetMainDisplayBounds

## Description
Returns the bounds of the main display device (Macintosh Only).

```pascal
PROCEDURE GetMainDisplayBounds(
				VAR outTop    : INTEGER;
				VAR outLeft   : INTEGER;
				VAR outBottom : INTEGER;
				VAR outRight  : INTEGER);
```

```python
def vs.GetMainDisplayBounds():
    return (outTop, outLeft, outBottom, outRight)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outTop|INTEGER|   |
|outLeft|INTEGER|   |
|outBottom|INTEGER|   |
|outRight|INTEGER|   |

## Examples
```pascal
GetMainDisplayBounds(1, 2, 3, 10);
```
```python
import vs

# Returns the bounds of the main display device (Macintosh Only).
outTop, outLeft, outBottom, outRight = vs.GetMainDisplayBounds()
vs.Message('GetMainDisplayBounds returned: ' + str((outTop, outLeft, outBottom, outRight)))
```

## Version
Availability: from Vectorworks 2014

## Category
* [Utility](../Categories/Utility.md)
