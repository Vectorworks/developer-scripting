# CC_OnFindAndReplace

## Description
Custom find and replace fuctionality for ConnectCAD objects.

```pascal
PROCEDURE CC_OnFindAndReplace(
				hObject    : HANDLE;
				fieldName  : STRING;
				fieldValue : STRING);
```

```python

def vs.CC_OnFindAndReplace(hObject, fieldName, fieldValue):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE||
|fieldName|STRING||
|fieldValue|STRING||

## Examples
```pascal
BEGIN
	CC_OnFindAndReplace(HObject, Fldname, gResultText);
END;
```
```python
import vs

# Custom find and replace fuctionality for ConnectCAD objects.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
fieldName = 'MyField'
fieldValue = 'MyField'

vs.CC_OnFindAndReplace(hObject, fieldName, fieldValue)
```

## Version
Availability: from Vectorworks 2023.6

## Category
* [ConnectCAD](../Categories/ConnectCAD.md)
