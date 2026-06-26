# Report for 2026-06-24 (Wednesday, June 24th, 2026)

6 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @badeball asked if information was lost during union simplification in [microsoft/TypeScript#63578](https://github.com/microsoft/TypeScript/issues/63578#issuecomment-4797686402)

## Activity Summary

### [Issue microsoft/TypeScript#62995](https://github.com/microsoft/TypeScript/issues/62995) (Closed, `Fixed`)

**Bug with type argument inference if it has default value \`= undefined\` and actual value is object with non\-arrow function**

*TypeScript incorrectly infers generic type arguments defaulting to undefined when given an inline object with non-arrow functions.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3761049019) **RyanCavanaugh** said "Confirmed in nightly playground"
 * (22 weeks ago) **RyanCavanaugh** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-4768241891) **hesprs** asked whether they needed to open a new issue or report to the linked TypeScript issue after still encountering errors
 * [today](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-4794212400) **RyanCavanaugh** said "@hesprs please log a new issue, thanks"

### [Issue microsoft/TypeScript#63481](https://github.com/microsoft/TypeScript/issues/63481) (Closed, `Help Wanted`, `Domain: lib.d.ts`, `Possible Improvement`)

**\`ReadonlySet\` lacks documentation for \`has\`, \`forEach\` and \`size\`**

*ReadonlySet<T> in lib.es2015.collection.d.ts lacks documentation for its has, forEach, and size members.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63481#issuecomment-4594935599) **RyanCavanaugh** said "Can people PLEASE stop sending PRs when there's already an open identical PR open for the issue? What is going on??"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63481#issuecomment-4595081680) **vitalysinitsin** noted that there were enough people looking into the issue and that they would bow out
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63481#issuecomment-4595148889) **RyanCavanaugh** appreciated the check before PRing and noted that Claude’s issue search list top issue often attracts multiple PRs regardless of the docs
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63483](https://github.com/microsoft/TypeScript/pull/63483) (Closed, `For Backlog Bug`)

**docs: add JSDoc comments to ReadonlySet interface**

*Add JSDoc comments to the ReadonlySet interface to improve its documentation.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/63483#issuecomment-4485867222) **niledas** said "Hi @RyanCavanaugh, please help review this small PR. Let me know if you have any suggestions."
 * (yesterday) **RyanCavanaugh** closed the issue
 * (yesterday) **RyanCavanaugh** reopened the issue
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63546](https://github.com/microsoft/TypeScript/issues/63546) (Open, `Bug`, `Domain: Declaration Emit`)

**Duplicate function declarations in generated \`\.d\.ts\` for non\-module JS files with \`allowJs\` \+ \`declaration\`**

*Non-module JavaScript files compiled with allowJs and declaration produce duplicate global function declarations across their emitted .d.ts files.*

 * **RyanCavanaugh** added label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/63546#issuecomment-4791015251) **RyanCavanaugh** said "Tagging bug for the exit code thing"
 * **RyanCavanaugh** added to milestone `Backlog`
 * **RyanCavanaugh** added label `Domain: Declaration Emit`

### [Issue microsoft/TypeScript#63551](https://github.com/microsoft/TypeScript/issues/63551) (Open, `Suggestion`, `Awaiting More Feedback`)

**Destructured function does not show outline of inner function parameters**

*Destructuring a function’s return value causes TypeScript’s outline model to hide nested parameters a, b, and c, unlike normal assignments.*

 * created by **aiday-mar**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63551#issuecomment-4693464522) **RyanCavanaugh** said "@Aditya07771 read CONTRIBUTING.md!"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63551#issuecomment-4699823578) **tahanawab4848** described an inconsistency in the outline model when destructuring return values and asked if it was expected
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63558](https://github.com/microsoft/TypeScript/issues/63558) (Open, `Unactionable`)

**Partial generic types get resolved completely incorrectly**

*Type guards on a union of a generic and a concrete type produce inconsistent and incorrect type inferences in TypeScript.*

 * created by **Mudloop**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63558#issuecomment-4713263946) **Mudloop** said "If partially generic types are too complex to resolve, I think an error would be preferable over a state where the value and its type no longer line up."
 * **RyanCavanaugh** added label `Unactionable`
 * [today](https://github.com/microsoft/TypeScript/issues/63558#issuecomment-4791327581) **RyanCavanaugh** expressed confusion about the proposal, stated that a "partial generic type" isn't a thing, and asserted that the Guard2 function could not be implemented correctly
 * [today](https://github.com/microsoft/TypeScript/issues/63558#issuecomment-4796322059) **Mudloop** clarified that he used 'partial generic type' loosely and showed through TypeScript examples that Guard2 can be implemented correctly in certain cases

### [Issue microsoft/TypeScript#63561](https://github.com/microsoft/TypeScript/issues/63561) (Closed, `Not a Defect`)

**Generator functions may not return \`IteratorObject\`**

*Generator functions declared to return IteratorObject<T> without explicit return statements incorrectly trigger a missing return value error.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4723589163) **Renegade334** observed that TypeScript already provides a dedicated return type for generator functions usable in return annotations
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4729759859) **nmain** questioned whether the facilitation was deliberate and asked why defaults are any on Generator<> and Iterable<> but unknown on IteratorObject<>
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4732242373) **laverdet** described using generator functions for simple iterables, downcasting to Iterator<T> due to Generator<T,R,N>’s complexity, noted lost functionality with built-in iterators, suggested creating a custom interface extending Generator, and proposed considering void as a default for TReturn on IteratorObject while acknowledging it may be too late
 * [today](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4791293884) **RyanCavanaugh** described that changing the type parameter default would break all existing IteratorObject<X> usages and that the upside was unclear
 * **RyanCavanaugh** added label `Not a Defect`
 * (today) **laverdet** closed the issue

### [Issue microsoft/TypeScript#63578](https://github.com/microsoft/TypeScript/issues/63578) (Open, `Not a Defect`)

**Unexpectedly narrow implicit generator type**

*TypeScript’s implicit type inference for generator functions produces an unexpectedly narrow union type across multiple versions.*

 * created by **badeball**
 * [today](https://github.com/microsoft/TypeScript/issues/63578#issuecomment-4791228589) **RyanCavanaugh** provided a minimal TypeScript example demonstrating that FeatureChild is assignable to RuleChild, causing FeatureChild | RuleChild to simplify to RuleChild and affecting the inferred yield type
 * **RyanCavanaugh** added label `Not a Defect`
 * [later](https://github.com/microsoft/TypeScript/issues/63578#issuecomment-4797686402) **badeball** pointed out a discrepancy in TypeScript's type inference where foo.location was inferred properly but foo.rule was typed as unknown and asked if this was due to union simplification
 * [later](https://github.com/microsoft/TypeScript/issues/63578#issuecomment-4800938464) **RyanCavanaugh** said "I agree in principle, but subtype reduction is critical for a lot of stuff to work and is always legal to occur. That sort of check isn't sound in the first place, since object types aren't sealed."

### [Issue microsoft/TypeScript#63579](https://github.com/microsoft/TypeScript/issues/63579) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-\-build false negative through export star facade project**

*Incremental tsc --build with composite projects using export * facades fails to detect downstream type changes, resulting in stale declarations.*

 * created by **jasonkuhrt**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript#63580](https://github.com/microsoft/TypeScript/issues/63580) (Closed, `Bug`, `Domain: Parser`)

**Parser hangs on comment ending with \`\-\*/\`**

*TypeScript's createSourceFile function hangs indefinitely when parsing a comment that begins with /** and ends with -*/.*

 * created by **core-dumpling**
 * [today](https://github.com/microsoft/TypeScript/issues/63580#issuecomment-4790844410) **RyanCavanaugh** said "Doesn't repro in tsgo but a total LS hang is quite bad; we might want to take this for a 6.0 patch"
 * **RyanCavanaugh** added label `Bug`
 * **RyanCavanaugh** added label `Domain: Parser`

### [PR microsoft/TypeScript#63581](https://github.com/microsoft/TypeScript/pull/63581) (Closed, `For Uncommitted Bug`)

**Fix infinite loop**

*Correct loop termination logic to fix an infinite loop in the application.*

 * created by **core-dumpling**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63581#issuecomment-4800446635) **core-dumpling** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63582](https://github.com/microsoft/TypeScript/issues/63582) (Open, `Suggestion`, `Out of Scope`)

**how can I make typescript recognize css or svg files that exist while still warning about files that don't exist \(without allegedly creating \.d\.css\.ts or whatever AI is trying to claim\)?**

*How can TypeScript be configured to recognize existing CSS or SVG imports and still warn about missing files without needing artificial declaration files?*

 * created by **Arlen22**
 * [later](https://github.com/microsoft/TypeScript/issues/63582#issuecomment-4800900797) **RyanCavanaugh** explained that build tools, not Node, resolve .svg imports and that TypeScript should rely on the build tool as the single source of truth for valid module paths
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Out of Scope`

### [Issue microsoft/TypeScript#63583](https://github.com/microsoft/TypeScript/issues/63583) (Open, `Bug`)

**Finally is not implemented correctly in all cases**

*TypeScript incorrectly flags missing return statements or unreachable code when a finally block both reads and writes a variable.*

 * created by **Mudloop**
 * (later) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63584](https://github.com/microsoft/TypeScript/issues/63584) (Open, `Bug`)

**tagged/named rest parameter participating in circular reference causes error**

*TypeScript incorrectly reports circular reference errors when a recursive tuple union uses a named rest parameter*

 * created by **dragoncoder047**
 * (later) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

