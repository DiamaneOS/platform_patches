# DiamaneOS patches

Fixes and library updates that DiamaneOS applies on top of its sources before a build, until upstream
carries them.

- `series.json` lists the patches in order: the project each one changes, the patch file with its
  SHA-256 and, for every file it touches, the file's mode and blob before and after.
- `patches/<project path>/` holds the patch files.
- The build tools apply the series, see
  [the patch series](https://github.com/DiamaneOS/diamaneos-tools/blob/main/docs/BUILD.md#the-patch-series)
  in the build reference.
- A patch is applied only to the exact file contents it is pinned to. When upstream changes such a
  file, the build stops, and the patch is refreshed or dropped.
- Each patch is under the licence of the files it changes.
