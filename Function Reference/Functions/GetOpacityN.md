# GetOpacityN

```pascal
FUNCTION GetOpacityN(
				h                  : HANDLE;
				VAR outPenOpacity  : INTEGER;
				VAR outFillOpacity : INTEGER): Boolean;
```

```python
def vs.GetOpacityN(h):
    return (Boolean, outPenOpacity, outFillOpacity)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Object handle to get the opacity values.|
|outPenOpacity|INTEGER|Output parameter. Return the object's pen opacity as percentage value in range [0-100].|
|outFillOpacity|INTEGER|Output parameter. Return the object's fill opacity as percentage value in range [0-100].|

## Version
Availability: from Vectorworks 2017

## Category
* [Object Attributes](../Categories/Object%20Attributes.md)
