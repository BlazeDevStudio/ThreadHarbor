# ThreadHarbor migration manifest

**State:** SOURCE_STAGED; NOT VERIFIED or released.  
**Destination:** `BlazingSystems/ThreadHarbor`, branch `migration/threadharbor-v010-source-20261028`.  
**Original source:** `BlazingSystems/BlazingSystems-Experiments/expiremental/Blaze-ThreadHarbor-Utility/`.  
**Source exact commit:** `a5ef1e1c959da06674540ffcd88c89fe01ee4261`.  
**Preserved source PR:** [Experiments #209](https://github.com/BlazingSystems/BlazingSystems-Experiments/pull/209) (draft, not closed or merged by migration).  
**Source PR base:** `main@9596fc6a9f8a6a42bc252019c24ca1f38d96dd7a`.  
**First complete source-staging commit:** `379d1905c6d8137e26797d6aa77a3bc42f72236e`.

## Verification

The complete source subtree of 27 tracked text files was copied without changing contents or mode. Cross-repository recursive tree comparison on 2026-10-28 verified **27/27 exact Git blob SHA and mode matches; zero missing, extra or different source files** at the source-staging commit. The original commit graph cannot be transferred by this content-only migration; original commit/PR history remains linked here for permanent attribution.

## CI provenance

Original source workflow: `BlazingSystems-Experiments/.github/workflows/threadharbor-android-preview.yml` on the exact head above. Its source-relative paths must not be reused unchanged in the dedicated repository. New destination `.github/workflows/threadharbor-ci.yml` is root-scoped and runs fixture protocol tests plus Gradle Android unit tests/build, without publishing releases. Its actual execution must be checked separately. The original emulator acceptance workflow remains in the source repository pending a verified destination replacement; absence of an emulator run is a blocker to VERIFIED status.

## Product limitations

Only the owned WebView fixture's semantic messages are supported; no live Facebook inbox/message integration, remote delivery guarantee, or general third-party site bridge is claimed. See source `README.md` and `docs/REAL_PRODUCT_GAP_AUDIT_20261026.md`.

## Before final cutover

- Require a successful exact-head destination CI run, including Android unit tests and debug APK checksum.
- Adapt and execute emulator device-flow acceptance against the same destination artifact before declaring VERIFIED.
- Confirm source PR #209's active head and discuss later changes before treating the copy as up to date.
- Keep original source and PR open until independent validation and explicit cutover authorization.
