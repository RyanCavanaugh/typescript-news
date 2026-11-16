# Report for 2026-11-09 (Monday, November 9th, 2026)

24 different users commented on 91 different issues.

## Recommended Actions

 * Response Recommended
    * @el-j asked how a working solution would be implemented for the behavior that caused TypeScript 7 and 7.1 beta to panic and remain unusable in [microsoft/TypeScript#65058](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6771312983)
    * @alshdavid clarified how their ticket differed from the referenced issue and emphasized its remote, npm-free type resolution requirements in [microsoft/TypeScript#65355](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6751850958)
    * @yassinelakchouch reported a TypeScript 6.0.3 bug and confirmed it was fixed in TypeScript 7 in [microsoft/TypeScript#65389](https://github.com/microsoft/TypeScript/issues/65389#issuecomment-6748360990)
    * @denis-migdal questioned whether TS 7 had fixed the issue and provided a reproduction link showing the error persisted in TS 7.0.2 in [microsoft/TypeScript#65389](https://github.com/microsoft/TypeScript/issues/65389#issuecomment-6748580701)
    * @asilgumus provided reproduction details and asked how competing PRs would affect their proposed fix in [microsoft/TypeScript#65394](https://github.com/microsoft/TypeScript/pull/65394#issuecomment-6749304362)

## Activity Summary

### [Issue microsoft/TypeScript#63843](https://github.com/microsoft/TypeScript/issues/63843) (Closed, `API Request`, **andrewbranch**)

**Add native\-preview API for capturing \.d\.ts emit output**

*Request an API-mode capability to emit and capture `.d.ts` contents through virtual filesystem callbacks without writing to disk.*

 * (10 weeks ago) **RyanCavanaugh** added label `API Request`, and set milestone to `TypeScript 7.1`
 * [today](https://github.com/microsoft/TypeScript/issues/63843#issuecomment-6744114116) **TyceHerrman** said "This appears to have been addressed by microsoft/typescript-go#4699 - i think this can be closed now"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64235](https://github.com/microsoft/TypeScript/issues/64235) (Closed, `Suggestion`, `Domain: LS: Outlining`, `Experimentation Needed`, **gabritto**)

**Include terminating line in folding ranges when last token has no trailing non\-trivia**

*Adjust folding ranges to include the terminating line only when it contains non-trivia after the final token, rather than always excluding closing braces.*

 * **DanielRosenwasser** assigned to **gabritto**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64235#issuecomment-6339137692) **n-gist** argued that code-folding regions should use a single consistent END-line convention, preferably including the closing-delimiter line, while comments and import regions should end on their last content line; explained that mixed conventions would require extra client-side parsing and that inline content should not affect END boundaries
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64235#issuecomment-6339463401) **n-gist** clarified that the discussion was separate from PR #334371, proposed language-server options for adjusting outlining regions, and raised naming considerations for those options
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript#64438](https://github.com/microsoft/TypeScript/issues/64438) (Open, `Bug`)

**Incorrect/unhelpful error message for non\-module jsx file**

*Improve JSX diagnostics for non-module files by explaining that scripts cannot import the configured JSX runtime and suggesting a module workaround.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-5911162732) **SiddhantShedge45** expressed interest in working on the issue and proposed improving the JSX diagnostic, adding a regression test, and verifying module-based JSX behavior
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-6260062351) **vivan070707-ctrl** asked whether the issue was still available to work on and offered to investigate it with a fix and regression test
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64438#issuecomment-6468222987) **Shriraj1901** offered to reproduce the JSX diagnostic issue, trace compiler checks, and add regression tests, while asking whether another contributor was already working on it before assignment
 * **RyanCavanaugh** removed label `Good First Issue`

### [PR microsoft/TypeScript#64445](https://github.com/microsoft/TypeScript/pull/64445) (Closed, `For Uncommitted Bug`)

**Improve diagnostic for implicit JSX runtime imports in non\-module files**

*Improve JSX implicit runtime import diagnostics by identifying non-module files and suggesting moduleDetection or an empty export.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64445#issuecomment-5833304536) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/64445#issuecomment-5833335173) **sh011** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/64445#issuecomment-6755657436) **RyanCavanaugh** said "Closing every PR for this issue because there are seven of them"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64501](https://github.com/microsoft/TypeScript/pull/64501) (Closed, `For Backlog Bug`)

**Improve error when break/continue label is in the same function but not enclosing**

*Improve break/continue diagnostics for same-function labels that do not enclose the statement, while preserving cross-function errors.*

 * (5 weeks ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64501#issuecomment-5891101326) **britsync07-prog** addressed both findings by caching per-function label sets on the checker, added coverage for break targets involving a function and class static block, signed the CLA, and reported that the break/continue/label tests passed with existing baselines unchanged
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64548](https://github.com/microsoft/TypeScript/issues/64548) (Closed, `Needs Investigation`, `Domain: Content Mappers`, **andrewbranch**)

**Content mappers: \`moduleSuffixes\` probes \`card\.foo\.web\` instead of \`card\.web\.foo\` for a registered extension**

*Content mapper resolution incorrectly applies module suffixes after custom extensions, causing imports like `./card.foo` to resolve to the wrong file.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-5916751267) **leonidaz** filed #64560 proposing an optional `moduleSuffixes` list for `contentMappers`, including a prototype and results table, and agreed to close this issue in favor of it
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-5964096116) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (5 weeks ago) **typescript-automation[bot]** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/64548#issuecomment-6750423962) **andrewbranch** questioned whether content mapper extensions should support `moduleSuffixes` like built-in extensions, noting that suffix resolution works even when the import includes an extension
 * (today) **andrewbranch** reopened the issue
 * (today) **andrewbranch** added labels `Needs Investigation`, `Domain: Content Mappers`, removed label `Working as Intended`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64560](https://github.com/microsoft/TypeScript/issues/64560) (Closed, `Suggestion`)

**Content mappers: a \`moduleSuffixes\` list on a \`contentMappers\` entry**

*Add optional per-content-mapper module suffixes to resolve platform-specific variants of files with custom extensions.*

 * created by **leonidaz**
 * **RyanCavanaugh** added label `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/64560#issuecomment-6750460393) **andrewbranch** said "Closing in favor of the original #64548"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64568](https://github.com/microsoft/TypeScript/issues/64568) (Closed)

**Bug Report: Severe memory leak triggered by "TypeScript \(Native Preview\)" extension**

*The TypeScript Native Preview extension causes an unrecoverable memory leak in empty projects near other Git repositories, unless a package.json exists.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-5931170686) **dbaeumer** said "Moving back to the TS team based on the above analysis."
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-6160927576) **DerekZiemba** reported that the TypeScript native preview extension launched its `tsc.exe` language server without the related TypeScript extension or Copilot installed, consumed about 10 GB of memory, and ignored the configured 4 GiB memory limits
 * **jakebailey** unassigned **dbaeumer**
 * [today](https://github.com/microsoft/TypeScript/issues/64568#issuecomment-6751667502) **RyanCavanaugh** reported that many memory issues had been fixed and that long synthetic LSP sessions showed stable memory usage, then requested a new issue with a concrete reproduction if the problem persisted
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64575](https://github.com/microsoft/TypeScript/pull/64575) (Closed, `For Uncommitted Bug`)

**Add regression test for jsxImportSource in non\-module files**

*Add a regression test ensuring jsxImportSource resolves correctly in non-module JSX files and uses the runtime’s intrinsic element types.*

 * created by **pmudassir**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64575#issuecomment-6755659839) **RyanCavanaugh** said "Closing every PR for this issue because there are seven of them"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64616](https://github.com/microsoft/TypeScript/pull/64616) (Closed, `For Uncommitted Bug`)

**fix: improve error message for JSX in non\-module files \(Issue \#64438\)**

*Improve JSX diagnostics in non-module files by reporting the missing JSX types error instead of a misleading react/jsx-runtime module error.*

 * created by **OMD-123**
 * (5 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64616#issuecomment-6755662156) **RyanCavanaugh** said "Closing every PR for this issue because there are seven of them"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64828](https://github.com/microsoft/TypeScript/issues/64828) (Closed, `Needs Investigation`, **andrewbranch**)

**Content mappers: go\-to\-definition on an module specifier returns nothing when the target file has more than one span\-map segment**

*Go-to-definition for module specifiers returns no result when content-mapped target files contain multiple span-map segments.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6276004130) **NullVoxPopuli-ai-agent** provided a minimal TypeScript reproduction, corrected the trigger to `export ... from`, and identified that failures depend on multiple span mappings in re-exports
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6328616011) **colinhacks** reported that non-relative import specifiers, including path aliases, also broke go-to-definition and provided reproduction details from 7.1.0-beta with a two-segment mapper
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64828#issuecomment-6504336488) **NullVoxPopuli** mentioned opening fix #65009 for `SourceFile` go-to-definition behavior in content-mapped files and adding tests for export and paths-alias imports
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64908](https://github.com/microsoft/TypeScript/pull/64908) (Closed, `For Uncommitted Bug`)

**Improve diagnostic for automatic JSX in script files**

*Improve diagnostics for automatic JSX in script files by reporting TS2884 and guiding users to add `export {}`, with regression tests and updated baselines.*

 * created by **gabrielvfonseca**
 * (2 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64908#issuecomment-6755664549) **RyanCavanaugh** said "Closing every PR for this issue because there are seven of them"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64933](https://github.com/microsoft/TypeScript/pull/64933) (Closed, `For Uncommitted Bug`)

**Fix: Improve error message for non\-module JSX files**

*Improve diagnostics for JSX in non-module scripts by explaining the module requirement and suggesting `export {}`.*

 * created by **Dipak-coder-06**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64933#issuecomment-6755666531) **RyanCavanaugh** said "Closing every PR for this issue because there are seven of them"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64983](https://github.com/microsoft/TypeScript/issues/64983) (Closed, `Duplicate`)

**Module resolution: imports in a referenced \`nodenext\` ESM project resolve in CJS mode when the referencing project uses \`bundler\`**

*TypeScript resolves imports in referenced NodeNext ESM projects using CJS conditions when the referencing project uses bundler resolution, selecting incorrect declaration files.*

 * created by **joshkel**
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/64983#issuecomment-6749719527) **RyanCavanaugh** identified the issue as a duplicate of #57553
 * (today) **joshkel** closed the issue

### [PR microsoft/TypeScript#65004](https://github.com/microsoft/TypeScript/pull/65004) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Skip code generation in CI**

*Add a flag to skip benchmarker code generation in CI, defaulting to enabled locally and disabled in CI.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65004#issuecomment-6673166572) **jakebailey** requested that @typescript-bot run the performance test faster to double-check the results
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65004#issuecomment-6673167953) **typescript-automation[bot]** reported that the performance test job started and linked to its results
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65004#issuecomment-6673851195) **typescript-automation[bot]** provided the requested performance-run results comparing the baseline and PR
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65005](https://github.com/microsoft/TypeScript/pull/65005) (Closed, `For Backlog Bug`)

**Report an error for class declarations in statement position**

*Report TS1156 for class declarations in statement positions, matching JavaScript engine behavior while preserving valid class expressions and block-scoped declarations.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65005#issuecomment-6486321253) **TimonGaertner** said "@microsoft-github-policy-service agree"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65005#issuecomment-6489373507) **RyanCavanaugh** said "@TimonGaertner this is an unusually good test, what model and reasoning effort were you using?"
 * (1 week ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/65005#issuecomment-6754940858) **TimonGaertner** said "@RyanCavanaugh I was using Claude Fable 5.1 with medium reasoning effort"

### [Issue microsoft/TypeScript#65008](https://github.com/microsoft/TypeScript/issues/65008) (Closed, `Working as Intended`)

**lib\.dom\.d\.ts: Transformer is missing the \`cancel\` member that WHATWG Streams defines**

*Add the missing WHATWG Streams `cancel` member to TypeScript’s DOM `Transformer` interface so valid TransformStream handlers compile.*

 * created by **HouMinXi**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65008#issuecomment-6504429596) **HouMinXi** explained that `Transformer.cancel` was intentionally omitted from `lib.dom.d.ts` because major browsers do not yet implement it, and provided a matching local declaration-merge workaround until two browser engines support it
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65008#issuecomment-6507251988) **timurzvural** opened a fix adding `Transformer.cancel` and `TransformerCancelCallback` to the DOM and Web Worker type definitions, along with a fixture update and compiler regression test
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/65008#issuecomment-6749745363) **RyanCavanaugh** explained that the behavior was expected because DOM libraries followed the generator’s browser-engine support policy, and noted that Node-specific support could be added locally using matching `any` type-parameter defaults

### [PR microsoft/TypeScript#65009](https://github.com/microsoft/TypeScript/pull/65009) (Closed, `For Milestone Bug`, **andrewbranch**)

**Go to a content\-mapped file from its module specifier**

*Fix go-to-definition for module specifiers targeting content-mapped files by navigating to the target file’s beginning.*

 * (1 week ago) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **andrewbranch**
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65009#issuecomment-6504340709) **NullVoxPopuli** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65009#issuecomment-6750177696) **NullVoxPopuli** noted that CI likely only needed a rerun because something appeared to have gone wrong with the runners
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#65022](https://github.com/microsoft/TypeScript/pull/65022) (Closed, `For Uncommitted Bug`)

**Keep nested JSDoc properties after a property with a missing name**

*Preserve nested JSDoc properties following a malformed property type instead of incorrectly promoting them to the top-level typedef.*

 * created by **NullVoxPopuli**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65022#issuecomment-6751966284) **NullVoxPopuli** said "thoughts on the approach here?"
 * [today](https://github.com/microsoft/TypeScript/pull/65022#issuecomment-6756159710) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65022#issuecomment-6756161331) **typescript-automation[bot]** reported that the requested test and performance jobs had started, with results available or pending
 * [today](https://github.com/microsoft/TypeScript/pull/65022#issuecomment-6756679417) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, with a link to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65022#issuecomment-6756764469) **typescript-automation[bot]** reported that user tests comparing the baseline and PR with tsc passed successfully
 * [today](https://github.com/microsoft/TypeScript/pull/65022#issuecomment-6757260800) **typescript-automation[bot]** reported that the requested performance run results were available and included a baseline-versus-PR comparison showing no meaningful changes in the displayed compiler metrics.
 * [today](https://github.com/microsoft/TypeScript/pull/65022#issuecomment-6757617148) **typescript-automation[bot]** reported that testing the top 400 repositories with tsc showed no differences between the baseline and PR, with everything looking good

### [Issue microsoft/TypeScript#65051](https://github.com/microsoft/TypeScript/issues/65051) (Open, `Suggestion`)

**API: coarse\-grained checker queries for tools that extract a whole API surface \(\`getSymbolDocumentations\`, \`getMembersOfType\`\)**

*Add bulk checker APIs for symbol documentation and type-member metadata to reduce round trips and improve out-of-process API extraction performance.*

 * created by **WinterYukky**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6518847399) **aetherxeg-source** proposed adding a differential regression fixture to compare fine-grained and coarse-grained member traversal, covering inheritance, overloads, visibility, filtering, metadata, and ordering
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65051#issuecomment-6519041664) **WinterYukky** said "Thanks, good suggestion. I'll add a differential fixture comparing both paths on the same program to the PR."
 * **RyanCavanaugh** added label `Suggestion`

### [Issue microsoft/TypeScript#65057](https://github.com/microsoft/TypeScript/issues/65057) (Closed)

**Native printer panics when printing JSDoc AST nodes**

*The native Go printer panics when printing JSDoc AST nodes because `emitJSDocNode` remains unimplemented.*

 * created by **el-j**
 * [today](https://github.com/microsoft/TypeScript/issues/65057#issuecomment-6750224428) **RyanCavanaugh** said "Please use a template"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65058](https://github.com/microsoft/TypeScript/pull/65058) (Closed, `For Uncommitted Bug`)

**feat\(printer\): implement JSDoc node emission in AST printer**

*Implements canonical JSDoc emission in the AST printer, including tags, parameter types, inline links, and synthetic comments for API-printed nodes.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6527458799) **el-j** said "@microsoft-github-policy-service agree"
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6527518658) **el-j** reported addressing all nine review threads, pushing updates to `release-7.1`, and passing local validation and focused printer tests; noted that fork PR CI and CodeQL workflows required maintainer approval and asked for workflow approval and PR review
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6528188256) **el-j** reported addressing all five new review comments in commit 4c2c6fa3ac, resolving all 14 threads, and passing the printer tests and validation locally; noted that upstream CI had not run and requested maintainer re-review and required CI checks
 * [today](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6750242760) **RyanCavanaugh** said "This needs an approved issue in order to think about a PR."
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/65058#issuecomment-6771312983) **el-j** argued that TypeScript 7 and 7.1 beta remained unusable because of panics, cited related open issues, and asked how the previously working behavior would be restored

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*A major checker overhaul aims to make type checking, diagnostics, and behavior fully independent of traversal, file, and cache ordering.*

 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6741290864) **typescript-automation[bot]** reported the requested performance results, showing increases in symbols, types, and memory usage for the Compiler-Unions native scenario while errors remained unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6741520688) **typescript-automation[bot]** reported new TypeScript errors in the user-test comparison and asked Jake Bailey to investigate the changes
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6744032788) **typescript-automation[bot]** reported results from running tsc on the top 1,000 repositories, highlighting unexpected build changes in PeerTube and Effect-TS projects for maintainer review
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6756378915) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6756380618) **typescript-automation[bot]** reported that automated build and test jobs had started and linked to their results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6757011867) **typescript-automation[bot]** provided the requested performance results, including compiler comparison metrics for the pull request
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6757066662) **typescript-automation[bot]** reported that the DT tests completed and exposed a branch-only TypeScript compile error in d3-selection involving an incompatible TransitionLike return type
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6757305882) **typescript-automation[bot]** reported new TypeScript errors in the Effect user-test comparison and asked Jake Bailey to investigate the changes
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6759187201) **typescript-automation[bot]** reported changed TypeScript compiler results from testing the top 1,000 repositories and asked for investigation
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6761556486) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6761558281) **typescript-automation[bot]** reported that the `pack this` job started and provided links to its workflow run and results
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6761695924) **typescript-automation[bot]** provided an installable npm package and playground for commit 9833c9c94ef92ecc036303c8bec404b4fe107503, along with installation instructions

### [Issue microsoft/TypeScript#65086](https://github.com/microsoft/TypeScript/issues/65086) (Closed)

**Implicit Function Parameter Types won't Work in JavaScript**

*JavaScript parameter types are not inferred for reassigned object or class methods outside function bodies under checkJs or @ts-check.*

 * created by **neurolag**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/65086#issuecomment-6556572911) **neurolag** said "Perhaps, this is related to #44640"
 * [today](https://github.com/microsoft/TypeScript/issues/65086#issuecomment-6751785588) **RyanCavanaugh** said "These are all fixed in TS7"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/65086#issuecomment-6752503429) **neurolag** said "Awesome, thank you so much for letting me know :smile: "

### [PR microsoft/TypeScript#65284](https://github.com/microsoft/TypeScript/pull/65284) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Restrict content mapper extensions to a single dot**

*Prohibit content mapper extensions containing multiple dots to avoid complexity and confusing interactions with module suffixes.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65284#issuecomment-6612111669) **jakebailey** said "Would this break say, .tar.gz?"
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65284#issuecomment-6612147209) **andrewbranch** said "Yep, exactly."
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/65284#issuecomment-6612192072) **andrewbranch** suggested prohibiting overlapping extension registrations, such as `.tar.gz` and `.gz`, as a configuration error to reduce complexity, noting that longer extensions were currently treated as more specific
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65316](https://github.com/microsoft/TypeScript/issues/65316) (Open, `Bug`)

**JSX error reporting is inconsistent**

*JSX type and syntax errors are inconsistent, excessive, and sometimes misleading, reducing developer experience and requiring improved diagnostics.*

 * created by **remcohaszing**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65319](https://github.com/microsoft/TypeScript/pull/65319) (Closed, `Author: Team`, `For Milestone Bug`, **gabritto**)

**Adjust folding range's end line only if closing bracket followed by non\-trivia**

*Adjust folding range end lines to hide standalone closing brackets while preserving lines containing relevant non-whitespace content, including content-mapped files.*

 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/65319#issuecomment-6672277703) **n-gist** argued that excluding the closing-bracket line from Language Service folding output could shift its purpose toward presentation, introduce ambiguity and information loss, and cause clients to adjust folding regions incorrectly; provided an example involving an `if`/`else` construct.
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65319#issuecomment-6697188838) **gabritto** argued that excluding a closing-bracket line with trailing non-trivia could shift language-service output from syntactic boundaries to opinionated presentation data, create ambiguity for clients, and cause incorrect folding adjustments
 * [today](https://github.com/microsoft/TypeScript/pull/65319#issuecomment-6751431376) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/65319#issuecomment-6751433195) **typescript-automation[bot]** reported that the `pack this` job had started and would update with build results
 * [today](https://github.com/microsoft/TypeScript/pull/65319#issuecomment-6752396910) **gabritto** updated the PR to preserve comments and hide only whitespace
 * [today](https://github.com/microsoft/TypeScript/pull/65319#issuecomment-6753761987) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/65319#issuecomment-6753764066) **typescript-automation[bot]** reported that the "pack this" job started and completed with failed results
 * [today](https://github.com/microsoft/TypeScript/pull/65319#issuecomment-6753911567) **typescript-automation[bot]** reported that it was unable to build and publish the PR and linked the failed workflow logs
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript#65321](https://github.com/microsoft/TypeScript/pull/65321) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Don't run go\-test\-wasm in merge queue CI**

*Remove go-test-wasm from merge queue CI to make quick checks faster.*

 * (5 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65326](https://github.com/microsoft/TypeScript/issues/65326) (Open, `Needs Investigation`, **andrewbranch**)

**Allow to influence trigger characters for files with content\-mappers**

*Request an API allowing content mappers to define additional completion trigger characters for embedded file types such as Svelte.*

 * created by **dummdidumm**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/65326#issuecomment-6754508009) **andrewbranch** said "I think this is a reasonable feature request, but I'm also curious if for this particular case you considered emitting TSX for Svelte files?"

### [Issue microsoft/TypeScript#65333](https://github.com/microsoft/TypeScript/issues/65333) (Open, `Bug`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Downlevel \`this\.\#x &&= v\` / \`\|\|=\` / \`??=\` on a private accessor always calls the setter**

*Downleveling private accessor logical assignments unconditionally invokes setters instead of preserving short-circuit behavior for &&=, ||=, and ??=.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/65333#issuecomment-6663396499) **RyanCavanaugh** asked @trackoor to detail the prompt, model, and approach used to generate the high-quality bug report
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/65333#issuecomment-6665295542) **morluto** said "nice."
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/65333#issuecomment-6677488799) **trackoor** described using a formally verified TypeScript compiler and runtime as a ground truth, differential fuzzing to find bugs, and AI to triage and report them; emphasized the importance of accurate specifications and invariants
 * **RyanCavanaugh** assigned to **weswigham**

### [Issue microsoft/TypeScript#65339](https://github.com/microsoft/TypeScript/issues/65339) (Open, `Bug`, `Domain: lib.d.ts`)

**ESNext\.SharedMemory still declares the removed Atomics\.pause parameter**

*Update the ESNext.SharedMemory declaration so Atomics.pause() accepts no arguments, matching the ECMAScript specification.*

 * created by **dvkam**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: lib.d.ts`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65346](https://github.com/microsoft/TypeScript/issues/65346) (Open, `Bug`, `Domain: API`)

**Sync API on Windows: "timed out connecting to named pipe" seconds after the server process already exited**

*On Windows, the sync API times out waiting for a named pipe instead of promptly reporting that its server process exited during startup.*

 * created by **YevheniiKotyrlo**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/65346#issuecomment-6678289890) **Princekrcoder** offered to reproduce and investigate the issue on Windows 11 and submit a fix if unassigned
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: API`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65352](https://github.com/microsoft/TypeScript/pull/65352) (Open, `For Backlog Bug`)

**lib: remove obsolete Atomics\.pause parameter**

*Remove the obsolete optional parameter from the Atomics.pause declaration and update conformance baselines to expect TS2554 for argument-bearing calls.*

 * created by **JemmyIndex**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65355](https://github.com/microsoft/TypeScript/issues/65355) (Closed, `Duplicate`)

**Remote declaration resolution**

*Request support for resolving remote TypeScript declaration files in browser-based, bundler-free ESM projects without installing runtime dependencies.*

 * created by **alshdavid**
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6750067519) **RyanCavanaugh** identified the issue as a duplicate of #35749
 * [today](https://github.com/microsoft/TypeScript/issues/65355#issuecomment-6751850958) **alshdavid** clarified that their ticket concerned modeling browser import maps and fetching type definitions from remote URLs without requiring npm installation, unlike the referenced ticket that used local node_modules types

### [Issue microsoft/TypeScript#65357](https://github.com/microsoft/TypeScript/issues/65357) (Closed, `Not a Defect`)

**TypeScript 7\.1: in checks always succeed for child properties on RemoteNode, breaking type narrowing**

*TypeScript 7.1 RemoteNode prototypes make `in` checks for child properties always succeed, breaking type narrowing and causing runtime errors.*

 * created by **k-taro56**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/65357#issuecomment-6682807545) **MartinJohns** said "Just pointing out that the in operator is intentionally unsound. Objects are not sealed and upcasting is implicitly allowed (assign type with the property to a type without it)."
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/65357#issuecomment-6685266543) **k-taro56** clarified that the issue concerned runtime behavior changes since version 6.0
 * [today](https://github.com/microsoft/TypeScript/issues/65357#issuecomment-6750082572) **RyanCavanaugh** said "6.0 and 7.0 API are not intended to work identically, and in isn't a documented/sound way of doing these checks."
 * **RyanCavanaugh** added label `Not a Defect`

### [PR microsoft/TypeScript#65359](https://github.com/microsoft/TypeScript/pull/65359) (Open, `For Backlog Bug`)

**Fix JSX intrinsic tag error reporting**

*Improve JSX intrinsic tag diagnostics by eliminating duplicates, pinpointing errors on tag names, and preserving closing-tag symbol resolution.*

 * created by **ayushtripathi-45**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65365](https://github.com/microsoft/TypeScript/issues/65365) (Closed, `Not a Defect`)

**TS2589 in 7\.1 on code that 5\.9 and 6\.0 accept, caused by stable union ordering \(6\.0 with \-\-stableTypeOrdering does not finish\)**

*TypeScript 7.1 reports TS2589 on valid recursive conditional and intersection types due to stable union ordering, unlike 5.9 and 6.0.*

 * created by **yusufyildiz34**
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/65365#issuecomment-6750101306) **RyanCavanaugh** clarified that the behavior was not a TS7 regression, existed in TS6 with `--stableTypeOrdering`, and that reporting TS2589 was preferable to a non-terminating check

### [PR microsoft/TypeScript#65367](https://github.com/microsoft/TypeScript/pull/65367) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] order independence \+ dynamic checkers / work stealing**

*Experiment proposes order-independent processing with dynamically adjustable checker counts and work stealing between checkers.*

 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6741032418) **typescript-automation[bot]** reported that the DT tests found a branch-only type error in d3-selection involving an incompatible TransitionLike<HTMLParagraphElement, number> return type
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6741053344) **typescript-automation[bot]** reported new TypeScript errors in the user-test comparison and asked Jake Bailey to investigate the changes
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6744438742) **typescript-automation[bot]** reported results from running tsc on the top 1,000 repositories, highlighting unexpected build changes in PeerTube and Effect-TS projects for maintainer review
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6745327159) **typescript-automation[bot]** reported the requested performance run results, including baseline-versus-PR compiler metric comparisons
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6756379296) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6756381520) **typescript-automation[bot]** reported that automated test jobs had started and provided links to their build and result pages
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6757143565) **typescript-automation[bot]** reported the requested performance-run results, including baseline-versus-PR compiler metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6757217936) **typescript-automation[bot]** reported that the DT tests completed and exposed a branch-only TypeScript compile error in d3-selection involving an incompatible TransitionLike return type
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6757366022) **typescript-automation[bot]** reported new TypeScript errors in the Effect user-test comparison and asked Jake Bailey to investigate the changes
 * [today](https://github.com/microsoft/TypeScript/pull/65367#issuecomment-6759229841) **typescript-automation[bot]** reported top-1000-repository tsc comparison results, highlighting unexpected build failures in PeerTube and Effect-TS and asking Jake Bailey to investigate

### [Issue microsoft/TypeScript#65371](https://github.com/microsoft/TypeScript/issues/65371) (Closed, `Needs Investigation`, **andrewbranch**)

**LSP messages are JSON\-encoded twice when written to the client**

*Avoid double JSON encoding of LSP messages by implementing direct encoder support, reducing completion response encoding time and allocations.*

 * created by **hood**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/65371#issuecomment-6746240225) **andrewbranch** said "@hood feel free to open the PR, thanks!"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65373](https://github.com/microsoft/TypeScript/pull/65373) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Drop old references and code relating to the tsgo name**

*Remove obsolete references and code associated with the deprecated tsgo name, since no tsgo artifacts are published.*

 * (3 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65378](https://github.com/microsoft/TypeScript/issues/65378) (Open, `Bug`, `Domain: Crashes`)

**Crash on async generator that yields a thenable and another value**

*TypeScript crashes when checking an async generator that yields a thenable followed by another value instead of reporting TS1321.*

 * created by **trackoor**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Crashes`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65379](https://github.com/microsoft/TypeScript/issues/65379) (Open, `Bug`, `Domain: Declaration Emit`)

**Declaration emit writes \`\[SymbolConstructor\.iterator\]\` as a computed key when a \`SymbolConstructor\` value is in scope**

*Declaration emit regressed in TypeScript 7.x, incorrectly emitting `[SymbolConstructor.iterator]` instead of `[S.iterator]` when `SymbolConstructor` is in scope.*

 * created by **trackoor**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Declaration Emit`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#65380](https://github.com/microsoft/TypeScript/issues/65380) (Open)

**\`readonly\` dropped from a function\-valued property under a \`const\` type parameter**

*TypeScript 7.x declaration emit incorrectly drops readonly from nested function-valued properties inferred under const type parameters.*

 * created by **trackoor**
 * (yesterday) **trackoor** closed the issue
 * (today) **trackoor** reopened the issue

### [Issue microsoft/TypeScript#65382](https://github.com/microsoft/TypeScript/issues/65382) (Closed)

**JS emit produces invalid or wrong code: downlevel \`for \(this\.\#x of \.\.\.\)\`, wrapped CommonJS calls, \`react\-jsxdev\` before \`super\(\)\`**

*Downleveling `for...in` and `for...of` loops assigning to private fields emits invalid left-hand sides without diagnostics.*

 * created by **trackoor**
 * [today](https://github.com/microsoft/TypeScript/issues/65382#issuecomment-6751142458) **RyanCavanaugh** said "Please log 3 separate bugs"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/65382#issuecomment-6751515248) **trackoor** said "@RyanCavanaugh Thanks! I have filed separately as #65413, #65414 and #65415."

### [Issue microsoft/TypeScript#65385](https://github.com/microsoft/TypeScript/issues/65385) (Open, `Needs More Info`)

**VisualStudio 2026 \- Razor Class Library**

*Adding Microsoft.TypeScript.MSBuild 7.0.1 to Razor or Blazor projects causes Visual Studio to repeatedly detect changes, prompt reloads, or prevent applications from running.*

 * created by **ghorner2**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/65385#issuecomment-6750712289) **RyanCavanaugh** requested a minimal Razor/Blazor project, the exact Visual Studio version, reproduction steps, the project file, and relevant build or ActivityLog output for the reload loop

### [Issue microsoft/TypeScript#65386](https://github.com/microsoft/TypeScript/issues/65386) (Closed, `Design Limitation`)

**Semantic tokens re\-check files on a cold query checker after diagnostics already checked them**

*Semantic token requests redundantly re-type-check edited files after diagnostics, and should reuse the completed diagnostics checker to reduce latency.*

 * created by **hood**
 * [today](https://github.com/microsoft/TypeScript/issues/65386#issuecomment-6752482533) **RyanCavanaugh** reported that the proposed reuse was unsafe because checker order sensitivity and cross-file operations could suppress circular-instantiation diagnostics, and provided a minimal reproduction and test results demonstrating the issue
 * **RyanCavanaugh** added label `Design Limitation`

### [Issue microsoft/TypeScript#65387](https://github.com/microsoft/TypeScript/issues/65387) (Closed, **jakebailey**, **Copilot**)

**LSP registers a recursive watch on \`/Users\` for projects without a package\.json on macOS**

*On macOS, the TypeScript LSP recursively watches `/Users` instead of the project directory when projects lack a package.json, causing excessive file-watcher CPU usage.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/65387#issuecomment-6720788144) **jakebailey** said "Yeah, I think the intent is that this behave like the other OSs."
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65389](https://github.com/microsoft/TypeScript/issues/65389) (Closed, `Bug`, `Fixed`)

**When a non\-generic value and a generic type shares the same name 'X', "Type 'X' is not generic\."**

*TypeScript incorrectly reports that a generic exported class value is not generic when sharing its name with an imported generic type.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/65389#issuecomment-6748360990) **yassinelakchouch** reported that TypeScript 6.0.3 incorrectly treated an imported generic type alias shadowed by an exported class as non-generic, and noted that TypeScript 7 fixed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/65389#issuecomment-6748580701) **denis-migdal** questioned whether TS 7 had fixed the issue and reported reproducing the same error in TS 7.0.2 using the unofficial playground
 * (today) **RyanCavanaugh** added labels `Bug`, `Fixed`
 * [today](https://github.com/microsoft/TypeScript/issues/65389#issuecomment-6750777381) **RyanCavanaugh** reported that the issue was fixed in the latest version
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/65389#issuecomment-6752276603) **denis-migdal** explained that the unofficial TypeScript playground used an older version, confirmed the issue was fixed in TS7, and thanked the maintainer for the information

### [PR microsoft/TypeScript#65393](https://github.com/microsoft/TypeScript/pull/65393) (Closed, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Avoid recursive LSP watches on macOS home\-directory roots**

*Prevent recursive LSP watches on macOS by grouping home-directory roots and verifying project and sibling-directory watches remain intact.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65394](https://github.com/microsoft/TypeScript/pull/65394) (Closed, `For Uncommitted Bug`)

**Improve diagnostic for JSX in script files**

*Improve JSX diagnostics by reporting when implicit runtime imports fail because a `.tsx` file is a non-module script.*

 * created by **asilgumus**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65394#issuecomment-6723851300) **jakebailey** said "Why did you choose to fix this specific issue?"
 * [today](https://github.com/microsoft/TypeScript/pull/65394#issuecomment-6749304362) **asilgumus** described reproducing issue #64438 in tsgo, confirmed the misleading TS2875 diagnostic was caused by a non-module script despite installed types, and explained that the proposed diagnostic provided a more actionable fix; offered to close the PR if another solution landed
 * [today](https://github.com/microsoft/TypeScript/pull/65394#issuecomment-6749333639) **asilgumus** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65394#issuecomment-6755670436) **RyanCavanaugh** said "Closing every PR for this issue because there are seven of them"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#65395](https://github.com/microsoft/TypeScript/pull/65395) (Closed, `For Backlog Bug`)

**Report an error for private identifiers in JSX tag and attribute names**

*Reject private identifiers in JSX tag and attribute names with an “Identifier expected” syntax error instead of emitting invalid JavaScript.*

 * created by **elecmonkey**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65395#issuecomment-6726325704) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65396](https://github.com/microsoft/TypeScript/issues/65396) (Open, `Bug`, `Domain: JSX/TSX`, **RyanCavanaugh**, **Copilot**)

**JSX tag and attribute names starting with \`\#\` are accepted without a syntax error**

*JSX incorrectly accepts tag and attribute names beginning with `#`, producing missing syntax errors and invalid JavaScript output.*

 * created by **elecmonkey**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: JSX/TSX`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65397](https://github.com/microsoft/TypeScript/pull/65397) (Closed, `Author: Team`, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 3 updates**

*Update the GitHub CodeQL Actions init, analyze, and upload-sarif dependencies from version 4.39.1 to 4.39.3.*

 * **dependabot[bot]** added label `github_actions`
 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65398](https://github.com/microsoft/TypeScript/pull/65398) (Open, `For Backlog Bug`)

**fix\(checker\): avoid crashing on invalid async generator yields**

*Prevent the native checker from crashing on invalid async generator yields by ignoring nil yielded types while preserving TS1321 diagnostics and inference.*

 * created by **JemmyIndex**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65399](https://github.com/microsoft/TypeScript/issues/65399) (Open, `Bug`, `Domain: Error Messages`)

**Inconsistent diagnostic and misleading error span for 'override declare' \(TS1040 vs TS1243\)**

*Report inconsistent diagnostics for `override declare` properties, requesting symmetric TS1243 errors and correctly positioned messaging regardless of modifier order.*

 * created by **ShakilUrRehman21**
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Error Messages`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#65400](https://github.com/microsoft/TypeScript/pull/65400) (Open, `For Backlog Bug`)

**Report TS1243 instead of TS1040 for 'override declare' modifier order**

*Report TS1243 instead of inaccurate TS1040 when `declare` precedes `override`, aligning diagnostics and error placement for modifier order.*

 * created by **ShakilUrRehman21**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65400#issuecomment-6733685761) **ShakilUrRehman21** said "@microsoft-github-policy-service agree"
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65402](https://github.com/microsoft/TypeScript/issues/65402) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**False TS7027 and wrong narrowing when the left operand of \`??\` is falsy but not nullish**

*Nullish coalescing incorrectly narrows falsy non-nullish left operands, causing false TS7027 unreachable-code errors and missed type errors.*

 * created by **cplieger**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#65403](https://github.com/microsoft/TypeScript/pull/65403) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**Add a false path for a falsy, non\-nullish left operand of \`??\`**

*Fix nullish-coalescing control-flow analysis to track falsy, non-nullish left operands and correctly model branching, narrowing, and unreachable code.*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **typescript-automation[bot]** assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#65406](https://github.com/microsoft/TypeScript/pull/65406) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Publish PR builds to npm for installation and the Playground**

*Restore the GitHub Actions workflow to publish PR builds to npm, enabling installation and Playground access for TS7 packages.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65407](https://github.com/microsoft/TypeScript/pull/65407) (Closed, `Domain: Performance`, `For Uncommitted Bug`, **andrewbranch**)

**Encode LSP messages directly instead of via MarshalJSON**

*Update lsproto.Message to encode directly via MarshalJSONTo, reducing redundant copying and validation while preserving identical JSON output and improving performance.*

 * created by **hood**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/65407#issuecomment-6746781790) **jakebailey** said "Er, well, CLA"
 * [today](https://github.com/microsoft/TypeScript/pull/65407#issuecomment-6746870499) **hood** said "@microsoft-github-policy-service agree"
 * **jakebailey** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/pull/65407#issuecomment-6747527692) **hood** mentioned having another quality-of-life improvement involving auto-import warm-up cancellation during typing and asked whether submitting the work would be welcome
 * [today](https://github.com/microsoft/TypeScript/pull/65407#issuecomment-6747560387) **jakebailey** said "As first impressions go, you win, so, please do send more 😄 "
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65408](https://github.com/microsoft/TypeScript/pull/65408) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Collect garbage before writing allocation profiles**

*Ensure garbage collection runs before writing allocation profiles to prevent substantial sample loss and incomplete profiling data.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65408#issuecomment-6747182921) **andrewbranch** asked whether the profile showed data only up to, rather than since, the last GC
 * [today](https://github.com/microsoft/TypeScript/pull/65408#issuecomment-6747276642) **jakebailey** said "Oh, yes, I accidentally flipped that wording "
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65409](https://github.com/microsoft/TypeScript/pull/65409) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Add flow path for a falsy, non\-nullish left operand of \`??\` and \`??=\`**

*Add flow analysis for falsy, non-nullish operands of ?? and ??= to prevent false reachability errors and incorrect narrowing.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `Author: Team`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6751861105) **RyanCavanaugh** said "@copilot 🚲"
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6751887408) **Copilot** asked for clarification about whether the 🚲 emoji meant addressing the earlier review findings
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6752443527) **RyanCavanaugh** said "@copilot do another "cycle" of work on this - you have high-priority comments, and failing CI!"
 * [today](https://github.com/microsoft/TypeScript/pull/65409#issuecomment-6753030269) **Copilot** added missing compiler baselines and regression cases, fixed reachability and optional-chain routing issues, and reported successful validation while noting that CodeQL was skipped due to database size limits

### [Issue microsoft/TypeScript#65410](https://github.com/microsoft/TypeScript/issues/65410) (Open, `Needs Investigation`, **andrewbranch**)

**Auto\-import warm\-up restarts from scratch on every keystroke while typing**

*Auto-import cache warm-up restarts and discards progress on every keystroke, causing excessive CPU usage and delayed completion indexing.*

 * created by **hood**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65411](https://github.com/microsoft/TypeScript/pull/65411) (Open, `Domain: Performance`, `For Uncommitted Bug`)

**Reuse diagnostics checker for semantic tokens of checked files**

*Reuse completed diagnostics checkers for semantic token requests to reduce redundant type inference and improve editor performance without changing checker ordering.*

 * created by **hood**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65411#issuecomment-6750576401) **jakebailey** warned that the approach was generally unsafe due to ordering issues and noted that #65064 aimed to address them comprehensively
 * [today](https://github.com/microsoft/TypeScript/pull/65411#issuecomment-6750883435) **hood** acknowledged that the guard was not generally safe because classification still created types and symbols, converted the change to a draft pending #65064, reported substantial performance gains if order independence landed, and offered an LSP typing harness for testing.
 * **jakebailey** added label `Domain: Performance`

### [PR microsoft/TypeScript#65412](https://github.com/microsoft/TypeScript/pull/65412) (Open, `Domain: Performance`, `For Uncommitted Bug`, **andrewbranch**)

**Keep extracted auto\-import packages across cancelled builds**

*Preserve completed auto-import package extractions across cancelled builds while invalidating stale results and coordinating concurrent extraction requests.*

 * created by **hood**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * **jakebailey** added label `Domain: Performance`
 * **typescript-automation[bot]** assigned to **andrewbranch**

### [Issue microsoft/TypeScript#65413](https://github.com/microsoft/TypeScript/issues/65413) (Open)

**Downlevel \`for \(this\.\#x of \.\.\.\)\` / \`for \(this\.\#x in \.\.\.\)\` emits \`\_\_classPrivateFieldGet\(\.\.\.\)\` as the loop target**

*Downlevel compilation incorrectly emits private-field getters as invalid for-in/for-of loop targets, causing generated JavaScript to fail parsing.*

 * created by **trackoor**

### [Issue microsoft/TypeScript#65414](https://github.com/microsoft/TypeScript/issues/65414) (Open)

**CommonJS emit gives an imported function the wrong \`this\` when the callee is wrapped**

*CommonJS emit incorrectly preserves the imported module object as `this` when an imported function call is wrapped in parentheses or expressions.*

 * created by **trackoor**

### [Issue microsoft/TypeScript#65415](https://github.com/microsoft/TypeScript/issues/65415) (Open, `Bug`)

**\`jsx: react\-jsxdev\` passes \`this\` to \`jsxDEV\` before \`super\(\)\` returns**

*The `react-jsxdev` transform passes `this` to `jsxDEV` before derived constructors call `super()`, unlike the correct `react-jsx` transform.*

 * created by **trackoor**

### [PR microsoft/TypeScript#65416](https://github.com/microsoft/TypeScript/pull/65416) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix PR package publishing**

*Fix PR package publishing by adding the Wasm repository link and granting permission for build report comment replies.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65417](https://github.com/microsoft/TypeScript/pull/65417) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Strip content mapper known extensions as part of moduleSuffixes lookups**

*Update moduleSuffixes resolution to strip known content-mapper extensions during lookups, correcting module resolution behavior.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#65418](https://github.com/microsoft/TypeScript/pull/65418) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use org\-local package feed in Pipelines**

*Switch Pipelines back to the organization-local package feed, using authenticated `npm pack` instead of `fetch` for VSIX tarballs.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65419](https://github.com/microsoft/TypeScript/pull/65419) (Open, `For Backlog Bug`)

**Infer \`RegExp\` for regular expression literals under \`isolatedDeclarations\`**

*Infer `RegExp` types for regular expression literals under `--isolatedDeclarations` to prevent unnecessary explicit annotation errors.*

 * created by **andriidrok1**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65419#issuecomment-6758596200) **andriidrok1** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/65419#issuecomment-6760263050) **jakebailey** said "I'm not sure why this issue was marked "help wanted"; this issue still requires discussion and has future implications "

### [PR microsoft/TypeScript#65420](https://github.com/microsoft/TypeScript/pull/65420) (Open, `For Backlog Bug`)

**Check super\(\) placement for parameter properties with native class fields**

*Ensure parameter-property constructors validate root-level super() placement with native class fields to prevent runtime errors and emit correct diagnostics.*

 * created by **DrSmoothl**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [PR microsoft/TypeScript#65421](https://github.com/microsoft/TypeScript/pull/65421) (Open, `For Uncommitted Bug`)

**Implement erasable enum annotations**

*Add erasable `: enum` annotations that provide nominal enum and member types for object literals while emitting unchanged JavaScript.*

 * created by **magic-akari**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65421#issuecomment-6758872793) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #60790. If you can get it accepted, this PR will have a better chance of being reviewed."

### [PR microsoft/TypeScript#65422](https://github.com/microsoft/TypeScript/pull/65422) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Disallow illegal 'timeZone' option in Temporal\.ZonedDateTime\.prototype\.toLocaleString \(\#64227\)**

*Disallow the illegal `timeZone` option in `Temporal.ZonedDateTime.prototype.toLocaleString` through stricter TypeScript typings.*

 * created by **mechazod**
 * (later) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Milestone Bug`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#65423](https://github.com/microsoft/TypeScript/pull/65423) (Closed, `For Backlog Bug`)

**Disallow private identifiers in JSX tag and attribute names \(\#65396\)**

*Disallow private identifiers beginning with `#` in JSX tag and attribute names by reporting syntax errors during parsing.*

 * created by **mechazod**
 * **typescript-automation[bot]** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#65424](https://github.com/microsoft/TypeScript/issues/65424) (Open)

**Native API: expose inferred type arguments of a resolved signature**

*Expose inferred type arguments for resolved signatures through the native synchronous and asynchronous TypeScript Checker APIs.*

 * created by **darkyeg**

### [Issue microsoft/TypeScript#65425](https://github.com/microsoft/TypeScript/issues/65425) (Open)

**References code lens missing on export default in the native language server**

*The native language server no longer shows references code lenses for identifiers in `export default` or `export =` assignments.*

 * created by **k1tbyte**

### [PR microsoft/TypeScript#65426](https://github.com/microsoft/TypeScript/pull/65426) (Open, `For Uncommitted Bug`)

**Show references code lens on export assignments in native language server**

*Show references code lenses for `export default` expressions and `export =` assignments in the native language server.*

 * created by **k1tbyte**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65426#issuecomment-6765369390) **k1tbyte** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65427](https://github.com/microsoft/TypeScript/pull/65427) (Open, `For Uncommitted Bug`)

**Fix downlevel emit for private names in for\-in/for\-of assignment targets**

*Fix downlevel emission of private-name and destructuring targets in for-in, for-of, and for-await loops by assigning through temporaries per iteration.*

 * created by **RealThanhNguyxn**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65428](https://github.com/microsoft/TypeScript/pull/65428) (Open, `Domain: Performance`, `For Backlog Bug`)

**Bound template literal expansion while computing base constraints**

*Bound template literal expansion during base-constraint computation to prevent excessive type creation and memory usage for large recursive conditional types.*

 * created by **Keviniscool-boy**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65428#issuecomment-6771780522) **Keviniscool-boy** said "@microsoft-github-policy-service agree"

