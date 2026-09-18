# SetCLOpacityN

```pascal
PROCEDURE SetCLOpacityN(
				className   : STRING;
				penOpacity  : INTEGER;
				fillOpacity : INTEGER);
```

```python
def vs.SetCLOpacityN(className, penOpacity, fillOpacity):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|className|STRING|   |
|penOpacity|INTEGER|   |
|fillOpacity|INTEGER|   |

## Examples
```pascal
SetCLOpacityN('Wall', 1, 2);
```
```python
import vs

className = 'None'
penOpacity = 1
fillOpacity = 2

vs.SetCLOpacityN(className, penOpacity, fillOpacity)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Classes](../Categories/Classes.md)
