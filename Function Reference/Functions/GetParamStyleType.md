# GetParamStyleType

## Description
Returns the style type (by instance or by style) for a parameter.

```pascal
FUNCTION GetParamStyleType(
				hStyle    : HANDLE;
				paramName : STRING): INTEGER;
```

```python
def vs.GetParamStyleType(hStyle, paramName):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hStyle|HANDLE|Handle to a symbol containing a plug-in style.|
|paramName|STRING|Universal name of a parameter to check for style type.|

## Examples
```pascal
hideStyleParms := GetObjectVariableBoolean( parmHand, 1168 );
doorHandStyleType := GetParamStyleType( parmHand, '__DoorHandle' );
drawerHandStyleType := GetParamStyleType( parmHand, '__DrawerHandle' );

shaftFinishStyleType	:= GetParamStyleType( objectHand,  'Shaft Finish' );
capitalFinishStyleType	:= GetParamStyleType( objectHand, 'Capital Finish' );
baseFinishStyleType		:= GetParamStyleType( objectHand, 'Base Finish' );
archClassStyleType		:= GetParamStyleType( objectHand, 'Arch Class' );
structClassStyleType	:= GetParamStyleType( objectHand, 'Struct Class' );

hideStyleParms := GetObjectVariableBoolean( gPluginH, 1168 );
architHeightStyleType := GetParamStyleType( gPluginH, kArchitHeightParam );
structHeightStyleType := GetParamStyleType( gPluginH, kStructHeightParam );
```
```python
import vs

# Returns the style type (by instance or by style) for a parameter.
hStyle = vs.FSActLayer()  # handle to the first selected object on the active layer
paramName = 'Example'

resultN = vs.GetParamStyleType(hStyle, paramName)
vs.Message('GetParamStyleType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
