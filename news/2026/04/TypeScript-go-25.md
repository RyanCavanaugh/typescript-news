# Report for 2026-04-25 (Saturday, April 25th, 2026)

13 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @RealHaris asked if the semantic tokens error had been resolved in [microsoft/TypeScript-go#3441](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4320897495)
    * @hkleungai provided repro steps demonstrating the issue with map assignment in constructor in [microsoft/TypeScript-go#3600](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4321250824)
    * @Withered-Flower-0422 reported missing nullable suffix and hover information in tsgo output in [microsoft/TypeScript-go#3607](https://github.com/microsoft/TypeScript-go/issues/3607#issuecomment-4320395685)

## Activity Summary

### [Issue microsoft/TypeScript-go#3441](https://github.com/microsoft/TypeScript-go/issues/3441) (Closed, **jakebailey**, **Copilot**)

**Panic handling textDocument/semanticTokens/{full,range}: slice bounds out of range and token\-spans\-multiple\-lines**

*Semantic tokens full and range handlers panic due to slice bounds out-of-range errors and multi-line token spans.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4285743482) **liby** clarified inability to share original files due to private codebase, corrected that both files were ASCII-only and that the panic was deterministic within a session, and provided verbose server logs with two panic instances showing semantic tokens spanning multiple lines errors
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4292366992) **jakebailey** said "I suspect #3483 will actually fix this. We'll see tomorrow."
 * (4 days ago) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4320897495) **RealHaris** reported an InternalError from textDocument/semanticTokens/full and asked if it was resolved
 * [today](https://github.com/microsoft/TypeScript-go/issues/3441#issuecomment-4320932292) **jakebailey** said "Please file a new issue, hopefully with a repro or LSP logs."

### [Issue microsoft/TypeScript-go#3576](https://github.com/microsoft/TypeScript-go/issues/3576) (Closed)

**\[Proposal\] strictArrayVariance: opt\-in invariance for mutable Array\<T\> element type \(post\-7\.0 discussion\)**

*Introduce a strictArrayVariance compiler option to enforce invariant element types on mutable arrays, preventing unsound covariance.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4313817349) **jakebailey** said "This is most certainly the wrong repo to file this in. We are not adding new features in 7.0. Those need to wait for 7.1, and will not be taken in this repo."
 * (yesterday) **RyanCavanaugh** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4314994623) **RyanCavanaugh** noted that invariant arrays brought a huge host of problems not addressed in the issue and referenced microsoft/TypeScript#18770
 * [today](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4321125933) **JustFly1984** said "@RyanCavanaugh thanks, I will track the progress, I thought this repo will continue with typescript 7+."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3576#issuecomment-4321126851) **JustFly1984** said "holy cow this issue is 9 years old..."

### [Issue microsoft/TypeScript-go#3585](https://github.com/microsoft/TypeScript-go/issues/3585) (Open)

**Remove extraneous \`declare\` in \.d\.ts output to better match strada**

*Remove extraneous declare modifiers from .d.ts output for both TypeScript and JavaScript*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3585#issuecomment-4320288542) **Andarist** noted that a change around ensureModifiers/maskModifierFlags wouldn't quite eliminate all diverging declare modifiers and linked a comparison

### [Issue microsoft/TypeScript-go#3600](https://github.com/microsoft/TypeScript-go/issues/3600) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behaviour differences observed when plain js class getter return null in conditional branch**

*TypeScript and tsgo differ in inferring nullability of JavaScript class getters, causing inconsistent errors on property access.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4319705569) **ahejlsberg** said "Looks like tsgo isn't picking up the JSDoc annotation on k1."
 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3600#issuecomment-4321250824) **hkleungai** observed that moving the map assignment into the constructor caused errors in tsgo but not in tsc and updated the comment to include both cases

### [PR microsoft/TypeScript-go#3606](https://github.com/microsoft/TypeScript-go/pull/3606) (Open)

**fix\(3605\): Missing generic param displayed in hover**

*Ensure generic type parameters are correctly displayed in hover tooltips.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#3607](https://github.com/microsoft/TypeScript-go/issues/3607) (Closed, `bug`, `Domain: Editor`, **ahejlsberg**)

**Missing hover for nullable method in type and interface**

*Hover tooltips for optional methods declared in type aliases and interfaces are not displayed in VS Code’s TypeScript extension.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3607#issuecomment-4320395685) **Withered-Flower-0422** identified missing '?' suffix for nullable property and method and missing hover output in tsgo

### [PR microsoft/TypeScript-go#3608](https://github.com/microsoft/TypeScript-go/pull/3608) (Closed)

**Reparse JSDoc annotations on get accessors**

*Reparse JSDoc annotations on getter accessors to ensure accurate metadata extraction.*

 * created by **ahejlsberg**

### [PR microsoft/TypeScript-go#3609](https://github.com/microsoft/TypeScript-go/pull/3609) (Closed)

**Fix hover for optional method members in types and interfaces**

*Recover signatures for optional method members to ensure hover tooltips display correctly in types and interfaces*

 * created by **MukundaKatta**

### [Issue microsoft/TypeScript-go#3610](https://github.com/microsoft/TypeScript-go/issues/3610) (Open)

**API: additional Checker methods for transpiler consumers \(follow\-up to \#3403\)**

*Extend tsgo's IPC Checker with additional high-priority TypeChecker methods identified from transpiler usage data.*

 * created by **RealColdFry**

### [Issue microsoft/TypeScript-go#3611](https://github.com/microsoft/TypeScript-go/issues/3611) (Open)

**Elevated CPU usage in \`\-\-watch\` mode when idle \(compared to tsc\)**

*tsgo --watch mode consistently consumes 5-10% CPU while idle, whereas tsc --watch mode remains at 0%.*

 * created by **alexswan93**

### [Issue microsoft/TypeScript-go#3612](https://github.com/microsoft/TypeScript-go/issues/3612) (Open)

**Intermittent tsgo build failures with incorrect inferences**

*tsgo intermittently misinfers arktype-inferred referenced types as empty objects, causing build failures in incremental builds*

 * created by **kwonoj**

### [Issue microsoft/TypeScript-go#3613](https://github.com/microsoft/TypeScript-go/issues/3613) (Open)

**Behaviour difference: merging \`interface\`s with identically named getter/setter pair and field**

*Merging interfaces with identical getter/setter and property definitions triggers duplicate identifier errors in tsgo but not in TypeScript 6.0.*

 * created by **mcpower**

### [PR microsoft/TypeScript-go#3614](https://github.com/microsoft/TypeScript-go/pull/3614) (Open)

**fix\(3613\): allow prop–accessor merging in interfaces**

*Allow property accessor merging in interfaces to support combined getter and setter declarations.*

 * created by **a-tarasyuk**

