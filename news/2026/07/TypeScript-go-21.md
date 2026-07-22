# Report for 2026-07-21 (Tuesday, July 21st, 2026)

20 different users commented on 41 different issues.

## Recommended Actions

 * Response Recommended
    * @elramus provided repro steps as requested in [microsoft/TypeScript-go#4587](https://github.com/microsoft/TypeScript-go/issues/4587#issuecomment-5047689267)
    * @jinxiangqiang asked for an expedited release in [microsoft/TypeScript-go#4677](https://github.com/microsoft/TypeScript-go/issues/4677#issuecomment-5042964606)
    * @daniele-orlando reported a type inference regression in TypeScript 7 in [microsoft/TypeScript-go#4686](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5037305000)
    * @daniele-orlando asked to mark the issue as a bug due to a regression in TypeScript 7 in [microsoft/TypeScript-go#4686](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5037399383)
    * @microsoft-github-policy-service asked the user to agree to the CLA by replying with the appropriate command in [microsoft/TypeScript-go#4696](https://github.com/microsoft/TypeScript-go/pull/4696#issuecomment-5037634833)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5045689255)

## Activity Summary

### [Issue microsoft/TypeScript-go#2424](https://github.com/microsoft/TypeScript-go/issues/2424) (Closed, `possible improvement`)

**Request for support for additional architectures**

*Support and a roadmap are requested for riscv64, ppc64le, and loong64 architectures in typescript-go.*

 * (1 month ago) **jakebailey** closed the issue
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4748935526) **darkyzhou** said "Thanks!"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-4954972211) **dannycreations** asked about Android platform support for Termux after encountering a TypeScript resolution error
 * [later](https://github.com/microsoft/TypeScript-go/issues/2424#issuecomment-5047903008) **jakebailey** said "Interesting; I didn't realize that node / android would actually select something different than linux. We can probably do that."

### [PR microsoft/TypeScript-go#3663](https://github.com/microsoft/TypeScript-go/pull/3663) (Open)

**Fix hover JSDoc for mapped type properties**

*Fix JSDoc hover tooltips for mapped type properties to display accurate documentation.*

 * created by **Andarist**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.1`, and removed from milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4462](https://github.com/microsoft/TypeScript-go/issues/4462) (Closed, `bug`, **ahejlsberg**)

**Regression \(7\.0\.0\-dev\.20260624\.1\): intersection type member dropped in generic position — TanStack Router \`stripSearchParams\` rejected \(TS2322\), clean in tsc \+ 20260623\.1**

*Upgrading to @typescript/native-preview 7.0.0-dev.20260624.1 drops members from intersection types in generics, triggering TS2322 errors in TanStack Router.*

 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (1 week ago) **ahejlsberg** added label `bug`, and removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4560](https://github.com/microsoft/TypeScript-go/issues/4560) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**Extension does not follow symlinks when resolving the tsdk path \(breaks pnpm virtual store\)**

*TypeScript native-preview extension ignores pnpm tsdk symlinks, fails to locate platform binary, and falls back to the bundled version.*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4561](https://github.com/microsoft/TypeScript-go/pull/4561) (Closed, **jakebailey**, **Copilot**)

**Resolve native\-preview tsdk symlinks before locating platform package**

*Resolve file-based tsdk symlinks with realpath to correctly locate TypeScript platform packages in pnpm virtual stores.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4587](https://github.com/microsoft/TypeScript-go/issues/4587) (Open, `Needs More Info`, **weswigham**)

**TSX files do not report TypeScript diagnostics, while TS files work correctly \(autocomplete still works\)**

*Enabling tsgo in VS Code’s TypeScript 7 extension causes .tsx files to omit diagnostics while .ts files report errors normally.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**
 * (today) **weswigham** added label `Needs More Info`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4587#issuecomment-5037332201) **weswigham** explained that the behavior was working as intended and not new, and noted that the issue report lacked standalone reproduction details
 * [later](https://github.com/microsoft/TypeScript-go/issues/4587#issuecomment-5047689267) **elramus** provided reproduction steps showing that the TypeScript 7 language server did not report missing required props

### [PR microsoft/TypeScript-go#4591](https://github.com/microsoft/TypeScript-go/pull/4591) (Closed)

**Sort by type depth in \`inferFromMatchingTypes\` function**

*Sort matching types by nesting depth in the inferFromMatchingTypes function to resolve regressions such as #4462.*

 * **ahejlsberg** added to milestone `Post-7.0`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4938930752) **typescript-automation[bot]** provided the requested performance run results
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4591#issuecomment-4939528081) **typescript-automation[bot]** reported that running tsc on the top 1000 repos showed no issues comparing main and the pull request merge
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592) (Open)

**Improve responsiveness of \`tsc build\` to interruption**

*Enhance tsc build responsiveness to SIGINT and SIGTERM by threading cancellation contexts through compilation, exiting with proper codes, and adding tests.*

 * created by **lukesandberg**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-4939791695) **lukesandberg** said "@microsoft-github-policy-service agree [company="Vercel"]"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-4939873881) **lukesandberg** agreed that the company was Vercel
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5036518306) **jakebailey** questioned whether Ctrl+C was handled previously or was unhandled in the old compiler

### [Issue microsoft/TypeScript-go#4607](https://github.com/microsoft/TypeScript-go/issues/4607) (Closed, `Crash`, **RyanCavanaugh**, **Copilot**)

**TypeScript 7\.0 Can't compile \`webpack\`**

*TypeScript 7.0 compiler panics with unexpected JSTypeAliasDeclaration nodes while compiling webpack*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4996255239) **weswigham** said "From the just the stack frame, I'm guessing a @typedef merged with a module.exports.Something = whatever."
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4607#issuecomment-4997380107) **RyanCavanaugh** provided a reproduction example and reported a compiler panic
 * **RyanCavanaugh** assigned to **Copilot**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4617](https://github.com/microsoft/TypeScript-go/issues/4617) (Closed, `Type Ordering`, `Working As Intended`, **weswigham**)

**Behavior difference: TS4023 on declaration emit when a spread of a symbol\-branded object is unioned with the original \(pattern used by zod \`\.brand\(\)\`\)**

*Unioning a symbol-branded object with its spread causes tsgo to inline the brand symbol and error TS4023, unlike tsc.*

 * (6 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **weswigham**
 * (today) **weswigham** added labels `Working As Intended`, `Type Ordering`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4617#issuecomment-5038793562) **weswigham** explained that with --stableTypeOrdering the order-dependent subtype reduction picks a different structurally identical type and suggested annotating f or casting to enforce the desired type
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4618](https://github.com/microsoft/TypeScript-go/issues/4618) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Some imports are not updated after a file rename, in composite projects**

*TypeScript 7 composite projects do not update imports in unloaded subprojects when renaming files, unlike TypeScript 6.*

 * created by **pascalspadone**
 * **pascalspadone** added label `Domain: Editor`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4633](https://github.com/microsoft/TypeScript-go/issues/4633) (Open, `Needs Investigation`, **jakebailey**)

**Publish an official wasip1 \(WASI\) build artifact of tsgo**

*Publish an official Go WASI (wasip1) WebAssembly build artifact of tsgo alongside native binaries in releases.*

 * (6 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Possible Improvement`, and assigned to **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5047893676) **jakebailey** asked about the expectation for distributing a .wasm file on npm, noted that special-casing it is feasible as esbuild does, and suggested falling back to Node's WASI shim when no native binary exists despite observed crashes
 * [later](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5048059112) **calvinrp** proposed publishing a versioned .wasm package per release and adding CI-built artifacts, and suggested decoupling the Node WASI-shim fallback as a separate issue

### [Issue microsoft/TypeScript-go#4635](https://github.com/microsoft/TypeScript-go/issues/4635) (Closed, `bug`)

**Semantic tokens: defaultLibrary modifier never set on case\-insensitive filesystems \(macOS/Windows\)**

*TypeScript Native Preview extension on macOS/Windows case-insensitive filesystems omits defaultLibrary semantic token modifier for library globals causing incorrect theming*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4635#issuecomment-4971925016) **philiplindberg** clarified that the issue reproduced identically on the released typescript@7.0.2 GA with zero tokens in both preview and GA binaries
 * (6 days ago) **RyanCavanaugh** added label `bug`, and set milestone to `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4654](https://github.com/microsoft/TypeScript-go/pull/4654) (Closed)

**Use canonical paths for the semantic tokens defaultLibrary check**

*Adjust semantic tokens handler to use canonical file paths for default library detection on case-insensitive file systems.*

 * created by **KlyneChrysler**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4663](https://github.com/microsoft/TypeScript-go/pull/4663) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix crash: JSTypeAliasDeclaration passed to GetTypeOfDeclaration during CJS declaration emit**

*Restrict the declaration emit fallback to only inferrable declarations to avoid passing JSTypeAliasDeclaration to GetTypeOfDeclaration and prevent related crashes.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4663#issuecomment-5037837814) **Copilot** fixed hasTypeAnnotation to explicitly exclude TypeAliasDeclaration and JSTypeAliasDeclaration
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4671](https://github.com/microsoft/TypeScript-go/issues/4671) (Closed)

**Parity: noEmit project reference dry build remains stale like microsoft/TypeScript\#63656**

*Projects using noEmit remain perpetually out-of-date under tsgo's dry build, erroneously flagged for missing outputs.*

 * created by **schickling-assistant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4671#issuecomment-5036299794) **jakebailey** said "I don't see why we need two issues to track the same thing, no need for an issue here if this is not a regression in 7.0, just use the other issue"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4673](https://github.com/microsoft/TypeScript-go/issues/4673) (Closed, `bug`, **ahejlsberg**)

**False\-positive TS7022 on destructured array element used as a 2\-D index**

*In TypeScript 7.x, destructuring a 2-D array index after control-flow narrowing erroneously triggers a TS7022 implicit any error.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** added label `bug`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4673#issuecomment-5036452568) **ahejlsberg** said "This is caused by a difference in the ported code for isMatchingConstructorReference. It's an easy fix, I will put up a PR."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4677](https://github.com/microsoft/TypeScript-go/issues/4677) (Open, `Domain: Editor`)

**JSDoc \(TSDoc ???\) is not shown for object literal properties on hover**

*In TypeScript 7, VS Code stops displaying JSDoc comments on hover for const object literal properties, losing per-property documentation.*

 * created by **nazmul-nhb**
 * **nazmul-nhb** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4677#issuecomment-5042964606) **jinxiangqiang** said "Release it as soon as possible. Thank you."

### [Issue microsoft/TypeScript-go#4678](https://github.com/microsoft/TypeScript-go/issues/4678) (Open, `Working As Intended`, **RyanCavanaugh**, **Copilot**)

**skipLibCheck doesn't suppress TS2320 "cannot simultaneously extend" for module augmentation of a \`\.d\.ts\` interface \(repro has no any\)**

*skipLibCheck:true does not suppress TS2320 cannot simultaneously extend errors during module augmentation of a .d.ts interface.*

 * created by **valentinmelusson**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4678#issuecomment-5039612384) **RyanCavanaugh** referenced issue #3814 and noted TS7 now consistently reported errors to avoid nondeterminism in multi-threaded checker mode and said they would add a general category to CHANGES.md
 * (today) **RyanCavanaugh** added label `Working As Intended`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4680](https://github.com/microsoft/TypeScript-go/issues/4680) (Open, `Needs More Info`)

**TS7030 "not all code paths return a value" false positive when a never\-returning exhaustiveness helper is called \(not returned\) in a switch default**

*tsgo wrongly reports not all code paths return for a switch default that calls a never-returning exhaustiveness helper*

 * created by **valentinmelusson**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4680#issuecomment-5037782672) **RyanCavanaugh** said "I can't repro this at typescript 7.0.2. Can you confirm what version you're running here?"
 * (today) **RyanCavanaugh** added label `Needs More Info`, removed label `bug`, set milestone to `Need More Info`, removed from milestone `TypeScript 7.1`, and unassigned **RyanCavanaugh**, **Copilot**

### [Issue microsoft/TypeScript-go#4681](https://github.com/microsoft/TypeScript-go/issues/4681) (Open, `duplicate`)

**skipLibCheck doesn't suppress TS18042/TS2693 when a \.d\.ts's own export = points to a type instead of a value**

*skipLibCheck does not prevent tsgo from reporting TS18042 and TS2693 errors when a .d.ts file’s export= incorrectly refers to a type instead of a value.*

 * created by **valentinmelusson**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4681#issuecomment-5039618337) **RyanCavanaugh** said "Same answer as #4678"
 * **RyanCavanaugh** added label `duplicate`

### [Issue microsoft/TypeScript-go#4683](https://github.com/microsoft/TypeScript-go/issues/4683) (Closed, `duplicate`, **ahejlsberg**)

**Generic type parameter inferred differently across two call\-site positions with opposite variance \(narrow type vs union\)**

*TypeScript infers D from the columns as MetricWithCardinality rather than the union type when passing data to Table.*

 * created by **valentinmelusson**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4683#issuecomment-5034155386) **Andarist** said "bisects to #4389"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4683#issuecomment-5040208344) **ahejlsberg** said "This was fixed by #4591 which is now in main."
 * (today) **ahejlsberg** added label `duplicate`, and removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4684](https://github.com/microsoft/TypeScript-go/issues/4684) (Closed, `Domain: Editor`)

**VS Code extension does not provide completions for directive comments**

*VS Code extension does not support completions for TypeScript directive comments such as @ts-expect-error.*

 * **mrazauskas** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4684#issuecomment-5035668136) **jakebailey** said "Do I dare claim that not offering these is a feature? 😄 "
 * [today](https://github.com/microsoft/TypeScript-go/issues/4684#issuecomment-5036084028) **mrazauskas** questioned whether the difference was intentional and suggested closing the issue if so
 * [today](https://github.com/microsoft/TypeScript-go/issues/4684#issuecomment-5036338543) **jakebailey** said "No, we just don't have a clear list of everything the old extension does, and this is really just an oversight (like JSDoc completions last minute in #4505)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4684#issuecomment-5039649702) **RyanCavanaugh** said "Let's say it's intentional, at least for now. This doesn't seem critical and it'd be better to have fewer things to maintain."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4686](https://github.com/microsoft/TypeScript-go/issues/4686) (Closed, `Working As Intended`)

**TypeScript 7\.0\.2 does not infer function generic parameter, TypeScript 6 does**

*TypeScript 7.0.2 fails to infer a function's generic parameter that TypeScript 6 infers correctly.*

 * (yesterday) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Need More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5028116077) **daniele-orlando** said "@RyanCavanaugh I have updated the issue reproduction description to point to a StackBlitz repository. Does it work for you?"
 * (today) **RyanCavanaugh** removed label `Needs More Info`, and removed from milestone `Need More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5037180524) **RyanCavanaugh** said "I don't see an error on that first line when running locally, but I do see the error state of the second two change."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5037305000) **daniele-orlando** showed that the `patch` function was correctly inferred as Io<Partial<State>, undefined> in TypeScript 6 but incorrectly inferred as Io<Partial<object>, undefined> in TypeScript 7
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5037381775) **daniele-orlando** said "I commented the StackBlitz code and I simplified it a bit to make the issue clearer."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5037399383) **daniele-orlando** said "@RyanCavanaugh Please can you mark this issue as a bug? As this is a regression in TypeScript 7."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5037448363) **RyanCavanaugh** said "@daniele-orlando can you give me time to confirm it first please?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5039501621) **RyanCavanaugh** identified a TS6 bug in JSX runtime import handling that imported react/jsx-runtime unnecessarily without JSX files, noted TS7 avoided this which affected type resolution, and recommended TS7’s behavior
 * **RyanCavanaugh** added label `Working As Intended`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4686#issuecomment-5039879156) **daniele-orlando** thanked the maintainers for investigating, confirmed that skipLibCheck traced the error but did not explain the TS6 vs TS7 behavior, and acknowledged understanding how to handle it in future cases
 * (today) **daniele-orlando** closed the issue

### [PR microsoft/TypeScript-go#4687](https://github.com/microsoft/TypeScript-go/pull/4687) (Closed)

**Optimize construction of union types**

*Optimize union type construction by collecting, sorting, and deduplicating types, adding suggestion limits, and stabilizing symbol ID assignment.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4687#issuecomment-5026680373) **typescript-automation[bot]** started build jobs and posted status updates with result links
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4687#issuecomment-5027083261) **typescript-automation[bot]** provided the requested performance run results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4687#issuecomment-5027339179) **typescript-automation[bot]** reported successful tsc test results for the top 400 repos comparing main and the pull request merge
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4691](https://github.com/microsoft/TypeScript-go/pull/4691) (Closed)

**Fix over\-eager \`isMatchingConstructorReference\` function**

*Refine the isMatchingConstructorReference function to align its behavior with Strada’s original implementation.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4692](https://github.com/microsoft/TypeScript-go/issues/4692) (Closed, `bug`, **jakebailey**, **Copilot**)

**checkJs \+ jsxImportSource does not recognize JSX namespace**

*tsgo fails to recognize the Preact JSX namespace in .js files when using checkJs and jsxImportSource*

 * created by **caseywebdev**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4692#issuecomment-5036945564) **nathanielop** said "I am also seeing this behavior"
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.1`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4693](https://github.com/microsoft/TypeScript-go/pull/4693) (Open, **RyanCavanaugh**, **Copilot**)

**Add regression test for TS7030 false positive with never\-returning function in switch default**

*Add regression tests verifying that calls to never-returning functions in switch defaults don't trigger TS7030 errors*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4694](https://github.com/microsoft/TypeScript-go/pull/4694) (Closed, **jakebailey**, **Copilot**)

**Recognize jsxImportSource namespaces in checked JavaScript**

*Enable jsxImportSource to resolve JSX namespaces in checked JavaScript files by including them in runtime import synthesis.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4694#issuecomment-5037768879) **caseywebdev** said "Awesome, thanks 🙏🏻"

### [PR microsoft/TypeScript-go#4695](https://github.com/microsoft/TypeScript-go/pull/4695) (Open, **jakebailey**, **Copilot**)

**Update imports in unloaded composite projects after file rename**

*Load full composite project tree before renaming files to update imports in unopened projects.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4696](https://github.com/microsoft/TypeScript-go/pull/4696) (Open)

**Fix merged polymorphic this reference analysis**

*Improves merged polymorphic this reference analysis by selecting the correct declaration to prevent runaway type instantiation and adding regression tests.*

 * created by **MatthewHarrigan**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4696#issuecomment-5037634833) **microsoft-github-policy-service[bot]** asked the user to agree to the CLA by replying with the appropriate command

### [Issue microsoft/TypeScript-go#4697](https://github.com/microsoft/TypeScript-go/issues/4697) (Open, `Working As Intended`)

**Behavior difference: import \* as x of an export = callable loses call signatures without esModuleInterop \(TS2349\)**

*Without esModuleInterop, tsgo’s import * from an export= callable incorrectly drops the call signature, causing TS2349 errors.*

 * created by **greg-flux**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4697#issuecomment-5037651107) **jakebailey** observed that esModuleInterop being disabled was unsupported and inquired if it defaulted to true
 * **RyanCavanaugh** added label `Working As Intended`

### [PR microsoft/TypeScript-go#4698](https://github.com/microsoft/TypeScript-go/pull/4698) (Open, **RyanCavanaugh**, **Copilot**)

**Document and lock in TS7 skipLibCheck behavior for merged\-interface heritage conflicts**

*Document and enforce TS7 skipLibCheck behavior retaining TS2320 errors for merged-interface heritage conflicts involving user augmentations*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4699](https://github.com/microsoft/TypeScript-go/pull/4699) (Open)

**API emit**

*Add program.emit, program.emitToString, getJavaScriptEmit, and getDeclarationEmit methods for flexible file system and in-memory emissions.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#4700](https://github.com/microsoft/TypeScript-go/pull/4700) (Open)

**Expose getFullyQualifiedName on the API Checker**

*Expose getFullyQualifiedName on the unstable Checker API to support symbol identification for compiler-based tooling.*

 * created by **WinterYukky**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4700#issuecomment-5040980972) **WinterYukky** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript-go#4701](https://github.com/microsoft/TypeScript-go/pull/4701) (Open)

**\[api\] Add \`\.getNonMissingTypeOfSymbol\(\)\` getter**

*Add .getNonMissingTypeOfSymbol() API getter to retrieve a symbol’s non-missing type.*

 * created by **mrazauskas**

### [PR microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703) (Open)

**Store value symbol links inline on checker\-created symbols**

*Inline per-symbol side data for checker-created symbols to avoid costly map accesses and improve type-checker performance by up to 8%.*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5045300017) **jakebailey** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5045301019) **typescript-automation[bot]** reported that perf test jobs had started and provided links to build and result statuses
 * [later](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5045689255) **typescript-automation[bot]** provided perf run results to @jakebailey

### [Issue microsoft/TypeScript-go#4704](https://github.com/microsoft/TypeScript-go/issues/4704) (Open)

**\`new super\(\)\` in static method does not cause error**

*new super() in static methods or blocks is incorrectly allowed without error instead of being flagged as invalid*

 * created by **Withered-Flower-0422**

### [Issue microsoft/TypeScript-go#4705](https://github.com/microsoft/TypeScript-go/issues/4705) (Open)

**\`hasTrailingComma\` property is not implemented in \`RemoteNodeList\` class in the API**

*The RemoteNodeList class in the API declares a hasTrailingComma property that is never assigned or implemented.*

 * created by **mrazauskas**

