# GetLayerElevationN

## Description
Gets the elevation and thickness of the specified layer in document units.

```pascal
PROCEDURE GetLayerElevationN(
				h             : HANDLE;
				VAR baseElev  : REAL;
				VAR thickness : REAL);
```

```python
def vs.GetLayerElevationN(h):
    return (baseElev, thickness)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to the layer.|
|baseElev|REAL|Base elevation of the layer in document units.|
|thickness|REAL|Thickness of the layer in document units.|

## Examples
```python
PROCEDURE Example;
VAR
	h :HANDLE; 
	baseElev, thickness :REAL;
BEGIN
	h := FLayer;
	WHILE h &lt;&gt; NIL DO BEGIN
		GetLayerElevationN(h, baseElev, thickness);
		thickness := thickness / (25.4 / GetPrefReal(152));
		AlrtDialog(Concat('layer name: ', GetLName(h), ', baseElev: ', baseElev, ', thickness: ', thickness));
		h := NextLayer(h);
	END;
END;
RUN(Example);
```

## See Also
VS Functions:
[SetLayerElevationN](SetLayerElevationN.md)

## Version
Availability: from Vectorworks 2025

## Category
* [Layers](../Categories/Layers.md)
