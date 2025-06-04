# SetStoryElevation

## Description
Sets the elevation of the indicated Story. Returns whether the elevation was successfully set. If the elevaton change would cause Layers associated with the Story to overlap Layers associated with another Story, then the change in elevation will be prevented.

```pascal
FUNCTION SetStoryElevation(
				story     : HANDLE;
				elevation : REAL): BOOLEAN;
```

```python
def vs.SetStoryElevation(story, elevation):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|story|HANDLE|The Story whose elevation is to be set.|
|elevation|REAL|The elevation to set the Story to.|

## Remarks
([[User:CBM-c-|_c_]], 2018.10.23): SetStoryElevations wants mm. It needs the story to have an associated design layer with [[VS:AssociateLayerWithStory]], or it will fail, while AssociateLayerWithStory needs the layer to be linked to a level with [[VS:SetLayerLevelType]] or it will fail. In the example below you have the sequence to make that work.

<code lang="pas">
{ _c_ }

PROCEDURE TEST;
VAR
	storyH, layerH : HANDLE;
	baseElev : REAL;
	storyN, layerN : STRING;
	i : INTEGER;
	
BEGIN
	baseElev := 0mm;
	
	FOR i:=1 TO 3 DO BEGIN
		storyN := Concat('Story-', i);
		
		IF CreateStory(storyN, Concat('ABCD-', i)) = FALSE THEN
			AlrtDialog(Concat(storyN, ' Story creation failed'));
		
		storyH := GetObject(storyN);
		IF storyH <> NIL THEN BEGIN
			layerN := Concat('ABCD-', i, '-OG');
			layerH := CreateLayer(layerN, 1);

			IF layerH <> NIL THEN BEGIN
				IF SetLayerLevelType(layerH, 'OKF') = FALSE THEN
					AlrtDialog(Concat(layerN, ': SetLayerLevelType failed'))
				
				{ fails if the layer is not linked to a level }
				ELSE IF AssociateLayerWithStory(layerH, storyH) = FALSE THEN
						AlrtDialog(Concat(layerN, ': AssociateLayerWithStory failed'))
					
					{ fails if the story is not associated to a layer }
					ELSE IF SetStoryElevation(storyH, baseElev) = FALSE THEN { always mm }
						AlrtDialog(Concat(storyN, ': SetStoryElevation failed'));
			END;
			
			baseElev := baseElev +3000mm;
		END;
	END;
END;
RUN(TEST);
</code>

## See Also
VS Functions:
[CreateStory](CreateStory.md) 
| [GetStoryElevation](GetStoryElevation.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
