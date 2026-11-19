# Report for 2026-11-12 (Thursday, November 12th, 2026)

13 different users commented on 70 different issues.

## Recommended Actions

 * Response Recommended
    * @remcohaszing asked for confirmation about supported `MappedOutput['extension']` values and the need for `outputExtensions` in [microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6831786212)
    * @remcohaszing proposed two changes to address content-mapper transform issues and requested maintainer consideration in [microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6851386454)
    * @meehow-m provided detailed reproduction steps and version results for a type inference regression that requires maintainer investigation in [microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6849600158)
    * @Sector6759 provided historical context about the original PR and the rationale for preferring `Omit<>` over `timeZone?: never` in [microsoft/TypeScript#65422](https://github.com/microsoft/TypeScript/pull/65422#issuecomment-6854695970)

## Activity Summary

### [Issue microsoft/TypeScript#64182](https://github.com/microsoft/TypeScript/issues/64182) (Open, `Suggestion`, `Domain: Content Mappers`, **andrewbranch**)

**Allow content\-mappers to return declarations instead of source files**

*Allow content mappers for static data formats to return declaration files, avoiding inappropriate module-format and syntax diagnostics.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6810719994) **andrewbranch** explained that the module format bug was fixed in #65432, but declaration file extensions must agree with the assigned module format to preserve declaration substitutability, and noted that this restriction reduced the motivation for returning declarations from Transform responses
 * [today](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6825097778) **remcohaszing** clarified that the `.cts` extension should produce declaration filenames such as `styles.d.css.cts`, then withdrew the earlier feature request after realizing it was based on a premature conclusion
 * [today](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6828331596) **andrewbranch** explained that `styles.d.css.cts` was not a recognized extension format and caused project-reference, incremental-compilation, and module-resolution issues
 * [today](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6831786212) **remcohaszing** asked whether `MappedOutput['extension']` could use `.mjs`, `.cjs`, `.mts`, or `.cts` without `outputExtensions`, and said they might update `css-modules-content-mapper` to emit ESM instead of CJS
 * [today](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6832876086) **andrewbranch** clarified that `.mts`/`.mjs` and their counterparts were interchangeable based on `package.json`, as long as input and output formats agreed
 * [later](https://github.com/microsoft/TypeScript/issues/64182#issuecomment-6851386454) **remcohaszing** proposed hiding TS1295 errors from virtual content-mapper code and passing allowed extensions in transform parameters to resolve module-syntax and extension-mapping issues

### [Issue microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **ahejlsberg**)

**Regression in 7\.1 \(\#64553\): R inferred as unknown through a generic type alias call signature with a nested same\-type argument**

*TypeScript 7.1 regression causes generic type inference to resolve a nested effect’s type parameter as unknown instead of Req.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6319872131) **kennysarnoski-jarvis** reported reproducing the regression on TypeScript 7.1 nightlies, identified its occurrence through nested generic aliases, and noted downstream impact on tsc-rs
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6544123377) **artile** provided a minimized reproduction showing a TypeScript 7.1 regression where inference changed from `never` to `unknown` for instantiated generic-interface methods when the outer type parameter was used in a nested type, and narrowed the regression to builds between 7.1.0-dev.20260930.4 and 7.1.0-dev.20261001.1
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6546851553) **kennysarnoski-jarvis** reported that #65077 identified and fixed the regression caused by an overly broad recursion check in #64553, added compiler coverage for the affected cases, and restored correct inference across the reported repros
 * [later](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6849600158) **meehow-m** reported a regression where generic object type aliases infer `T` as `unknown`, allowing invalid writes through `Promise<AsyncIterable<T>>`, and provided reproduction steps, version results, and analysis

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Proposes making type checking fully order-independent, with randomized ordering tests and extensive fixes for cache, traversal, and identifier-dependent behavior.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6811839297) **typescript-automation[bot]** reported that the requested performance run results were available and showed increased symbols and memory usage for the Compiler-Unions native scenario
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6811863495) **typescript-automation[bot]** reported new TypeScript errors in the Effect project’s user-test comparison and asked the maintainer to investigate the changes
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6813575722) **typescript-automation[bot]** reported changed top-1000-repository build results between the baseline and PR, including new TypeScript errors in PeerTube and Effect-TS, and asked the maintainer to investigate
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6852917162) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6852920064) **typescript-automation[bot]** reported that automated jobs had started and provided links to their build results
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6853646053) **typescript-automation[bot]** reported new TypeScript errors found when comparing baseline and PR user-test results, including implicit return type errors in SchemaAST.ts
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6853673975) **typescript-automation[bot]** reported that the DT tests completed and exposed a branch-only TypeScript compile error in d3-selection involving incompatible TransitionLike element types
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6853807663) **typescript-automation[bot]** provided the requested performance-run results, including compiler comparison metrics showing increased symbols and memory usage
 * [later](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6856589252) **typescript-automation[bot]** reported results from comparing the baseline and pull request TypeScript compiler runs across the top 1,000 repositories and flagged unexpected build changes for investigation

### [PR microsoft/TypeScript#65422](https://github.com/microsoft/TypeScript/pull/65422) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Disallow illegal 'timeZone' option in Temporal\.ZonedDateTime\.prototype\.toLocaleString \(\#64227\)**

*Disallow the illegal `timeZone` option in `Temporal.ZonedDateTime.prototype.toLocaleString` through stricter TypeScript typings.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65422#issuecomment-6780104468) **RyanCavanaugh** said "CI failing, please someone who can run hereby test open a PR."
 * (2 days ago) **RyanCavanaugh** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/65422#issuecomment-6782316508) **mechazod** said "@RyanCavanaugh I will revise the MR to include baseline test to fix the CI."
 * [later](https://github.com/microsoft/TypeScript/pull/65422#issuecomment-6854695970) **Sector6759** explained that the original PR’s author may have disappeared from the issue, described the implemented `timeZone?: never` suggestion, and noted that the latest PR documented why `Omit<>` was preferred

### [PR microsoft/TypeScript#65450](https://github.com/microsoft/TypeScript/pull/65450) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Key deferred indexed access types by their persistent access flags**

*Fix a porting bug so deferred indexed access types are keyed by persistent access flags rather than all access flags.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6811587717) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, linking to the build log
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6811765621) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65450#issuecomment-6812456020) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65455](https://github.com/microsoft/TypeScript/pull/65455) (Open, `For Uncommitted Bug`)

**Add opt\-in formatter options for blank lines**

*Add opt-in formatter settings to remove pre-brace blank lines and limit consecutive blank lines while preserving existing defaults.*

 * created by **rafamolina1**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65455#issuecomment-6832294784) **rafamolina1** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65456](https://github.com/microsoft/TypeScript/pull/65456) (Open, `For Backlog Bug`)

**Fix prepareRename placeholders for quoted and computed properties**

*Fix rename placeholders for quoted and computed properties by using the source node’s name while preserving existing range and fallback behavior.*

 * created by **rafamolina1**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65457](https://github.com/microsoft/TypeScript/issues/65457) (Open, `Bug`, `Domain: API`)

**\`typescript/async\`: getSourceFile\(\) returns a NumberKeyword for a typeToTypeNode\(\) result**

*`typeToTypeNode()` synthesizes a `NumberKeyword` whose `getSourceFile()` incorrectly returns the node itself instead of a `SourceFile`.*

 * created by **mathcovax**

### [Issue microsoft/TypeScript#65458](https://github.com/microsoft/TypeScript/issues/65458) (Open, `Bug`, `Domain: API`)

**Native API: Wtf8Decoder drops U\+FEFF from string literals and template text**

*Wtf8Decoder incorrectly strips U+FEFF from leading positions in string literals and template text when using the native TypeScript API.*

 * created by **mrousavy**

### [PR microsoft/TypeScript#65459](https://github.com/microsoft/TypeScript/pull/65459) (Closed, `For Uncommitted Bug`)

**Fix checker crash when sync iteration awaits an invalid thenable**

*Fixes a checker crash when sync iteration awaits invalid thenables by supplying construct-specific diagnostics for yield*, for-await, and direct yield.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65459#issuecomment-6838051625) **joshbarros** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65460](https://github.com/microsoft/TypeScript/pull/65460) (Closed, `For Uncommitted Bug`)

**Preserve U\+FEFF when Wtf8Decoder reads payload text**

*Make Wtf8Decoder preserve leading U+FEFF characters, including those following lone surrogates, by defaulting ignoreBOM to true.*

 * created by **joshbarros**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65460#issuecomment-6837568187) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **joshbarros** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65460#issuecomment-6838052128) **joshbarros** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65460#issuecomment-6838095276) **joshbarros** said "This PR references #65458 (Fixes #65458 in the description), so it already has a linked issue."

### [PR microsoft/TypeScript#65461](https://github.com/microsoft/TypeScript/pull/65461) (Closed, `For Backlog Bug`)

**Fix ASI diagnostics for Unicode line separators \(U\+2028 and U\+2029\)**

*Fix ASI diagnostics and source-position tracking for ECMAScript Unicode line separators U+2028 and U+2029 across compiler and language services.*

 * created by **amr807**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65461#issuecomment-6841292026) **amr807** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#65462](https://github.com/microsoft/TypeScript/issues/65462) (Closed)

**Content mappers: report a mapper's diagnostics without stopping type checking**

*Allow content mapper diagnostics to be reported as semantic errors without suppressing unrelated TypeScript type-checking diagnostics.*

 * created by **colinhacks**

### [PR microsoft/TypeScript#65463](https://github.com/microsoft/TypeScript/pull/65463) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve formatter alignment across tabs and enum decorators**

*Preserve formatter alignment by handling mixed whitespace tab stops and matching enum keywords after decorators.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65464](https://github.com/microsoft/TypeScript/pull/65464) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Check the preceding rune before recognizing conflict markers**

*Update conflict-marker detection to decode the preceding rune for line-boundary checks while preserving the ASCII fast path.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65465](https://github.com/microsoft/TypeScript/pull/65465) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Avoid slicing truncated source map charset values**

*Prevent panics when truncated data URLs contain incomplete UTF-8 charset prefixes while preserving case-insensitive matching and fallback behavior.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65466](https://github.com/microsoft/TypeScript/pull/65466) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore the enclosing variance diagnostic context**

*Restore the enclosing variance diagnostic context so variance errors retain their surrounding diagnostic information.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65467](https://github.com/microsoft/TypeScript/pull/65467) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Bind every destructured parameter in node\-builder scopes**

*Ensure all destructured parameters are bound in node-builder scopes to prevent incorrect declaration emission and global name resolution.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65468](https://github.com/microsoft/TypeScript/pull/65468) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Route typed emit paths to per\-file trace threads**

*Fix typed emit paths so tracing routes each path to its corresponding per-file trace thread instead of using `any`.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65469](https://github.com/microsoft/TypeScript/pull/65469) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove an random accessor from object literal grammar checking**

*Remove the unexplained random accessor from object literal grammar checking.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65470](https://github.com/microsoft/TypeScript/pull/65470) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix TODO in psuedochecker's typeNodeCouldReferToUndefined**

*Implement the pseudochecker’s typeNodeCouldReferToUndefined TODO and validate its behavior with a test.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65471](https://github.com/microsoft/TypeScript/pull/65471) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Return freshly cached post\-super flow results**

*Add the missing return statement so post-super flow results are returned when freshly cached.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65472](https://github.com/microsoft/TypeScript/pull/65472) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix getAdjustedLocationForDeclaration oops**

*Fix getAdjustedLocationForDeclaration to correctly use its provided parameter.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65473](https://github.com/microsoft/TypeScript/pull/65473) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Suggest the ES2015 library for missing Symbol references**

*Update missing Symbol references to suggest the appropriate ES2015 library, likely correcting an accidental find-and-replace error.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65474](https://github.com/microsoft/TypeScript/pull/65474) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix numeric falsiness and circular config parsing**

*Fix bugs involving numeric falsiness and circular configuration parsing.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65475](https://github.com/microsoft/TypeScript/pull/65475) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**, **johnfav03**)

**Prevent emitted files from retriggering native watch builds**

*Prevent generated output files from triggering native watch-mode rebuilds.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**, **johnfav03**

### [PR microsoft/TypeScript#65476](https://github.com/microsoft/TypeScript/pull/65476) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore fourslash marker selection and native JS test discovery**

*Fix fourslash marker iteration and restore native JavaScript test discovery after `_js_test.go` was misinterpreted as a GoOS-specific file.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65477](https://github.com/microsoft/TypeScript/pull/65477) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Preserve glob range negation and path boundaries**

*Fix the vendored glob implementation to correctly preserve range negation and enforce path boundaries.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65478](https://github.com/microsoft/TypeScript/pull/65478) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Respect Unicode boundaries when scanning symbol references**

*Ensure symbol reference scanning respects Unicode boundaries and refactor duplicated logic into a shared function.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65479](https://github.com/microsoft/TypeScript/pull/65479) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**, **gabritto**)

**Read declared members while instantiating base types**

*Ensure declared members are read during base-type instantiation by pushing resolvingObjectTypeStack earlier and updating base types.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**, **gabritto**

### [PR microsoft/TypeScript#65480](https://github.com/microsoft/TypeScript/pull/65480) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix mistaken slice delete in extractFromSymbol**

*Fix an out-of-bounds slice deletion in extractFromSymbol that can cause a crash when the second condition is true.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65481](https://github.com/microsoft/TypeScript/pull/65481) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ignore source files / module declarations in couldContainTypeVariables**

*Update couldContainTypeVariables to skip source file and module declaration nodes when traversing synthetic module wrapper symbols.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65482](https://github.com/microsoft/TypeScript/pull/65482) (Open, `For Backlog Bug`)

**fix\(api\): avoid encoder panic on normalized numeric literals**

*Prevent the API encoder from panicking when normalized numeric literals produce negative source offsets, preserving existing fallback behavior and wire format.*

 * created by **JemmyIndex**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65483](https://github.com/microsoft/TypeScript/issues/65483) (Open, `Bug`, `Domain: check: Order Dependence`)

**7\.1 regression: TS2339 in a self\-referencing object literal is dropped when another file on the same checker hits the same error first**

*A 7.1 regression drops TS2339 diagnostics in self-referencing object literals when another file reports the same error first under single-threaded checking.*

 * created by **meehow-m**

### [PR microsoft/TypeScript#65484](https://github.com/microsoft/TypeScript/pull/65484) (Open, `For Uncommitted Bug`)

**Stop alias deprecation walks at declaration\-free targets**

*Prevent alias deprecation checks from hanging by stopping traversal when an alias target has no declarations, such as intrinsic undefined.*

 * created by **mrousavy**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65484#issuecomment-6851748657) **mrousavy** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/65484#issuecomment-6851759466) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

