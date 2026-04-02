# Report for 2026-03-29 (Sunday, March 29th, 2026)

8 different users commented on 24 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234) (Closed, `Needs More Info`)

**tsgo eagerly resolve the type of inferred function Expression**

*tsgo eagerly resolves inferred function expression types, causing Record<keyof TestInterface, string> to collapse to Record<never, string> without explicit annotations.*

 * (2 days ago) **RyanCavanaugh** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-4144822504) **brokenmass** said "@RyanCavanaugh would you be so kind to leave this open until I test the new build (tomorrow or Monday)?"
 * (2 days ago) **RyanCavanaugh** reopened the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-4155134019) **brokenmass** said "@RyanCavanaugh I'm happy to confirm that this bug is no longer present in latest code. thanks for the amazing work."
 * (later) **brokenmass** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-4155186328) **RyanCavanaugh** said "Thanks for confirming!"

### [Issue microsoft/TypeScript-go#2379](https://github.com/microsoft/TypeScript-go/issues/2379) (Closed, **andrewbranch**)

**TS2307 can't resolve type that import from pkg/dist directly**

*TypeScript fails to resolve types imported from a package’s dist folder, triggering TS2307 errors and any type fallbacks*

 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2379#issuecomment-3651559068) **ChangeHow** confirmed the same bundler mode bug and provided log output
 * (2 days ago) **RyanCavanaugh** added label `bug`, and assigned to **andrewbranch**
 * **andrewbranch** removed label `bug`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2379#issuecomment-4156059747) **andrewbranch** clarified that the "exports" field blocks deep imports of arbitrary files in node_modules packages and suggested using "resolvePackageJsonExports": false while warning against it
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2701](https://github.com/microsoft/TypeScript-go/issues/2701) (Closed)

**Declaration emit for named inferred types used in further inference inlines inferred types instead of naming them**

*tsgo inlines inferred types in declaration emit even when named, causing slower type checking in consuming packages.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3928362389) **jakebailey** asked to report the missing .d.ts files separately
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-3928857325) **privatenumber** said "Sorry about that — the 48 missing files were a measurement error on my end. Both tsc and tsgo produce all 4,710 .d.ts files. I've updated my previous comment with corrected numbers."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4137500062) **jakebailey** said "@chriskrycho Is this now fixed since #2459?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2701#issuecomment-4154924127) **RyanCavanaugh** mentioned that Nightly now emitted the expected code snippet
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2944](https://github.com/microsoft/TypeScript-go/pull/2944) (Open)

**\[draft\] more formatting tests **

*Add draft formatting tests to validate and troubleshoot the repository’s testing pipelines.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4113812716) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4114084080) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4148801620) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4152659049) **typescript-bot** provided the requested perf run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/2944#issuecomment-4152679800) **typescript-bot** said "@iisaduan, the perf run you requested failed. You can check the log here."

### [Issue microsoft/TypeScript-go#3027](https://github.com/microsoft/TypeScript-go/issues/3027) (Closed)

**New TS2883 "\.\.\. cannot be named \.\.\." error exporting an arrow function\.**

*Arrow-exported functions with CSSProperties['cursor'] return types trigger TS2883 in TS 7.0 preview due to unnamed csstype dependencies, unlike function declarations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4020873172) **simonbuchan** highlighted another styled-components variant that may be harder to workaround and noted uncertainty about its TypeScript behavior
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4020989945) **hkleungai** noted a potential duplicate of issues #2911 and #2504 and expressed hope for more attention from the TypeScript team
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4021083531) **simonbuchan** said "Those are TS4023 and TS4053 so they are at least hitting a different code path, but there does seem to be some relation."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3027#issuecomment-4155024237) **RyanCavanaugh** reported that nightly now emitted the foo and bar declarations without error
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3072](https://github.com/microsoft/TypeScript-go/issues/3072) (Closed)

**getTargetOfType panics on non\-generic types via the api server**

*getTargetOfType panics on intersection or union types instead of returning null as expected*

 * created by **souporserious**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3072#issuecomment-4154998438) **RyanCavanaugh** disagreed with the assessment that returning an error rather than null is semantically correct, argued that returning null implies a successful operation and conflates illegal and legal nil targets
 * [later](https://github.com/microsoft/TypeScript-go/issues/3072#issuecomment-4156038896) **RyanCavanaugh** noted that the TS API restricts calls to legal types, so this case is analogous to other malformed requests triggering asserts
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3291](https://github.com/microsoft/TypeScript-go/pull/3291) (Closed)

**Fix import require error**

*Update error reporting to remove TypeScript references in JavaScript files and eliminate unused parameters in error methods.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3292](https://github.com/microsoft/TypeScript-go/pull/3292) (Closed)

**Fix rune iteration bugs**

*Fix three bugs in rune iteration over strings discovered while writing a lint rule for string range operations.*

 * created by **jakebailey**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3293](https://github.com/microsoft/TypeScript-go/pull/3293) (Closed)

**Accept baseline diffs, round 2**

*Accepts a second batch of baseline diffs to update the project’s accepted baselines.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#3295](https://github.com/microsoft/TypeScript-go/pull/3295) (Closed)

**Fixed a completion crash after invalid token in array literal**

*Prevents autocompletion from crashing due to invalid tokens in array literals.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3296](https://github.com/microsoft/TypeScript-go/pull/3296) (Closed)

**Fixed a call hierarchy crash in arrow prop declaration in exported default class**

*Fixes call hierarchy crash caused by arrow property declaration in an exported default class*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3297](https://github.com/microsoft/TypeScript-go/pull/3297) (Open)

**Allow global Symbol computed names during pseudochecker object literal serialization**

*Support global Symbol computed property names in pseudochecker object literal serialization to match Strada’s behavior.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3298](https://github.com/microsoft/TypeScript-go/pull/3298) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump codecov/codecov-action from 5.5.3 to 6.0.0 and update github/codeql-action to the latest version in the root directory workflows.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * (later) **jakebailey** closed the issue

