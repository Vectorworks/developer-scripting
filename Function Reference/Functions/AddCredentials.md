# AddCredentials

## Description
Adds credentials to VectorScript plug-ins. "pluginsPath" expects a full path to a file or the path to a folder containing plug-ins. "credentialFilePath" expects a full path to a .vst credential file. Empty would report the credentials of the plugins. Returns true if no errors and false if any errors were encountered. Actions are logged in "AddCredentialsLog.txt" in the user Plug-ins folder.

```pascal
FUNCTION AddCredentials(
				pluginsPath        : STRING;
				credentialFilePath : STRING) : BOOLEAN;
```

```python
def vs.AddCredentials(pluginsPath, credentialFilePath):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|pluginsPath|STRING|Full path to a folder or to a specific plugin. When folder, all plugins will be processed|
|credentialFilePath|STRING|Full path to the credentials file. When empty, it will report the status of the plugins|

## Remarks
This function is provided by an external plug-in that is not provided by the normal distribution of Vectorworks.

You need to install the <code>Script Batch Process</code> feature from the <code>Vectorworks Developer</code> section of <code>Help → Install Partner Products...</code> menu command.

More info, see here [Prepare Release Plugins](../../Common/Partner%20Install/pages/PrepareReleasePlugins.md)

Additionally, the plug-in is called ‘BatchEncryption’ and can be found inside ‘ToolsWin’ or ‘ToolsMac’ folders of the corresponding Vectorworks SDKs.

The Vectorworks SDK can be downloaded here:
http://www.vectorworks.net/support/custom/sdk/sdkdown.php

## Version
Availability: from Vectorworks 2026

## Category
* [Utility](../Categories/Utility.md)

