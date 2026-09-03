# GetDefOpacityByClsN

```pascal
PROCEDURE GetDefOpacityByClsN(
				VAR outDefFillOpacityByClass : BOOLEAN;
				VAR outDefPenOpacityByClass  : BOOLEAN);
```

```python
def vs.GetDefOpacityByClsN():
    return (outDefFillOpacityByClass, outDefPenOpacityByClass)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|outDefFillOpacityByClass|BOOLEAN|   |
|outDefPenOpacityByClass|BOOLEAN|   |

## Examples
```pascal
GetDefOpacityByClsN(TRUE, FALSE);
```
```python
import vs

outDefFillOpacityByClass, outDefPenOpacityByClass = vs.GetDefOpacityByClsN()
vs.Message('GetDefOpacityByClsN returned: ' + str((outDefFillOpacityByClass, outDefPenOpacityByClass)))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
