# SetTopPlan2DComp

## Description
Sets the 2D component that is shown in Top/Plan view for a symbol definition or plug-in object<BR>
                           Table - components:<BR>
Component			Constant<BR>
Top				0<BR>
Top and Bottom Cut		                1

```pascal
FUNCTION SetTopPlan2DComp(
				objectHandle : HANDLE;
				component    : INTEGER): BOOLEAN;
```

```python
def vs.SetTopPlan2DComp(objectHandle, component):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object.|
|component|INTEGER|2D component to be shown in Top/Plan view.|

## Examples
```pascal
resultOK := SetTopPlan2DComp(objectHandle, 1);
```
```python
import vs

# Sets the 2D component that is shown in Top/Plan view for a symbol
# definition or plug-in object Table - components: Component Constant Top 0
# Top and Bottom Cut 1.
objectHandle = vs.FSActLayer()  # handle to the first selected object on the active layer
component = 1

ok = vs.SetTopPlan2DComp(objectHandle, component)
if ok:
    vs.Message('SetTopPlan2DComp succeeded')
else:
    vs.Message('SetTopPlan2DComp failed')
```

## See Also
VS Functions:
[GetTopPlan2DComp](GetTopPlan2DComp.md) 
| [Set2DComponentGroup](Set2DComponentGroup.md) 
| [Get2DComponentGroup](Get2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
