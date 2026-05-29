# Report for 2026-05-28 (Thursday, May 28th, 2026)

7 different users commented on 50 different issues.

## Recommended Actions

 * Response Recommended
    * @anotheri asked to take a look at details in a linked issue in [microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4574995897)
    * @Kelpy2004 asked whether @jakebailey was the right person to review the changes in [microsoft/TypeScript-go#4074](https://github.com/microsoft/TypeScript-go/pull/4074#issuecomment-4575919369)

## Activity Summary

### [PR microsoft/TypeScript-go#3172](https://github.com/microsoft/TypeScript-go/pull/3172) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow in instantiateTypeWorker with recursive intersections \(TypeScript\#63269\)**

*Enforce the recursion depth limit in instantiateTypeWorker by setting instantiationCount high to avoid stack overflows in recursive intersections.*

 * created by **Copilot**
 * (10 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3172#issuecomment-4567420125) **RyanCavanaugh** said "Not a regression and I'm not 100% on this fix"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3354](https://github.com/microsoft/TypeScript-go/pull/3354) (Open, **jakebailey**, **Copilot**)

**Fix panic in declaration emit for named CommonJS exports from \.cjs files**

*Add missing diagnostic context in transformCommonJSExport to prevent declaration emit panics for named CommonJS exports in .cjs files.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3375](https://github.com/microsoft/TypeScript-go/pull/3375) (Open, **DanielRosenwasser**, **Copilot**)

**Fix index out of bounds panic in setLastNonTriviaPosition for empty strings**

*Add a bounds check to the trailing whitespace loop in setLastNonTriviaPosition to prevent panics on empty strings*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3379](https://github.com/microsoft/TypeScript-go/pull/3379) (Open, **DanielRosenwasser**, **Copilot**)

**Fix panic in transformCommonJSExport for named non\-default exports**

*Add missing symbol accessibility diagnostic for named non-default CommonJS exports to avoid declaration emit panics and include a test*

 * **Copilot** assigned to **DanielRosenwasser**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3379#issuecomment-4425665109) **jakebailey** said "@copilot+claude-opus-4.7 If you undo your fixes, your test doesn't actually crash."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3379#issuecomment-4425736135) **Copilot** confirmed that reverting the fixes caused the test to pass without crashing, tested various scenarios without reproducing the panic, removed the speculative pre-check, retained the structural fix, adjusted the test to a sanity check, and requested a reproduction case that crashes
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3405](https://github.com/microsoft/TypeScript-go/issues/3405) (Closed, `Domain: Editor`, **ahejlsberg**)

**JSDoc disapprears after type calculation**

*Hovering over a parameter from an intersection type no longer shows its JSDoc comment after TS type calculation.*

 * (6 days ago) **ahejlsberg** assigned to **ahejlsberg**, and unassigned **jakebailey**, **Copilot**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3408](https://github.com/microsoft/TypeScript-go/pull/3408) (Open, **jakebailey**, **Copilot**)

**Fix JSDoc disappearing on destructured parameters from intersection types**

*Ensure JSDoc comments appear on destructured parameters from intersection types by falling back to symbol declarations when ValueDeclaration is missing.*

 * created by **Copilot**
 * (6 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3432](https://github.com/microsoft/TypeScript-go/pull/3432) (Open)

**Enable allowJs when inferred project has root JS files**

*Automatically enable allowJs for inferred projects with root JS files and introduce a @noDefaultOpen option to prevent default file openings in fourslash tests.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271133192) **jakebailey** said "We actually do not yet support client setting any compiler options."
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271642537) **andrewbranch** confirmed that session.compilerOptionsForInferredProjects was never set in real VS Code and that project.go default options always included --allowJs
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3432#issuecomment-4271924781) **jakebailey** mentioned that the issue wasn't urgent, said they would investigate adjusting tests to use defaults, and noted the need to support the VS Code options for those defaults
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3592](https://github.com/microsoft/TypeScript-go/pull/3592) (Open, **DanielRosenwasser**, **Copilot**)

**Fix CommonJS emit of export declarations in nested statement contexts**

*CommonJS transformer now properly strips and transpiles export modifiers on nested variable statements in labeled and conditional blocks.*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Open)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4492416380) **DanielRosenwasser** asked why the user was tracing tsconfig.json resolution for paths and reiterated that the pattern list wasn't supposed to be passed
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4527660962) **kuishou68** added a new test file internal/core/pattern_test.go covering exact versus wildcard orderings, longer versus shorter prefix wildcard precedence, no-match behavior, and single/multiple wildcard match scenarios with self-documenting assertions
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4527804370) **kuishou68** said "I have added the test cases as requested. Could you please take another look?"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3630](https://github.com/microsoft/TypeScript-go/pull/3630) (Open, **DanielRosenwasser**, **Copilot**)

**Fix formatting failure when whitespace\-only line exists between single\-line comments**

*A whitespace-only line between single-line comments causes the formatter to produce overlapping delete edits due to unguarded startPos updates.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4331257440) **Copilot** reported the fix in commit 22e4165a by replacing the compiler test with a fourslash formatting test
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4400770306) **DanielRosenwasser** said "@copilot investigate and make sure we are testing variations of TrimTrailingWhitespace for this"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4400890083) **Copilot** added a test variant that disables TrimTrailingWhitespace and verified whitespace preservation; confirmed both variations pass
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3663](https://github.com/microsoft/TypeScript-go/pull/3663) (Open)

**Fix hover JSDoc for mapped type properties**

*Fix hover tooltips to correctly display JSDoc comments for mapped type properties*

 * created by **Andarist**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3690](https://github.com/microsoft/TypeScript-go/pull/3690) (Open)

**fix: handle symlink workspace roots in project reference redirects**

*Improve project reference redirects to correctly handle symlinked workspace roots.*

 * created by **Zzzen**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3726](https://github.com/microsoft/TypeScript-go/pull/3726) (Open, **DanielRosenwasser**, **Copilot**)

**Preserve original stack traces in cross\-project panic handling**

*Add a PanicWithStack wrapper to record and rethrow the original panic stack trace in cross-project worker recovery.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4391869776) **Copilot** demonstrated telemetry stack trace before and after the fix, preserved original crash site, and added a baseline test
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4392374682) **DanielRosenwasser** asked whether duplicate parts of the stack trace could be omitted
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-4392475333) **Copilot** fixed NewPanicWithStack to strip recovery infrastructure frames from the captured stack to prevent duplication in telemetry output
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3729](https://github.com/microsoft/TypeScript-go/pull/3729) (Open, **RyanCavanaugh**, **Copilot**)

**Remove extraneous \`declare\` in \.d\.ts output to better match strada**

*Strip redundant ambient declare modifiers from all .d.ts outputs to align with strada behavior.*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3738](https://github.com/microsoft/TypeScript-go/pull/3738) (Open, **gabritto**, **Copilot**)

**Implement pre\-emit/post\-emit diagnostic count mismatch detection \(TS\-1\)**

*Implement TS-1 diagnostic in Go test harness to detect and report mismatches between pre-emit and post-emit diagnostic counts.*

 * (3 weeks ago) **Copilot** assigned to **Copilot**, **gabritto**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3738#issuecomment-4400192625) **jakebailey** said "I think this is technically a dupe of #1301 but it's been a while so I think we don't need some of the fixes in that PR?"
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3765](https://github.com/microsoft/TypeScript-go/pull/3765) (Open, **jakebailey**, **Copilot**)

**Fix custom tsgo path: read from \`js/ts\.tsdk\.path\` unified setting**

*Support reading custom tsgo binary path from unified js/ts.tsdk.path setting with fallback to typescript.native-preview.tsdk.*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3771](https://github.com/microsoft/TypeScript-go/pull/3771) (Open, **RyanCavanaugh**, **Copilot**)

**Accept CJS export alias and element access pattern baseline diffs**

*Accept five baseline diffs reflecting Corsa’s correct export alias and element access handling over Strada’s mangled outputs.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3807](https://github.com/microsoft/TypeScript-go/pull/3807) (Open, **jakebailey**, **Copilot**)

**Fix stack overflow on circular reference after \`satisfies\`**

*Pass checkMode to skip assignability checks in satisfies expressions during serialization to prevent circular stack overflow*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4427875598) **jakebailey** said "@copilot+claude-opus-4.6 is this a porting bug? If not why doesn't Strada hit this?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4427900074) **Copilot** described the issue as a porting bug and explained why Strada didn’t hit it due to lacking the pseudochecker path, outlining the cyclic call sequence in the Go port
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4444350161) **weswigham** explained that the issue arose from creating a fresh node builder on each invocation rather than caching it, compared it to strada's behavior, and suggested caching a single node builder for intra-checker usage
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3834](https://github.com/microsoft/TypeScript-go/pull/3834) (Open)

**add localization for extension**

*Add localization support to the TypeScript VS Code extension by integrating non-English translation files and enabling pseudo-language testing.*

 * created by **iisaduan**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3842](https://github.com/microsoft/TypeScript-go/issues/3842) (Open, `bug`, **ahejlsberg**)

**Missing support for namespaces in JSDoc types**

*Reinstate nested JSDoc typedef namespace support in tsgo, as the .d.ts workaround breaks single-file typing workflows.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** added label `bug`, and removed label `Needs Investigation`

### [PR microsoft/TypeScript-go#3850](https://github.com/microsoft/TypeScript-go/pull/3850) (Open)

**Fixed CJS class expression exports emit anonymous constructor types**

*Exports of class expressions in CommonJS modules produce anonymous constructor types in the emitted output.*

 * created by **johnfav03**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3854](https://github.com/microsoft/TypeScript-go/pull/3854) (Open)

**check that all files in \`"files"\` in tsconfig exist**

*Implement a check during tsconfig root file loading to confirm that all "files" entries exist.*

 * created by **iisaduan**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3871](https://github.com/microsoft/TypeScript-go/pull/3871) (Open, **sandersn**, **RyanCavanaugh**, **Copilot**)

**Use named\-function overload diagnostic for JSDoc \`@overload\` return\-type omissions**

*Change JSDoc @overload return-type omission diagnostics to report function names (TS7010) for named functions instead of generic TS7012 errors.*

 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **sandersn**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3872](https://github.com/microsoft/TypeScript-go/pull/3872) (Open, **RyanCavanaugh**, **Copilot**)

**Reclassify \`nodeModulesAllowJsImportAssignment\` JS emit diffs as accepted baselines**

*Reclassify nodeModulesAllowJsImportAssignment JS emit diffs as accepted baselines reflecting export import changes.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3874](https://github.com/microsoft/TypeScript-go/pull/3874) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer crash in Program\.SingleThreaded on snapshot update**

*Prevent nil pointer crash by adding nil checks in SingleThreaded and skipping CreateProgram when CommandLine is unset.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4462933487) **RyanCavanaugh** said "@copilot why didn't you follow the PR instructions here? https://github.com/microsoft/typescript-go/blob/main/.github/copilot-instructions.md#pr-template"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4463078701) **Copilot** updated the PR description to follow the template and noted that build, test, lint, and format checks passed
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4463100044) **jakebailey** said "no it doesn't, not at all"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3879](https://github.com/microsoft/TypeScript-go/pull/3879) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil dereference in resolveHelpersModule via checkExternalEmitHelpers**

*Prevent nil dereference in resolveHelpersModule by falling back to file.AsNode when checkExternalEmitHelpers runs without an import specifier.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3879#issuecomment-4480157845) **DanielRosenwasser** said "@copilot I don't see a panic from that test locally."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3879#issuecomment-4480319374) **Copilot** verified that tests did not panic without the fix, proposed a theory regarding project references with differing importHelpers settings, removed irrelevant tests, retained the defensive nil check, and offered to add a proper test if provided with a repro case
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3910](https://github.com/microsoft/TypeScript-go/pull/3910) (Open, **jakebailey**, **Copilot**)

**Fix incorrect renaming of \`arguments\` in non\-reference positions in async downlevel**

*Async downlevel incorrectly renames `arguments` in non-reference contexts, now fixed by using the AST IsIdentifierName utility and label checks.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3912](https://github.com/microsoft/TypeScript-go/pull/3912) (Open, **jakebailey**, **Copilot**)

**Fix type soundness for lone\-surrogate string literals**

*Ensure lone-surrogate string literals are encoded and compared distinctly to maintain type soundness and correctness.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3912#issuecomment-4481127125) **jakebailey** said "@copilot apply changes based on the comments in this thread"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3912#issuecomment-4481339817) **Copilot** fixed CompareStringsCaseInsensitive to use decodeCESU8OrUTF8 and applied extended escape surrogate handling with tests in commit ef2a8254
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3912#issuecomment-4481362050) **jakebailey** noted that the situation seemed spooky and suggested consistent use of WTF-8 everywhere
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3923](https://github.com/microsoft/TypeScript-go/pull/3923) (Open, **jakebailey**, **Copilot**)

**Fix source\-map emit panic for unclosed blocks**

*Prevent panics in source-map emission by handling positions beyond EOF when processing unclosed code blocks*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3941](https://github.com/microsoft/TypeScript-go/pull/3941) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil dereference crash in loadModuleFromSpecificNodeModulesDirectory**

*Prevent nil dereference in loadModuleFromSpecificNodeModulesDirectory by adding a packageInfo.Exists() guard and a subpath node_modules resolution test case.*

 * **Copilot** assigned to **DanielRosenwasser**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4474794206) **DanielRosenwasser** said "The test seems insufficient if this is about race conditions. @copilot is there a better test here? Possibly a server test or a programmatic test of our APIs?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4474873463) **Copilot** replaced the compiler test with a programmatic race condition test and detailed deterministic reproduction steps
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3987](https://github.com/microsoft/TypeScript-go/pull/3987) (Open, **RyanCavanaugh**, **Copilot**)

**Avoid fatal panic on stale config\-retainer project paths in project rebuild flow**

*Prevent panic in markProjectsAffectedByConfigChanges by skipping stale project paths and add a regression test to verify safe handling.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#3994](https://github.com/microsoft/TypeScript-go/pull/3994) (Open, **DanielRosenwasser**, **Copilot**)

**Fix external helper crash after module\-status updates**

*Treating module-indicator changes as non-reusable to force rebuilds and prevent missing tslib-import crashes after updates.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4492292470) **DanielRosenwasser** said "Perfect - can you write this as a fourslash test instead? Make sure the fourslash test actually fails without the fix."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4492293827) **DanielRosenwasser** said "@copilot"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4492417437) **Copilot** addressed the request by adding a fourslash test and verifying it failed without the production fix
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4015](https://github.com/microsoft/TypeScript-go/pull/4015) (Open)

**Do not emit declaration files when they contain a declaration emit error**

*Prevent TypeScript from emitting declaration files when declaration emit errors occur.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4029](https://github.com/microsoft/TypeScript-go/pull/4029) (Closed)

**Fix and simplify JSDoc handling for binding elements**

*Simplify and fix JSDoc quick info handling for destructured binding elements to prevent duplicate documentation and improve consistency.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4033](https://github.com/microsoft/TypeScript-go/pull/4033) (Open)

**Fix resolveNodeHandle to check not only child nodes but ancestor nodes**

*Enhance resolveNodeHandle to traverse ancestor nodes alongside children to correctly identify the actual AST node*

 * created by **jet2jet**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4034](https://github.com/microsoft/TypeScript-go/issues/4034) (Closed, `Domain: Declaration Emit`, `possible improvement`, `Needs Investigation`, **weswigham**)

**Behavior difference: tsgo emits different output when keys from one object are referenced in another object**

*tsgo emits generic index signatures for computed property keys instead of preserving specific keys, causing noise in diffs compared to tsc*

 * (2 days ago) **weswigham** added labels `Domain: Declaration Emit`, `possible improvement`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4034#issuecomment-4549484598) **weswigham** explained that the behavior was intentional for synthesized node types, acknowledged that more verbose output is preferable, and noted that the logic tracking original computed property names got lost in the port and needs reporting
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4035](https://github.com/microsoft/TypeScript-go/issues/4035) (Open, `bug`, `Domain: Editor`, **gabritto**)

**VSCode bulk save \(Replace All / Save All across many \.ts files\) deadlocks the LSP server**

*Bulk replacing across many .ts files in VSCode deadlocks the TypeScript Native Preview LSP server, which doesn’t restart on reload.*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**
 * (today) **gabritto** added label `bug`, and removed label `Needs Investigation`

### [PR microsoft/TypeScript-go#4058](https://github.com/microsoft/TypeScript-go/pull/4058) (Open)

**Reparse non\-identifier jsdoc names where possible, error otherwise**

*The parser now reparses non-identifier JSDoc names when possible and errors on unsupported nameless typedef patterns.*

 * created by **weswigham**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4549523307) **DanielRosenwasser** said "Can we give a more-specialized error message for reserved names?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4556668076) **weswigham** clarified that keywords were allowed as identifiers and that the check concerned only actual allowed characters in JS identifiers
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#4059](https://github.com/microsoft/TypeScript-go/issues/4059) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**reference directive caused issue with ts\-check**

*Placing a triple-slash reference directive after a // @ts-check comment causes tsgo to bypass type-checking, effectively acting like ts-nocheck.*

 * (yesterday) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060) (Open, `Crash`)

**Data race in module resolver — SIGSEGV in \`loadModuleFromTargetExportOrImport\` / \`OrderedMap\.Keys\` under concurrent goroutines**

*Concurrent access to OrderedMap.Keys within the module resolver's loadModuleFromTargetExportOrImport triggers a data race causing a SIGSEGV.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4560952310) **dimikot** said "@mscrivo What version were you at when it was working?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4564424105) **mscrivo** identified that the crash started in version 20260515.1 through a binary search and offered to provide repo access
 * [today](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4564450769) **mscrivo** suggested a related PR and noted that the issue only occurred on macOS arm machines, not on Linux CI runners
 * [later](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4574995897) **anotheri** reported experiencing the same issue and linked to a related issue with additional macOS AMD machine details

### [PR microsoft/TypeScript-go#4061](https://github.com/microsoft/TypeScript-go/pull/4061) (Open, **RyanCavanaugh**, **Copilot**)

**Preserve ts\-check across reference directives**

*Triple-slash reference directives were overriding ts-check pragmas and disabling type checking, so check-mode selection is now limited to ts-check/ts-nocheck pragmas*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4062](https://github.com/microsoft/TypeScript-go/pull/4062) (Open)

**Check \`this\` params when comparing pseudotype signatures to type signatures**

*Include `this` parameters in comparisons between pseudotype signatures and actual type signatures.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4063](https://github.com/microsoft/TypeScript-go/pull/4063) (Open)

**Warn on TSServer Plugin Contributions from other extensions**

*Display a warning when non-core extensions contribute TSServer plugins to prevent unexpected conflicts.*

 * created by **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#4064](https://github.com/microsoft/TypeScript-go/pull/4064) (Closed)

**Emit index components for computed names instead of signatures**

*Modify the compiler to emit index components for computed property names in generated code instead of signatures.*

 * created by **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4065](https://github.com/microsoft/TypeScript-go/pull/4065) (Open)

**Revise logic for gathering JSDoc \`@template\` type parameters**

*Revise JSDoc @template parameter gathering logic to fix issue 4037 and document differences in CHANGES.md.*

 * created by **ahejlsberg**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#4070](https://github.com/microsoft/TypeScript-go/issues/4070) (Open, `Needs Investigation`, **DanielRosenwasser**, **Copilot**)

**typescript\.native\-preview\.tsdk: relative path in committed \.vscode/settings\.json gets overwritten with absolute path when accepting the workspace version prompt**

*Accepting the workspace version prompt for TypeScript Native Preview converts a relative tsdk path to an absolute one, dirtying settings.*

 * created by **Cellule**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **Copilot**

### [Issue microsoft/TypeScript-go#4071](https://github.com/microsoft/TypeScript-go/issues/4071) (Open)

**Behavior difference: Emoji string in tsgo emit does not align well with tsc**

*Emoji-containing string literal types emit differently in tsgo than tsc, causing misalignment after recent emoji handling fixes.*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#4072](https://github.com/microsoft/TypeScript-go/pull/4072) (Open, **DanielRosenwasser**, **Copilot**)

**Fix tsdk relative path overwrite and unnecessary prompt on workspace open**

*Prevent tsdk setting from being overwritten with machine-specific absolute paths by auto-detecting workspace tsdk, skipping prompts, and using relative paths.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4569008721) **Copilot** stated that the issue was fixed in commit 0f8de0c
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4569028963) **DanielRosenwasser** requested more feedback and asked about built-in TS extension behavior with an explicit tsdk even after workspace trust
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4569059752) **Copilot** addressed both reviewer points regarding restart on early-return and multi-root workspaces path resolution and explained the built-in TS extension tsdk prompt behavior

### [PR microsoft/TypeScript-go#4073](https://github.com/microsoft/TypeScript-go/pull/4073) (Open)

**Restore JSDoc namespace declarations**

*Simplifies JSDoc handling and adds reparsed node remapping to restore namespace declarations for Quick Info, find references, and rename support.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#4074](https://github.com/microsoft/TypeScript-go/pull/4074) (Open)

**Fix stale pull diagnostics after document edits**

*Implement request-time document snapshots and freshness checks to avoid applying stale diagnostics after edits.*

 * created by **Kelpy2004**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4074#issuecomment-4575919369) **Kelpy2004** asked whether @jakebailey was the right person to review the follow-up on microsoft/vscode#317522 and offered to adjust the approach

