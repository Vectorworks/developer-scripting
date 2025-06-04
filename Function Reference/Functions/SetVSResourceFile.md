# SetVSResourceFile

## Description
<b>This function does not do anything in Vectorworks 2015 and later.</b> This is because the resource system changed. See more at: [[Vectorworks VWR Resources]]

As of Vectorworks 2015, resources are accessed directly by specifying full resource path (resource identifier) and using [[VS:GetVWRString]]

Pre Vectorworks 2015:
Sets the active resource file for a script. The resource file is opened for the duration of script execution.

The name of the resource file should be specified without the file extension.

```pascal
FUNCTION SetVSResourceFile(fileName : STRING): BOOLEAN;
```

```python
def vs.SetVSResourceFile(fileName):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|fileName|STRING|The name of the resource file to be opened.|

## Remarks
Specify the file name without an extension. However, the file must exist in the plug-ins folder WITH an extension. Use .rsr on Windows and .rsrc on the Mac.

## See Also
VS Functions:
[GetResourceString](GetResourceString.md)

## Version
Availability: from VectorWorks9.0

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
