[//]: # (cache-etag: "")
[//]: # (cache-source: https://raw.githubusercontent.com/Vectorworks/developer-scripting/main/Function%20Reference/Functions/InsertPulldownSearch.md)
[//]: # (cache-date: 2026-04-21)

# InsertPulldownSearch

## Description
Inserts an item into a Layout Manager searchable pulldown

```pascal
FUNCTION InsertPulldownSearch(
                dialogID        : LONGINT;
                controlID       : LONGINT;
                itemIDStr       : STRING;
                itemDisplayName : STRING;
                itemTooltip     : STRING;
                itemImageSpec   : STRING;
                shouldUpdate    : BOOLEAN) : BOOLEAN;
```

```python
def vs.InsertPulldownSearch(dialogID, controlID, itemIDStr, itemDisplayName, itemTooltip, itemImageSpec, shouldUpdate):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|ID of the dialog the controls is in|
|controlID|LONGINT|ID of the control to add item to|
|itemIDStr|STRING|ID of the new item|
|itemDisplayName|STRING|Display name of the new item|
|itemTooltip|STRING|Tooltip message of the new item|
|itemImageSpec|STRING|Filename, including path, of the image to be displayed for the new item|
|shouldUpdate|BOOLEAN|Whether or not the pulldown should be updated immediately|

## Examples
[CreateAndInsertPulldownSearch](examples/CreateAndInsertPulldownSearch.md)

## Version
Availability: from Vectorworks 2027

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
