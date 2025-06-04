# CreateLayer

## Description
Creates a layer of the specified type.

layerType values:
Design = 1
Presentation	= 2

```pascal
FUNCTION CreateLayer(
				layerName : STRING;
				layerType : INTEGER): HANDLE;
```

```python
def vs.CreateLayer(layerName, layerType):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layerName|STRING|   |
|layerType|INTEGER|   |

## Remarks
[[User:CBM-c-|_c_]], 2015.07.12: The layer type constants can be fetched using [[VS:GetObjectVariableInt]](layerHandle, 154).

## Version
Availability: from VectorWorks 10.5

## Category
* [Layers](../Categories/Layers.md)
