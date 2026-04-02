# Report for 2026-01-23 (Friday, January 23rd, 2026)

11 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @devanshj provided an experimental PR for existential types in [microsoft/TypeScript#30581](https://github.com/microsoft/TypeScript/issues/30581#issuecomment-3794249198)
    * @nnmrts asked why this isn't the default and what would break in [microsoft/TypeScript#37527](https://github.com/microsoft/TypeScript/issues/37527#issuecomment-3794180526)
    * @JosXa asked OpenCode to take a stab at this in [microsoft/TypeScript#63039](https://github.com/microsoft/TypeScript/issues/63039#issuecomment-3792416694)
    * @JosXa provided a detailed investigation summary in [microsoft/TypeScript#63039](https://github.com/microsoft/TypeScript/issues/63039#issuecomment-3792579763)

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3794176642) **zakhenry** said "!User reads as "not User" to me, especially for those familiar with Rust syntax e.g. !Send means a type that does not implement Send."

### [Issue microsoft/TypeScript#30581](https://github.com/microsoft/TypeScript/issues/30581) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Wishlist: support for correlated union types**

*Support correlated discriminated union types so TypeScript infers matching f and v properties and allows record.f(record.v) without errors.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/30581#issuecomment-1805251779) **jedwards1211** proposed a syntax `<expr> for branch of <identifier>` to typecheck each branch of a record separately and union the resulting types
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/30581#issuecomment-1805791448) **jcalz** said "@jedwards1211 Like #25051 (which was closed as a duplicate 🤷‍♂️)"
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/30581#issuecomment-1806074746) **jedwards1211** said "Why yes...I agree with you that should not have been closed as a duplicate"
 * [later](https://github.com/microsoft/TypeScript/issues/30581#issuecomment-3794249198) **devanshj** noted that despite the fix by #47109 some StackOverflow issues remained unsolved and suggested using existential types by linking an experimental PR

### [Issue microsoft/TypeScript#37527](https://github.com/microsoft/TypeScript/issues/37527) (Open, `Needs Investigation`)

**new Map\(\) infers type only from the first item in the iterable**

*new Map infers its key and value types only from the first iterable entry, causing mismatched types without explicit generics.*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/37527#issuecomment-750412755) **ModProg** mentioned that Map type inference from parameter type still failed and provided a code example
 * [51 weeks ago](https://github.com/microsoft/TypeScript/issues/37527#issuecomment-2625995075) **jcalz** said "cross-linking #39133"
 * [51 weeks ago](https://github.com/microsoft/TypeScript/issues/37527#issuecomment-2625999667) **jcalz** suggested that interested parties could locally merge a MapConstructor interface snippet into their environment to get the desired behavior
 * [later](https://github.com/microsoft/TypeScript/issues/37527#issuecomment-3794180526) **nnmrts** asked why merging the interface into the environment wasn't the default and what would break

### [PR microsoft/TypeScript#60646](https://github.com/microsoft/TypeScript/pull/60646) (Closed, `For Backlog Bug`)

**Add the type of Intl\.DurationFormat to the lib\.**

*Add initial type definitions for the Intl.DurationFormat API to the TypeScript standard library declarations*

 * [11 weeks ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3480333874) **Standard8** said "It looks like there's just one change remaining to complete this. Would it be possible that it could happen soon, or should someone take over (or maybe a maintainer can change the branch?)?"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3654395110) **smorimoto** said "Gentle ping"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3659820449) **developer-bandi** apologized for the delay and reflected the requested changes in the PR
 * [later](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3794808977) **petamoriken** said "@developer-bandi The format CI is failing. Could you take a look at it?"
 * [later](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3794844061) **petamoriken** offered to add the ES2025 target via a pull request, asked to take over the existing changes to build upon them, and noted having created the PR with a Co-authored-by commit

### [Issue microsoft/TypeScript#61735](https://github.com/microsoft/TypeScript/issues/61735) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Add ES2025 target and library**

*Add ES2025 as a TypeScript compilation target and library to support upcoming syntax and standard APIs.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/61735#issuecomment-3140226507) **CavaliereDavid** said "Is this a good first issue? I would like to contribute"
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [later](https://github.com/microsoft/TypeScript/issues/61735#issuecomment-3794800718) **petamoriken** said "I'll work for this issue"

### [Issue microsoft/TypeScript#62630](https://github.com/microsoft/TypeScript/issues/62630) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow classes to implement unions of object types**

*Allow classes to implement unions of object types with identical properties for discriminated type narrowing.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3780881723) **justinfagnani** explained that he kept interfaces and union types, dropped the class, and demonstrated the existing mutation problem, and asked valler to clarify the analogy
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3781173035) **DanielRosenwasser** asked if the provided code snippet met the requirements
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3781279691) **justinfagnani** reported that the proposed construction failed to narrow 'this' in methods and demonstrated the type error with a code snippet
 * [today](https://github.com/microsoft/TypeScript/issues/62630#issuecomment-3793277857) **valler** argued that union types already exhibited mutation hazards and questioned the need for classes implementing unions, providing examples and explanations

### [PR microsoft/TypeScript#63026](https://github.com/microsoft/TypeScript/pull/63026) (Open, `For Milestone Bug`, **gabritto**)

**Fixed a crash caused by circularly\-reentrant \`getEffectsSignature\`**

*Restores control flow container flags to function-like type-level nodes to prevent circular recursion in getEffectsSignature.*

 * (2 days ago) **typescript-bot** added label `For Milestone Bug`, and assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3790911144) **ahejlsberg** expressed unease about introducing a stopgap recursion limiter and suggested restoring original ContainerFlags.IsControlFlowContainer values to match previous behavior
 * [today](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3791104920) **Andarist** said "Thanks for the feedback. I’ll work on the suggested solution"

### [Issue microsoft/TypeScript#63028](https://github.com/microsoft/TypeScript/issues/63028) (Closed, `Not a Defect`)

**\(ES2024\) The resolving function in Promise\.withResolvers\(\) is not allowed to be passed no arguments \(void\) unless explicitly specified**

*In ES2024, Promise.withResolvers() erroneously treats its resolve function as requiring arguments unless explicitly typed as void.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63028#issuecomment-3781015419) **rugk** thanked for the link, tested the old-school Promise approach and confirmed the error, found the void handling unexpected, and suggested adding documentation on Promise handling
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63028#issuecomment-3781046115) **RyanCavanaugh** explained that explicitly using Promise.withResolvers<void> was unnecessary since void is the default and that TypeScript errs on the side of safety distinguishing omitted versus provided arguments, suggesting resolve(undefined) to omit values
 * [today](https://github.com/microsoft/TypeScript/issues/63028#issuecomment-3793358023) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63030](https://github.com/microsoft/TypeScript/pull/63030) (Open, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Deprecate alwaysStrict: false in TypeScript 6\.0**

*TypeScript 6.0 deprecates alwaysStrict=false, emitting warnings and requiring ignoreDeprecations to silence them ahead of its removal in 7.0.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787552435) **typescript-bot** reported test results comparing main and PR merge, noted infrastructure failures but otherwise found no issues
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787619893) **typescript-bot** provided the requested performance run results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787685188) **typescript-bot** provided results of running tsc on the top 400 repos comparing main and the pull request merge and reported that everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3791464828) **jakebailey** noted that the PR would not detect the problem because alwaysStrict can be disabled by setting strict to false and suggested forcing alwaysStrict when strict is false

### [PR microsoft/TypeScript#63035](https://github.com/microsoft/TypeScript/pull/63035) (Closed, `For Uncommitted Bug`)

**Add messageformat types**

*Add TypeScript type definitions for the messageformat library to improve type safety*

 * created by **aprameyak**
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63035#issuecomment-3782352197) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63035#issuecomment-3792140073) **jakebailey** said "#63025"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63039](https://github.com/microsoft/TypeScript/issues/63039) (Open)

**Regression of \`this is\` type predicate for intersection of unions from 4\.7 to 4\.8**

*TypeScript 4.8 regression prevents this is type predicates from correctly narrowing intersection of union types that worked in 4.7*

 * created by **KnorpelSenf**
 * [today](https://github.com/microsoft/TypeScript/issues/63039#issuecomment-3792416694) **JosXa** said "Hey OpenCode, can you take a stab at this?"
 * [today](https://github.com/microsoft/TypeScript/issues/63039#issuecomment-3792579763) **JosXa** investigated and identified a regression in TypeScript 4.8 where type predicate narrowing on unions with conflicting property types produced a never intersection

### [PR microsoft/TypeScript#63043](https://github.com/microsoft/TypeScript/pull/63043) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix transform crash with destructured parameter property **

*Ensure the compiler skips transforming illegal destructured parameter properties to prevent crashes when targeting ES2024*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63044](https://github.com/microsoft/TypeScript/issues/63044) (Closed, `Fix Available`)

**Crash: Stack overflow when checking identifier in binding pattern with strict mode enabled**

*When strict mode is enabled, TypeScript crashes with a stack overflow while checking an identifier in a binding pattern with an optional default parameter.*

 * created by **na7ure-a**
 * [later](https://github.com/microsoft/TypeScript/issues/63044#issuecomment-3794617524) **MartinJohns** said "Related: #62282"
 * **typescript-bot** added label `Fix Available`
 * [later](https://github.com/microsoft/TypeScript/issues/63044#issuecomment-3794871156) **Andarist** mentioned that his proposed fix for a related TypeScript issue already fixed this one and is likely implemented in the Go port via PR #2542 with a working example in the TS Go playground

