# Report for 2026-05-03 (Sunday, May 3rd, 2026)

3 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @carljohnsonnewhampshire-hue provided two workarounds for the type issue in [microsoft/TypeScript#63457](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4368495242)

## Activity Summary

### [Issue microsoft/TypeScript#46011](https://github.com/microsoft/TypeScript/issues/46011) (Open, `Suggestion`, `Needs Proposal`, `In Discussion`)

**Support for opting out of jsdoc @typedef exports**

*Allow disabling automatic export of root-scope @typedef declarations in JSDoc.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-2137964557) **stoicbuddha** mentioned that editor autocompletion pollution could justify file-specific usage and noted potential annoyance; observed a potential disagreement on definitions of danger but deemed it unimportant to solving the overall issue
 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-3395687680) **mhofman** described encountering the need to define a local module type for implementation details without exporting it
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-4332923366) **natsuki-engr** outlined the issue of unwanted @typedef exports, compared opt-out tag proposals, and asked if there was a path to formalize @local
 * [later](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-4370363309) **natsuki-engr** discussed how types marked with @local should be included in exported signatures following existing TypeScript behavior and shared an implementation confirming it works
 * [later](https://github.com/microsoft/TypeScript/issues/46011#issuecomment-4371089184) **natsuki-engr** proposed introducing a new tag named @jsdoc-strict-export to disable automatic exports for an entire file and minimize impact on existing codebases, noted that no existing TS tag works at file level and suggested this warrants broader discussion

### [PR microsoft/TypeScript#63453](https://github.com/microsoft/TypeScript/pull/63453) (Closed, `For Uncommitted Bug`)

**fix: detected calls to child\_process from a function\.\.\. in\.\.\.**

*Sanitized child_process usage in scripts/find-unused-diganostic-messages.mjs to prevent command injection*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4354624555) **jakebailey** noted that this was not a security problem, suggested the author hadn't tested locally, pointed out formatting issues, and asked if the author was a bot and how they determined the issue needed fixing
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4359360882) **ritschwumm** asked why the change modified every line of the diagnostic script and whether the line endings were switched
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4363011723) **orbisai0security** acknowledged the review, clarified that diagName was repo-controlled and not attacker-controlled, refocused the PR on security hardening and cleaned up line-ending noise
 * [later](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4372510948) **RyanCavanaugh** said "This repo is closed to new PRs except for critical issues, which this isn't."
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454) (Closed, `Design Limitation`)

**\`1 \| 2 \| 3\` can be assigned to \`1 \| 2\` when using a recursive type**

*A recursive mapped type wrapper in TypeScript unsoundly allows assignment between unions 1|2|3 and 1|2.*

 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366403308) **carljohnsonnewhampshire-hue** thanked the respondent, described their workaround, and asked how to push a new generic type instantiation to avoid TypeScript treating repeated types as identical
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366481833) **carljohnsonnewhampshire-hue** asked why a recursive mapped type over an infinite circular type worked in one version but broke after slight modifications
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366526176) **jcalz** guessed that TypeScript's variance markers cause the issue, described a workaround using an Invariant wrapper type, and asked for advice
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366744218) **carljohnsonnewhampshire-hue** thanked @jcalz and shared an improved TypeScript workaround addressing variance
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4367079972) **carljohnsonnewhampshire-hue** provided an improved TypeScript BuildType utility type that avoids creating extra properties in nested object types

### [Issue microsoft/TypeScript#63456](https://github.com/microsoft/TypeScript/issues/63456) (Open, `Suggestion`, `Awaiting More Feedback`)

**String\.split\(\) method's separator argument should allow undefined**

*Allow undefined as separator in String.split to return the full string array per spec.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4362960471) **MartinJohns** noted that the issue duplicated #38331, argued that optional parameters and undefined are equivalent, and suggested providing types locally
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4364715573) **JohanRonnblom** illustrated that passing undefined as an argument can be useful by showing a highlightText example and explaining general split behavior
 * [today](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4366516491) **jcalz** suggested using declaration merging to add a call signature for split accepting undefined and argued that changing the built-in signature requires evidence of net benefit in real-world code
 * [later](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4372476749) **RyanCavanaugh** explained that the split behavior is entirely defined by the spec, highlighted the significant difference between split() and split(c), and requested a code sample with a strong feedback signal to consider changing it
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63457](https://github.com/microsoft/TypeScript/issues/63457) (Closed, `Duplicate`)

**\`Equals\<T, U\>\` used inside of generic type gets simplified to \`false\` immediately if only \`T\` or only \`U\` depends on a type variable**

*Equals<T, U> inside a generic type prematurely resolves to false when only one type parameter varies, even if types match.*

 * created by **carljohnsonnewhampshire-hue**
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4368495242) **carljohnsonnewhampshire-hue** provided two workarounds: one using dependent type arguments and one by adding a T extends U condition to the Equals type
 * [later](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4372497400) **RyanCavanaugh** said "See https://github.com/microsoft/TypeScript/issues/56721; you should not use this definition of Equals unless you fully understand its caveats."
 * **RyanCavanaugh** added label `Duplicate`

