# FObject

## Description
Function FObject returns a handle to the first object in the first layer of the active document. If the document is empty, the function returns NIL.

```pascal
FUNCTION FObject : HANDLE;
```

```python
def vs.FObject():
    return HANDLE
```

## Examples
[TraverseObjects](examples/TraverseObjects.md)

## See Also
Relative calls:
* [NextObj](NextObj.md) | [PrevObj](PrevObj.md)
* [FObject](FObject.md) | [LObject](LObject.md)
* [FSActLayer](FSActLayer.md) | [LSActLayer](LSActLayer.md)
* [FSObject](FSObject.md)  | [LActLayer](LActLayer.md)
* [NextDObj](NextDObj.md) | [PrevDObj](PrevDObj.md)
* [NextSObj](NextSObj.md) | [PrevSObj](PrevSObj.md)

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
