# GetTopPlan2DComp

## Description
Gets the 2D component that is shown in Top/Plan view for a symbol definition or plug-in object.


**Table - components**

| Constant | component         |
|----------|------------------|
| 0        | Top              |
| 1        | Top and Bottom Cut|

```pascal
FUNCTION GetTopPlan2DComp(objectHandle : HANDLE): INTEGER;
```

```python
def vs.GetTopPlan2DComp(objectHandle):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objectHandle|HANDLE|Handle to the object.|

## See Also
VS Functions:
[SetTopPlan2DComp](SetTopPlan2DComp.md) 
| [Get2DComponentGroup](Get2DComponentGroup.md) 
| [Set2DComponentGroup](Set2DComponentGroup.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
