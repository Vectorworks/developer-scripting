# NextDObj

## Description
Function NextDObj returns the next deselected object after the referenced object in a list. If the end of the list is reached, the function returns NIL.

```pascal
FUNCTION NextDObj(h : HANDLE): HANDLE;
```

```python
def vs.NextDObj(h):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Examples
==== VectorScript ====
```pascal
handleToObject:=FObject;
WHILE handleToObject &lt;&gt; NIL DO BEGIN
SetSelect(handleToObject);
handleToObject:=NextDObj(handleToObject);
END;
{ selects all deselected objects }
```
==== Python ====
```python

```

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
