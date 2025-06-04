# GetWSImgComponent

## Description
Gets the specified component of a worksheet cell image.<BR>
Table - Components:     <BR>
Component			Constant<BR>
&quot;3D&quot; 				0<BR>
&quot;2D&quot;				1<BR>
&quot;2D Cut&quot;			                2<BR>
&quot;Not set&quot;			                4

```pascal
PROCEDURE GetWSImgComponent(
				worksheet     : HANDLE;
				row           : INTEGER;
				column        : INTEGER;
				VAR component : INTEGER);
```

```python
def vs.GetWSImgComponent(worksheet, row, column):
    return component
```

## Parameters
|Name|Type|Description|
|---|---|---|
|worksheet|HANDLE|The worksheet handle.|
|row|INTEGER|The cell row.|
|column|INTEGER|The cell column.|
|component|INTEGER|The image component|

## See Also
VS Functions:
[SetWSImgComponent](SetWSImgComponent.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Worksheets](../Categories/Worksheets.md)
