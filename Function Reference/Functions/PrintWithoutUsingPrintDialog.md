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

## Version
Availability: from VectorWorks10.5

## Category
* [Command](../Categories/Command.md)
