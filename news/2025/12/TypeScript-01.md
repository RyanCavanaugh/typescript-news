# Report for 2025-12-01 (Monday, December 1st, 2025)

11 different users commented on 66 different issues.

## Recommended Actions

 * Response Recommended
    * @alpha2420 asked for guidelines or initial steps to follow in [microsoft/TypeScript#62737](https://github.com/microsoft/TypeScript/issues/62737#issuecomment-3597562402)
    * @TyIsI asked whether documentation should reference this in the wiki page in [microsoft/TypeScript#62815](https://github.com/microsoft/TypeScript/issues/62815#issuecomment-3599338551)

## Activity Summary

### [Issue microsoft/TypeScript#38520](https://github.com/microsoft/TypeScript/issues/38520) (Open, `Suggestion`, `Awaiting More Feedback`)

**Object\.values and Object\.entries are unsound and inconsistent with Object\.keys\.**

*Update Object.values and Object.entries to use sound generic types consistent with Object.keys and eliminate current unsound behavior.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/38520#issuecomment-1579899854) **babur001** suggested using Rambda's toPairs to convert an object into key/value pairs and shared example code and docs
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/38520#issuecomment-1582493088) **devinrhode2** suggested ts-extras and Froebel as alternative libraries with typed utilities
 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/38520#issuecomment-1646797657) **craigphicks** argued that property keys and values have different needs and consistency isn't necessary because keys have limited type range and values require explicit typing
 * [today](https://github.com/microsoft/TypeScript/issues/38520#issuecomment-3599885901) **jedwards1211** suggested adding a compiler option to choose whether Object.keys() returned (keyof T)[] or string[] due to unsound Record<string, T> typing

### [PR microsoft/TypeScript#53017](https://github.com/microsoft/TypeScript/pull/53017) (Open, `For Backlog Bug`, **ahejlsberg**)

**Infer type parameters from indexes on those parameters**

*Infer generic type parameters in TypeScript based on index accesses of those parameters.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591710203) **typescript-bot** provided the requested performance run results comparing baseline to the PR
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591733538) **typescript-bot** provided comparative tsc results for top 400 repos, highlighted build failures in react-navigation/react-navigation, and requested a review
 * [yesterday](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3592607394) **Andarist** provided repro examples with react-hook-form and TS playground links
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3598522672) **jakebailey** requested the TypeScript bot to test and pack
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3598522899) **typescript-bot** posted automated CI status update listing build jobs and results
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3598536620) **typescript-bot** provided an installable tgz and playground/npm module links for testing the TypeScript 6.0.0-insiders build
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3598605009) **typescript-bot** reported DT test results and noted a compile error in rdfjs__data-model due to an unused '@ts-expect-error' directive
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3598620093) **typescript-bot** reported user test results comparing main and the pull request, noted an infrastructure failure and new TS2345 errors in webpack configurations
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3598704011) **typescript-bot** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3598803595) **typescript-bot** provided tsc build comparison results for top repositories and highlighted a tldraw build failure

### [Issue microsoft/TypeScript#62737](https://github.com/microsoft/TypeScript/issues/62737) (Open, `Suggestion`, `Help Wanted`, `Experimentation Needed`)

**Show incompatible union members in discriminated union discriminator errors**

*Enhance TypeScript's discriminated union error messages to identify which union members in the discriminator cause assignment failures.*

 * (3 weeks ago) **RyanCavanaugh** added labels `Experimentation Needed`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62737#issuecomment-3597562402) **alpha2420** said "Hi @jankeape, I’d like to start working on this issue. Please let me know if there are any guidelines or initial steps I should follow."

### [Issue microsoft/TypeScript#62779](https://github.com/microsoft/TypeScript/issues/62779) (Open, `Bug`, `Help Wanted`, `Domain: This-Typing`)

**Type parameter leak caused by \`this\` and reverse mapped type**

*Referencing this in a reverse-mapped generic function causes the type parameter T to leak into the inferred object type.*

 * (1 week ago) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62779#issuecomment-3564415404) **learn-dumboo24** said "Hey @Andarist, I would like to work on this issue can you please assign it to me. "
 * **RyanCavanaugh** added label `Domain: This-Typing`

### [Issue microsoft/TypeScript#62780](https://github.com/microsoft/TypeScript/issues/62780) (Closed, `Bug`, `Help Wanted`, `Domain: LS: Refactorings`, `7.0 LS Migration`)

**"Move to file" Code Action/Hint triggers in an if statement in JS**

*Move to new file action is inappropriately triggered inside JavaScript if/else statements, moving the whole block instead of the intended portion.*

 * (1 week ago) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: LS: Refactorings`

### [Issue microsoft/TypeScript#62787](https://github.com/microsoft/TypeScript/issues/62787) (Open, **Copilot**)

**"Never nullish" checks miss "never nullish" through parens**

*TypeScript’s never-nullish checks inconsistently fail to flag parenthesized never-nullish expressions.*

 * created by **jakebailey**
 * **jakebailey** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript/issues/62787#issuecomment-3598073776) **RyanCavanaugh** provided an automated list of similar issues for potential duplicates

### [PR microsoft/TypeScript#62790](https://github.com/microsoft/TypeScript/pull/62790) (Open, `For Backlog Bug`)

**Fix compiler crash on generics overload resolution failure**

*Generate appropriate diagnostics instead of invoking Debug.fail to avoid compiler crashes when generic overload resolution fails.*

 * created by **moznion**
 * **typescript-bot** added label `For Backlog Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3561575931) **moznion** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3599611006) **jakebailey** said "I think this is just papering over a bug somewhere else. IIRC the intent of these debug fails are to assert that the previous steps added an error."

### [Issue microsoft/TypeScript#62798](https://github.com/microsoft/TypeScript/issues/62798) (Open, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`, `Cursed?`)

**Conditional type eagerly calculated to be invariant breaks referential transparency**

*Eager evaluation of conditional type F<T> as invariant breaks referential transparency, making F<{}> extends F<{a:string}> yield false instead of true*

 * (1 week ago) **RyanCavanaugh** added label `Cursed?`, and set milestone to `Backlog`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/62798#issuecomment-3574814438) **Andarist** said "I can only confirm that F is measured to be invariant here and that the other example ends up comparing different type aliases so it goes straight~ to the structural comparison."
 * **RyanCavanaugh** added label `Domain: check: Variance Relationships`

### [PR microsoft/TypeScript#62799](https://github.com/microsoft/TypeScript/pull/62799) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Update GitHub Actions in the root directory by bumping actions/checkout to v6.0.0 and github/codeql-action*

 * (1 week ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62806](https://github.com/microsoft/TypeScript/issues/62806) (Open)

**Self\-referencing causes non\-portable inferred types \(TS2742\) false positive**

*A self-referencing import in package c triggers a false-positive TS2742 non-portable type inference error in project builds.*

 * created by **gluxon**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/62806#issuecomment-3579055371) **gluxon** added usage context, explained that they fixed false positives with a lint rule, and noted the issue's low priority
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/62806#issuecomment-3579063584) **gluxon** described debugging notes highlighting two issues with module resolution in built outputs and in --build mode
 * [today](https://github.com/microsoft/TypeScript/issues/62806#issuecomment-3598073957) **RyanCavanaugh** provided an auto-generated response listing similar issues and thanked the user

### [Issue microsoft/TypeScript#62807](https://github.com/microsoft/TypeScript/issues/62807) (Closed, `Duplicate`)

**Switch doesn't narrow type when type isn't a disc union**

*Switch statement on a non-discriminated type does not narrow the default branch to never as expected.*

 * created by **aryzing**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62807#issuecomment-3580828234) **MartinJohns** said "Duplicate of #13182."
 * [today](https://github.com/microsoft/TypeScript/issues/62807#issuecomment-3598074013) **RyanCavanaugh** provided an automatically generated reply with analysis, examples, and relevant FAQs explaining switch-based narrowing and union type behavior in TypeScript
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#62808](https://github.com/microsoft/TypeScript/pull/62808) (Closed, `For Uncommitted Bug`)

**Update CopyrightNotice\.txt \(typo\)**

*Correct the typo in CopyrightNotice.txt.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/62808#issuecomment-3583225309) **justanotheranonymoususer** asked what work was needed and told to merge it
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/62808#issuecomment-3584858733) **MartinJohns** said "The work consists of reviewing the changes and making sure they're correct. The work consists of fixing the automated checks (which are currently failing due to your change)."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/62808#issuecomment-3584868877) **justanotheranonymoususer** stated that if tests fail due to a typo fix in a text file, the tests are flawed
 * [today](https://github.com/microsoft/TypeScript/pull/62808#issuecomment-3598053356) **RyanCavanaugh** said "If you're going to send a PR for a typo in defiance of the contributing guidelines, please at least send one that doesn't break the build"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62809](https://github.com/microsoft/TypeScript/issues/62809) (Open, `Help Wanted`)

**Typo in CopyrightNotice\.txt**

*CopyrightNotice.txt contains a typo with “MERCHANTABLITY” misspelled.*

 * created by **justanotheranonymoususer**
 * (today) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#62811](https://github.com/microsoft/TypeScript/pull/62811) (Closed, `For Uncommitted Bug`)

**Improve satisfies semantics: return never when target type is never**

*Make TypeScript’s satisfies operator narrow expressions to never when the specified target type is exactly never.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/62811#issuecomment-3585583356) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/62811#issuecomment-3586965882) **MartinJohns** said "Won't this change allow foo satisfies never when foo does not satisfy never?"
 * [today](https://github.com/microsoft/TypeScript/pull/62811#issuecomment-3598210135) **RyanCavanaugh** questioned the change's goal and noted it was unapproved, explaining that `assertNever(foo satisfies never)` is equivalent to `assertNever(foo)`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62812](https://github.com/microsoft/TypeScript/issues/62812) (Open, `Bug`, `Help Wanted`, `Domain: Conditional Types`)

**Spread operator fails to distribute over union when recursive type call is inlined instead of aliased**

*TypeScript’s spread operator fails to distribute over union types when using an inlined recursive type instead of an alias.*

 * created by **MMF2**
 * [today](https://github.com/microsoft/TypeScript/issues/62812#issuecomment-3598074105) **RyanCavanaugh** provided an automated list of similar issues for context
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#62813](https://github.com/microsoft/TypeScript/pull/62813) (Open, `For Uncommitted Bug`)

**Add go\-to\-definition inference for shadowed namespaces**

*Enhance go-to-definition behavior in shadowed namespaces by inferring the correct symbol through kind comparison with a timeout-based fallback.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3587615019) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3587618790) **PierceLanternStudios** said "@microsoft-github-policy-service agree"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3587768314) **rattrayalex** asked for thoughts on supporting namespace/interface shadowing patterns used by Stripe, OpenAI, and Anthropic SDKs
 * [today](https://github.com/microsoft/TypeScript/pull/62813#issuecomment-3597836148) **jakebailey** criticized the change as non-idempotent and asked to try the new language server to see if the issue persists

### [Issue microsoft/TypeScript#62814](https://github.com/microsoft/TypeScript/issues/62814) (Closed, `Working as Intended`)

**Inference mismatch in strict and non\-strict mode**

*TypeScript strict mode erroneously changes boolean literal inference, causing compilation errors absent in non-strict mode.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3588396026) **MartinJohns** explained how enabling or disabling strictNullChecks changes type inference for the logical-or expression, causing different types for ‘miniature’ and affecting assignment compatibility
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3589201164) **dipeshkaphle** asked if the behavior was documented in the strict mode docs
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3589290382) **MartinJohns** referenced the TypeScript handbook sections on strict null checks and truthiness narrowing
 * [today](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3598074176) **RyanCavanaugh** provided an automatically generated list of similar issues with relevance percentages
 * **RyanCavanaugh** added label `Working as Intended`

### [Issue microsoft/TypeScript#62815](https://github.com/microsoft/TypeScript/issues/62815) (Closed, `Working as Intended`)

**Getting error 2576 when accessing static methods of a class as a passed parameter\.**

*Invoking a static class method on a parameter typed as the class instance leads to TypeScript error 2576.*

 * created by **TyIsI**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62815#issuecomment-3590630122) **MartinJohns** explained how to access static members by using typeof Fafo1 instead of an instance of the class
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62815#issuecomment-3590639917) **TyIsI** acknowledged that using typeof solved the issue, speculated on prototype comparison behavior, and asked whether this should be documented due to confusing error
 * [today](https://github.com/microsoft/TypeScript/issues/62815#issuecomment-3598074225) **RyanCavanaugh** thanked the user and explained that the field was typed as an instance rather than the constructor type, suggesting to declare it as `typeof Fafo1` so the static method can be called
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/62815#issuecomment-3599338551) **TyIsI** asked whether documentation should reference the solution on the wiki page
 * (today) **TyIsI** closed the issue

### [Issue microsoft/TypeScript#62816](https://github.com/microsoft/TypeScript/issues/62816) (Closed, `Question`)

**\`tsc\` transpile js to js converts Set iteration loops to invalid numeric key indexing**

*Transpiling JavaScript with tsc’s allowJs option converts Set for-of loops into invalid .length-based index loops.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591683354) **sparr** thanked the maintainers and expressed confusion about invalid code being "working as intended"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591703024) **MartinJohns** explained that downleveling to ES5 intentionally produced the correct for-of loop code and that enabling type checks would warn about missing length properties
 * [today](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3596641898) **nmain** suggested using the downlevelIteration option and explained that ES6 features like Set and iterators can't be polyfilled properly
 * [today](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3598074292) **RyanCavanaugh** provided automated analysis linking to similar issues
 * **RyanCavanaugh** added label `Question`

### [Issue microsoft/TypeScript#62819](https://github.com/microsoft/TypeScript/issues/62819) (Closed, `Duplicate`)

**invalid behavior of \`satisfies\`**

*TypeScript’s satisfies operator fails to flag extra spread properties from a const union object while direct object literals error*

 * created by **salisbury-espinosa**
 * [today](https://github.com/microsoft/TypeScript/issues/62819#issuecomment-3596691093) **MartinJohns** said "Duplicate of #39998."
 * [today](https://github.com/microsoft/TypeScript/issues/62819#issuecomment-3598074343) **RyanCavanaugh** provided an automated analysis of how 'satisfies' handles excess properties with object literals and spread expressions and linked to relevant FAQs
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#62820](https://github.com/microsoft/TypeScript/issues/62820) (Closed, `Suggestion`, `Out of Scope`)

**@Concurrent decorator**

*Add a @Concurrent decorator to iterate loops concurrently with optional batching and Promise.all or Promise.allSettled logic.*

 * created by **Mindaugas3**
 * [today](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3597843019) **MartinJohns** said "This is explicitly out of scope for TypeScript."
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Out of Scope`

### [PR microsoft/TypeScript#62821](https://github.com/microsoft/TypeScript/pull/62821) (Open, `For Uncommitted Bug`)

**Fix: Allow arbitrary attribute order in triple\-slash directives**

*Refactor createGroupChannel to use SaveMultipleMembers instead of individual SaveMember calls to reduce database queries.*

 * created by **Bitshifter-9**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62821#issuecomment-3600356974) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62821#issuecomment-3600356977) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62821#issuecomment-3600357455) **microsoft-github-policy-service[bot]** prompted the contributor to agree to the CLA by replying with the appropriate command

### [PR microsoft/TypeScript#62822](https://github.com/microsoft/TypeScript/pull/62822) (Open, `For Uncommitted Bug`)

**Replace replaceable indexed accesses early to reuse cache entries**

*Use replaceIndexedAccess earlier in TypeScript to maximize cache reuse when constructing reverse-mapped type objects.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62822#issuecomment-3601581037) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/62822#issuecomment-3602189469) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/62822#issuecomment-3602189725) **typescript-bot** reported status updates for CI build jobs
 * [later](https://github.com/microsoft/TypeScript/pull/62822#issuecomment-3602286221) **typescript-bot** reported that the DT tests ran with identical results and shared the log link
 * [later](https://github.com/microsoft/TypeScript/pull/62822#issuecomment-3602308435) **typescript-bot** reported user test results, noted a Git clone failure and that everything else looked good
 * [later](https://github.com/microsoft/TypeScript/pull/62822#issuecomment-3602413804) **typescript-bot** provided the requested performance run results
 * [later](https://github.com/microsoft/TypeScript/pull/62822#issuecomment-3602566365) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the pull request merge yielded no issues

