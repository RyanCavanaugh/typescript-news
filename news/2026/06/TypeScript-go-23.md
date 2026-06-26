# Report for 2026-06-23 (Tuesday, June 23rd, 2026)

15 different users commented on 67 different issues.

## Recommended Actions

 * Response Recommended
    * @Ijtihed asked for an explanation in [microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4782196616)
    * @Ijtihed provided requested information in [microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4785998449)
    * @crystalfp reported warning popup about Vue.volar plugins not loading in [microsoft/TypeScript-go#4388](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4786221145)

## Activity Summary

### [Issue microsoft/TypeScript-go#1493](https://github.com/microsoft/TypeScript-go/issues/1493) (Open, `Domain: CLI`, **jakebailey**, **Copilot**)

**Exit code for type error is incorrect starting from \`7\.0\.0\-dev\.20250724\.1\`**

*tsgo in @typescript/native-preview@7.0.0-dev.20250724.1 returns exit code 1 for type errors instead of the expected code 2.*

 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`

### [Issue microsoft/TypeScript-go#1789](https://github.com/microsoft/TypeScript-go/issues/1789) (Closed, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Inference fails form unions of arrays of different depths \(T\[\] \| T\[\]\[\]\)**

*A generic flat function fails to infer type T for T[]|T[][] arguments under tsgo, though TypeScript 5.8 succeeds.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1789#issuecomment-3378695181) **jakebailey** corrected his previous statement and showed the TypeScript lib.d.ts implementation of flat without a union
 * (12 weeks ago) **RyanCavanaugh** set milestone to `Possible Improvement`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4218](https://github.com/microsoft/TypeScript-go/pull/4218) (Open, `Voight-Kampff Anomaly`)

**Allow lone & in Unicode sets regexp classes**

*Update native scanner to allow lone & in Unicode Set regex character classes while preserving && intersections.*

 * created by **Ijtihed**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4782196616) **Ijtihed** expressed appreciation for the label and asked for an explanation
 * [today](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4782550377) **RyanCavanaugh** explained that the label is applied to high-PR contributors under the bulk contributors policy and asked why the user decided to fix that particular issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4218#issuecomment-4785998449) **Ijtihed** explained that they were a junior engineer who picked the issue to learn after browsing rather than from personal need

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Open, `No linked issue`)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770071961) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770072931) **typescript-automation[bot]** reported the start of performance tests and provided links to build status and results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4770330390) **typescript-automation[bot]** provided the requested TypeScript compiler performance run results in a detailed comparison report
 * [later](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4787742205) **mds-ant** said "Let's close out this PR given that it improves some benchmarks but slightly regresses others."
 * (later) **mds-ant** closed the issue
 * (later) **DanielRosenwasser** reopened the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4790862837) **DanielRosenwasser** said "We're actually not convinced it's a regression - the benchmarking infra has a lot of noise."

### [Issue microsoft/TypeScript-go#4249](https://github.com/microsoft/TypeScript-go/issues/4249) (Closed, `Domain: API and Extensibility`)

**\`\.getProgramDiagnostics\(\)\` is missing in the API**

*Add an API method like program.getProgramDiagnostics or project.getProjectDiagnostics to retrieve missing compiler options diagnostics.*

 * created by **mrazauskas**
 * (2 weeks ago) **RyanCavanaugh** added label `Domain: API and Extensibility`, and set milestone to `Post-7.0`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4267](https://github.com/microsoft/TypeScript-go/issues/4267) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Unknown file type\(?\) triggers fatal server crash**

*Loading a file with an unrecognized type intermittently triggers a fatal server crash during parsing.*

 * (1 week ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4269](https://github.com/microsoft/TypeScript-go/issues/4269) (Open, **DanielRosenwasser**, **Copilot**)

**Fatal error when project reference objects have unexpected types for \`path\` and \`circular\`**

*tsconfig parsing crashes when project references specify non-string values for path or circular properties.*

 * created by **DanielRosenwasser**
 * (1 week ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4292](https://github.com/microsoft/TypeScript-go/issues/4292) (Open, `Domain: Editor`)

**Can't enable TypeScript native preview in VS Code**

*VS Code fails to activate the experimental TypeScript Native Preview and continues using the previous TypeScript version.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4292#issuecomment-4694044207) **DanielRosenwasser** said "Weirdly I have hit something similar but I'm no longer able to repro it."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4292#issuecomment-4694635964) **denexapp** said "@DanielRosenwasser if there are ways to see* debug logs, I can do that and attach them here"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4292#issuecomment-4748649207) **geelove** said "This doesn't work for me either, switching the ts server versions to the experimental native preview does nothing and it still runs VS code's version (6.0.3)"
 * **RyanCavanaugh** added to milestone `Need More Info`

### [Issue microsoft/TypeScript-go#4293](https://github.com/microsoft/TypeScript-go/issues/4293) (Closed)

**Behavior difference: Expando function emit between tsc & tsgo**

*Expando functions emit differently between TypeScript’s tsc and tsgo, with tsgo omitting certain post-bind attributes.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4293#issuecomment-4781773085) **weswigham** explained that main now emits Internal's expando field and described bound reexports behavior and strict mode errors in the test
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4295](https://github.com/microsoft/TypeScript-go/issues/4295) (Open, `possible improvement`)

**Behavior difference: \(jsdoc\) comment emit inconsistencies on expando functions**

*JSDoc comments on expando arrow functions are inconsistently preserved by tsgo compared to tsc when compiling JavaScript sources.*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4304](https://github.com/microsoft/TypeScript-go/issues/4304) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript's main pipeline analyzed 300 repositories and encountered seven changes, five clone failures, 76 timeouts, and 18 unknown failures.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4304#issuecomment-4696884423) **typescript-automation[bot]** reported a server connection closed prematurely with undefined while processing t4t5/sweetalert
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4304#issuecomment-4696884454) **typescript-automation[bot]** reported that the server connection closed prematurely and provided repro steps for pixijs/pixijs
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4304#issuecomment-4696884486) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error and provided logs, requests, and repro steps
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4308](https://github.com/microsoft/TypeScript-go/pull/4308) (Closed)

**API: add the missing position and text getters to Node**

*Add missing position and text getters to the API Node implementation and include tests for them.*

 * created by **oMatheusmol**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4310](https://github.com/microsoft/TypeScript-go/issues/4310) (Closed, **jakebailey**, **Copilot**)

**Behavior difference: \(Another\) Expando function emit between tsc & tsgo**

*tsgo omits generating propTypes for function component aliases while tsc emits them*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4310#issuecomment-4745590237) **weswigham** said "Is this by chance fixed by #4356?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4310#issuecomment-4745602654) **hkleungai** said "I guess we can wait for the next nightly release then. 😄 "
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4310#issuecomment-4750101327) **hkleungai** said "Issue remains in 7.0.0-dev.20260619.1, in both .js & .tsx extensions 😓 "
 * [today](https://github.com/microsoft/TypeScript-go/issues/4310#issuecomment-4783369154) **weswigham** confirmed that on main branch, the emit included the propTypes member on FunctionComponent and its alias
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4311](https://github.com/microsoft/TypeScript-go/pull/4311) (Closed, **jakebailey**, **Copilot**)

**Fix declaration emit for expando function aliases**

*Modify declaration generation so exported expando function aliases are emitted as function declarations with namespaces to expose merged properties.*

 * **Copilot** assigned to **jakebailey**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4311#issuecomment-4744669358) **jakebailey** said "@copilot+gpt-5.5 Merge main and update tests"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4311#issuecomment-4744899347) **Copilot** merged main, updated tests, and reported successful validation
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4314](https://github.com/microsoft/TypeScript-go/issues/4314) (Closed, `Type Ordering`)

**Behavior difference: tsgo misses TS2345 when a namespace translator union is called with a template\-literal key union**

*tsgo incorrectly accepts a union of template-literal translation keys across namespaces without raising TS2345, whereas tsc errors.*

 * created by **chitwitgit**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4314#issuecomment-4705432420) **DanielRosenwasser** suggested that the issue was due to union ordering and shared a self-contained playground link
 * **RyanCavanaugh** added label `Type Ordering`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4314#issuecomment-4784793929) **RyanCavanaugh** said "I agree, this is type ordering issue unless it can be more clearly demonstrated otherwise."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4317](https://github.com/microsoft/TypeScript-go/issues/4317) (Closed, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Behavior difference: tsgo inconsistently emits overloaded signature**

*tsgo inconsistently emits overloaded signatures for certain class field and variable functions using interface-based overloads*

 * (5 days ago) **weswigham** added labels `bug`, `Domain: Declaration Emit`, and removed label `Needs Investigation`
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4332](https://github.com/microsoft/TypeScript-go/issues/4332) (Open, `possible improvement`, **jakebailey**, **Copilot**)

**Behavior difference: Type emit inconsistency with dangling block comment in file**

*Dangling block comments in top-level files are incorrectly attached to variables by tsgo while tsc erases them*

 * (1 week ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * **RyanCavanaugh** added label `possible improvement`

### [PR microsoft/TypeScript-go#4333](https://github.com/microsoft/TypeScript-go/pull/4333) (Closed)

**feat\(ast\): implement GetLineStarts and GetLineAndCharacterOfPosition \(\#4215\)**

*Implement GetLineStarts and GetLineAndCharacterOfPosition on Go AST’s SourceFile with unit tests.*

 * created by **ntoulasm**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4333#issuecomment-4718570077) **ntoulasm** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4333#issuecomment-4783420849) **jakebailey** said "the issue was filed about the JS API, not the Go API, which already has this"
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4333#issuecomment-4786542946) **ntoulasm** said "Ah, got it! Thank you for the clarification.. I completely missed that the issue was specifically about the JS API."

### [Issue microsoft/TypeScript-go#4335](https://github.com/microsoft/TypeScript-go/issues/4335) (Closed, `Needs Investigation`, **andrewbranch**, **Copilot**)

**checker\.getBaseTypes panics for type alias to generic interface instantiation**

*checker.getBaseTypes panics with a nil pointer dereference when processing a type alias to a generic interface instantiation*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4335#issuecomment-4752576072) **ahejlsberg** explained that getBaseTypes was being called on a type reference and suggested calling getTarget first
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4335#issuecomment-4770603293) **andrewbranch** asked whether the type flags disagreed with the underlying data after encountering a panic in c.getBaseTypes
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4335#issuecomment-4776387189) **ahejlsberg** clarified that the getBaseTypes function should test for ObjectFlagsClassOrInterface|ObjectFlagsTuple to return nil on plain type references and explained why the existing code still works
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4337](https://github.com/microsoft/TypeScript-go/pull/4337) (Closed)

**API: add checker methods to get true and false types of a conditional type**

*Add API checker methods for obtaining the true and false branch types of a conditional type.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4726236305) **mrazauskas** asked to link to issue #2851 and suggested adding getTrueType() and getFalseType() to ConditionalType
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4731859787) **piotrtomiak** asked what “link” referred to and said they would implement the change after PR 4341 merged due to needing a Type–projectId association
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4738685584) **mrazauskas** responded that they originally thought the PR could close issue #2851 but then noted they seem different domains and that the PR’s motivation is missing
 * (later) **piotrtomiak** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4790918979) **piotrtomiak** said "Sorry, accidentally closed - followed up in #4431"

### [Issue microsoft/TypeScript-go#4338](https://github.com/microsoft/TypeScript-go/issues/4338) (Open, `bug`, `Domain: API and Extensibility`)

**checker\.getTypeArguments panics for non\-reference types**

*Calling checker.getTypeArguments on non-reference types such as string triggers a nil pointer panic.*

 * created by **tomquist**
 * (today) **RyanCavanaugh** added labels `Domain: API and Extensibility`, `bug`, and set milestone to `Post-7.0`

### [PR microsoft/TypeScript-go#4341](https://github.com/microsoft/TypeScript-go/pull/4341) (Closed)

**API: make object registries project\-specific to avoid id collisions on types and signatures**

*Make object registries project-specific to prevent ID collisions on types and signatures and facilitate checker method refactoring.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4776701704) **piotrtomiak** suggested improving symbol caching by moving the data cache to the Snapshot level and proposed relocating Checker methods to the Symbol interface for a more intuitive API
 * [today](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4780656375) **andrewbranch** said "I'm not sure that's a goal, since those Checker methods are identical to Strada. Either way, having Symbol reference equality (within a snapshot but across projects) is a hard requirement."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4780993512) **piotrtomiak** said "Ok, got it. I'll move symbols down to the snapshot level then, keeping types and signatures at project level. OK?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4781131778) **andrewbranch** said "Yeah, I think that makes sense!"
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4781763993) **andrewbranch** suggested converting checker.getTrueTypeOfConditionalType and checker.getFalseTypeOfConditionalType into Type methods and noted that formatting was failing
 * [today](https://github.com/microsoft/TypeScript-go/pull/4341#issuecomment-4782095295) **piotrtomiak** removed dependency on #4337 and cleaned up formatting and indicated plans to update the PR for true/false conditional types
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4342](https://github.com/microsoft/TypeScript-go/issues/4342) (Closed, `Needs Investigation`)

**Behavior difference: \(Another\) Type emit issue on non\-const object keys referencing**

*tsgo emits a generic string index signature for constMap instead of preserving literal key types when importing non-const object keys*

 * created by **hkleungai**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4342#issuecomment-4781957000) **weswigham** noted that it wasn’t a functional behavior difference, justified refusing to emit computed names in this destructuring case, and said they would investigate why Strada emitted the computed names
 * **weswigham** added label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4342#issuecomment-4782035354) **weswigham** explained that strada incorrectly emitted computed property names for constMap, provided a TypeScript code example, and noted it was fixed during the corsa ID rework
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4345](https://github.com/microsoft/TypeScript-go/pull/4345) (Closed, **andrewbranch**, **Copilot**)

**Fix getBaseTypes panic on type reference instantiations**

*Change getBaseTypes guard flags to exclude plain type references and prevent nil pointer panics on generic instantiations.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4725013121) **Copilot** acknowledged overstatement and corrected the wording, explained the behavioral equivalence and redirect mechanism compared to Strada, and noted the fix in commit 1e9b
 * [today](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4780674562) **andrewbranch** said "@copilot this is wrong. Check the latest conversation in https://github.com/microsoft/typescript-go/issues/4335 and update accordingly."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4780728949) **Copilot** updated the guard to use ObjectFlagsClassOrInterface|ObjectFlagsTuple, removed the ref.target redirect, and reverted commit bb5ad67 per Anders' guidance
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4352](https://github.com/microsoft/TypeScript-go/issues/4352) (Open, `possible improvement`)

**Behavior difference: Block comments on \`@typedef\` structural types are not preserved, if they are imported and reconstructed as inline types in another file**

*tsgo fails to preserve block comments on @typedef structural types when they are imported and reconstructed as inline types*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4744716271) **hkleungai** said "But why not? If the transpiler is reconstructing an existing type in-place, shouldn't the original block comment be brought over to the new types as well? 😕 "
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4745039645) **jakebailey** said "We don't do that for TS, no?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4745160967) **hkleungai** described expectation that jsdoc-defined types produce valid emits and propagate attribute comments in IDEs as they do in TS 6
 * [today](https://github.com/microsoft/TypeScript-go/issues/4352#issuecomment-4783320543) **weswigham** explained that the old .d.ts emitter used setSyntheticLeadingComments to preserve comments, noted that the current corsa node builder predates this support causing missing comments on reparsed typedefs, and suggested reimplementing preserveCommentsOn inside addPropertyToElementList
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4358](https://github.com/microsoft/TypeScript-go/issues/4358) (Open, `bug`, **jakebailey**, **Copilot**)

**SourceFile\.ContainsNonASCII can be false for non\-ASCII in string literal fast path**

*Non-ASCII characters inside simple string literals bypass detection in SourceFile.ContainsNonASCII, resulting in incorrect UTF-16 position mapping.*

 * created by **CPunisher**
 * (6 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#4360](https://github.com/microsoft/TypeScript-go/pull/4360) (Closed, **jakebailey**, **Copilot**)

**Fix non\-ASCII detection for source file position maps**

*Enhance non-ASCII detection and position mapping to compute correct UTF-16 offsets with a shared helper and regression tests.*

 * created by **Copilot**
 * (6 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4361](https://github.com/microsoft/TypeScript-go/issues/4361) (Closed, **jakebailey**, **Copilot**)

**${configDir} path candidate resolving is incorrect when extending base config**

*Extending a base tsconfig in TypeScript 7 causes `${configDir}` paths to resolve to the project root instead of the current package.*

 * created by **Matthieu7503**
 * (5 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 Stable`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4361#issuecomment-4789370040) **Matthieu7503** said "Fixed in #4362 "
 * (later) **Matthieu7503** closed the issue

### [PR microsoft/TypeScript-go#4362](https://github.com/microsoft/TypeScript-go/pull/4362) (Closed, **jakebailey**, **Copilot**)

**Fix ${configDir} path candidate resolving in extended config**

*Ensure ${configDir} is correctly resolved for path mappings inherited from extended configurations*

 * **Copilot** assigned to **jakebailey**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4362#issuecomment-4743158672) **jakebailey** said "@copilot+gpt-5.5 you left this as WIP; are you done?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4362#issuecomment-4743297883) **Copilot** confirmed completion and provided final validation steps and commit hash
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4363](https://github.com/microsoft/TypeScript-go/issues/4363) (Open, **jakebailey**, **Copilot**)

**Behavior difference: Comment above \`@typedef\` does not become comment for the corresponding emitted type in tsgo**

*tsgo fails to preserve JSDoc comments above @typedef by emitting them after the generated type declaration*

 * created by **hkleungai**
 * (5 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4367](https://github.com/microsoft/TypeScript-go/pull/4367) (Closed)

**Allow parameter type reuse even when return type is inferred**

*Allow reusing parameter types when return types are inferred by adding void return type inference for functions with no return statements.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4746204661) **weswigham** explained that they discard pseudotype-inferred results mismatches in normal builds making the issue harmless and noted that in single-file emit incorrect types can still be emitted, affecting all return type inferences
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4746270494) **jakebailey** said "But by construction, we don't ever even try to produce things if we know we cannot, by the rules we defined for ID early on. I don't think this is one of them, right?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4367#issuecomment-4746611248) **weswigham** described a potential improvement by adding a restriction to bail on syntactic inference when function calls occur outside return expressions, noted exceptions for getters, setters, and proxies, and explained how exit() propagation differs between function returns and const contexts
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4375](https://github.com/microsoft/TypeScript-go/issues/4375) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**Add native\-preview API for capturing \.d\.ts emit output**

*Request for extending the TypeScript native-preview JS API to emit and capture .d.ts declaration output via virtual filesystem callbacks.*

 * created by **hegrec**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4375#issuecomment-4753149490) **jakebailey** said "Related is #3616"
 * (today) **RyanCavanaugh** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4378](https://github.com/microsoft/TypeScript-go/issues/4378) (Open, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-watch\` error: "error starting FSEvents stream" on large \`node\_modules\` since the fswatch rewrite**

*tsgo watch mode fails to initiate its file watcher on large node_modules directories after the fswatch rewrite in recent 7.0.0-dev builds*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4755249604) **Alex-Bond** confirmed that they meant full workspace diagnostics, noted the LSP diagnosticProvider settings from issue 2169 and that full workspace diagnostics is planned but not in the first release, and confirmed that PR #4379 enabled watch mode and resolved the issue
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4755392077) **jakebailey** asked if the current PR state had been tried and invited filing an issue if needed
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4755443201) **Alex-Bond** confirmed compiling and running with commit ce359c1
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4388](https://github.com/microsoft/TypeScript-go/issues/4388) (Open, `bug`)

**Parameters not automatically filled for JSdoc comments**

*JSDoc comment skeletons generated by tsgo omit @param tags, unlike the default TypeScript 6.0 behavior.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4765261220) **jakebailey** said "You haven't turned off the main TS extension, right? That's what should be doing this still."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4765277247) **crystalfp** installed the Typescript native preview extension and enabled it with the 'Enable (experimental)' command then observed that disabling it reverted to v6 behavior
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4776578634) **crystalfp** said "Nothing change disabling all the other extensions."
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4388#issuecomment-4786221145) **crystalfp** reported that VS Code displayed a warning stating Vue.volar plugins would not load because TypeScript Native Preview was enabled globally and suggested this might explain the behavior change

### [PR microsoft/TypeScript-go#4389](https://github.com/microsoft/TypeScript-go/pull/4389) (Closed)

**Prefer covariant inferences with deeper type argument nesting**

*Prioritize covariant type inferences originating from more deeply nested type arguments to improve inference quality.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770150195) **typescript-automation[bot]** reported CI test top400 job started and linked to build status and results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4770703379) **typescript-automation[bot]** reported successful tsc runs on top 400 repos comparing main and the PR merge
 * **ahejlsberg** added to milestone `TypeScript 7.0 Stable`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4781531734) **DanielRosenwasser** said "@typescript-bot test top1000"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4781532378) **typescript-automation[bot]** reported that test jobs had started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4389#issuecomment-4781982162) **typescript-automation[bot]** posted test results from running top 400 repos with tsc comparing main and the PR merge and reported that everything looked good
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4391](https://github.com/microsoft/TypeScript-go/issues/4391) (Open, `Needs Investigation`, **ahejlsberg**)

**const type parameter doesn't capture string\-literal property when the parameter type is wrapped in Omit\<\.\.\.\>**

*A const type parameter on interface call signatures loses string-literal property inference when the parameter type uses Omit<…>.*

 * created by **IanVS**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4391#issuecomment-4769860340) **jakebailey** said "Bisects to #4242. @ahejlsberg"
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 Stable`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#4393](https://github.com/microsoft/TypeScript-go/issues/4393) (Closed, `question`)

**typescript@7\.0\.1\-rc: programmatic AST codegen with \`import ts from "typescript"\` fails**

*Missing root export in typescript@7.0.1-rc package prevents importing ts from "typescript", breaking standard programmatic AST code generation.*

 * created by **wizardnet972**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4393#issuecomment-4770115664) **jakebailey** said "The API is unstable; we didn't describe it on purpose. We weren't even sure if we wanted to include it in the package so early. It's not for wider use!"
 * **RyanCavanaugh** added label `question`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4393#issuecomment-4785173822) **RyanCavanaugh** mentioned the TypeScript 7.0 RC announcement detailing side-by-side usage with TypeScript 6.0 and the @typescript/typescript6 compatibility package
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4396](https://github.com/microsoft/TypeScript-go/pull/4396) (Open, **jakebailey**, **Copilot**)

**Emit JS \`this\` properties in declarations matching tsc's serializePropertySymbol**

*Align JS declaration emit with tsc by skipping redundant this-assigned properties inherited from base classes and add regression tests.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4396#issuecomment-4783404345) **weswigham** said "@copilot you need to fix the TODO at the bottom of GetBaseDeclarationsForPropertyDeclaration for this to be more right - base props from implements clauses matter."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4396#issuecomment-4783548086) **Copilot** corrected GetBaseDeclarationsForPropertyDeclaration to collect declarations from all base types and implements clauses, added a test case, and referenced the fixing commit
 * [today](https://github.com/microsoft/TypeScript-go/pull/4396#issuecomment-4783588663) **weswigham** said "@copilot actually, go back and just remove the TODO - classes need to redeclare interface-inherited members anyway."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4396#issuecomment-4783874544) **Copilot** removed the TODO and changed skip logic to only consult extends base types, ensuring implements-clause members are always emitted

### [PR microsoft/TypeScript-go#4399](https://github.com/microsoft/TypeScript-go/pull/4399) (Open)

**Watcher performance improvements**

*Implement single-file program reuse, skip redundant operations, and track rebuild requirements with watchSetDirty to improve watcher performance.*

 * created by **johnfav03**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4399#issuecomment-4773796433) **jakebailey** said "Do you have any data about how this affects things?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4399#issuecomment-4780787469) **johnfav03** provided benchmark results showing single-file edits had a 50% rebuild time decrease and higher-volume edits saw about 10% improvement
 * [today](https://github.com/microsoft/TypeScript-go/pull/4399#issuecomment-4783318074) **jakebailey** provided two focused tests that reproduced correctness regressions in the watcher fast path

### [PR microsoft/TypeScript-go#4402](https://github.com/microsoft/TypeScript-go/pull/4402) (Closed)

**\[api\] Flesh out project/file open state management**

*Enhance the API client's updateSnapshot to support opening and closing files and projects, enabling inferred projects and tsconfig auto-discovery.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4402#issuecomment-4783071575) **andrewbranch** noted that the API previously supported opening additional projects, suggested deferring filtering decisions until LSP plugins gain usage, pointed out the new ability for API clients to add files to inferred projects, and argued that sharing inferred projects is preferable to duplicating them
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4406](https://github.com/microsoft/TypeScript-go/issues/4406) (Closed)

**Independent cross\-platform benchmark of TypeScript 7\.0\.1 RC vs TypeScript 6\.0\.3**

*Reproducible cross-platform benchmark shows TypeScript 7.0.1 RC outperforms 6.0.3 by 4.6–6.5× across diverse build scenarios with identical outputs.*

 * created by **safal207**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4406#issuecomment-4781618863) **RyanCavanaugh** said "You also might try passing a larger value to --checkers depending on project shape"

### [PR microsoft/TypeScript-go#4407](https://github.com/microsoft/TypeScript-go/pull/4407) (Open, **jakebailey**, **Copilot**)

**Restore tsgo noEmit exit status semantics**

*Restore tsgo’s noEmit exit status semantics by porting tsc’s handleNoEmitOptions logic to ensure exit code 2 for type errors*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-4781670224) **jakebailey** criticized the implementation as random and hacky and said the test case was not valid
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-4782003646) **Copilot** identified the root cause as the EmitSkipped value, ported handleNoEmitOptions into Program.Emit, reverted the cmd/tsgo hack and its test, and added a tsc command-line test

### [Issue microsoft/TypeScript-go#4411](https://github.com/microsoft/TypeScript-go/issues/4411) (Open, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**\`isolatedDeclarations\` quick\-fix cannot consistently use auto\-imports**

*IsolatedDeclarations quick-fix fails to auto-import missing types when no existing import is present*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4412](https://github.com/microsoft/TypeScript-go/pull/4412) (Closed, **DanielRosenwasser**, **Copilot**)

**\[WIP\] Add fourslash test for isolated declarations quick\-fix**

*Add a fourslash test and minimal implementation to auto-import type annotations for isolated declarations.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#4413](https://github.com/microsoft/TypeScript-go/pull/4413) (Closed)

**\[api\] Add missing program diagnostic getters**

*Add missing diagnostic getter methods to the program API.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4414](https://github.com/microsoft/TypeScript-go/pull/4414) (Closed)

**API: cache SourceFile text to heavily improve performance**

*Add a cache for SourceFile text in getTokenPosOfNode to eliminate redundant retrievals and enhance performance.*

 * created by **piotrtomiak**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4414#issuecomment-4783094591) **andrewbranch** said "This is a good optimization—could you put the cache on RemoteSourceFile instead of RemoteNode and override get text() there?"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4415](https://github.com/microsoft/TypeScript-go/pull/4415) (Closed)

**Fix/configdir extended config cache**

*Clone Paths map before substituting ${configDir} to prevent shared config cache mutations causing wrong path resolutions.*

 * created by **UditDewan**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4415#issuecomment-4782635807) **UditDewan** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4415#issuecomment-4782639910) **jakebailey** said "This is the same as https://github.com/microsoft/typescript-go/pull/4362"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4416](https://github.com/microsoft/TypeScript-go/pull/4416) (Open)

**Fix panic in checker\.GetTypeArguments for non\-reference types \(\#4338\)**

*Guard exported Checker.GetTypeArguments to return an empty slice for non-reference types instead of panicking.*

 * created by **UditDewan**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4417](https://github.com/microsoft/TypeScript-go/issues/4417) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**\-\-listEmittedFiles whitespace difference**

*tsgo's --listEmittedFiles output inserts two spaces after 'TSFILE:' instead of the single space used by tsc, causing inconsistency.*

 * created by **yoursunny**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4417#issuecomment-4783635846) **RyanCavanaugh** said "Fixed in https://github.com/microsoft/typescript-go/pull/4419"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4418](https://github.com/microsoft/TypeScript-go/pull/4418) (Open)

**Infer void for statement\-less function bodies in \`isolatedDeclarations\` syntactic inference**

*Syntactically infer void return types for statement-less functions to avoid isolatedDeclarations errors.*

 * created by **weswigham**
 * **weswigham** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4419](https://github.com/microsoft/TypeScript-go/pull/4419) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix extra space in \`\-\-listEmittedFiles\` TSFILE output**

*Correct the tsgo --listEmittedFiles TSFILE output by removing an unintended extra space.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4420](https://github.com/microsoft/TypeScript-go/pull/4420) (Open)

**\[api\] Add SourceFile line mapping methods**

*Add line mapping methods to the SourceFile API to map between source and generated code lines.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#4421](https://github.com/microsoft/TypeScript-go/pull/4421) (Closed)

**Add \`arguments\` inference removal to CHANGES\.md**

*Document removal of arguments type inference in CHANGES.md.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4422](https://github.com/microsoft/TypeScript-go/pull/4422) (Open)

**Use auto\-imports for \`isolatedDeclarations\` fixes**

*Add auto-imports to address missing imports in codebases with TypeScript’s isolatedDeclarations enabled.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4423](https://github.com/microsoft/TypeScript-go/pull/4423) (Closed)

**Fix macOS lspwatcher missing directory recovery**

*Add a macOS lspwatcher missing directory recovery workaround and verify its compatibility on Windows*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4424](https://github.com/microsoft/TypeScript-go/pull/4424) (Closed)

**\[api\] Add missing checker methods**

*Adds missing checker methods by porting JSDoc tag retrieval from Strada to return text as strings.*

 * created by **andrewbranch**

### [Issue microsoft/TypeScript-go#4425](https://github.com/microsoft/TypeScript-go/issues/4425) (Closed, `Crash`)

**Panic \(nil deref\) in checker\.GetBaseTypes for plain type references \(e\.g\. \`string\[\]\`\) via the API**

*Calling GetBaseTypes on a plain type reference like string[] via the API causes a nil pointer panic due to a missing InterfaceType check*

 * created by **UditDewan**
 * **UditDewan** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4425#issuecomment-4785793455) **jakebailey** said "Is this #4335?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4425#issuecomment-4785817337) **UditDewan** apologized for not checking for duplicate issues and promised to verify before coding late at night
 * (today) **UditDewan** closed the issue

### [Issue microsoft/TypeScript-go#4426](https://github.com/microsoft/TypeScript-go/issues/4426) (Open, `Crash`, **andrewbranch**)

**Panic \(Unhandled case in Type\.Types\) in checker\.Type\.Types for non\-union types \(e\.g\. string\) via the API getTypes\(\)**

*Calling getTypes() on non-union types like string through the API causes an unhandled case panic in Type.Types due to missing guard.*

 * created by **UditDewan**
 * **UditDewan** added label `Crash`

### [PR microsoft/TypeScript-go#4427](https://github.com/microsoft/TypeScript-go/pull/4427) (Open)

**Fix panic in checker\.Type\.Types for non\-union types via the API \(\#4426\)**

*Implement a guard in the API so Type.getTypes() returns an empty array for non-union types instead of panicking.*

 * created by **UditDewan**

### [Issue microsoft/TypeScript-go#4428](https://github.com/microsoft/TypeScript-go/issues/4428) (Open, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**\`js/ts\.reportStyleChecksAsWarnings\` is not respected**

*TypeScript 7.0 in VS Code ignores js/ts.reportStyleChecksAsWarnings and always marks unused variables as warnings.*

 * created by **DanielRosenwasser**
 * (later) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4429](https://github.com/microsoft/TypeScript-go/pull/4429) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix \`js/ts\.reportStyleChecksAsWarnings\` not being read from VS Code config**

*Add missing config annotation and tests so VS Code js/ts.reportStyleChecksAsWarnings setting is correctly parsed*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4430](https://github.com/microsoft/TypeScript-go/pull/4430) (Open)

**Match Strada's behavior to allow satisfying recursive indexed access**

*Align Corsa’s base-constraint caching with Strada’s two-tier model to restore correct recursive indexed-access constraint resolution.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4431](https://github.com/microsoft/TypeScript-go/pull/4431) (Closed)

**API: add checker methods to get true and false types of a conditional type**

*Add API checker methods to fetch true and false branches of a conditional type.*

 * created by **piotrtomiak**

