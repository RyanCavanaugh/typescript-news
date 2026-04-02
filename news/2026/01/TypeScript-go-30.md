# Report for 2026-01-30 (Friday, January 30th, 2026)

14 different users commented on 18 different issues.

## Recommended Actions

 * Response Recommended
    * @amyssnippet reported no errors and provided command outputs and version details in [microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3828657207)

## Activity Summary

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Closed, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3718503020) **rubenferreira97** reported experiencing a process deadlock when running tsgo --build and provided a log file and project configuration details
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3720038671) **jakebailey** said "@rubenferreira97 that is totally unrelated to this issue; please file a new issue with a repro."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3814613904) **sheetalkamat** said "Can you please try build from https://github.com/microsoft/typescript-go/pull/2604 to see if it helps"
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2331](https://github.com/microsoft/TypeScript-go/pull/2331) (Open)

**Organize Imports**

*Implement functionality to automatically organize and sort imports within source files.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3814667929) **jakebailey** tested import organizing and found the shebang repeated before each import
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3814678385) **jakebailey** reported import reorganization and indentation loss in two TypeScript files
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3820320228) **iisaduan** identified missing indenting logic that could affect organize imports and cause a loss of smaller indent
 * [today](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3825049874) **johnfav03** updated the code to account for the shebang issue, changed textwriter.go to use ls.formatOptions.indentSize instead of hardcoded spaces, noted the LSP still didn’t sync indentSize settings, and explained that require statements are sorted separately following TypeScript’s import order
 * [today](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3825234891) **jakebailey** said "I think there's a bug in the way we load indent size out of the settings; it's some discrepency i noticed when working on my user prefs refactor. VS Code's setting has a different name than we do."

### [PR microsoft/TypeScript-go#2459](https://github.com/microsoft/TypeScript-go/pull/2459) (Open)

**Port \-\-isolatedDeclarations related node builder logic, with baseline updates**

*Port node builder logic for the --isolatedDeclarations option and apply baseline updates for review.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-3827377748) **Zzzen** described testing the branch and noting the type emit was cleaner, reported still hitting OOM, and asked for tips on pinpointing memory usage

### [Issue microsoft/TypeScript-go#2574](https://github.com/microsoft/TypeScript-go/issues/2574) (Open, `Crash`, **andrewbranch**)

**panic: cache entry not found \[recovered, repanicked\]**

*A panic occurs in typescript-go v7.0.0-dev when cloning project snapshots due to a missing cache entry.*

 * created by **joepjoosten**
 * **joepjoosten** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2598](https://github.com/microsoft/TypeScript-go/issues/2598) (Closed, `Crash`, **iisaduan**)

**Auto\-imports broken in JS files when user preferences are used**

*Applying user preferences in JavaScript files causes auto-import suggestions to fail and trigger a panic in the TypeScript-Go server*

 * (2 days ago) **andrewbranch** assigned to **iisaduan**, and unassigned **andrewbranch**, **Copilot**
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#2604](https://github.com/microsoft/TypeScript-go/pull/2604) (Closed)

**Some of the changes to improve \-\-build memory footprint**

*Improved build memory footprint by fixing writerPool retention, restricting source file caching to d.ts/json, and adjusting builder concurrency flag.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3821615246) **Zzzen** explained that tsgo fully expanded DeepReadonly<LargeType> in the generated .d.ts, causing excessively large declaration files
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3821657311) **jakebailey** said "Can you try building #2459 and see if that fixes your issue?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3822178978) **Zzzen** confirmed that the emitted types and .d.ts files matched tsc output and requested a merge soon
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3825090985) **jakebailey** asked whether the merge request referred to the other PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3825131378) **sheetalkamat** clarified that the build process wasn't fully concurrent due to high memory usage and agreed that using --builders 1 is acceptable
 * (today) **sheetalkamat** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2604#issuecomment-3827356078) **Zzzen** clarified that they meant the referenced pull request

### [Issue microsoft/TypeScript-go#2611](https://github.com/microsoft/TypeScript-go/issues/2611) (Closed)

**typeRoots behavior difference from tsc v9 \(vitest/globals\)**

*tsgo fails to recognize vitest/globals types configured via typeRoots, resulting in 'vi' name not found errors while tsc succeeds.*

 * created by **sammarks-stukent**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2611#issuecomment-3819738992) **sammarks-stukent** said "Might be related to https://github.com/microsoft/typescript-go/issues/2147"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2612](https://github.com/microsoft/TypeScript-go/issues/2612) (Open, `Crash`)

**tsgo crashes**

*tsgo crashes with a stack trace when running deno check on ignore_test.ts with DENO_UNSTABLE_TSGO enabled in Deno 2.6.6.*

 * created by **sigmaSd**
 * **sigmaSd** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2612#issuecomment-3828657207) **amyssnippet** reported that they didn’t get any errors and shared clone commands and deno version output

### [PR microsoft/TypeScript-go#2614](https://github.com/microsoft/TypeScript-go/pull/2614) (Closed)

**fix: use typeRoot instead of candidate when resolving types references from config**

*Modify resolveTypeReferenceDirective to use typeRoots rather than candidate paths when resolving type references from tsconfig, fixing resolution errors.*

 * created by **sammarks-stukent**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2614#issuecomment-3820300047) **sammarks-stukent** said "@microsoft-github-policy-service agree company="Stukent""
 * [today](https://github.com/microsoft/TypeScript-go/pull/2614#issuecomment-3824348781) **sammarks-stukent** said "@andrewbranch for sure! Extra tests have been removed 👍 "
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2616](https://github.com/microsoft/TypeScript-go/pull/2616) (Closed)

**fix autoimports crash in js files **

*Fix autoimports crash in JavaScript files, correct miscapitalization parsing bug, and add a parsing test.*

 * created by **iisaduan**
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#2620](https://github.com/microsoft/TypeScript-go/pull/2620) (Open)

**Bring back async API, allow API connection to LSP process**

*Reintroduce a decoupled async JSON-RPC API client and server in the LSP to enable external extensions to query TypeScript state.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#2621](https://github.com/microsoft/TypeScript-go/issues/2621) (Open, **iisaduan**, **Copilot**)

**Fourslash is broken when making requests in unconfigured \.js files**

*Fourslash requests in unconfigured .js files fail with “no project found” errors, breaking tests such as auto-import completion.*

 * created by **iisaduan**
 * (today) **iisaduan** assigned to **Copilot**, **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2621#issuecomment-3825894034) **DanielRosenwasser** reported that restarting the extension while a .js file was open produced a 'no project found for URI' diagnostic error

### [PR microsoft/TypeScript-go#2622](https://github.com/microsoft/TypeScript-go/pull/2622) (Open, **iisaduan**, **Copilot**)

**Fix inferred project JavaScript file support when compiler options are provided**

*Apply AllowJs:true default for unset compilerOptions in inferred projects to include JavaScript files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **iisaduan**

### [PR microsoft/TypeScript-go#2623](https://github.com/microsoft/TypeScript-go/pull/2623) (Open)

**Fix inlay hints panic: guard against stale line map in LineAndCharacterToPosition**

*Prevent inlay hint panics by guarding against stale line map offsets in LineAndCharacterToPosition*

 * created by **abelcha**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2623#issuecomment-3827319301) **jakebailey** said "I don't think we should do this. If this happens, the caller is at fault and needs to be fixed. It can only be a symptom of a worse problem above."

### [Issue microsoft/TypeScript-go#2624](https://github.com/microsoft/TypeScript-go/issues/2624) (Closed, `Crash`)

**\*lsproto\.ID\.String\(\) hangs if nil on android**

*Printing a nil request ID in lsproto.ID.String() causes the LSP server to hang on Android.*

 * created by **cplepage**
 * **cplepage** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2624#issuecomment-3827583936) **jakebailey** expressed confusion about running the LSP server on Android
 * [today](https://github.com/microsoft/TypeScript-go/issues/2624#issuecomment-3827587952) **cplepage** shared a link to fullstackedorg/fullstacked, noted it ran smoothly, mentioned the fix wasn't purely Android related, and asked for thoughts
 * [today](https://github.com/microsoft/TypeScript-go/issues/2624#issuecomment-3827588891) **jakebailey** expressed shock that notifications had nil IDs and asked why the Info implementation wasn’t handling them
 * [today](https://github.com/microsoft/TypeScript-go/issues/2624#issuecomment-3827594925) **cplepage** reported that fmt.Println also hung and that they tried iterating through args before calling fmt.Sprint but found handling the nil case cleaner
 * [today](https://github.com/microsoft/TypeScript-go/issues/2624#issuecomment-3827604194) **jakebailey** noted that the method returned (<nil>), which seemed strange
 * [today](https://github.com/microsoft/TypeScript-go/issues/2624#issuecomment-3827626619) **cplepage** said "Yeah I'm not sure why it's not seg faulting instead of hanging... or yeah just printing ``"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2625](https://github.com/microsoft/TypeScript-go/pull/2625) (Closed)

**Enhance logging for handled methods with request ID**

*Enhance logging for handled methods by including request IDs to improve traceability and debugging.*

 * created by **cplepage**
 * (today) **cplepage** closed the issue
 * (today) **cplepage** reopened the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2626](https://github.com/microsoft/TypeScript-go/issues/2626) (Open, `Domain: Editor`)

**Extension softly crashes \(hangs indefinitely\) at sudden**

*The TypeScript extension v0.20260131.1 hangs and shows stale diagnostics when experimental useTsgo and project diagnostics are enabled, requiring restarts.*

 * created by **piscopancer**
 * **piscopancer** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961) (Open, `bug`, `Domain: Emit`, `Domain: Type Checking`, **jakebailey**)

**tsgo fails to resolve namespace symbols in non\-extends contexts across files**

*tsgo fails to qualify namespace symbols A and Afunc outside extends contexts across files, causing incorrect JS and runtime errors.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3822550361) **rubenferreira97** asked whether TypeScript 6's deprecation behavior within the same file was intended and suggested finding a middle ground for namespace merging restrictions
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3822759112) **magic-akari** highlighted that more complex cross-namespace scenarios require careful support definition and provided an example that works in TypeScript 5
 * [today](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3824394383) **dtscd** provided a code example demonstrating that a simple patch resolves nested namespace access within the same file
 * [later](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828459486) **magic-akari** thanked @dtscd for the patch, confirmed it worked for same-file scenarios, and asked whether cross-namespace value qualification should be supported, noting architectural consistency and ecosystem precedent
 * [later](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828685368) **dtscd** argued that removing cross-namespace resolution trivialized namespaces, highlighted ES modules' per-file scoping and minimal linking performance impact, and lamented added user complexity compared to Go

