# vsoWidgetSetIndLvl

## Description
Sets the indenting level of the specified parameter on the Object Info Palette.

```pascal
PROCEDURE vsoWidgetSetIndLvl(
				widgetID    : LONGINT;
				indentLevel : LONGINT);
```

```python
def vs.vsoWidgetSetIndLvl(widgetID, indentLevel):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|widgetID|LONGINT|   |
|indentLevel|LONGINT|   |

## Remarks
\_c\_ (2022.01.05): There is a commented example of plug-in object (Python) with collapsable widgets here: [[User:CBM-c-/Plug-in_with_widget_basic_example]]

## Examples
#### VectorScript ####
```pascal
5: {kObjOnInitXProperties}
        BEGIN
            result := SetObjPropVS(8, TRUE); {kObjXPropHasUIOverride}
            result := SetObjPropVS(12, TRUE); {kObjXHasCustomWidgetVisibilities} {send kObjOnWidgetPrep}
            result := vsoInsertAllParams;
            result := vsoInsertWidget (3, 12 {kWidgetButton}, 100, 'Edit List...', 0);
 
            result := vsoPrmName2WidgetID( '', 'text', widgetID ); {empty string means the record of this parametric}
            vsoWidgetSetIndLvl( 100, 1 );
            vsoWidgetSetIndLvl( widgetID, 1 );
        END;
 
41: {kObjOnWidgetPrep}
	BEGIN
            result := vsoPrmName2WidgetID( '', 'text', widgetID ); {empty string means the record of this parametric}

            vsoWidgetSetVisible( widgetID, PUseCustomText );
            vsoWidgetSetEnable( 100, PUseCustomText );
	END;
```
#### Python ####
```python

```

```pascal
BEGIN
	vsoWidgetSetIndLvl( architHgtInfoWidgetID,			widgetIndent );

widgetIndent := 1;
vsoWidgetSetIndLvl( kFillButtonWidgetID,  widgetIndent );
IF ( p__version < 1900 ) & (p__version <> 0) THEN
BEGIN
  gShowAisle := False;
  if (gPluginH <> nil) then

vsoWidgetSetEnable( wigID_LineMode, NOT pWasConvToOutline );
vsoWidgetSetVisible( wigID_LineWidth,	pLineMode );
vsoWidgetSetVisible( kConvToOutlineBtn_ID,	pLineMode );
vsoWidgetSetEnable( kConvToOutlineBtn_ID, (pioHand <> NIL) );	{//// Fix for VB-181191: Disable Button in Tool Prefs dialog }
vsoWidgetSetIndLvl( wigID_LineWidth, 1 );
vsoWidgetSetIndLvl( kConvToOutlineBtn_ID, 1 );
```
```python
vs.vsoWidgetSetIndLvl( kWidgetID_NorthArrow,  	widgetCheckBoxIndent )
vs.vsoWidgetSetIndLvl( kWidgetID_NorthNo,  		widgetTextIndent )
```
See also in tutorials: [Plug-in with widgets, basic example (Python)](../../Common/Tasks/Parametrics/Plug-in%20with%20widget%20basic%20example.md)

## Version
Availability: from Vectorworks 2011

## Category
* [Object Events](../Categories/Object%20Events.md)
