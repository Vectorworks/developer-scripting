# NextObj

## Description
Function NextObj returns the next object in any list . If the end of the list is reached, the function returns NIL. This procedure can be used with other handle routines such as FirstIn3D,FInGroup, FirstInSymDef, or FLayer.

```pascal
FUNCTION NextObj(h : HANDLE): HANDLE;
```

```python
def vs.NextObj(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object,  group, or  symbol definition.|

## Examples
mplexDialogLayout4}}

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
