# Space_AddDiscription

## Description
Add a new Description to the space object.

```pascal
PROCEDURE Space_AddDiscription(
				space       : HANDLE;
				discription : STRING);
```

```python
def vs.Space_AddDiscription(space, discription):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|space|HANDLE|   |
|discription|STRING|   |

## Examples
```pascal
Space_AddDiscription(space, 'Example');
```
```python
import vs

# Add a new Description to the space object.
space = vs.FSActLayer()  # handle to the first selected object on the active layer
discription = 'Example'

vs.Space_AddDiscription(space, discription)
```

## Version
Availability: from Vectorworks 2014

## Category
* [SpaceObjectCoreTools](../Categories/SpaceObjectCoreTools.md)
