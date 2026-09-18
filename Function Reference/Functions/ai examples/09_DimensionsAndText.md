# 09. Dimensioning and Text Annotation

## Description
Builds a small "measured drawing" — a rectangle representing a room, a locus
at each corner, a text callout, and horizontal + vertical linear dimensions.
This is the pattern used by the drawing-border and grid-bubble plug-ins in
`Common/Includes`.

## What This Demonstrates
- Creating linear dimensions with
  [`LinearDim`](../LinearDim.md) (horizontal + vertical)
- Dropping locus markers at key points with
  [`Locus`](../Locus.md)
- Formatting text with [`TextFont`](../TextFont.md),
  [`TextSize`](../TextSize.md) and
  [`TextOrigin`](../TextOrigin.md)

## Python Script
```python
import vs

# LinearDim flags. See Appendix E in the docs for the full bit table.
kDim_Horizontal = 1     # dimension along X
kDim_Vertical   = 2     # dimension along Y

# Arrow style: 0 = simple filled-triangle arrow.
kArrow_Default  = 0

# Text-flag bits: 771 selects "text above the line" with associative behaviour;
# it's the same value used by the plug-ins in Common/Includes.
kTextFlag_AboveAssoc = 771


def DrawRoomWithDims(x, y, width, depth, roomLabel, dimOffset=0.4):
    """Draw a rectangle plus a horizontal and vertical dimension."""
    # 1. Draw the room outline.
    vs.Rect(x, y, x + width, y + depth)

    # 2. Corner loci as reference marks (visible only in Snap-Loci mode).
    vs.Locus(x,          y)
    vs.Locus(x + width,  y)
    vs.Locus(x + width,  y + depth)
    vs.Locus(x,          y + depth)

    # 3. Room label, centred above the rectangle.
    vs.TextFont(vs.GetFontID('Arial'))
    vs.TextSize(10)
    vs.TextOrigin(x + width / 2 - 0.7, y + depth + dimOffset)
    vs.CreateText(roomLabel)

    # 4. Horizontal dimension below the room.
    vs.LinearDim(x,         y,
                 x + width, y,
                 -dimOffset,                    # negative = below the line
                 kDim_Horizontal,
                 kArrow_Default,
                 kTextFlag_AboveAssoc,
                 0.0)

    # 5. Vertical dimension on the right side.
    vs.LinearDim(x + width, y,
                 x + width, y + depth,
                 dimOffset,                     # positive = to the right
                 kDim_Vertical,
                 kArrow_Default,
                 kTextFlag_AboveAssoc,
                 0.0)


def main():
    DrawRoomWithDims(x=0.0, y=0.0, width=6.0, depth=4.0, roomLabel='Kitchen')
    DrawRoomWithDims(x=7.0, y=0.0, width=3.5, depth=4.0, roomLabel='Pantry')

    vs.Message('Rooms with dimensions drawn.')

main()
```

## Key VectorScript Functions Used
- [`LinearDim`](../LinearDim.md)
- [`Rect`](../Rect.md), [`Locus`](../Locus.md)
- [`CreateText`](../CreateText.md), [`TextOrigin`](../TextOrigin.md), [`TextSize`](../TextSize.md), [`TextFont`](../TextFont.md)
- [`GetFontID`](../GetFontID.md)
- [`Message`](../Message.md)
