# SetLightColorRGB

## Description
Procedure SetLightColorRGB sets the RGB color values for the referenced light object.

```pascal
PROCEDURE SetLightColorRGB(
				light : HANDLE;
				red   : LONGINT;
				green : LONGINT;
				blue  : LONGINT);
```

```python
def vs.SetLightColorRGB(light, red, green, blue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|light|HANDLE|Handle to light.|
|red|LONGINT|RGB color component value.|
|green|LONGINT|RGB color component value.|
|blue|LONGINT|RGB color component value.|

## Remarks
Color param range is 0..65535 -DLD 8/28/98

## Version
Availability: from MiniCAD7.0.1

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
