# Field Reference

The object fields are most reliable when each one answers a single question. Use short, literal instructions and name visible details that must be preserved.

## Overall Scene Request

Controls the room type, camera view, and broad composition. Leave it blank when the object cards already define the scene clearly.

Good example:

> Wide front-facing view of a contemporary bedroom with the bed centered on the back wall and clear views of both side walls.

Avoid repeating every object here. Detailed placement belongs in the object cards.

## Object Name

Use a short, stable name such as `bed`, `organic mirror`, `left wall panelling`, or `display wall`. The same name appears in the scene summary, diagrams, and final prompt.

## What should be extracted?

State exactly what should come from the reference and what should be ignored.

Good example:

> Mauve upholstered sofa only; exclude the wall, lamp, plant, rug, table, and app controls.

For a wall reference, say whether the full installation is required:

> Complete illuminated display-wall installation, including all niches, lighting, planters, and the lower fountain base.

## Count

Enter the number of copies required in the final scene. Use `1` for a unique object. If the count is greater than one, the diagrams expand the object into numbered instances.

## Position

Describe three things when placement matters:

1. Surface: back wall, left wall, right wall, floor, ceiling, or freestanding.
2. Horizontal and vertical location: left, center, right, upper, middle, or lower.
3. Depth: foreground, midground, rear, or against a wall.

Good example:

> Centered against the back wall, floor level, rear midground.

For wall-mounted objects, name the containing wall or panel:

> Mounted inside the central panel of the left wall, centered between the two sconces.

## Orientation

Describe the direction the object faces or the wall plane it follows.

Examples:

- `Facing camera`
- `Facing inward toward the center of the room`
- `Parallel to the back wall`
- `Mounted flush on the left wall and facing right into the room`

## Relationships

Use this field for a specific dependency between objects. Separate multiple relationships with commas.

Examples:

- `Bed directly in front of the back-wall feature`
- `Mirror inside the central panel of the left wall`
- `Sofa along the left wall, clear of the bed`

Relationships are more reliable when both objects use the same names everywhere.

## Adding more than one object from a reference

Select **Add Another Object From This Reference** when a single image supplies separate items. Give each item its own name, extraction scope, count, and placement. Do not combine unrelated objects into one card.

## Diagram choices

| Diagram | Best use |
| --- | --- |
| Combined Precision Map | General room compositions with several objects and walls |
| Top-Down Precision Map | Floor placement and left/right relationships |
| Wall and Surface Assignment | Confirming which wall or surface receives each object |
| Depth Bands | Foreground, midground, and rear placement |
| Orientation Map | Facing direction and rotation |
| Wall Elevation | Vertical placement on a specific wall |

If the tool reports that the model-generated diagrams failed validation, it shows deterministic diagrams built from the locked scene data. Review those diagrams normally; the warning does not mean that the scene data was lost.

## Output settings

The selected aspect ratio is the primary constraint. The resolution is a preferred target because some image generators choose their own supported dimensions.

For a custom output, write the ratio as `WIDTH:HEIGHT` and the resolution as `WIDTHxHEIGHT`. Both values must describe the same shape.
