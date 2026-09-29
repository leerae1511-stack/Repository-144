# Tool Pocket Generator V144 — Release Notes

## Provenance
V144 is built directly from `Tool_Pocket_Generator_V143_FINAL.zip`. V143 is the sole source build; its four-file archive is the starting point.

## Problem addressed
Add point projected onto a 48-step approximation of curved edges, while the displayed profile is rendered using the generator's 12-step sampled curve. These can differ, so a new point was not guaranteed to lie on the visible line.

## Exact changes
- Changed only `nearestProfileInsertion()` geometry in `index.html`: it now uses 12 intervals for curved edges and 1 for straight edges, matching the visible profile's sampling.
- Updated embedded version identifiers from V143 to V144 (page title, heading, app metadata, saved-tool key/version and STL label) so the delivered generator identifies as V144.

## What was not changed
No changes to curve interpolation, existing point coordinates, point numbering logic, Straight/Curve settings, dimensions, photo/grid workflow, finger reliefs, geometry check, JSON import/export logic, STL geometry logic, layout, manifest, or service worker.

## Verification
- Source archive: V143 ZIP only; all four archive paths preserved.
- Confirmed V144 identifiers are present and V143 identifiers are absent in `index.html`.
- JavaScript syntax check and ZIP integrity check completed.
- iPad/Safari touch behaviour has NOT been tested; this build needs your retest.

## Retest
1. Open `index.html` from this V144 ZIP and confirm the heading says V144.
2. Load the same profile used for the earlier Add point test.
3. Use Add point on a straight section and check the new dot lies on the black profile line.
4. Use Add point on a curved section and check the new dot lies on the black profile line.
5. Confirm existing points, numbering, Straight/Curve settings, and the remaining workflow are unchanged.

Single-purpose Add point placement correction. No other fixes included.
