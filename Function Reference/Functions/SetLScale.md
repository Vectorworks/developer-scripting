# SetLScale

## Description
Procedure SetLScale sets the scale of the referenced layer. 

Calculating the Scale:

To calculate the scale parameter from an architecural scale, the following formula may be used:
:denominator/numerator * true size(in inches) = ActualSize

For example, to calculate a scale of 3/8"=1'-0", the scale parameter would be 8/3 *12 = 32.

```pascal
PROCEDURE SetLScale(
				h     : HANDLE;
				scale : REAL);
```

```python
def vs.SetLScale(h, scale):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to layer.|
|scale|REAL|Scale value for layer.|

## Examples
#### VectorScript ####
```pascal
SetLScale(HandleToLayer,96);
{sets the referenced layer to a scale of 1/8&quot; = 1'}
```
#### Python ####
```python

```

```pascal
{Set The scale of this layer to the scale specified by the sheet}
IF UserLayerName <> gCommonLayer THEN
	SetLScale(GetLayerByName(UserLayerName), gSheetInfo [i].SheetScale);

writeln (' ###### Creating layer - ',UserLayerName,'    layerH  = ',layerH ,'    visibility = ',visibility,'    sheet type = ',gSheetInfo [sheetNum].SheetType,'    type = ',GetType (layerH));
END;
									{set the scale of the layer based on the setup value}
									CASE gSheetInfo [sheetNum].SheetType OF
										1:    SetLScale (layerH, gSetupRecord.SitePlanScale);
										2, 3: SetLScale (layerH, gSetupRecord.FloorPlanScale);
										4:    SetLScale (layerH, gSetupRecord.AuxViewScale);
										5:    SetLScale (layerH, gSetupRecord.NoteSheetScale);
									END;

BEGIN
	SetLScale (layerH [i], currLayerScale [i]);
END;
```
```python
vs.SetLScale(h, scale)
```
See also in tutorials: [07. Set Up Document Structure: Layers and Classes](ai%20examples/07_LayersAndClasses.md)

## Version
Availability: from MiniCAD6.0

## Category
* [Layers](../Categories/Layers.md)
