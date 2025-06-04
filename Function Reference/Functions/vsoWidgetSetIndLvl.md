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
[[User:CBM-c-|_c_]] (2022.01.05): There is a commented example of plug-in object (Python) with collapsable widgets here: [[User:CBM-c-/Plug-in_with_widget_basic_example]]

## Examples
==== VectorScript ====
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
==== Python ====
```python

```

## Version
Availability: from Vectorworks 2011

## Category
* [Object Events](../Categories/Object%20Events.md)
