# Report for 2026-06-06 (Saturday, June 6th, 2026)

10 different users commented on 18 different issues.

## Recommended Actions

 * Response Recommended
    * @apostate0 asked why duplicate directives are used and reported a semantic regression in module augmentation in [microsoft/TypeScript-go#3481](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4642469732)
    * @rubenferreira97 provided regression tests for dependency invalidation and watch path casing for maintainers to validate in [microsoft/TypeScript-go#3670](https://github.com/microsoft/TypeScript-go/pull/3670#issuecomment-4642936422)
    * @mds-ant asked if there's precedent for enabling optimizations only for batch compilations in [microsoft/TypeScript-go#4226](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4640495531)

## Activity Summary

### [Issue microsoft/TypeScript-go#3481](https://github.com/microsoft/TypeScript-go/issues/3481) (Open, `help wanted`)

**Corsa differences in \`export=\` module augmentation**

*Corsa changes how export= module augmentation works, causing differences in exported name visibility.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4291838613) **ahejlsberg** said "The issue in augmentExportEquals2.errors.txt.diff is actually that the test is broken. There are two // @filename: file3.ts in a row, which we apparently no longer handle."
 * (1 month ago) **RyanCavanaugh** added label `help wanted`, and set milestone to `Post-7.0`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3481#issuecomment-4642469732) **apostate0** described that augmentExportEquals2.errors.txt.diff wasn't a real bug but caused by duplicate filename directives and asked why they're used; identified a real semantic regression in exportAssignmentMembersVisibleInAugmentation.errors.txt.diff due to module augmentation symbol lookup and suggested a root cause in checker.go

### [PR microsoft/TypeScript-go#3670](https://github.com/microsoft/TypeScript-go/pull/3670) (Open, **johnfav03**)

**Watcher build mode efficiency updates**

*Refactors tsc --build --watch to use a shared FileWatcher and trackingVFS structure, reducing code duplication and redundant dependency scanning.*

 * created by **johnfav03**
 * (1 month ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **johnfav03**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3670#issuecomment-4642936422) **rubenferreira97** shared a test-only branch with two regression tests and described failures in dependency invalidation and path casing when building and watching

### [Issue microsoft/TypeScript-go#4219](https://github.com/microsoft/TypeScript-go/issues/4219) (Closed, `bug`, **ahejlsberg**)

**JSDoc \`@private\`/\`@protected\` on a constructor is ignored**

*tsgo ignores JSDoc @private/@protected on constructors, permitting instantiation that TypeScript correctly errors on.*

 * (today) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4223](https://github.com/microsoft/TypeScript-go/issues/4223) (Closed, `bug`, **ahejlsberg**)

**Spelling suggestions \('Did you mean'\) diverge for non\-ASCII identifiers**

*tsgo’s spelling suggestion for the non-ASCII identifier Aé diverges by recommending class Aé instead of class.*

 * (today) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4224](https://github.com/microsoft/TypeScript-go/issues/4224) (Closed, `bug`, **ahejlsberg**)

**Late\-bound \(computed\-name\) member incompatibility reported as class\-level TS2415**

*tsgo misreports late-bound computed-name property incompatibility as a class-level TS2415 error instead of the more specific TS2416 property error*

 * created by **mds-ant**
 * (today) **ahejlsberg** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4225](https://github.com/microsoft/TypeScript-go/issues/4225) (Closed, `possible improvement`, **jakebailey**, **Copilot**)

**'Expected N type arguments' position does not skip trivia after '\<'**

*tsgo incorrectly reports error positions by not skipping whitespace after '<' when determining type argument counts.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4226](https://github.com/microsoft/TypeScript-go/pull/4226) (Open, `No linked issue`)

**Convert \`valueSymbolLinks\` and \`symbolNodeLinks\` to id\-paged arrays**

*Replace valueSymbolLinks and symbolNodeLinks map stores with ID-paged arrays to reduce hash lookup costs and improve typechecking performance*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4639120627) **mds-ant** said "@microsoft-github-policy-service agree company="Anthropic""
 * [today](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4639582618) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4639582927) **typescript-automation[bot]** reported that the perf test job started and provided links to the build status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4639658148) **typescript-automation[bot]** posted performance run results including a comparison report of baseline versus pr metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4639982017) **ahejlsberg** highlighted performance gains and memory trade-offs of using dense node and symbol IDs, noting potential costs for less common links and increasing memory usage over long sessions
 * [today](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4640495531) **mds-ant** tried converting a handful more stores to the page array scheme but observed increased memory usage, suggested converting only valueSymbolLinks and symbolNodeLinks for performance gains, asked if there was precedent for enabling optimizations only for batch compilations and retaining the existing link store for the language server use case
 * [today](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4640630251) **jakebailey** suggested that it'd require a runtime switch but could be noted on Program or Checker creation, though found it weird

### [PR microsoft/TypeScript-go#4227](https://github.com/microsoft/TypeScript-go/pull/4227) (Closed)

**fix jsdoc accessibility modifiers on constructors**

*Correct the JSDoc accessibility modifiers on class constructors to reflect intended access levels.*

 * created by **a-tarasyuk**
 * (today) **a-tarasyuk** closed the issue

### [PR microsoft/TypeScript-go#4228](https://github.com/microsoft/TypeScript-go/pull/4228) (Closed)

**fix exact optional argument diagnostic**

*Refines the TypeScript diagnostic for non-assignable arguments when exactOptionalPropertyTypes is enabled to recommend adding undefined to target properties.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#4229](https://github.com/microsoft/TypeScript-go/pull/4229) (Closed)

**Fix reparsing of JSDoc modifiers on constructor declarations**

*Improves reparsing logic for JSDoc modifiers applied to constructor declarations.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4230](https://github.com/microsoft/TypeScript-go/issues/4230) (Open, `documentation`)

**Behavior difference: tsgo no longer infer variadic \`args\` type when \`arguments\[\.\.\.\]\` is referenced inside plain js function body**

*tsgo no longer infers variadic args in plain JS functions referencing 'arguments', causing missing rest parameter types.*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#4231](https://github.com/microsoft/TypeScript-go/pull/4231) (Closed, **jakebailey**, **Copilot**)

**Skip trivia after '\<' in type\-argument arity error spans**

*Modifies TypeScript's type-argument arity diagnostics to skip trivia after '<' so error spans start at the first type argument.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4232](https://github.com/microsoft/TypeScript-go/pull/4232) (Closed)

**Fix spelling suggestions involving Unicode characters**

*Fix spelling suggestion logic to correctly handle and process Unicode characters.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4233](https://github.com/microsoft/TypeScript-go/pull/4233) (Closed)

**Obtain late\-bound symbol in error reporting**

*Retrieve late-bound symbols for error reports to improve diagnostic accuracy.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4234](https://github.com/microsoft/TypeScript-go/pull/4234) (Open, `No linked issue`)

**Skip mark/rewind in \`tryParseTypeArgumentsInExpression\` when token isn't \`\<\`**

*Optimize tryParseTypeArgumentsInExpression by skipping parser mark/rewind overhead when the token isn't '<', improving performance.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4640652269) **jakebailey** said "Do you have a benchmark that would show where this matters? And how often it matters?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4640655237) **mds-ant** committed to adding a benchmark before marking the PR ready for review

### [Issue microsoft/TypeScript-go#4235](https://github.com/microsoft/TypeScript-go/issues/4235) (Open, `bug`)

**Behavior difference: tsgo no longer emits comment on \`@typedef\` style object attributes**

*tsgo no longer preserves JSDoc comments on object properties defined via @typedef, causing missing documentation in emitted types.*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#4236](https://github.com/microsoft/TypeScript-go/issues/4236) (Open, `possible improvement`)

**\[Post\-7\.0\] Improve readability of \`Array\.from\` / \`TypedArray\.from\` \`mapFn\` parameters**

*Rename Array.from and TypedArray.from mapFn parameter names from v and k to element and index for improved IDE tooltip readability.*

 * created by **AXT-AyaKoto**

