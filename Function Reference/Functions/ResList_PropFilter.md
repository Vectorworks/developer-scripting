# ResList_PropFilter

## Description
Sets the filter for the resource properties. The 'uniqueID' is a string identifier uniquely identifying this control.

```pascal
PROCEDURE ResList_PropFilter(
				uniqueID : STRING;
				callback : PROCEDURE);
```

```python
def vs.ResList_PropFilter(uniqueID, callback):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|callback|PROCEDURE|   |

## Examples
```pascal
ResList_PropFilter('Example', callback);
```
```python
import vs

# Sets the filter for the resource properties.
def handle_object(objHandle):
    vs.Message('Processing: ' + str(objHandle))

uniqueID = 'Example'
callback = handle_object

vs.ResList_PropFilter(uniqueID, callback)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
