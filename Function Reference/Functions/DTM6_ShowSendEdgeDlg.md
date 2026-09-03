# DTM6_ShowSendEdgeDlg

## Description
Shows the Send to Surface dialog for modifier objects with retaining edge.

```pascal
FUNCTION DTM6_ShowSendEdgeDlg(objWEdgeType : INTEGER): INTEGER;
```

```python
def vs.DTM6_ShowSendEdgeDlg(objWEdgeType):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|objWEdgeType|INTEGER|   |

## Examples
```pascal
IF ( hasSelRetEdgeObj ) THEN { make choice }
	sendType := DTM6_ShowSendEdgeDlg( modifObjType );
```
```python
import vs

# Shows the Send to Surface dialog for modifier objects with retaining edge.
objWEdgeType = 0

resultN = vs.DTM6_ShowSendEdgeDlg(objWEdgeType)
vs.Message('DTM6_ShowSendEdgeDlg returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2014

## Category
* [SiteModel Interface Library](../Categories/SiteModel%20Interface%20Library.md)
