# CreateChainDimension

## Description
Creates and returns a single chain dimension object when the two dimensions or chains that are passed in meet the requirements for being in a single chain dimension object.

```pascal
FUNCTION CreateChainDimension(
				h1 : HANDLE;
				h2 : HANDLE): HANDLE;
```

```python
def vs.CreateChainDimension(h1, h2):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h1|HANDLE|   |
|h2|HANDLE|   |

## Examples
```pascal
resultH := CreateChainDimension(h1, h2);
```
```python
import vs

# Creates and returns a single chain dimension object when the two dimensions
# or chains that are passed in meet the requirements for being in a single
# chain di.
h1 = vs.FSActLayer()  # handle to the first selected object on the active layer
h2 = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object

objHandle = vs.CreateChainDimension(h1, h2)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from VectorWorks12.5

## Category
* [Dimensions](../Categories/Dimensions.md)
