# 07. Set Up Document Structure: Layers and Classes

## Description
Before you draw anything permanent, most Vectorworks scripts prep the document
by creating design layers at the correct scale and a set of classes that carry
the pen, fill and visibility rules. This example builds a small architectural
setup: three layers (Site, Floor Plan, Sheet) and four classes with distinct
graphic attributes, then drops a titled rectangle on each layer so you can see
which class is active.

## What This Demonstrates
- Creating layers with [`CreateLayer`](../CreateLayer.md)
  (type 1 = design, type 2 = sheet)
- Switching the active layer with [`Layer`](../Layer.md)
  and its scale with [`SetLScale`](../SetLScale.md)
- Creating a class on the fly by activating a name with
  [`NameClass`](../NameClass.md)
- Configuring class attributes with
  [`SetClPenFore`](../SetClPenFore.md),
  [`SetClFillFore`](../SetClFillFore.md),
  [`SetClLW`](../SetClLW.md),
  [`SetClUseGraphic`](../SetClUseGraphic.md)

## Python Script
```python
import vs

# Layer type constants (see CreateLayer).
kLayerType_Design = 1
kLayerType_Sheet  = 2

kMax = 65535  # full-channel RGB value


def ConfigureClass(name, penRGB, fillRGB, lineWeightMils):
    """Create (or activate) a class and set its default attributes."""
    # NameClass creates the class if it doesn't already exist.
    vs.NameClass(name)
    r, g, b = penRGB
    vs.SetClPenFore(name, r, g, b)
    r, g, b = fillRGB
    vs.SetClFillFore(name, r, g, b)
    vs.SetClLW(name, lineWeightMils)
    # Tell VW to actually use the class's graphic attributes on new objects.
    vs.SetClUseGraphic(name, True)


def MakeDesignLayer(name, scale):
    """Create a design layer at the given scale and make it active."""
    hLayer = vs.CreateLayer(name, kLayerType_Design)
    vs.SetLScale(hLayer, scale)
    return hLayer


def DropLabeledRect(x, y, width, height, className, caption):
    """Draw a labeled 2D rectangle in the given class."""
    vs.NameClass(className)
    vs.Rect(x, y, x + width, y + height)
    vs.TextOrigin(x + 0.1, y + height + 0.1)
    vs.CreateText(caption)


def main():
    # --- Classes ---------------------------------------------------------
    ConfigureClass('Walls-Exterior', penRGB=(0, 0, 0),
                   fillRGB=(kMax // 4, kMax // 4, kMax // 4),
                   lineWeightMils=30)
    ConfigureClass('Walls-Interior', penRGB=(kMax // 3, kMax // 3, kMax // 3),
                   fillRGB=(kMax // 2, kMax // 2, kMax // 2),
                   lineWeightMils=15)
    ConfigureClass('Furniture',      penRGB=(0, kMax // 2, 0),
                   fillRGB=(kMax // 5 * 4, kMax, kMax // 5 * 4),
                   lineWeightMils=10)
    ConfigureClass('Landscape',      penRGB=(0, kMax // 3, 0),
                   fillRGB=(kMax // 5 * 4, kMax // 5 * 4, kMax // 3),
                   lineWeightMils=8)

    # --- Layers ----------------------------------------------------------
    hSite = MakeDesignLayer('Site',       scale=200.0)     # 1:200 site plan
    hPlan = MakeDesignLayer('Floor Plan', scale=50.0)      # 1:50 architectural
    hSheet = vs.CreateLayer('Sheet-A101', kLayerType_Sheet)

    # --- Draw a swatch on each design layer ------------------------------
    vs.Layer('Site')
    DropLabeledRect(0, 0, 6, 4, 'Landscape', 'Site @ 1:200 (Landscape class)')

    vs.Layer('Floor Plan')
    DropLabeledRect(0, 0, 4, 3, 'Walls-Exterior', 'Plan @ 1:50 (Walls-Exterior)')
    DropLabeledRect(0.3, 0.3, 1.5, 1.0, 'Furniture', 'Furniture')

    vs.Message('3 layers + 4 classes created. Active layer: Floor Plan.')

main()
```

## Key VectorScript Functions Used
- [`CreateLayer`](../CreateLayer.md), [`Layer`](../Layer.md), [`SetLScale`](../SetLScale.md)
- [`NameClass`](../NameClass.md)
- [`SetClPenFore`](../SetClPenFore.md), [`SetClFillFore`](../SetClFillFore.md), [`SetClLW`](../SetClLW.md), [`SetClUseGraphic`](../SetClUseGraphic.md)
- [`Rect`](../Rect.md), [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`Message`](../Message.md)
