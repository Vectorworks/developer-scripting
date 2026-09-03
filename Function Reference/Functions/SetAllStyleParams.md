# SetAllStyleParams

```pascal
PROCEDURE SetAllStyleParams(
				hStyle    : HANDLE;
				styleType : INTEGER);
```

```python
def vs.SetAllStyleParams(hStyle, styleType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hStyle|HANDLE|Handle to a symbol definition contain a plug-in style|
|styleType|INTEGER|0 = Set all parameters to be ny istance parameters 1 = Set all parameters to be by stuyle parameters|

## Examples
```pascal
SetAllStyleParams(hStyle, 1);
```
```python
import vs

hStyle = vs.FSActLayer()  # handle to the first selected object on the active layer
styleType = 0

vs.SetAllStyleParams(hStyle, styleType)
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
