# SetDefGenStoryBound

## Description
This will set the default generic story bound for a plugin that has the kObjXPropSupportGenericStoryLevel property.

```pascal
FUNCTION SetDefGenStoryBound(
				format         : HANDLE;
				boundType      : INTEGER;
				boundStory     : INTEGER;
				layerLevelType : STRING;
				offSet         : REAL): BOOLEAN;
```

```python
def vs.SetDefGenStoryBound(format, boundType, boundStory, layerLevelType, offSet):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|format|HANDLE|Handle of the parametric's format|
|boundType|INTEGER|Bounding type:  0 - LayerZ; 1 - DefaultWallHeight; 2 - Story|
|boundStory|INTEGER|The story for the bound. If 'boundStory' = 0 then it is the object's story. If 'boundStory' = 1 then it is the story above. If 'boundStory' = -1 then it is the story below.|
|layerLevelType|STRING|The layer type which defines this bound (e.g. &quot;Ceiling&quot;).|
|offSet|REAL|The offset distance from the specified bound story.|

## See Also
VS Functions:
[GetDefGenStoryBound](GetDefGenStoryBound.md)

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Architectural](../Categories/Objects%20-%20Architectural.md)
