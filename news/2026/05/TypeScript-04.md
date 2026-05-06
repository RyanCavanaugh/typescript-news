# Report for 2026-05-04 (Monday, May 4th, 2026)

7 different users commented on 12 different issues.

## Recommended Actions

 * Moderation
    * @carljohnsonnewhampshire-hue posted rude content in [microsoft/TypeScript#63457](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4372635907)
 * Response Recommended
    * @carljohnsonnewhampshire-hue asked if this issue was a bug in [microsoft/TypeScript#63457](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4372578016)
    * @carljohnsonnewhampshire-hue asked if the conditional type falls under Hyrum's Law and is valid to rely on in [microsoft/TypeScript#63457](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4373016442)
    * @carljohnsonnewhampshire-hue provided a workaround using a TypeScript type definition in [microsoft/TypeScript#63459](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4378484995)

## Activity Summary

### [Issue microsoft/TypeScript#21934](https://github.com/microsoft/TypeScript/issues/21934) (Closed, `Suggestion`, `Declined`, `Domain: JavaScript`)

**Understand 'int', 'integer', 'float', 'double', etc\. as 'number' in JSDoc**

*Treat numeric-sounding JSDoc type names such as int, integer, float, and double as equivalent to number by default.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/21934#issuecomment-1287570011) **Rudxain** proposed allowing type aliases to be defined as subsets or supersets of existing types and noted that JS lacks official integer types
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/21934#issuecomment-1306341594) **pilattebe** explained that JS arrays accept any key type including floats and strings and noted that TypeScript only enforces numeric keys without distinguishing integers from floats
 * [3.4 years ago](https://github.com/microsoft/TypeScript/issues/21934#issuecomment-1306444781) **Rudxain** noted that assigning a negative value to an array's length property throws a runtime error and wished for runtime index validation; referenced Python's literal types; agreed that arbitrary expressions with multiple operators, especially bigints and exponentials, can be problematic
 * (today) **DanielRosenwasser** added label `Declined`, and removed label `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/21934#issuecomment-4375567802) **DanielRosenwasser** pointed out that the rewrite complicated rationalizing loose JS behavior given modern TypeScript-focused JSDoc annotations
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#25624](https://github.com/microsoft/TypeScript/issues/25624) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: JSDoc`, `checkJs`, `Domain: JavaScript`)

**In JS, \`object\` is treated as 'any'**

*TypeScript treats a JSDoc-defined object type as any, allowing assignment of non-objects without error*

 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/25624#issuecomment-589748157) **ExE-Boss** said "I’d like if there was a way to use the object type in JSDoc without needing to enable noImplicitAny."
 * [6.2 years ago](https://github.com/microsoft/TypeScript/issues/25624#issuecomment-589748709) **sandersn** suggested defining `NonPrimitive = object` in a .d.ts file and noted that many JS codebases misuse `object` as `any` or `unknown`
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/25624#issuecomment-780172583) **ExE-Boss** shared a personal inline typedef implementation for Object.create and its equivalent using NonNullable and Parameters
 * [today](https://github.com/microsoft/TypeScript/issues/25624#issuecomment-4375722669) **DanielRosenwasser** said "Keywords: object non-primitive non primitve nonprimitive jsdoc"
 * [today](https://github.com/microsoft/TypeScript/issues/25624#issuecomment-4375723057) **DanielRosenwasser** said "Looks like TypeScript 7 might end up actually doing this."
 * **DanielRosenwasser** removed label `Domain: lib.d.ts`

### [Issue microsoft/TypeScript#63448](https://github.com/microsoft/TypeScript/issues/63448) (Open, `Suggestion`, `Awaiting More Feedback`)

**\`libReplacement: true\` lookup folder should be configurable \(via \`typeRoots\` ?\)**

*Enable configuring the module resolution path for @typescript/lib-dom when using libReplacement via typeRoots*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63448#issuecomment-4345330527) **RyanCavanaugh** explained that typeRoots resolves type directives rather than modules and recommended using files or include with noLib for alternate lib files
 * (5 days ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63448#issuecomment-4373762285) **freshp86** thanked the proposal and said they would try it and provide updates, explained that during the TypeScript v7 migration they needed both v6 and v7 compilers side by side and wanted to use libReplacement for consistent local patches

### [Issue microsoft/TypeScript#63451](https://github.com/microsoft/TypeScript/issues/63451) (Open, `Bug`, `Fix Available`, `Domain: classes`)

**\`new super\(\)\` in static method does not cause error**

*TypeScript 6.0 incorrectly allows new super() in static blocks and methods without error.*

 * **RyanCavanaugh** added to milestone `Dormant`
 * **typescript-bot** added label `Fix Available`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63451#issuecomment-4361516140) **mkantor** asked why the bot added the "Fix Available" label and noted it happened on issue #63391 as well
 * [today](https://github.com/microsoft/TypeScript/issues/63451#issuecomment-4372524268) **RyanCavanaugh** said "Bot's broken and no one has had the time to figure out why 😅. We don't really use the label for anything at the moment"

### [Issue microsoft/TypeScript#63457](https://github.com/microsoft/TypeScript/issues/63457) (Open, `Duplicate`)

**\`Equals\<T, U\>\` used inside of generic type gets simplified to \`false\` immediately if only \`T\` or only \`U\` depends on a type variable**

*Equals<T, U> inside a generic type prematurely resolves to false when only one type parameter varies, even if types match.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4368495242) **carljohnsonnewhampshire-hue** provided two workarounds: one using dependent type arguments and one by adding a T extends U condition to the Equals type
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4372497400) **RyanCavanaugh** said "See https://github.com/microsoft/TypeScript/issues/56721; you should not use this definition of Equals unless you fully understand its caveats."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4372578016) **carljohnsonnewhampshire-hue** stated understanding of caveats, asserted it was a bug, and asked for agreement while defending the use of extends checks for type equality in tests
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4372635907) **carljohnsonnewhampshire-hue** complained that maintainers had not read their issue and incorrectly marked it as a duplicate and insisted the reported behavior was distinct and widely relied upon
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4372745822) **RyanCavanaugh** explained that Equals can return false in some cases, referenced the FAQ, and asked what makes the commenter think this isn't a manifestation of its caveats
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4373016442) **carljohnsonnewhampshire-hue** thanked the maintainer for the FAQ link, suggested adding a TOC for the long page, acknowledged the documented implementation detail, and asked if the conditional type falls under Hyrum's Law and is valid to rely on
 * [today](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4374434222) **mkantor** asked what the use case for the type was and suggested that mutual assignability might be the intended concept instead of type equality
 * [later](https://github.com/microsoft/TypeScript/issues/63457#issuecomment-4378267616) **carljohnsonnewhampshire-hue** explained that he wanted strong type assertions in unit tests to ensure types are identical without unsoundness and decided to stick to the augmented Equals definition

### [PR microsoft/TypeScript#63458](https://github.com/microsoft/TypeScript/pull/63458) (Open, `For Backlog Bug`)

**feat: Add Math\.sumPrecise type definition \(ES2025\)**

*Add type definitions for the ES2025 Math.sumPrecise method to enable more accurate summation.*

 * created by **jlaportebot**
 * (today) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63458#issuecomment-4375780938) **jlaportebot** said "@microsoft-github-policy-service agree individual"
 * [today](https://github.com/microsoft/TypeScript/pull/63458#issuecomment-4375789666) **jlaportebot** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63458#issuecomment-4376396766) **MartinJohns** said "There already is #63429. This seems to be yet another AI spambot."

### [Issue microsoft/TypeScript#63459](https://github.com/microsoft/TypeScript/issues/63459) (Closed, `Not a Defect`)

**branded type erroneously replaced with \`never\` in a conditional type**

*Conditional type returns never when checking branded number types instead of preserving the branded type.*

 * created by **carljohnsonnewhampshire-hue**
 * [later](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4378484995) **carljohnsonnewhampshire-hue** provided a workaround using a TypeScript type definition
 * [later](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4379753807) **mkantor** discussed conditional type behavior and asked if number & object should not be never
 * [later](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4380195264) **mkantor** observed that a more natural-looking rewrite of the bug type using a single conditional resulted in repro becoming false and was not equivalent to the nested conditional version
 * [later](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4380298085) **carljohnsonnewhampshire-hue** expected `number & object` to be `never` like `string & number`, explaining that `object` is a fundamental type used to distinguish primitives from objects
 * [later](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4380337552) **carljohnsonnewhampshire-hue** recommended adjusting the type narrowing logic to handle branded types, noting their widespread usage and expected behavior with extends checks

