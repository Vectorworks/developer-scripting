# GetPluginChoiceIndex

## Description
Returns true with outIndex as specified by inPluginNameand inParameterName.  Each of the input names are universal names.

```pascal
FUNCTION GetPluginChoiceIndex(
				inPluginName    : STRING;
				inParameterName : STRING;
				inChoiceName    : STRING;
				VAR outIndex    : INTEGER): BOOLEAN;
```

```python
def vs.GetPluginChoiceIndex(inPluginName, inParameterName, inChoiceName):
    return (BOOLEAN, outIndex)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPluginName|STRING|The universal name of the plug-in.|
|inParameterName|STRING|The universal name of the parameter.|
|inChoiceName|STRING|The universal name of the choice.|
|outIndex|INTEGER|The index of the requested choice.  ( range is 1 to n)|

## Examples
```pascal
result := GetPluginChoiceIndex(parmName,'LineMode',pLineMode,TempIndex);
CASE TempIndex OF
	1:	vsoWidgetSetEnable(18,TRUE);
	2,3: vsoWidgetSetEnable(18,FALSE);
END;

gArrowAngle			:= Str2Num ( GetRField( objectHand, objectName, 'Arrow Angle' ) );
gThicknessBasis		:= 0;
gArrowThickness		:= 0;
gArrowWidth			:= 0;
status				:= GetPluginChoiceIndex( objectName, 'Arrow Style', arrowStyle, arrowPopupIndex );
VerifyArrowData;
CASE arrowPopupIndex OF
	kHollowArrowIndex:
		BEGIN

BEGIN
	DetermineClassName := inChoiceName;
	IF UCase(inChoiceName) = 'NONE'
		THEN DetermineClassName := noneClass
		ELSE IF GetPluginChoiceIndex(inPluginName, inParameterName, inChoiceName, index) &
			  GetLocalizedPluginChoice(inPluginName, inParameterName, index, outChoice)
			THEN DetermineClassName := outChoice;
END;
```
```python
import vs

# Returns true with outIndex as specified by inPluginNameand inParameterName.
inPluginName = 'Example'
inParameterName = 'Example'
inChoiceName = 'Example'

ok, outIndex = vs.GetPluginChoiceIndex(inPluginName, inParameterName, inChoiceName)
vs.Message('GetPluginChoiceIndex returned: ' + str((ok, outIndex)))
```

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
