# vstSetModeHelpBase

```pascal
PROCEDURE vstSetModeHelpBase(inTextRsrcIDBase : INTEGER);
```

```python
def vs.vstSetModeHelpBase(inTextRsrcIDBase):
    return None
```

## Parameters
|Name|Type|Description|
|---|---|---|
|inTextRsrcIDBase|INTEGER|   |

## Examples
```pascal
{set the beginning baloon help string}
vstSetModeHelpBase (11045);
BeginModeButtonsText;
SetModeButtonTextN( GetPluginString( kOval ), 				GetPluginString( 7001 ), 0 );
SetModeButtonTextN( GetPluginString( kRectangular ), 		GetPluginString( 7002 ), 0 );
SetModeButtonTextN( GetPluginString( kRegularPolygon ), 	GetPluginString( 7003 ), 0 );

{set the beginning baloon help string}
vstSetModeHelpBase (kModeButton_1_ID);
BeginModeButtonsText;
SetModeButtonTextN( GetPluginString( 3001 ), GetPluginString( 8001 ), 0 );
SetModeButtonTextN( GetPluginString( 3002 ), GetPluginString( 8002 ), 0 );
SetModeButtonTextN( GetPluginString( 3003 ), GetPluginString( 8003 ), 0 );

	BeginModeButtonsText;
	SetModeButtonText( GetPluginString( 6000 ), 2 );
	EndModeButtonsText;
	vstSetPtBehavior(kPolyPointTool);
	vstSetModeHelpBase( -2322 );
END;
```
```python
import vs

inTextRsrcIDBase = 1

vs.vstSetModeHelpBase(inTextRsrcIDBase)
```

## Version
Availability: from All Versions

This is drop-in function.

## Category
* [Tool Events](../Categories/Tool%20Events.md)
