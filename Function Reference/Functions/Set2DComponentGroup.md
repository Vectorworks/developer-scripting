# Set2DComponentGroup

## Description
Sets the specified 2D component group of a symbol definition or plug-in object.  Use Top/Plan if you want to add the group into the main container of the object. 

**Table - 2D components**

| Constant | 2D component        |
|----------|--------------------|
| 0        | Not Set            |
| 1        | Top                |
| 2        | Bottom             |
| 3        | Top and Bottom Cut |
| 4        | Front              |
| 5        | Back               |
| 6        | Front and Back Cut |
| 7        | Left               |
| 8        | Right              |
| 9        | Left and Right Cut |
| 10       | Top/Plan           |

```pascal
FUNCTION Set2DComponentGroup(
				objectHandle : HANDLE;
				groupHandle  : HANDLE;
				component    : INTEGER): BOOLEAN;
```

```python
def vs.Set2DComponentGroup(objectHandle, groupHandle, component):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object.|
|groupHandle|HANDLE|Handle to the graphics group. Can be a group or a single object. To delete the corresponding group provide NULL.|
|component|INTEGER|2D component.|

## Examples
```pascal
resultOK := Set2DComponentGroup(objectHandle, groupHandle, 1);
```
```python
import vs

# Sets the specified 2D component group of a symbol definition or plug-in object.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
groupHandle = vs.NextSObj(vs.FSActLayer())  # handle to the next selected object
component = 1

ok = vs.Set2DComponentGroup(objectHandle, groupHandle, component)
if ok:
    vs.Message('Set2DComponentGroup succeeded')
else:
    vs.Message('Set2DComponentGroup failed')
```

## See Also
VS Functions:
[Get2DComponentGroup](Get2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
