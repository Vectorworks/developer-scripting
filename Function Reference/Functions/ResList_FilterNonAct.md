# ResList_FilterNonAct

## Description
Sets the filter for resource in the non-active open documents. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_FilterNonAct(
				uniqueID : STRING;
				callback : PROCEDURE);
```

```python
def vs.ResList_FilterNonAct(uniqueID, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|callback|PROCEDURE|   |

## Examples
```pascal
ResList_FilterNonAct('Example', callback);
```
```python
import vs

# Sets the filter for resource in the non-active open documents.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

uniqueID = 'Example'
callback = handle_object

vs.ResList_FilterNonAct(uniqueID, callback)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
