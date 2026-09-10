# Technical Overview

Visual Prompt Generator uses a six-step web interface backed by a structured scene model. The public repository contains the workflow documentation and examples. Application source remains in a separate private repository.

## Application structure

| Layer | Responsibility |
| --- | --- |
| Next.js frontend | Reference upload, object intake, scene review, diagram selection, output settings, and prompt display |
| FastAPI backend | Project state, image checks, scene construction, diagram generation, prompt assembly, and validation |
| Gemini integration | Reference interpretation and scene planning |
| Deterministic validation | Reference integrity, required fields, diagram structure, object coverage, and final-prompt completeness |
| JSON project storage | Project records, uploads, and generated prompt files |

## Scene data

Each scene stores:

- references with a stable ID and upload order;
- objects with extraction scope, count, position, orientation, and relationships;
- environment, camera, and lighting context when supplied;
- available diagrams and the selected diagram;
- aspect ratio, preferred resolution, rendering style, background mode, and output format.

This structure keeps layout decisions separate from visual styling. The final prompt is built only after a diagram and output format have been selected.

## Validation sequence

1. Uploaded bytes are decoded and checked against the supported image formats.
2. Reference IDs and upload positions are checked for uniqueness.
3. Every object is checked against an existing reference.
4. Counts, extraction scope, surface assignment, and orientation are validated.
5. Diagram options are checked for required sections and object coverage.
6. The final prompt is checked for missing objects, reference assignments, and unresolved template fields.

If generated diagram text fails its checks, the application returns deterministic diagrams built from the same locked scene data.

## Output modes

`SCENE_COMPOSITION` creates a full-scene prompt. `SCENE_EDIT` applies a layout correction and invalidates the previous diagram selection. `OBJECT_OUTPUT` creates a prompt for selected objects on a transparent PNG background.

## Deployment model

The frontend is deployed on Vercel and communicates with a FastAPI service. The backend requires persistent storage for uploaded references and project records. Credentials and private source files are not included in this documentation repository.

## Scope

The tool prepares a controlled prompt and verifies its structure. The image generator remains responsible for the final pixels, so output review is part of the workflow.
