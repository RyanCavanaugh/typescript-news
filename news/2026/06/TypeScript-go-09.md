# Report for 2026-06-09 (Tuesday, June 9th, 2026)

11 different users commented on 33 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#3102](https://github.com/microsoft/TypeScript-go/pull/3102) (Open, **DanielRosenwasser**)

**Fix a formatting crash caused by template literal in parser\-recovered property signature**

*Process grammar error nodes to correctly handle template literals in recovered property signatures and prevent formatting crashes.*

 * created by **Andarist**
 * (7 weeks ago) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3102#issuecomment-4665116908) **DanielRosenwasser** said "Unfortunately we've got merge conflicts. 🙁"

### [PR microsoft/TypeScript-go#3391](https://github.com/microsoft/TypeScript-go/pull/3391) (Open, **ahejlsberg**)

**Fix inference from unions of arrays with different nesting depths**

*Add a matching pass to infer equally nested arrays first, correcting generic type inference for unions like T[] | T[][]*

 * created by **Yiin**
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3391#issuecomment-4231802984) **Yiin** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#3753](https://github.com/microsoft/TypeScript-go/issues/3753) (Closed, `bug`, **iisaduan**)

**Missing error for non\-existent root files**

*tsgo silently ignores missing root files specified in tsconfig.json instead of reporting an error.*

 * (1 month ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#3832](https://github.com/microsoft/TypeScript-go/pull/3832) (Closed)

**Add recursion limiter for \`TypeToString\`**

*Limit TypeToString recursion to two levels by returning "?" and discarding diagnostics to prevent infinite recursion and stack overflows.*

 * (3 weeks ago) **ahejlsberg** closed the issue
 * (yesterday) **ahejlsberg** reopened the issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4653778017) **ahejlsberg** said "This also fixes https://github.com/microsoft/TypeScript/issues/63273, so I'm reopening. I think we should merge this as it is a general solution to an unknown number of latent circularities."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3846](https://github.com/microsoft/TypeScript-go/pull/3846) (Closed, `No linked issue`)

**Find all references API endpoints**

*Request to implement API endpoints that return all references for specified code symbols.*

 * created by **navya9singh**
 * (yesterday) **RyanCavanaugh** added label `No linked issue`, and set milestone to `Possible Improvement`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3854](https://github.com/microsoft/TypeScript-go/pull/3854) (Closed)

**check that all files in \`"files"\` in tsconfig exist**

*Implement a check during tsconfig root file loading to confirm that all "files" entries exist.*

 * created by **iisaduan**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3854#issuecomment-4654368434) **iisaduan** implemented a new fix based on andrewbranch’s comments and requested a review, explaining the tsconfig-based file resolution with a cwd fallback
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#3949](https://github.com/microsoft/TypeScript-go/pull/3949) (Open)

**feat: completion snippets**

*Add completion snippets functionality to enable snippet-based code suggestions during development.*

 * created by **a-tarasyuk**
 * (2 weeks ago) **a-tarasyuk** closed the issue
 * (today) **a-tarasyuk** reopened the issue
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4019](https://github.com/microsoft/TypeScript-go/issues/4019) (Closed, `Crash`, **weswigham**)

**Crash on file rename \+ \`workspace/didChangeWatchedFiles\`, \\w \`composite\` option enabled**

*The TypeScript language server crashes with a nil pointer panic when processing a file rename alongside workspace/didChangeWatchedFiles in composite-enabled projects.*

 * **mpal9000** added label `Crash`
 * (4 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4019#issuecomment-4663782366) **weswigham** said "Fixed in https://github.com/microsoft/typescript-go/commit/69b0d53976ef291fa0bb2b636ec1b557a015f6b3 (presumably - it no longer repros at main)"
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4028](https://github.com/microsoft/TypeScript-go/pull/4028) (Closed)

**fix\(4019\): skip unloaded projects during file rename**

*Skip projects without loaded programs during file rename handling to prevent nil pointer panics*

 * created by **dcsid**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4028#issuecomment-4522106807) **dcsid** said "@microsoft-github-policy-service agree"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4028#issuecomment-4523304765) **DanielRosenwasser** said "Are we going to miss rename locations in any unloaded programs? In other words, should we be loading the programs on the fly? If not, whose responsibility is it to do that?"
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4172](https://github.com/microsoft/TypeScript-go/pull/4172) (Open, `Voight-Kampff Anomaly`, **ahejlsberg**)

**Fix redundant undefined wrapping in optional parameter declaration emit**

*Update declaration emission for optional parameters to avoid redundant '| undefined' wrapping when types already include undefined*

 * created by **danyalahmed1995**
 * (6 days ago) **RyanCavanaugh** added label `Voight-Kampff Anomaly`, and set milestone to `TypeScript 7.0 RC`
 * **RyanCavanaugh** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4235](https://github.com/microsoft/TypeScript-go/issues/4235) (Closed, `bug`)

**Behavior difference: tsgo no longer emits comment on \`@typedef\` style object attributes**

*tsgo no longer preserves JSDoc comments on object properties defined via @typedef, causing missing documentation in emitted types.*

 * created by **hkleungai**
 * (yesterday) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4244](https://github.com/microsoft/TypeScript-go/issues/4244) (Open, `Crash`, `Needs More Info`)

**Fatal server error: nil Session from \`flushChangesLocked\(\)\`**

*Server crashes with a fatal nil pointer dereference in Session.flushChangesLocked caused by an unexpected nil session.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **RyanCavanaugh** added label `Needs More Info`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4247](https://github.com/microsoft/TypeScript-go/issues/4247) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal error during resolution through \`RootLength\`**

*A non-absolute path passed to vfs/internal.RootLength triggers a panic and aborts module resolution.*

 * (yesterday) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4247#issuecomment-4663523545) **RyanCavanaugh** said "Moving to post-7.0 until we get a userland repro"

### [PR microsoft/TypeScript-go#4248](https://github.com/microsoft/TypeScript-go/pull/4248) (Open, **DanielRosenwasser**, **Copilot**)

**Fix fatal panic on non\-absolute path in VFS**

*Update VFS RootLength, SplitPath, and RootAndPath to return defaults for non-absolute paths instead of panicking.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4661380146) **DanielRosenwasser** said "@copilot+gpt-5.5 you did not add a test"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4661516807) **Copilot** added a focused regression test covering ResolveModuleName('./foo', '', ...) to exercise the non-absolute VFS lookup path that previously panicked; noted in commit f7f88aae
 * [today](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4662353054) **DanielRosenwasser** said "@copilot can you investigate adding a real world example as a compiler or fourslash test that fails without any fix?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4248#issuecomment-4662531216) **Copilot** investigated compiler and fourslash test normalization and determined that no real-world test could reproduce the panic without giving false confidence

### [Issue microsoft/TypeScript-go#4249](https://github.com/microsoft/TypeScript-go/issues/4249) (Open, `Domain: API and Extensibility`)

**\`\.getProgramDiagnostics\(\)\` is missing in the API**

*Add an API method like program.getProgramDiagnostics or project.getProjectDiagnostics to retrieve missing compiler options diagnostics.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Domain: API and Extensibility`, and set milestone to `Post-7.0`

### [PR microsoft/TypeScript-go#4250](https://github.com/microsoft/TypeScript-go/pull/4250) (Closed, **weswigham**)

**preserve jsdoc prop descriptions in declaration emit**

*Retain JSDoc property descriptions when emitting TypeScript declaration files.*

 * created by **a-tarasyuk**
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **weswigham**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4251](https://github.com/microsoft/TypeScript-go/issues/4251) (Closed, `bug`, **jakebailey**, **Copilot**)

**Triple slash reference does not emit files from referenced ts projects**

*tsgo omits triple slash reference paths in generated declaration files for referenced TypeScript projects, unlike tsc.*

 * created by **HolgerJeromin**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `bug`, set milestones to `Post-7.0`, `TypeScript 7.0 RC`, and removed from milestone `Post-7.0`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4252](https://github.com/microsoft/TypeScript-go/issues/4252) (Closed, `bug`, **ahejlsberg**)

**JSDoc \`@typedef\` silently dropped when preceded by a multi\-line \`@property\` function type and an interface\-returning call**

*tsgo silently drops a JSDoc typedef when preceded by a multiline function-type property and a generic interface call*

 * created by **turadg**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **sandersn**
 * (today) **ahejlsberg** assigned to **ahejlsberg**, and unassigned **sandersn**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4252#issuecomment-4664330598) **ahejlsberg** diagnosed that top-level await reparsing mishandles JSDoc typedefs, provided a minimal repro and offered to submit a PR with a fix
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4253](https://github.com/microsoft/TypeScript-go/pull/4253) (Closed, **jakebailey**, **Copilot**)

**Emit triple\-slash references to referenced\-project sources in declaration files**

*Fix omission of preserved triple-slash references to referenced-project TypeScript sources in emitted declaration files by enhancing resolution logic.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4254](https://github.com/microsoft/TypeScript-go/issues/4254) (Open, `Needs Investigation`)

**Behavior difference: Notable inconsistencies on type inference for expando arrow function imports**

*Inconsistent handling of expando arrow function imports between tsc and tsgo results in verbose in-place type redefinitions instead of reusing imported component types.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Post-7.0`

### [PR microsoft/TypeScript-go#4255](https://github.com/microsoft/TypeScript-go/pull/4255) (Closed)

**Fix lint in darwin\-only build file**

*Re-enable the macOS CI lint job and fix lint errors in the Darwin-only build file.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4256](https://github.com/microsoft/TypeScript-go/pull/4256) (Closed)

**Fix top\-level await reparsing with following \`@typedef\`**

*Update parsing to handle top-level await statements followed by @typedef annotations without errors.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4257](https://github.com/microsoft/TypeScript-go/pull/4257) (Open)

**Don't add global diags when not checking a file**

*Avoid storing global diagnostics for files that are not being checked to improve performance.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#4258](https://github.com/microsoft/TypeScript-go/issues/4258) (Closed)

**Consider adding \`path\` entry point to public API**

*Add a path (or uri) entry point to TypeScript's public API providing fileNameToDocumentURI and documentURIToFileName functions.*

 * created by **mrazauskas**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4258#issuecomment-4668341670) **mrazauskas** said "Oh… This is already available from sync and async entry points. Amazing! Thanks a lot! (Sorry, about the noise.)"
 * (later) **mrazauskas** closed the issue

### [Issue microsoft/TypeScript-go#4259](https://github.com/microsoft/TypeScript-go/issues/4259) (Closed, `Crash`)

**panic: cache entry not found \[recovered, repanicked\] \- exponentially increasingly random sporadic crashes until full VSCode Restart**

*Intermittent ‘cache entry not found’ panics in typescript-go cause exponentially increasing VSCode crashes until a full restart.*

 * created by **klydra**
 * **klydra** added label `Crash`

### [PR microsoft/TypeScript-go#4260](https://github.com/microsoft/TypeScript-go/pull/4260) (Closed)

**Fix stack overflow caused by simplification of recursive type**

*TypeScript now removes self-referential indexed access types from unions during simplification to prevent infinite recursion.*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4671766785) **ahejlsberg** said "@typescript-bot test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4671849860) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4260#issuecomment-4671857206) **jakebailey** said "Ah, GitHub outage "

