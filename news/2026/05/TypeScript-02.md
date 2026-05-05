# Report for 2026-05-02 (Saturday, May 2nd, 2026)

4 different users commented on 4 different issues.

## Recommended Actions

 * Response Recommended
    * @carljohnsonnewhampshire-hue asked how to push a new generic type instantiation so TypeScript doesn't think it's the same type in [microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366403308)
    * @carljohnsonnewhampshire-hue asked why slight changes to BuildType broke the recursive type checker in [microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366481833)

## Activity Summary

### [Issue microsoft/TypeScript#46726](https://github.com/microsoft/TypeScript/issues/46726) (Closed, `Needs Investigation`, `Domain: Performance`, `7.0 LS Migration`)

**Slow IntelliSense with react\-hook\-form resolvers on commands \`completionInfo\`, \`completionEntryDetails\`, and, \`encodedSemanticClassifications\-full\`**

*Integrating react-hook-form Zod resolvers causes slow IntelliSense for completionInfo, completionEntryDetails, and encodedSemanticClassifications-full commands.*

 * **andrewbranch** added label `7.0 LS Migration`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/46726#issuecomment-4314328340) **andrewbranch** said "Closing language service bugs related to the 6.0 implementation. For more information, see https://github.com/microsoft/TypeScript/issues/62827"
 * (1 week ago) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/46726#issuecomment-4365508467) **Zain-ul-din** said "Actually, my bad here, Claude Code installed version 3 of the package, where the latest is i think, 5 rn."

### [Issue microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454) (Open, `Design Limitation`)

**\`1 \| 2 \| 3\` can be assigned to \`1 \| 2\` when using a recursive type**

*A recursive mapped type wrapper in TypeScript unsoundly allows assignment between unions 1|2|3 and 1|2.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4354488447) **RyanCavanaugh** explained inability to know ahead of time that BuildType will terminate and requested a reliable heuristic to detect termination without false positives
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4355952195) **carljohnsonnewhampshire-hue** asked for suggestions on intentionally circumventing TypeScript's recursive type heuristics
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4357766912) **carljohnsonnewhampshire-hue** asked if there was a way to write the recursive type definition differently to allow TypeScript to check assignments, perhaps via tail recursion
 * [later](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366258876) **jcalz** demonstrated unrolling recursion to reveal structural type differences and showed assignment compatibility with example code
 * [later](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366403308) **carljohnsonnewhampshire-hue** thanked the respondent, described their workaround, and asked how to push a new generic type instantiation to avoid TypeScript treating repeated types as identical
 * [later](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366481833) **carljohnsonnewhampshire-hue** asked why a recursive mapped type over an infinite circular type worked in one version but broke after slight modifications
 * [later](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4366526176) **jcalz** guessed that TypeScript's variance markers cause the issue, described a workaround using an Invariant wrapper type, and asked for advice

### [Issue microsoft/TypeScript#63456](https://github.com/microsoft/TypeScript/issues/63456) (Open, `Suggestion`, `Awaiting More Feedback`)

**String\.split\(\) method's separator argument should allow undefined**

*Allow undefined as separator in String.split to return the full string array per spec.*

 * created by **JohanRonnblom**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4362960471) **MartinJohns** noted that the issue duplicated #38331, argued that optional parameters and undefined are equivalent, and suggested providing types locally
 * [today](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4364715573) **JohanRonnblom** illustrated that passing undefined as an argument can be useful by showing a highlightText example and explaining general split behavior
 * [later](https://github.com/microsoft/TypeScript/issues/63456#issuecomment-4366516491) **jcalz** suggested using declaration merging to add a call signature for split accepting undefined and argued that changing the built-in signature requires evidence of net benefit in real-world code

