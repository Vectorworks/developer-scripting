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

## See Also
VS Functions:
[GetTopPlan2DComp](GetTopPlan2DComp.md) 
| [Set2DComponentGroup](Set2DComponentGroup.md) 
| [Get2DComponentGroup](Get2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
