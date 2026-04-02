# Report for 2025-12-05 (Friday, December 5th, 2025)

7 different users commented on 31 different issues.

## Recommended Actions

 * Moderation
    * @bimocd posted rude content in [microsoft/TypeScript#30919](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3618885329)
 * Response Recommended
    * @dbrxnds asked whether an issue should be opened in the native repo to track the Go port in [microsoft/TypeScript#60005](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3620601531)

## Activity Summary

### [Issue microsoft/TypeScript#30919](https://github.com/microsoft/TypeScript/issues/30919) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: shorthand for templated type to extend and default to the same type**

*Add shorthand syntax to declare generic parameters that both extend and default to the same type using 'is' or similar.*

 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-693558456) **AlansCodeLog** asked for updates on the 'extends =' syntax feature and described its space-saving benefits
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-787397165) **tannerlinsley** expressed support for the syntax improvement and offered to help implement it
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-1731173950) **vzakharov** said "I’d love this, please also consider this possible syntax: https://github.com/microsoft/TypeScript/issues/55826"
 * [today](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3618369276) **bimocd** expressed support for the feature request and noted surprise at lack of response after six years
 * [today](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3618603965) **RyanCavanaugh** said "There are nearly 3,000 open suggestions, you can't really expect all of them to be in the language. The documentation would be the size of an encyclopedia."
 * [today](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3618885329) **bimocd** criticized the dismissive reply and defended the suggestion as a simple extension of TypeScript’s existing philosophy

### [PR microsoft/TypeScript#55222](https://github.com/microsoft/TypeScript/pull/55222) (Open, `Experiment`, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**Remove reportErrors check in relateVariances**

*Remove the reportErrors check in relateVariances to prevent inconsistent relation behavior in error and non-error modes.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613665151) **typescript-bot** reported user test results indicating a Git clone failure but otherwise no issues
 * [yesterday](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613801361) **typescript-bot** provided the performance run results for tsc including comparison metrics
 * [yesterday](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3613929898) **typescript-bot** reported results of running tsc on top 400 repos comparing main and PR merge and noted everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3617679166) **jakebailey** questioned whether it was finally acceptable and asked @typescript-bot to run performance tests faster
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3617679393) **typescript-bot** posted an automated build status update including command, status, and results links
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3617858059) **typescript-bot** reported the requested performance run results with a comparison report
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3617928264) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3617928643) **typescript-bot** provided automated build status updates for several commands
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618016640) **typescript-bot** reported the results of running the DT tests, showing debug failure errors in ember and ember/v3 packages related to cached relationship mismatches
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618043520) **typescript-bot** reported user test results indicating a Git clone failure but otherwise no issues
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618139025) **typescript-bot** reported perf run results for tsc with detailed comparison metrics
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618174081) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618174396) **typescript-bot** updated CI job status and linked build results for the 'pack this' command
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618194249) **typescript-bot** provided an installable tgz link and installation instructions
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618259691) **typescript-bot** reported results of running tsc on top 400 repos comparing main and PR merge and noted everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618522613) **Andarist** provided a repro snippet illustrating the ember break issue

### [PR microsoft/TypeScript#59682](https://github.com/microsoft/TypeScript/pull/59682) (Open, `For Backlog Bug`)

**Normalize \`NoInfer\`red tuple types in rest/spread positions**

*Ensure NoInfer-wrapped tuple types are correctly normalized in rest and spread type positions.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#60005](https://github.com/microsoft/TypeScript/pull/60005) (Open, `For Backlog Bug`)

**Add source mappings for serialized properties with available declaration**

*Enable generating source mappings for serialized properties in output files when their declarations exist*

 * [12 weeks ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3269469395) **mamlzy** said "sorry for tagging @Andarist, is this pr going to be merged?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3547407768) **prometx11** asked if the change could be merged soon because it was blocking go-to navigation in monorepos and degrading developer experience
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3554914218) **jakebailey** requested merging main and inquired about porting to the Go codebase
 * [later](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3620601531) **dbrxnds** said "Should there be an issue opened in the native repo to track this for the go port? We recently switched to go but would like for this to stick. "

### [PR microsoft/TypeScript#61092](https://github.com/microsoft/TypeScript/pull/61092) (Open, `For Backlog Bug`)

**Do not defer index types on intersections containing \`NoInfer\` types with non\-instantiable base type**

*Prevent deferring index type resolution for intersection types containing NoInfer types with non-instantiable base types.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#61185](https://github.com/microsoft/TypeScript/pull/61185) (Open, `For Backlog Bug`)

**Contextual typing for return expressions of functions with contextual signatures based on instantiated types**

*Enable contextual typing of function return expressions when functions have contextual signatures derived from instantiated types.*

 * created by **Andarist**
 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/61185#issuecomment-2661094891) **Andarist** said "@jakebailey would you be so kind and run tests here? :)"
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#61233](https://github.com/microsoft/TypeScript/pull/61233) (Open, `For Backlog Bug`)

**Fixed accidental \`undefined\` omissions in union props sourced from index types under \`noUncheckedIndexedAccess\`**

*Ensures that union type properties derived from index types correctly include undefined when noUncheckedIndexedAccess is enabled.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/61233#issuecomment-2672365029) **typescript-bot** reported that user tests with tsc comparing main and the pull request merge passed with no issues
 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/61233#issuecomment-2672411836) **typescript-bot** provided the results of the requested performance run with a detailed comparison report
 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/61233#issuecomment-2672533422) **typescript-bot** provided results of running the top 400 repos with tsc comparing main and PR merge and reported everything looked good
 * **typescript-bot** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#61524](https://github.com/microsoft/TypeScript/issues/61524) (Open, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`, `Fix Available`)

**Error: Debug Failure\. No error for last overload signature**

*TypeScript nightly v5.9.0-dev crashes with "Debug Failure. No error for last overload signature" during overload resolution in a generic function.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/61524#issuecomment-2780342066) **Andarist** described that relateVariances behaves differently on reportErrors leading to inconsistent results and noted that PR #55222 would fix it
 * **RyanCavanaugh** added label `Domain: Variance Relationships`
 * **typescript-bot** added label `Fix Available`

### [PR microsoft/TypeScript#61980](https://github.com/microsoft/TypeScript/pull/61980) (Open, `For Backlog Bug`)

**Fixed \`anyFunctionType\` leak**

*Resolved a memory leak in TypeScript’s anyFunctionType internal type implementation.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript/pull/61980#issuecomment-3021091939) **typescript-bot** reported that tsc user tests passed successfully when comparing main and the pull request merge
 * [22 weeks ago](https://github.com/microsoft/TypeScript/pull/61980#issuecomment-3021125236) **typescript-bot** reported the requested performance run results
 * [22 weeks ago](https://github.com/microsoft/TypeScript/pull/61980#issuecomment-3021240617) **typescript-bot** reported that running the top 400 repos with tsc showed everything looked good
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/61980#issuecomment-3618158044) **jakebailey** said "This feels plausible, but I find it surprising that we haven't used this trick elsewhere?"
 * [today](https://github.com/microsoft/TypeScript/pull/61980#issuecomment-3618249468) **Andarist** explained how generic functions with context-sensitive parts leaked due to incorrect argCheckMode propagation causing wrong caching

### [PR microsoft/TypeScript#62283](https://github.com/microsoft/TypeScript/pull/62283) (Closed, `For Uncommitted Bug`)

**Avoid \`silentNeverType\` leaking into generator types inferred based on inner generic calls at \`yield\`s**

*Prevent silentNeverType from leaking into generator return types inferred from inner generic calls at yield points*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/62283#issuecomment-3185710878) **typescript-bot** reported test results comparing main and PR merge, noting an infrastructure failure and otherwise everything looked good
 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/62283#issuecomment-3185847700) **typescript-bot** provided performance run results in a comparison report
 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/62283#issuecomment-3185967418) **typescript-bot** reported that tsc comparisons on the top 400 repos showed no regressions
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62341](https://github.com/microsoft/TypeScript/pull/62341) (Open, `For Backlog Bug`)

**Allow parameters to be contextually\-typed based on contextual rest instantiated using return mapper**

*Allow function parameters to derive types contextually from rest parameters instantiated by return mappers.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#62361](https://github.com/microsoft/TypeScript/pull/62361) (Closed, `For Uncommitted Bug`)

**Make go to definition go to the constraint's properties for object literals in argument positions**

*Enhance the go-to-definition feature to jump from object literals used as arguments directly to their constraint properties.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62361#issuecomment-3617672118) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#62720](https://github.com/microsoft/TypeScript/issues/62720) (Closed, `Bug`, `Help Wanted`, `Domain: Conditional Types`)

**Conditional type inference fails when generic parameter has Readonly\<T\> in function parameter position**

*Conditional type inference fails in TypeScript functions when a generic parameter is declared as Readonly<T>.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62720#issuecomment-3492772882) **RyanCavanaugh** provided an automated analysis of structural vs instantiation-based inference and suggested three workarounds
 * **RyanCavanaugh** added label `Domain: Conditional Types`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62722](https://github.com/microsoft/TypeScript/pull/62722) (Closed, `For Backlog Bug`)

**Widen reverse mapped type properties to fix them being treated as EPC\-valid sources**

*Reverse mapped type properties must be widened to prevent them from being treated as valid EPC sources.*

 * **typescript-bot** added label `For Backlog Bug`
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62722#issuecomment-3492793669) **typescript-bot** provided requested performance run results
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/62722#issuecomment-3492943821) **typescript-bot** reported successful test results for the top 400 repos comparing main and the pull request merge
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62807](https://github.com/microsoft/TypeScript/issues/62807) (Closed, `Duplicate`)

**Switch doesn't narrow type when type isn't a disc union**

*Switch statement on a non-discriminated type does not narrow the default branch to never as expected.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62807#issuecomment-3598074013) **RyanCavanaugh** provided an automatically generated reply with analysis, examples, and relevant FAQs explaining switch-based narrowing and union type behavior in TypeScript
 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62807#issuecomment-3606596218) **aryzing** described annoyance at needing to update switch statements when a discriminated union reduces to a single variant
 * [today](https://github.com/microsoft/TypeScript/issues/62807#issuecomment-3619131711) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62825](https://github.com/microsoft/TypeScript/pull/62825) (Open, `For Backlog Bug`)

**Fixed \`silentNeverType\` leak by propagating it through \`getIndexType\`**

*Propagate silentNeverType through getIndexType to prevent unintended type leakage.*

 * (3 days ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618125419) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618125795) **typescript-bot** posted CI build statuses for test top400, user test this, run dt, and perf test this faster
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618224624) **typescript-bot** notified that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618241558) **typescript-bot** reported test results for user tests indicating one infrastructure failure and otherwise success
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618314267) **typescript-bot** posted the requested performance run results with a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618363282) **jakebailey** said "Big xstate regression it seems"
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618449176) **typescript-bot** reported that tests on the top 400 repos with tsc showed no regressions
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618527360) **jakebailey** said "@typescript-bot pack this"
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618527663) **typescript-bot** posted an automated CI status update with job start and result links
 * [today](https://github.com/microsoft/TypeScript/pull/62825#issuecomment-3618544058) **typescript-bot** provided an installable tgz link and instructions for testing the build via package.json, along with playground and npm module references

### [Issue microsoft/TypeScript#62828](https://github.com/microsoft/TypeScript/issues/62828) (Closed, `Duplicate`)

**non\-null check incorrectly narrows type to "never" if non\-null write happens inside closure**

*TypeScript incorrectly narrows a variable to never when assigning a non-null value inside a callback before checking it.*

 * created by **Dirbaio**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62828#issuecomment-3604704241) **MartinJohns** said "Another duplicate of #9998."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62828#issuecomment-3619131681) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62842](https://github.com/microsoft/TypeScript/issues/62842) (Open, `Suggestion`, `Awaiting More Feedback`)

**Consider deprecating \`\<prefix\>\` type assertions**

*Deprecate legacy `<type>value` assertions in TypeScript in favor of modern `value as type` syntax for improved compatibility and consistency.*

 * created by **robpalme**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [PR microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844) (Closed, `For Milestone Bug`)

**Allow subpath imports that start with \`\#/\`**

*Allow subpath imports starting with '#/' in package.json imports to mirror matching exports entries.*

 * created by **magic-akari**
 * **typescript-bot** added label `For Uncommitted Bug`

