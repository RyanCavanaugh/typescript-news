# Report for 2026-10-31 (Saturday, October 31st, 2026)

17 different users commented on 31 different issues.

## Recommended Actions

 * Response Recommended
    * @ismailkarsli requested to consider supporting the simple sql`select ${1}` syntax in [microsoft/TypeScript#33304](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-6546795334)
    * @trevorparscal noted that all SvelteKit 3 projects are affected due to the alias change in [microsoft/TypeScript#44564](https://github.com/microsoft/TypeScript/issues/44564#issuecomment-6548215219)
    * @aetherxeg-source asked for contract clarification regarding entry lifetimes in SyncMap resurrection in [microsoft/TypeScript#65072](https://github.com/microsoft/TypeScript/pull/65072#issuecomment-6551598550)
    * @GoodbyeNJN provided detailed findings about duplicate inlay hints and a confirmation of the root cause in [microsoft/TypeScript#65092](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6560928348)

## Activity Summary

### [Issue microsoft/TypeScript#33304](https://github.com/microsoft/TypeScript/issues/33304) (Open, `Suggestion`, `In Discussion`)

**Type safety with \`TemplateStringsArray\` and tag functions**

*Enhance TypeScript’s TemplateStringsArray interface to accept generic types, enabling type-safe tagged template functions.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-2758397463) **martaver** asked to reconsider the previously shelved PR #45310 given new developments like typescript-go's announcement
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-2914501602) **justinfagnani** described a use case for Zod 4's template literal types and suggested supporting template literal syntax for z.templateLiteral
 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-3807802305) **char** proposed a patch to the TypeScript type checker enabling Zod-like const template literal schema inference and asked if it would be welcome as a pull request
 * [today](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-6546795334) **ismailkarsli** described a TypeScript SQL parsing library and requested support for the simple sql`select ${1}` syntax instead of the current workaround

### [Issue microsoft/TypeScript#44564](https://github.com/microsoft/TypeScript/issues/44564) (Open, `Suggestion`, `Experience Enhancement`)

**Support go\-to\-definition on tsconfig mapped paths for non\-source files**

*Add go-to-definition support for non-source files referenced via tsconfig.json path mappings.*

 * (5.3 years ago) **RyanCavanaugh** added labels `Experience Enhancement`, `Suggestion`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/44564#issuecomment-6548215219) **trevorparscal** said "This affects all SvelteKit 3 projects (so, TS6 here since TS7 isn't yet supported there) since the $lib alias has been replaced with a #lib subpath import."

### [Issue microsoft/TypeScript#64757](https://github.com/microsoft/TypeScript/issues/64757) (Open, `Needs Investigation`, **ahejlsberg**)

**Regression in 7\.1 \(\#64553\): R inferred as unknown through a generic type alias call signature with a nested same\-type argument**

*A TypeScript 7.1 regression makes R infer as unknown rather than Req in a nested generic type alias call signature.*

 * **RyanCavanaugh** added label `Needs Investigation`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6319872131) **kennysarnoski-jarvis** ran the repro locally and confirmed regression TS2571 on nightly builds, described inference failure conditions and downstream tool impact
 * [today](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6544123377) **artile** provided a third real-world example highlighting a TypeScript inference failure in nested generic interfaces, added two distinguishing details, and demonstrated which 7.1.0-dev versions failed using code, tsconfig, and a results table
 * [today](https://github.com/microsoft/TypeScript/issues/64757#issuecomment-6546851553) **kennysarnoski-jarvis** described the root cause of the type inference issue, opened issue #65077 with a fix and a compiler test, and confirmed that it resolves the previously reported repro cases

### [PR microsoft/TypeScript#65003](https://github.com/microsoft/TypeScript/pull/65003) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Report process CPU time in extended diagnostics**

*Add reporting of process CPU time in extended diagnostics to capture actual CPU usage by the process.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6483489524) **typescript-automation[bot]** reported the requested perf run results including a detailed comparison table
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6483634710) **typescript-automation[bot]** provided the requested performance run results
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6483652625) **jakebailey** said "Hm, benchmarker does not understand this"
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6551774401) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6551775234) **typescript-automation[bot]** announced starting jobs and provided build status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/65003#issuecomment-6552261464) **typescript-automation[bot]** posted perf run results showing no significant changes between baseline and PR across metrics like errors, symbols, types, and memory usage

### [PR microsoft/TypeScript#65064](https://github.com/microsoft/TypeScript/pull/65064) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] fully order independent type checking**

*Make the type checker fully order independent by replacing ID-based caching with content-based memos and order-variant tests.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6533497319) **typescript-automation[bot]** reported user test results with new TypeScript errors and requested review
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6533969647) **typescript-automation[bot]** provided the requested performance run results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6534283900) **jakebailey** said "Well, that's a little bleak."
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6546210308) **jakebailey** said "Not sure why top400 didn't come back either"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6548606063) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6548606977) **typescript-automation[bot]** said "Hey @jakebailey, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6548785435) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6548786499) **typescript-automation[bot]** posted build job status updates
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6549163012) **typescript-automation[bot]** reported DT test results with branch-only errors in d3-selection due to TypeScript compile errors
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6549239542) **typescript-automation[bot]** reported new TS7023 errors for implicit any return types in functions '_rebuild' and 'recur' in SchemaAST.ts during user tests comparison
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6549401685) **typescript-automation[bot]** posted the requested performance run results including metrics for errors, symbols, types, and memory usage
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6549499867) **jakebailey** said "Now we're talking "
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6549793751) **typescript-automation[bot]** reported tsc run results comparing baseline and pr for top 400 repos and highlighted build failures and errors in two projects
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6551357815) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6551358966) **typescript-automation[bot]** initiated CI jobs and posted status updates
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6551720359) **typescript-automation[bot]** reported DT test results with branch-only errors in d3-selection due to TypeScript compile errors
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6551788903) **typescript-automation[bot]** reported new TS7023 errors for implicit any return types in SchemaAST.ts when comparing baseline and pr
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6551896318) **typescript-automation[bot]** informed @jakebailey of the requested performance run results and presented comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/65064#issuecomment-6552290072) **typescript-automation[bot]** reported tsc build results for the top 400 repos, noted an interesting change, and provided failure details for cheaper-inference/OmniRoute

### [PR microsoft/TypeScript#65072](https://github.com/microsoft/TypeScript/pull/65072) (Closed, `For Uncommitted Bug`)

**fix\(65071\): resurrect dirty\.SyncMap entries after Delete in LoadOrStore**

*Resurrect deleted dirty.SyncMap entries in LoadOrStore to prevent nil returns after tombstones.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65072#issuecomment-6551598550) **aetherxeg-source** proposed a test for stale-reference concerns when reusing the same SyncMapEntry after deletion and requested clarification of the intended entry lifetime contract

### [PR microsoft/TypeScript#65073](https://github.com/microsoft/TypeScript/pull/65073) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Compute CommonJSModuleIndicator in the parser**

*Move CommonJSModuleIndicator computation from the binding phase into the parser to enable earlier, consistent file reuse without race conditions.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/65073#issuecomment-6540223174) **jakebailey** said "Uh. Interesting"
 * [today](https://github.com/microsoft/TypeScript/pull/65073#issuecomment-6548778038) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65073#issuecomment-6548778973) **typescript-automation[bot]** announced starting jobs with status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/65073#issuecomment-6549314978) **typescript-automation[bot]** posted the requested perf run results with a detailed comparison report for tsc metrics

### [Issue microsoft/TypeScript#65076](https://github.com/microsoft/TypeScript/issues/65076) (Closed, `Bug`)

**Native tsc reads a literal U\+FFFD in a regex character class as 0xEF \(false TS1517 / TS1516\)**

*TypeScript 7's native tsc misreads a literal U+FFFD in regex character classes as 0xEF, causing false TS1517/TS1516 errors.*

 * created by **evanmarrone**

### [PR microsoft/TypeScript#65077](https://github.com/microsoft/TypeScript/pull/65077) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**Keep inferring from type arguments when the same generic type is nested inside them**

*Generic type inference drops inner parameters for nested identical generics due to a recursion guard, and this PR fixes it by bypassing recursion checks for type-argument inference.*

 * created by **kennysarnoski-jarvis**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/65077#issuecomment-6546968750) **kennysarnoski-jarvis** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#65078](https://github.com/microsoft/TypeScript/issues/65078) (Open, `Bug`)

**panic: strings: negative Repeat count with \-\-pretty; TS8010 span for an empty type annotation in JS ends before it starts**

*TypeScript 7.x crashes with a negative Repeat count panic when pretty-printing a TS8010 error for an empty JS type annotation.*

 * created by **THEtheChad**

### [Issue microsoft/TypeScript#65079](https://github.com/microsoft/TypeScript/issues/65079) (Open, `Bug`)

**panic: nil pointer dereference in CreateDiagnosticForNodeInSourceFile for a malformed "files" array in tsconfig\.json**

*TypeScript 7.x crashes with a nil pointer dereference on a malformed 'files' array in tsconfig.json instead of reporting an error.*

 * created by **THEtheChad**

### [PR microsoft/TypeScript#65080](https://github.com/microsoft/TypeScript/pull/65080) (Closed, `For Backlog Bug`)

**fix\(65076\): treat literal U\+FFFD as a real rune in regex classes**

*Modify regex literal parsing to recognize real U+FFFD runes in character classes instead of misclassifying them as decode errors.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65081](https://github.com/microsoft/TypeScript/pull/65081) (Closed, `For Backlog Bug`)

**fix\(65078\): keep empty spans for missing nodes when skipping trivia**

*Preserve empty spans for missing nodes when skipping trivia to avoid negative-length diagnostic ranges and crashes.*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65082](https://github.com/microsoft/TypeScript/pull/65082) (Open, `For Backlog Bug`)

**fix\(tsoptions\): don't panic on empty files when AST node is missing**

*Fallback to a compiler diagnostic to avoid panics when tsconfig.json has an empty files array without an AST node*

 * created by **timurzvural**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65083](https://github.com/microsoft/TypeScript/issues/65083) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**API: \`tsc\.exe\` opens a visible console window on Windows when the parent process has no console**

*On Windows, using the TypeScript sync API from a GUI process unexpectedly opens a visible tsc.exe console window.*

 * created by **SegaraRai**

### [Issue microsoft/TypeScript#65084](https://github.com/microsoft/TypeScript/issues/65084) (Open)

**Content mappers: saving a \`watchedFiles\` file that is open in the editor never re\-runs \`openProject\` \(stale types until the language server is restarted\)**

*Saving a watched config file fails to refresh content mappers, resulting in stale types until the server restarts.*

 * created by **toiroakr**

### [PR microsoft/TypeScript#65085](https://github.com/microsoft/TypeScript/pull/65085) (Closed, `Author: Team`, `For Uncommitted Bug`)

**Update localization files**

*Update localization files and regenerate corresponding runtime artifacts.*

 * created by **typescript-automation[bot]**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65086](https://github.com/microsoft/TypeScript/issues/65086) (Open)

**Implicit Function Parameter Types won't Work in JavaScript**

*With ts-check enabled, JSDoc parameter types aren’t inferred for functions assigned to object or class members at the top level.*

 * created by **neurolag**
 * [later](https://github.com/microsoft/TypeScript/issues/65086#issuecomment-6556572911) **neurolag** said "Perhaps, this is related to #44640"

### [Issue microsoft/TypeScript#65087](https://github.com/microsoft/TypeScript/issues/65087) (Open)

**Native API: formatDiagnosticsWithColorAndContext drops related information without a file location**

*The native formatDiagnosticsWithColorAndContext API omits related diagnostic messages lacking file locations.*

 * created by **emerardd**

### [PR microsoft/TypeScript#65088](https://github.com/microsoft/TypeScript/pull/65088) (Open, `For Backlog Bug`)

**Reject pending async API requests when the connection closes**

*Drain complete responses and reject any remaining pending asynchronous API requests when the connection closes.*

 * created by **wsjwu58-cmd**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65088#issuecomment-6557153358) **wsjwu58-cmd** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#65089](https://github.com/microsoft/TypeScript/issues/65089) (Open, `Bug`)

**Async API requests remain pending after the RPC connection closes**

*Asynchronous API requests via the RPC client remain pending and never settle after the connection closes.*

 * created by **wsjwu58-cmd**

### [Issue microsoft/TypeScript#65090](https://github.com/microsoft/TypeScript/issues/65090) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Native compiler API resolves a default\-parameter reference to a body function binding**

*The TypeScript native compiler API incorrectly resolves default parameter references to an inner function declaration instead of the outer variable.*

 * created by **CaliLuke**

### [PR microsoft/TypeScript#65091](https://github.com/microsoft/TypeScript/pull/65091) (Closed, `For Milestone Bug`, **RyanCavanaugh**)

**Fill the config cycle into the TS18000 circularity message**

*Include the chain of configuration file paths causing a circular extends error in the TS18000 diagnostic message*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65091#issuecomment-6560560316) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#65092](https://github.com/microsoft/TypeScript/issues/65092) (Open, `Suggestion`, `Declined`)

**Feature Request: Allow Content Mappers to opt\-in to transforming files end in built\-in extensions**

*Enable content mappers to opt in to transforming built-in TypeScript/JavaScript file extensions with scoped applicability and avoid duplicate LSP registrations.*

 * created by **GoodbyeNJN**
 * [later](https://github.com/microsoft/TypeScript/issues/65092#issuecomment-6560928348) **GoodbyeNJN** described a local experiment bypassing extension checks that led to duplicate inlay hints for .ts files and confirmed the cause by filtering out built-in JS/TS extensions

