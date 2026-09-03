# CustomTexPartExists

## Description
Returns true if object has the specified partID custom texture part.

```pascal
FUNCTION CustomTexPartExists(
				obj    : HANDLE;
				partID : LONGINT): BOOLEAN;
```

```python
def vs.CustomTexPartExists(obj, partID):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|Object handle|
|partID|LONGINT|Custom texture part ID, ex: 100.|

## Examples
```python
hasPart := CustomTexturePartExists(h, 100);
```

```pascal
resultOK := CustomTexPartExists(obj, 1);
```
```python
import vs

# Returns true if object has the specified partID custom texture part.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer
partID = 1

ok = vs.CustomTexPartExists(obj, partID)
if ok:
    vs.Message('CustomTexPartExists succeeded')
else:
    vs.Message('CustomTexPartExists failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Textures](../Categories/Textures.md)
