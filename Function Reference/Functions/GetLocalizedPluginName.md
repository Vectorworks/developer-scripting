# GetLocalizedPluginName

## Description
Get the localized name of a plug-in given its universal name.  

When VectorWorks plug-ins are localized by distributors in other countries, their names are translated to the appropriate language.  The plug-in file stores both the original universal name and this translated localized name.  The translated name is displayed by the VectorWorks user interface instead of the original name.  If a script needs to display the name of a plug-in in a dialog or message then it should call this function to determine the localized name.  (Note that scripts will use the universal name to specify a plug-in when the name is not being displayed to the user.) 

If the plug-in has not been localized, then this function will return the universal name.

```pascal
FUNCTION GetLocalizedPluginName(
				inPluginName : STRING;
				VAR outName  : STRING): BOOLEAN;
```

```python
def vs.GetLocalizedPluginName(inPluginName):
    return (BOOLEAN, outName)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inPluginName|STRING|Universal name of the plug-in.|
|outName|STRING|The localized name of the plug-in|

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
TYPE
plugin = STRUCTURE
universalName :STRING;
localizedName :STRING;
params :ARRAY[1..99,1..2] OF STRING;
popups :ARRAY[1..99,1..99] OF STRING;
END;
VAR
plugins :ARRAY[1..99] OF plugin;
cnt1, cnt2, cnt3, pluginCnt :INTEGER;
str1, str2, str3, str4 :STRING;
boo :BOOLEAN;
int1, int2 :INTEGER;

PROCEDURE GetInfo(h :HANDLE);
VAR
recHand :HANDLE;
recName :STRING;
BEGIN
recHand := GetRecord(h, NumRecords(h));
recName := GetName(recHand);
FOR cnt1 := 1 TO pluginCnt DO 
IF recName = plugins[cnt1].universalName 
THEN cnt1 := pluginCnt + 2;
IF cnt1 &lt; pluginCnt + 2 THEN BEGIN
boo := GetLocalizedPluginName(recName, str2);
pluginCnt := pluginCnt + 1;
plugins[pluginCnt].universalName := recName;
plugins[pluginCnt].localizedName := str2;
FOR cnt2 := 1 TO NumFields(recHand) DO BEGIN
str1 := GetFldName(recHand, cnt2);
int1 := GetFldType(recHand, cnt2);
boo := GetLocalizedPluginParameter(recName, str1, str2);
plugins[pluginCnt].params[cnt2, 1] := str1;
plugins[pluginCnt].params[cnt2, 2] := str2;
IF int1 = 8 THEN BEGIN
FOR cnt3 := 1 TO NumCustomObjectChoices(recName, str1) DO BEGIN
str3 := GetCustomObjectChoice(recName, str1, cnt3);
boo := GetPluginChoiceIndex(recName, str1, str3, int2);
boo := GetLocalizedPluginChoice(recName, str1, int2, str4);
plugins[pluginCnt].popups[cnt2, cnt3] := Concat(str3, Chr(9), str4);
END;
END;
END;
END;
END;

BEGIN
pluginCnt := 0;
ForEachObject(GetInfo, (T=86));
FOR cnt1 := 1 TO pluginCnt DO BEGIN
WriteLn(plugins[cnt1].universalName, Chr(9), plugins[cnt1].localizedName);
cnt2 := 1;
WHILE plugins[cnt1].params[cnt2, 1] &lt;&gt; '' DO BEGIN
WriteLn('    ', plugins[cnt1].params[cnt2, 1], Chr(9), plugins[cnt1].params[cnt2, 2]);
cnt3 := 1;
WHILE plugins[cnt1].popups[cnt2, cnt3] &lt;&gt; '' DO BEGIN
WriteLn('        ', plugins[cnt1].popups[cnt2, cnt3]);
cnt3 := cnt3 + 1;
END;
cnt2 := cnt2 + 1;
END;
END;
END;
RUN(Example);
```
#### Python ####
```python
def GetInfo( h ):	
	global pluginCnt
	recHand = vs.GetRecord(h, vs.NumRecords(h))
	recName = vs.GetName(recHand)
	for cnt1 in range(1, pluginCnt):
		if recName == plugins[cnt1]['universalName']:
			cnt1 = pluginCnt + 2
		if cnt1 < pluginCnt + 2:
			boo, str2 = vs.GetLocalizedPluginName(recName)
			pluginCnt = pluginCnt + 1
			plugins[pluginCnt]['universalName'] = recName
			plugins[pluginCnt]['localizedName'] = str2
			for cnt2 in range(1, vs.NumFields(recHand)):
				str1 = vs.GetFldName(recHand, cnt2)
				int1 = vs.GetFldType(recHand, cnt2)
				boo, str2 = vs.GetLocalizedPluginParameter(recName, str1)
				plugins[pluginCnt]['params1'][cnt2] = str1
				plugins[pluginCnt]['params2'][cnt2] = str2
				#if int1 == 8:
				#	for cnt3 in range(1, vs.NumCustomObjectChoices(recName, str1)):
				#		str3 = vs.GetCustomObjectChoice(recName, str1, cnt3)
				#		boo, int2 = vs.GetPluginChoiceIndex(recName, str1, str3)
				#		boo, str4 = vs.GetLocalizedPluginChoice(recName, str1, int2)
				#		plugins[pluginCnt].popups[cnt2, cnt3] = vs.Concat(str3, vs.Chr(9), str4)


def Example():	
	global pluginCnt
	global plugins
	global cnt2
	plugins = [{'universalName':'','localizedName':'','params1':['' for kk in range(99)],'params2':['' for kkk in range(99)]} for k in range(99)]
	
	pluginCnt = 0
	vs.ForEachObject(GetInfo, '(T=86)')
	for cnt1 in range(1, pluginCnt):
		vs.WriteLn(plugins[cnt1]['universalName'], vs.Chr(9), plugins[cnt1]['localizedName'])
		cnt2 = 1
		while plugins[cnt1]['params1'][cnt2] != '':
			vs.WriteLn('    ', plugins[cnt1]['params1'][cnt2], vs.Chr(9), plugins[cnt1]['params2'][cnt2])
			cnt3 = 1
			#while plugins[cnt1].popups[cnt2, cnt3] != '':
			#	vs.WriteLn('        ', plugins[cnt1].popups[cnt2, cnt3])
			#	cnt3 = cnt3 + 1				
			cnt2 = cnt2 + 1

Example()
```

## See Also
VS Functions:
[GetLocalizedPluginParameter](GetLocalizedPluginParameter.md) 
| [GetLocalizedPluginChoice](GetLocalizedPluginChoice.md)

## Version
Availability: from VectorWorks10.0

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
