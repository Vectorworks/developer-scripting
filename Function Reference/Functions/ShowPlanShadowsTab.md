# ShowPlanShadowsTab

## Description
Opens the Pane Shadows tab of the Document Preferences dialog

```pascal
FUNCTION ShowPlanShadowsTab : BOOLEAN;
```

```python
def vs.ShowPlanShadowsTab():
    return BOOLEAN
```

## Examples
```pascal
resultOK := ShowPlanShadowsTab;
```
```python
import vs

# Opens the Pane Shadows tab of the Document Preferences dialog.
ok = vs.ShowPlanShadowsTab()
if ok:
    vs.Message('ShowPlanShadowsTab succeeded')
else:
    vs.Message('ShowPlanShadowsTab failed')
```

## Version
Availability: from Vectorworks 2014

## Category
* [Document Attributes](../Categories/Document%20Attributes.md)
