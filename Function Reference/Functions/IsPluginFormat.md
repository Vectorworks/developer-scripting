# IsPluginFormat

## Description
Determines if the format node is used for the parameters of a plug-in object, plug-in tool or plug-in menu command.

```pascal
FUNCTION IsPluginFormat(theFormat : HANDLE): BOOLEAN;
```

```python
def vs.IsPluginFormat(theFormat):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|theFormat|HANDLE|Handle to the format node in question.|

## Remarks
(*\_c\_*), 2014.09.22: VW 2014, 2015: This routine crashes VW instantly if the passed handle is NIL, be careful. 

It is unreliable, for example it fails to recognize a Door format as plug-in format, but will succeed on the Window format. 
* generic objects with attached format (normal format in the Resource Browser) will be mistakenly recognized as parametric (type 48), while their record definition (type 47) won't.
* on the opposite, parametric objects often won't be recognized as parametric (type 48), while their record definition (type 47) will .

It seems to succeed while parsing clean third-party VS parametric objects, but there are loads of shipped objects where this fails - also VS not only SDK, for example: Spiral, Callout, North Arrow, Landscape Area, Grade Tool, Parking along Path, Parking Area, Roadway Tee, Guardrail (Curved), Graticule, Adjacent Matrix, Stacking Diagram, Space Link, Slab, Window Wall (Curved), Column, Pilaster, CW-Stair, Simple Elevator, Chain Extrude, Renderworks Camera, Human Figure, Handrail (Curved), Toilet Stall, Ceiling Grid, Seating Count, Table and Chairs, Slope Dimension, Stipple, Reference Marker, Revision Marker, Linear Marker, Repetitive Unit, and so on...

## Version
Availability: from VectorWorks 11.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
