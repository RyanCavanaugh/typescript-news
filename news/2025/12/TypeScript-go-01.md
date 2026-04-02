# Report for 2025-12-01 (Monday, December 1st, 2025)

6 different users commented on 36 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#1495](https://github.com/microsoft/TypeScript-go/issues/1495) (Closed, `Domain: Editor`)

**Signature help may not respect capabilities for \`NoActiveParameterSupport\`**

*Signature help incorrectly handles the NoActiveParameterSupport capability by leaving activeParameter unset instead of defaulting to zero and lacking tests.*

 * created by **DanielRosenwasser**
 * **jakebailey** added label `Domain: Editor`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1591](https://github.com/microsoft/TypeScript-go/pull/1591) (Closed)

**Misc LSP server / fourslash testing improvements**

*Redirect LSP stderr to test output, add context-based lifetime control, and ensure tests await clean server shutdown with logging.*

 * created by **jakebailey**
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1591#issuecomment-3192224177) **jakebailey** said "Wow, okay, apparently I'm fixing a latent bug here were a load of tests were broken due to the LSP lifetime and we did not realize."
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1591#issuecomment-3192232087) **jakebailey** said "No, I just caused a race. Will figure it out."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1616](https://github.com/microsoft/TypeScript-go/issues/1616) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**The last overload gave the following error\. Type 'unknown' is not assignable to type 'Foo'**

*After updating the TypeScript native-preview extension, DialogConfig calls fail with unknown not assignable to the expected modal confirmation generic type.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3592010666) **urielzen** acknowledged that they updated the extensions but didn't realize it was disabled and apologized for the confusion
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3592032586) **jakebailey** said "So, it's fixed? 😄"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3592034829) **urielzen** said "not yet, sorry"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3598605809) **RyanCavanaugh** said "We need minimal isolated repro."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3598619168) **urielzen** offered to put something together and report back

### [PR microsoft/TypeScript-go#1850](https://github.com/microsoft/TypeScript-go/pull/1850) (Closed, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#60304: More rigorous ASI prevention when emitting return/yield**

*Port TypeScript’s stricter ASI prevention for return and yield emission into Corsa with improved naming, tests, and addressing architectural concerns.*

 * **RyanCavanaugh** assigned to **weswigham**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1850#issuecomment-3388293216) **jakebailey** said "@copilot read comments and address"
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1850#issuecomment-3388324987) **Copilot** implemented functionality and confirmed tests passed matching TypeScript baselines while acknowledging prior failures and potential architectural concerns
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1855](https://github.com/microsoft/TypeScript-go/pull/1855) (Closed, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Port PR\#576 from original repository**

*Work in progress to port PR#576 from the original TypeScript repository into this project.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1856](https://github.com/microsoft/TypeScript-go/pull/1856) (Closed, **RyanCavanaugh**, **Copilot**)

**Verify TypeScript PR \#60680 already ported: Mark inherited any\-based index signatures**

*The TypeScript PR #60680 changes for marking inherited any-based index signatures have already been implemented in the Go codebase.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1857](https://github.com/microsoft/TypeScript-go/pull/1857) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR\#60980: Fix wrong error on required initialized parameters with isolatedDeclarations**

*Fix wrong enclosing declaration for initialized constructor parameter properties under isolatedDeclarations to properly add implicit undefined*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1858](https://github.com/microsoft/TypeScript-go/pull/1858) (Closed, **RyanCavanaugh**, **Copilot**)

**Port PR\#60052: Computed names in declaration files are resolved even when non\-literal, preserve computed names when expressions are entity names**

*Ported TypeScript PR#60052 to Go, enabling non-literal computed property name resolution and preservation in declarations while improving index signature checks.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1859](https://github.com/microsoft/TypeScript-go/pull/1859) (Closed, **RyanCavanaugh**, **Copilot**)

**Port PR\#61261: Fix accidentally reused comments between files in the emitter**

*Port TypeScript PR 61261 to Go, preventing accidental comment reuse across files in the declaration emitter.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1860](https://github.com/microsoft/TypeScript-go/pull/1860) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR\#61342: Rename type parameters when they are shadowed**

*Port TypeScript change to rename shadowed type parameters in declaration emitter for unambiguous declarations.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1861](https://github.com/microsoft/TypeScript-go/pull/1861) (Closed, **RyanCavanaugh**, **Copilot**)

**Port PR\#60234: Use signature\.parameters directly instead of getExpandedParameters**

*Port PR#60234 to Go by replacing getExpandedParameters with direct signature.parameters usage to simplify and improve rest parameter type emissions.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1862](https://github.com/microsoft/TypeScript-go/pull/1862) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR\#61813: Implement new \`tsc \-\-init\` template**

*Port PR#61813 changes to implement a modern, opinionated tsconfig.json template for tsc --init.*

 * created by **Copilot**
 * (7 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1868](https://github.com/microsoft/TypeScript-go/pull/1868) (Closed, **jakebailey**, **Copilot**)

**Fix \-\-customConditions null not being respected when overriding tsconfig\.json**

*Fix tsgo to respect --customConditions null when merging tsconfig.json by adding raw option parsing support*

 * (7 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1868#issuecomment-3391138929) **Copilot** clarified that the implementation already supported null for unsetting any CompilerOptions and verified it with --lib, --types, and --outDir
 * [today](https://github.com/microsoft/TypeScript-go/pull/1868#issuecomment-3599487375) **jakebailey** said "@copilot you did not run the formatter as instructed"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1868#issuecomment-3599507154) **Copilot** fixed indentation by running the formatter in commit 81d4e0

### [Issue microsoft/TypeScript-go#1897](https://github.com/microsoft/TypeScript-go/issues/1897) (Closed, `Domain: Editor`)

**Add support for references code lenses in VS Code extension**

*Add support for reference code lenses in the VS Code tsgo extension to match existing functionality.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1897#issuecomment-3439360441) **jakebailey** suggested implementing code lenses server-side to minimize data transfer, clarified VS Code's use of the showReferences command for both references and implementations, and noted the need to verify client support for these commands
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#1932](https://github.com/microsoft/TypeScript-go/pull/1932) (Closed, **RyanCavanaugh**, **Copilot**)

**Port PR 62656: Fix TS2783 false positive for union types in object spread expressions**

*Port PR 62656 to fix false positive TS2783 errors when spreading union types in object literals by considering partial flags.*

 * created by **Copilot**
 * (5 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#1949](https://github.com/microsoft/TypeScript-go/pull/1949) (Open, **jakebailey**, **Copilot**)

**Fix signature help applicable span for nested calls**

*Improves signature help applicable span for nested function calls to correctly handle empty argument lists and prioritize outer calls.*

 * created by **Copilot**
 * (5 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3599375519) **jakebailey** reported that the PR failed TestSignatureHelpWithTriggers02 due to using foo instead of bar when inserting a parenthesis
 * [today](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3599472557) **Copilot** reverted the changes in commit bed1740 and explained conflicting requirements between TestSignatureHelpWithTriggers02 and the nested calls fix, noting a pre-existing issue and the need for a nuanced approach
 * [today](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3599484546) **jakebailey** clarified that the test transforms foo(bar|) into foo(bar(|) and expects bar's signature help, stating that there is no conflict and attributing the confusion to a misunderstanding
 * [today](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3599507732) **Copilot** acknowledged a misunderstanding, clarified that signature help should appear inside inner call parentheses, noted that TestSignatureHelpWithTriggers02 was failing, and said they would investigate and fix the span calculation for empty argument lists

### [PR microsoft/TypeScript-go#1982](https://github.com/microsoft/TypeScript-go/pull/1982) (Closed, **jakebailey**, **Copilot**)

**Add test reproducing panic on out\-of\-bounds textDocument/definition request**

*A new test exposes a panic in the LSP server when handling textDocument/definition requests with line numbers beyond the file length*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/1982#issuecomment-3599323829) **jakebailey** said "Bad test, this just sends something out of bounds which is not helpful"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2012](https://github.com/microsoft/TypeScript-go/pull/2012) (Closed, **jakebailey**, **Copilot**)

**\[WIP\] Fix component prop usage references to include all instances**

*Extend Find All References to include JSX attribute usages for React component props across files*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2104](https://github.com/microsoft/TypeScript-go/pull/2104) (Closed, **jakebailey**, **Copilot**)

**Add missing TS6504 diagnostic for JavaScript files without allowJs**

*Add diagnostic TS6504 for JavaScript files when allowJs is disabled in all inclusion scenarios.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3599606585) **jakebailey** reported a data race in includeProcessor concurrent use and provided the stack trace

### [Issue microsoft/TypeScript-go#2108](https://github.com/microsoft/TypeScript-go/issues/2108) (Open)

**Import containing a dot give an error**

*Importing from 'socket.io/dist/namespace' works in TypeScript 5.8 but causes TS2307 'cannot find module' errors in tsgo.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2108#issuecomment-3542739690) **jakebailey** said "This is not enough information. Can you please provide a repro?"
 * **jakebailey** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2108#issuecomment-3580290747) **Niron68** provided a repository demonstrating inconsistent results between npm run check:tsc and npm run check:tsgo
 * [today](https://github.com/microsoft/TypeScript-go/issues/2108#issuecomment-3599008290) **RyanCavanaugh** noted that a deprecated compiler option was being used and showed the resulting error message
 * **RyanCavanaugh** removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2108#issuecomment-3599030621) **jakebailey** said "Yeah, unfortunately we are not yet hard erroring in tsgo on node10."

### [Issue microsoft/TypeScript-go#2114](https://github.com/microsoft/TypeScript-go/issues/2114) (Closed, **ahejlsberg**)

**Stamp out remaining ordering differences requiring multi\-checker error**

*Apply patch disabling multi-checker error merging and re-enable tests, resulting in four failing baseline errors.*

 * created by **jakebailey**
 * **jakebailey** assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2145](https://github.com/microsoft/TypeScript-go/pull/2145) (Closed)

**Implement support for Code Lenses**

*Implements server-side LSP support for code lenses with resolve functionality and a client command to preview references and implementations.*

 * created by **DanielRosenwasser**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2145#issuecomment-3564586409) **jakebailey** said "Thankfully this is opt-in, otherwise I'd be even more worried about merging this given this also uses the checker."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2156](https://github.com/microsoft/TypeScript-go/pull/2156) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Update GitHub Actions in the root directory by bumping actions/checkout to v6.0.0 and github/codeql-action*

 * (1 week ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2167](https://github.com/microsoft/TypeScript-go/pull/2167) (Closed)

**fix: preserve comments on import attribute values**

*Add missing support for preserving trailing comments on import attribute values in the TypeScript emitter.*

 * created by **a-tarasyuk**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2168](https://github.com/microsoft/TypeScript-go/pull/2168) (Closed)

**Revise type\-only alias logic to not depend on full type checks**

*Revise type-only import/export alias checking so files can be type-checked independently without full program checks.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2169](https://github.com/microsoft/TypeScript-go/issues/2169) (Open, `Domain: Editor`)

**Support for \`workspace/diagnostic\` from LSP 3\.17**

*Implement LSP 3.17 workspace/diagnostics to provide reliable project-wide diagnostics without opening each file.*

 * created by **versecafe**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2169#issuecomment-3597790119) **jakebailey** expressed support for replacing the experimental enableProjectDiagnostics setting with a request-based LSP system
 * **jakebailey** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2170](https://github.com/microsoft/TypeScript-go/pull/2170) (Closed)

**Generate remaining sig help tests, fix remaining bugs**

*Generate missing signature help tests and fix related bugs including active parameter capability handling, inComment checks, and backup JS sig help code porting.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2171](https://github.com/microsoft/TypeScript-go/pull/2171) (Closed)

**Port call hierarchy, fourslash tests**

*Reconcile tsserver and LSP call hierarchy by combining logic with VS Code post-processing and correcting script file kind to file.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2171#issuecomment-3598487488) **jakebailey** said "Yeesh, either our tests are bad or I did something very wrong (well, I'm wrong either way); this does not seem to work in the editor past a single resolve."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2171#issuecomment-3598684052) **jakebailey** admitted choosing a test function with no callers and decided to use a better function like assert
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2172](https://github.com/microsoft/TypeScript-go/pull/2172) (Closed)

**Never create more checkers than files in a program**

*Limit the number of checkers in a program to the number of files to prevent wasted resources.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2172#issuecomment-3599291579) **jakebailey** said "This will conflict with #2159 so I'll wait for that as it's more critical."

### [PR microsoft/TypeScript-go#2173](https://github.com/microsoft/TypeScript-go/pull/2173) (Closed)

**Update LSP error generation, enum naming, string enums**

*Refactor LSP error generation and enum definitions by removing duplicate error types, correcting enum naming, and title-casing string enum values.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2174](https://github.com/microsoft/TypeScript-go/pull/2174) (Closed)

**Server\-to\-client refresh requests for user preference updates**

*Adds server-to-client refresh for inlay hints and code lenses, nested UserPreferences hierarchy, verbose go generate, and fixes inlay hint parsing typos.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2175](https://github.com/microsoft/TypeScript-go/issues/2175) (Closed, `Domain: Editor`)

**tsgo doesn't suggest \(autoimport\) of packages in monorepo and tries to use relative path in vscode**

*tsgo’s autoimport in a monorepo bypasses configured package paths and suggests incorrect deep relative imports instead of package names.*

 * created by **darklight9811**

