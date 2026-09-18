# ConvToUnstyledRoof

## Description
Sets a roof to be unstyled.

```pascal
PROCEDURE ConvToUnstyledRoof(roof : HANDLE);
```

```python
def vs.ConvToUnstyledRoof(roof):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|roof|HANDLE|The roof.|

## Examples
```pascal
ConvToUnstyledRoof(roof);
```
```python
import vs

# Sets a roof to be unstyled.
roof = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.ConvToUnstyledRoof(roof)
```

## Version
Availability: from Vectorworks 2016

## Category
* [Objects - Roofs](../Categories/Objects%20-%20Roofs.md)
