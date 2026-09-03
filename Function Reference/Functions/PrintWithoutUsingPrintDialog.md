# PrintWithoutUsingPrintDialog

## Description
Available in Industry Series products only. Prints the active document. Neither the Print Dialog nor the PageSetup dialog will be displayed. This function can fail with certain printers if PrintUsingPrintDialog had not previously been called for the active document.

```pascal
FUNCTION PrintWithoutUsingPrintDialog : INTEGER;
```

```python
def vs.PrintWithoutUsingPrintDialog():
    return INTEGER
```

## Examples
```pascal
resultN := PrintWithoutUsingPrintDialog;
```
```python
import vs

# Available in Industry Series products only.
resultN = vs.PrintWithoutUsingPrintDialog()
vs.Message('PrintWithoutUsingPrintDialog returned: ' + str(resultN))
```

## Version
Availability: from VectorWorks10.5

## Category
* [Command](../Categories/Command.md)
