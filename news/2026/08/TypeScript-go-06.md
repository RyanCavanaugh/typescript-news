# Report for 2026-08-06 (Thursday, August 6th, 2026)

9 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @MulverineX asked for ideas about the issue in Bun in [microsoft/TypeScript-go#4567](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-5211055508)
    * @johnnyreilly asked whether the custom transformers functionality would cover what transformers did in the TS API in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5213869402)
    * @nikeedw provided a minimal repro and proposed fix in #4842 in [microsoft/TypeScript-go#4748](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5209111655)
    * @nikeedw stated they will not sign the CLA in [microsoft/TypeScript-go#4842](https://github.com/microsoft/TypeScript-go/pull/4842#issuecomment-5215747276)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5170503808) **Princesseuh** apologized for the late answer and explained how multiple TS/JS script blocks in an Astro file share scope or isolate modules and compile to a single default export
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5170697901) **NullVoxPopuli** explained Ember component format in glimmer-ts preserving block scope semantics and provided code examples
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5193510895) **andrewbranch** asked for confirmation about the need for multiple virtual backing files due to global script scope across multiple HTML-like files
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5211151982) **andrewbranch** noted that the latest commit of #4712 now supports mapping a single non-TS file into multiple distinct files

### [Issue microsoft/TypeScript-go#4567](https://github.com/microsoft/TypeScript-go/issues/4567) (Closed)

**\`tsc\` incorrectly points to v6 rather than v7**

*The npm alias setup for TypeScript 6 and 7 side-by-side assigns the tsc binary to version 6 instead of 7.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4927717897) **RyanCavanaugh** suggested adding nmHoistingLimits: dependencies to .yarnrc.yml as a workaround
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-4928028399) **AndrewMax** provided a minimal reproducible example repository, noted a workaround and its drawback, and referenced a related issue
 * (1 month ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-5211055508) **MulverineX** said "I'm having this issue in Bun, any ideas? @RyanCavanaugh "
 * [later](https://github.com/microsoft/TypeScript-go/issues/4567#issuecomment-5219261783) **RyanCavanaugh** said "@MulverineX you'll have to talk to bun, we do not control how package managers lay out their bin refs"

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Support external content mappers in tsconfig to transform and map unsupported file types into valid TypeScript*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5175223764) **jasonlyu123** described issues with completion position mapping and span mapping constraints in Svelte transformations and asked for feedback on treating completion positions as range ends and on overlapping segment rules
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5180574756) **andrewbranch** acknowledged the same mapping issue, noted a stashed fix, thanked for the example, asked if spans should be broken into tokens or kept contiguous, and recommended using minimal spans
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5185808920) **andrewbranch** updated the PR description, replaced SpanMapPurpose with per-LSP-feature bit flags, and added two ways to inject extra configuration options into content mappers
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5211145449) **andrewbranch** said "Another significant change: a content mapper may now emit additional supplemental files as part of any Transform response. PR description updated again."
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5213869402) **johnnyreilly** asked whether the custom transformers functionality would cover what transformers did in the TS API
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5218558612) **andrewbranch** said "No, but custom transformers are still planned, mentioned in #4830. I’ll add ts-loader to the list of projects that needs it!"

### [Issue microsoft/TypeScript-go#4748](https://github.com/microsoft/TypeScript-go/issues/4748) (Open, `Needs More Info`)

**Panic: nil pointer in NodeList\.HasTrailingComma during incremental rebuild \(build\-mode declaration printer\) — 7\.0\.2 and current nightly**

*A nil pointer dereference in NodeList.HasTrailingComma triggers a panic during incremental build-mode declaration printing in TypeScript.*

 * (1 week ago) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5121048546) **RyanCavanaugh** requested repro steps and suggested bisecting to an anonymized code subset
 * [today](https://github.com/microsoft/TypeScript-go/issues/4748#issuecomment-5209111655) **nikeedw** described root cause with a two-file minimal repro, proposed a fix in PR #4842, and requested maintainers’ judgment

### [PR microsoft/TypeScript-go#4835](https://github.com/microsoft/TypeScript-go/pull/4835) (Closed, **RyanCavanaugh**, **Copilot**)

**Preserve TS2307 in concurrent mode for import/export declarations inside non\-scope blocks**

*Restore module-resolution diagnostics TS2307 for import/export declarations in non-scope blocks under concurrent mode without altering TS1233 placement errors.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4835#issuecomment-5208150075) **RyanCavanaugh** said "Zero files changed?"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4839](https://github.com/microsoft/TypeScript-go/pull/4839) (Open)

**fix\(63726\): fix declaration emit for multiline jsdoc literal types**

*Ensure TypeScript declaration files accurately emit multiline JSDoc literal types.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#4840](https://github.com/microsoft/TypeScript-go/pull/4840) (Open)

**WIP**

*A work-in-progress placeholder issue created without any accompanying details.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#4841](https://github.com/microsoft/TypeScript-go/pull/4841) (Open, **weswigham**)

**Fix false\-positive TS2354 for native private class field access with importHelpers at dated targets**

*With importHelpers enabled and a dated ECMAScript target, the Go port of TypeScript wrongly reports TS2354 on native private class field access.*

 * created by **astegmaier**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4841#issuecomment-5209140467) **astegmaier** noted that the PR contained the discussed bug fix and disclosed that the reproduction was hand-crafted while the PR itself was agent-generated

### [PR microsoft/TypeScript-go#4842](https://github.com/microsoft/TypeScript-go/pull/4842) (Closed)

**Fix crash when a call signature's type parameter cannot be reused**

*Call signature type parameter reuse failure currently produces nil AST nodes unchecked, causing a printer crash.*

 * created by **nikeedw**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4842#issuecomment-5215747276) **nikeedw** thanked CI for green results, declined to sign the CLA, suggested treating the PR as a proposal rather than merging, and noted the change may only address a symptom

### [PR microsoft/TypeScript-go#4843](https://github.com/microsoft/TypeScript-go/pull/4843) (Open)

**Add environment variable for single\-threaded mode**

*Add support for TS_SINGLE_THREADED environment variable to enable single-threaded compilation in normal and build modes.*

 * created by **maschwenk**

