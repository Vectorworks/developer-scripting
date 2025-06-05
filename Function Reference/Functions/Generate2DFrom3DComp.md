# Generate2DFrom3DComp

## Description
Generates the specified 2D component of a symbol definition or plug-in object from the 3D component.<BR>
The resulting graphics will be similar to converting the 3D component to lines from a view corresponding to the 2D component view. <BR>
3D objects visible in the specified detail level will be used to generate the 2D component.


**Table - 2D components**

| Constant | 2D component         |
|----------|---------------------|
| 0        | Not Set             |
| 1        | Top                 |
| 2        | Bottom              |
| 3        | Top and Bottom Cut  |
| 4        | Front               |
| 5        | Back                |
| 6        | Front and Back Cut  |
| 7        | Left                |
| 8        | Right               |
| 9        | Left and Right Cut  |


**Table - Available Render Modes**

| Constant | Render Mode         |
|----------|--------------------|
| 0        | Wireframe          |
| 6        | Hidden Line        |
| 7        | Dashed Hidden Line |


**Table - Detail levels**

| Constant | Detail level |
|----------|-------------|
| 1        | Low         |
| 2        | Medium      |
| 4        | High        |
| 7        | All         |

```pascal
FUNCTION Generate2DFrom3DComp(
				objectHandle  : HANDLE;
				component     : INTEGER;
				renderMode    : INTEGER;
				levelOfDetail : INTEGER): BOOLEAN;
```

```python
def vs.Generate2DFrom3DComp(objectHandle, component, renderMode, levelOfDetail):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle of a symbol or plug-in object.|
|component|INTEGER|2D component.|
|renderMode|INTEGER|Render mode.|
|levelOfDetail|INTEGER|Detail level. 3D objects visible in this detail level will be used to generate 2D component.|

## See Also
VS Functions:
[Get2DComponentGroup](Get2DComponentGroup.md) 
| [Set2DComponentGroup](Set2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
