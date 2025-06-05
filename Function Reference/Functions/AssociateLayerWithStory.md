# AssociateLayerWithStory

## Description
Associates a Layer with a Story. When a Layer is associated with a Story, the Layer's elevation is displayed relative to the Story elevation. If the elevation of the associated Story is changed, the elevation of the Layer changes with it.

```pascal
FUNCTION AssociateLayerWithStory(
				layer : HANDLE;
				story : HANDLE): BOOLEAN;
```

```python
def vs.AssociateLayerWithStory(layer, story):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|layer|HANDLE|The Layer to associate.|
|story|HANDLE|The Story to associate.|

## Remarks
(*_c_*, 2018.10.23): This needs the layer to be linked to a level with [SetLayerLevelType](SetLayerLevelType.md) or it will fail. In the example below you have the sequence to make that work.

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

## Examples
```pascal
VAR

success:BOOLEAN;
story:HANDLE;
layer:HANDLE;

BEGIN

story := GetObject('4th Floor');
layer := GetObject('Plan 4');
success := AssociateLayerWithStory(layer, story);
```

## See Also
VS Functions:
[GetNumStories](GetNumStories.md) 
| [GetStoryOfLayer](GetStoryOfLayer.md) 
| [CreateStory](CreateStory.md)

## Version
Availability: from Vectorworks 2012

## Category
* [Layers](../Categories/Layers.md)
