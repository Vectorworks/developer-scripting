# SetParamStyleType

```pascal
PROCEDURE SetParamStyleType(
				hStyle    : HANDLE;
				paramName : STRING;
				styleType : INTEGER);
```

```python
def vs.SetParamStyleType(hStyle, paramName, styleType):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|hStyle|HANDLE|Handle to a symbol containing a plug-in style.|
|paramName|STRING|Name of parameter to set|
|styleType|INTEGER|0 = By Instance 1 = By Style|

## Examples
```pascal
SetParamStyleType(styleHandle, 'ControlPoint01X',	kByInstance);
SetParamStyleType(styleHandle, 'ControlPoint01Y',	kByInstance);

BEGIN
	SetParamStyleType(ghParm, '__ColorArrayString',		kByStyle);
	SetParamStyleType(ghParm, '__ColorCountTotal',		kByStyle);
	SetParamStyleType(ghParm, '__ImTexture',			kByStyle);
	SetParamStyleType(ghParm, 'CurOpt',					kByStyle);
	SetParamStyleType(ghParm, '__NoTextureAdjust',		kByStyle);
```
```python
import vs

hStyle = vs.FSActLayer()  # handle to the first selected object on the active layer
paramName = 'Example'
styleType = 0

resultN = vs.SetParamStyleType(hStyle, paramName, styleType)
vs.Message('SetParamStyleType returned: ' + str(resultN))
```

## Version
Availability: from Vectorworks 2017

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
