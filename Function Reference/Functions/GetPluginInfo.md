# GetPluginInfo

## Description
Returns the name and attached parameter record of the currently executing plug-in. Use with menu command or tool item plug-ins.

```pascal
FUNCTION GetPluginInfo(
				VAR pluginName : STRING;
				VAR recordHand : HANDLE): BOOLEAN;
```

```python
def vs.GetPluginInfo():
    return (BOOLEAN, pluginName, recordHand)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pluginName|STRING|Name of plug-in.|
|recordHand|HANDLE|Handle to parameter record of plug-in.|

## Remarks
Maybe a new function class of &quot;Plug-ins&quot; would be more appropriate than &quot;Objects - Custom&quot;.

Please mind that this routine returns obj type 48 (record instance). In case of command plug-ins this might be kind of unexpected. Use getObject'commandName') instead to access the obj type 47 (record definition).

## Examples
```pascal
BEGIN
{*/// Main Program ///*}
	IF GetPluginInfo (pluginName, recordH) THEN
	BEGIN
		formatH := GetObject (pluginName);
		IF pMethod = GetCustomObjectChoice (pluginName, 'pMethod', 2) THEN method := 2
		ELSE method := 1;

PushAttrs;
status := GetPluginInfo (pluginName, recordH);
recordName := GetName (recordH);
pluginH := GetObject (pluginName);

IF GetPluginInfo (pluginName, pluginH) THEN
	recordH := GetObject (pluginName);
```
```python
import vs

# Returns the name and attached parameter record of the currently executing
# plug-in.
ok, pluginName, recordHand = vs.GetPluginInfo()
vs.Message('GetPluginInfo returned: ' + str((ok, pluginName, recordHand)))
```

## Version
Availability: from VectorWorks8.5

## Category
* [Objects - Custom](../Categories/Objects%20-%20Custom.md)
