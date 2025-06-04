# GetLightColorRGB

## Description
Procedure GetLightColorRGB returns the RGB color values for the referenced light object.

```pascal
PROCEDURE GetLightColorRGB(
				light     : HANDLE;
				VAR red   : LONGINT;
				VAR green : LONGINT;
				VAR blue  : LONGINT);
```

```python
def vs.GetLightColorRGB(light):
    return (red, green, blue)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|light|HANDLE|Handle to light.|
|red|LONGINT|Returns RGB color component value.|
|green|LONGINT|Returns RGB color component value.|
|blue|LONGINT|Returns RGB color component value.|

## Remarks
Color param range is 0..65535 -DLD 8/28/98

## Version
Availability: from MiniCAD7.0.1

## Category
* [Objects - Lights](../Categories/Objects%20-%20Lights.md)
