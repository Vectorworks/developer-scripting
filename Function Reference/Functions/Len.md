# Len

## Description
Function Len returns the length of the specified string value.

```pascal
FUNCTION Len(v : DYNARRAY[] of CHAR): INTEGER;
```

```python
def vs.Len(v):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|v|DYNARRAY[] of CHAR|Source string.|

## Remarks
_Vectorworks 2018_: This function will behave differently when used during dialog creation. 
:When used between [CreateLayout](CreateLayout.md), [CreateResizableLayout](CreateResizableLayout.md) and [RunLayoutDialog](RunLayoutDialog.md) and [RunLayoutDialogN](RunLayoutDialogN.md) it will return the length of a string in bytes count, mimicking dialog units.
:This means that the number might not be what you expect during the creation of the layout. In this case where this is a problem, you can use it outside the creation and move the value via a variable.
:This was needed to solve alignment issues with Japanese and Unicode in Vectorworks 2018.

## Examples
```pascal
styleName := GetPluginStyle( parmHand );
IF  len( styleName ) > 0  THEN
BEGIN

	hideStyleParms := GetObjectVariableBoolean( parmHand, 1168 );
	doorHandStyleType := GetParamStyleType( parmHand, '__DoorHandle' );
	drawerHandStyleType := GetParamStyleType( parmHand, '__DrawerHandle' );

minStr := Num2Str(0, minutes);
if Len(minStr) = 1 then minStr := Concat('0', minStr);
secStr := Num2Str(0, seconds);
if Len(secStr) = 1 then secStr := Concat('0', secStr);

bsb := GetCustomObjectInfo(objectName,objectHand,recordHand,wallHand);
styleName := GetPluginStyle( objectHand );
IF  len( styleName ) > 0  THEN BEGIN

	shaftFinishStyleType	:= GetParamStyleType( objectHand,  'Shaft Finish' );
	capitalFinishStyleType	:= GetParamStyleType( objectHand, 'Capital Finish' );
	baseFinishStyleType		:= GetParamStyleType( objectHand, 'Base Finish' );
	archClassStyleType		:= GetParamStyleType( objectHand, 'Arch Class' );
	structClassStyleType	:= GetParamStyleType( objectHand, 'Struct Class' );
```
```python
import vs

# Function Len returns the length of the specified string value.
v = 'Example'

resultN = vs.Len(v)
vs.Message('Len returned: ' + str(resultN))
```

## Version
Availability: from All Versions

## Category
* [Strings](../Categories/Strings.md)
