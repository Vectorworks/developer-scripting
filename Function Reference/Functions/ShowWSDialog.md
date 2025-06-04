# ShowWSDialog

## Description
Displays a worksheet preference or settings dialog for the active worksheet. 

Settings or attributes modified by the dialog will be applied to the current selection range of the worksheet.
{| class="wikitable_c"
|+ Table - Worksheet Dialog Selectors
! Index !! Dialog
|- 
| style="text-align:center"| 0
| Column Width
|- 
| style="text-align:center"| 1
| Cell Border
|- 
| style="text-align:center"| 2
| Number
|- 
| style="text-align:center"| 3
| Preferences
|- 
| style="text-align:center"| 4
| Print Setup
|- 
| style="text-align:center"| 5
| Print
|-  
| style="text-align:center"| 6
| Function
|- 
| style="text-align:center"| 7
| Criteria
|-  
| style="text-align:center"| 8
| Format Text
|- 
| style="text-align:center"| 9
| Set Row Criteria
|- 
| style="text-align:center"| 10
| Edit Row Criteria
|}

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
