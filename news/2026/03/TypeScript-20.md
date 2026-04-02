# Report for 2026-03-20 (Friday, March 20th, 2026)

3 different users commented on 10 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#50235](https://github.com/microsoft/TypeScript/issues/50235) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support inlay hint text edits**

*Enable JS/TS inlay hints to include text edits that add explicit type annotations upon double-click.*

 * created by **mjbvz**
 * (3.6 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/50235#issuecomment-4099335845) **insilications** said "TS/JS needs to adopt this"

### [Issue microsoft/TypeScript#62963](https://github.com/microsoft/TypeScript/issues/62963) (Open, `Meta-Issue`)

**Transition to 6\.0 Maintenance Mode**

*TypeScript 6.0 is now in maintenance mode, accepting only regression, deprecation, and crash fixes while the team prioritizes TypeScript 7.0.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3842750039) **RyanCavanaugh** said "@KnorpelSenf yep!"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3940657202) **jogibear9988** asked whether there was a plan for a WASM version of TypeScript 7.0 and how it would integrate into the Monaco editor or client-side websites
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3956082889) **RyanCavanaugh** said "WASM is definitely possible. The perf today is not super -- about on par with the JS codebase -- but it would hopefully get better over time as Go and/or browsers get better at it."
 * [today](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-4100336368) **RyanCavanaugh** enumerated PR merge criteria for post-6.0 changes

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087508959) **jakebailey** said "That run is unrelated to a release."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4087648587) **newives** asked if a specific release date was available
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4094003838) **simonbuchan** joked about looking like a fool for promising the release on the 17th
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4099966321) **RyanCavanaugh** said "We hit some issues when testing in Visual Studio, so 23 is the new 17"

### [Issue microsoft/TypeScript#63206](https://github.com/microsoft/TypeScript/issues/63206) (Open, `Bug`, `Help Wanted`, `Domain: Error Messages`)

**Confusing error message \(2322\), should use \(2741\) and \(2322\) error message when this\["XXX"\] = {\.\.\.} has a missing \(or mispelled\) key or an incompatible value\.**

*Improve TypeScript error messaging for this['XXX'] assignments by distinguishing missing property errors (2741) from type mismatches (2322).*

 * (2 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: Error Messages`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-3995817875) **denis-migdal** asked whether TypeScript could enforce explicit casts to signal intent for potentially unsafe assignments
 * [today](https://github.com/microsoft/TypeScript/issues/63206#issuecomment-4102579315) **WhiteMinds** traced the root cause and identified that reportRelationError discarded error elaboration for indexed access types, and proposed preserving errorInfo in that case (PR #63278)

### [Issue microsoft/TypeScript#63271](https://github.com/microsoft/TypeScript/issues/63271) (Open, `Bug`, `Domain: Crashes`)

**Crash: RangeError: Invalid string length in addSpans during instantiation of recursive template literal types**

*TypeScript crashes with a RangeError due to exponential string growth in deeply recursive template literal type instantiation*

 * created by **na7ure-a**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63273](https://github.com/microsoft/TypeScript/issues/63273) (Open, `Bug`, `Domain: check: Type Circularity`)

**Crash: RangeError: Maximum call stack size exceeded in getNameOfSymbolAsWritten via recursive conditional ReturnType**

*The TypeScript compiler crashes with a maximum call stack size exceeded error when handling a recursive conditional ReturnType in a clone function.*

 * created by **na7ure-a**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63274](https://github.com/microsoft/TypeScript/issues/63274) (Open, `Bug`, `Domain: Error Messages`, `i18n`)

**\[Localization\] Misleading Chinese translation for TS2561 error message**

*The Chinese translation for TS2561 error message incorrectly swaps the property and type relationship, causing confusion and requiring correction.*

 * created by **HHaoWang**
 * (today) **RyanCavanaugh** added labels `Bug`, `i18n`

### [Issue microsoft/TypeScript#63275](https://github.com/microsoft/TypeScript/issues/63275) (Closed, `Question`)

**TypeScript enum emit inconsistency**

*TypeScript 5.x now emits enum members with const string values as string-enum style instead of reverse-mapping, influenced by annotations.*

 * created by **magic-akari**
 * [today](https://github.com/microsoft/TypeScript/issues/63275#issuecomment-4099773091) **RyanCavanaugh** explained enum initializer rules and answered questions about intentionality, documentation, and compatibility
 * **RyanCavanaugh** added label `Question`

### [PR microsoft/TypeScript#63278](https://github.com/microsoft/TypeScript/pull/63278) (Closed)

**Preserve error elaboration for indexed access type assignments**

*Preserve specific error details for indexed access type assignments so users see both the generic message and elaborated diagnostics.*

 * created by **WhiteMinds**
 * [later](https://github.com/microsoft/TypeScript/pull/63278#issuecomment-4102749773) **WhiteMinds** said "@microsoft-github-policy-service agree"

