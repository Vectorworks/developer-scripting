# TestEncryptPlugins

## Description
This will test do batch encryption of all VectorScript plug-ins in the Plug-ins folder and put the reuslt in a test folder.

```pascal
PROCEDURE TestEncryptPlugins;
```

```python
def vs.TestEncryptPlugins():
    return None
```
## Remarks
This function is provided by an external plug-in that is not provided by the normal distribution of Vectorworks.

You need to install the <code>Script Batch Process</code> feature from the <code>Vectorworks Developer</code> section of <code>Help → Install Partner Products...</code> menu command.

More info, see here [Prepare Release Plugins](../../Common/Partner%20Install/pages/PrepareReleasePlugins.md)

Additionally, the plug-in is called ‘BatchEncryption’ and can be found inside ‘ToolsWin’ or ‘ToolsMac’ folders of the corresponding Vectorworks SDKs.

The Vectorworks SDK can be downloaded here:
http://www.vectorworks.net/support/custom/sdk/sdkdown.php

## See Also
* [EncryptPlugin](EncryptPlugin.md)
* [EncryptAllPlugins](EncryptAllPlugins.md)

## Version
Availability: from Vectorworks 2018

## Category
* [Utility](../Categories/Utility.md)
