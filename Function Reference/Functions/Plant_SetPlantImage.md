# Plant_SetPlantImage

## Description
Sets or deletes an image attached to a plant style(styleName) or instance(hPlant). If hPlant is provided it takes priority over styleName. imageIndex selects the image slot : 0 = Plant Form, 1 = Detail, 2 = Misc, 3 = Custom Image. If deleteOnly is true, the image in the specified slot is removed. If deleteOnly is false, the image at imagePath is loaded and attached to the specified slot.

```pascal
PROCEDURE Plant_SetPlantImage(
				styleName  : STRING;
				imageIndex : INTEGER;
				deleteOnly : BOOLEAN;
				imagePath  : STRING;
				hPlant     : HANDLE);
```

```python
def vs.Plant_SetPlantImage(styleName, imageIndex, deleteOnly, imagePath, hPlant):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|styleName|STRING||
|imageIndex|INTEGER||
|deleteOnly|BOOLEAN||
|imagePath|STRING||
|hPlant|HANDLE||

## Version
Availability: from Vectorworks 2026.5

## Category
* [PlantObjectCoreTools](Categories/PlantObjectCoreTools.md)

