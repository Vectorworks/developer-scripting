# ShowWebDlg

## Description
Display a web view dialog. Provide empty button name to have the button invisible.

```pascal
PROCEDURE ShowWebDlg(
				title            : STRING;
				url              : STRING;
				buttonText       : STRING;
				contextualHelpID : STRING);
```

```python
def vs.ShowWebDlg(title, url, buttonText, contextualHelpID):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|title|STRING|   |
|url|STRING|   |
|buttonText|STRING|   |
|contextualHelpID|STRING|   |

## Examples
VectorScript:
```pascal
ShowWebDlg('Title', 'www.gooogle.com', 'Close', '');
```
Python:
```python
vs.ShowWebDlg('Title', 'www.gooogle.com', 'Close', '')
```

```pascal
ShowWebDlg('Example', 'Example', 'Example', 'Example');
```
```python
import vs

# Display a web view dialog.
title = 'Example'
url = 'C:/Temp/example.txt'
buttonText = 'Example text'
contextualHelpID = 'Example'

vs.ShowWebDlg(title, url, buttonText, contextualHelpID)
```

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
