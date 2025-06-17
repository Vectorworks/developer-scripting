<p>
To increase the reliability and performance of Vectorworks, the way that dash patterns for dashed line types are stored internally is changing. The dash pattern table is being removed; instead, the patterns are being stored within the line type definition. Because of this, there is no dash index anymore; instead, the Internal Index of a dashed line type is used.</p>
<p>SDK and Vectorscript calls that used a dash index as an argument or return value are replaced with calls that use an Internal Index instead of a dash index. Some of the replacement functions already existed; new ones were added where necessary. For the new calls, the sign conventions still hold; functions that used or returned a negative dash index now use or return a negative Internal Index and those that used or returned positive dash index now use or return a positive Internal Index. The conventions for denoting solid or patterned lines are unchanged.</p>
<p>Plug-in developers must change their code to use the new calls; the old ones are being removed (SDK) or deprecated with error (Vectorscript). This is true even if those calls were being used to set a solid line or pattern.</p>
<p>The line style popup methods return Internal Index rather than dash index for dashed lines, as do functions that get an object’s pen style, etc. Plug-ins that stored those values in a record field, XML file, dialog settings, etc., will now be storing an Internal Index. This creates a problem because the plug-ins need to be able to move between files (e.g., work group referencing, copy and paste, project sharing) and Vectorworks doesn’t know the value is being stored so it can’t convert the Internal Index into one appropriate for the file. Moving between files was a problem when using dash indices (there was no guarantee that a given dashed line would exist in in a different file or have the same index in a new file), but it becomes more obvious when using internal indices.</p>
<p>SDK plug-ins that stored a dash index (either as a hard-coded value, a value in a record field, a value in an XML file, etc.) should be changed to store either the name of the line type or its definition (segments). Vectorscript plug-ins that stored a dash index should be changed to store the name of a line type. Both SDK and Vectorscript plug-ins may still use hard-coded segment values to create dash line types.</p>

## SDK Functions

### Removed SDK functions and their equivalents

The following table contains the removed SDK functions and their equivalents. Calls relating to worksheet cell borders that used the structure `TCellBorder` have new equivalents that use the structure `TCellBorderRefNum`. This was done to emphasize that the Style field is not a dash index.
Two new functions were added: `GetSimpleLineTypeDefinition` and `CreateOrFindSimpleLineType`. These were added to support developers who wish to store the dash definition. The functions allow plug-in developers to obtain the dash pattern definition and use that definition to create or find a dashed line type that looks the same as the original.

Below the table are the declarations for the new functions.

| Removed | Replacement | Notes |
|---------|-------------|-------|
| GetDefaultPenPat | GetDefaultPenPatN | Replacement exists |
| SetDefaultPenPat | SetDefaultPenPatN | Replacement exists |
| GetPenPat | GetPenPatN | Replacement exists |
| SetPenPat | SetPenPatN | Replacement exists |
| GetLineAttributeData | GetLineTypeAttributeData | Replacement exists |
| SetLineAttributeData | SetLineTypeAttributeData | Replacement exists |
| GetLineStyleChoice | GetLineTypeChoice | Replacement exists |
| SetLineStyleChoice | SetLineTypeChoice | Replacement exists |
| GetListBrowserItemDashStyle | GetListBrowserItemLineTypeRef | Replacement exists |
| SetListBrowserItemDashStyle | SetListBrowserItemLineTypeRef | Replacement exists |
| GetClPenPat | GetClPenPatN | Replacement exists |
| SetClPenPat | SetClPenPatN | Replacement exists |
| GetDashPat | GetCumulativeDashPat. See GetSimpleLineTypeDefinition to get definition that can be used to create line type with same pattern. | New. The dash pat returned has the cumulative segment values, NOT the dashes and gaps needed to create a line with the same pattern. |
|  | GetSimpleLineTypeDefinition | New, see description below table. |
|  | CreateOrFindSimpleLineType | New, see description below table. |
| SetDashPat | None | Obsolete prior to this reengineering. |
| GetDashStyleIndex | GetDashLineStyle | New |
| SetDashStyleName | SetDashLineTypeName | New |
| GetDashStyleName | GetDashLineTypeName | New |
| GetDLComponentPenStyles | GetComponentPenStylesN | Replacement exists |
| SetDLComponentPenStyles | SetComponentPenStylesN | Replacement exists |
| InsertNewDLComponent | InsertNewDLComponentN | New |
| GetComponentPenStyles | GetComponentPenStylesN | Replacement exists |
| SetComponentPenStyles | SetComponentPenStylesN | Replacement exists |
| InsertNewComponent | InsertNewComponentN | New |
| GetNumDashPats | None |   |
| AddDashPat | None | Obsolete prior to this reengineering. |
| DeleteDashPat | None | Obsolete prior to this reengineering. |
| Kludge calls with selectors: <br />kKludgeGetLineTypeFromDashIndex (4012), <br />kKludgeGetDashStyleIndexFromLineType (4013) | Validation functionality is provided by IsDashLineStyle | New |
| varHiddenLineDashStyle selector for GetProgramVariable, SetProgramVariable | varHiddenLineDashType | New, value is Sint32 |
| TCellBorder structure removed from SDK, new structure for SDK callers | TCellBorderRefNum | In new structure, Style field is negative InternalIndex if style is a dashed line. |
| GetWSCellAllBorders | GetWSCellAllBordersN | New |
| SetWSCellAllBorders | SetWSCellAllBordersN | New |
| SetWSCellBottomBorder | SetWSCellBottomBorderN | New |
| SetWSCellInsideHorizBorder | SetWSCellInsideHorizBorderN | New |
| SetWSCellInsideVertBorder | SetWSCellInsideVertBorderN | New |
| SetWSCellLeftBorder | SetWSCellLeftBorderN | New |
| SetWSCellOutlineBorder | SetWSCellOutlineBorderN | New |
| SetWSCellRightBorder | SetWSCellRightBorderN | New |
| SetWSCellTopBorder | SetWSCellTopBorderN | New |

The declarations for the new calls in the above table are listed below with the changed argument or return type(s) in **bold italics**. In cases where the original calls used a negative dash index, the new ones use a negative internal index. The first two calls are completely new.

* `Boolean GetSimpleLineTypeDefinition(const InternalIndex lineTypeRef, **DashPatDef**& outDashPat)`
  * Given a positive InternalIndex of a simple line type, returns its definition. The segs member of DashPatDef contains the vectors that define the dashes and spacing; these values can be used to find or create a dashed line type with the same look. The DashPatDef returned here can be used directly in CreateOrFindSimpleLineTypeDefinition.
* `InternalIndex CreateOrFindSimpleLineTypeDefinition(const **DashPatDef**& inDashPat)`
  * Returns the positive InternalIndex of a simple line type, given a dash pattern definition. Will look in default content and import if necessary. Will create line type if not found.
* **InternalIndex** `GetDashLineStyle(bool scaleWithThick, **const std::vector<double>**& theVectors)`
* `Boolean SetDashLineTypeName(**InternalIndex** lineTypeRef, const TXString& dashStyleName)`
* `TXString GetDashLineTypeName(**InternalIndex** lineTypeRef)`
* `Boolean GetDLComponentPenStylesN(Sint16 index, **InternalIndex**& outPenStyleLeft, **InternalIndex**& outPenStyleRight)`
* `Boolean SetDLComponentPenStylesN(Sint16 index, **InternalIndex** penStyleLeft, **InternalIndex** penStyleRight)`
* `Boolean InsertNewDLComponentN(Sint16 beforeIndex, WorldCoord width, Sint32 fill, Uint8 penWeightLeft, Uint8 penWeightRight, **InternalIndex** penStyleLeft, **InternalIndex** penStyleRight)`
* `Boolean InsertNewComponentN(MCObjectHandle object, short beforeComponentIndex, WorldCoord width, Sint32 fill, Uint8 leftPenWeight, Uint8 rightPenWeight, **InternalIndex** leftPenStyle, **InternalIndex** rightPenStyle)`
* `Boolean IsDashLineStyle(**InternalIndex** lineStyle)`
* `void GetWSCellAllBordersN(MCObjectHandle worksheet, const ViewPt& cell, **TCellBorderRefNum**& top, **TCellBorderRefNum**& left, **TCellBorderRefNum**& bottom, **TCellBorderRefNum**& right)`
* `void SetWSCellAllBordersN(MCObjectHandle worksheet, const ViewPt& topLeftCell, const ViewPt& bottomRightCell, **TCellBorderRefNum** top, **TCellBorderRefNum** left, **TCellBorderRefNum** bottom, **TCellBorderRefNum** right, **TCellBorderRefNum** insideVert, **TCellBorderRefNum** insideHorz)`
* `void SetWSCellBottomBorderN(MCObjectHandle worksheet, const ViewPt& topLeftCell, const ViewPt& bottomRightCell, **InternalIndex** style, Uint8 weight, ColorRef color)`
* `void SetWSCellInsideHorizBorderN(MCObjectHandle worksheet, const ViewPt& topLeftCell, const ViewPt& bottomRightCell, **InternalIndex** style, Uint8 weight, ColorRef color)`
* `void SetWSCellInsideVertBorderN(MCObjectHandle worksheet, const ViewPt& topLeftCell, const ViewPt& bottomRightCell, **InternalIndex** style, Uint8 weight, ColorRef color)`
* `void SetWSCellLeftBorderN(MCObjectHandle worksheet, const ViewPt& topLeftCell, const ViewPt& bottomRightCell, **InternalIndex** style, Uint8 weight, ColorRef color)`
* `void SetWSCellOutlineBorderN(MCObjectHandle worksheet, const ViewPt& topLeftCell, const ViewPt& bottomRightCell, **InternalIndex** style, Uint8 weight, ColorRef color)`
* `void SetWSCellRightBorderN(MCObjectHandle worksheet, const ViewPt& topLeftCell, const ViewPt& bottomRightCell, **InternalIndex** style, Uint8 weight, ColorRef color)`
* `void SetWSCellTopBorderN(MCObjectHandle worksheet, const ViewPt& topLeftCell, const ViewPt& bottomRightCell, **InternalIndex** style, Uint8 weight, ColorRef color)`

## Vectorscript Functions

### Deprecated Vectorscript functions and their equivalents

| Deprecated | Replacement | Notes |
|------------|-------------|-------|
| GetLineStyleChoice | GetLineTypeChoice | Replacement exists |
| SetLineStyleChoice | SetLineTypeChoice | Replacement exists |
| GetLineAttributeData | GetLineTypeAttriData | Replacement exists |
| SetLineAttributeData | SetLineTypeAttriData | Replacement exists |
| InsertNewComponent | InsertNewComponentN | New |
| SetComponentPenStyles | SetCompPenStylesN | Replacement exists |
| GetComponentPenStyles | GetCompPenStylesN | Replacement exists |
| SetLBItemDashStyle | SetLBItemLineType | Replacement exists |
| GetLBItemDashStyle | GetLBItemLineType | Replacement exists |
| InsertNewDLComponent | InsertNewDLCompN | New |
| GetDLComponentPenStyles | GetDLCompPenStylesN | New |
| SetDLComponentPenStyles | SetDLCompPenStylesN | New |
| SetDashStyleName | SetDashLineTypeName | New |
| GetDashStyleName | GetDashLineTypeName | New |
| GetDashStyle | GetDashStyleN | New |
| GetDashStyleIndex | GetDashStyleIndexN | New |
| GetDashDataValPairAt | GetDashDataValPrAtN | New |
| GetNumDashDataPairs | GetNumDashDataPairsN | New |
| GetLS | GetLSN | Deprecated in 2013, replacement exists |
| SetLS | SetLSN | Deprecated in 2013, replacement exists |
| GetClLS | GetClLSN | Deprecated in 2013, replacement exists |
| SetClLS | SetClLSN | Deprecated in 2013, replacement exists |
| FPenPat | FPenPatN | Deprecated in 2013, replacement exists |
| PenPat | PenPatN | Deprecated in 2013, replacement exists |
| NumDashStyles | None |   |
| PrefInt for hidden line dash style; selector 66 | Use PrefLongInt with selector 197 instead | Won't give a deprecation error |
| SetWSCellTopBorder | SetWSCellTopBN | New |
| SetWSCellBottomBorder | SetWSCellBottomBN | New |
| SetWSCellRightBorder | SetWSCellRightBN | New |
| SetWSCellLeftBorder | SetWSCellLeftBN | New |
| SetWSCellInsideHorizBorder | SetWSCellInsideHzBN | New |
| SetWSCellOutlineBorder | SetWSCellOutlineBN | New |
| SetWSCellInsideVertBorder | SetWSCellInsideVtBN | New |

The declarations for the new calls in the above table are listed below with the changed argument or return type(s) in **bold italics**. In cases where the original calls used a negative dash index, the new ones use a negative internal index (LONGINT).

* `FUNCTION InsertNewComponentN (object: HANDLE; beforeComponentIndex: INTEGER; width: REAL; fill: LONGINT; leftPenWeight: INTEGER; rightPenWeight: INTEGER; leftPenStyle: **LONGINT**; rightPenStyle: **LONGINT**): BOOLEAN;`
* `FUNCTION InsertNewDLCompN (beforeIndex: INTEGER; widthDistance: REAL; fill: LONGINT; penWeightLeft: INTEGER; penWeightRight: INTEGER; penStyleLeft: **LONGINT**; penStyleRight: **LONGINT**): BOOLEAN;`
* `FUNCTION GetDLCompPenStylesN(index: INTEGER; penStyleLeft: **LONGINT**; penStyleRight: **LONGINT**): BOOLEAN;`
* `FUNCTION SetDLCompPenStylesN(index: INTEGER; penStyleLeft: **LONGINT**; penStyleRight: **LONGINT**): BOOLEAN;`
* `FUNCTION SetDashLineTypeName (DashStyleIndex: **LONGINT**; DashStyleName: STRING): BOOLEAN;`
* `FUNCTION GetDashLineTypeName (DashStyleIndex: **LONGINT**): STRING;`
* `FUNCTION GetDashStyleN (swt: BOOLEAN; numPairs: INTEGER; pair1: REAL; pair2: REAL; pair3: REAL; pair4: REAL; pair5: REAL;): **LONGINT**;`
* `FUNCTION GetDashStyleIndexN(swt: BOOLEAN; numPairs: INTEGER; pair1: REAL; pair2: REAL; pair3: REAL; pair4: REAL; pair5: REAL;): **LONGINT**;`
* `FUNCTION GetDashDataValPrAtN (dashStyleIndex: **LONGINT**; dataIndex: INTEGER; dash: REAL; gap: REAL): BOOLEAN;`
* `FUNCTION GetNumDashDataPairsN(dashIndex: **LONGINT**; swt: BOOLEAN): INTEGER;`
* `PROCEDURE SetWSCellTopBN(worksheet: HANDLE; topRow: INTEGER; leftColumn: INTEGER; bottomRow: INTEGER; rightColumn: INTEGER; style: **LONGINT**; weight: INTEGER; color: LONGINT);`
* `PROCEDURE SetWSCellLeftBN(worksheet: HANDLE; topRow: INTEGER; leftColumn: INTEGER; bottomRow: INTEGER; rightColumn: INTEGER; style: **LONGINT**; weight: INTEGER; color: LONGINT);`
* `PROCEDURE SetWSCellBottomBN(worksheet: HANDLE; topRow: INTEGER; leftColumn: INTEGER; bottomRow: INTEGER; rightColumn: INTEGER; style: **LONGINT**; weight: INTEGER; color: LONGINT);`
* `PROCEDURE SetWSCellRightBN(worksheet: HANDLE; topRow: INTEGER; leftColumn: INTEGER; bottomRow: INTEGER; rightColumn: INTEGER; style: **LONGINT**; weight: INTEGER; color: LONGINT);`
* `PROCEDURE SetWSCellOutlineBN(worksheet: HANDLE; topRow: INTEGER; leftColumn: INTEGER; bottomRow: INTEGER; rightColumn: INTEGER; style: **LONGINT**; weight: INTEGER; color: LONGINT);`
* `PROCEDURE SetWSCellInsideHzBN(worksheet: HANDLE; topRow: INTEGER; leftColumn: INTEGER; bottomRow: INTEGER; rightColumn: INTEGER; style: **LONGINT**; weight: INTEGER; color: LONGINT);`
* `PROCEDURE SetWSCellInsideVtBN(worksheet: HANDLE; topRow: INTEGER; leftColumn: INTEGER; bottomRow: INTEGER; rightColumn: INTEGER; style: **LONGINT**; weight: INTEGER; color: LONGINT);`
