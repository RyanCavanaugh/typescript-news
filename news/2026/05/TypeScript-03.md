# Report for 2026-05-03 (Sunday, May 3rd, 2026)

2 different users commented on 5 different issues.

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

### [Issue microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454) (Open, `Design Limitation`)

**\`1 \| 2 \| 3\` can be assigned to \`1 \| 2\` when using a recursive type**

*A recursive mapped type wrapper in TypeScript unsoundly allows assignment between unions 1|2|3 and 1|2.*

 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366403308) **carljohnsonnewhampshire-hue** thanked the respondent, described their workaround, and asked how to push a new generic type instantiation to avoid TypeScript treating repeated types as identical
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366481833) **carljohnsonnewhampshire-hue** asked why a recursive mapped type over an infinite circular type worked in one version but broke after slight modifications
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366526176) **jcalz** guessed that TypeScript's variance markers cause the issue, described a workaround using an Invariant wrapper type, and asked for advice
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366744218) **carljohnsonnewhampshire-hue** thanked @jcalz and shared an improved TypeScript workaround addressing variance
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4367079972) **carljohnsonnewhampshire-hue** provided an improved TypeScript BuildType utility type that avoids creating extra properties in nested object types

### [Issue microsoft/TypeScript#63457](https://github.com/microsoft/TypeScript/issues/63457) (Open)

**\`Equals\<T, U\>\` used inside of generic type gets simplified to \`false\` immediately if only \`T\` or only \`U\` depends on a type variable**

*Equals<T, U> inside a generic type prematurely resolves to false when only one type parameter varies, even if types match.*

 * created by **carljohnsonnewhampshire-hue**
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4368495242) **carljohnsonnewhampshire-hue** provided two workarounds: one using dependent type arguments and one by adding a T extends U condition to the Equals type

