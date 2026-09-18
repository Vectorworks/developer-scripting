# CreateMaterial

```pascal
FUNCTION CreateMaterial(
				name             : STRING;
				isSimpleMaterial : BOOLEAN): HANDLE;
```

```python
def vs.CreateMaterial(name, isSimpleMaterial):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|name|STRING|   |
|isSimpleMaterial|BOOLEAN|   |

## Examples
```pascal
resultH := CreateMaterial('Example', TRUE);
```
```python
import vs

name = 'Example'
isSimpleMaterial = True

objHandle = vs.CreateMaterial(name, isSimpleMaterial)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2021

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
