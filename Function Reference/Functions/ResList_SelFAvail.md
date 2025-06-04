# ResList_SelFAvail

## Description
Set the first available item in the resource popup. The 'uniqueID' is a string identifier uniquely identifying this control, item name is the item to search for, if not empty, rest is search properties

```pascal
PROCEDURE ResList_SelFAvail(
				uniqueID            : STRING;
				VAR itemName        : STRING;
				onlyCurrentDocument : BOOLEAN;
				searchOnline        : BOOLEAN;
				skipCurrentDocument : BOOLEAN);
```

```python
def vs.ResList_SelFAvail(uniqueID, onlyCurrentDocument, searchOnline, skipCurrentDocument):
    return itemName
```

## Parameters
|Name|Type|Description|
|---|---|---|
|uniqueID|STRING|   |
|itemName|STRING|   |
|onlyCurrentDocument|BOOLEAN|   |
|searchOnline|BOOLEAN|   |
|skipCurrentDocument|BOOLEAN|   |

## Version
Availability: from Vectorworks 2020

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
