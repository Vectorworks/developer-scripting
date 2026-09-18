# WebDlgEnableConsole

## Description
Enable web dialog console logging file. File located at: &lt;user folder&gt;/Plug-ins/ChromiumEF/WebBrowser_Console_Output.txt

```pascal
PROCEDURE WebDlgEnableConsole(enable : BOOLEAN);
```

```python
def vs.WebDlgEnableConsole(enable):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|enable|BOOLEAN|   |

## Examples
```pascal
WebDlgEnableConsole(TRUE);
```
```python
import vs

# Enable web dialog console logging file.
enable = True

vs.WebDlgEnableConsole(enable)
```

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
