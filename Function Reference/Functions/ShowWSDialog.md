# ShowWSDialog

## Description
Displays a worksheet preference or settings dialog for the active worksheet. 

Settings or attributes modified by the dialog will be applied to the current selection range of the worksheet.

**Table - Worksheet Dialog Selectors**

| Index | Dialog           |
|-------|------------------|
| 0     | Column Width     |
| 1     | Cell Border      |
| 2     | Number           |
| 3     | Preferences      |
| 4     | Print Setup      |
| 5     | Print            |
| 6     | Function         |
| 7     | Criteria         |
| 8     | Format Text      |
| 9     | Set Row Criteria |
| 10    | Edit Row Criteria|}

```pascal
PROCEDURE ShowWSDialog(dialogType : INTEGER);
```

```python
def vs.ShowWSDialog(dialogType):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogType|INTEGER|Index of dialog to be displayed.|

## Version
Availability: from VectorWorks 9.0

## Category
* [Worksheets](../Categories/Worksheets.md)
