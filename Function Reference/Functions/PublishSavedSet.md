# PublishSavedSet

## Description
This function publishes passed saved set from the opened document to the given folder. Returns true if succeeded to publish items.

```pascal
FUNCTION PublishSavedSet(
				savedSetName : STRING;
				outputFolder : DYNARRAY[] of CHAR): BOOLEAN;
```

```python
def vs.PublishSavedSet(savedSetName, outputFolder):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|savedSetName|STRING|Saved set to be published.|
|outputFolder|DYNARRAY[] of CHAR|Output folder for the createded files.|

## Examples
```pascal
resultOK := PublishSavedSet('Example', outputFolder);
```
```python
import vs

# This function publishes passed saved set from the opened document to the
# given folder.
savedSetName = 'Example'
outputFolder = 'C:/Temp'

ok = vs.PublishSavedSet(savedSetName, outputFolder)
if ok:
    vs.Message('PublishSavedSet succeeded')
else:
    vs.Message('PublishSavedSet failed')
```

## Version
Availability: from Vectorworks 2020

## Category
* [ImportExport](../Categories/ImportExport.md)
