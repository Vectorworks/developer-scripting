# GetPluginStyle

## Description
Get the name of the plug-in style for an object.

```pascal
FUNCTION GetPluginStyle(hObject : HANDLE): STRING;
```

```python
def vs.GetPluginStyle(hObject):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to a plug-in object|

## Examples
```pascal
styleName := GetPluginStyle( parmHand );
IF  len( styleName ) > 0  THEN
BEGIN

bsb := GetCustomObjectInfo(objectName,objectHand,recordHand,wallHand);
styleName := GetPluginStyle( objectHand );
IF  len( styleName ) > 0  THEN BEGIN

{ Style support for parameters }
styleName := GetPluginStyle( gPluginH );
IF  len( styleName ) > 0  THEN
BEGIN
```
```python
import vs

# Get the name of the plug-in style for an object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer

text = vs.GetPluginStyle(hObject)
vs.Message('GetPluginStyle returned: ' + str(text))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
