# GetStorySuffix

## Description
Returns the suffix of the indicated Story.

```pascal
FUNCTION GetStorySuffix(story : HANDLE): STRING;
```

```python
def vs.GetStorySuffix(story):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The Story whose suffix is desired.|

## Examples
```pascal
{ Find the story we are currently working on }
hStory := GetStoryBelow( NIL );
storySuffix := GetStorySuffix( hStory );
WHILE (( storySuffix  <> TmpLayerSuffix ) AND ( hStory <> NIL ) ) DO BEGIN
	hStory := GetStoryAbove( hStory );
	if ( hStory <> NIL ) THEN BEGIN
		storySuffix := GetStorySuffix( hStory );

3: BEGIN
	story := GetStoryBelow(NIL);
	WHILE story <> NIL DO BEGIN
		AddChoice(dialogID, 10, GetStorySuffix(story), 0);
		story := GetStoryAbove(story);
	END;
```
```python
import vs

# Returns the suffix of the indicated Story.
story = vs.FSActLayer()  # handle to the first selected object on the active layer

text = vs.GetStorySuffix(story)
vs.Message('GetStorySuffix returned: ' + str(text))
```

## See Also
VS Functions:
[GetStoryElevation](GetStoryElevation.md) 
| [SetStorySuffix](SetStorySuffix.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
