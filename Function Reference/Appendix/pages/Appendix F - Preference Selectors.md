# Appendix F - Preference Selectors

## Application Preference Selectors

| Preference | Selector | Preference Value | Function |
|------------|----------|------------------|----------|
| Click-Drag Mode | 0 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Offset Duplicates | 1 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Full Screen Cursor | 2 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Screen Hints | 3 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Floating Datum | 4 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap To Loci | 5 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Rulers | 6 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Scroll Bars | 7 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| No Fill Behind Text | 8 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Zoom Line Thickness | 9 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Black and White Only | 10 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Layer Colors | 11 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Log Time in Program | 12 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Adjust Flipped Text | 13 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Other Objects While In Group | 14 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show 3D Axis Labels | 15 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Black Background | 16 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Eight Selection Handles | 17 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Current Background Color | 4003 | | [GetPrefRGB](../../Functions/GetPrefRGB.md) |
| Use Sound | 18 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Issue Undo Warnings | 19 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Opaque SmartCursor | 20 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Stop VectorScript on Warnings | 21 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Left Palette Margin | 22 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Right Palette Margin | 23 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Save Reminder | 24 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Parametric Constraints | 25 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Minor Alerts on Mode Bar | 27 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Associate Dimensions | 28 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Spell Check Capitalized Words | 29 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Spell Check Words in ALL CAPS | 30 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Spell Check Mixed Case Words | 31 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Spell Check Words With Numbers | 32 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Auto Join Walls | 33 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Page Breaks | 34 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Grid | 35 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Print Grid | 36 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap To Grid | 37 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap To Object | 38 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Occluded Picking And Snapping | 105 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Save By Time | 39 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Save Confirm | 40 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Save To Backup | 41 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Palette Docking | 43 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Create Dimensions in Dimension Class | 44 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Accelerated 2D Navigation | 45 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Vector Caching | 46 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Sketch Hidden Line | 47 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Edge Points | 48 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Page Boundary | 49 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Default Content | 130 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Dimension Slash Thickness Unit | 50 | 3 = points, 2 = mils, 1 = mm | [GetPrefInt](../../Functions/GetPrefInt.md) |
| 3D Rotation Responsiveness | 52 | 1(detailed)..5(responsive) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Custom Constraint Angle | 53 | REAL (degrees) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap Radius | 54 | INTEGER value | [GetPrefInt](../../Functions/GetPrefInt.md) |
| 2D Conversion Resolution | 55 | INTEGER value | [GetPrefInt](../../Functions/GetPrefInt.md) |
| 3D Conversion Resolution | 56 | INTEGER value | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Current Document Text Size | 57 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Current Document Text Style | 58 | 0 (Plain) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (Bold) | |
| | | 2 (Italic) | |
| | | 4 (Underline) | |
| | | 8 (Outline [Mac only]) | |
| | | 16 (Shadow [Mac only]) | |
| Current Document Text Justification | 82 | 1 (Left) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (Center) | |
| | | 3 (Right) | |
| Current Document Text Vertical Alignment | 83 | 1 (TopBox) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (TopBaseline) | |
| | | 3 (CenterBox) | |
| | | 4 (BottomBaseline) | |
| | | 5 (BottomBox) | |
| Current Document Text Vertical Spacing | 84 | 0 (Custom Leading) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (Single) | |
| | | 3 (Three Halves) | |
| | | 4 (Double) | |
| Current Document Text Vertical Spacing Custom Value | 85 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Maximum Number of Undos | 59 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Undo View Changes | 26 | 1 (never) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (combine all) | |
| | | 3 (combine similar) | |
| | | 4 (combine none) | |
| Save Interval | 60 | no. of minutes | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Display Light Objects | 61 | 0(always) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1(wireframe) | |
| | | 2(never) | |
| Display 3D Loci Objects | 91 | 0(always) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1(wireframe) | |
| | | 2(never) | |
| Retain QuickDraw 3D Model | 62 | 1(never)...5(always) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Rotated Text Display | 63 | 0(box) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1(normal) | |
| | | 2(high) | |
| Bitmap Display | 64 | 0(box) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1(low res) | |
| | | 2(hi res) | |
| Dimension Slash Thickness | 65 | INTEGER value (mils) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Hidden Line Dash Style | 197 | LONGINT selector | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Hidden Line Shading | 67 | 1(dark)...4(light) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Grid X | 78 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Grid Y | 79 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Origin X | 6702 | REAL (current units) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Origin Y | 6702 | REAL (current units) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Page Origin X | 80 | REAL (current units) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Page Origin Y | 81 | REAL (current units) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Page Scaling Factor | 70 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Dimension Standard | 71 | 1 (Arch) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (ASME) | |
| | | 3 (BSI) | |
| | | 4 (DIN) | |
| | | 5 (ISO) | |
| | | 6 (JIS) | |
| | | 7 (SIA) | |
| | | 8 (ASME Dual Side-by-Side) | |
| | | 9 (ASME Dual Stacked) | |
| Defacet Angle | 72 | REAL (0-90) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Grid Angle | 73 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Move Objects on Grid Keys | 74 | 1 (arrow) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (cmd+arrow) | |
| | | 3 (shift+arrow) | |
| | | 4 (shift+cmd+arrow) | |
| Nudge Objects Keys | 75 | 1-4 (see above) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Show Nudge Message | 6712 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Pan Drawing Keys | 76 | 1-4 (see above) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Switch Active Layer/Class Keys | 77 | 1-4 (see above) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Default Compression | 86 | 1 = JPEG, 2 = PNG | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Line Weight Array Count | 87 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Sound Volume | 88 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Custom Move Distance | 89 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Plan Rotation | 92 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Plan Rotation Angle | 93 | REAL (read-only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Stack Layers | 94 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Stack Layers Create 2D Objects | 95 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Stack Layers Ignore Other Scales | 96 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Stack Layers Restore Views | 97 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Open MP Multithreading | 98 | 0 (No) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (Yes) | |
| | | 2 (Partial) | |
| Stack Layers Center View | 99 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Text Font Name | 100 | STRING | [GetPrefString](../../Functions/GetPrefString.md) |
| Stack Layers Show Page Boundary | 101 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Stack Layers Only Active Layer 2D Objects | 102 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Stack Layers Display Only Story Layers | 103 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Stack Layers Stories Enabled | 104 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Enable Legacy 2D Layer Mode | 6839 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Angular Precision | 120 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Angular Unit | 121 | 0 (degrees) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (radians) | |
| | | 2 (gradians) | |
| Resetting Plugin-ins During File Read | 129 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Enable Vectorworks Libraries | 130 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Auto File Extensions On Mac | 131 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Advanced Imaging | 132 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Anti Aliasing | 133 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Auto Associate Dims | 134 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Mouse Wheel Zoom | 135 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Custom Move Distance | 136 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Print Switch Binary | 137 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Create New Document on Startup | 138 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Change Layer for Create Similar | 139 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Watermarks | 142 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Unit1 Dim Fraction Display Style | 190 | 0 (regular style) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (diagonal style) | |
| | | 2 (horizontal style) | |
| DXF Add Prefix To DXF Layers | 328 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| DXF Prefix To DXF Edit | 329 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| DXF External Refs Handling | 330 | 0 (Bind External Refs) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (Ignore External Refs) | |
| | | 2 (Create VW Refs) | |
| | | 3 (Use Layer Import) | |
| DXF ADT Objects 2D View | 331 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Framed Highlighting | 410 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Smart Cursor Show Interactive Segment | 411 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap To Tool Snap Geometry Only | 460 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| whether to coordinate sheet and drawing numbers for various items | 544 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Auto Save To Custom Location | 552 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Autosave Custom Location | 554 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Keep Backups By Number Value | 555 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Center View | 558 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Allow Copy on Option Click | 559 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| AutoUpdate Frequency | 1054 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Error Reporting Mode | 1056 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Use Multithreading for Textures | 1057 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Multithreading for Image | 1058 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Multithreading for Render | 1059 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Multithreading for Geometry | 1060 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Multithreading for DTM | 1061 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Multithreading for Other | 1062 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Open MP Multithreading | 98 | 0 = No | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 = Yes | |
| | | 2 = Partial | |
| Save DTM Cache | 1097 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Enable X-Ray Mode | 106 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Scale Layer Text | 107 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Hierarchical Classes In Popups | 108 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Save Expand State Of Classes In Popups | 111 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Save Undo View Changes | 112 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Fill Style By Class | 534 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Setting low detail factor. If LayerScales >= LowDetailFactor will only show low detail and will hide wall cavities | 538 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Setting medium detail factor. LayerScales >= MediumDetailFactor will show medium detail, <= MediumDetailFactor will show high detail | 539 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| View Transition Animation | 1227 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| View Transition Speed | 6725 | Real | [GetPref](../../Functions/GetPref.md)  |
| Allow Docking to Drawing | 6752 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Allow Internal Palette Docking | 6753 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Docked Document Tabs | 6754 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Force the tool to trap the shift key for when it is used with the short keys for modebar | 6770 | TRUE or FALSE (write only) | [GetPref](../../Functions/GetPref.md)  |
| Controls the state in which windowshaded palettes automaticaly unshade based on mouse proximity | 6775 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Controls the state in which docked palettes automaticaly hides based on mouse proximity | 6776 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Worksheet parameter delimiter | 6798 | String | [GetPrefString](../../Functions/GetPrefString.md) |
| Worksheet Column Crop Marker Display Always| 7020 | String | Boolean | [GetPref](../../Functions/GetPref.md)  
| Worksheet Menu Display Always | 7021 | String | Boolean | [GetPref](../../Functions/GetPref.md)  
| Turns screen redraws on/off | 6799 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Enable Multiview | 6802 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Multiview visibilities | 6803 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| turns on/off the Duplicate Tags With Objects | 6804 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| turns on/off the drawing of the ray+octree intersected mesh vrefs | 6806 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Enable profile VectorScript execution | 6807 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Enable profile VectorScript execution | 6807 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Enable On Demand Level Of Detail | 6808 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Hide GPU Display Alert Dialog | 6809 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Hide Graphics Adapters Alert Dialog | 6810 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Enable OnDemand Level Of Detail 2D | 6811 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Smart Cursor Lock Special X | 6812 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Smart Cursor Lock Special Y | 6813 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use OpenGL Background Context | 6816 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| OpenGL AntiAliasing Supported | 593 | Boolean |  [GetPref](../../Functions/GetPref.md) |
| OpenGL Draw Edges Supported | 594 | Boolean |  [GetPref](../../Functions/GetPref.md) |
| OpenGL Use Shadows Supported | 595 | Boolean |  [GetPref](../../Functions/GetPref.md) |
| Block Until Done Rendering | 596 | Boolean (write only) |  [GetPref](../../Functions/GetPref.md) |
| Allow Drop Shadows | 597 | Boolean |  [GetPref](../../Functions/GetPref.md) |
| OpenGL Environment Lighting Capability | 598 | Boolean |  [GetPref](../../Functions/GetPref.md) |
| OpenGL Environment Reflection Capability | 599 | Boolean |  [GetPref](../../Functions/GetPref.md) |
| OpenGL Screen Space Reflection Capability | 601 | Boolean |  [GetPref](../../Functions/GetPref.md) |
| Dark Sym Previews | 602 | Boolean |  [GetPref](../../Functions/GetPref.md) |
| Use Duplicates For Raster VPs | 6817 | Boolean | [GetPref](../../Functions/GetPref.md)  |
| Default Render Mode Render Mode | 1318 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Default Render Mode Projection Mode | 1319 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Use Local Help System | 6724 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Home Screen on Startup | 7009 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Home Screen on Closing Last Doc | 7010 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Enable Legacy Eight Lights | 7100 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Enable Emitters | 7102 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Non-Printable Indicators | 7301 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Release Version Integer | 570 | SHORT - The release version integer defaults to 0 | [GetPrefInt](../../Functions/GetPrefInt.md) |
| get/set the insertion mode of the symbol tool | 580 | SHORT | [GetPrefInt](../../Functions/GetPrefInt.md) |
| get/set the wall insertion mode of the symbol tool | 581 | SHORT | [GetPrefInt](../../Functions/GetPrefInt.md) |
| get/set the alignment mode of the symbol tool | 582 | SHORT | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Parametric Enable State Eventing | 590 | 0 (NoStateEvents) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (ResetStatesEvent) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (InternalStatesEvent) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Save VGM Cache | 6840 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |

### Smart Cursor / Appearance Preference Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Store / Recall Interactive Preferences | 1200 | Set=Store Get=Recall | [GetPref](../../Functions/GetPref.md)  |
| Show Selection Box | 1000 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Snap Box | 1001 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Animation Mode | 1003 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Pre-selection Highlighting | 1004 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Marquee Pre-selection Highlighting | 1005 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snapped Object Pre-selection Highlighting | 1006 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Tool Highlighting | 1007 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Highlighting Timer | 1008 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Selection Radius | 1009 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap Box Radius | 1010 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Show Snap Points | 1013 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Zoom to Linethickness in Snap Loop | 1014 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Offset from Source | 1015 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Acquisition Hints | 1016 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Reference Grid X | 1019 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Reference Grid Y | 1020 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Grid Angle Y | 1021 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Sheet Layer Grid Snap X | 1022 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Sheet Layer Grid Snap Y | 1023 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Sheet Layer Reference Grid X | 1024 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Sheet Layer Reference Grid Y | 1025 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Sheet Layer Grid Angle Y | 1026 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap to End Point | 1027 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Mid Point | 1028 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Center Point | 1029 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Quadrant Points | 1030 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Insertion Point | 1031 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Vertex Points | 1032 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Nearest point on Edge | 1033 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap Angles in Degrees | 1034 | Angles are separated by a Semicolon | [GetPrefString](../../Functions/GetPrefString.md) |
| Plan Rotation | 1035 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Alternate Cordinate Extension Lines | 1036 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Horizontal Vertical Extensions | 1037 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Angular Extensions | 1038 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Floating Smart Point | 1039 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Acquire Smart Point if the mouse stops for | 1040 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Set Datum if mouse stops for | 1041 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use Datum Offset | 1042 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Datum Offset | 1043 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Acquire Edge | 1044 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Acquire Edge if mouse follows edge for | 1045 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap to Bisector | 1046 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Offset | 1047 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap Offset Diatance | 1048 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap to Extension Lines | 1049 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap Proportional | 1050 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap by Percent | 1051 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap by Distance | 1052 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap Mutiple Divisions | 1053 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Others in Group Gray | 1055 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show 3D Z Axis | 1063 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show 3D Z Axis Grp | 1064 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Relative Angles | 1086 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Relative Snap Angle | 1087 | Clockwise from Horizontal | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Relative Snap Angle Hint | 1088 | TRUE = Tangent FALSE = Parallel | [GetPref](../../Functions/GetPref.md)  |
| Clear Relative Angle and Hint | 1089 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Combined Page Area | 1090 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Individual Pages | 1091 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Angles form Axes | 1092 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Alternate Cordinate System | 1093 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Line Between Smart Points | 1094 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to All Extensions from Nearby Smart Points | 1095 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Disable All Snaps | 1096 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Working Plane Axes in Plan View | 1098 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Tool Help On Status Bar | 7014 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |

### Interactive Smart Cursor Dialog Preference Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Store / Recall Interactive Preferences | 1200 | Set=Store Get=Recall | [GetPref](../../Functions/GetPref.md)  |
| Full Screen Cursor | 1210 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Selection Box | 1211 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Snap Box | 1212 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Acquisition Hints | 1213 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Selection Radius | 1214 | Screen Inches | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap Radius | 1215 | Screen Inches | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Grid Radius | 1216 | Screen Inches | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Selection Highlighting Mode | 1220 | | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Animation Mode | 1221 | | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Cursor Preselection Highlighting | 1222 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Marquee Preselection Highlighting | 1223 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snapped Object Highlighting | 1224 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Tool Highlighting | 1225 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Highlighting Timer | 1226 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Show Smart Cursor Cues | 1230 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Snap Points | 1231 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Loci | 1232 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Zoom Line Thickness in Snap Loop | 1233 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Combined Page Area | 1234 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Individual Pages | 1235 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Offset from Source | 1236 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Ignore Non Planar Shapes | 1237 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Do Not Show Grid | 1240 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Print Grid | 1241 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show 3D Axis Grid | 1242 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show 3D Axis Grid Labels | 1243 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show 3D Axis Grid Grip | 1299 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to End Points | 1250 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Mid Point | 1251 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Center | 1252 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Quad | 1253 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Intersection | 1254 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Vertex | 1255 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Edge | 1256 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Master | 1257 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to User Angles | 1260 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| User Angle Count | 1261 | 1 to 8 | [GetPrefInt](../../Functions/GetPrefInt.md) |
| User Angle Degrees 1 | 1262 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Angle Degrees 2 | 1263 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Angle Degrees 3 | 1264 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Angle Degrees 4 | 1265 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Angle Degrees 5 | 1266 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Angle Degrees 6 | 1267 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Angle Degrees 7 | 1268 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| User Angle Degrees 8 | 1269 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Snap to Relative Angles | 1280 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Plan Rotation Angle | 1281 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Alternative Coordinate System | 1282 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Alternative Coordinate System Angle | 1283 | | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use Horizontal and Vertical Extensions | 1290 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Angular Extensions | 1291 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Lines Between Smart Points | 1292 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Allow Extensions from Nearby Smart Points | 1293 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Floating Smart Points | 1294 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Floating Point Smart Time | 1295 | Seconds | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use Floating Datum | 1296 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Floating Datum Time | 1297 | Seconds | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use Floating Edges | 1300 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Floating Edge Time | 1301 | Seconds | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use Angle Bisector | 1302 | TRUE or FALSE | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use Curve Extensions | 1303 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Object | 1310 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Grid | 1311 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Constrain to Angle | 1312 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Intersection | 1313 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Smart Points | 1314 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Distance | 1315 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Snap to Smart Edge | 1316 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Constrain Tangent | 1317 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |

### Interactive Appearance Preference Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Standard Background Properties Selector Base | 1325 | Add the selectors below | |
| Black Background Properties Selector Base | 4025 | Add the selectors below | |
| Smart Cursor Selection Box | + 0 | | |
| Smart Cursor Snap Box | + 30 | | |
| Smart Cursor Datum Indicator | + 60 | | |
| Smart Cursor Points | + 90 | | |
| Smart Cursor Edges | + 120 | | |
| Smart Cursor Vector Locks | + 150 | | |
| Smart Cursor Acquisition Hints | + 180 | | |
| Snap Points Available | + 210 | | |
| Current Snap Points | + 240 | | |
| Snap Points Obtained | + 270 | | |
| Snap Points Congestion Indicator | + 300 | | |
| Object Highlighting PreSelection Active Layer | + 330 | | |
| Object Highlighting Selection Active Layer | + 360 | | |
| Object Highlighting Selection Inactive Layer | + 390 | | |
| Object Highlighting Selection Locked | + 420 | | |
| Object Highlighting Snap Object | + 450 | | |
| Object Highlighting Tool Highlighting | + 480 | | |
| Object Highlighting Action | + 510 | | |
| General Exit Edit Context Frame | + 540 | | |
| General Exit Edit Context Show Others | + 570 | | |
| General Page Boundary | + 600 | | |
| General Grid | + 630 | | |
| General Working Plane | + 660 | | |
| General Ground Plane | + 690 | | |
| General Hint Text | + 720 | | |
| General Hint Background | + 750 | | |
| General Reshape Handles Active Layer | + 780 | | |
| General Reshape Handles Inactive Layer | + 810 | | |
| Object Highlighting PreSelection Inactive Layer | + 840 | | |
| Object Highlighting PreSelection Locked | + 870 | | |
| Snap Points Object Oriented | + 900 | | |
| Smart Cursor Planes | + 930 | | |
| Smart Cursor Smart Point Lines | + 960 | | |
| General Repetition Opacity | + 990 | | |
| Smart Cursor Angle Lines | + 1020 | | |
| Object Highlighting Automatic Plane Source | + 1050 | | |
| General XRay Edge Selection | + 1080 | | |
| General Top Plan Backgrond Color | + 1110 | | |
| General Sheet Layer Background Color | + 1140 | | |
| General 3D View Background Color | + 1170 | | |
| General Background Perspective Horizon Sky | + 1200 | | |
| General Background Perspective Horizon Ground | + 1230 | | |
| Object Highlighting Occluded Feedback | + 1260 | | |
| Clip Cube Solid Cut | + 1290 | | |
| Clip Cube Hollow Cut | + 1320 | | |
| Snap Points Master | + 1350 | | |
| Object Highlighting Checked Out | + 1380 | | |
| Subdivision Crease Highlighting | + 1410 | | |
| Ruler Cursor Position Indicators | + 1440 | | |
| Ruler Background | + 1470 | | |
| Ruler Marks and Text | + 1500 | | |
| Floating Databar Background | + 1530 | | |
| Floating Databar Outline and Text | + 1560 | |
| General Object Previews | + 1590 | |
| General Unhide Objects Button | + 1620 | |
| Onscreen View Control Text And Accents | + 1650 | |
| Onscreen View Control Cube | + 1680 | |
| Onscreen View Control Working Plane Cube Face | + 1710 | |
| General Active View Pane Label | + 1740 | |
| Property Available | + 0 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Different Background Color | + 1 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Pattern | + 2 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Foreground Color | + 4 | RGB | [VS:GetPrefRGB](#) |
| Background Color | + 5 | RGB | [VS:GetPrefRGB](#) |
| Opacity | + 6 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Size | + 7 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Minimum Size | + 8 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Maximum Size | + 9 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Opacity 1 | + 10 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Size 1 | + 11 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Minimum Size 1 | + 12 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Maximum Size 1 | + 13 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Opacity 2 | + 14 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |

**Example:** To access the Opacity of Object Highlighting Tool Highlighting with a Standard Background use 1811 (1325 + 480 + 6)

## On-Demand Menu Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Use ODM | 6900 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show ODM After Mouse Idle | 6901 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| ODM Mouse Idle Timer | 6902 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Show ODM with Spacebar | 6903 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show ODM with Middle Mouse Button | 6904 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Initialize ODM Layout | 6905 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 0 (Icon Hint) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (Text Hint) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (Icon and Text Hint) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 3 (Full View) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Section ODM Parameters | 6906 | Integer | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 0 (Section ID) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (Section Type) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 0 (None) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (Tool Modes) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (Snapping Bar) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 3 (Recent Tools) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 4 (Standard Views) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 5 (Tool Sets) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (Quadrant Position) | | |
| | | 0 (Top Left) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (Top Right) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (Bottom Left) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 3 (Bottom Right) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 3 (Tool Set ID) | | |
| | | 4 (Tool Set Name) |
| Show ODM Search Filters | 7000 | True or False | [GetPref](../../Functions/GetPref.md)  |
| Show Items Not In Workspace | 7001 | True or False | [GetPref](../../Functions/GetPref.md)  |
| Show ODM Command Context | 7002 | True or False | [GetPref](../../Functions/GetPref.md)  |
| Activate Tool Set On Tool Selection | 7003 | True or False | [GetPref](../../Functions/GetPref.md)  

## Primary Units Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Unit Fraction | 150 | REAL value | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Units Per Inch | 152 | REAL value | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Unit Style Name | 153 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Unit Mark | 154 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Sunit Mark | 155 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Sunit Divider | 156 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Smultiplier | 157 | INTEGER value | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Square Unit Mark | 158 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Square Unit Divisor | 159 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Cube Unit Mark | 160 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Cube Unit Divisor | 161 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Display Fraction | 162 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Show Unit Mark | 163 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Leading Zero | 164 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Trailing Zeroes | 165 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Minimum Units | 166 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Custom Units | 167 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Decimals as Fractions | 168 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Dimension Precision | 169 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Predefined Units Style | 170 | 1 (Feet & Inches) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (Inches) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 3 (Feet) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 4 (Yards) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 5 (Miles) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 6 (Microns) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 7 (Millimeters) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 8 (Centimeters) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 9 (Meters) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 10 (Kilometers) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 11 (Degrees – Landmark & Azimuth only) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Fractional Display Precision | 171 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Fractional Dimension Precision | 172 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Metric Unit Flag | 173 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Angular Unit | 174 | 0 (degrees) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (radians) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (gradians) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Round Fraction to Decimal | 175 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Area Units Per Square Inch | 176 | REAL value | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Area Unit Name | 177 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Area Unit Mark | 178 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Area Precision | 179 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Volume Units Per Cubic Inch | 180 | REAL value | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Volume Unit Name | 181 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Volume Unit Mark | 182 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Volume Precision | 183 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Use Custom Area Units | 184 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Custom Volume Units | 185 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Area Unit Fraction | 186 | REAL value | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Volume Unit Fraction | 187 | REAL value | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Display Rounding Base | 188 | 0 (1) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (2.5) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (5) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Dimension Rounding Base | 189 | 0 (1) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (2.5) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (5) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Dimension Rounding Base | 190 | 0 (regular style) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 1 (diagonal style) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 2 (horizontal style) | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Show Thousands Separator | 191 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Save and Restore Unit1 | 192 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| HiddenLineDashType | 197 | Integer value | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Default Dimension Class ID | 546 | RefNumber | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |

### Secondary Units Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Unit Fraction | 200 | REAL value | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Units Per Inch | 202 | REAL value | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Unit Style Name | 203 | 64 character STRING | [GetPrefString](../../Functions/GetPrefString.md) |
| Unit Mark | 204 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Sunit Mark | 205 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Sunit Divider | 206 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Smultiplier | 207 | INTEGER value | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Square Unit Mark | 208 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Square Unit Divisor | 209 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Cube Unit Mark | 210 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| Cube Unit Divisor | 211 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Display Fraction | 212 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Show Unit Mark | 213 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Display Leading Zero | 214 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Display Trailing Zeroes | 215 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Use Minimum Units | 216 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Use Custom Units | 217 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Show Decimals as Fractions | 218 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Dimension Precision | 219 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Predefined Units Style | 220 | 1 (Feet & Inches) | [GetPrefInt](../../Functions/GetPrefInt.md) |
|  |  | 2 (Inches) | " |
|  |  | 3 (Feet) | " |
|  |  | 4 (Yards) | " |
|  |  | 5 (Miles) | " |
|  |  | 6 (Microns) | " |
|  |  | 7 (Millimeters) | " |
|  |  | 8 (Centimeters) | " |
|  |  | 9 (Meters) | " |
|  |  | 10 (Kilometers) | " |
|  |  | 11 (Degrees – Landmark & Azimuth only) | " |
| Fractional Display Precision | 221 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Fractional Dimension Precision | 222 | LONGINT value | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Metric Unit Flag | 223 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Angular Unit | 224 | 0 (degrees) | [GetPrefInt](../../Functions/GetPrefInt.md) |
|  |  | 1 (radians) | " |
|  |  | 2 (gradians) | " |
| Round Fraction to Decimal | 225 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Dimension Rounding Base | 226 | 0 (1) | [GetPrefInt](../../Functions/GetPrefInt.md) |
|  |  | 1 (2.5) | " |
|  |  | 2 (5) | " |

### DXF Preference Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Auto Units | 300 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Units | 301 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| DXF Units Per Inch | 302 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Auto Model Space Scale | 303 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Model Space Scale | 304 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| 2D 3D Import Handling | 305 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Map Layers to Classes | 306 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Convert Mlines to Walls | 307 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Convert Rays and Xlines | 308 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Scale Dash Lengths | 309 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Dash Length Scale | 310 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Auto Block Attribute Handling | 311 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Block Attribute Handling | 312 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Auto Point Handling | 313 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Convert Points to Loci | 314 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Point Symbols are Guides | 315 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Map Colors to Line Weights | 316 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Set Line Colors Black | 317 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Paper Space Units | 318 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Auto Scale Dash Lengths | 319 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Group Record Fields | 320 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Auto Line Weight Handling | 321 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Convert Dimensions To Groups | 322 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Rays and Lines To Guides | 323 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Auto Center After Import | 324 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Center After Import | 325 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Use World Origin | 326 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Set Vectorworks Units To Match | 327 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Add Prefix To DXF Layers | 328 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Prefix To DXF Edit | 329 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| External Refs Handling | 330 | 0 (bind external refs) | [GetPrefInt](../../Functions/GetPrefInt.md) |
|  |  | 1 (ignore external refs) | " |
|  |  | 2 (create VW refs) | " |
|  |  | 3 (use layer import) | " |
| ADT Objects 2D View | 331 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Ignore Block Clipping | 334 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Conversion Ref | 335 | 0 (VW Conversion Res) |[GetPrefInt](../../Functions/GetPrefInt.md) |
|  |  | 1 (Low) |  |
|  |  | 2 (Medium) |  |
|  |  | 3 (High) |  |
|  |  | 4 (Very High) |  |
| Convert Tables To Worksheets | 338 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Import As Solid Line | 339 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Smallest Gap | 340 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Import Textures | 341 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Purge Unused Blocks | 344 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Purge Unused Layers | 345 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Purge Unused Dim Styles | 346 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Purge Unused Line Types | 347 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Purge Unused Materials | 348 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| CL Mapping Name | 349 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |
| GeoRef Import Type | 350 | 0 (None) | [GetPrefInt](../../Functions/GetPrefInt.md) |
|  |  | 1 (UseDocument) |  |
|  |  | 2 (User) |  |
|  |  | 3 (UserAndAplly) |  |
| GeoRef Import Type | 351 | STRING value | [GetPrefString](../../Functions/GetPrefString.md) |

## Structural Units

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Mass Units | 6821 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 0 (Milligram) | |
| | | 1 (Gram) | |
| | | 2 (Kilogram) | |
| | | 3 (Tonne) | |
| | | 4 (Ounce) | |
| | | 5 (Pound) | |
| | | 6 (Stone) | |
| | | 7 (Quarter) | |
| | | 8 (Hundred Weight UK) | |
| | | 9 (Hundred Weight US) | |
| | | 10 (Short Ton) | |
| | | 11 (Long Ton) | |
| | | 12 (Custom) | |
| Mass Unit Precision | 6822 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Show Unit Mark | 6823 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Current Unit Mark | 6824 | STRING (Read Only) | [GetPrefString](../../Functions/GetPrefString.md) |
| Unit Name | 6825 | STRING (Read Only) | [GetPrefString](../../Functions/GetPrefString.md) |
| Mass Unit Scale per Gram | 6826 | Real (Read Only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Force Unit Index | 6827 | Integer | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 0 (Newton) | |
| | | 1 (Kilonewton) | |
| | | 2 (Ounce Force) | |
| | | 3 (Pound Force) | |
| | | 4 (Custom) | |
| Force Unit Precision | 6828 | Integer | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Show Force Unit Mark | 6829 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Force Unit Mark | 6830 | STRING (Read Only) | [GetPrefString](../../Functions/GetPrefString.md) |
| Force Unit Name | 6831 | STRING (Read Only) | [GetPrefString](../../Functions/GetPrefString.md) |
| Force Unit Scale per Neuton | 6832 | REAL (Read Only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Distributed Mass Unit Index | 6833 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| | | 0 (Gram per Millimeter) | |
| | | 1 (Kilogram per Meter) | |
| | | 2 (Ounce per Inch) | |
| | | 3 (Pound per Foot) | |
| | | 4 (Custom) | |
| Distributed Mass Unit Precision | 6834 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Distributed Mass Unit Show Unit Mark | 6835 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Distributed Mass Unit Mark | 6836 | STRING | [GetPrefString](../../Functions/GetPrefString.md) |
| Distributed Mass Unit Name | 6837 | STRING (Read Only) | [GetPrefString](../../Functions/GetPrefString.md) |
| DistributedMassUnit Scale Grams per Millimeter | 6838 | REAL (Read Only) | [GetPrefReal](../../Functions/GetPrefReal.md) |

## Gradient and Image Fill Preference Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| Default Gradient Fill | 508 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Default Gradient Fill Angle | 512 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Default Gradient Fill Repeat | 513 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Default Gradient Fill Geometric Type | 515 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Default Gradient Fill Mirror | 516 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Default Image Fill Maintain Aspect Ratio | 517 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Default Image Fill | 518 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Default Image Fill Angle | 523 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Default Image Fill Repeat | 524 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Default Image Fill Mirror | 526 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Default Image Fill Flip | 527 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Default Image Fill I-Length | 532 | REAL (current units) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Default Image Fill J-Length | 533 | REAL (current units) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Default Fill Style | 528 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Default Fill Type | 529 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Default Hatch Fill | 530 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |

## Misc. Preference Selectors

| Preference | Selector | Preference Data Type | Function |
|------------|----------|----------------------|----------|
| RenderWorks Enabled | 240 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Disable RenderWorks | 241 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| PDF Page Object Paint Node Resolution | 270 | LONGINT (DPI) | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Don't Cache Plug-in Scripts | 407 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Auto Refresh Mode | 450 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Window Zoom Factor | 500 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Layer Options | 506 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Class Options | 507 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Hide Wall Cavity Threshold | 540 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Save Viewport Cache | 541 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Smooth Mesh | 542 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Mesh Crease Angle | 543 | REAL | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use Auto Draw Coord | 544 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Text Files in Plugin Editor | 560 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Release Version Integer | 570 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Symbol Tool Insert Mode | 580 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Symbol Tool Wall Insertion | 581 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Symbol Tool Alignement Mode | 582 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Parametric Enable State Eventing | 590 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Update Text Style Size | 685 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Hide Non Detail | 705 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| DVLP Position Locked | 709 | TRUE or FALSE (Read Only) | [GetPref](../../Functions/GetPref.md)  |
| Display Horizontal DPI | 1011 | REAL (read-only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Display Vertical DPI | 1012 | REAL (read-only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Screen Plane Mode | 1099 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Windows 64bit OS | 1100 | TRUE or FALSE (read-only) | [GetPref](../../Functions/GetPref.md)  |
| Is Autoplane Active | 1101 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Plane Mode is set to ScreenOrWorkingPlane | 1102 | TRUE or FALSE (read-only) | [GetPref](../../Functions/GetPref.md)  |
| Enable online content | 1104 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Enable Subscription Libraries | 1106 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Same Visibilities in All Panes | 1107 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| GeoRef Layer | 1117 | INTEGER | [GetPrefInt](../../Functions/GetPrefInt.md) |
| Compact Document Planes | 565 | TRUE or FALSE (write-only) | [GetPref](../../Functions/GetPref.md)  |
| Number of Document Planes | 566 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Max Document Planes | 567 | LONGINT | [GetPrefLongInt](../../Functions/GetPrefLongInt.md) |
| Plan Rotation Paused | 591 | TRUE or FALSE (read-only) | [GetPref](../../Functions/GetPref.md)  |
| Plan Rotation Paused Angle | 592 | REAL (read-only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Use Screen and Working Plane | 1102 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Perspective Cropped | 127 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Use Old 2D Pan and Zoom | 128 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Interactive Zoom Pan Mode | 6704 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Heliodon Interactive Render | 6706 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Clip Cube | 6707 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Write VS Binary Mode | 6708 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Hidden Line Surface Hatches | 280 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Hidden Line Text And Markers | 281 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Show Linear Direction Marker | 6719 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Feedback Scale Factor | 6716 | REAL (read-only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Feedback Resolution | 6717 | REAL (read-only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Document Window Resolution | 671 | REAL (read-only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Show Internal Origin Marker | 6723 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Always Show Current Tool On FDB | 9999 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)  |
| Display Hidden Objects Ghosted | 604 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Low Detail Exist Comp Objs | 605 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Low Detail Exist SymsPios | 606 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Low Detail Removed Comp Objs | 607 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Low Detail Removed SymsPios | 608 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| Alt Attrib Removed Objs | 609 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md) |
| CurrentLayerScale | 6757 | Real (read-only) | [GetPrefReal](../../Functions/GetPrefReal.md) |
| Parametric Regen Paused Plan Rotation | 591 | TRUE or FALSE  (read-only)| [GetPref](../../Functions/GetPref.md)  |
| Parametric Regen Paused Plan Rotation Angle | 592 | TRUE or FALSE  (read-only)| [GetPref](../../Functions/GetPref.md)  |
| Visibility of newly imported classes in Saved Views | 6841 | Integer| [GetPrefInt](../../Functions/GetPrefINt.md)  |
||| -1 invisibl||
|||0 visible||
||| 2 gray||
| Visibility of newly imported classes in Viewports | 6842 | Integer| [GetPrefInt](../../Functions/GetPrefInt.md)  |
||| -1 invisibl||
|||0 visible||
||| 2 gray||
| Visibility of newly imported classes in Graphics Legends | 6843 |Integer| [GetPrefInt](../../Functions/GetPrefInt.md)  |
||| -1 invisibl||
|||0 visible||
||| 2 gray||
| Use VGM Legacy | 10100 | TRUE or FALSE | [GetPref](../../Functions/GetPref.md)

### Notes:
#### Symbol Tool Insert Mode:
- 1 - Regular Insertion
- 2 - Offset Insertion
- 3 - Pick-up Mode

#### Symbol Tool Alignement Mode:
- 1 - Left
- 2 - Center
- 3 - Right
- 4 - Natural
