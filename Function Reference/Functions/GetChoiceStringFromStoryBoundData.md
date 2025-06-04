# GetChoiceStringFromStoryBoundData

## Description
Gets the story bound choice string from story bound data.

```pascal
PROCEDURE GetChoiceStringFromStoryBoundData(
				boundType        : INTEGER;
				boundStory       : INTEGER;
				layerLevelType   : STRING;
				VAR choiceString : STRING);
```

```python
def vs.GetChoiceStringFromStoryBoundData(boundType, boundStory, layerLevelType):
    return choiceString
```

## Parameters
|Name|Type|Description|
|---|---|---|
|boundType|INTEGER|Bounding type: 0 - DefaultWallHeight; 1 - LayerZ; 2 - Story.|
|boundStory|INTEGER|The story identified by 'boundType' = (2 - Story). If 'boundStory' = 0 then it is this story (the object's story); If 'boundStory' = 1 then it is the story above; If 'boundStory' = 2 then it is the story below.|
|layerLevelType|STRING|The layer type which defines this bound.|
|choiceString|STRING|Returns the choice string that represents the story bound data.|

## See Also
VS Functions:
[GetStoryBoundChoiceStrings](GetStoryBoundChoiceStrings.md) 
| [GetStoryBoundDataFromChoiceString](GetStoryBoundDataFromChoiceString.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
