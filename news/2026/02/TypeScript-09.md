# Report for 2026-02-09 (Monday, February 9th, 2026)

9 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @yjfvictor suggested a feature request for an explicit [[fallthrough]] attribute in [microsoft/TypeScript#46251](https://github.com/microsoft/TypeScript/issues/46251#issuecomment-3875941036)
    * @Ayoub-glitsh requested clearer documentation around generic constraints and indexed access types in [microsoft/TypeScript#62514](https://github.com/microsoft/TypeScript/issues/62514#issuecomment-3874839145)
    * @Ayoub-glitsh offered help with implementation or prototype in [microsoft/TypeScript#62634](https://github.com/microsoft/TypeScript/issues/62634#issuecomment-3874832301)
    * @Ayoub-glitsh offered to help clarify JSDoc guidance and asked if the issue is still open for contributions in [microsoft/TypeScript#62967](https://github.com/microsoft/TypeScript/issues/62967#issuecomment-3874825064)
    * @Ayoub-glitsh offered to implement the feature and asked if maintainers approve in [microsoft/TypeScript#63121](https://github.com/microsoft/TypeScript/issues/63121#issuecomment-3874818261)

## Activity Summary

### [Issue microsoft/TypeScript#23911](https://github.com/microsoft/TypeScript/issues/23911) (Open, `Suggestion`, `In Discussion`)

**Experiment with always using parameters from base types for derived methods**

*Automatically inherit base method parameter types in derived classes to eliminate redundant signatures and prevent implicit any issues.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/23911#issuecomment-1771849728) **jonlepage** criticized the approach as losing prototype reference and class optimisation due to a type feature and deemed it unsuitable
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/23911#issuecomment-1780327203) **tadhgmister** criticized using an arrow function override because it lost prototype reference and class optimizations, provided an alternative implementation using Parameters and ReturnType generics, and suggested supporting issue #36165
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/23911#issuecomment-2079145023) **hediet** suggested covering the `override` case first and provided a simple TypeScript reference implementation using `Parameters` and `ReturnType` utilities
 * [later](https://github.com/microsoft/TypeScript/issues/23911#issuecomment-3877871522) **a-non-a-mouse** proposed a syntax for typing non-arrow function methods to handle generics without losing the prototype chain

### [Issue microsoft/TypeScript#46251](https://github.com/microsoft/TypeScript/issues/46251) (Closed, `Suggestion`, `Out of Scope`)

**Statement to fallthrough in switch cases with \-\-noFallthroughCasesInSwitch**

*Introduce a fallthrough keyword to permit deliberate switch-case fallthrough without disabling the --noFallthroughCasesInSwitch option*

 * (4.3 years ago) **andrewbranch** closed the issue
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/46251#issuecomment-938245272) **FilipeBeck** lamented that JavaScript would never implement anything beyond console warnings when omitting breaks and said the flag was useless without it
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/46251#issuecomment-939148306) **FilipeBeck** said "@andrewbranch Thanks for the clarification."
 * [today](https://github.com/microsoft/TypeScript/issues/46251#issuecomment-3875941036) **yjfvictor** suggested that TypeScript add an explicit [[fallthrough]] statement

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation List**

*Proposed deprecations of outdated TypeScript 6.0 compiler options, with full removal planned for version 7.0.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3774124466) **RyanCavanaugh** stated that noUncheckedIndexAccess would not be enabled by default in strict mode
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3843337972) **RyanCavanaugh** said "Edited to add target: es5 and downlevelIteration (entirely) being deprecated."
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3861434363) **RyanCavanaugh** said "Edited to un-deprecate enum merging and cross-namespace value referencing; these are in 7.0 already and removing them wouldn't produce the upside I had hoped for."
 * [today](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3874952761) **DanielRosenwasser** said "I think we also passed on conditional import fallbacks: https://github.com/microsoft/TypeScript/issues/50762"

### [Issue microsoft/TypeScript#60959](https://github.com/microsoft/TypeScript/issues/60959) (Closed, `Suggestion`, `Fixed`, `Committed`, **jakebailey**)

**tsconfig\.json "lib": "dom" should include "dom\.iterable"\(?\)**

*Automatically include dom.iterable types when the DOM library is specified in tsconfig.json.*

 * (19 weeks ago) **jakebailey** assigned to **jakebailey**, and unassigned **rbuckton**
 * (18 weeks ago) **jakebailey** closed the issue
 * (today) **DanielRosenwasser** added labels `Suggestion`, `Fixed`, `Committed`, removed label `Needs Investigation`, and set milestone to `TypeScript 6.0.0`

### [Issue microsoft/TypeScript#62514](https://github.com/microsoft/TypeScript/issues/62514) (Open, `Docs`)

**Generic constraints are "shallow", don't account for depth subtyping**

*TypeScript’s generic constraints ignore depth subtyping, so T extends { value: string } allows unsafe assignments to T["value"].*

 * created by **sliminality**
 * **RyanCavanaugh** added label `Docs`
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/62514#issuecomment-3353931177) **RyanCavanaugh** said "This could go in the Indexed Access Types section, since it's really the T['name'] expression resolving to string (instead of staying deferred) that's the root cause of the behavior"
 * [today](https://github.com/microsoft/TypeScript/issues/62514#issuecomment-3874839145) **Ayoub-glitsh** commented that the inconsistency between primitive and object generic constraints around indexed access types was confusing and requested clearer documentation

### [Issue microsoft/TypeScript#62529](https://github.com/microsoft/TypeScript/issues/62529) (Closed, `Suggestion`, `Breaking Change`, `Discussion`, **andrewbranch**)

**\`esModuleInterop\` and \`allowSyntheticDefaultImports\` in TypeScript 6\.0\+**

*Improve TypeScript 6.0+ interoperability options to support default imports from both pure CJS modules and ESM-transpiled CJS files.*

 * **RyanCavanaugh** added label `Discussion`
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/62529#issuecomment-3378243563) **andrewbranch** reported that the design meeting concluded to deprecate allowSyntheticDefaultImports (making it always-on), migrate DT for less ambiguity, and rely on verbatimModuleSyntax to mitigate the soundness hole
 * (15 weeks ago) **andrewbranch** closed the issue
 * (today) **DanielRosenwasser** added labels `Breaking Change`, `Suggestion`, and set milestone to `TypeScript 6.0.0`

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3865491719) **justingrant** expressed support for TS integrating Temporal and suggested contributing polyfill declaration types to lib.d.ts for compatibility, citing existing Temporal TS types and recommending tagging proposal champions
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3867787970) **justingrant** inquired where MDN showed content about custom calendars
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3867845545) **jakebailey** clarified that they had confused custom calendars with non-Gregorian calendars
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3873092192) **jakebailey** noted that correct emission of names and types into .d.ts files is more critical for compatibility, observed that the current definitions likely satisfy this, and invited testing and suggestions before the 6.0 RC cut

### [Issue microsoft/TypeScript#62634](https://github.com/microsoft/TypeScript/issues/62634) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: make hover tooltips more readable by showing the generic parameters names instead of their value \(in some cases\)\.\.**

*Show generic parameter names instead of their full types by default in hover tooltips to improve readability.*

 * created by **denis-migdal**
 * (16 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/62634#issuecomment-3874832301) **Ayoub-glitsh** praised the proposal’s DX improvements and offered to help implement a prototype

### [Issue microsoft/TypeScript#62967](https://github.com/microsoft/TypeScript/issues/62967) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`)

**JSDoc comments for async\_hooks are confusing/misleading**

*JSDoc comments in the async_hooks module misleadingly discourage its use while recommending AsyncLocalStorage, causing confusion in TypeScript.*

 * (3 weeks ago) **RyanCavanaugh** added label `Experience Enhancement`, and set milestone to `Backlog`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62967#issuecomment-3757602066) **pranamya123** said "Hi @a-non-a-mouse  I’ve opened a PR in DefinitelyTyped to clarify the async_hooks JSDoc warning so it doesn’t read as discouraging the module while recommending AsyncLocalStorage from the same import."
 * [today](https://github.com/microsoft/TypeScript/issues/62967#issuecomment-3874825064) **Ayoub-glitsh** offered to clarify the JSDoc guidance and volunteered to fix the issue if it was still open

### [PR microsoft/TypeScript#63071](https://github.com/microsoft/TypeScript/pull/63071) (Closed, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Deprecate downlevelIteration**

*Deprecate the downlevelIteration compiler flag in TypeScript 7.0 since it’s redundant for ES2015+ targets.*

 * **jakebailey** added label `Breaking Change`
 * [6 days ago](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3843827126) **typescript-bot** reported the results of running the top 800 repositories with tsc comparing `main` and the pull request merge and noted an interesting change
 * (5 days ago) **jakebailey** closed the issue
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.0`

### [Issue microsoft/TypeScript#63082](https://github.com/microsoft/TypeScript/issues/63082) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add support for OSC8 hyperlinks in TTY output**

*Support OSC8 hyperlinks in TypeScript build output to enable reliable clickable file paths in terminal emulators*

 * (6 days ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63082#issuecomment-3842777187) **Ayoub-glitsh** offered to help and requested assignment to investigate and propose an implementation
 * [later](https://github.com/microsoft/TypeScript/issues/63082#issuecomment-3876231994) **mrazauskas** pointed out that the OSC8 hyperlink implementation in Jest previously caused visual issues such as flickers, jumps, slower rendering and cluttered underlines, and noted that a revert was accepted

### [Issue microsoft/TypeScript#63121](https://github.com/microsoft/TypeScript/issues/63121) (Open)

**Display files with errors summary in \`\-\-watch\` mode**

*Enhance tsc --watch to display a summary of files with errors and their counts after each compilation*

 * created by **dwjohnston**
 * [today](https://github.com/microsoft/TypeScript/issues/63121#issuecomment-3874818261) **Ayoub-glitsh** offered to implement a file-level error summary in --watch mode pending maintainer approval

### [PR microsoft/TypeScript#63123](https://github.com/microsoft/TypeScript/pull/63123) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.0 to 4\.32\.2 in the github\-actions group**

*Upgrade the github-actions group’s github/codeql-action from version 4.32.0 to 4.32.2 to update the default CodeQL bundle.*

 * (yesterday) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63124](https://github.com/microsoft/TypeScript/pull/63124) (Closed, `For Uncommitted Bug`)

**feat\(watch\): show file\-level error summary in watch mode**

*Update watch mode to display a detailed per-file error summary using getErrorSummaryText and a new diagnostic message*

 * created by **suvendukungfu**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63124#issuecomment-3871128563) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63124#issuecomment-3872885080) **suvendukungfu** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63125](https://github.com/microsoft/TypeScript/issues/63125) (Open)

**Inline typing for object destructuring in function parameters**

*Enable inline type annotations for object destructuring in function parameters to avoid redundant type repetition.*

 * created by **benhatsor**
 * [today](https://github.com/microsoft/TypeScript/issues/63125#issuecomment-3874804343) **MartinJohns** said "Duplicate of #29526."

