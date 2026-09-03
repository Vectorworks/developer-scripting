# ResList_Filter

## Description
Set a filter for resource in active document. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_Filter(
				uniqueID : STRING;
				callback : PROCEDURE);
```

```python
def vs.ResList_Filter(uniqueID, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|callback|PROCEDURE|   |

## Examples
```pascal
ResList_Init( LocID , 16 );
ResList_AddCont1( LocID, LocBaseFolderID,LocFolderName );
ResList_Filter(LocID,Filter);
ResList_DlgInit( LocID, dialog, LocControl );
```
```python
import vs

# Set a filter for resource in active document.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

uniqueID = 'Example'
callback = handle_object

vs.ResList_Filter(uniqueID, callback)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
