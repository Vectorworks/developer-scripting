# 02. Draw 2D Geometry Primitives

## Description
Creates a small "attribute swatch" board that shows the same primitive shape
(a rectangle, oval, line and arc) with several different attribute
combinations. It's the same pattern the roadway and interior-elevation objects
use in `Common/Includes/*.py`: switch the active attributes, draw an object,
then use [`LNewObj`](../LNewObj.md) if you need a handle to
tune it further.

## What This Demonstrates
- Setting pen and fill attributes with [`PenSize`](../PenSize.md),
  [`PenFore`](../PenFore.md), [`FillFore`](../FillFore.md),
  [`FillPat`](../FillPat.md)
- Drawing common 2D primitives:
  [`Rect`](../Rect.md), [`Oval`](../Oval.md),
  [`Arc`](../Arc.md), [`Line`](../Line.md)
- Placing a caption next to each shape with [`TextOrigin`](../TextOrigin.md)
  and [`CreateText`](../CreateText.md)

## Python Script
```python
import vs

# Simple color palette (VW RGB is 0-65535 per channel).
kMax = 65535

def SetLineAttrs(weight_mils, r, g, b):
    """Set the current pen thickness (in mils) and pen color."""
    vs.PenSize(weight_mils)
    vs.PenFore(r, g, b)


def SetFillAttrs(pattern, r, g, b):
    """Set the fill pattern (0=none, 1=solid) and its foreground color."""
    vs.FillPat(pattern)
    vs.FillFore(r, g, b)


def Caption(x, y, msg):
    """Drop a small label under a shape."""
    vs.TextOrigin(x, y)
    vs.CreateText(msg)


def main():
    step = 3.0                  # spacing between columns
    y0, y1 = 2.0, 2.0 + 2.0     # bottom and top of the swatch shape

    # --- 1. Filled rectangle with a thick red pen ---------------------------
    SetLineAttrs(20, kMax, 0, 0)
    SetFillAttrs(1, kMax // 4, kMax // 4, kMax)      # light blue solid
    vs.Rect(0.0, y0, 2.0, y1)
    Caption(0.0, y0 - 0.4, 'Rect + solid fill')

    # --- 2. Oval with no fill and dashed pen --------------------------------
    SetLineAttrs(10, 0, 0, 0)
    SetFillAttrs(0, 0, 0, 0)                          # no fill
    vs.Oval(step, y0, step + 2.0, y1)
    Caption(step, y0 - 0.4, 'Oval, hollow')

    # --- 3. Straight line ---------------------------------------------------
    SetLineAttrs(30, 0, kMax // 2, 0)                 # green, heavy
    vs.MoveTo(2 * step, y0)
    vs.LineTo(2 * step + 2.0, y1)
    Caption(2 * step, y0 - 0.4, 'MoveTo/LineTo')

    # --- 4. Quarter-arc, clockwise ------------------------------------------
    SetLineAttrs(15, 0, 0, kMax // 2)
    SetFillAttrs(0, 0, 0, 0)
    # Arc(x1, y1, x2, y2, startAngle, sweep) fits an arc into the bounding rect.
    vs.Arc(3 * step, y0, 3 * step + 2.0, y1, 0, 90)
    Caption(3 * step, y0 - 0.4, 'Arc 0->90 deg')

    vs.Message('Primitive swatch drawn.')

main()
```

## Key VectorScript Functions Used
- [`Rect`](../Rect.md), [`Oval`](../Oval.md), [`Arc`](../Arc.md)
- [`MoveTo`](../MoveTo.md), [`LineTo`](../LineTo.md)
- [`PenSize`](../PenSize.md), [`PenFore`](../PenFore.md)
- [`FillPat`](../FillPat.md), [`FillFore`](../FillFore.md)
- [`TextOrigin`](../TextOrigin.md), [`CreateText`](../CreateText.md)
- [`Message`](../Message.md)
