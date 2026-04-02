# Report for 2026-03-19 (Thursday, March 19th, 2026)

14 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @ppoulard provided a solution for wrapping React elements in Web components in [microsoft/TypeScript#52923](https://github.com/microsoft/TypeScript/issues/52923#issuecomment-4097969179)
    * @iluha168 reported a bug with lib implementation of Awaited in [microsoft/TypeScript#63244](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4092078699)
    * @AkaHarshit asked to approve workflows so CI tests can run in [microsoft/TypeScript#63256](https://github.com/microsoft/TypeScript/pull/63256#issuecomment-4097446197)
    * @ace-tk asked for a review of the fixes they made in [microsoft/TypeScript#63276](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4097328396)
    * @brillout asked if collaborating with the TypeScript team could accelerate the adoption of function decorators in [microsoft/TypeScript#7318](https://github.com/microsoft/TypeScript/issues/7318#issuecomment-4096519815)
    * @menocomp asked why this issue was raised in TypeScript instead of JavaScript after ten years in [microsoft/TypeScript#7318](https://github.com/microsoft/TypeScript/issues/7318#issuecomment-4096584165)

## Activity Summary

### [Issue microsoft/TypeScript#2944](https://github.com/microsoft/TypeScript/issues/2944) (Closed, `Suggestion`, `Declined`, `Too Complex`)

**Support Pluggable, 3rd\-party Type Systems**

*Request to support pluggable third-party type assertion libraries in TypeScript via tsconfig.json.*

 * (10.9 years ago) **danquirk** added labels `Declined`, `Too Complex`
 * [today](https://github.com/microsoft/TypeScript/issues/2944#issuecomment-4093101525) **iisaduan** said "Sorry about the spam-- bot's posting to the wrong repo :/. I think I fixed it but might take a bit to register"

### [Issue microsoft/TypeScript#52923](https://github.com/microsoft/TypeScript/issues/52923) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow \`this\` parameter in property accessors \(getter/setter\)**

*Allow specifying a typed this parameter in TypeScript property getters and setters.*

 * [3 years ago](https://github.com/microsoft/TypeScript/issues/52923#issuecomment-1456920694) **fatcerberus** expressed confusion about the practice of phrasing developer expectations in terms of what ChatGPT would want
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/52923#issuecomment-1708103789) **matAtWork** asked for guidance on implementing support for prototype-based getters and setters in TypeScript
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/52923#issuecomment-2561772059) **magicdawn** disputed the fix for issue #36883, arguing that cheating the TS compiler’s this type should allow no type error despite a runtime failure
 * [later](https://github.com/microsoft/TypeScript/issues/52923#issuecomment-4097969179) **ppoulard** provided a code snippet demonstrating how to wrap React elements in Web components by assigning a getter to TabElement.prototype returning the child nodes

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087494508) **newives** reported that the TypeScript 6.0 Final Release job failed to launch
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087508959) **jakebailey** said "That run is unrelated to a release."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087648587) **newives** asked if a specific release date was available
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4094003838) **simonbuchan** joked about looking like a fool for promising the release on the 17th

### [Issue microsoft/TypeScript#63244](https://github.com/microsoft/TypeScript/issues/63244) (Open, `Needs Proposal`)

**bug\(lib\): Explicitly stating wrong return type of \`Promise\.then\` without arguments results in no error**

*Current TypeScript versions fail to report a type mismatch when Promise<string> is assigned from Promise.resolve(1).then() with no arguments.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4050549212) **Andarist** mentioned another instance of .then's typing affecting a scenario negatively and linked to a related TypeScript issue
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4055854137) **paigefletcher1282-code** reported that the issue hadn't yet been reproduced and linked to issue #62071
 * **RyanCavanaugh** added label `Needs Proposal`
 * [today](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4092078699) **iluha168** mentioned that their overload idea solved the sample code, provided a playground link, and reported encountering a bug with Awaited implementation

### [PR microsoft/TypeScript#63256](https://github.com/microsoft/TypeScript/pull/63256) (Closed)

**fix: improve confusing TS1107 error for mislabeled jump targets**

*The compiler now only emits TS1107 for jump labels crossing function boundaries, otherwise emitting missing label errors.*

 * created by **AkaHarshit**
 * [later](https://github.com/microsoft/TypeScript/pull/63256#issuecomment-4097446197) **AkaHarshit** requested workflow approval for CI tests after signing the CLA

### [PR microsoft/TypeScript#63261](https://github.com/microsoft/TypeScript/pull/63261) (Closed, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.4\.1 to 5\.5\.6**

*Upgrade fast-xml-parser from v5.4.1 to v5.5.6 for various bug fixes, performance improvements, and new features.*

 * (2 days ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript/pull/63261#issuecomment-4094744442) **dependabot[bot]** said "Superseded by #63272."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63264](https://github.com/microsoft/TypeScript/issues/63264) (Closed, `Duplicate`)

**Return statement required even when not needed**

*TypeScript incorrectly requires a return statement in an exhaustively covered function over a closed union, causing a missing return error.*

 * created by **eliashakuni**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63264#issuecomment-4081968705) **MartinJohns** said "Duplicate of #21985."
 * **RyanCavanaugh** added label `Duplicate`
 * [later](https://github.com/microsoft/TypeScript/issues/63264#issuecomment-4097300406) **Withered-Flower-0422** suggested writing testFunction with an ArgType union and throwing an error for invalid arguments

### [Issue microsoft/TypeScript#63268](https://github.com/microsoft/TypeScript/issues/63268) (Closed, `Bug`, `Fixed`)

**Crash: TypeError: Cannot read properties of undefined \(reading 'flags'\) at tryGetDeclaredTypeOfSymbol when using typeof this in arrow function parameter**

*Using 'typeof this' in an arrow function parameter triggers a TypeError crash in the TypeScript compiler.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/63268#issuecomment-4093869797) **RyanCavanaugh** noted that TS7 now prints two errors in a.ts about assignability and capturing global this
 * (today) **RyanCavanaugh** added labels `Bug`, `Fixed`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63269](https://github.com/microsoft/TypeScript/issues/63269) (Open, `Bug`, `Domain: check: Type Circularity`)

**Regression: RangeError: Maximum call stack size exceeded in instantiateTypeWorker with recursive intersections and invalid type queries**

*Recursive intersection and invalid type query patterns cause a RangeError maximum call stack size exceeded in instantiateTypeWorker in TypeScript 5.7.3 through 5.9.3 and nightly builds.*

 * created by **na7ure-a**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63269#issuecomment-4093876109) **RyanCavanaugh** said "Confirmed repro in TS7"

### [Issue microsoft/TypeScript#63270](https://github.com/microsoft/TypeScript/issues/63270) (Open, `Bug`, `Domain: check: Type Circularity`)

**Crash: RangeError: Maximum call stack size exceeded in isRelatedTo with recursive tuple types and spread elements**

*TypeScript's type checker overflows the call stack when processing recursive variadic tuple types with spread elements.*

 * created by **na7ure-a**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63271](https://github.com/microsoft/TypeScript/issues/63271) (Open, `Bug`, `Domain: Crashes`)

**Crash: RangeError: Invalid string length in addSpans during instantiation of recursive template literal types**

*TypeScript crashes with a RangeError due to exponential string growth in deeply recursive template literal type instantiation*

 * created by **na7ure-a**

### [PR microsoft/TypeScript#63272](https://github.com/microsoft/TypeScript/pull/63272) (Closed, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.4\.1 to 5\.5\.7**

*Bump fast-xml-parser dependency from 5.4.1 to 5.5.7 to include performance improvements, security fixes, and new features.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`

### [Issue microsoft/TypeScript#63273](https://github.com/microsoft/TypeScript/issues/63273) (Open, `Bug`, `Domain: check: Type Circularity`)

**Crash: RangeError: Maximum call stack size exceeded in getNameOfSymbolAsWritten via recursive conditional ReturnType**

*The TypeScript compiler crashes with a maximum call stack size exceeded error when handling a recursive conditional ReturnType in a clone function.*

 * created by **na7ure-a**

### [Issue microsoft/TypeScript#63274](https://github.com/microsoft/TypeScript/issues/63274) (Open, `Bug`, `Domain: Error Messages`, `i18n`)

**\[Localization\] Misleading Chinese translation for TS2561 error message**

*The Chinese translation for TS2561 error message incorrectly swaps the property and type relationship, causing confusion and requiring correction.*

 * created by **HHaoWang**

### [Issue microsoft/TypeScript#63275](https://github.com/microsoft/TypeScript/issues/63275) (Closed, `Question`)

**TypeScript enum emit inconsistency**

*TypeScript 5.x now emits enum members with const string values as string-enum style instead of reverse-mapping, influenced by annotations.*

 * created by **magic-akari**

### [Issue microsoft/TypeScript#63276](https://github.com/microsoft/TypeScript/issues/63276) (Closed)

**Missing \`undefined\` for hover**

*VSCode's hover tooltip for a type with several optional properties only displays '| undefined' on the first property, omitting it on the others when exactOptionalPropertyTypes is false.*

 * created by **Withered-Flower-0422**
 * [later](https://github.com/microsoft/TypeScript/issues/63276#issuecomment-4097328396) **ace-tk** said "Can u please review the fixes i made."

### [PR microsoft/TypeScript#63277](https://github.com/microsoft/TypeScript/pull/63277) (Closed)

**fixed issue GH\#63276**

*The pull request titled “fixed issue GH#63276” lacks the required associated issue reference, up-to-date code, tests, and completed contribution checklist items.*

 * created by **ace-tk**

### [Issue microsoft/TypeScript#7318](https://github.com/microsoft/TypeScript/issues/7318) (Open, `Suggestion`, `Domain: Decorators`, `Waiting for TC39`)

**allow decorators for functions**

*Allow decorators to be applied to standalone functions in addition to classes, methods, and properties.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/7318#issuecomment-1541186557) **nowaysgit** said "1 !"
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/7318#issuecomment-1756081761) **tareksaleem** proposed a hack to transpile TypeScript decorator syntax using higher-order functions and asked how the compiler could implement this transformation
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/7318#issuecomment-1756817523) **MartinJohns** stated that hacks were explicitly out of scope for TypeScript
 * [later](https://github.com/microsoft/TypeScript/issues/7318#issuecomment-4096519815) **brillout** listed the new TC39 proposal repos for function and object literal element decorators and asked if collaborating with the TypeScript team could accelerate the adoption of function decorators
 * [later](https://github.com/microsoft/TypeScript/issues/7318#issuecomment-4096584165) **menocomp** questioned why the issue was raised in TypeScript rather than JavaScript after ten years

