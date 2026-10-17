# Zenni & The Hollow Star — Development Instructions

This branch is dedicated to game-content development for CoCX, based on `master-wip`.

## Boundaries
- Keep Zenni/Hollow Star content development separate from the Android wrapper, APK packaging, fullscreen and performance work.
- Preserve existing saves: no changes to save paths, format, slots, or identifiers without explicit approval.
- Do not modify touchscreen controls.
- Preserve complete required game-system and content initialization before gameplay or save loading is enabled. Do not introduce lazy initialization of essential systems.
- Make focused, reviewable ActionScript changes. Follow `CODING.md` and `CONTRIBUTING.md`; avoid unrelated reformatting.
- Preserve upstream game behavior unless a content change specifically requires it.
- Do not assume a compiled SWF is source-equivalent; validate content against this branch's source and the intended game version.
- Do not claim a successful build without actually compiling and testing it.

## Workflow
1. Read `BUILDING.md`, `CODING.md`, and relevant source before changing anything.
2. Develop content in focused commits on this branch, not on `master-wip`.
3. Check that all references, imports, registration paths, flags, and event triggers are wired correctly.
4. Test new content and regressions, including save/load and game startup, whenever a working build environment is available.
5. Keep any Android-specific packaging changes in a different branch/workstream.

## Version provenance and SWF artifact
- **Intended base game:** CoCX **0.9a.995-mod** for Zenni & The Hollow Star. This fork currently starts from upstream `master-wip`; **the exact upstream source version has not yet been independently verified** against 0.9a.995-mod.
- **Existing compiled mod artifact:** `CoCX_0.9a.995mod_Zenni_HollowStar.swf` (filename supplied in the earlier project). Its filename indicates **0.9a.995mod**, but that does not establish the source revision from which it was compiled. Do not claim the current source reproduces it without a source/version comparison.
- **SWF repository status:** Not uploaded yet. Add the original SWF as a binary artifact once the file bytes are available; do not substitute a placeholder or rename another build.
- Once verified, record the source commit, upstream tag/version, SWF SHA-256, build command, and any differences between the verified source baseline and the 0.9a.995mod artifact.
