# Report for 2026-07-12 (Sunday, July 12th, 2026)

11 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @dannycreations asked about Android platform support for Termux in [microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4954972211)
    * @Skykill provided repro steps and analysis in issue #4612 and suggested cross-linking for triage in [microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4952534039)

## Activity Summary

### [Issue microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424) (Closed, `possible improvement`)

**Request for support for additional architectures**

*Support and a roadmap are requested for riscv64, ppc64le, and loong64 architectures in typescript-go.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4746763098) **jakebailey** noted that the RC supports a full set of platform-specific optionalDependencies for tagged releases and that nightly releases will remain limited to arm64 and amd64 on darwin, linux, and windows
 * (3 weeks ago) **jakebailey** closed the issue
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4748935526) **darkyzhou** said "Thanks!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4954972211) **dannycreations** asked about Android platform support for Termux after encountering a TypeScript resolution error

### [Issue microsoft/TypeScript-go#4503](https://github.com/microsoft/TypeScript-go/issues/4503) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Add APIs that set the compiler options programatically**

*Provide an API to programmatically set or update compiler options for inferred and configured projects.*

 * (6 days ago) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4503#issuecomment-4956401973) **mrazauskas** described using vfs, a virtual tsconfig file, and openProjects to meet their project needs and closed the issue
 * (later) **mrazauskas** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/4503#issuecomment-4959823560) **andrewbranch** said "FYI, I think I'll also eventually add a top-level createProgram(rootFiles, compilerOptions) API, separate from the snapshot system but with no ability to incrementally update that program."

### [Issue microsoft/TypeScript-go#4519](https://github.com/microsoft/TypeScript-go/issues/4519) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Consider exporting the \`inferredProjectName\` constant from the API**

*Propose exporting the inferredProjectName constant from the API to prevent breaking changes and facilitate reliable detection of inferred projects.*

 * (6 days ago) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4519#issuecomment-4956405233) **mrazauskas** said "See https://github.com/microsoft/typescript-go/issues/4503#issuecomment-4956401973"
 * (later) **mrazauskas** closed the issue

### [Issue microsoft/TypeScript-go#4520](https://github.com/microsoft/TypeScript-go/issues/4520) (Open, `Domain: Editor`)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*Enabling the TypeScript Native Preview extension in an empty folder without package.json causes a persistent memory leak until VS Code is closed.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4868442056) **KostyaTretyak** said "Google Gemini =)"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869357111) **KostyaTretyak** clarified that adding a default package.json with npm init -y prevented the memory leak and suggested a nearby service might be scanning git repositories
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4869534469) **KostyaTretyak** confirmed no memory leak when moving folder to a directory without other git repositories and suggested a service might misdetect neighboring repositories as part of the monorepo
 * [today](https://github.com/microsoft/TypeScript-go/issues/4520#issuecomment-4952534039) **Skykill** reported that their three.js case reproduced with a minimal CLI setup, filed issue #4612 with repro steps and analysis, and suggested cross-linking due to a potential common underlying cause

### [PR microsoft/TypeScript-go#4611](https://github.com/microsoft/TypeScript-go/pull/4611) (Open)

**Update \_scripts tooling deps and lockfiles**

*Update _scripts tooling dependencies, regenerate lockfiles, and add devcontainer lockfile for merging into main.*

 * created by **MasterTLF**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-4951714474) **MasterTLF** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4611#issuecomment-4951931688) **MasterTLF** said "fix without second review and approval"

### [Issue microsoft/TypeScript-go#4612](https://github.com/microsoft/TypeScript-go/issues/4612) (Open, `duplicate`)

**Checker memory explosion from repeated cross\-product distribution \(repro: @types/three TSL\)**

*Repeated cross-product distribution in @types/three TSL types causes the TypeScript Go checker to consume excessive memory.*

 * created by **Skykill**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4612#issuecomment-4959089348) **ahejlsberg** said "This appears to be a duplicate of #4528. The fix I suggest there also fixes this issue."
 * **ahejlsberg** added label `duplicate`

### [Issue microsoft/TypeScript-go#4613](https://github.com/microsoft/TypeScript-go/issues/4613) (Open)

**Exhaustive switch on co\-narrowed tuple's \`\.length\` does not terminate fallthrough control flow \(works in TS 6\.0\)**

*TypeScript 7.0 misidentifies an exhaustive inner switch on a co-narrowed tuple’s length as non-terminating, leading to incorrect type inference.*

 * created by **sergey-shandar**

### [Issue microsoft/TypeScript-go#4614](https://github.com/microsoft/TypeScript-go/issues/4614) (Open)

**\`tsc \-b \-\-watch\` takes tens of seconds to start watching on a large project\-references solution \(\`computeDesiredWatches\` is O\(files × dirs\)\)**

*tsc -b --watch stalls for tens of seconds on large project-reference solutions because computeDesiredWatches’s O(files×dirs) logic delays filesystem watch registration*

 * created by **dyantako**

### [PR microsoft/TypeScript-go#4615](https://github.com/microsoft/TypeScript-go/pull/4615) (Open, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Upgrade the root GitHub CodeQL Actions by bumping init to v4.37.0 and updating autobuild and analyze.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#4616](https://github.com/microsoft/TypeScript-go/issues/4616) (Open)

**Behavior difference: declaration emit synthesizes extensionless \`import\(\)\` specifier under \`allowImportingTsExtensions\`, invalid in nodenext**

*Using allowImportingTsExtensions with module nodenext, tsgo's declaration emit drops file extensions, producing invalid import() specifiers.*

 * created by **dario-causaly**

### [Issue microsoft/TypeScript-go#4617](https://github.com/microsoft/TypeScript-go/issues/4617) (Open)

**Behavior difference: TS4023 on declaration emit when a spread of a symbol\-branded object is unioned with the original \(pattern used by zod \`\.brand\(\)\`\)**

*Unioning a symbol-branded object with its spread causes tsgo to inline the brand symbol and error TS4023, unlike tsc.*

 * created by **dario-causaly**

### [Issue microsoft/TypeScript-go#4618](https://github.com/microsoft/TypeScript-go/issues/4618) (Open, `Domain: Editor`)

**Some imports are not updated after a file rename, in composite projects**

*TypeScript 7 composite projects do not update imports in unloaded subprojects when renaming files, unlike TypeScript 6.*

 * created by **pascalspadone**
 * **pascalspadone** added label `Domain: Editor`

