# EditShaderRecord

## Description
Brings up the edit shader dialog for this shader.  Returns true if the user pressed the OK button to dismiss the dialog.

```pascal
FUNCTION EditShaderRecord(shaderRecord : HANDLE): BOOLEAN;
```

```python
def vs.EditShaderRecord(shaderRecord):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|shaderRecord|HANDLE|The shader record to edit.|

## Examples
```pascal
resultOK := EditShaderRecord(shaderRecord);
```
```python
import vs

# Brings up the edit shader dialog for this shader.
shaderRecord = vs.GetObject('MyRecord')  # handle to a record format

ok = vs.EditShaderRecord(shaderRecord)
if ok:
    vs.Message('EditShaderRecord succeeded')
else:
    vs.Message('EditShaderRecord failed')
```

## Version
Availability: from VectorWorks10.1

## Category
* [Textures](../Categories/Textures.md)
