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

## Version
Availability: from Vectorworks 2017

## Category
* [Textures](../Categories/Textures.md)
