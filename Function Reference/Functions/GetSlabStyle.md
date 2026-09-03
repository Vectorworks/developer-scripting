# GetSlabStyle

## Description
Gets the Slab Style of a slab.

```pascal
FUNCTION GetSlabStyle(slab : HANDLE): LONGINT;
```

```python
def vs.GetSlabStyle(slab):
    return LONGINT
```

## Parameters
|Name|Type|Description|
|---|---|---|
|slab|HANDLE|The slab.|

## Examples
```pascal
resultN := GetSlabStyle(slab);
```
```python
import vs

# Gets the Slab Style of a slab.
slab = vs.FSActLayer()  # handle to the first selected object on the active layer

resultN = vs.GetSlabStyle(slab)
vs.Message('GetSlabStyle returned: ' + str(resultN))
```

## See Also
VS Functions:
[SetSlabStyle](SetSlabStyle.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
