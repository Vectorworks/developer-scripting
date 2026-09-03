# GetDefaultOpacityN

```pascal
PROCEDURE GetDefaultOpacityN(
				VAR outPenOpacity  : INTEGER;
				VAR outFillOpacity : INTEGER);
```

```python
def vs.GetDefaultOpacityN():
    return (outPenOpacity, outFillOpacity)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outPenOpacity|INTEGER|   |
|outFillOpacity|INTEGER|   |

## Examples
```pascal
GetDefaultOpacityN(1, 2);
```
```python
import vs

outPenOpacity, outFillOpacity = vs.GetDefaultOpacityN()
vs.Message('GetDefaultOpacityN returned: ' + str((outPenOpacity, outFillOpacity)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
