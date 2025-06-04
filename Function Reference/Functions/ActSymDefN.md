# ActSymDefN

## Description
Function ActSymDefN returns a handle to the currently active symbol.<BR>
<BR>
If the active symbol is not in the active document, it will be imported, unless there is a conflict and the allowConflictDlg parameter is set to FALSE. After being imported, the imported symbol will be returned.

```pascal
FUNCTION ActSymDefN(allowConflictDlg : BOOLEAN): HANDLE;
```

```python
def vs.ActSymDefN(allowConflictDlg):
    return HANDLE
```

## Parameters
|Name|Type|Description|
|---|---|---|
|allowConflictDlg|BOOLEAN|Whether to show a conflict dialog if the active symbol is not in the active document, and a conflict would need to be resolved to import it. If there is a conflict and allowConflictDlg is set to FALSE, ActSymDefN will return NULL.|

## Examples
```python
HandleToActiveSym:=ActSymDefN(TRUE);
```

## See Also
VS Functions:
[ActLayer](ActLayer.md) 
| [ActiveClass](ActiveClass.md) 
| [ActSymDef](ActSymDef.md)

## Version
Availability: from Vectorworks 2021

## Category
* [Objects - Symbols](../Categories/Objects%20-%20Symbols.md)
