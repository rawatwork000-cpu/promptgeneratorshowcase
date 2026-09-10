# User Guide

This guide covers the complete workflow from reference selection to a final concept image.

## Before you begin

Prepare clear reference images with visible shapes, materials, and colors. Crop away app controls, watermarks, and unrelated objects when possible. Decide which image will supply each object or wall treatment.

The tool accepts JPG, JPEG, PNG, and WEBP files. A project can contain up to 20 references, with a maximum size of 20 MB per image.

## 1. Upload and order the references

Open the [Visual Prompt Generator](https://prompt-generator-iota-seven.vercel.app/) and add all reference images. Drag the thumbnails into the correct order before selecting **Upload & Lock References**.

![Reference upload screen](../image/1.png)

After upload, each file receives a stable reference ID such as `REF_1` or `REF_2`. The final prompt uses these IDs, so keep the same file order when you move to the image generator.

![Locked reference registry](../image/3.png)

## 2. Define the objects

Complete one object card for each reference. Describe what the tool should use and where it belongs in the final scene. Add another card when one reference contains more than one required object.

![Object intake form](../image/4.png)

Use the optional overall scene request only when you need to control the room type, camera view, or general composition. The individual object fields should contain the placement details that must not change.

See the [Field Reference](field-reference.md) for examples of every input.

## 3. Review the scene

The scene summary lists every object with its reference, count, position, orientation, and relationships. Check this screen carefully. A wrong assignment at this stage will carry into the diagram and final prompt.

![Scene review](../image/6.png)

When the summary is correct, select **Generate Diagram Options**.

## 4. Choose a spatial diagram

The diagrams show the same scene from different planning views. For most room compositions, start with **Combined Precision Map** because it includes the wall assignment, top-down placement, depth, and facing direction.

![Combined Precision Map](../image/7.png)

Choose another diagram when a specific relationship is clearer in that view. Wall elevations are useful for vertical placement; the depth map is useful for foreground and background separation.

If a position is wrong, use **Edit Layout**, describe the correction in one direct sentence, regenerate the diagrams, and review them again.

![Layout correction controls](../image/10.png)

Select the best diagram and continue.

## 5. Choose the output format

Select the aspect ratio that matches the intended use.

![Output settings](../image/12.png)

| Ratio | Preferred size | Typical use |
| --- | --- | --- |
| 1:1 | 1024 × 1024 | Square concept or social post |
| 4:5 | 1080 × 1350 | Portrait presentation or social post |
| 3:2 | 1800 × 1200 | Landscape image |
| 16:9 | 1920 × 1080 | Wide room view or presentation slide |
| 9:16 | 1080 × 1920 | Vertical story or mobile layout |

Custom dimensions are accepted when the pixel dimensions match the entered aspect ratio. The image generator may use the ratio while returning a different exact pixel size.

## 6. Generate the final prompt

Select **Generate Final Prompt**. Review the validation status, then use **Copy Prompt** or **Download .txt**.

![Final prompt generation](../image/14.png)

![Validated final prompt](../image/15.png)

Do not rewrite the generated prompt unless a detail is genuinely wrong. Return to the relevant object field or diagram when the scene itself needs correction.

## 7. Generate the scene in ChatGPT

Open ChatGPT Images and attach:

1. The copied prompt or downloaded prompt file.
2. The same reference images in the same order used by the tool.

Use a capable image-generation model and set the reasoning effort to **High** when that option is available. Confirm the requested aspect ratio before sending.

![Prompt and references attached in ChatGPT](../image/17.png)

Compare the result against the scene summary. Check the large structural decisions first: wall assignment, central object, foreground placement, and camera direction. Then check materials and decorative details.

## 8. Create isolated object assets when needed

The application includes an **Object Output** section. Build the scene first, open Object Output, select the required objects, choose the size, and generate the transparent-background prompt.

For a quick ChatGPT follow-up, use:

> Give me each main object from this interior separately as a transparent PNG, one object per file.

This step is optional. Use it only when the objects are needed for a presentation board, catalog, or further compositing.

## 9. Refine the final visual in mnml.ai

Open [mnml.ai Studio](https://mnml.ai/) and upload the generated room image. Choose an Interior workflow and use a high form-control value when the composition must remain close to the source.

Use this prompt:

> Refine this interior into a presentation-ready visual. Preserve the room layout, furniture placement, wall features, materials, colors, and lighting. Improve realism, texture detail, and overall image clarity.

Review the output for layout drift before downloading. The refined image should improve finish and clarity without changing the design decisions already approved in the scene diagram.

## Final review

Before sharing the concept, compare the output with the original references and confirm:

- every required object is present once unless another count was requested;
- each wall treatment is on the correct wall;
- the main furniture follows the selected layout;
- no source background or unwanted prop has been carried into the scene;
- the aspect ratio is correct for the intended presentation.
