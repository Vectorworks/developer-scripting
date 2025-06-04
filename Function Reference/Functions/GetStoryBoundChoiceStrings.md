# GetStoryBoundChoiceStrings

## Description
Gets the choice strings for a story bound control.

```pascal
PROCEDURE GetStoryBoundChoiceStrings(
				story       : HANDLE;
				topBound    : BOOLEAN;
				VAR strings : ARRAY);
```

```python
def vs.GetStoryBoundChoiceStrings(story, topBound):
    return strings
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The story relative to which to get the strings. Nil gets a generic list of strings.|
|topBound|BOOLEAN|Whether to get the strings for a top bound or a bottom bound.|
|strings|ARRAY|Returns the strings.|

## See Also
VS Functions:
[GetStoryBoundDataFromChoiceString](GetStoryBoundDataFromChoiceString.md) 
| [GetChoiceStringFromStoryBoundData](GetChoiceStringFromStoryBoundData.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
