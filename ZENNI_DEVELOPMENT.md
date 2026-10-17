# Zenni & The Hollow Star — Development Instructions

This contribution is **based on the CoCX 0.9a.995 game source** (the `CoCX_0.9a.995` snapshot). The GitHub contribution branch starts from upstream `master-wip`; verify that upstream's current revision matches the target source before applying or merging the content files.

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
2. Develop content in focused commits on `feature/zenni-hollow-star`, not on `master-wip`.
3. Check that all references, imports, registration paths, flags, and event triggers are wired correctly.
4. Test new content and regressions, including save/load and game startup, whenever a working build environment is available.
5. Keep any Android-specific packaging changes in a different branch/workstream.

## Version provenance and SWF artifact
- **Source base:** `CoCX_0.9a.995` / `v0.9a.995`, as supplied for this expansion. This is a source-version claim, not a claim that current upstream `master-wip` is unchanged.
- **Compiled review artifact:** `CoCX_Zenni_HollowStar_ScorpionTail_Cleanup_Test_Build.swf`. It was compiled from the cleaned content source, preserving the upstream in-game version string. Structural SWF checks and static regression checks were completed; interactive gameplay testing remains outstanding.
- **SWF repository status:** Not uploaded as a binary artifact yet. Add the actual compiled file to a draft GitHub Release or other binary-hosting location once the bytes are transferred.
- Once published, record the source commit, target upstream source revision, SWF SHA-256, build command, and any difference between the GitHub branch baseline and the CoCX 0.9a.995 source snapshot.
