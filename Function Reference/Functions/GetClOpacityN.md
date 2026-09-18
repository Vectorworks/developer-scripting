# GetClOpacityN

```pascal
PROCEDURE GetClOpacityN(
				strClassName       : STRING;
				VAR outFillOpacity : INTEGER;
				VAR outPenOpacity  : INTEGER);
```

```python
def vs.GetClOpacityN(strClassName):
    return (outFillOpacity, outPenOpacity)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|strClassName|STRING|   |
|outFillOpacity|INTEGER|   |
|outPenOpacity|INTEGER|   |

## Examples
```pascal
GetClOpacityN('Wall', 1, 2);
```
```python
import vs

strClassName = 'None'

outFillOpacity, outPenOpacity = vs.GetClOpacityN(strClassName)
vs.Message('GetClOpacityN returned: ' + str((outFillOpacity, outPenOpacity)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Classes](../Categories/Classes.md)
