# CreateRenderBkg

```pascal
FUNCTION CreateRenderBkg(Background : INTEGER): HANDLE;
```

```python
def vs.CreateRenderBkg(Background):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|Background|INTEGER|Background is the type of background the function should return.||0 returns a background with no shader attached.|1 returns a cloud background|2 returns a one color background|3 returns a two color background|4 returns a physical sky background.|

## Examples
```pascal
resultH := CreateRenderBkg(1);
```
```python
import vs

Background = 1

objHandle = vs.CreateRenderBkg(Background)
if objHandle is not None:
    vs.Message('Created object handle: ' + str(objHandle))
```

## Version
Availability: from Vectorworks 2013

## Category
* [Objects - 2D](../Categories/Objects%20-%202D.md)
