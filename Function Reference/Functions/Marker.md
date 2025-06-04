# Marker

## Description
<b>OBSOLETE for VW2008: Use [[VS:SetDefaultBeginningMarker|SetDefaultBeginningMarker]] and/or [[VS:SetDefaultEndMarker|SetDefaultEndMarker]] instead.</b>
Marker defines a marker (arrowhead) style for the document. This marker style becomes the active style for the document.

A complete listing of marker styles can be found in the [[VS:Function Reference Appendix#Appendix I - Markers |Appendix]]

```pascal
PROCEDURE Marker(
				style : INTEGER;
				size  : REAL;
				ang   : INTEGER);
```

```python
def vs.Marker(style, size, ang):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|style|INTEGER|Marker style constant.|
|size|REAL|Marker size in inches measured in page space.  Legal values are 0.0 to 2.0.|
|ang|INTEGER|Marker angle.|

## Remarks
OBSOLETE for VW2008: Use SetDefaultBeginningMarker and/or SetDefaultEndMarker instead.
See FMarker for parameter descriptions.

[sd 8/14/98]

## Examples
==== VectorScript ====
```pascal
Marker(2,0.25,60);
```
==== Python ====
```python

```

## Version
Marker is obsolete as of VectorWorks13.0<P>


Availability: from MiniCAD6.0

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
