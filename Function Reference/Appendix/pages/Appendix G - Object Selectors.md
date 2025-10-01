# Appendix G - Object Selectors

## Dimensions

| Object Setting | Selector | Setting Value | Function Type |
|----------------|----------|---------------|---------------|
| Dimension Standard | 0 | 1 (Arch) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 2 (ASME) | " |
| | | 3 (BSI) | " |
| | | 4 (DIN) | " |
| | | 5 (ISO) | " |
| | | 6 (JIS) | " |
| | | 7 (SIA) | " |
| | | 8 (ASME Dual Side-by-Side) | " |
| | | 9 (ASME Dual Stacked) | " |
| Arrows Inside | 3 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Use Text Box (Primary Value) | 5 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Show Primary Dimension Text | 6 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Display Starting Witness Line | 7 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Display Ending Witness Line | 8 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Leader Text (Primary) | 9 | 31 character STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Trailer Text (Primary) | 10 | 31 character STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Dimension Tolerancing | 11 | 0 (no tolerance) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (single tolerance) | " |
| | | 2 (double tolerance) | " |
| | | 3 (limit tolerance) | " |
| Dimension Text Offset | 15 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Dimension Text Font Size | 17 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Dimension Text Font Style | 19 | 0 (Plain) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (Bold) | " |
| | | 2 (Italic) | " |
| | | 4 (Underline) | " |
| | | 8 (Outline [Mac only]) | " |
| | | 16 (Shadow [Mac only]) | " |
| Dimension Precision (Primary) | 20 | For decimal precision: value is digits after decimal point. | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| | | For fractional precision: value is power of 2 for fractional denominator (1 for 1/2, 2 for 1/4, 3 for 1/8, 4 for 1/16, etc). | " |
| | | For angular precision: 1 for whole number, 2 (degrees min), 3 (degrees min sec), 5 (x.x angular units), 6 (x.xx), 7 (x.xxx), 8 (x.xxxx), 9 (x.xxxxx), 10 (x.xxxxxx), 11 (x.xxxxxxx), 12 (x.xxxxxxxx) | " |
| Dimension Precision (Secondary) | 21 | For decimal precision: value is digits after decimal point. | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| | | For fractional precision: value is power of 2 for fractional denominator (1 for 1/2, 2 for 1/4, 3 for 1/8, 4 for 1/16, etc). | " |
| | | For angular precision: value is not used. | " |
| Use Text Box (Secondary) | 22 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Show Secondary Dimension Text | 23 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Leader Text (Secondary) | 24 | 31 character STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Trailer Text (Secondary) | 25 | 31 character STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Dimension Type | 26 | 0 (Constrained) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (Unconstrained) | " |
| | | 2 (Ordinate) | " |
| | | 3 (Radial) | " |
| | | 4 (Diameter) | " |
| | | 5 (Angular) | " |
| Dimension Standard Name | 27 | STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Dimension Font ID | 28 | Font ID | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Calculate Dim Text Position | 29 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Force Dim Text Inside | 30 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Angle is Reference | 31 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Show Only Primary | 32 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Show Only Secondary | 33 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Top Tolerance Value | 34 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Bottom Tolerance Value | 35 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Top Tolerance String | 36 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Bottom Tolerance String | 37 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Use Tolerance Strings | 38 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Flip Text | 39 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Dimension Text Font Size | 40 | in points | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Dimension Text Rotation | 41 | 0 = Aligned, 1 = Horizontal, 2 = Horiz/Vertical | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Dim Text Offset Above Line | 43 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Dim Text Offset | 44 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Dimension Offset | 45 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Show Elevation Dimension (SIA Only) | 46 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Elevation Dimension Value (SIA Only) | 47 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Leader Text for Elevation Dimension (SIA Only) | 48 | 31 character STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Trailer Text for Elevation Dimension (SIA Only) | 49 | 31 character STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Leader Arrow Width | 50 | INTEGER value | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Text Style | 51 | Text Style Index | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Text Position | 52 | LONGINT value | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Witness Override Settings | 1235 | 0 = Standard | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 = Single Custom Length | |
| | | 2 = Multiple Custom Length | |
| | | 3 = Single Custom Offset | |
| | | 4 = Multiple Custom Offset | |
| Witness Line Length for Single Custom or Starting Multiple Custom | 1236 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Witness Line Length for Ending Witness Line | 1237 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Witness Line offset for Single Custom or Starting Multiple Custom | 1238 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Witness Line offset for Ending Witness Line | 1239 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Leader Line Visibility | 1240 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Leader Line Marker Type | 1241 | Marker Type | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Leader Line Marker Size | 1242 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Leader Line Marker Angle | 1243 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Leader Line Marker Thickness Basis | 1244 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Leader Line Marker Thickness | 1245 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Leader Line Marker Visibility | 1246 | -1 = Undefined Visibility | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 0 = Invisible | |
| | | 1 = Visible | |
| The width of the marker for the leader line | 1247 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Dimension Text Style | 1248 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Use SIA Custom Elevation Dimension | 1249 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Use Compact mode for Radial Dimensions | 1250 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Witness Line Perp to Chord | 1250 | TRUE or FALSE (read-only) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Arc Indicator | 1251 | TRUE or FALSE (read-only) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Clockwise Arc | 1252 | TRUE or FALSE (read-only) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Dim Note Text | 1233 | The note text under dimension line or value. | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Viewport RePosition Dimension Text | 1042 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Is Design Layer Section Viewport | 1043 | TRUE or FALSE (read only) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Display Flattened Viewport in Wireframe (OBSOLETE) | 1044 | TRUE or FALSE (read only) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| The viewport page symbol scale | 1045 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Viewport Detail Level low detail = 0, medium detail = 1, high detail = 2 | 1047 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Viewport Is Horizontal Section | 1048 | Read Only | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Viewport Is Section Viewport | 1054 | Read Only | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |

## Lights

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Light On | 50 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Brightness | 51 | REAL (percentage) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Shadow Casting On | 53 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Light Type | 55 | 1 (Directional) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 2 (Point) | " |
| | | 3 (Spotlight) | " |
| Light Pan Angle | 57 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Light Tilt Angle | 58 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Distance Falloff Type | 59 | 0 (None) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (Smooth) | " |
| | | 2 (Sharp) | " |
| Angular Falloff Type | 60 | 0 (none) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (Normal) | " |
| | | 2 (Smooth) | " |
| | | 3 (Sharp) | " |
| Light Spread Angle | 61 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Beam Angle | 62 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Light Lit Fog | 63 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Use Soft Shadows | 64 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Use Emitter | 1620 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Emitter Brightness | 1621 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Emitter Brightness Units | 1622 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 0 (Lumens) | |
| | | 1 (Candelas) | |
| | | 2 (Lux) | |
| | | 3 (Footcandles) | |
| Use Color Temperature | 1623 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Color Temperature | 1624 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Caustic Photons | 1625 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| | | 0 (None) | |
| | | 1000 (Low) | |
| | | 100000 (Medium) | |
| | | 1000000 (High) | |
| | | 10000000 (Very High) | |
| Use Caustics Only | 64 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |

## Symbols

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Symbol Light Multiplier | 100 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Symbol Scale Type | 101 | 1 (None) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (None) | " |
| | | 2 (Symmetric) | " |
| | | 3 (Asymmetric) | " |
| Symbol X Scale Factor | 102 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Symbol Y Scale Factor | 103 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Symbol Z Scale Factor | 104 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Symbol Insert Mode | 125 | 0 (On center of wall) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (On edge of wall) | " |
| Symbol Break Mode | 126 | 1 (Full break) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 2 (Full break no caps) | " |
| | | 3 (Half break) | " |
| | | 4 (no break) | " |
| Insert As Group | 127 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Use Class of Symbol Definition | 128 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Symbol Definition Insert Into Walls | 129 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Symbol Definition Page Based | 130 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Whether the symbol's height will be bound by story levels | 131 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |

## Roofs, Floors, Columns

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Slab Type | 172 | 1 (Roof) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 2 (Floor) | " |
| | | 3 (Column) | " |
| Slab Thickness | 173 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Slab Height | 174 | REAL (current units) (1) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Roof Edge Miter Type | 180 | 1 (Vertical) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 2 (Horizontal) | " |
| | | 3 (Compound) | " |
| Double Miter Ratio Value | 181 | REAL value (3) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Roof Rise | 182 | REAL (current units) (2) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Roof Run | 183 | REAL (current units) (2) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |

**Notes:**
1. Height is the bottom of the slab for floors and columns, elevation of the roof axis for roofs.
2. Roof only.
3. A value between 0 and 1 indicating the percentage of the miter which is vertical.

## Layer

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Layer Ambient Status | 150 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Layer Ambient Brightness | 151 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Layer Visibility | 153 | -1 (Invisible) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 0 (Normal) | " |
| | | 2 (Grayed) | " |
| Layer Type | 154 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Layer Printing DPI | 155 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Layer Renderworks Background | 591 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Layer Repaginate | 156 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Layer Height | 157 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Layer Thickness | 158 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Sheet Layer Title | 159 | STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| HDRI Layer | 592 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |

## Layer Link

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Source Layer Name | 160 | STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Project 2D Objects | 161 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Layer Expanded Sheet Name | 162 | STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|

## Viewports

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Projection Type | 1000 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Render Type | 1001 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Perspective Distance | 1002 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Scale | 1003 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Needs Update | 1004 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Project 2D | 1005 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Render Background | 1006 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| View Type | 1007 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Line Weight Scale | 1008 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Arrowhead Scale | 1009 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Dashed Line Scale | 1010 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Hatch Line Scale | 1011 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Design Text Scale | 1012 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Slash Thickness Scale | 1013 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Ambient light is ON | 1014 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Ambient Light Brightness | 1015 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| HDRI Viewport | 1019 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| 2D Class Attributes | 1020 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| 2D Other Attributes | 1021 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| 3D Class Fill Style | 1022 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| 3D Class Line Style | 1023 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Viewport x Position | 1024 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Viewport y Position | 1025 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Angle With Axis | 1026 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Shadow Wall Components | 1027 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Gray Transparent | 1028 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Flip Text | 1029 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Black and White | 1030 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Viewport Use Document Class Visibility | 1031 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Viewport Description | 1032 | STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Viewport Locator | 1033 | STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Viewport Is Linked | 1032 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Viewport Display Planar | 1035 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Viewport Foreground Render Type | 1036 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |

**Notes:**
1. View Type values are different then SetView

| viewUserDefined | 0 |
|-----------------|---|
| viewFront | 3 |
| viewBack | 4 |
| viewLeft | 5 |
| viewRight | 6 |
| viewTop | 7 |
| viewBottom | 8 |
| viewRightIso | 9 |
| viewLeftIso | 10 |
| viewRightRearIso | 11 |
| viewLeftRearIso | 12 |
| viewBottomRightIso | 13 |
| viewBottomLeftIso | 14 |
| viewBottomRightRearIso | 15 |
| viewBottomLeftRearIso | 16 |

## Walls

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Number of Cavities | 199 | INTEGER value (1) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Cavity is Pair | 240 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Cavity Fill Pattern | 260 | LONGINT index (0-71) (2) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Cavity Pen Weight | 280 | INTEGER value (mils) (2) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Cavity Pen Style | 300 | INTEGER index (2) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Cavity Left Offset | 320 | REAL (2) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Cavity Right Offset | 340 | REAL (2) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Hide Cavity Detail | 701 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Counterclockwise Round Wall | 570 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Round Wall Radius | 571 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Left Gross Area | 608 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Right Gross Area | 609 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Gross Area | 610 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Left Net Area | 611 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Right Net Area | 612 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Net Area | 613 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Left Average Height | 614 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Right Average Height | 615 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Wall Average Height | 616 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |

**Notes:**
1. Pass NIL to access default cavity values.
2. To access different cavities within a wall, add the zero-based cavity index to the selector value. For example, to access the right offset of cavity 6, specify 346 (340 + 6).

## Wall and Slab Styles

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Thickness | 1177 | REAL (1) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill | 1178 | LONGINT Pattern (0 to 71) or negative resource fill ref number | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Pen Style | 1179 | INTEGER Pattern (0 to 71) or dash (-1 to -10) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Pen Weight | 1180 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Fill Foreground Color | 1181 | INTEGER Color index (0 to 255) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Fill Background Color | 1182 | INTEGER Color index (0 to 255) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Pen Foreground Color | 1183 | INTEGER Color index (0 to 255) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Pen Background Color | 1184 | INTEGER Color index (0 to 255) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Opacity | 1185 | INTEGER Percent (0 to 100) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Use Fill Class Attributes | 1186 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Use Pen Class Attributes | 1187 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Use Class Opacity | 1188 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Cap Attributes Type | 1189 | INTEGER (0 = Wall line, 1 = Component lines) (2) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Caps | 1194 | INTEGER (0 = None, 1 = Start, 2 = End, 3 = Both) (2) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Class | 1195 | LONGINT Ref number | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Control Offset | 1196 | REAL (2) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Texture Set | 1197 | INTEGER (0 = Object textures, 1 = Component textures) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Overall Texture | 1198 | LONGINT Ref number | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Left Texture | 1199 | LONGINT Ref number (2) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Right Texture | 1200 | LONGINT Ref number (2) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Start Cap Texture | 1201 | LONGINT Ref number (2) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| End Cap Texture | 1202 | LONGINT Ref number (2) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Top Texture | 1203 | LONGINT Ref number | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Bottom Texture | 1204 | LONGINT Ref number | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Holes Texture | 1205 | LONGINT Ref number (2) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Sides Texture | 1206 | LONGINT Ref number (3) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Mark | 1207 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Description | 1208 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Function | 1209 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Exterior | 1210 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Load Bearing | 1211 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Fire Rating | 1212 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Combustible Construction | 1213 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Compartmentation | 1214 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| U-Value | 1215 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| R-Value | 1216 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Acoustic Rating | 1217 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Cost Index System | 1218 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Cost Index Code | 1219 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Model | 1220 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Manufacturer | 1221 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| URL | 1222 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|

**Notes:**
1. Wall Styles and read-only for Slab Styles
2. Wall Styles only
3. Slab Styles only

## Building Materials

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Is Volumetric | 1569 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Category | 1570 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Standard | 1571 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 0 (Omni Class) | |
| | | 1 (Uni Class) | |
| | | 2 (None) | |
| | | 3 (Txt Class) | |
| Reference ID | 1572 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Classification | 1573 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Manufacturer | 1574 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Product Model | 1575 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Product Name | 1576 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Product Description | 1577 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Product URL | 1578 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Specific Gravity | 1579 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Modulus of Elasticity | 1580 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Yield Strength | 1581 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Tensile Strength | 1582 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Specific Heat | 1583 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Emissivity | 1584 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Albedo | 1585 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Thermal Expansion Coefficient | 1586 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Lambda | 1587 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Embodied Carbon | 1588 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Sound Velocity | 1589 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Density | 1590 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Acoustic Impedance | 1591 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Uses Specific Gravity | 1592 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Modulus of Elasticity | 1593 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Yield Strength | 1594 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Tensile Strength | 1595 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Specific Heat | 1596 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Emissivity | 1597 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Albedo | 1598 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Thermal Expansion Coefficient | 1599 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Lambda | 1600 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Embodied Carbon | 1601 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Sound Velocity | 1602 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Density | 1603 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Uses Acoustic Impedance | 1604 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Is Surface Area Measure | 1605 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Description | 1606 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Mark | 1607 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Keynote | 1608 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Cost | 1609 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Source | 1610 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Finish | 1611 | STRING | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Slip Resistance | 1612 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Uses Slip Resistance | 1613 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |

## Plug-in Objects

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Insertion Mode | 123 | 0 (On center of wall) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (On edge of wall) | " |
| Break Mode | 124 | 1 (Full break) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 2 (Full break no caps) | " |
| | | 3 (Half break) | " |
| | | 4 (no break) | " |
| Font Style Enabled | 800 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| CreateCustomObject Don't Insert in Wall | 6709 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Parametric Internal ID | 1165 | INTEGER (read-only) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Parametric Localized Name | 1166 | STRING (read-only) | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Immediate Reset | 1167 | Write Only (Use on SDK parametric objects only!) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Hide Style Parameter check | 1168 | Read Only | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |

## 2D - 3D Status

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Object Is 3D | 650 | TRUE or FALSE (read-only) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Object Is 2D | 651 | TRUE or FALSE (read-only) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |

## Worksheets

| Object Setting | Selector | Setting Value | Function |
|----------------|----------|---------------|----------|
| Worksheet Header | 80 | STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Worksheet Footer | 81 | STRING value | [GetObjectVariableString](../../Functions/GetObjectVariableString.md)|
| Show Database Headers | 82 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Show Gridlines | 83 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Show Tabs | 84 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Auto-Recalculate | 85 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Default Font Index | 86 | INTEGER value | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Default Font Size | 87 | INTEGER value | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Top Print Margin | 88 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Left Print Margin | 89 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Bottom Print Margin | 90 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Right Print Margin | 91 | REAL value | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |

## Textures

| Object Setting | Selector | Data Type | Function |
|----------------|----------|-----------|----------|
| Texturable Object | 500 | TRUE or FALSE (read-only) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Expanded Material Set | 501 | TRUE or FALSE (1) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Material Size | 511 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Texture Bitmap Horiz Repeat | 524 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Texture Bitmap Vertical Repeat | 525 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Texture Bitmap Feature Size | 527 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Paint Width | 530 | LONGINT (pixels) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Paint Height | 531 | LONGINT (pixels) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Texture Space Type | 540 | 0 (Plane) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 1 (Sphere) | " |
| | | 2 (Cylinder) | " |
| | | 3 (Algorithmic/Perimeter) | " |
| | | 4 (Shader) | " |
| Texture Space Scale | 543 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Texture Space Rotation | 544 | REAL value (in radians) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Texture Space Use Start Cap | 546 | TRUE or FALSE (3) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Texture Space Use End Cap | 547 | TRUE or FALSE (3) | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Texture Space Part ID | 548 | INTEGER index (4) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Texture Space Radius | 549 | REAL (current units) (2) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Same Texture as Parent Wall | 704 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |

**Notes:**
1. Sets whether multiple textures can be applied to object (two for roof, three for walls).
2. Valid for sphere texture space only.
3. Valid for extrudes and sweeps only.
4. Index of multi-texturable object component.

## Gradient, Image, Tile and Hatch Fills

| Object Setting | Selector | Data Type | Function |
|----------------|----------|-----------|----------|
| Fill X Offset | 70 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill Y Offset | 71 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill I-Axis Length | 72 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill J-Axis Length | 73 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill Angle | 74 | REAL (radians) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill Repeat | 75 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Fill Mirror | 76 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Image Flip | 77 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Gradient Geometry Type | 78 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Image Aspect Ratio | 79 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Fill X Offset | 110 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill Y Offset | 111 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill I-Axis Length | 112 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Fill J-Axis Length | 113 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Image Width in Pixels | 534 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Image Width in Pixels | 535 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |

## Hatches

| Object Setting | Selector | Data Type | Function |
|----------------|----------|-----------|----------|
| Number of Levels | 660 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Is Transparent | 661 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Has Page Units | 662 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Rotate In Wall | 663 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Rotate In Symbol | 664 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |

## Materials

Selectors are here: [VS:Working_with_Materials](VS:Working_with_Materials#MaterialProperty_values)

## Misc.

| Object Setting | Selector | Data Type | Function |
|----------------|----------|-----------|----------|
| Is 2D Poly Clockwise | 652 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Object Fill Style | 695 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Object Fill Type | 696 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Object Use Local Mapping | 697 | BOOLEAN | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Object is Locked | 700 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Object is visible in high detail level | 750 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Object is visible in middle detail level | 751 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Object is visible in low detail level | 752 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Format is Visible | 900 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Text Is Linked To Record | 680 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Text Repeating Tab | 682 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Sweep Z Offset | 401 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Saved View Saves View Orientation | 450 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Saved View Saves Zoom and Pan | 456 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Saved View Saves Page Location | 451 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Saved View Saves Class Visibilities | 452 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Saved View Saves Layer Visibilities | 453 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Solid Has History | 630 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Solid Scale X | 631 | REAL scale factor | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Solid Scale Y | 632 | REAL scale factor | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Solid Scale Z | 633 | REAL scale factor | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Bitmap Object Compression | 532 | 0 (None) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| | | 1 (JPEG) | " |
| | | 2 (PNG) | " |
| | | 3 (PNG Monochrome) | " |
| Image Resource Compression | 533 | 0 (None) | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| | | 1 (JPEG) | " |
| | | 2 (PNG) | " |
| | | 3 (PNG Monochrome) | " |
| Set Specified Design Layer Visibility in All Saved Views | 454 | -1 (Invisible) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 0 (Normal) | " |
| | | 2 (Grayed) | " |
| | | 3 (Don't Save) | " |
| Set Specified Class Visibility in All Saved Views | 455 | -1 (Invisible) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| | | 0 (Normal) | " |
| | | 2 (Grayed) | " |
| | | 3 (Don't Save) | " |
| Mark Object as Structural | 702 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| First Aux List Object | 703 | HANDLE | [GetObjectVariableHandle](../../Functions/GetObjectVariableHandle.md) |
| Custom Object Area | 801 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Custom Object Perimeter | 802 | REAL (current units) | |
| Sketch Style | 1100 | -2 No Sketch | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| | | 0 Default | |
| | | Index of Sketch Style | |
| Set Specified Design Layer Visibility In All Viewports | 1017 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Set Specified Class Visibility In All Viewports | 1018 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Projection Type | 1110 | 0 (Lambert Conic) 1 (UTM) | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Lat./Long. vs XY Flag | 1111 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| First Import Flag | 1112 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| New Layer/Class Flag | 1113 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
| Model Space Scale | 1114 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Georeference Point | 1115 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Georeference Offset | 1116 | REAL | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Layer of First Import To Class | 1117 | LONGINT | [GetObjectVariableLongInt](../../Functions/GetObjectVariableLongInt.md) |
| Thumbnail View | 1152 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| Thumbnail Render | 1153 | INTEGER | [GetObjectVariableInt](../../Functions/GetObjectVariableInt.md) |
| RenderWorks Background Width | 1154 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| RenderWorks Background Height | 1155 | REAL (current units) | [GetObjectVariableReal](../../Functions/GetObjectVariableReal.md) |
| Planar Object Is Screen Object | 1160 | TRUE or FALSE | [GetObjectVariableBoolean](../../Functions/GetObjectVariableBoolean.md) |
