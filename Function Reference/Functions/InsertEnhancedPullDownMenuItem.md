# InsertEnhancedPullDownMenuItem

## Description
<b>[[VS:Vectorworks 2012 Deprecated Functions|DEPRECATED after Vectorworks2012]]</b>. See [[VS:InsertEnhanPullDownMenuItem|InsertEnhanPullDownMenuItem]] for a replacement.

Inserts the item into the specified Layout Manager created with [[VS:CreateEnhancedPullDownMenu| CreateEnhancedPullDownMenu]]

```pascal
FUNCTION InsertEnhancedPullDownMenuItem(
				dialogID    : LONGINT;
				componentID : LONGINT;
				strName     : STRING;
				iIconID     : INTEGER): INTEGER;
```

```python
def vs.InsertEnhancedPullDownMenuItem(dialogID, componentID, strName, iIconID):
    return INTEGER
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|strName|STRING|   |
|iIconID|INTEGER|   |

## Examples
#### VectorScript ####
```pascal
PROCEDURE CreateControlsTest;
CONST

    { control IDs}
    kCreateEnhancedPullDownMenu          = 20;

VAR
    dialog            :INTEGER;

PROCEDURE Dialog_Handler(VAR item :LONGINT; data :LONGINT);
VAR
result : INTEGER;
            
BEGIN
    CASE item OF
        SetupDialogC: BEGIN

            result := InsertEnhancedPullDownMenuItem( dialog, kCreateEnhancedPullDownMenu, 'kCreateEnhancedPullDownMenu choice', 128 );

        END;
    END;
END;


BEGIN
    dialog := CreateLayout( 'InsertEnhancedPullDownMenuItem Test', TRUE, 'OK', 'Cancel' );

    {create controls}
    CreateEnhancedPullDownMenu( dialog, kCreateEnhancedPullDownMenu, 24, TRUE );

    {set relations}
    SetFirstLayoutItem( dialog, kCreateEnhancedPullDownMenu );

    IF RunLayoutDialog( dialog, Dialog_Handler ) = 1 then BEGIN
    END;

END;
RUN( CreateControlsTest );
```
#### Python ####
```python

```

## Version
Availability: from VectorWorks12.5
Deprecated: [[VS:Vectorworks 2012 Deprecated Functions|Vectorworks 2012]]

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
