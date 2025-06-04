# EnableDrawingWorksheetPalette

## Description
Enables/disables drawing for the specified worksheet or all displayed worksheet palettes if worksheet is nil.<BR>
<BR>
To improve speed and avoid flickering, it is highly recommended to disable drawing in worksheet palettes before performing several write operations in an opened worksheet. <BR>
Enable drawing back when the operations are completed. <BR>

```pascal
PROCEDURE EnableDrawingWorksheetPalette(
				enable    : BOOLEAN;
				worksheet : HANDLE);
```

```python
def vs.EnableDrawingWorksheetPalette(enable, worksheet):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|enable|BOOLEAN|Specifies if worksheet palettes' drawing  should be enabled or disabled.|
|worksheet|HANDLE|Handle to specific worksheet for which to enable/disable drawing;|Set it to nil to enable/disable drawing in all displayed worksheet palettes.|

## Examples
#### VectorScript ####
```pascal
{Disable drawing in all displayed worksheet palettes.}
EnableDrawingWorksheetPalette(false, nil);

{Write it worksheets ....}
...
...
...

{Enable back drawing in all displayed worksheet palettes.}
EnableDrawingWorksheetPalette(true, nil);
```
#### Python ####
```python
{Disable drawing in all displayed worksheet palettes.}
vs.EnableDrawingWorksheetPalette(False, None)

{Write it worksheets ....}
...
...
...

{Enable back drawing in all displayed worksheet palettes.}
vs.EnableDrawingWorksheetPalette(True, None)
```

## Version
Availability: from Vectorworks14.0

## Category
* [Worksheets](../Categories/Worksheets.md)
