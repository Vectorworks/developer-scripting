# EditGeorefWithUI

## Description
Edit the georeferenced settings of the specified layer. Pass NIL to edit the document.

```pascal
FUNCTION EditGeorefWithUI(hLayer : HANDLE): BOOLEAN;
```

```python
def vs.EditGeorefWithUI(hLayer):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hLayer|HANDLE|   |

## Examples
```pascal
	GetSelectedChoiceInfo(dlogID, kTitleBlockPopup, 0, choiceNum, choiceStr);
	gBorderLayer := choiceStr;
END;
kGeoreferencingBtn: BEGIN
	tmpBool	:= EditGeorefWithUI( NIL );
	IF GetProjectionLocName( NIL, projectionFormat ) THEN
		SetItemText( dlogID , kGeoreferencingSecText, projectionFormat );
END;
```
```python
import vs

# Edit the georeferenced settings of the specified layer.
hLayer = vs.ActLayer()  # handle to the active design layer

ok = vs.EditGeorefWithUI(hLayer)
if ok:
    vs.Message('EditGeorefWithUI succeeded')
else:
    vs.Message('EditGeorefWithUI failed')
```

## Version
Availability: from Vectorworks 2012

## Category
* [GIS](../Categories/GIS.md)
