# EnableDropShadow

```pascal
PROCEDURE EnableDropShadow(
				h      : HANDLE;
				enable : BOOLEAN);
```

```python
def vs.EnableDropShadow(h, enable):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|   |
|enable|BOOLEAN|   |

## Examples
```pascal
EnableDropShadow(h, TRUE);
```
```python
import vs

h = vs.FSActLayer()  # handle to the first selected object on the active layer
enable = True

vs.EnableDropShadow(h, enable)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
