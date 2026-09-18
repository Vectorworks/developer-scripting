# ActLayer

## Description
Function ActLayer returns a handle to the currently active layer in a document.

```pascal
FUNCTION ActLayer : HANDLE;
```

```python
def vs.ActLayer():
    return HANDLE
```

## Remarks
For changing the active layer you can use [Layer](Layer.md).

## Examples
```pascal
resultH := ActLayer;
```
```python
activeLayerName = vs.GetLName( vs.ActLayer() )

if ( objH == None ) or ( vs.IsNewCustomObject( vs.GetName( objH ) ) ):
	containerHandle = vs.ActLayer()
```
See also in tutorials: [10. Iterate the Drawing and Report a Summary](ai%20examples/10_IterateAndReport.md), [23. Count Objects by Criteria (Formula-Driven)](ai%20examples/23_WorksheetCountByCriteria.md), [25. Geometric Property Extraction Table](ai%20examples/25_WorksheetPolyGeometry.md), [27. Formatted Wall Schedule](ai%20examples/27_WorksheetFormattedSchedule.md)

## See Also
VS Functions:
[ActiveClass](ActiveClass.md) 
| [ActSymDef](ActSymDef.md) 
| [GetLName](GetLName.md)

## Version
Availability: from All Versions

## Category
* [Layers](../Categories/Layers.md)
