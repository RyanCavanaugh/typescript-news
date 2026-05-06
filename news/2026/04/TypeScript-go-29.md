# Report for 2026-04-29 (Wednesday, April 29th, 2026)

10 different users commented on 20 different issues.

## Recommended Actions

 * Response Recommended
    * @RealColdFry asked about ast/*/enums/* subpath stability in [microsoft/TypeScript-go#3610](https://github.com/microsoft/TypeScript-go/issues/3610#issuecomment-4351861910)
    * @Netail provided logs and error context as requested in [microsoft/TypeScript-go#3638](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4351168228)
    * @hkleungai asked if `@param {Object} [x]` should imply `?:` as the optional marker in [microsoft/TypeScript-go#3656](https://github.com/microsoft/TypeScript-go/issues/3656#issuecomment-4345631041)
    * @kbrooks provided requested company affiliation in [microsoft/TypeScript-go#3664](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4347528448)

## Activity Summary

### [PR microsoft/TypeScript-go#3403](https://github.com/microsoft/TypeScript-go/pull/3403) (Closed)

**Exposing more endpoints**

*Expose additional API endpoints to expand available functionality.*

 * created by **navya9singh**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **navya9singh** closed the issue

### [Issue microsoft/TypeScript-go#3610](https://github.com/microsoft/TypeScript-go/issues/3610) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API: additional Checker methods for transpiler consumers \(follow\-up to \#3403\)**

*Extend tsgo's IPC Checker with additional high-priority TypeChecker methods identified from transpiler usage data.*

 * created by **RealColdFry**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3610#issuecomment-4329142502) **andrewbranch** thanked for the list and asked if anything outside the checker is missing or if the list fully unblocks migration
 * [later](https://github.com/microsoft/TypeScript-go/issues/3610#issuecomment-4351861910) **RealColdFry** listed the remaining API gaps for the TSTL feature, including missing Program methods and checker-side accessors
 * (later) **andrewbranch** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#3628](https://github.com/microsoft/TypeScript-go/pull/3628) (Closed, **andrewbranch**, **Copilot**)

**Fix server hang after "Running scheduled diagnostics refresh"**

*Convert scheduled diagnostics refresh to non-blocking and introduce per-request timeouts, watcher deduplication, and registry encapsulation to prevent server deadlocks.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4338359955) **andrewbranch** said "@copilot write a test for the updateWatch timeout and retry. I think you should be able to mock the client implementation using synctest."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4338480676) **Copilot** added synctest subtests verifying that a slow client triggers timeout and rollback and that a subsequent call succeeds
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4339083623) **Copilot** rewrote the test for updateWatch timeout and retry using real session operations and synctest, mocking WatchFilesFunc to block on the first batch and verifying that after a timeout-induced rollback the registry remained clean for re-registration
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4345426618) **andrewbranch** said "@copilot address review comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3628#issuecomment-4345569244) **Copilot** addressed all five review comments in commit 22abe61, including changes to refcount rollback on error, consistent locking requirements, per-request timeouts, duplicate-pattern deduplication, and stronger test assertions

### [Issue microsoft/TypeScript-go#3638](https://github.com/microsoft/TypeScript-go/issues/3638) (Open, `Domain: Editor`)

**Cannot find name html element\.**

*Closing div tags in .tsx files intermittently trigger “Cannot find name 'div'” errors in VS Code’s TypeScript language server until it’s restarted.*

 * **Netail** added label `Domain: Editor`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4335853459) **jakebailey** said "We would really need a repro, or at least some logs"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4335893311) **Netail** explained that the issue occurred randomly across multiple TSX files and offered to provide logs
 * [later](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4351168228) **Netail** attached log file and described that the error occurred spontaneously on a large TSX file after idling

### [PR microsoft/TypeScript-go#3649](https://github.com/microsoft/TypeScript-go/pull/3649) (Closed, **RyanCavanaugh**, **Copilot**)

**Add TS\_GO\_DEBUG\_STACK\_LIMIT to cap goroutine stack size at entry points**

*Add an opt-in TS_GO_DEBUG_STACK_LIMIT environment variable to configure and enforce goroutine stack size caps at startup.*

 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3649#issuecomment-4339647092) **RyanCavanaugh** tested stack limit thresholds and observed instant failure at 1,000,000 with 3,000 elided frames and fast execution at 5,000,000 with 28,000 elided frames, recommending the latter for local development
 * [today](https://github.com/microsoft/TypeScript-go/pull/3649#issuecomment-4345431990) **jakebailey** discussed the choice of the TSGO prefix and questioned how much 'Go' should be included in names
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3655](https://github.com/microsoft/TypeScript-go/issues/3655) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: Pattern matching against \`extends { \[P in K\]?: unknown }\` emit slightly different error in tsgo**

*tsgo inconsistently expands mapped type constraint { [P in K]?: unknown } in generics, causing different errors than tsc*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3655#issuecomment-4346081658) **ahejlsberg** said "I think the tsgo behavior is quite reasonable here. In general, tsgo tries harder to print back what was actually written."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3655#issuecomment-4346415073) **hkleungai** expressed doubt about the intent, provided a code example, and noted that the printed output's type syntax was complex and harder to comprehend than TS 6's output

### [Issue microsoft/TypeScript-go#3656](https://github.com/microsoft/TypeScript-go/issues/3656) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Optional marking with jsdoc does not correctly treat param as undefined**

*JSDoc optional parameter marking in tsgo fails to include undefined in the parameter type, causing null assignment errors.*

 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, and set milestone to `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3656#issuecomment-4345409706) **jakebailey** asked whether it was a bug and noted that TypeScript produces the same error
 * [today](https://github.com/microsoft/TypeScript-go/issues/3656#issuecomment-4345631041) **hkleungai** said "@param {Object} [x] should imply ?: I think. Isn't this what optional marker used for?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3656#issuecomment-4345653744) **jakebailey** said "Right, but that's what = is already in TS."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3656#issuecomment-4345666172) **jakebailey** demonstrated that the change didn’t prevent accepting undefined externally
 * [today](https://github.com/microsoft/TypeScript-go/issues/3656#issuecomment-4345712197) **hkleungai** said "Looks like I am re-learning typescript fundamental here... TS 6 gives an impression that an undefined is not an Object...."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3656#issuecomment-4345840305) **ahejlsberg** suggested reparsing parameters as optional with initializers to match Strada behavior and suppress errors
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3657](https://github.com/microsoft/TypeScript-go/issues/3657) (Closed, `wontfix`)

**Behavior difference: TS2349 error does not tell resolution\-mode in tsgo**

*tsgo’s TS2349 error output omits the resolution-mode annotation that tsc includes under nodenext module resolution.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3657#issuecomment-4345351366) **jakebailey** said "I have no idea why 6.0 would print it that way, when the import statement does not have  resolution-mode written?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3657#issuecomment-4346066058) **ahejlsberg** said "Yeah, don't think we want to change anything here."
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3659](https://github.com/microsoft/TypeScript-go/issues/3659) (Open)

**Behavior difference: JSDoc comments are stripped for mapped types**

*Mapped types in TypeScript 7 beta strip JSDoc comments from original properties, unlike TypeScript 6.0.3.*

 * created by **andrewzolotukhin**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3659#issuecomment-4346021402) **Withered-Flower-0422** said "Maybe related to #3405 ?"

### [PR microsoft/TypeScript-go#3660](https://github.com/microsoft/TypeScript-go/pull/3660) (Closed)

**Always reparse bracketed \`@param\` names into \`?\` modifiers**

*Reparse bracketed @param names as optional parameters by converting them into question mark modifiers.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3660#issuecomment-4346062582) **jakebailey** said "I think you should also delete this entry: https://github.com/microsoft/typescript-go/blob/main/CHANGES.md#optional-marking-on-parameter-names-now-makes-the-parameter-both-optional-and-undefined"
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3661](https://github.com/microsoft/TypeScript-go/issues/3661) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo emits an "extra" TS7006 along with TS2769 at the same line in case of overload mismatch**

*tsgo redundantly emits both TS2769 and TS7006 errors for an overload mismatch call, unlike tsc.*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#3662](https://github.com/microsoft/TypeScript-go/issues/3662) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo wrongly allows \`include\` to contain files that is not under \`rootDir\` from tsconfig**

*tsgo incorrectly permits including files outside the configured rootDir in tsconfig without reporting errors.*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#3663](https://github.com/microsoft/TypeScript-go/pull/3663) (Open)

**Fix hover JSDoc for mapped type properties**

*Fix hover tooltips to correctly display JSDoc comments for mapped type properties*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3664](https://github.com/microsoft/TypeScript-go/pull/3664) (Open)

**Align dependency symlink handling with TS6 for module specifiers**

*Align tsgo’s dependency symlink cache with TypeScript 6 by using normal module resolution to respect paths mappings in declaration emits.*

 * created by **kbrooks**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4347464727) **kbrooks** agreed with the policy service and indicated affiliation with Snap Inc.
 * [today](https://github.com/microsoft/TypeScript-go/pull/3664#issuecomment-4347528448) **kbrooks** agreed to policy request and specified company as Snap Inc.

### [Issue microsoft/TypeScript-go#3665](https://github.com/microsoft/TypeScript-go/issues/3665) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: jsdoc typing on child class member overrides parent class's type in tsgo but not in tsc**

*tsgo incorrectly reports an error when a child class’s JSDoc-typed state property overrides its parent class’s type, while tsc accepts it.*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#3666](https://github.com/microsoft/TypeScript-go/issues/3666) (Open, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo does not \(fully\) respect jsdoc \`@extend\` clause**

*tsgo fails to report mismatched JSDoc @extends errors for JS classes, unlike tsc which correctly flags them.*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#3667](https://github.com/microsoft/TypeScript-go/issues/3667) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Assigning array to uninitialized class members yields different error on tsc & tsgo**

*Assigning arrays to uninitialized class members in JavaScript triggers different implicit any and type inference errors in tsc vs tsgo.*

 * created by **hkleungai**

