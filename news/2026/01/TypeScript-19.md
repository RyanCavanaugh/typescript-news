# Report for 2026-01-19 (Monday, January 19th, 2026)

12 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @Tasin5541 asked for an update in [microsoft/TypeScript#29036](https://github.com/microsoft/TypeScript/issues/29036#issuecomment-3771112566)
    * @nekolab requested a PR review from @RyanCavanaugh in [microsoft/TypeScript#59745](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3771797151)
    * @KoxyG asked if the issue was a verified bug and offered to fix it in [microsoft/TypeScript#62965](https://github.com/microsoft/TypeScript/issues/62965#issuecomment-3770585196)
    * @Milad93R provided updated information about Scheduler API types availability and a workaround in [microsoft/TypeScript#63016](https://github.com/microsoft/TypeScript/issues/63016#issuecomment-3771906119)

## Activity Summary

### [Issue microsoft/TypeScript#29036](https://github.com/microsoft/TypeScript/issues/29036) (Open, `Suggestion`, `In Discussion`, `Domain: API`, `Domain: LS: TSServer`)

**TSServer navtree — Way to differentiate function declarations from function expressions**

*Request to enhance TypeScript Server's navtree response to distinguish function declarations from expressions for code lens placement*

 * (7.1 years ago) **weswigham** added labels `In Discussion`, `API`, `Domain: TSServer`
 * [today](https://github.com/microsoft/TypeScript/issues/29036#issuecomment-3771112566) **Tasin5541** said "Any update on this?"

### [PR microsoft/TypeScript#59745](https://github.com/microsoft/TypeScript/pull/59745) (Open, `For Backlog Bug`)

**Narrow destructured variables based on initializer's analysis result**

*Enhance destructured object variable type narrowing by using initializer control flow analysis instead of discriminant properties.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615417612) **typescript-bot** reported test results and noted unrelated infrastructure failures
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615468257) **typescript-bot** provided requested performance run results with detailed comparison metrics
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3615530759) **typescript-bot** reported that tests on the top 400 repos comparing main and the PR merge all passed
 * [later](https://github.com/microsoft/TypeScript/pull/59745#issuecomment-3771797151) **nekolab** said "Hi @RyanCavanaugh, just a friendly ping if you have time to review this PR, as we got all green from the bot"

### [Issue microsoft/TypeScript#62965](https://github.com/microsoft/TypeScript/issues/62965) (Open, `Bug`, `Domain: LS: Type Display`)

**\`@deprecated\` on property getter and setters\.**

*Regression in TypeScript 5.1.6 causing @deprecated tags on property getters and setters to not be recognized consistently.*

 * (6 days ago) **RyanCavanaugh** added label `Domain: LS: Type Display`, and set milestone to `Backlog`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/62965#issuecomment-3746763003) **a-tarasyuk** pointed out that the change applied only to completion items and explained that getters and setters share a symbol with two declarations requiring each declaration to be deprecated
 * [today](https://github.com/microsoft/TypeScript/issues/62965#issuecomment-3770585196) **KoxyG** said "is this a verified bug?, if yes i would love to give it a try to fix it."

### [Issue microsoft/TypeScript#63003](https://github.com/microsoft/TypeScript/issues/63003) (Closed, `Bug`, `Domain: lib.d.ts`)

**\[Typo\] Possible typo in JSDoc string for \`Math\.trunc\(…\)\` function \(lib\.es2015\.core\.d\.ts\)**

*The JSDoc comment for Math.trunc in lib.es2015.core.d.ts contains a typo with an extra 'the' before 'a numeric expression'.*

 * created by **MichaelZalla**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63003#issuecomment-3765303007) **Yashxp1** said "Yeah, I think it's a typo since x refers to a specific parameter, it should be “the numeric expression x” instead of “a numeric expression, x""
 * [later](https://github.com/microsoft/TypeScript/issues/63003#issuecomment-3773635577) **o-m12a** redirected the issue to the typescript-go repository, created issue #2546 and PR #2547, and suggested further discussion there

### [Issue microsoft/TypeScript#63015](https://github.com/microsoft/TypeScript/issues/63015) (Open, `Bug`, `Fix Available`, `Domain: Crashes`, **gabritto**)

**Regression Crash: RangeError: Maximum call stack size exceeded in isThisInTypeQuery on Nightly**

*Nightly TypeScript crashes with RangeError stack overflow when type-checking a union of call signatures with differing return types*

 * created by **na7ure-a**
 * [later](https://github.com/microsoft/TypeScript/issues/63015#issuecomment-3771901740) **Andarist** said "This is a fallout of https://github.com/microsoft/TypeScript/pull/62243/files#r2264931395 . I'm investigating this and I'll put up a PR with a fix soon"

### [Issue microsoft/TypeScript#63016](https://github.com/microsoft/TypeScript/issues/63016) (Closed)

**Add Scheduler API types**

*Add TypeScript type definitions for globalThis.scheduler and its postTask method per the Scheduler API spec.*

 * created by **dislido**
 * [later](https://github.com/microsoft/TypeScript/issues/63016#issuecomment-3771847224) **Milad93R** offered to work on adding the Scheduler API types, explained that the existing PR was previously blocked but is now unblocked due to Firefox support, and noted that they commented on the PR to advance it for inclusion in future TypeScript releases
 * [later](https://github.com/microsoft/TypeScript/issues/63016#issuecomment-3771906119) **Milad93R** reported that the Scheduler API types were added to the TypeScript-DOM-lib-generator baselines, noted they were not yet in TypeScript 5.9.3, and suggested using the @types/web package as a workaround

### [Issue microsoft/TypeScript#63017](https://github.com/microsoft/TypeScript/issues/63017) (Closed)

**Please search thoroughly in GitHub or by the query site:github\.com/microsoft/TypeScript \<your keywords\> in your favorite search engine before reporting a new bug as most bugs are very likely to find precedents\.  Please fill in each section compl**

*A template reminding contributors to search existing TypeScript issues and thoroughly fill out all bug report sections before submitting.*

 * created by **vinitsati7-rgb**

### [Issue microsoft/TypeScript#63018](https://github.com/microsoft/TypeScript/issues/63018) (Closed)

**Wrong result type for \|\| or ?? operation for interface value and object of some other type structure**

*TypeScript's || and ?? operations with an interface and an incompatible object fail to trigger expected type errors.*

 * created by **blazkovicz**
 * [later](https://github.com/microsoft/TypeScript/issues/63018#issuecomment-3771810414) **MartinJohns** noted that the issue template was incomplete and linked to a playground demonstrating the expected error, suggesting the problem lies in the user's setup
 * [later](https://github.com/microsoft/TypeScript/issues/63018#issuecomment-3772926706) **blazkovicz** said "Wow, this is really interesting. I will check ts config. Thank you!"
 * [later](https://github.com/microsoft/TypeScript/issues/63018#issuecomment-3773005386) **blazkovicz** said "Bug was in our code. All good. thanks."
 * (later) **blazkovicz** closed the issue

### [Issue microsoft/TypeScript#63019](https://github.com/microsoft/TypeScript/issues/63019) (Open)

**Regression: Generic function returning union of tuples is not assignable to identical type since v4\.2**

*TypeScript 4.2 regression incorrectly widens generics causing identical generic functions returning unions of tuples to be unassignable.*

 * created by **ikeyan**

