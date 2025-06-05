# FSymDef

## Description
Function FSymDef returns a handle to the first symbol definition in the current document's symbol library. If the symbol library is empty, the function returns NIL.

```pascal
FUNCTION FSymDef : HANDLE;
```

```python
def vs.FSymDef():
    return HANDLE
```

## Remarks
If the document's level ('top level') contains only symbol folders (type 92) and the symbol definitions (type 16) are all nested in symbol folders, the routine will return the first symbol folder. Using then [NextSymDef](NextSymDef.md) will set the list navigation on the type 92, ignoring the symbol definitions.

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
