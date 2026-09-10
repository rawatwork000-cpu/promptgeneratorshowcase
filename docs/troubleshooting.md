# Troubleshooting

## An image will not upload

Confirm that the file is JPG, JPEG, PNG, or WEBP and smaller than 20 MB. Re-export files that have an image extension but cannot be opened as a valid image.

## The reference IDs are in the wrong order

Start a new scene and reorder the thumbnails before selecting **Upload & Lock References**. Reference order cannot be changed after it is locked.

## The final scene includes unwanted items from a reference

Tighten the extraction scope. Name the required object first, then list the surrounding items to exclude.

Example:

> Sofa only; exclude the wall, lamp, plant, rug, table, and interface controls.

## An object appears on the wrong wall

Write the surface in the Position field and repeat the dependency in Relationships.

Example:

> Position: Center of the left wall, middle height.
>
> Relationship: Mounted inside the central panel of the left wall.

Regenerate the diagrams and confirm the wall assignment before continuing.

## The diagram does not match the intended layout

Use **Edit Layout** and describe one correction at a time. Regenerate the diagrams after each material change. Select a diagram only after its wall, depth, and facing information agree with the scene summary.

## A diagram-validation warning appears

When a generated diagram does not pass validation, the tool displays deterministic diagrams created from the locked scene data. Review the displayed diagrams and continue if their assignments are correct.

## The exact pixel dimensions are different

The aspect ratio is the primary image constraint. Some generators do not support every requested resolution and return their closest native size. Confirm the shape first, then upscale or resize the accepted result if exact dimensions are required.

## The generated image crops a side object

Use a wider aspect ratio or move the object from `foreground` to `midground`. State that both side walls and the full object must remain visible. A 16:9 frame may still crop furniture placed close to the camera.

## The mirror or wall art is simplified

Add the distinguishing features to the extraction scope and preserve-details wording: silhouette, frame material, backlight, shelves, and position inside the wall panel. Keep the object large enough in the composition for those details to remain visible.

## Object Output is unavailable

Complete the Scene Builder first. Object Output uses the objects already registered in the current scene.

## The result is visually polished but structurally wrong

Return to the scene summary and diagram rather than adding more style language to the final prompt. Correct the wall assignment, depth, orientation, or relationship that caused the structural error.
