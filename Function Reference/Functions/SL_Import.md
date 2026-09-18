# SL_Import

## Description
Import Spotlight Data from xml file.

```pascal
PROCEDURE SL_Import(paramSelfHandle : HANDLE);
```

```python
def vs.SL_Import(paramSelfHandle):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|paramSelfHandle|HANDLE|   |

## Examples
```pascal
SL_Import(paramSelfHandle);
```
```python
import vs

# Import Spotlight Data from xml file.
paramSelfHandle = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.SL_Import(paramSelfHandle)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
