# PrintUsingPrintDialog

## Description
Available in Industry Series products only. Prints the active document.  The Print Dialog will be displayed.  The PageSetup dialog will be displayed, before the print dialog, if the existing print settings are not valid for the current printer

```pascal
FUNCTION PrintUsingPrintDialog : INTEGER;
```

```python
def vs.PrintUsingPrintDialog():
    return INTEGER
```

## Remarks
Use GetEnabledModules to determine if an Industry Series product is installed.

## Examples
==== VectorScript ====
```pascal

```
==== Python ====
```python
result = vs.PrintUsingPrintDialog()
```

## Version
Availability: from VectorWorks10.5

## Category
* [Command](../Categories/Command.md)
