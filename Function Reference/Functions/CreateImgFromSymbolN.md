# CreateImgFromSymbolN

## Description
Creates an image  from the specified symbol in the specified rendering mode and view, and uses the specified component of the image.       Table - Render Modes <BR>
Render Mode                  Constant <BR>
Wireframe 			0 <BR>
Unshaded Polygon 		2 <BR>
Shaded Polygon 			3 <BR>
Shaded Polygon No Lines 	4 <BR>
Final Shaded Polygon 		5 <BR>
Hidden Line 			6 <BR>
Dashed Hidden Line 		7 <BR>
OpenGL 				11 <BR>
Fast RenderWorks 		12 <BR>
Fast RenderWorks with Shadows 	13 <BR>
Final Quality RenderWorks 	14 <BR>
Custom RenderWorks 		15 <BR>
Artistic RenderWorks 		17 <BR>
Sketch 				18 <BR>
<BR>
Table - Views <BR>
View 				Constant <BR>
Top/Plan 			2 <BR>
Front 				3 <BR>
Back 				4 <BR>
Left 				5 <BR>
Right 				6 <BR>
Top 				7 <BR>
Bottom 				8 <BR>
Right Isometric 		9 <BR>
Left Isometric 			10 <BR>
Right Rear Isometric 		11 <BR>
Left Rear Isometric 		12 <BR>
Bottom Right Isometric 		13 <BR>
Bottom Left Isometric 		14 <BR>
Bottom Right Rear Isometric 	15 <BR>
Bottom Left Rear Isometric 	16 <BR>
<BR>
Table - Components    <BR>
Component			Constant<BR>
&quot;3D&quot; 				0<BR>
&quot;2D&quot;				1<BR>
&quot;2D Cut&quot;			2<BR>
&quot;Not set&quot;			4

```pascal
FUNCTION CreateImgFromSymbolN(
				symbolName : STRING;
				width      : INTEGER;
				height     : INTEGER;
				margin     : INTEGER;
				renderMode : INTEGER;
				view       : INTEGER;
				component  : INTEGER): HANDLE;
```

```python
def vs.CreateImgFromSymbolN(symbolName, width, height, margin, renderMode, view, component):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symbolName|STRING|The name of the symbol to display.|
|width|INTEGER|The width of the symbol to display.|
|height|INTEGER|The height of the symbol to display.|
|margin|INTEGER|The margin of the symbol to display.|
|renderMode|INTEGER|The render mode in which to display the symbol.|
|view|INTEGER|The standard view in which to display the symbol.|
|component|INTEGER|Image component to use.|

## See Also
VS Functions:
[CreateImgFromSymbol](CreateImgFromSymbol.md)

## Version
Availability: from Vectorworks 2019

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
