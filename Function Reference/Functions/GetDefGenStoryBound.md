# GetDefGenStoryBound

## Description
This will get the default story bound for a plugin that has the kObjXPropSupportGenericStoryLevel property.<BR>
The bound information returned is only valid when the return value of the function is TRUE.

```pascal
FUNCTION GetDefGenStoryBound(
				format             : HANDLE;
				VAR boundType      : INTEGER;
				VAR boundStory     : INTEGER;
				VAR layerLevelType : STRING;
				VAR offset         : REAL): BOOLEAN;
```

```python
def vs.GetDefGenStoryBound(format):
    return (BOOLEAN, boundType, boundStory, layerLevelType, offset)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|format|HANDLE|Handle of the parametric's format|
|boundType|INTEGER|Bounding type:  0 - LayerZ; 1 - DefaultWallHeight; 2 - Story|
|boundStory|INTEGER|The story for the bound. If 'boundStory' = 0 then it is the object's story. If 'boundStory' = 1 then it is the story above. If 'boundStory' = -1 then it is the story below.|
|layerLevelType|STRING|The layer type which defines this bound (e.g. &quot;Ceiling&quot;).|
|offset|REAL|The offset distance from the specified bound story.|

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
