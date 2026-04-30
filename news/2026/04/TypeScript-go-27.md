# Report for 2026-04-27 (Monday, April 27th, 2026)

22 different users commented on 49 different issues.

## Recommended Actions

 * Response Recommended
    * @RealHaris asked if anything more was required after adding the info in [microsoft/TypeScript-go#3441](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4329246949)
    * @nileshpatil6 asked if they should push a revised version without TSGO_BINARY in [microsoft/TypeScript-go#3451](https://github.com/microsoft/TypeScript-go/pull/3451#issuecomment-4333762563)
    * @hkleungai asked whether to reopen the issue or open a new one in [microsoft/TypeScript-go#3600](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4333661647)
    * @hkleungai asked if the PR addresses errors mentioned in #3600 and suggested adding a testcase file in [microsoft/TypeScript-go#3608](https://github.com/microsoft/TypeScript-go/pull/3608#issuecomment-4329720012)
    * @kwonoj asked about signing an NDA to access private code in [microsoft/TypeScript-go#3612](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4330791306)
    * @Netail provided additional details about the inconsistent occurrence and offered to share logs in [microsoft/TypeScript-go#3638](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4335893311)

## Activity Summary

### [Issue microsoft/TypeScript-go#2386](https://github.com/microsoft/TypeScript-go/issues/2386) (Closed, `Domain: Editor`, **gabritto**)

**TS2307 Delete a folder of \`\.ts\` files does not trigger \`ts\(2307\)\` error hint**

*VSCode does not display a ts(2307) missing module error when a referenced folder of .ts files is deleted*

 * **ColaFanta** added label `Domain: Editor`
 * (3 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2387](https://github.com/microsoft/TypeScript-go/issues/2387) (Closed, `bug`, **iisaduan**)

**Diagnostics don't refresh after file rename**

*After renaming a file, TypeScript diagnostics sometimes fail to update until the server is reloaded.*

 * (1 month ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2387#issuecomment-4333240137) **iisaduan** said "should be fixed after https://github.com/microsoft/typescript-go/pull/3483"
 * (later) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#2875](https://github.com/microsoft/TypeScript-go/issues/2875) (Closed, `Crash`, **iisaduan**)

**Occasional error invalid memory address/nil pointer dereference \- codeAction failed**

*TypeScript-Go LSP server intermittently panics with a nil pointer dereference when handling textDocument/codeAction requests.*

 * **lukpsaxo** added label `Crash`
 * (1 month ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2875#issuecomment-4330177578) **jakebailey** said "Given the failure mode, I think this was fixed by #3483, but please refile if you hit this again"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3384](https://github.com/microsoft/TypeScript-go/issues/3384) (Closed, `Crash`, **andrewbranch**)

**Crash in adjusting positions for folding ranges**

*Adjusting folding range end positions in the Go language service now crashes due to LineAndCharacterToPosition conversion errors.*

 * (1 week ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4253249016) **andrewbranch** said "This doesn't look like a bug to me—e.Change clones the file which unsets its line map."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4330164116) **andrewbranch** said "This should be closed now, right?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3384#issuecomment-4330172555) **jakebailey** said "I suspect so after #3483, given we do not see this failure category anymore."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3441](https://github.com/microsoft/TypeScript-go/issues/3441) (Closed, **jakebailey**, **Copilot**)

**Panic handling textDocument/semanticTokens/{full,range}: slice bounds out of range and token\-spans\-multiple\-lines**

*Semantic tokens full and range handlers panic due to slice bounds out-of-range errors and multi-line token spans.*

 * (6 days ago) **jakebailey** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4320897495) **RealHaris** reported an InternalError from textDocument/semanticTokens/full and asked if it was resolved
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4320932292) **jakebailey** said "Please file a new issue, hopefully with a repro or LSP logs."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4329246949) **RealHaris** notified that they added the required information and asked if anything more was needed

### [PR microsoft/TypeScript-go#3451](https://github.com/microsoft/TypeScript-go/pull/3451) (Open)

**perf: add TSGO\_BINARY env var and fast\-path sibling check in getExePath**

*Introduce TSGO_BINARY override and a fast-path sibling binary check in getExePath to avoid repeated import.meta.resolve calls and boost performance.*

 * created by **nileshpatil6**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3451#issuecomment-4284655558) **jakebailey** said "If someone has this path, why wouldn't they just run it directly? This seems really special case-y."
 * [later](https://github.com/microsoft/TypeScript-go/pull/3451#issuecomment-4333762563) **nileshpatil6** proposed dropping TSGO_BINARY and asked whether to push a revised version with only the sibling check

### [Issue microsoft/TypeScript-go#3456](https://github.com/microsoft/TypeScript-go/issues/3456) (Closed, `Domain: Declaration Emit`, **weswigham**)

**JS declaration emit ignores properties declared through \`this\.xxx\` assignments**

*Declaration emission for JavaScript ignores properties declared through this.xxx assignments in constructors and methods.*

 * (6 days ago) **ahejlsberg** set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3456#issuecomment-4289186020) **Andarist** suggested adding tests for static properties declared in static blocks because Strada emitted an empty class for them
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3541](https://github.com/microsoft/TypeScript-go/pull/3541) (Closed)

**Collect this property assignments in JS declaration emit and transform them to TS declarations**

*Expand JS declaration emit to support 'this' assignments, require imports, module.exports class hoisting, and static block expando tests.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3552](https://github.com/microsoft/TypeScript-go/issues/3552) (Open, `Domain: Declaration Emit`, **andrewbranch**, **RyanCavanaugh**, **Copilot**)

**Baselines: export = a reordered; ESM side\-effect import replaces export {}**

*Baseline diffs indicate that CommonJS export assignments are reordered after declarations and empty ES exports are replaced by side-effect imports.*

 * **RyanCavanaugh** added label `wontfix`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4316483827) **jakebailey** said "Shouldn't we be eliding that unused import?"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4316606320) **RyanCavanaugh** asked for thoughts on an input code snippet showing different module configurations
 * [today](https://github.com/microsoft/TypeScript-go/issues/3552#issuecomment-4328772548) **andrewbranch** weighed arguments for preserving and eliding side-effect imports in declaration files and recommended continuing to elide
 * (today) **RyanCavanaugh** removed label `wontfix`, set milestone to `TypeScript 7.0 RC`, and assigned to **andrewbranch**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3576](https://github.com/microsoft/TypeScript-go/issues/3576) (Closed)

**\[Proposal\] strictArrayVariance: opt\-in invariance for mutable Array\<T\> element type \(post\-7\.0 discussion\)**

*Introduce a strictArrayVariance compiler option to enforce invariant element types on mutable arrays, preventing unsound covariance.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4314994623) **RyanCavanaugh** noted that invariant arrays brought a huge host of problems not addressed in the issue and referenced microsoft/TypeScript#18770
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4321125933) **JustFly1984** said "@RyanCavanaugh thanks, I will track the progress, I thought this repo will continue with typescript 7+."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4321126851) **JustFly1984** said "holy cow this issue is 9 years old..."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4328559427) **RyanCavanaugh** stated the plan was to move discussion back to the TypeScript repo and noted that longstanding issues were hard to fix

### [PR microsoft/TypeScript-go#3595](https://github.com/microsoft/TypeScript-go/pull/3595) (Closed)

**Don't cancel refresh except on file change**

*Cancel diagnostics refresh only on client file-change notifications instead of open/close/save events to prevent stale diagnostics.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3600](https://github.com/microsoft/TypeScript-go/issues/3600) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behaviour differences observed when plain js class getter return null in conditional branch**

*TypeScript and tsgo differ in inferring nullability of JavaScript class getters, causing inconsistent errors on property access.*

 * (2 days ago) **ahejlsberg** added labels `bug`, `Domain: Type Checking`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4321250824) **hkleungai** observed that moving the map assignment into the constructor caused errors in tsgo but not in tsc and updated the comment to include both cases
 * (today) **ahejlsberg** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4333661647) **hkleungai** reported that 7.0.0-dev.20260428.1 only partially resolved the issue, shared new tsgo errors, and asked whether to reopen the issue or open a new one

### [Issue microsoft/TypeScript-go#3607](https://github.com/microsoft/TypeScript-go/issues/3607) (Closed, `bug`, `Domain: Editor`, **ahejlsberg**)

**Missing hover for nullable method in type and interface**

*Hover tooltips for optional methods declared in type aliases and interfaces are not displayed in VS Code’s TypeScript extension.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3607#issuecomment-4320395685) **Withered-Flower-0422** identified missing '?' suffix for nullable property and method and missing hover output in tsgo
 * (today) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3608](https://github.com/microsoft/TypeScript-go/pull/3608) (Closed)

**Reparse JSDoc annotations on get accessors**

*Reparse JSDoc annotations on getter accessors to ensure accurate metadata extraction.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3608#issuecomment-4329720012) **hkleungai** asked if the PR also addressed other errors raised in issue #3600 and suggested adding a new testcase file documenting example codes
 * [today](https://github.com/microsoft/TypeScript-go/pull/3608#issuecomment-4329740792) **Andarist** questioned what typing a setter would imply in the given examples
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3609](https://github.com/microsoft/TypeScript-go/pull/3609) (Closed)

**Fix hover for optional method members in types and interfaces**

*Recover signatures for optional method members to ensure hover tooltips display correctly in types and interfaces*

 * created by **MukundaKatta**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3609#issuecomment-4329172394) **ahejlsberg** said "@MukundaKatta Appreciate the PR, but this isn't quite the right fix. See #3620."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3609#issuecomment-4329522556) **MukundaKatta** said "Thanks @ahejlsberg, makes sense. #3620 looks like the cleaner fix at the source. Closing this in favor of yours."
 * (today) **MukundaKatta** closed the issue

### [Issue microsoft/TypeScript-go#3610](https://github.com/microsoft/TypeScript-go/issues/3610) (Open)

**API: additional Checker methods for transpiler consumers \(follow\-up to \#3403\)**

*Extend tsgo's IPC Checker with additional high-priority TypeChecker methods identified from transpiler usage data.*

 * created by **RealColdFry**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3610#issuecomment-4329142502) **andrewbranch** thanked for the list and asked if anything outside the checker is missing or if the list fully unblocks migration

### [Issue microsoft/TypeScript-go#3612](https://github.com/microsoft/TypeScript-go/issues/3612) (Open)

**Intermittent tsgo build failures with incorrect inferences**

*tsgo intermittently misinfers arktype-inferred referenced types as empty objects, causing build failures in incremental builds*

 * created by **kwonoj**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4330636333) **jakebailey** suggested trying --checkers 1, --singleThreaded, and disabling incremental mode, and asked if the code is public or could be shared under NDA
 * [today](https://github.com/microsoft/TypeScript-go/issues/3612#issuecomment-4330791306) **kwonoj** suggested trying --checkers 1 or --singleThreaded, noted one fixed the issue but forgot which, said the code is private and asked if they'd sign an NDA

### [Issue microsoft/TypeScript-go#3615](https://github.com/microsoft/TypeScript-go/issues/3615) (Open, **andrewbranch**, **Copilot**)

**Server stops responding after \`Running scheduled diagnostics refresh\`**

*The TypeScript language server hangs after running scheduled diagnostics refresh in large monorepos with many open editors and file system event bursts.*

 * created by **ekazakov14**
 * (today) **andrewbranch** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Open)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * created by **kuishou68**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4323606759) **jakebailey** said "This will require a test, preferably one we can cross check with the old code to double check it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4331007584) **DanielRosenwasser** said "As far as I remember, this code path isn't supposed to be hit for an exact match. Did you actually run into a problem with a specific project?"

### [PR microsoft/TypeScript-go#3619](https://github.com/microsoft/TypeScript-go/pull/3619) (Open)

**perf: Make \`NodeArray\` no longer inherit from \`Array\`**

*Detach NodeArray from Array prototype to prevent direct array method usage and achieve significant performance gains.*

 * created by **liuxingbaoyu**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-4329156551) **andrewbranch** asked what made inheriting from Array expensive for materialization and guessed it was due to removing numeric index getters
 * [today](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-4329869917) **liuxingbaoyu** said "Yes, the issue is that Object.defineProperty is slow."

### [PR microsoft/TypeScript-go#3620](https://github.com/microsoft/TypeScript-go/pull/3620) (Closed)

**Quick info signature display for optional members**

*Enable quick info tooltips to display signatures for optional class or interface members.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621) (Open, `Crash`)

**Panic Alert Notification when Cursor edits some file and opening that file causes panic\.**

*Opening or editing a file causes a panic in the semanticTokens request because a token improperly spans multiple lines.*

 * created by **RealHaris**
 * **RealHaris** added label `Crash`

### [Issue microsoft/TypeScript-go#3622](https://github.com/microsoft/TypeScript-go/issues/3622) (Closed)

**Assertion violation in signature help for \`import\.defer\(\)\`**

*Requesting signature help for import.defer() in TypeScript causes an internal assertion failure and server panic.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3622#issuecomment-4329319389) **DanielRosenwasser** said "Note this crashes in the Strada codebase as well."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3623](https://github.com/microsoft/TypeScript-go/pull/3623) (Closed)

**Prefer project\-reference paths over workspace symlink paths**

*Use project-reference file paths rather than workspace symlink paths for module imports.*

 * created by **kbrooks**
 * (today) **kbrooks** closed the issue

### [PR microsoft/TypeScript-go#3624](https://github.com/microsoft/TypeScript-go/pull/3624) (Open, **RyanCavanaugh**, **Copilot**)

**Elide bare side\-effect imports in JS declaration emit**

*Omit bare side-effect imports from JS file .d.ts outputs while preserving them for TS files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3625](https://github.com/microsoft/TypeScript-go/issues/3625) (Open, **DanielRosenwasser**, **Copilot**)

**Formatting fails for entire file when a line contains only whitespace between two comments**

*When a line contains only whitespace between two single-line comments, the TypeScript/JavaScript formatter fails to indent the entire file.*

 * created by **glitcher255**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3626](https://github.com/microsoft/TypeScript-go/pull/3626) (Closed)

**fix\(3622\): prevent panic in signature help for import\.defer**

*Prevent panics in signature help when processing import.defer statements.*

 * created by **a-tarasyuk**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3627](https://github.com/microsoft/TypeScript-go/pull/3627) (Open)

**Runtime tracing, flight recording**

*Integrate Go runtime/trace support and flight recording into the VS Code extension similarly to pprof profiling.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3628](https://github.com/microsoft/TypeScript-go/pull/3628) (Open, **andrewbranch**, **Copilot**)

**Fix server hang after "Running scheduled diagnostics refresh"**

*Unbounded diagnostic and watch waits causing server hangs are fixed by non-blocking refresh, timed rollback, and a watch registry.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4336939973) **andrewbranch** said "@copilot fix review comments"

### [Issue microsoft/TypeScript-go#3629](https://github.com/microsoft/TypeScript-go/issues/3629) (Closed, `Crash`, **ahejlsberg**)

**Request failures from printing nodes in quick info/completions**

*Quick info and completion requests for generic instances cause the TypeScript-Go language server to panic on unhandled property access type nodes.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3629#issuecomment-4330810264) **DanielRosenwasser** said "Probably related to #3412."
 * (today) **ahejlsberg** added label `Crash`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3629#issuecomment-4331559630) **gabritto** noted that the fix in #3517 was undone when a later commit merged due to merge queue issues
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3630](https://github.com/microsoft/TypeScript-go/pull/3630) (Open, **DanielRosenwasser**, **Copilot**)

**Fix formatting failure when whitespace\-only line exists between single\-line comments**

*Whitespace-only lines between single-line comments cause overlapping delete edits in formatting, fixed by ensuring startPos only advances forward.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3630#issuecomment-4331257440) **Copilot** reported the fix in commit 22e4165a by replacing the compiler test with a fourslash formatting test

### [Issue microsoft/TypeScript-go#3631](https://github.com/microsoft/TypeScript-go/issues/3631) (Open, `Domain: Editor`, **DanielRosenwasser**)

**New untitled files are not correctly managed by config file status bar indicator**

*Unsaved TypeScript buffers in VS Code erroneously display the previous project's tsconfig.json status until editor focus changes, after which they show “No tsconfig”.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3632](https://github.com/microsoft/TypeScript-go/issues/3632) (Closed)

**Semantic Tokens are commented out again**

*Semantic tokens support was inadvertently commented out again in a squash commit, and clarification is requested on whether this change was intentional or accidental.*

 * created by **zeehjr**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3632#issuecomment-4331398849) **jakebailey** said "Oh no. We lost a lot more commits in the merge queue bug than I thought "
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3633](https://github.com/microsoft/TypeScript-go/pull/3633) (Closed)

**Handle property access expressions in type node serialization**

*Add support for serializing property access expressions within type nodes.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3633#issuecomment-4331550998) **jakebailey** noted that more changes from main were missing due to the merge queue bug and outage
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3634](https://github.com/microsoft/TypeScript-go/pull/3634) (Closed)

**Restore 4 more lost PRs**

*Restore four pull requests (#3328, #3445, #3502, #3513) lost due to a merge queue bug and fix issue #3632.*

 * created by **jakebailey**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3635](https://github.com/microsoft/TypeScript-go/issues/3635) (Open, `Crash`)

**When entering "\<" in it, it will panic**

*Typing '<' triggers a panic in the TypeScript language server’s signatureHelp handler due to a 'Not a subspan' assertion failure.*

 * created by **liy010**
 * **liy010** added label `Crash`

### [PR microsoft/TypeScript-go#3636](https://github.com/microsoft/TypeScript-go/pull/3636) (Open)

**Fix signature help crash in WIP JSX text on opening \`\<\`**

*Resolve a crash in TypeScript signature help triggered by typing an opening “<” in work-in-progress JSX text*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3637](https://github.com/microsoft/TypeScript-go/issues/3637) (Closed, `Domain: Editor`)

**"import" is highlighted as a keyword in Node\.js "import\.meta\.dirname" expression**

*VS Code’s JavaScript syntax highlighting incorrectly marks the “import” in import.meta.dirname as a keyword.control.import token*

 * created by **hisbvdis**
 * **hisbvdis** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3637#issuecomment-4335843006) **jakebailey** clarified that the language support is from the TypeScript-TmLanguage shipped with VS Code rather than their extension and referred to issue #3632 for missing semantic tokens
 * [later](https://github.com/microsoft/TypeScript-go/issues/3637#issuecomment-4335852658) **hisbvdis** thanked the maintainer for the answer and apologized for the bother
 * (later) **hisbvdis** closed the issue

### [Issue microsoft/TypeScript-go#3638](https://github.com/microsoft/TypeScript-go/issues/3638) (Open, `Domain: Editor`)

**Cannot find name html element\.**

*Closing div tags in .tsx files intermittently trigger “Cannot find name 'div'” errors in VS Code’s TypeScript language server until it’s restarted.*

 * created by **Netail**
 * **Netail** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4335853459) **jakebailey** said "We would really need a repro, or at least some logs"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4335893311) **Netail** explained that the issue occurred randomly across multiple TSX files and offered to provide logs

### [Issue microsoft/TypeScript-go#3639](https://github.com/microsoft/TypeScript-go/issues/3639) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behaviour differences: plain js's ternary assignment of objects in different shapes confuses tsgo**

*tsgo does not detect a missing 'message' property error when destructuring objects assigned with a ternary operator in JavaScript code, unlike TypeScript 6*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#3640](https://github.com/microsoft/TypeScript-go/pull/3640) (Closed)

**Restore \#3529**

*Restore PR #3529 which was accidentally reverted due to a merge queue bug.*

 * created by **gabritto**

