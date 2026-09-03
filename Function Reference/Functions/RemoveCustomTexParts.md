# RemoveCustomTexParts

## Description
This routine removes all custom texture parts from the object.

```pascal
PROCEDURE RemoveCustomTexParts(obj : HANDLE);
```

```python
def vs.RemoveCustomTexParts(obj):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|obj|HANDLE|The object from which to remove custom texture parts.|

## Examples
```python
RemoveCustomTexParts(h);
AddCustomTexPart(100, ‘Stringers’);
AddCustomTexPart(200, ‘Treads’);
```

```pascal
RemoveCustomTexParts(obj);
```
```python
import vs

# This routine removes all custom texture parts from the object.
obj = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.RemoveCustomTexParts(obj)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Textures](../Categories/Textures.md)
