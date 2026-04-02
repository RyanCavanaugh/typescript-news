# Report for 2026-01-02 (Friday, January 2nd, 2026)

6 different users commented on 5 different issues.

## Recommended Actions

 * Moderation
    * @mekrix777mekort-ops posted spam content in [microsoft/TypeScript#62939](https://github.com/microsoft/TypeScript/issues/62939#issuecomment-3706630767)

## Activity Summary

### [Issue microsoft/TypeScript#51612](https://github.com/microsoft/TypeScript/issues/51612) (Open, `Suggestion`, `Experimentation Needed`)

**Improve reverse mapped types inference by creating candidates from concrete index types**

*Improve TypeScript's reverse mapped types inference by using concrete index types to avoid circularity when inferring constrained properties.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3614423612) **RyanCavanaugh** shared a Copilot-generated summary of reverse mapped types in TypeScript, including definitions, examples, and a historical timeline of related issues and PRs
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3614455161) **RyanCavanaugh** provided a comprehensive list of demonstrative before/after samples for reverse mapped type PRs, illustrating fixes in PR #28494 and PR #31221
 * [today](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3705708494) **devanshj** suggested using quantified types instead of reverse mapped types and demonstrated this with code examples, noting that multiple inference passes (#51511) would be required
 * [today](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3705783160) **Andarist** suggested leveraging intra expression sites inference and expanding the algorithm to push/pop multiple inference contexts, referencing relevant TypeScript PRs
 * [today](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3705849111) **devanshj** expressed difficulty understanding intra expression sites and argued that multiple inferences in code were easier for complex dependency chains
 * [today](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3705864509) **Andarist** provided TS playground examples and noted that the only rule was to put the producer before consumer, similar to positional arguments
 * [today](https://github.com/microsoft/TypeScript/issues/51612#issuecomment-3705891345) **devanshj** said "Oh that's really cool didn't know that!"

### [Issue microsoft/TypeScript#62939](https://github.com/microsoft/TypeScript/issues/62939) (Closed)

**Docs: Explain advanced Git commands and their usage with examples**

*Enhance the documentation by providing clear explanations and usage examples for advanced Git commands.*

 * created by **mekrix777mekort-ops**
 * (2 days ago) **mekrix777mekort-ops** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62939#issuecomment-3702930372) **mekrix777mekort-ops** said "Obieg Sprawdza Czy Pisanie Bez Opieki Insnstuacj Może Znikać ."
 * [today](https://github.com/microsoft/TypeScript/issues/62939#issuecomment-3706630767) **mekrix777mekort-ops** attempted to mark the issue as a duplicate without providing a valid reference
 * (today) **mekrix777mekort-ops** closed the issue

### [Issue microsoft/TypeScript#62944](https://github.com/microsoft/TypeScript/issues/62944) (Open, `Suggestion`, `Declined`)

**Allow inferred object literal optional properties**

*Introduce syntax for inferring optional object literal properties (e.g. prop2?) to allow marking certain properties optional during type inference.*

 * created by **rtcpw**
 * [today](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706086092) **MartinJohns** said "I'm not sure I see the purpose behind this. The proposed object literals will always have prop2 set, so marking it as optional doesn't make much sense."
 * [today](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706115817) **jcalz** suggested writing a helper function 'partial' to widen types from T to Partial<T> and provided example code and a playground link
 * [today](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706222022) **rtcpw** explained that literal object templates in libraries like zod require optional properties to cascade type information and optionality through factory definitions
 * [today](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706224710) **rtcpw** thanked the contributor for suggesting a helper function and said it was a nice workaround
 * [today](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706285199) **MartinJohns** explained that existing helper types could support optional properties and cautioned that the proposed syntax might mislead users

### [Issue microsoft/TypeScript#62946](https://github.com/microsoft/TypeScript/issues/62946) (Closed)

**I acknowledge that issues using this template may be closed without further explanation at the maintainer's discretion\.**

*Acknowledgement that issues using this template can be closed at the maintainer’s discretion without explanation.*

 * created by **mekrix777mekort-ops**
 * [today](https://github.com/microsoft/TypeScript/issues/62946#issuecomment-3706781505) **jcalz** said "Sir, this is a Wendy's."
 * [later](https://github.com/microsoft/TypeScript/issues/62946#issuecomment-3706899605) **MartinJohns** said "No, this is Patrick!"

