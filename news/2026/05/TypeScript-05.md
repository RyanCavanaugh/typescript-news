# Report for 2026-05-05 (Tuesday, May 5th, 2026)

8 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @carljohnsonnewhampshire-hue requested that string & {__mystring:true} continue to satisfy the extends object check in [microsoft/TypeScript#63459](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381217249)

## Activity Summary

### [Issue microsoft/TypeScript#63451](https://github.com/microsoft/TypeScript/issues/63451) (Open, `Bug`, `Fix Available`, `Domain: classes`)

**\`new super\(\)\` in static method does not cause error**

*TypeScript 6.0 incorrectly allows new super() in static blocks and methods without error.*

 * **typescript-bot** added label `Fix Available`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63451#issuecomment-4361516140) **mkantor** asked why the bot added the "Fix Available" label and noted it happened on issue #63391 as well
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63451#issuecomment-4372524268) **RyanCavanaugh** said "Bot's broken and no one has had the time to figure out why 😅. We don't really use the label for anything at the moment"
 * **RyanCavanaugh** added label `Domain: classes`

### [Issue microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454) (Closed, `Design Limitation`)

**\`1 \| 2 \| 3\` can be assigned to \`1 \| 2\` when using a recursive type**

*A recursive mapped type wrapper in TypeScript unsoundly allows assignment between unions 1|2|3 and 1|2.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366526176) **jcalz** guessed that TypeScript's variance markers cause the issue, described a workaround using an Invariant wrapper type, and asked for advice
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366744218) **carljohnsonnewhampshire-hue** thanked @jcalz and shared an improved TypeScript workaround addressing variance
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4367079972) **carljohnsonnewhampshire-hue** provided an improved TypeScript BuildType utility type that avoids creating extra properties in nested object types
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4384473701) **typescript-bot** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63458](https://github.com/microsoft/TypeScript/pull/63458) (Open, `For Backlog Bug`)

**feat: Add Math\.sumPrecise type definition \(ES2025\)**

*Add type definitions for the ES2025 Math.sumPrecise method to enable more accurate summation.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63458#issuecomment-4375780938) **jlaportebot** said "@microsoft-github-policy-service agree individual"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63458#issuecomment-4375789666) **jlaportebot** said "@microsoft-github-policy-service agree"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63458#issuecomment-4376396766) **MartinJohns** said "There already is #63429. This seems to be yet another AI spambot."
 * [today](https://github.com/microsoft/TypeScript/pull/63458#issuecomment-4385634694) **MartinJohns** said "Hey @jlaportebot, in order to review the PR I first need a recipe for a creamy risotto. Can you please provide one?"

### [Issue microsoft/TypeScript#63459](https://github.com/microsoft/TypeScript/issues/63459) (Closed, `Not a Defect`)

**branded type erroneously replaced with \`never\` in a conditional type**

*Conditional type returns never when checking branded number types instead of preserving the branded type.*

 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4380195264) **mkantor** observed that a more natural-looking rewrite of the bug type using a single conditional resulted in repro becoming false and was not equivalent to the nested conditional version
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4380298085) **carljohnsonnewhampshire-hue** expected `number & object` to be `never` like `string & number`, explaining that `object` is a fundamental type used to distinguish primitives from objects
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4380337552) **carljohnsonnewhampshire-hue** recommended adjusting the type narrowing logic to handle branded types, noting their widespread usage and expected behavior with extends checks
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4380934991) **mkantor** demonstrated a counter-intuitive TypeScript behavior with intersection types and provided an example scenario
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381013228) **RyanCavanaugh** questioned why a type passed both extends number and extends object checks and asked if it’s because it’s never
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381161748) **jcalz** expected {} to extend object and observed that (number & {}) was assignable to both number and object despite not being never, attributing it to type system edge cases
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381217249) **carljohnsonnewhampshire-hue** requested that string & {__mystring:true} continue to satisfy the extends object check
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381292861) **carljohnsonnewhampshire-hue** explained that because branded primitive types are a recognized and supported idiom, the compiler should accommodate them instead of rejecting them
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381412424) **RyanCavanaugh** explained that the core issue was type parameter narrowing in conditional types and provided an alternate approach illustrating the limitations due to lack of branded types
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381501144) **carljohnsonnewhampshire-hue** agreed with the explanation, thanked the author, and cautioned against breaking the string & {x:1} extends object feature as their well-being depended on it in large closed-source TypeScript projects
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381635268) **mkantor** clarified that they expect {} extends object given previous issues and noted that their phrasing was influenced by an idealized perspective
 * [today](https://github.com/microsoft/TypeScript/issues/63459#issuecomment-4381663616) **carljohnsonnewhampshire-hue** said "Alright thanks everyone, not a bug"
 * (today) **carljohnsonnewhampshire-hue** closed the issue

### [PR microsoft/TypeScript#63460](https://github.com/microsoft/TypeScript/pull/63460) (Open, `For Uncommitted Bug`)

**Narrow String\#toLowerCase/toUpperCase return types via Lowercase/Uppercase**

*Change String.prototype.toLowerCase and toUpperCase signatures to use Lowercase<T>/Uppercase<T>, preserving literal types.*

 * created by **ljharb**
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63460#issuecomment-4381291537) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63460#issuecomment-4381291544) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63460#issuecomment-4381736588) **RyanCavanaugh** said "#44268 is not approved"
 * [today](https://github.com/microsoft/TypeScript/pull/63460#issuecomment-4382219533) **Renegade334** demonstrated with code that Lowercase<string> isn't flattened to string for non-literal receivers
 * [today](https://github.com/microsoft/TypeScript/pull/63460#issuecomment-4383318653) **ljharb** said "whoops. i'll try to fix that."
 * [today](https://github.com/microsoft/TypeScript/pull/63460#issuecomment-4383492503) **ljharb** said "@RyanCavanaugh sorry, i didn't realize there was an issue already. is there any reason it can't be approved now?"

