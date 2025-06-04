# NextSymDef

## Description
Function NextSymDef returns a handle to the next definition in the symbol library after the referenced symbol. If the end of the list has been reached, the function returns NIL.

```pascal
FUNCTION NextSymDef(symHd : HANDLE): HANDLE;
```

```python
def vs.NextSymDef(symHd):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|symHd|HANDLE|Handle to symbol definition in library.|

## Remarks
If the symHd passed as argument is a symbol folder, the list ignores the symbol definitions. See: [[VS:FSymDef]].

## Version
Availability: from All Versions

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
