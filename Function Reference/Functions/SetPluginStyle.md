# SetPluginStyle

## Description
Set the style to associate with a plug-in object

```pascal
FUNCTION SetPluginStyle(
				hObject   : HANDLE;
				styleName : STRING): BOOLEAN;
```

```python
def vs.SetPluginStyle(hObject, styleName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hObject|HANDLE|Handle to a plug-in object.|
|styleName|STRING|Name of style to use|

## Examples
```pascal
createStyle := SetPluginStyle(borderH, titleBlockType);
UpdatePIOFromStyle(borderH);

strTagStyle := GetRField( stakeHandle, 'Stake Object', '__DataTagStyleName' );
dx := Str2Num( GetRField( stakeHandle, 'Stake Object', 'ControlPoint01X' ) );
dy := Str2Num( GetRField( stakeHandle, 'Stake Object', 'ControlPoint01Y' ) );
tagHandle := CreateCustomObjectN( 'Data Tag',x + dx, y + dy, rotation, FALSE );
valid := SetPluginStyle( tagHandle, strTagStyle );
valid := DT_AssociateWithObj( tagHandle, stakeHandle );
END;
```
```python
import vs

# Set the style to associate with a plug-in object.
hObject = vs.FSActLayer()  # handle to the first selected object on the active layer
styleName = 'Example'

ok = vs.SetPluginStyle(hObject, styleName)
if ok:
    vs.Message('SetPluginStyle succeeded')
else:
    vs.Message('SetPluginStyle failed')
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
