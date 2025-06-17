# ResetDefStoryLevels

## Description
Clears default story levels and repopulates the list from XML data files on disk.

```pascal
FUNCTION ResetDefStoryLevels(bDeleteExisting : BOOLEAN): BOOLEAN;
```

```python
def vs.ResetDefStoryLevels(bDeleteExisting):
    return BOOLEAN
```

## Parameters
|Name|Type|Description|
|---|---|---|
|bDeleteExisting|BOOLEAN|Whether to delete existing default story levels before reloading the original defaults.|

## Remarks
{ \_c\_ 2018.10.22} This, as of VW 2019, uses the default content from the Application folder. And nothing else. Not even that in the User Folder.
{ \_c\_ 2022/10/10} In VW 2023 the default contents from workgroup folders or user folder are used before the default contents from the application folder.

## See Also
VS Functions:
[GetLevelTemplateName](GetLevelTemplateName.md) 
| [SetLevelTemplateName](SetLevelTemplateName.md) 
| [GetLevelTemplateInfo](GetLevelTemplateInfo.md) 
| [GetNumLevelTemplates](GetNumLevelTemplates.md)

## Version
Availability: from Vectorworks 2015

## Category
* [Layers](../Categories/Layers.md)
