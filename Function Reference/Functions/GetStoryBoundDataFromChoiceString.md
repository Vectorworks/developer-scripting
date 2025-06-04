# GetStoryBoundDataFromChoiceString

## Description
Gets the story bound data from a story bound choice string.

```pascal
PROCEDURE GetStoryBoundDataFromChoiceString(
				choiceString       : STRING;
				VAR boundType      : INTEGER;
				VAR boundStory     : INTEGER;
				VAR layerLevelType : STRING);
```

```python
def vs.GetStoryBoundDataFromChoiceString(choiceString):
    return (boundType, boundStory, layerLevelType)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|choiceString|STRING|The choice string that represents the story bound data.|
|boundType|INTEGER|Returns the bounding type: 0 - DefaultWallHeight; 1 - LayerZ; 2 - Story.|
|boundStory|INTEGER|Returns the story identified by 'boundType' = (2 - Story). If 'boundStory' = 0 then it is this story (the object's story); If 'boundStory' = 1 then it is the story above; If 'boundStory' = 2 then it is the story below.|
|layerLevelType|STRING|Returns the layer type which defines this bound.|

## See Also
VS Functions:
[GetStoryBoundChoiceStrings](GetStoryBoundChoiceStrings.md) 
| [GetChoiceStringFromStoryBoundData](GetChoiceStringFromStoryBoundData.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
