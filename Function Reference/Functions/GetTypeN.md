# GetTypeN

## Description
Returns the type index of the referenced planar or screen object.

A complete listing of supported object types may be found in the [[VS:Function_Reference_Appendix#Object_Types| Appendix]].

```pascal
FUNCTION GetTypeN(h : HANDLE): INTEGER;
```

```python
def vs.GetTypeN(h):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|Handle to object.|

## Remarks
[[User:Rgm|Rgm]] [2012.05.16]: Note that to distinguish a Sheet Layer from a Design Layer, you need to check object variable 154 (ovLayerType), eg. GetObjectVariableInt(layerHd,154). If 1, then it's a Design Layer. If 2, then it's a Sheet Layer. GetTypeN will return 31 (kLayerNode) for both types.
[[User:Ptr|Ptr]] [2020.09.14]: In Python you can also use "h.type" where h=HANDLE to get the object type integer. Other attributes of handles are:
<lineList indent = 1>
<line>aux - Get first aux object, or add to an object to the aux list of this one.</line>
<line>locked - Access locked state of the object.</line>
<line>name - Access the name of the object.</line>
<line>next - Access next object in the drawing list.</line>
<line>parent - Access the parent object in the drawing list.</line>
<line>prev - Access previous object in the drawing list.</line>
<line>selected - Access the selection state of the object.</line>
<line>type - Access the type of the object. Get-only.</line>
</linelist>

## Examples
==== Python ====
```python
_hObject=vs.LSActLayer()#get handle of last selected object

_tObject=vs.GetTypeN(_hObject)# get typeindex
#_tObject=_hObject.type is also possible

_list=["1","Line","Rectangle","Oval","Polygon","Arc","7","Freehand","3D Locus","Text","Group","12","Rounded rectangle","Bitmap Image","Symbol in document","Symbol definition","2D Locus","Worksheet","19","20","Polyline","PICT Image","23","Extrude","3D Polygon","26","27","28","Layer Link","30","Layer","32","33","Sweep	","35","36","37","Multiple extrude","39","Mesh","Mesh vertex","42","43","44","45","46","Record Definition (Format)","Record","Document script (1)","50","Script palette (1)","52","53","54","55","Worksheet container","57","58","59","60","61","62","Dimension","64","65","Hatch definition (1)","67","Wall","69","70","Column, Floor, Roof Face","72","73","74","75","76","77","78","79","80","Light","Roof edge","Roof object","CSG Solid (Addition,Subtraction)","85","Plug-in object","Roof element","88","Round walls","90","91","Symbol folder","Texture","Class definition (1)","Solid (Cone, Sphere, ...)","96","Texture Definition(Material)","98","99","100","101","102","103","104","105","106","107","108","109","110","NURBS Curve","112","NURBS Surface","114","115","116","117","118","Image Fill Definition (1)","Gradient Fill Definition (1)","Fill Space (1)","ViewPort"]

vs.AlrtDialog('type no. :',_tObject,'\ntype name :',_list[_tObject-1]) # show type index and type name of selected object in an dialog
```

## See Also
VS Functions:
[GetType](GetType.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Object Info](../Categories/Object%20Info.md)
