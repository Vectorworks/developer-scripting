# 01. Draw a Room with Walls

## Description
Draws a rectangular room from four walls and sets a consistent overall height on
each of them. The script is written the same way the sample plug-in objects in
`Common/Includes` build walls: draw the wall, keep the handle returned by
`vs.LNewObj()`, and configure it before moving on to the next segment.

## What This Demonstrates
- Creating [`Wall`](../Wall.md) segments from `(x1, y1)` to `(x2, y2)`
- Retrieving the handle of the object just placed with [`LNewObj`](../LNewObj.md)
- Setting the top/bottom height of every wall with [`SetWallOverallHeights`](../SetWallOverallHeights.md)
- Closing a wall's ends with [`WallCap`](../WallCap.md)
- Routing everything through a specific class using [`NameClass`](../NameClass.md)

## Python Script
```python
import vs

def DrawRoom(originX, originY, width, depth, wallHeight):
    """Draw a closed 4-wall room with the given footprint and height.

    All coordinates are in document units. Corners are placed counter-clockwise
    starting at the lower-left, so wall normals point outward.
    """
    # Route new walls through a dedicated class so they can be styled together.
    vs.NameClass('Walls-Exterior')

    # Four corners of the room, counter-clockwise.
    p1 = (originX,         originY)
    p2 = (originX + width, originY)
    p3 = (originX + width, originY + depth)
    p4 = (originX,         originY + depth)

    segments = ((p1, p2), (p2, p3), (p3, p4), (p4, p1))

    for (ax, ay), (bx, by) in segments:
        vs.Wall(ax, ay, bx, by)
        wallH = vs.LNewObj()

        # Uniform top/bottom heights: bound to no story, no offset, height = wallHeight.
        vs.SetWallOverallHeights(wallH, 0, 0, '', wallHeight,
                                 0, 0, '', wallHeight)

        # Square-cut ends so adjacent walls miter cleanly.
        vs.WallCap(False, False, False, 0, 0)


def main():
    # Reset origin and draw a 6m x 4m room, 2.7m tall.
    DrawRoom(originX=0, originY=0, width=6.0, depth=4.0, wallHeight=2.7)

    # A smaller room next to the first one.
    DrawRoom(originX=6.5, originY=0, width=3.5, depth=4.0, wallHeight=2.7)

    vs.Message('Two rooms drawn.')

main()
```

## Key VectorScript Functions Used
- [`Wall`](../Wall.md) — creates a straight wall segment
- [`LNewObj`](../LNewObj.md) — returns the last object just created
- [`SetWallOverallHeights`](../SetWallOverallHeights.md) — sets top/bottom heights
- [`WallCap`](../WallCap.md) — configures the end caps
- [`NameClass`](../NameClass.md) — activates a class for subsequent objects
- [`Message`](../Message.md) — writes a short status to the message bar
