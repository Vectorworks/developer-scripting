# BuildResourceList

## Description
Creates an implicit list of  resources of a specified type, and returns an ID for the list. Values in the list can be retrieved using GetNameFromResourceList.

If the Display Default Content preference (#130) is on and folderIndex is not  0, it will also include all the resources of the specified type in all the files in the selected folder.

If folderIndex is positive, the list will include all the resources of that type from the current document, as well as from the specified folder. If folderIndex is 0, only the resources in the current document will be in the list. If folderIndex is negative, only the resources in the specified folder will be in the list.

A complete listing of supported object types may be found in the [Script Appendix](../Appendix/pages/Appendix%20D%20-%20Vectorworks%20Object%20Types%20and%20Subtypes.md).

| Folder Name                              | Constant |
|------------------------------------------|----------|
| Application                              | 1        |
| Plug-Ins                                 | 2        |
| Workspaces                               | 4        |
| Templates                                | 7        |
| Standards                                | 8        |
| Help                                     | 9        |
| Dictionaries                             | 10       |
| User App Data                            | 12       |
| Libraries                                | 13       |
| Defaults                                 | 14       |
| Settings                                 | 15       |
| PDF Resources                            | 18       |
| Plug-In Data                             | 20       |
| Plug-In Includes                         | 21       |
| Plug-In interfaces                       | 22       |
| Favorites                                | 23       |
| Renderworks - Textures                   | 100      |
| Cabinet - Handles                        | 101      |
| Door - Hardware                          | 102      |
| Attributes - Gradients                   | 103      |
| Hardscape - Hatches                      | 104      |
| Attributes - Hatches                     | 105      |
| Attributes - Image Fills                 | 106      |
| Plants                                   | 107      |
| Toilet Stall - Fixtures                  | 108      |
| RenderWorks - Backgrounds                | 109      |
| Seating Layout - Symbols                 | 110      |
| Tile - Symbols                           | 111      |
| Human Figure - Textures                  | 112      |
| Walls                                    | 113      |
| Stairs                                   | 114      |
| Drawing Border - Title Blocks            | 115      |
| Section - Markers                        | 116      |
| Repetitive Unit                          | 117      |
| Door - Custom Leaves                     | 118      |
| Lighting Instrument - Gobos              | 119      |
| Reports~Schedules                        | 120      |
| Lighting Instrument - Symbols            | 121      |
| Plants - Hatches                         | 124      |
| Repetitive Unit: Flooring/Decking        | 125      |
| Repetitive Unit: Framing                 | 126      |
| Repetitive Unit: Masonry Units           | 127      |
| Repetitive Unit: Miscellaneous           | 128      |
| Repetitive Unit: Roofing                 | 129      |
| Repetitive Unit: Siding                  | 130      |
| Walls - Hatches                          | 131      |
| Walls - Textures                         | 132      |
| Window - Custom Shutters                 | 133      |
| Sketch Styles                            | 134      |
| Plant Database                           | 135      |
| VW Plants                                | 136      |
| Color Palettes                           | 137      |
| Framing Member - Custom Profile          | 138      |
| Spaces - Occupant Organization Name Lists| 140      |
| Spaces - Space Name Lists and Libraries  | 141      |
| Structural Shapes                        | 142      |
| Reports~Schedules - Landmark Schedules   | 143      |
| Video Screen                             | 144      |
| Video Screen - Casings CRT 4-3           | 145      |
| Video Screen - Casings CRT 16-9          | 146      |
| Video Screen - Casings Flat 4-3          | 147      |
| Video Screen - Casings Flat 16-9         | 148      |
| Video Screen - Casings CRT Curved 4-3    | 149      |
| Video Screen - Screen Images             | 150      |
| Video Screen - Projector Models          | 151      |
| Video Screen - Stand Models              | 152      |
| Attributes - Line Types                  | 153      |
| Event Planning                           | 154      |
| Event Planning - Room                    | 155      |
| Event Planning - Stage                   | 156      |
| Event Planning - Lectern                 | 157      |
| Event Planning - Screen                  | 158      |
| Event Planning - Seating                 | 159      |
| Event Planning - Step                    | 160      |
| Stairs - Custom Stair Tool               | 161      |
| Stairs - Custom Stair Tool - Stringer Profiles | 162 |
| Tile - Symbols                           | 163      |
| Text Styles                              | 164      |
| Focus Points                             | 165      |
| Renderworks - Render Styles              | 166      |
| Existing Tree                            | 167      |
| Heliodon                                 | 168      |
| Heliodon - Symbols                       | 169      |
| Heliodon - Cities                        | 170      |
| Renderworks - Render Styles              | 171      |
| Story Support                            | 172      |
| Detail Callout-Marker                    | 173      |
| Attributes - Line Types                  | 174      |
| Audio Tools                              | 175      |
| Audio Tools - Bumpers                    | 176      |
| Audio Tools - Speakers                   | 177      |
| Extras                                   | 178      |
| Samples                                  | 179      |
| Parking Space                            | 180      |
| Reports~Schedules - Spotlight Schedules  | 181      |
| Workspaces                               | 182      |

```pascal
FUNCTION BuildResourceList(
				type          : INTEGER;
				folderIndex   : INTEGER;
				subFolderName : STRING;
				VAR numItems  : LONGINT): LONGINT;
```

```python
def vs.BuildResourceList(type, folderIndex, subFolderName):
    return (LONGINT, numItems)
```

## Parameters
|Name|Type|Description|
|---|---|---|
|type|INTEGER|the type of resource to put in the list|
|folderIndex|INTEGER|the index of a VW folder.|
|subFolderName|STRING|the name of a subfolder inside the folder specified by folderIndex. This can also be a partial path.  Use an empty string to request the resources from all files in the folderIndex folder.|
|numItems|LONGINT|the number of items in the list built|

## Remarks
It also will not work on any symbol which is ''inside'' a folder -- it only works on symbols at the top level.
[[User:User:KKeizer| Kars]], 26-08-2020: it is now getting all symbols including "inside" a folder and handling them as one resource list. (using VW 2020).

*\_c\_*, 2007.06.02]: This doesn't seem to support Symbol Folders (object type 92). 
[[User:User:KKeizer| Kars]], 26-08-2020: it is working with Symbol Folders (object type 92) (using VW 2020).

*\_c\_*, 2009.12.29: To obtain a list of sketch styles excluding records pass object type -47. This is to my knowledge the only usage of a negative object type.

*\_c\_*, 2016.02.29:  Here some usage examples:
<code lang="vs">
resID := 127; { wall styles }
pathID := 113; { Wall ~ Slabs folder }

list := BuildResourceList(resID, 0, '', cnt); { current document }
list := BuildResourceList(resID, pathID, '', cnt); { current document + app folder }
list := BuildResourceList(resID, -pathID, '', cnt); { current document + user folder }
```

[[User:Ptr| ptr]], 2019.09.16:

**Undocumented list id's**

| Resource type | List ID |
|---------------|---------|
| Line Types    | 96      |
| Roof Styles   | 102     |
| Slab Styles   | 107     |
| Tiles         | 108     |
| Wall Styles   | 127     |

## Examples
#### VectorScript ####
```pascal
CONST
    kHatch = 66;
    kDefHatchFolder = 105;
VAR
    listID, numItems: LONGINT;
BEGIN
    { Create a resource list of hatches from the current document and } 
    { the default hatch folder. }
    listID := BuildResourceList(kHatch, kDefHatchFolder, '', numItems);
    { ... }
```

```pascal
{ try this on a file with some symbol folders }
PROCEDURE testResCountSymFolders;
VAR
    folderList : LONGINT;
    numFolders : INTEGER;
BEGIN
    { list symbol folders in curr doc }
    folderList := BuildResourceList(92, 0, '', numFolders);
    alrtDialog(concat(numFolders));
END;
Run(testResCountSymFolders);
```
VectorScript ====
```pascal
CONST
    kHatch = 66;
    kDefHatchFolder = 105;
VAR
    listID, numItems: LONGINT;
BEGIN
    { Create a resource list of hatches from the current document and } 
    { the default hatch folder. }
    listID := BuildResourceList(kHatch, kDefHatchFolder, '', numItems);
    { ... }
```

```pascal
{ try this on a file with some symbol folders }
PROCEDURE testResCountSymFolders;
VAR
    folderList : LONGINT;
    numFolders : INTEGER;
BEGIN
    { list symbol folders in curr doc }
    folderList := BuildResourceList(92, 0, '', numFolders);
    alrtDialog(concat(numFolders));
END;
Run(testResCountSymFolders);
```

Another example from Pat Stanford <pat@coviana.com>
November 2006
[WorkingWithResrouceList](examples/WorkingWithResrouceList.md)

## See Also
VS Functions:
[AddResourceToList](AddResourceToList.md) 
| [DeleteResourceFromList](DeleteResourceFromList.md) 
| [GetNameFromResourceList](GetNameFromResourceList.md) 
| [GetResourceFromList](GetResourceFromList.md) 
| [ImportResourceToCurrentFile](ImportResourceToCurrentFile.md)

## Version
Availability: from VectorWorks 12.0

## Category
* [Document List Handling](../Categories/Document%20List%20Handling.md)
