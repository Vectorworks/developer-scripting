# DisplayOrganizationDialog

## Description
Displays the organization dialog with the specified integer as the initially slected tab.
:0: The most recently displayed tab is selected.
:1: The Classes tab is selected.
:2: The Design Layers tab is selected.
:3: The Sheet Layers tab is selected.
:4: The Viewports tab is selected.
:5: The Saved Views tab is selected.
:6: The References tab is selected.
:7: The Stories tab is selected.

```pascal
PROCEDURE DisplayOrganizationDialog(tabToSelect : INTEGER);
```

```python
def vs.DisplayOrganizationDialog(tabToSelect):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|tabToSelect|INTEGER|The tab to be initially selected.|

## Remarks
[[User:CBM-c-|_c_]] (2016.06.20): This doesn't answer to [[VS:DidCancel| DidCancel]].

## Version
Availability: from VectorWorks 12.0

## Category
* [Utility](../Categories/Utility.md)
