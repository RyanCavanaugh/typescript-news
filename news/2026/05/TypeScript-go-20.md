# Report for 2026-05-20 (Wednesday, May 20th, 2026)

18 different users commented on 42 different issues.

## Recommended Actions

 * Response Recommended
    * @Netail asked for clarification on expected behavior and if this was different in earlier TypeScript in [microsoft/TypeScript-go#4002](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4500734557)
    * @Netail asked if using React types should throw an unknown element error instead of resolving via the JSX namespace in [microsoft/TypeScript-go#4002](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4502028391)
    * @rchl confirmed that @typescript/native-preview@7.0.0-dev.20260512.1 works correctly in [microsoft/TypeScript-go#4010](https://github.com/microsoft/TypeScript-go/issues/4010#issuecomment-4502313040)

## Activity Summary

### [PR microsoft/TypeScript-go#1301](https://github.com/microsoft/TypeScript-go/pull/1301) (Open)

**Enable pre/post emit diagnostic consistency tests**

*Enable pre/post emit diagnostic consistency tests after triaging newly surfaced test failures.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#2565](https://github.com/microsoft/TypeScript-go/pull/2565) (Open)

**Experiment with emulating typing within editor in fourslash tests**

*Experiment with emulating typing in Corsa's fourslash tests like Strada to improve tests despite diagnostic errors and timeouts.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#2602](https://github.com/microsoft/TypeScript-go/pull/2602) (Open)

**feat: comprehensive Type Hierarchy LSP support**

*Adds comprehensive LSP-based Type Hierarchy support in TypeScript language service for navigating class, interface, and type alias supertypes and subtypes.*

 * created by **kbrilla**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#2908](https://github.com/microsoft/TypeScript-go/pull/2908) (Open, **DanielRosenwasser**, **Copilot**)

**Add regression test for inlay hints crash on reparsed nodes \(\#2460\)**

*Add a regression test to ensure computing inlay hints on reparsed AST nodes in a JS module.exports function prevents panics.*

 * (1 month ago) **jakebailey** reopened the issue
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2908#issuecomment-4403509887) **DanielRosenwasser** said "@copilot try building and fix and build errors."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2908#issuecomment-4403591216) **Copilot** fixed the build error by replacing bool true with core.TSTrue, adding the core import, and updating the baseline to reflect the correct output after the crash fix
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3228](https://github.com/microsoft/TypeScript-go/pull/3228) (Open, **DanielRosenwasser**, **Copilot**)

**Track file extension in LSP request failure telemetry**

*Include an optional fileExtension field in LSP request failure telemetry to capture the affected file type.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3228#issuecomment-4156546121) **DanielRosenwasser** said "@copilot+claude-sonnet-4.6 merge from main and resolve conflicts"
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3228#issuecomment-4156638191) **Copilot** merged from main and resolved two conflicts in server.go
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3277](https://github.com/microsoft/TypeScript-go/pull/3277) (Open, **DanielRosenwasser**, **Copilot**)

**Implement "find file references"**

*Implement cross-project 'find file references' for JS/TS in VS Code by adding a custom LSP request and core reference logic.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3309](https://github.com/microsoft/TypeScript-go/pull/3309) (Open)

**Don't strip release binaries**

*Disable stripping of release binaries to retain debug symbols for easier debugging and tooling support despite larger package size*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3362](https://github.com/microsoft/TypeScript-go/pull/3362) (Open)

**Replace most ID usage with pointers**

*Propose replacing most ID fields with pointers in Go to leverage pointer comparability and reduce overhead.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4208295994) **jakebailey** said "@typescript-bot perf test this faster"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4208296421) **typescript-bot** reported starting jobs and provided build status and results links
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4208449180) **typescript-bot** provided the performance run results for the requested baseline vs pr comparison
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3397](https://github.com/microsoft/TypeScript-go/pull/3397) (Open)

**Use GHA runners instead of custom runners**

*Benchmarking shows GitHub-hosted runners run jobs roughly twice as slow as custom runners, questioning their necessity.*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3616](https://github.com/microsoft/TypeScript-go/pull/3616) (Open)

**API \`emit\` support to generate \.d\.ts / \.js files from sources**

*Expose compiler emit in TSGO API and TypeScript client to generate .js and .d.ts files using virtual FS*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4323425060) **pfumagalli** said "@microsoft-github-policy-service agree"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4418086735) **hegrec** asked if the PR would be merged and explained their use case for wrapping the emission pipeline with the virtual file system to capture d.ts content
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3616#issuecomment-4420025854) **pfumagalli** said "Resolved conflicts with upstream..."
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3627](https://github.com/microsoft/TypeScript-go/pull/3627) (Open)

**Runtime tracing, flight recording**

*Integrate Go runtime/trace support and flight recording into the VS Code extension similarly to pprof profiling.*

 * created by **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#3758](https://github.com/microsoft/TypeScript-go/issues/3758) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**File argument of \`@\` crashes CLI**

*Providing `@` with no file path to tsgo crashes the CLI with a “path "" is not absolute” panic.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3758#issuecomment-4461879124) **RyanCavanaugh** reported that the panic occurred for any file and that the path wasn't processed correctly before reading
 * (5 days ago) **RyanCavanaugh** assigned to **Copilot**, and unassigned **Copilot**
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3859](https://github.com/microsoft/TypeScript-go/pull/3859) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix panic when passing \`@\` response file argument to CLI**

*Normalize response file paths before reading to avoid tsgo panics when using '@' or relative '@filename' arguments.*

 * (5 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3859#issuecomment-4462641033) **RyanCavanaugh** said "@copilot address CR comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3859#issuecomment-4503444585) **RyanCavanaugh** said "@copilot resolve merge conflicts"
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3957](https://github.com/microsoft/TypeScript-go/issues/3957) (Closed, `possible improvement`, **jakebailey**, **Copilot**)

**Property names are quoted one level deep in inferred type**

*tsgo preserves quotes on one-level-deep property names in inferred types, unlike TypeScript 6.0 which strips them.*

 * **jakebailey** assigned to **jakebailey**
 * (2 days ago) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3965](https://github.com/microsoft/TypeScript-go/pull/3965) (Closed, **jakebailey**, **Copilot**)

**Normalize reused string\-literal property names to identifiers in declaration emit**

*Convert reused string-literal property names with valid identifier text into identifiers in declaration emit, excluding 'new' to preserve method signatures.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3996](https://github.com/microsoft/TypeScript-go/pull/3996) (Open)

**Extract tscInput tests to individual per\-scenario files with imperative edits to improve debuggability**

*Extract tscInput tests into individual scenario files with imperative edits, remove intra-test parallelism, simplify debugging while preserving original tests.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4496173212) **jakebailey** said "Not sure I like this, but at the very least I think the filenames shouldn't start with capital T"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4500666020) **weswigham** said "The filename shouldn't start with a capital T but the function should, go figure. Fixed."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4500751011) **weswigham** asked if others preferred keeping test duplication for debuggability or the new test format and offered to delete originals and the extraction script

### [PR microsoft/TypeScript-go#3997](https://github.com/microsoft/TypeScript-go/pull/3997) (Closed)

**Warn against AI botting**

*Port AI botting warning guidance from Strada’s contributing.md into the current project.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3998](https://github.com/microsoft/TypeScript-go/issues/3998) (Open, `bug`, **andrewbranch**)

**Intermittent \`tsgo \-\-build\` TS2345: \`paths\` \+ \`@types/\*\` conflict \(\`tsc\` accepts\)**

*tsgo --build randomly fails with TS2345 errors caused by conflicting path aliases and @types/react types while tsc builds and single-threaded tsgo builds consistently succeed.*

 * created by **adamnreed**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**, **Copilot**, and unassigned **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3998#issuecomment-4502016583) **RyanCavanaugh** described that trailing slashes in tsconfig-base.json paths triggered a race between module resolution parts
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, assigned to **andrewbranch**, and unassigned **RyanCavanaugh**, **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3998#issuecomment-4502041513) **RyanCavanaugh** said "@andrewbranch both Copilot PRs above look plausible but they can't both be right."

### [Issue microsoft/TypeScript-go#4000](https://github.com/microsoft/TypeScript-go/issues/4000) (Open, `enhancement`)

**Make typedef exporting explicit**

*Propose introducing a new @export JSDoc tag to explicitly mark exported typedefs and type re-exports in TypeScript 7*

 * created by **remcohaszing**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4000#issuecomment-4497729784) **ahejlsberg** rejected the suggestion to add new JSDoc features and recommended writing the code in TypeScript
 * **ahejlsberg** added label `enhancement`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4000#issuecomment-4507848992) **remcohaszing** noted the trade-offs between JavaScript and TypeScript and suggested issue #58250 as an alternative solution to type export dependency concerns

### [Issue microsoft/TypeScript-go#4002](https://github.com/microsoft/TypeScript-go/issues/4002) (Closed, `Domain: Editor`, `Needs More Info`)

**Image JSX type**

*The VS Code extension incorrectly treats the global Image constructor as a valid JSX element type.*

 * created by **Netail**
 * **Netail** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4500594338) **RyanCavanaugh** said "This is an error under ts-check. I'm not sure what else you want to happen here -- "should not be allowed" means what?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4500734557) **Netail** questioned the assignment of types to JSX elements, noting it gave a false impression and asked if this behavior differed from earlier TypeScript
 * [today](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4501370864) **nmain** explained how TypeScript transforms JSX elements into function calls and why type errors occur based on the JSX namespace definitions
 * [today](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4501903491) **RyanCavanaugh** questioned what the expected behavior was for go-to-definition and asked how to investigate a value as a JSX element
 * [today](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4502017852) **Netail** suggested throwing an "Unknown element" error when Image is used as a JSX element without importing a custom component
 * [today](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4502028391) **Netail** asked if using React types should throw an unknown element error instead of resolving via the JSX namespace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4502064685) **RyanCavanaugh** asked what 'throw' meant
 * [today](https://github.com/microsoft/TypeScript-go/issues/4002#issuecomment-4502074796) **Netail** said "nvm, same behaviour as pre-tsgo"
 * (today) **Netail** closed the issue

### [PR microsoft/TypeScript-go#4003](https://github.com/microsoft/TypeScript-go/pull/4003) (Open, **joj**, **Copilot**)

**Add VS hidden\-in\-editor tag for Unnecessary diagnostics and cover with manual fourslash tests**

*Enable Visual Studio hidden-in-editor tag for unnecessary diagnostics and add manual fourslash tests for both VS and non-VS scenarios.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **joj**

### [Issue microsoft/TypeScript-go#4004](https://github.com/microsoft/TypeScript-go/issues/4004) (Open, `duplicate`)

**Spurious "multiple properties with the same name" errors for unpaired surrogates**

*tsgo incorrectly reports duplicate property name errors for object literals using unpaired Unicode surrogate keys.*

 * created by **blickly**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4004#issuecomment-4502260136) **RyanCavanaugh** said "Same root cause as #3899"
 * **RyanCavanaugh** added label `duplicate`

### [Issue microsoft/TypeScript-go#4005](https://github.com/microsoft/TypeScript-go/issues/4005) (Open, `Domain: Editor`, `Needs More Info`)

**Native Preview returns no code actions for any TS diagnostic**

*TypeScript native preview on Remote-SSH shows diagnostics but no code actions for TS errors when using tsgo.*

 * created by **umbriquse**
 * **umbriquse** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4005#issuecomment-4502555182) **RyanCavanaugh** noted that TS7 lacked the full suite of code actions and requested feedback to prioritize which ones to re-implement
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4005#issuecomment-4502684407) **a-tarasyuk** said "It could be useful, for instance, if VS Code tracked which quick fixes are used most often (if any 😄 )."

### [PR microsoft/TypeScript-go#4006](https://github.com/microsoft/TypeScript-go/pull/4006) (Closed)

**Bump fast\-uri to 3\.1\.2**

*Upgrade fast-uri to 3.1.2 to address high-severity CVE-2026-6321 and CVE-2026-6322*

 * created by **lucygramley**

### [PR microsoft/TypeScript-go#4007](https://github.com/microsoft/TypeScript-go/pull/4007) (Open)

**Accepted symbol baselines**

*Establish accepted symbol baselines before addressing bugs and investigations in a later pull request.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4008](https://github.com/microsoft/TypeScript-go/pull/4008) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix intermittent TS2345 with paths \+ @types/\* conflict in concurrent builds**

*Concurrent tsgo builds intermittently fail TS2345 because a race in the packageJsonInfoCache causes path aliases to resolve to @types packages.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4008#issuecomment-4502040125) **Copilot** added a compiler test for path alias trailing slash conflict with @types/react and noted existing unit tests reproducing the cache race
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4009](https://github.com/microsoft/TypeScript-go/pull/4009) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix package identity for paths\-mapped directory resolutions**

*Normalize and tag paths-mapped directory resolutions with package identities to eliminate inconsistent module loading and intermittent TS2345 errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4010](https://github.com/microsoft/TypeScript-go/issues/4010) (Open, `Needs Investigation`, **gabritto**)

**\[lsp\] Hover verbosity fails after increasing verbosity**

*Toggling hover verbosity levels in LSP-tsgo for JobsStateToColor causes canIncreaseVerbosity to be omitted from server responses.*

 * created by **rchl**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4010#issuecomment-4501974533) **jakebailey** said "Can you try before https://github.com/microsoft/typescript-go/commit/49f210f36d71b3160a7c586990a73d10a81f157d?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4010#issuecomment-4502313040) **rchl** said "@typescript/native-preview@7.0.0-dev.20260512.1 works correctly."
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**

### [Issue microsoft/TypeScript-go#4011](https://github.com/microsoft/TypeScript-go/issues/4011) (Open, `bug`, **weswigham**)

**Property names from JSDoc types not escaped in declaration files**

*Declaration files generated by tsgo fail to quote hyphenated JSDoc property names, leading to syntax errors.*

 * created by **tidychips**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4012](https://github.com/microsoft/TypeScript-go/pull/4012) (Closed, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Quote invalid JSDoc property names in declaration emit**

*Declaration emit now quotes hyphenated JSDoc typedef property names as string literals in generated .d.ts files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4012#issuecomment-4502751367) **RyanCavanaugh** asked Copilot to explore JSDoc constructs for non-identifier names requiring cleanup and report findings without pushing code
 * **RyanCavanaugh** assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4012#issuecomment-4502838280) **Copilot** explored JSDoc constructs and reported that property-signature fix covers @property cases, but typedef/callback name sanitization and hyphenated qualified subproperty tags remain unhandled
 * [today](https://github.com/microsoft/TypeScript-go/pull/4012#issuecomment-4502875187) **RyanCavanaugh** said "@copilot ok, add testcases for each of those setups and fix them as well"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4012#issuecomment-4503058837) **Copilot** added test coverage for hyphenated/backquoted typedef properties, typedef/callback names, callback parameter names, qualified subproperty tags, and template names; and improved declaration emit to sanitize and quote paths
 * [today](https://github.com/microsoft/TypeScript-go/pull/4012#issuecomment-4503487242) **RyanCavanaugh** criticized the validity of the Copilot test and recommended reverting source changes, writing proper tests to demonstrate the issue, and then fixing the bug with a fresh approach
 * [today](https://github.com/microsoft/TypeScript-go/pull/4012#issuecomment-4503596126) **Copilot** addressed the flawed parser/nodebuilder changes and declaration-transformer fix in commits 79ff5800 and 3f849d26, removed invalid nested-property cases, preserved regression coverage, and confirmed tests passed
 * [later](https://github.com/microsoft/TypeScript-go/pull/4012#issuecomment-4510092605) **RyanCavanaugh** said "Going to clean this up in a subsequent PR"
 * (later) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4012#issuecomment-4510096546) **RyanCavanaugh** said "Now at #4021"

### [PR microsoft/TypeScript-go#4013](https://github.com/microsoft/TypeScript-go/pull/4013) (Closed)

**Fix panic when bare '@' is passed as a CLI argument**

*Add a check to return an error instead of panicking when the '@' response-file argument has no filename.*

 * created by **RonGamzu**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4013#issuecomment-4503035529) **RonGamzu** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4013#issuecomment-4503441024) **RyanCavanaugh** said "Did you read the comments on the issue? https://github.com/microsoft/typescript-go/issues/3758#issuecomment-4461879124"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4013#issuecomment-4507073660) **RonGamzu** said "@RyanCavanaugh I’ve read it over and made a few more edits and adjustments. "
 * [later](https://github.com/microsoft/TypeScript-go/pull/4013#issuecomment-4509208640) **RyanCavanaugh** said "Already addressed in #3859"
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4014](https://github.com/microsoft/TypeScript-go/issues/4014) (Open, `Domain: Declaration Emit`, `Domain: Build Mode`, `Needs More Info`, `Needs Investigation`)

**\`DeepCloneNode\` allocation runaway \(44 GB / 308 s\) for recursive tagged\-tuple type alias**

*tsgo’s DeepCloneNode allocation spikes (44 GB over 308 s) when type-checking a recursive variadic tuple alias with a .tsbuildinfo file.*

 * created by **ebramanti**

### [PR microsoft/TypeScript-go#4015](https://github.com/microsoft/TypeScript-go/pull/4015) (Open)

**Do not emit declaration files when they contain a declaration emit error**

*Prevent TypeScript from emitting declaration files when declaration emit errors occur.*

 * created by **weswigham**

### [Issue microsoft/TypeScript-go#4016](https://github.com/microsoft/TypeScript-go/issues/4016) (Open)

**@fileoverview breaks @jsx comments**

*tsgo does not honor @jsx annotations in @fileoverview comments, using the default JSX factory instead of the specified one.*

 * created by **blickly**

### [Issue microsoft/TypeScript-go#4017](https://github.com/microsoft/TypeScript-go/issues/4017) (Open, `Domain: Editor`, `possible improvement`)

**Extension does not respect \`js/ts\.locale\`**

*The extension ignores js/ts.locale settings and always displays English error messages because it does not send locale to the server.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4503923191) **jakebailey** said "The LSP client does this automatically; I assume the old server has this as it was the only way to do it. Does anyone actually set this? (Will have to make sure undefined works at least)"
 * (today) **DanielRosenwasser** added label `possible improvement`, removed label `bug`, set milestone to `Possible Improvement`, and unassigned **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4017#issuecomment-4505111440) **DanielRosenwasser** noted that the feature automatically takes effect when using "Configure Display Language" and suggested gathering feedback before considering overrides

### [PR microsoft/TypeScript-go#4018](https://github.com/microsoft/TypeScript-go/pull/4018) (Closed)

**Quote invalid property names in declaration emit**

*Declaration emit quotes invalid identifier property names and includes a regression test for JSDoc typedef properties like data-test-name and aria-label*

 * created by **kiwigitops**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4018#issuecomment-4509189820) **RyanCavanaugh** directed the contributor to review the AI assistance guidelines and warned that opening a duplicate PR was a red flag
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4019](https://github.com/microsoft/TypeScript-go/issues/4019) (Open, `Crash`)

**Crash on file rename \+ \`workspace/didChangeWatchedFiles\`, \\w \`composite\` option enabled**

*The TypeScript language server crashes with a nil pointer panic when processing a file rename alongside workspace/didChangeWatchedFiles in composite-enabled projects.*

 * created by **mpal9000**
 * **mpal9000** added label `Crash`

### [PR microsoft/TypeScript-go#4020](https://github.com/microsoft/TypeScript-go/pull/4020) (Open)

**fix\(4016\): skip unknown pragmas**

*Modify the parser to skip unrecognized pragmas instead of producing errors.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#4021](https://github.com/microsoft/TypeScript-go/pull/4021) (Closed)

**Rewrite invalid identifiers originating in JSDoc**

*Add sanitization helpers to the declaration transformer to rewrite invalid JSDoc identifiers and property names into valid TypeScript keys.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#717](https://github.com/microsoft/TypeScript-go/pull/717) (Open)

**Enable staticcheck**

*Enabling the staticcheck linter raises linting time dramatically, prompting performance investigation and reporting.*

 * created by **jakebailey**
 * [28 weeks ago](https://github.com/microsoft/TypeScript-go/pull/717#issuecomment-3475151354) **jakebailey** said "Perf of this is still pretty bad. A lint run on main in CI takes about 30s, but on this branch takes 4m44s."
 * **RyanCavanaugh** added to milestone `Possible Improvement`

