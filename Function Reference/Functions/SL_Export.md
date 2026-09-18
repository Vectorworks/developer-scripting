# SL_Export

## Description
Export Spotlight Data to xml file.

```pascal
PROCEDURE SL_Export(
				exportType : INTEGER;
				instHand   : HANDLE;
				fieldName  : DYNARRAY[] of CHAR);
```

```python
def vs.SL_Export(exportType, instHand, fieldName):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|exportType|INTEGER|   |
|instHand|HANDLE|   |
|fieldName|DYNARRAY[] of CHAR|   |

## Examples
```pascal
Begin
		SL_Export(ExportType,InstHand,OneField);
End;
```
```python
import vs

# Export Spotlight Data to xml file.
exportType = 0
instHand = vs.FSActLayer()  # handle to the first selected object on the active layer
fieldName = 'MyField'

vs.SL_Export(exportType, instHand, fieldName)
```

## Version
Availability: from Vectorworks 2011

## Category
* [Spotlight](../Categories/Spotlight.md)
