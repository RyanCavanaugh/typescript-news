# Report for 2025-11-27 (Thursday, November 27th, 2025)

8 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @RobertSandiford asked why the feature was on hold and whether technical constraints or maintainer opposition caused it, and if v7 or the Go implementation addresses it in [microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3587413546)
    * @RobertSandiford asked why the feature was on hold and whether technical constraints or maintainer opposition caused it, and if v7 or the Go implementation addresses it in [microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3587413546)
    * @PierceLanternStudios asked whether the comment sufficiently referenced the PR or if a separate issue was needed in [microsoft/TypeScript#55593](https://github.com/microsoft/TypeScript/issues/55593#issuecomment-3587622070)
    * @Fuzzyma provided explanation and example use-case for Vue reactive computed refs type mismatch in [microsoft/TypeScript#56158](https://github.com/microsoft/TypeScript/issues/56158#issuecomment-3588334251)
    * @rattrayalex asked for thoughts on supporting namespace/interface shadowing pattern in [microsoft/TypeScript#62813](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3587768314)
    * @dipeshkaphle asked if typecheck failure when swapping variable order is reasonable in [microsoft/TypeScript#62814](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3588182924)
    * @dipeshkaphle provided repro steps as requested in [microsoft/TypeScript#62814](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3588190199)
    * @dipeshkaphle asked if the behavior was documented in the strict mode documentation in [microsoft/TypeScript#62814](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3589201164)

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [29 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-2864039225) **niti2539** provided a workaround solution with screenshots illustrating various type matching scenarios
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3419149140) **shoxter** asked why the holdout existed and whether technical reasons or maintainers' opposition and if the v7 release and Go implementation address it
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3419149140) **shoxter** asked why the holdout existed and whether technical reasons or maintainers' opposition and if the v7 release and Go implementation address it
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3587413546) **RobertSandiford** asked why the feature was on hold, inquired if technical constraints or maintainer opposition caused it, and asked if v7 or the Go implementation fixes it, and raised concerns about interoperability between exact and loose object types
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3587413546) **RobertSandiford** asked why the feature was on hold, inquired if technical constraints or maintainer opposition caused it, and asked if v7 or the Go implementation fixes it, and raised concerns about interoperability between exact and loose object types

### [Issue microsoft/TypeScript#55593](https://github.com/microsoft/TypeScript/issues/55593) (Open, `Suggestion`, `Awaiting More Feedback`)

**Go\-to\-definition on interfaces shadowed by namespaces opens a selection dialog instead of going to the interface, when used as one\.**

*Go-to-definition on interfaces shadowed by namespaces in VS Code opens a selection dialog instead of navigating to the interface definition.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/55593#issuecomment-1703548497) **andrewbranch** said "I think that might be fine. In my experience, it’s hard to predict how much this kind of change will impact people. Hence “awaiting more feedback.” If the feedback is positive I think we could try it."
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/55593#issuecomment-1787569258) **rattrayalex** said "Hey, this keeps coming up, and I'd be interested in funding someone to put up a PR with this behavior to try out and see if you like it. Would that be welcome?"
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/55593#issuecomment-1787659018) **andrewbranch** encouraged putting up an experimental PR but warned it might not be merged and offered to create an experimental playground/npm build
 * [today](https://github.com/microsoft/TypeScript/issues/55593#issuecomment-3587622070) **PierceLanternStudios** mentioned an experimental PR for the issue and asked whether this comment sufficiently referenced it or if a separate issue was needed

### [Issue microsoft/TypeScript#56158](https://github.com/microsoft/TypeScript/issues/56158) (Closed, `Design Notes`)

**Design Meeting Notes, 10/18/2023**

*Exploring proposals to support distinct read and write types for TypeScript index signatures and mapped types, including grouped accessor syntax.*

 * [2 years ago](https://github.com/microsoft/TypeScript/issues/56158#issuecomment-1773263213) **DanielRosenwasser** said "(I've amended my comment to have an example of the type itself)"
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/56158#issuecomment-1773279912) **pikax** described the current behavior of Reactive and Ref types with TypeScript code examples and suggested making the set method generic
 * (2 years ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/56158#issuecomment-3588334251) **Fuzzyma** described how Vue's reactive function unwraps computed refs and breaks the read type by using the setter type for both read and write

### [Issue microsoft/TypeScript#62803](https://github.com/microsoft/TypeScript/issues/62803) (Closed, `Question`)

**ScrollIntoViewOptions missing \`container\` option**

*TypeScript's ScrollIntoViewOptions type definition lacks the 'container' property, causing validation errors.*

 * created by **jillyj**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62803#issuecomment-3573964571) **Renegade334** referred to documentation and noted that the option hadn't met browser support threshold for inclusion in lib.dom
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/62803#issuecomment-3587653296) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62811](https://github.com/microsoft/TypeScript/pull/62811) (Closed, `For Uncommitted Bug`)

**Improve satisfies semantics: return never when target type is never**

*Make TypeScript’s satisfies operator narrow expressions to never when the specified target type is exactly never.*

 * created by **ViKing-Coder-jpg**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62811#issuecomment-3585583356) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62811#issuecomment-3586965882) **MartinJohns** said "Won't this change allow foo satisfies never when foo does not satisfy never?"

### [Issue microsoft/TypeScript#62812](https://github.com/microsoft/TypeScript/issues/62812) (Open, `Bug`, `Help Wanted`, `Domain: Conditional Types`)

**Spread operator fails to distribute over union when recursive type call is inlined instead of aliased**

*TypeScript’s spread operator fails to distribute over union types when using an inlined recursive type instead of an alias.*

 * created by **MMF2**

### [PR microsoft/TypeScript#62813](https://github.com/microsoft/TypeScript/pull/62813) (Open, `For Uncommitted Bug`)

**Add go\-to\-definition inference for shadowed namespaces**

*Enhance go-to-definition behavior in shadowed namespaces by inferring the correct symbol through kind comparison with a timeout-based fallback.*

 * created by **PierceLanternStudios**
 * [today](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3587614875) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3587615019) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3587618790) **PierceLanternStudios** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3587768314) **rattrayalex** asked for thoughts on supporting namespace/interface shadowing patterns used by Stripe, OpenAI, and Anthropic SDKs

### [Issue microsoft/TypeScript#62814](https://github.com/microsoft/TypeScript/issues/62814) (Closed, `Working as Intended`)

**Inference mismatch in strict and non\-strict mode**

*TypeScript strict mode erroneously changes boolean literal inference, causing compilation errors absent in non-strict mode.*

 * created by **dipeshkaphle**
 * [today](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3588135860) **MartinJohns** explained that disabling strictNullChecks permitted null or undefined values, which altered the logical-or check and changed the inferred type
 * [today](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3588182924) **dipeshkaphle** asked whether swapping variable order in an OR expression causing a typecheck failure was reasonable given the LSP's reported type
 * [today](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3588190199) **dipeshkaphle** provided the original program and demonstrated that swapping the variable order still caused compilation to fail under the same flags
 * [today](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3588233534) **MartinJohns** clarified that with strictNullChecks disabled the type true can be three different values and affirmed the suggestion's reasonableness
 * [later](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3588396026) **MartinJohns** explained how enabling or disabling strictNullChecks changes type inference for the logical-or expression, causing different types for ‘miniature’ and affecting assignment compatibility
 * [later](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3589201164) **dipeshkaphle** asked if the behavior was documented in the strict mode docs
 * [later](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3589290382) **MartinJohns** referenced the TypeScript handbook sections on strict null checks and truthiness narrowing

