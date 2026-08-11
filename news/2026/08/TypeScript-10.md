# Report for 2026-08-10 (Monday, August 10th, 2026)

9 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @KumJungMin offered to work on the issue in [microsoft/TypeScript#63712](https://github.com/microsoft/TypeScript/issues/63712#issuecomment-5248209956)
    * @DannKenn provided repro steps as requested in [microsoft/TypeScript#63743](https://github.com/microsoft/TypeScript/issues/63743#issuecomment-5246701457)
    * @SnowingFox provided repro steps and root cause analysis in [microsoft/TypeScript#63746](https://github.com/microsoft/TypeScript/issues/63746#issuecomment-5248716689)

## Activity Summary

### [PR microsoft/TypeScript#63248](https://github.com/microsoft/TypeScript/pull/63248) (Open, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Add lib types for JSON\.rawJSON, JSON\.isRawJSON, and reviver context**

*Add TypeScript declarations for ES2025’s JSON.rawJSON, JSON.isRawJSON, and JSON.parse reviver context*

 * **typescript-bot** added label `For Backlog Bug`
 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4270116628) **RyanCavanaugh** said "@afurm future automated comments will result in a block; any automated activity we want to occur in this repo we will set up ourselves or already have"
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/63248#issuecomment-4346296546) **MulverineX** said "@RyanCavanaugh the commandLineParser.ts has since been removed, is there a reason this PR is not proceeding?"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [Issue microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646) (Closed, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch does not work in docker**

*tsc --watch fails to detect file changes in Docker bind-mounted workspaces on macOS after upgrading to version 7.0.2.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4999890598) **jakebailey** advised the user to file a separate issue for the MacOS problem and clarified that TS7 has no toggle to revert to NodeJS behavior
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5137934722) **danyreyna** reported a similar issue when building with Docker using node:22.22.3-slim, where subsequent tsc --watch builds stalled due to a fanotify_mark operation not supported error
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5145530428) **johnfav03** thanked maintainers and explained that Docker's filesystem returns EOPNOTSUPP and that the watch will fall back from fanotify to inotify once the PR is merged
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript#63678](https://github.com/microsoft/TypeScript/issues/63678) (Closed, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch doesn't work on NTFS partitions on Linux**

*After upgrading to TypeScript 7, tsc --watch fails on Linux NTFS partitions due to fanotify_mark no such device errors.*

 * created by **bt7s7k7**
 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**
 * (today) **johnfav03** closed the issue

### [Issue microsoft/TypeScript#63712](https://github.com/microsoft/TypeScript/issues/63712) (Open, `Bug`)

**Exported namespace class suppresses TS1308 for await in computed member names**

*Exporting a namespace class incorrectly disables the TS1308 error for await in computed member names.*

 * created by **mohsen1**
 * (1 week ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63712#issuecomment-5248209956) **KumJungMin** said "Hi! I'd be interested in working on this issue if no one is already working on it :)"

### [Issue microsoft/TypeScript#63731](https://github.com/microsoft/TypeScript/issues/63731) (Open, `Needs Investigation`, `Fix Available`, **johnfav03**)

**\-\-incremental: after a pnpm dependency version change, the cached run is slower than a cold run and most of the time is unattributed**

*pnpm's versioned module paths on dependency updates invalidate TypeScript incremental cache, causing cached builds to be slower with unaccounted time.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63731#issuecomment-5219905839) **RyanCavanaugh** said "What's the behavior in TypeScript 7.0?"
 * [today](https://github.com/microsoft/TypeScript/issues/63731#issuecomment-5243251674) **johnfav03** reported that TypeScript 7.0 exhibited the same regression and submitted a PR to fix it

### [Issue microsoft/TypeScript#63735](https://github.com/microsoft/TypeScript/issues/63735) (Closed, `Working as Intended`)

**Syntax error in an importing root file suppresses diagnostics in unrelated root files**

*A syntax error in an importing root file suppresses semantic error diagnostics in unrelated files.*

 * created by **mohsen1**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63735#issuecomment-5231137711) **Mahnoor-Zaffar** suggested investigating TypeScript compiler error handling, asked about specific compilation configurations, and offered to work on a fix
 * [today](https://github.com/microsoft/TypeScript/issues/63735#issuecomment-5245729108) **RyanCavanaugh** clarified that the behavior was intentional to avoid overwhelming users with type errors caused by a syntax error
 * **RyanCavanaugh** added label `Working as Intended`
 * (later) **mohsen1** closed the issue

### [Issue microsoft/TypeScript#63743](https://github.com/microsoft/TypeScript/issues/63743) (Open, `Needs More Info`)

**Project references resolve a symlinked sibling's raw source instead of its own composite output, using the wrong project's compilerOptions**

*TypeScript project references incorrectly resolve symlinked sibling packages’ source files using the wrong compilerOptions instead of their composite outputs.*

 * created by **DannKenn**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63743#issuecomment-5246501547) **RyanCavanaugh** requested full package.jsons and tsconfig.jsons and a cloneable repo to diagnose the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63743#issuecomment-5246701457) **DannKenn** provided a minimal cloneable reproduction and flagged a regression in TypeScript 6.0.3 causing build failures with symlinked npm workspaces in a diamond-shaped reference graph; confirmed the issue is not specific to Bun

### [Issue microsoft/TypeScript#63744](https://github.com/microsoft/TypeScript/issues/63744) (Closed)

**I acknowledge that issues using this template may be closed without further explanation at the maintainer's discretion\.**

*Acknowledgement that issues using this template can be closed at the maintainer’s discretion without explanation.*

 * created by **DannKenn**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63745](https://github.com/microsoft/TypeScript/pull/63745) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump js\-yaml from 4\.1\.1 to 4\.3\.1**

*Bump js-yaml to 4.3.1 for security fix removing quadratic complexity in omap duplicate detection*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63746](https://github.com/microsoft/TypeScript/issues/63746) (Open)

**\[7\.0\] Downlevel emit places a comment after a synthesized return, causing arrow functions to return undefined**

*TypeScript 7.0's downlevel emit places comments after synthesized returns in arrow functions with optional chaining, causing ASI to return undefined.*

 * created by **diego9497**
 * [today](https://github.com/microsoft/TypeScript/issues/63746#issuecomment-5248716689) **SnowingFox** reproduced the issue on the TS 7.0 native compiler and confirmed it as a native-port regression, provided reproduction steps, compared native and JS emitter outputs, and identified the root cause in typescript-go
 * [today](https://github.com/microsoft/TypeScript/issues/63746#issuecomment-5249376232) **MartinJohns** said "Duplicate of https://github.com/Microsoft/typescript-go/issues/4722."

### [Issue microsoft/TypeScript#63747](https://github.com/microsoft/TypeScript/issues/63747) (Open, `Docs`, `Fix Available`)

**Update wiki "Using the Compiler API" for TypeScript v7**

*Update the Using the Compiler API wiki documentation to cover new types and patterns in TypeScript v7.*

 * created by **peterpeterparker**
 * (later) **RyanCavanaugh** added label `Docs`, and set milestone to `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`

