# GetLocalizedPluginChoice

## Description
Returns true with outChoice as specified by inPluginName, inParameterName and inChoiceIndex.  Each of the input names are universal names.

```pascal
FUNCTION GetLocalizedPluginChoice(
				inPluginName    : STRING;
				inParameterName : STRING;
				inChoiceIndex   : INTEGER;
				VAR outChoice   : STRING): BOOLEAN;
```

```python
def vs.GetLocalizedPluginChoice(inPluginName, inParameterName, inChoiceIndex):
    return (BOOLEAN, outChoice)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPluginName|STRING|The universal name of the plug-in.|
|inParameterName|STRING|The universal name of the parameter.|
|inChoiceIndex|INTEGER|The  index of the requested choice. ( range is 1 to n)|
|outChoice|STRING|The requested choice string.|

## Examples
```pascal
BEGIN
	status := GetLocalizedPluginChoice( 'Flowchart Node', 'Config', kSortIndex, localizedSortStr );

DelChoices(dialogID, controlID);
pParamName := FieldNameToParamName(fldName);
allChoicesCnt := NumCustomObjectChoices(pioName, pParamName);
for cnt := 1 to allChoicesCnt DO BEGIN
	IF GetLocalizedPluginChoice(pioName, fldName, cnt, str) THEN BEGIN

		strDefault := ConvertOldSizeToSize( default, pioName, seriesIndex );
		strFinal := ConvertOldSizeToSize( str, pioName, seriesIndex );

	ArrowArray[6, 1] :=	kMarkStyle6{ = '6-Circle'};
	ArrowArray[7, 1] :=	kMarkStyle7{ = '7-Cross'};
	ArrowArray[8, 1] :=	kMarkStyle8{ = '8-Slash'};
	ArrowArray[9, 1] :=	kMarkStyle9{ = '9-Lasso'};
	For I := 1 to 10 DO Good := GetLocalizedPluginChoice(kPIOName, kTagPrefsField8, I, ArrowArray[I-1, 2]);
END;
```
```python
import vs

# Returns true with outChoice as specified by inPluginName, inParameterName
# and inChoiceIndex.
inPluginName = 'Example'
inParameterName = 'Example'
inChoiceIndex = 1

ok, outChoice = vs.GetLocalizedPluginChoice(inPluginName, inParameterName, inChoiceIndex)
vs.Message('GetLocalizedPluginChoice returned: ' + str((ok, outChoice)))
```

## See Also
VS Functions:
[GetLocalizedPluginName](GetLocalizedPluginName.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
