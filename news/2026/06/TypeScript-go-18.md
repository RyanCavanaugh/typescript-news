# Report for 2026-06-18 (Thursday, June 18th, 2026)

14 different users commented on 42 different issues.

## Recommended Actions

 * Response Recommended
    * @geelove reported that switching to the experimental native preview didn't update the TS server version in [microsoft/TypeScript-go#4292](https://github.com/microsoft/TypeScript-go/issues/4292#issuecomment-4748649207)
    * @christianvuerings asked @jakebailey to review the PR in [microsoft/TypeScript-go#4297](https://github.com/microsoft/TypeScript-go/pull/4297#issuecomment-4744853071)
    * @hkleungai reported that the issue remains in version 7.0.0-dev.20260619.1 for both .js and .tsx extensions in [microsoft/TypeScript-go#4310](https://github.com/microsoft/TypeScript-go/issues/4310#issuecomment-4750101327)
    * @hkleungai asked why block comments weren't preserved when transpiling reconstructed types in [microsoft/TypeScript-go#4352](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4744716271)
    * @maik-bol provided detailed analysis of the Yarn-side bug and its failure mode in [microsoft/TypeScript-go#4368](https://github.com/microsoft/TypeScript-go/issues/4368#issuecomment-4746202177)
    * @nikelborm provided error logs about symlink failures in [microsoft/TypeScript-go#4372](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4749620235)

## Activity Summary

### [Issue microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424) (Closed, `possible improvement`)

**Request for support for additional architectures**

*Support and a roadmap are requested for riscv64, ppc64le, and loong64 architectures in typescript-go.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-3721623829) **darkyzhou** clarified whether the concern about adding more architectures was mainly about increased CI running time and proposed starting support for riscv64, loong64, ppc64le, and s390x on Linux
 * (11 weeks ago) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4746763098) **jakebailey** noted that the RC supports a full set of platform-specific optionalDependencies for tagged releases and that nightly releases will remain limited to arm64 and amd64 on darwin, linux, and windows
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4748935526) **darkyzhou** said "Thanks!"

### [Issue microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032) (Closed, `Domain: Editor`, `Needs More Info`)

**tsgo \-\-lsp memory leak on large projects / triggers OOM**

*The tsgo LSP process in the TypeScript Native Preview extension leaks memory when handling large projects, causing OOM on low-RAM Linux machines.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4623808592) **andrewbranch** said "@jakebailey any ideas?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4634340466) **jakebailey** said "I have no idea, the only way I can think this is breaking is due to truncation but if the process is not exiting, there's no reason for it."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4741315097) **doylio** shared a heap profile attachment
 * [today](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4744371800) **jakebailey** said "That one loads, but doesn't provide much interesting besides typical checker stuff, which should be getting cleaned up, including on idle after #3435 too..."

### [PR microsoft/TypeScript-go#3391](https://github.com/microsoft/TypeScript-go/pull/3391) (Open, **ahejlsberg**)

**Fix inference from unions of arrays with different nesting depths**

*Add a matching pass to infer equally nested arrays first, correcting generic type inference for unions like T[] | T[][]*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3391#issuecomment-4696161856) **typescript-automation[bot]** started build jobs and posted status updates with result links
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3391#issuecomment-4696378472) **typescript-automation[bot]** provided performance run results comparing baseline and PR metrics to jakebailey
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3391#issuecomment-4696630928) **typescript-automation[bot]** reported that the tsc results for the top 400 repos comparing main and the pull request merge looked good
 * (today) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3687](https://github.com/microsoft/TypeScript-go/issues/3687) (Closed, `possible improvement`)

**No compiled packages for netbsd**

*No compiled @typescript/native-preview package is available for NetBSD x64, causing an error.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3687#issuecomment-4375095282) **jakebailey** explained that builds currently match VS Code and that supporting additional platforms will be considered but nightly builds for all platforms are unlikely at this time
 * (6 weeks ago) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3687#issuecomment-4746763293) **jakebailey** noted that the RC supports a full set of platform-specific optionalDependencies for tagged releases and that nightly releases will remain limited to arm64 and amd64 on darwin, linux, and windows
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3722](https://github.com/microsoft/TypeScript-go/issues/3722) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**custom tsgo path is now ignored**

*VS Code's TypeScript native-preview ignores the configured custom tsgo path and launches its bundled tsgo instead.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3722#issuecomment-4709452700) **oMatheusmol** said "Hi! I noticed that #3765 was closed, but this issue is still open and targeted for the 7.0 RC milestone. Is this still available for contribution? I'd be happy to take a look."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3722#issuecomment-4709558358) **jakebailey** said "We are currently moving everything around in prep for a release; it wouldn't be helpful to get a PR for this outside the team, no."
 * (today) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3727](https://github.com/microsoft/TypeScript-go/issues/3727) (Open, `Domain: Editor`, `possible improvement`, **jakebailey**)

**Unify tsdk between built\-in and native preview extensions**

*Share the built-in tsdk setting with the native preview and choose the TypeScript server based on useTsGo and tsdk directory.*

 * **RyanCavanaugh** assigned to **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3727#issuecomment-4674335592) **DanielRosenwasser** outlined a step-by-step approach to determine whether to activate Strada, Corsa, or built-in TypeScript servers based on tsdk and useTsgo settings, including precedence and folder validation
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3727#issuecomment-4674445561) **andrewbranch** proposed a flowchart outlining the priority of settings in deciding between Corsa and Strada and the TypeScript SDK
 * (today) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3848](https://github.com/microsoft/TypeScript-go/issues/3848) (Closed, `Domain: Editor`, **DanielRosenwasser**)

**Issue warning when extensions try to contribute TSServer plugins that while \`useTsgo\` is on**

*Warn users when extensions contribute TSServer plugins with useTsgo enabled, offering Dismiss, Disable Native Preview, and Don't Show Again options.*

 * (5 weeks ago) **DanielRosenwasser** added label `Domain: Editor`, set milestone to `TypeScript 7.0 RC`, and assigned to **DanielRosenwasser**
 * (today) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4063](https://github.com/microsoft/TypeScript-go/pull/4063) (Closed)

**Warn on TSServer Plugin Contributions from other extensions**

*Display warnings when external extensions contribute TSServer plugins in both single-folder and multi-root workspaces*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and removed from milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4158](https://github.com/microsoft/TypeScript-go/pull/4158) (Open, **jakebailey**, **Copilot**)

**Preserve source text for negative numeric literals in declaration emit**

*Preserve original source text for top-level negative numeric const literals in TypeScript declaration emit instead of canonicalizing them.*

 * **Copilot** assigned to **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4595857814) **jakebailey** said "@copilot+claude-opus-4.8 no test??"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4595951958) **Copilot** added a compiler test covering negative and positive numeric literal behaviors with baselines
 * [today](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4744666084) **jakebailey** said "@copilot+gpt-5.5 Merge main and update tests"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4158#issuecomment-4744848306) **Copilot** merged origin/main and resolved pseudotypenodebuilder.go conflict by combining flag handling and reused-literal state, ran tests successfully with no compiler baseline updates needed

### [PR microsoft/TypeScript-go#4160](https://github.com/microsoft/TypeScript-go/pull/4160) (Open, **jakebailey**, **Copilot**)

**Preserve inline parameter comments on inferred function types in declaration emit**

*Restore inline parameter comments when emitting declarations for inferred function types by preserving parameter positions.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4160#issuecomment-4744667296) **jakebailey** said "@copilot+gpt-5.5 Merge main and update tests"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4160#issuecomment-4744925609) **Copilot** merged main and updated the affected baselines

### [Issue microsoft/TypeScript-go#4292](https://github.com/microsoft/TypeScript-go/issues/4292) (Open, `Domain: Editor`)

**Can't enable TypeScript native preview in VS Code**

*VS Code fails to activate the experimental TypeScript Native Preview and continues using the previous TypeScript version.*

 * **denexapp** added label `Domain: Editor`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4292#issuecomment-4694044207) **DanielRosenwasser** said "Weirdly I have hit something similar but I'm no longer able to repro it."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4292#issuecomment-4694635964) **denexapp** said "@DanielRosenwasser if there are ways to see* debug logs, I can do that and attach them here"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4292#issuecomment-4748649207) **geelove** said "This doesn't work for me either, switching the ts server versions to the experimental native preview does nothing and it still runs VS code's version (6.0.3)"

### [PR microsoft/TypeScript-go#4297](https://github.com/microsoft/TypeScript-go/pull/4297) (Open)

**Push per\-file diagnostics for clients without pull diagnostics support**

*Implement per-file push diagnostics for clients with publishDiagnostics but no pull support, sending open/change/close updates without affecting pull-capable clients.*

 * created by **christianvuerings**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4297#issuecomment-4744853071) **christianvuerings** asked @jakebailey to take a look at the PR and noted that Claude code didn't support pull diagnostics and TypeScript Go didn't support push diagnostics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4297#issuecomment-4745627690) **jakebailey** said "We haven't had time to test it; we'd have to disable pull diags and test in VS Code and make sure it works. Push diagnostics get tricky when dealing with LS restarts and other racy ish conditions."

### [Issue microsoft/TypeScript-go#4310](https://github.com/microsoft/TypeScript-go/issues/4310) (Open, **jakebailey**, **Copilot**)

**Behavior difference: \(Another\) Expando function emit between tsc & tsgo**

*tsgo omits generating propTypes for function component aliases while tsc emits them*

 * created by **hkleungai**
 * (5 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4310#issuecomment-4745590237) **weswigham** said "Is this by chance fixed by #4356?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4310#issuecomment-4745602654) **hkleungai** said "I guess we can wait for the next nightly release then. 😄 "
 * [later](https://github.com/microsoft/TypeScript-go/issues/4310#issuecomment-4750101327) **hkleungai** said "Issue remains in 7.0.0-dev.20260619.1, in both .js & .tsx extensions 😓 "

### [PR microsoft/TypeScript-go#4311](https://github.com/microsoft/TypeScript-go/pull/4311) (Open, **jakebailey**, **Copilot**)

**Fix declaration emit for expando function aliases**

*Modify declaration generation so exported expando function aliases are emitted as function declarations with namespaces to expose merged properties.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4311#issuecomment-4744669358) **jakebailey** said "@copilot+gpt-5.5 Merge main and update tests"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4311#issuecomment-4744899347) **Copilot** merged main, updated tests, and reported successful validation

### [Issue microsoft/TypeScript-go#4317](https://github.com/microsoft/TypeScript-go/issues/4317) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Behavior difference: tsgo inconsistently emits overloaded signature**

*tsgo inconsistently emits overloaded signatures for certain class field and variable functions using interface-based overloads*

 * created by **hkleungai**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4317#issuecomment-4707639427) **hkleungai** noted inconsistency between tsgo and tsc in emitting overloaded parameters and asked if existing TS6 behavior on Parameters<typeof overloadInline> is a bug
 * (today) **weswigham** added labels `Needs Investigation`, `bug`, `Domain: Declaration Emit`, removed label `Needs Investigation`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4325](https://github.com/microsoft/TypeScript-go/issues/4325) (Closed, **DanielRosenwasser**, **Copilot**)

**Behavior difference: Reassigning class method inside constructor will make tsgo emit an extra line of method signature**

*tsgo emits an additional method declaration for a class method rebound in the constructor, unlike plain TypeScript.*

 * created by **hkleungai**
 * (2 days ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4331](https://github.com/microsoft/TypeScript-go/pull/4331) (Closed, **DanielRosenwasser**, **Copilot**)

**Skip bound method assignments in JS declaration emit**

*Skip redundant property signatures for constructor-bound methods in JS declaration emit by detecting assignments and tracking declared members.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4335](https://github.com/microsoft/TypeScript-go/issues/4335) (Open, `Needs Investigation`, **andrewbranch**, **Copilot**)

**checker\.getBaseTypes panics for type alias to generic interface instantiation**

*checker.getBaseTypes panics with a nil pointer dereference when processing a type alias to a generic interface instantiation*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Post-7.0`
 * **andrewbranch** assigned to **Copilot**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4335#issuecomment-4752576072) **ahejlsberg** explained that getBaseTypes was being called on a type reference and suggested calling getTarget first

### [PR microsoft/TypeScript-go#4349](https://github.com/microsoft/TypeScript-go/pull/4349) (Open)

**Collate\-free import sorting**

*Introduce a collate-free import sorting scheme with customizable ordinal and natural case options to replace and deprecate x/text/collate dependency*

 * created by **jakebailey**
 * **jakebailey** added to milestone `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#4351](https://github.com/microsoft/TypeScript-go/pull/4351) (Closed)

**Deduplicate declaration emit for this\-assigned methods**

*Deduplicate declaration emissions of this-assigned methods and correct late binding for static methods to ensure accurate type checking.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4352](https://github.com/microsoft/TypeScript-go/issues/4352) (Open)

**Behavior difference: Block comments on \`@typedef\` structural types are not preserved, if they are imported and reconstructed as inline types in another file**

*tsgo fails to preserve block comments on @typedef structural types when they are imported and reconstructed as inline types*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4744615896) **jakebailey** said "You're expecting the comments from another file to come along? If that was happening, I feel like that is a bug in the old codebase."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4744716271) **hkleungai** said "But why not? If the transpiler is reconstructing an existing type in-place, shouldn't the original block comment be brought over to the new types as well? 😕 "
 * [today](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4745039645) **jakebailey** said "We don't do that for TS, no?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4745160967) **hkleungai** described expectation that jsdoc-defined types produce valid emits and propagate attribute comments in IDEs as they do in TS 6

### [PR microsoft/TypeScript-go#4356](https://github.com/microsoft/TypeScript-go/pull/4356) (Closed)

**Re\-allow nested cjs export assignments in declaration emit**

*Restore support for nested CJS export assignments in declaration emit, update export ordering and naming, and revise related tests.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4356#issuecomment-4744439500) **weswigham** pointed out the deleted chunk and supporting binder/ast structs and logic
 * [today](https://github.com/microsoft/TypeScript-go/pull/4356#issuecomment-4744448938) **jakebailey** said "Ah, it was just a oneliner"
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4357](https://github.com/microsoft/TypeScript-go/pull/4357) (Open)

**Lint on all OSs**

*Run lint checks on all operating systems in CI to simplify maintenance and avoid omissions.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4357#issuecomment-4744155276) **jakebailey** said "45 minutes, yikes"

### [Issue microsoft/TypeScript-go#4359](https://github.com/microsoft/TypeScript-go/issues/4359) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Missing some completion and hover document in namespaced JSX intrinsic element**

*VSCode’s TypeScript JSX support lacks attribute completions and hover documentation for namespaced JSX intrinsic elements like foo:bar*

 * created by **hjkcai**
 * **hjkcai** added label `Domain: Editor`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4363](https://github.com/microsoft/TypeScript-go/issues/4363) (Open, **jakebailey**, **Copilot**)

**Behavior difference: Comment above \`@typedef\` does not become comment for the corresponding emitted type in tsgo**

*tsgo fails to preserve JSDoc comments above @typedef by emitting them after the generated type declaration*

 * created by **hkleungai**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4364](https://github.com/microsoft/TypeScript-go/pull/4364) (Open)

**Add default\.pgo file for main entrypoint**

*Add a default.pgo file for the main entrypoint to utilize the new performance infrastructure*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4364#issuecomment-4743658006) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4364#issuecomment-4743658692) **typescript-automation[bot]** notified of job start and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4364#issuecomment-4743897697) **typescript-automation[bot]** reported the requested perf run results

### [PR microsoft/TypeScript-go#4365](https://github.com/microsoft/TypeScript-go/pull/4365) (Open, **jakebailey**, **Copilot**)

**Preserve typedef comments in declaration emit**

*Preserve descriptive JSDoc comments on typedefs and callbacks in emitted declaration files while preventing duplicate comment output*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4366](https://github.com/microsoft/TypeScript-go/pull/4366) (Open, **jakebailey**, **Copilot**)

**Fix namespaced JSX intrinsic completions and hover**

*Add attribute completions and hover support for namespaced JSX elements by updating context recognition and quick-info resolution.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4366#issuecomment-4745452398) **jakebailey** said "@copilot a now non-failing test needs to be removed from  internal/fourslash/_scripts/failingTests.txt"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4366#issuecomment-4745572053) **Copilot** removed the now-passing TestQuickInfoOnNewKeyword01 from failingTests.txt

### [PR microsoft/TypeScript-go#4367](https://github.com/microsoft/TypeScript-go/pull/4367) (Open)

**Allow parameter type reuse even when return type is inferred**

*Allow reusing parameter types when return types are inferred by adding void return type inference for functions with no return statements.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4745588540) **jakebailey** said "IIRC we can't do this, because even a function without a return can have its type differ based on whether or not all paths lead to never?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4745678978) **weswigham** clarified that ID return inferences already treat a returned expression as T rather than never, similar to other control-flow-influenced return cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4746053881) **jakebailey** questioned the return type inference behavior and expressed surprise it was allowed
 * [today](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4746204661) **weswigham** explained that they discard pseudotype-inferred results mismatches in normal builds making the issue harmless and noted that in single-file emit incorrect types can still be emitted, affecting all return type inferences
 * [today](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4746270494) **jakebailey** said "But by construction, we don't ever even try to produce things if we know we cannot, by the rules we defined for ID early on. I don't think this is one of them, right?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4746611248) **weswigham** described a potential improvement by adding a restriction to bail on syntactic inference when function calls occur outside return expressions, noted exceptions for getters, setters, and proxies, and explained how exit() propagation differs between function returns and const contexts

### [Issue microsoft/TypeScript-go#4368](https://github.com/microsoft/TypeScript-go/issues/4368) (Closed)

**@typescript/typescript6 compat package fails to install under Yarn \(builtin TypeScript patch hard\-errors on missing 'lib/\_tsc\.js'\)**

*Yarn’s built-in TypeScript compat patch incorrectly targets the @typescript/typescript6 alias and fails on missing lib/_tsc.js*

 * created by **maik-bol**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4368#issuecomment-4746031377) **jakebailey** questioned the need for changes, explained yarn should patch the reexported typescript dependency, noted patching the wrong package is a bug, and referred to issue #1966 for PnP
 * [today](https://github.com/microsoft/TypeScript-go/issues/4368#issuecomment-4746202177) **maik-bol** explained the Yarn-side bug causing the shim package to be patched incorrectly and the optional builtin patch failure handling
 * (today) **maik-bol** closed the issue

### [Issue microsoft/TypeScript-go#4369](https://github.com/microsoft/TypeScript-go/issues/4369) (Open, **jakebailey**)

**Publish an "other" platform VSIX**

*Publish a generic VSIX for unsupported platforms that omits TypeScript bundling and uses configured tsdk*

 * created by **jakebailey**
 * (today) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#4370](https://github.com/microsoft/TypeScript-go/issues/4370) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**\`js/ts\.preferences\.useAliasesForRenames\` not respected**

*Disabling js/ts.preferences.useAliasesForRenames has no effect in VS Code’s native TypeScript extension, causing renamed imports to be aliased rather than updated at their source.*

 * created by **LiamMorrow**
 * **LiamMorrow** added label `Domain: Editor`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4371](https://github.com/microsoft/TypeScript-go/pull/4371) (Open, **jakebailey**, **Copilot**)

**Respect useAliasesForRenames in rename edits**

*Renames now respect the useAliasesForRenames preference, updating exported declarations when disabled instead of aliasing imports.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4372](https://github.com/microsoft/TypeScript-go/issues/4372) (Closed, **jakebailey**, **Copilot**)

**7\.0\.1\-rc binary in watch mode fails to resolve symlinks in node\_modules**

*TypeScript 7.0.1-rc watch mode fails to resolve or watch symlinked node_modules dependencies, causing fanotify errors.*

 * created by **nikelborm**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4749620235) **nikelborm** reported that bun max spawned multiple tsc watchers and produced symlink errors
 * [later](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4752646521) **jakebailey** suggested ensuring that fswatch validated directory paths or ignored non-directory symlinks
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4373](https://github.com/microsoft/TypeScript-go/issues/4373) (Open)

**Project\-reference redirect fails for directory \(\`index\.ts\`\) subpaths of symlinked packages**

*Importing a directory subpath from a symlinked, unbuilt project-reference package fails to resolve to source with TS2307.*

 * created by **sverrejoh**

### [PR microsoft/TypeScript-go#4374](https://github.com/microsoft/TypeScript-go/pull/4374) (Open)

**Resolve symlinked project\-reference directory \(\`index\.ts\`\) subpaths to source**

*Fix regression causing directory subpath imports in symlinked project references to fail by lazily registering package symlinks.*

 * created by **sverrejoh**

### [Issue microsoft/TypeScript-go#4375](https://github.com/microsoft/TypeScript-go/issues/4375) (Open)

**Add native\-preview API for capturing \.d\.ts emit output**

*Request for extending the TypeScript native-preview JS API to emit and capture .d.ts declaration output via virtual filesystem callbacks.*

 * created by **hegrec**

### [PR microsoft/TypeScript-go#4376](https://github.com/microsoft/TypeScript-go/pull/4376) (Closed, **jakebailey**, **Copilot**)

**Fix watches on symlinked directories**

*Fix watch mode on symlinked directories by resolving watch roots to physical paths and preserving symlink paths in events.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

