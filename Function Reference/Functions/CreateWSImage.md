# CreateWSImage

## Description
Creates an in-document image of the specified worksheet. The specified point location is the top left corner of the image object.

```pascal
FUNCTION CreateWSImage(
				worksheet           : HANDLE;
				locationX,locationY : REAL): HANDLE;
```

```python
def vs.CreateWSImage(worksheet, location):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|Handle to worksheet.|
|location|REAL|X-Y coordinate location of image object.|

## Remarks
*_c_*, 2015.06.20: It is possible to have any number of worksheet images on drawing, each on a different location. But be warned: if you use this routine AND already have some images of the chosen worksheet on drawing, the routine will shift the last created image object, placing it at the chosen coordinates. 

You must check for the presence of other worksheet images using [ GetWSImage](GetWSImage.md) before trying to create a new one then duplicate one of the found items, instead of creating an image.

Moreover, if the WS image is too large to display (about 11 meters long), it will be zero-sized. This also rises a Vectorscript error that - as far as I can tell - is not avoidable, since only creating it you can know if it's too large.

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
