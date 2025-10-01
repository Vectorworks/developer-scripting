# GetFolderPath

## Description
Function GetFolderPath returns the full path to the requested folder independent of localized folder names. It returns an empty string if the folder isn't found.

Note:
use of the negative values of these constants can be used to get the user-based folder path.  The positive values are for application-based paths, which should not be used for writing.

A complete listing of supported folders may be found in the [Script Appendix](../Appendix/pages/Appendix%20J%20-%20Folder%20Indexes.md).

```pascal
FUNCTION GetFolderPath(whichPath : INTEGER): STRING;
```

```python
def vs.GetFolderPath(whichPath):
    return STRING
```

## Parameters
|Name|Type|Description|
|---|---|---|
|whichPath|INTEGER|Path constant.|

## Remarks
[sd 8/18/98]:
Get folder path returns the fully qualified path with platform specific folder separators. On the Mac it returns the path with colons as the separator and uses the backslash on windows. If you are concatenating your own path on the end of a GetFolderPath return string you need to match the qualifier to the platform.

*\_c\_* [2007.06.17]: 
Always generates a minor alert if the path doesn't exist (VW 12.5.x). Can be annoying if user doesn't have "Display minor alerts on mode bar" on. Toggling the preference is also useless: by the end of the script, restoring user's preferences, the alert will be seen. 

*\_c\_* [2007.06.21]: 
In order to access the user's settings folder use flag -15 (VW 12.5.x)
alrtDialog(concat('User settings path: ', getFolderPath(-15)));
Then I have no idea how to resolve eventual localizations of the SavedSettings.xml or SavedSettingsUser.xml file. I could find no string in the resources storing these file names. The SavedSettingsUser.xml can be accessed directly by GetSavedSetting/SetSavedSetting.

*\_c\_* [2008.03.29]: 
Since VW 13 the flag system has been expanded:
negative flag number: user's folders (by default in Application Support)
positive flag number: application folders (where the VW folder resides)
The path defined with the flag (positive) 12 will point to the User's folder.

[[User:Ptr|Ptr]] [2021.02.26]:
List above updated.

## Examples
#### VectorScript ####
```pascal
PROCEDURE Example;
BEGIN
AlrtDialog(GetFolderPath(12));
END;
RUN(Example);
```
#### Python ####
```python
def Example():
	vs.AlrtDialog(vs.GetFolderPath(12))
Example()
```

## Version
Availability: from VectorWorks 8.0

## Category
* [File IO](../Categories/File%20IO.md)

