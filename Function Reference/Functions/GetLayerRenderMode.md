# GetLayerRenderMode

## Description
Returns the render mode for the referenced layer.

**Table - Render Modes**

| Render Mode                   | Constant |
|-------------------------------|----------|
| Wireframe                     | 0        |
| Unshaded Polygon              | 2        |
| Shaded Polygon                | 3        |
| Shaded Polygon No Lines       | 4        |
| Final Shaded Polygon          | 5        |
| Hidden Line                   | 6        |
| Dashed Hidden Line            | 7        |
| OpenGL                        | 11       |
| Fast RenderWorks              | 12       |
| Fast RenderWorks with Shadows | 13       |
| Final Quality Renderworks     | 14       |
| Custom Renderworks            | 15       |

```pascal
FUNCTION GetLayerRenderMode(theLayer : HANDLE): INTEGER;
```

```python
def vs.GetLayerRenderMode(theLayer):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theLayer|HANDLE|   |

## Version
Availability: from VectorWorks 10.0

## Category
* [Layers](../Categories/Layers.md)
