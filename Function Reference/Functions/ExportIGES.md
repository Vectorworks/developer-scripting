# ExportIGES

## Description
Export the document in 3D IGES file. (Initial Graphics Exchange Specification)

```pascal
FUNCTION ExportIGES(
				fileName             : STRING;
				exportSolidAsSurface : BOOLEAN): BOOLEAN;
```

```python
def vs.ExportIGES(fileName, exportSolidAsSurface):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|Output file path.|
|exportSolidAsSurface|BOOLEAN|Export solit objects as surface.|

## See Also
VS Functions:
[ImportIGES](ImportIGES.md)

## Version
Availability: from Vectorworks 2014

## Category
* [File I@O](../Categories/File%20IO.md)
