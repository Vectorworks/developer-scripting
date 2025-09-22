## Prepare the script plugins for release

The Vectorworks script plugin files \[.vsm, .vso, and .vst] contain the source code. If you are a third-party developer indending to distribute these plugins as features [Install Partner Products](../README.md) it's a good idea to obfuscate the code in them.

This process includes packaging of all code inside the plugin, so the plugin can be used by itself. This is what legacy terminology calls "encryption":

* Pascal VectorScript enryption will expand all <code>{$INCLUDE}</code> statements and precompile the code into binary bytecode and include it in the .vsm, .vso, or .vst files.

* Python scripts will require an .xml file be placed next to the plugin file \[.vsm, .vso, and .vst], with the same name, listing all dependent .py files used by this plugin. This will include the code of the plugin, plus all dependent .pyo files \[compiled python files], into the plugin binary. This will allow the .vsm, .vso, or .vst plugin files to execute without additional dependencies.

  Here is an example of this satelite file for python scripts:
  ```xml
  <?xml version="1.0" encoding="UTF-8" standalone="no"?><!-- This file defines how the corresponding script plug-in should be packaged-->
  <Plugin>
  	<Package>
  		<File>Common/__init__.py</File>
  		<File>Common/Includes/__init__.py</File>
  		<File>Common/Includes/vsoEventsConstants.py</File>
  		<File>Common/Includes/Vector.py</File>
  		<File>Common/Includes/Utilities_Setup.py</File>
  	</Package>
  </Plugin>
  ```

## Manual packaging

You can use Vectorworks itself to package/encrypt the plugin binary.

* Go to the menu <code>Tools → Plug-ins → Plugin Manager...</code>

* Find your plugin in the <code>Custom Plugins</code> tab (where all unencrypted/unpackaged plugins are listed)

  Note: Make sure you have a copy of your plugin \[.vsm, .vso, and .vst file], as the operation will change the file

	<span style="color:red">**Warning:** Make sure you back up your plugin files before proceeding—this operation can result in permanent loss of source code!</span>

* Select your plugin and click the following key combination:

  Mac: <code>Caps Lock + Shift + Option + Command</code>

  Windows: <code>Shift + Ctrl + Alt</code>

* After confirming the alert dialogs, the plugin will be packaged/encrypted in place.

## Developer Credentials

With Vectorworks 2026, you are required to include developer credentials with your plugins. 

More information can be found here: [Plugin Credentials](../../Tasks/Info/PluginCredentials.md)

## Automation

If you have a number of plugins, the manual process can very tedious. Then you can automate the process by using scripts.

First, install the <code>Script Batch Process</code> feature from the <code>Vectorworks Developer</code> section of <code>Help → Install Partner Products...</code> menu command.

This will add a plugin which will provide the following helper script functions. You can write a document script in Vectorworks to mass process plugin files.

### • [EncryptPlugin](../../../Function%20Reference/Functions/EncryptPlugin.md)
  Encrypt one VectorScript Plug-in file.

```pascal
FUNCTION EncryptPlugin(fullPath : STRING): BOOLEAN;
```

```python
def vs.EncryptPlugin(fullPath):
    return BOOLEAN
```


### • [EncryptAllPlugins](../../../Function%20Reference/Functions/EncryptAllPlugins.md)
  will do batch encryption of all VectorScript plug-ins in the Plug-ins folder..

```pascal
PROCEDURE EncryptAllPlugins;
```

```python
def vs.EncryptAllPlugins():
    return None
```


### • [TestEncryptPlugins](../../../Function%20Reference/Functions/TestEncryptPlugins.md)
  will test do batch encryption of all VectorScript plug-ins in the Plug-ins folder and put the reuslt in a test folder. in the Plug-ins folder..

```pascal
PROCEDURE EncryptAllPlugins;
```

```python
def vs.EncryptAllPlugins():
    return None
```


### • [AddCredentials](../../../Function%20Reference/Functions/AddCredentials.md)
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

Note: A file <code>_AddCredentialsLog.txt</code> will be created in the <code>pluginsPath</code> containing the log of the operation.

Make sure you delete the cach of temporary allowed plugins (that still bring up the lauch alert dialog): 

Mac: /Users/user_name/Library/Application Support/Vectorworks/2026/Settings

Windows: C:\user_name\vstanev\AppData\Roaming\Nemetschek\Vectorworks\2026\Settings\ ExceptionsMissingCredentials.bin
