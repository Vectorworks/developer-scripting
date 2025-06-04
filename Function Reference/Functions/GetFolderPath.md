# GetFolderPath

## Description
Function GetFolderPath returns the full path to the requested folder independent of localized folder names. It returns an empty string if the folder isn't found.

; Note:
: use of the negative values of these constants can be used to get the user-based folder path.  The positive values are for application-based paths, which should not be used for writing.

{| class="wikitable_c"
|+ Table - Folder Path Selectors
! Folder Name !! Constant
|-
| APPLICATION FOLDER
| 1
|-
| Plug-ins
| 2
|-
| Workspaces
| 4
|-
| Plug-ins
| 5
|-
| Libraries/Defaults/Templates
| 7
|-
| Libraries/Defaults/Standards
| 8
|-
| VWHelp
| 9
|-
| Plug-ins/Dictionaries
| 10
|-
| USER FOLDER
| 12
|-
| Libraries
| 13
|-
| Libraries/Defaults
| 14
|-
| Settings
| 15
|-
| Plug-ins/Common/Data
| 20
|-
| Plug-ins/Common/Includes
| 21
|-
| Libraries/Favorites
| 23
|-
| Libraries/Defaults/Templates/Architect
| 25
|-
| Libraries/Defaults/Templates/Landmark
| 26
|-
| Libraries/Defaults/Templates/Spotlight
| 27
|-
| Libraries/Defaults/Templates/ConnectCAD
| 29
|-
| Libraries/Defaults/Renderworks - Textures
| 100
|-
| Libraries/Defaults/Cabinet - Handles
| 101
|-
| Libraries/Defaults/Door - Hardware
| 102
|-
| Libraries/Defaults/Attributes - Gradients
| 103
|-
| Libraries/Defaults/Attributes - Hatches
| 105
|-
| Libraries/Defaults/Attributes - Image Fills
| 106
|-
| Libraries/Object Styles/Plant
| 107
|-
| Libraries/Defaults/Toilet Stall - Fixtures
| 108
|-
| Libraries/Defaults/Renderworks - Backgrounds
| 109
|-
| Libraries/Defaults/Seating Layout - Symbols
| 110
|-
| Libraries/Defaults/Tile - Symbols
| 111
|-
| Libraries/Defaults/Human Figure - Textures
| 112
|-
| Libraries/Object Styles/Walls_Slabs_Roofs
| 113
|-
| Libraries/Defaults/Stairs
| 114
|-
| Libraries/Defaults/Title Blocks
| 115
|-
| Libraries/Defaults/Section - Markers
| 116
|-
| Libraries/Defaults/Repetitive Unit
| 117
|-
| Libraries/Defaults/Door - Custom Leaves
| 118
|-
| Libraries/Defaults/Lighting Instrument - Gobos
| 119
|-
| Libraries/Defaults/Reports_Schedules
| 120
|-
| Libraries/Objects - Ent Lighting Instruments
| 121
|-
| Libraries/Defaults/Plants - Hatches
| 124
|-
| Libraries/Defaults/Repetitive Unit/Flooring~Decking
| 125
|-
| Libraries/Defaults/Repetitive Unit/Framing
| 126
|-
| Libraries/Defaults/Repetitive Unit/Masonry Units
| 127
|-
| Libraries/Defaults/Repetitive Unit/Miscellaneous
| 128
|-
| Libraries/Defaults/Repetitive Unit/Roofing
| 129
|-
| Libraries/Defaults/Repetitive Unit/Siding
| 130
|-
| Libraries/Defaults/Walls_Slabs_Roofs - Hatches
| 131
|-
| Libraries/Defaults/Walls_Slabs_Roofs - Textures
| 132
|-
| Libraries/Defaults/Window - Custom Shutters
| 133
|-
| Libraries/Defaults/Sketch Styles
| 134
|-
| Plant Database
| 135
|-
| Plant Database/Vectorworks Plants
| 136
|-
| Libraries/Defaults/Color Palettes
| 137
|-
| Libraries/Defaults/Framing Member - Custom Profile
| 138
|-
| Libraries/Defaults
| 140
|-
| Libraries/Defaults
| 141
|-
| Libraries/Defaults/Structural Shapes
| 142
|-
| Libraries/Defaults/Reports_Schedules/Landmark Schedules
| 143
|-
| Libraries/Defaults/Video Screen
| 144
|-
| Libraries/Defaults/Video Screen/Casings CRT 4-3
| 145
|-
| Libraries/Defaults/Video Screen/Casings CRT 16-9
| 146
|-
| Libraries/Defaults/Video Screen/Casings Flat 4-3
| 147
|-
| Libraries/Defaults/Video Screen/Casings Flat 16-9
| 148
|-
| Libraries/Defaults/Video Screen/Casings CRT Curved 4-3
| 149
|-
| Libraries/Defaults/Video Screen/Screen Images
| 150
|-
| Libraries/Defaults/Video Screen/Projector Models
| 151
|-
| Libraries/Defaults/Video Screen/Stand Models
| 152
|-
| Libraries/Defaults/Attributes - Line Types
| 153
|-
| Libraries/Defaults/Event Planning
| 154
|-
| Libraries/Defaults/Event Planning/Room
| 155
|-
| Libraries/Defaults/Event Planning/Stage
| 156
|-
| Libraries/Defaults/Event Planning/Lectern
| 157
|-
| Libraries/Defaults/Event Planning/Screen
| 158
|-
| Libraries/Defaults/Event Planning/Seating
| 159
|-
| Libraries/Defaults/Event Planning/Step
| 160
|-
| Libraries/Defaults/Stairs - Custom Stair Tool
| 161
|-
| Libraries/Defaults/Stairs - Custom Stair Tool - Stringer Profiles
| 162
|-
| Libraries/Defaults/Attributes - Tile Fills
| 163
|-
| Libraries/Defaults/Text Styles
| 164
|-
| Libraries/Defaults/Focus Points
| 165
|-
| Renderworks
| 166
|-
| Libraries/Defaults/Existing Tree
| 167
|-
| Libraries/Defaults/Heliodon
| 168
|-
| Libraries/Defaults/Heliodon/Symbols
| 169
|-
| Libraries/Defaults/Heliodon/Cities
| 170
|-
| Libraries/Defaults/Renderworks - Render Styles
| 171
|-
| Libraries/Defaults/Story Support
| 172
|-
| Libraries/Defaults/Detail Callout-Marker
| 173
|-
| Libraries/Defaults/Attributes - Line Types
| 174
|-
| Libraries/Defaults/Audio Tools
| 175
|-
| Libraries/Defaults/Parking Space
| 180
|-
| Libraries/Defaults/Reports_Schedules/Spotlight Schedules
| 181
|-
| Libraries/Defaults
| 182
|-
| Libraries/Defaults/Notes
| 183
|-
| Libraries/Defaults/Energy Analysis
| 187
|-
| Libraries/Defaults/Hoist Tools
| 188
|-
| Libraries/Objects - Ent Lighting Accessories
| 189
|-
| Libraries/Objects - Ent Lighting Instruments
| 190
|-
| Libraries/Defaults/Marionette
| 191
|-
| Libraries/Defaults/Marionette/Objects
| 194
|-
| Libraries/Defaults/Marionette/Objects/NURBS$
| 195
|-
| Libraries/Defaults/Record Formats
| 197
|-
| Libraries/Defaults/Irrigation
| 198
|-
| Libraries/Defaults/Tag-Label
| 199
|-
| Libraries/Defaults/Stage Deck
| 200
|-
| Libraries/Objects - Ent Truss
| 201
|-
| Libraries/Defaults/Interior Elevation Marker
| 202
|-
| Libraries/Defaults/Soft Goods - Custom Textures
| 203
|-
| Libraries/Defaults/Railing Fence
| 204
|-
| Libraries/Defaults/Railing Fence/Profile Posts
| 205
|-
| Libraries/Defaults/Railing Fence/Profile Top Rail
| 206
|-
| Libraries/Defaults/Railing Fence/Railing Fence
| 207
|-
| Libraries/Defaults/Railing Fence/Railing Fence/Fence
| 208
|-
| Libraries/Defaults/Railing Fence/Symbol Posts
| 210
|-
| Libraries/Defaults/Slab Drainage
| 211
|-
| Libraries/Defaults/BIMobject
| 212
|-
| Libraries/Defaults/Cable Tools
| 214
|-
| Libraries/Defaults/Cable Tools/Break Out Labels
| 215
|-
| Libraries/Defaults/Cable Tools/Multi Head Symbols
| 216
|-
| Libraries/Object Styles
| 217
|-
| Libraries/Object Styles/Bath-Shower
| 218
|-
| Libraries/Object Styles/Cabinet Base
| 219
|-
| Libraries/Object Styles/Cabinet Utility
| 220
|-
| Libraries/Object Styles/Cabinet Wall
| 221
|-
| Libraries/Object Styles/Campanile
| 222
|-
| Libraries/Object Styles/Column
| 223
|-
| Libraries/Object Styles/Comm Device
| 224
|-
| Libraries/Object Styles/Compartment Sink
| 225
|-
| Libraries/Object Styles/Cabinet Custom
| 226
|-
| Libraries/Object Styles/Desk
| 227
|-
| Libraries/Object Styles/Door
| 228
|-
| Libraries/Object Styles/Escalator
| 229
|-
| Libraries/Object Styles/Fireplace
| 230
|-
| Libraries/Object Styles/Grab Bar
| 231
|-
| Libraries/Object Styles/Hardscape
| 232
|-
| Libraries/Object Styles/HVAC Damper
| 233
|-
| Libraries/Object Styles/HVAC Diffuser
| 234
|-
| Libraries/Object Styles/HVAC Elbow Duct
| 235
|-
| Libraries/Object Styles/HVAC Flex Duct
| 236
|-
| Libraries/Object Styles/HVAC Outlet
| 237
|-
| Libraries/Object Styles/HVAC Splitter
| 238
|-
| Libraries/Object Styles/HVAC Straight Duct
| 239
|-
| Libraries/Object Styles/HVAC Transition
| 240
|-
| Libraries/Object Styles/HVAC Vertical Duct
| 241
|-
| Libraries/Object Styles/HVAC Vertical Elbow
| 242
|-
| Libraries/Object Styles/Incandescent Fixture
| 243
|-
| Libraries/Object Styles/Landscape Area
| 244
|-
| Libraries/Object Styles/Pilaster
| 247
|-
| Libraries/Object Styles/Ramp
| 248
|-
| Libraries/Object Styles/Receptacle
| 249
|-
| Libraries/Object Styles/Shelving Unit
| 250
|-
| Libraries/Object Styles/Simple Elevator
| 251
|-
| Libraries/Object Styles/Switch
| 254
|-
| Libraries/Object Styles/Tables and Chairs
| 255
|-
| Libraries/Object Styles/Toilet Stall
| 256
|-
| Libraries/Object Styles/Window
| 257
|-
| Libraries/Object Styles/Workstation Counter
| 258
|-
| Libraries/Object Styles/Workstation Overhead
| 259
|-
| Libraries/Object Styles/Workstation Panel
| 260
|-
| Libraries/Object Styles/Workstation Pedestal
| 261
|-
| Libraries/Objects - Architecture
| 266
|-
| Libraries/Objects - Building Equip_Appliances
| 267
|-
| Libraries/Objects - Building Furnishings
| 268
|-
| Libraries/Objects - Building Services
| 269
|-
| Libraries/Objects - Ent Audio
| 270
|-
| Libraries/Objects - Ent Controls
| 271
|-
| Libraries/Objects - Ent Stage
| 272
|-
| Libraries/Objects - Ent Truss
| 273
|-
| Libraries/Objects - Landscape Plants
| 274
|-
| Libraries/Objects - Landscape Site
| 275
|-
| Libraries/Objects - Miscellaneous_Entourage
| 276
|-
| Libraries/Defaults/Irrigation/Catalogs
| 277
|-
| Libraries/Defaults/Irrigation/Saved Content/Controllers
| 278
|-
| Libraries/Defaults/Irrigation/Saved Content/Outlets
| 279
|-
| Libraries/Defaults/Irrigation/Saved Content/Drip Outlets
| 280
|-
| Libraries/Defaults/Irrigation/Saved Content/Pipes
| 281
|-
| Libraries/Defaults/Irrigation/Saved Content/Points of Connection
| 282
|-
| Libraries/Defaults/Irrigation/Saved Content/System Components
| 283
|-
| Libraries/Defaults/Irrigation/Saved Content/Valves
| 284
|-
| Libraries/Defaults/Irrigation/Symbols/Controllers
| 285
|-
| Libraries/Defaults/Irrigation/Symbols/Outlets
| 286
|-
| Libraries/Defaults/Irrigation/Symbols/Points of Connection
| 287
|-
| Libraries/Defaults/Irrigation/Symbols/System Components
| 288
|-
| Libraries/Defaults/Irrigation/Symbols/Valves
| 289
|-
| Libraries/Defaults/Cable Tools/Marker Symbols
| 290
|-
| Libraries/Objects - Landscape Site/Stipples
| 291
|-
| Libraries/Defaults/Foliage
| 292
|-
| Libraries/Defaults/Space Planning
| 293
|-
| Libraries/Defaults/Title Blocks/North Points
| 294
|-
| Libraries/Object Styles/Title Block Border
| 300
|-
| Plug-ins/VW_Spotlight
| 302
|-
| Plug-ins/VW_Spotlight/Data
| 303
|-
| Plug-ins/VW_Spotlight/Data/Braceworks
| 304
|-
| Plug-ins/VW_Spotlight/Data/Braceworks/TrussCrossSectionData
| 305
|-
| Libraries/Objects - Ent Event
| 306
|-
| Libraries/Defaults/Hyperlink
| 307
|-
| Libraries/Objects - Ent Lighting Gobos
| 308
|-
| Libraries/Objects - Landscape Furnishings
| 309
|-
| Libraries/Object Styles/Data Tag
| 310
|-
| Libraries/Defaults/Dead Hang Tool
| 311
|-
| Libraries/Defaults/House Rigging Points
| 312
|-
| Libraries/Defaults/Stock Bridle Material
| 313
|-
| Libraries/Defaults/Video Camera
| 314
|-
| Libraries/Defaults/Video Camera/Lenses
| 315
|-
| Libraries/Defaults/Video Camera/Bodies
| 316
|-
| Libraries/Defaults/Video Camera/Stands
| 317
|-
| Libraries/Object Styles/Seating Section
| 319
|-
| Plug-ins/VW_Spotlight/Data/GDTF
| 320
|-
| Libraries/Object Styles/Lighting Pipe
| 321
|-
| Libraries/Object Styles/Lighting Pipe Ladder
| 322
|-
| Libraries/Objects - Ent Video
| 323
|-
| Libraries/Objects - ConnectCAD
| 324
|-
| Libraries/Object Styles/Drawing Label
| 325
|-
| Libraries/Object Styles/Reference Marker
| 326
|-
| Libraries/Object Styles/Interior Elevation
| 327
|-
| Libraries/Object Styles/Section-Elevation Line
| 328
|-
| Libraries/Object Styles/Detail Callout
| 329
|-
| Libraries/Object Styles/Grid Line
| 332
|-
| Libraries/Defaults/ConnectCAD
| 334
|-
| Libraries/Defaults/ConnectCAD/Device
| 335
|-
| Libraries/Defaults/ConnectCAD/Terminator
| 336
|-
| Libraries/Defaults/ConnectCAD/External
| 337
|-
| Libraries/Defaults/ConnectCAD/Distribution
| 338
|-
| Libraries/Defaults/ConnectCAD/Jacks
| 339
|-
| Libraries/Defaults/ConnectCAD/Panels
| 340
|-
| Libraries/Defaults/ConnectCAD/Socket
| 341
|-
| Libraries/Defaults/ConnectCAD/Panel Connectors
| 342
|-
| Libraries/Defaults/Reports_Schedules/ConnectCAD
| 344
|-
| Libraries/Defaults/Materials
| 345
|-
| Libraries/Renderworks Cameras
| 346
|-
| Libraries/Objects - Ent Audio/Speakers
| 347
|-
| Libraries/Objects - Ent Audio/Bumpers
| 348
|-
| Libraries/Object Styles/Cable Tools
| 349
|-
| Libraries/Defaults/Hoist Origin
| 351
|-
| Libraries/Defaults/Classifications
| 352
|}

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

[[User:CBM-c-|_c_]] [2007.06.17]: 
Always generates a minor alert if the path doesn't exist (VW 12.5.x). Can be annoying if user doesn't have "Display minor alerts on mode bar" on. Toggling the preference is also useless: by the end of the script, restoring user's preferences, the alert will be seen. 

[[User:CBM-c-|_c_]] [2007.06.21]: 
In order to access the user's settings folder use flag -15 (VW 12.5.x)
alrtDialog(concat('User settings path: ', getFolderPath(-15)));
Then I have no idea how to resolve eventual localizations of the SavedSettings.xml or SavedSettingsUser.xml file. I could find no string in the resources storing these file names. The SavedSettingsUser.xml can be accessed directly by GetSavedSetting/SetSavedSetting.

[[User:CBM-c-|_c_]] [2008.03.29]: 
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
* [File I@O](../Categories/File%20IO.md)
