# WSScript_AddHandle

## Description
Add a handle for a worksheet script usage. This is most notable used for scripts that generate object database for worksheets.

```pascal
PROCEDURE WSScript_AddHandle(h : HANDLE);
```

```python
def vs.WSScript_AddHandle(h):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|h|HANDLE|The handle of an object to be added|

## Remarks
\_c\_ (2021.02.08):
See excellent intrduction to Worksheet Scripting by Pat Stanford on the Techboard:

forum.vectorworks.net/index.php?/topic/75193-a-super-short-course-in-worksheet-scripts/

## Examples
```pascal
WSScript_AddHandle(h);
```
```python
import vs

# Add a handle for a worksheet script usage.
h = vs.FSActLayer()  # handle to the first selected object on the active layer

vs.WSScript_AddHandle(h)
```

## Version
Availability: from Vectorworks 2020

## Category
* [Worksheets](../Categories/Worksheets.md)
