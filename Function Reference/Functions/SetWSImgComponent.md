# SetWSImgComponent

## Description
Sets the specified 2D component of a worksheet cell image.<BR>
Table - Components:     <BR>
Component			Constant<BR>
&quot;3D&quot; 				0<BR>
&quot;2D&quot;				1<BR>
&quot;2D Cut&quot;			                2<BR>
&quot;Not set&quot;			                4

```pascal
PROCEDURE SetWSImgComponent(
				worksheet   : HANDLE;
				topRow      : INTEGER;
				leftColumn  : INTEGER;
				bottomRow   : INTEGER;
				rightColumn : INTEGER;
				component   : INTEGER);
```

```python
def vs.SetWSImgComponent(worksheet, topRow, leftColumn, bottomRow, rightColumn, component):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|topRow|INTEGER|Top row of cell range.|
|leftColumn|INTEGER|Left column of cell range.|
|bottomRow|INTEGER|Bottom row of cell range.|
|rightColumn|INTEGER|Right column of cell range.|
|component|INTEGER|The image component.|

## Examples
```pascal
SetWSImgComponent(worksheet, 1, 2, 3, 10, 5);
```
```python
import vs

# Sets the specified 2D component of a worksheet cell image.
worksheet = vs.GetObject('MyWorksheet')  # handle to a worksheet
topRow = 10
leftColumn = 5
bottomRow = 10
rightColumn = 5
component = 1

vs.SetWSImgComponent(worksheet, topRow, leftColumn, bottomRow, rightColumn, component)
```

## See Also
VS Functions:
[GetWSImgComponent](GetWSImgComponent.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Worksheets](../Categories/Worksheets.md)
