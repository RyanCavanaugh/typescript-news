# Report for 2026-01-08 (Thursday, January 8th, 2026)

7 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @grundmanise reported persistent node module errors despite exclusion in [microsoft/TypeScript#36664](https://github.com/microsoft/TypeScript/issues/36664#issuecomment-3725979139)
    * @AceCodePt asked why a definition or constant for exact match was missing in [microsoft/TypeScript#43284](https://github.com/microsoft/TypeScript/issues/43284#issuecomment-3727858728)

## Activity Summary

### [Issue microsoft/TypeScript#36664](https://github.com/microsoft/TypeScript/issues/36664) (Closed, `Suggestion`, `Committed`, **RyanCavanaugh**)

**Support closed\-file diagnostics in VS Code**

*Enable project-wide closed-file TypeScript diagnostics in VS Code by adding an inverse-dependencies API independent of compileOnSave*

 * (23 weeks ago) **RyanCavanaugh** closed the issue
 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/36664#issuecomment-3187689451) **louwers** said "https://github.com/microsoft/vscode/issues/117732 was closed as a duplicate of this issue, but the issue still seems to be present."
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/36664#issuecomment-3236959133) **FunctionDJ** encouraged moving the setting out of experimental to unblock other projects
 * [today](https://github.com/microsoft/TypeScript/issues/36664#issuecomment-3725979139) **grundmanise** reported that node module problems continued to appear despite being excluded and only temporarily disappeared when reopening each file

### [Issue microsoft/TypeScript#43284](https://github.com/microsoft/TypeScript/issues/43284) (Open, `Suggestion`, `Awaiting More Feedback`)

**Narrowing for key type by \`in\` operator**

*Allow 'in' operator checks to narrow a string key variable to the object's keyof type*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/43284#issuecomment-1997753065) **fenghourun** asked about the consensus on using type-guards, noting they felt no safer than type casting and could result in runtime errors
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/43284#issuecomment-2000409456) **RyanCavanaugh** clarified that types from const assertions are not sealed and illustrated this with an example
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/43284#issuecomment-2379484686) **karlismelderis-mckinsey** clarified that const assertions don't seal objects, demonstrated this with an example, and asked whether to wait for a stricter key-only type
 * [later](https://github.com/microsoft/TypeScript/issues/43284#issuecomment-3727858728) **AceCodePt** said "Shouldn't there be a definition of exact match? Why don't we have the const the exact match? "

### [Issue microsoft/TypeScript#61375](https://github.com/microsoft/TypeScript/issues/61375) (Closed, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**\`for\`\-\`let\` \+ inner function incorrectly says variable is used before being assigned**

*Loop-scoped let variables referenced in inner functions incorrectly trigger 'used before assignment' errors in TypeScript 5.7.*

 * (43 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Control Flow`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#61376](https://github.com/microsoft/TypeScript/pull/61376) (Closed, `For Backlog Bug`)

**Fixed an issue causing spurious "used before being assigned" errors in for of/in loops**

*Fixes spurious 'used before being assigned' errors in for-of and for-in loops.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/61376#issuecomment-3725833993) **RyanCavanaugh** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/61376#issuecomment-3725834877) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/61376#issuecomment-3725853233) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/61376#issuecomment-3725853491) **typescript-bot** reported CI build statuses and result links
 * [today](https://github.com/microsoft/TypeScript/pull/61376#issuecomment-3725965192) **typescript-bot** reported that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/61376#issuecomment-3725987089) **typescript-bot** reported test results showing infrastructure failures but otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/61376#issuecomment-3726060484) **typescript-bot** posted performance run results as requested
 * [today](https://github.com/microsoft/TypeScript/pull/61376#issuecomment-3726212863) **typescript-bot** reported that tsc runs on the top 400 repos comparing main and the PR merge succeeded
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62789](https://github.com/microsoft/TypeScript/pull/62789) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Fix "never nullish" diagnostic missing expressions wrapped in parentheses**

*The never-nullish TS2881 diagnostic was not reported for operands wrapped in parentheses in nullish coalescing expressions*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3573083720) **typescript-bot** reported an infrastructure failure in user tests and confirmed all other tests passed
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3573152782) **typescript-bot** provided the requested performance run results
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3573205792) **typescript-bot** reported that everything looked good running the top 400 repos with tsc comparing main and the PR merge
 * [today](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3726604843) **RyanCavanaugh** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3726604982) **typescript-bot** reported test top800 job start and completion statuses with links
 * [today](https://github.com/microsoft/TypeScript/pull/62789#issuecomment-3726927034) **typescript-bot** reported results of running the top 800 repos with tsc comparing main and the PR merge, noting that everything looked good

### [Issue microsoft/TypeScript#62910](https://github.com/microsoft/TypeScript/issues/62910) (Closed, `Not a Defect`)

**\`as\` type assertion fails for \`ReadonlyArray\<T\>\` but succeeds for \`T\[\]\` with identical object literal**

*TypeScript rejects 'as ReadonlyItems' assertions with ReadonlyArray properties but accepts identical 'as MutableItems' assertions.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62910#issuecomment-3672530315) **Andarist** explained that the underlying cause was the same as in a provided code example, highlighted mismatched nested properties, and linked a related issue
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62910#issuecomment-3715695939) **RyanCavanaugh** clarified that type assertions only worked when the asserted type subtyped or supertyped the expression type to prevent incorrect assertions
 * [today](https://github.com/microsoft/TypeScript/issues/62910#issuecomment-3726679576) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62926](https://github.com/microsoft/TypeScript/issues/62926) (Closed, `Suggestion`, `Help Wanted`, `Domain: lib.d.ts`, `Experience Enhancement`)

**Add generateKey X25519 CryptoKeyPair**

*Add generateKey support for X25519 algorithm returning CryptoKeyPair to TypeScript DOM definitions to avoid missing publicKey property errors*

 * (2 days ago) **RyanCavanaugh** added label `Experience Enhancement`, and set milestone to `Backlog`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62926#issuecomment-3716873994) **anflext** said "💯  Excelent! If add an overload for "X25519", later new beginner will not break by the compile check error."
 * (today) **github-actions[bot]** closed the issue

### [PR microsoft/TypeScript#62961](https://github.com/microsoft/TypeScript/pull/62961) (Closed, `For Backlog Bug`)

**\[moved\] Add X25519 generateKey overload to SubtleCrypto**

*Add a TypeScript overload for SubtleCrypto.generateKey with X25519 to enable deriveKey and deriveBits usage and proper CryptoKeyPair typing.*

 * **typescript-bot** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62961#issuecomment-3720880463) **typescript-bot** notified that the pull request updated generated DOM declaration files which should not be edited and that the PR would be closed
 * (yesterday) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/62961#issuecomment-3726048016) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#62962](https://github.com/microsoft/TypeScript/issues/62962) (Closed, `Duplicate`)

**Monorepo support**

*Allow TypeScript compiler to recognize monorepo package boundaries and skip type checking of node_modules during noEmit builds*

 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3723676162) **mkantor** asked what would happen if the compiler applied a String augmentation from an imported module and allowed a.foo, and asked the same for process from @types/node
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3723744830) **valler** explained that the code would type check as part of the interface but the issue relates to uncompiled TS sources rather than declaration files and described how the type checker only verifies code under its control
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3724088615) **valler** updated the comment in the motivating example to align wording and avoid confusion
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Needs Proposal`
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3725021606) **RyanCavanaugh** explained thorny type-checking issues with `tsc --noEmit` in monorepos due to mismatched tsconfig options and ambiguous return types
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3726479236) **valler** thanked RyanCavanaugh, agreed on isolatedDeclarations for monorepos, suggested using --noEmit or a new --check flag to streamline efficient two-pass type checking and reduce redundant compilation and checks
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3726514021) **RyanCavanaugh** questioned whether the description referred to current tsc -b behavior plus automatic inference of references
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3726518341) **valler** clarified that they meant tsc -b with automatic inference of references and emphasized its importance
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3726691945) **valler** added a workaround suggesting use of `tsc --build` with references mirroring `package.json` dependencies to minimize full builds
 * [today](https://github.com/microsoft/TypeScript/issues/62962#issuecomment-3727161649) **valler** proposed updating the composite config to an enum with values false, true, and package to eliminate references and leverage package.json for monorepo builds

### [Issue microsoft/TypeScript#62966](https://github.com/microsoft/TypeScript/issues/62966) (Open, `Bug`, `Help Wanted`, `Domain: check: Type Circularity`)

**Regression: RangeError: Maximum call stack size exceeded in type instantiation with recursive types and intersections**

*Regression in TypeScript 5.9 causes infinite recursion and a RangeError stack overflow when instantiating recursive intersection types.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/62966#issuecomment-3725972002) **RyanCavanaugh** said "Bisects to #61505, hangs in TS7"
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`

