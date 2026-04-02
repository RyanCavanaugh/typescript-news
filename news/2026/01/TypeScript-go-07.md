# Report for 2026-01-07 (Wednesday, January 7th, 2026)

7 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @darkyzhou asked whether the primary concern was increased CI running time and proposed adding support for riscv64, loong64, ppc64le, and s390x on Linux in [microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3721623829)

## Activity Summary

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3698941951) **spanishpear** reported high memory usage when typechecking a large project and its dependents, noted that tsc was faster, provided profiling details, and asked if the test was configured correctly
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3700541007) **spanishpear** noted similar performance struggles in tsgolint and pointed to a related issue for potential resolution
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3718503020) **rubenferreira97** reported experiencing a process deadlock when running tsgo --build and provided a log file and project configuration details
 * [today](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3720038671) **jakebailey** said "@rubenferreira97 that is totally unrelated to this issue; please file a new issue with a repro."

### [Issue microsoft/TypeScript-go#2336](https://github.com/microsoft/TypeScript-go/issues/2336) (Open, `Crash`, **jakebailey**, **Copilot**)

**Crash for signature help in arrow function parameters**

*Signature help invoked on arrow function parameters crashes the TypeScript server without a stack trace*

 * (1 month ago) **DanielRosenwasser** assigned to **Copilot**, **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3711830899) **gabritto** explained that printing the signature label for an anonymous function type generated an invalid UTF-8 name, causing JSON marshalling to fail and the server to stop
 * [today](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3720201285) **jakebailey** said "We should probably make it so that the node builder detects internal types and auto-escapes them like the old compiler?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3720210437) **gabritto** asked where the old compiler escaped internal types and noted that Strada returned "__type(...)" as label
 * [today](https://github.com/microsoft/TypeScript-go/issues/2336#issuecomment-3720242722) **jakebailey** clarified that symbol names with __ prefixes sometimes leaked, which was unacceptable in Go code due to the UTF-8 trick, and that they had not found a better alternative

### [Issue microsoft/TypeScript-go#2399](https://github.com/microsoft/TypeScript-go/issues/2399) (Closed, `bug`, **DanielRosenwasser**)

**Implement JSX tag\-closing completions**

*JSX closing tag isn't auto-inserted when using tsgo but works with TypeScript 5.9.*

 * created by **navya9singh**
 * **navya9singh** added label `bug`
 * **DanielRosenwasser** assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2400](https://github.com/microsoft/TypeScript-go/pull/2400) (Closed)

**fix: show completion after class members with const assertion initializers**

*Enable code completion suggestions after class members initialized with const assertions.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2413](https://github.com/microsoft/TypeScript-go/pull/2413) (Closed)

**Make repo package funcs lazy, not broken**

*Make repository package functions initialize lazily, fix go.mod upward lookup, and panic early on invalid embedded source paths.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2419](https://github.com/microsoft/TypeScript-go/pull/2419) (Open)

**Fix: Handle Negative VLQ Offsets in Source Maps for VSCode Jump to Definition**

*Clamp inverted ranges caused by negative VLQ offsets in source maps to restore correct VSCode jump to definition behavior.*

 * created by **sethconvex**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-3684054114) **sethconvex** agreed company affiliation as Convex, Inc.
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-3695863591) **sethconvex** asked if there was a path to getting this into main and for instructions on adding spec behavior fixes to the roadmap
 * [today](https://github.com/microsoft/TypeScript-go/pull/2419#issuecomment-3720619871) **jakebailey** said "We were all on vacation 🙂 "

### [Issue microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424) (Open)

**Request for support for additional architectures**

*Support and a roadmap are requested for riscv64, ppc64le, and loong64 architectures in typescript-go.*

 * created by **darkyzhou**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3690771942) **jakebailey** noted that testing and releasing on additional platforms would be infeasible, stated that the current list matches VS Code marketplace support, and asked how the commonality of those platforms was determined
 * [today](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3720653589) **jakebailey** noted that esbuild builds all variants without testing and cautioned about the signing overhead with many optional dependencies
 * [today](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3721623829) **darkyzhou** clarified whether the concern about adding more architectures was mainly about increased CI running time and proposed starting support for riscv64, loong64, ppc64le, and s390x on Linux

### [Issue microsoft/TypeScript-go#2427](https://github.com/microsoft/TypeScript-go/issues/2427) (Open, `bug`)

**\`isolatedDeclarations\` is not yet implemented**

*tsgo does not implement the isolatedDeclarations compiler option, so it fails to report missing annotations unlike tsc 5.9.*

 * created by **so1ve**
 * **DanielRosenwasser** added label `bug`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3720630512) **jakebailey** said "See also #1693, #2459"

### [Issue microsoft/TypeScript-go#2441](https://github.com/microsoft/TypeScript-go/issues/2441) (Closed)

**using tsgo fails with pnpx**

*Invoking tsgo via pnpx with @typescript/native-preview fails with a spawnSync ENOENT error because tsgo.exe cannot be found.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3711193517) **TFTomSun** suggested that a Windows long path issue caused the ENOENT spawnSync error due to a path exceeding 256 characters
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3712210293) **DanielRosenwasser** said "So would this be a bug in pnpx?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3712297789) **JoostK** doubted that pnpx had a bug and explained that the tsgo JS wrapper spawned a native binary at a too-long path
 * [today](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3720254684) **jakebailey** said "Yes, we just do execFileSync with the path name. Not super clear to me why pnpx/npx/etc could do better here for binaries (in general) since surely those paths would be long too."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3720405992) **jakebailey** said "I think #2448 should fix it"

### [Issue microsoft/TypeScript-go#2443](https://github.com/microsoft/TypeScript-go/issues/2443) (Open)

**\[Doc\]: paths map value points to removed baseUrl value**

*Inline documentation incorrectly references the removed baseUrl option for computing paths map values.*

 * created by **tanepiper**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2443#issuecomment-3720182702) **jakebailey** mentioned the source of the tooltips in schemastore and suggested updating them with neutral language

### [Issue microsoft/TypeScript-go#2445](https://github.com/microsoft/TypeScript-go/issues/2445) (Open, `bug`, **andrewbranch**)

**resolvePackageJsonExports false ignored in tsgo, works in v5\.9 and v6**

*tsgo ignores resolvePackageJsonExports:false causing incorrect import paths in generated d.ts files, unlike TypeScript 5.9 and 6 preview*

 * created by **freshp86**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2445#issuecomment-3719228344) **freshp86** uploaded a minimal repro example
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2446](https://github.com/microsoft/TypeScript-go/issues/2446) (Open, **jakebailey**, **Copilot**)

**\`tsgo\` emits invalid code for decorated class methods with \`Symbol\` names**

*When compiling decorated class methods with computed Symbol names, tsgo emits invalid code referencing _a, causing a ReferenceError.*

 * created by **KostyaTretyak**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2447](https://github.com/microsoft/TypeScript-go/pull/2447) (Open, **jakebailey**, **Copilot**)

**Fix decorated class methods with Symbol names to emit valid code**

*tsgo emits invalid JavaScript for decorated class methods with computed Symbol names, causing a ReferenceError due to an undefined variable.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2448](https://github.com/microsoft/TypeScript-go/pull/2448) (Closed)

**Handle long paths in native\-preview tsgo entrypoint**

*Enable the native-preview tsgo entrypoint to correctly handle long file paths.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2449](https://github.com/microsoft/TypeScript-go/pull/2449) (Closed)

**Update SECURITY\.md**

*Update SECURITY.md by copying over content from the main TypeScript repository.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2450](https://github.com/microsoft/TypeScript-go/issues/2450) (Open, `bug`, **iisaduan**)

**Review ported code from formatter**

*The Go port of the TypeScript formatter omitted retrieving the preceding token's parent before falling back to previousParent.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **weswigham**

### [PR microsoft/TypeScript-go#2451](https://github.com/microsoft/TypeScript-go/pull/2451) (Closed)

**Port the \`jsxClosingTag\` command**

*Port the jsxClosingTag command in the TypeScript Go plugin to resolve issues 2369 and 2399.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2452](https://github.com/microsoft/TypeScript-go/pull/2452) (Closed)

**Fix AST construction during error recovery in parsing JSX**

*Fixed AST construction in JSX parsing error recovery for mismatched tags by porting previous parsing logic and removing outdated baselines.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2454](https://github.com/microsoft/TypeScript-go/issues/2454) (Closed, **ahejlsberg**)

**\`tsgo\` slow \- too much type and type instantiation without \`\-\-singleThreaded\` options**

*Excessive type instantiation in tsgo results in much slower builds than tsc unless using --singleThreaded.*

 * created by **noelkim-prestolabs**

### [Issue microsoft/TypeScript-go#2455](https://github.com/microsoft/TypeScript-go/issues/2455) (Open, `Needs More Info`)

**TSGO not reporting TS2548**

*TSGO reports TS6133 but omits the TS2548 error when spreading a value typed as unknown[]|null.*

 * created by **Titozzz**

