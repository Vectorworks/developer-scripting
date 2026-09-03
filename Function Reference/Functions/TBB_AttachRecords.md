# TBB_AttachRecords

## Description
Attach Project, Sheet, Revision and Issue Records

```pascal
PROCEDURE TBB_AttachRecords(VAR TitleBlockBorder : HANDLE);
```

```python
def vs.TBB_AttachRecords():
    return TitleBlockBorder
```

## Parameters
|Name|Type|Description|
|---|---|---|
|TitleBlockBorder|HANDLE|   |

## Examples
```pascal
}
	Layer( sheetLayer );
	borderName := 'Title Block Border';
	borderH := CreateCustomObjectN (borderName, 0, 0, 0, FALSE);
	TBB_AttachRecords(borderH);
	recordName := GetName (GetRecord (borderH, NumRecords (borderH)));
```
```python
import vs

# Attach Project, Sheet, Revision and Issue Records.
result = vs.TBB_AttachRecords()
```

## Version
Availability: from Vectorworks 2019

## Category
* [Utility](../Categories/Utility.md)
