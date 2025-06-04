# SetStaticTextColorN

```pascal
PROCEDURE SetStaticTextColorN(
				dialogID    : LONGINT;
				componentID : LONGINT;
				tint        : INTEGER);
```

```python
def vs.SetStaticTextColorN(dialogID, componentID, tint):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|dialogID|LONGINT|   |
|componentID|LONGINT|   |
|tint|INTEGER|Tint number. See Appendix for the available values.|

## Remarks
List of available tints as of VW2023:

<code lang="cpp">
eDefaultTint = 0
eDisabledTint = 1
eRotatedCoordTint = 2
ePageBasedSymTint = 3
ePluginSymTint = 4
eGroupSymTint = 5
eAllLayersTint = 6
eCustomItem1Tint = 7

eGenericRedTint = 200
eGenericGreenTint = 201
eGenericBlueTint = 203
eGenericOrangeTint = 204
eGenericYellowTint = 205
eGenericBrownTint = 206
eGenericPurpleTint = 207
eGenericPinkTint = 208
eGenericGrayTint = 209
eGenericBlackTint = 210
eGenericWhiteTint = 211
</code>
A more frequently updated tint list can be found by looking for the EUiControlTextTint enumeration in the MiniCadCallbacks.h file.

## Version
Availability: from Vectorworks 2023

## Category
* [Dialogs - Modern](../Categories/Dialogs%20-%20Modern.md)
