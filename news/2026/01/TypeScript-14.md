# Report for 2026-01-14 (Wednesday, January 14th, 2026)

13 different users commented on 30 different issues.

## Recommended Actions

 * Response Recommended
    * @DayKev asked the maintainers to actively explore changing the stance on .d.ts inputs and consider a new skipLibCheck setting in [microsoft/TypeScript#30511](https://github.com/microsoft/TypeScript/issues/30511#issuecomment-3753166339)
    * @denexapp suggested adding Temporal types to lib.d.ts in [microsoft/TypeScript#60164](https://github.com/microsoft/TypeScript/issues/60164#issuecomment-3753413293)
    * @akaltar asked whether the built-in variance check failure was expected in [microsoft/TypeScript#62973](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3754460457)
    * @shkumbinhasani asked if this is a limitation of infer with intersections or if there's a supported pattern for subtracting intersections in [microsoft/TypeScript#62985](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3750575470)
    * @AFatNiBBa asked if there was any chance of a fix or if it was impossible to fix in [microsoft/TypeScript#62986](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3750374698)

## Activity Summary

### [Issue microsoft/TypeScript#30511](https://github.com/microsoft/TypeScript/issues/30511) (Open, `Suggestion`, `In Discussion`)

**Feature Request: allow exclusion of node\_modules when skipLibCheck is false**

*Add an option to exclude node_modules from library type checking without enabling skipLibCheck.*

 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/30511#issuecomment-2692391186) **DanKaplanSES** preferred extending skipLibCheck to accept glob patterns and provided a use case about conflicting types in testcafe-hammerhead dependency
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/30511#issuecomment-3057658817) **ernestostifano** provided a script that reports all TypeScript issues with skipLibCheck disabled while excluding node_modules in projects using incremental builds
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/30511#issuecomment-3168049450) **alexsch01** said "Any update on this?"
 * [today](https://github.com/microsoft/TypeScript/issues/30511#issuecomment-3753166339) **DayKev** urged the team to actively explore changing the current stance on .d.ts files and supported adding a 'skipLibCheck: external' option
 * [later](https://github.com/microsoft/TypeScript/issues/30511#issuecomment-3755454722) **skarab42** pointed out that .d.ts files are often hand-authored via DefinitelyTyped and that treating them as outputs only ignores documented workflows and causes skipLibCheck DX issues

### [Issue microsoft/TypeScript#51155](https://github.com/microsoft/TypeScript/issues/51155) (Open, `Suggestion`, `Needs Proposal`, `Domain: LS: Auto-import`)

**Auto\-import priority rules**

*Allow configuring VSCode auto-imports to prioritize local, aliased, and nearby modules over external or internal ones.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/51155#issuecomment-3164068872) **akodkod** said "+1 for this issue"
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/51155#issuecomment-3234102430) **dallenbaldwin** upvoted the issue, described difficulties trusting the add missing imports feature when using a wrapped function, and suggested auto-importing everything and removing duplicates as a workaround
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/51155#issuecomment-3237144133) **adrian-gierakowski** said "Another issue I always face is auto import from src/ instead of dist/ in a monorepo where stuff is import d directly from files instead of the index "
 * [today](https://github.com/microsoft/TypeScript/issues/51155#issuecomment-3752877055) **jpike88** expressed disappointment that the missing feature blocked TSGO and stressed its critical need for hoisting internal imports to improve TypeScript ergonomics

### [Issue microsoft/TypeScript#60164](https://github.com/microsoft/TypeScript/issues/60164) (Open, `Domain: lib.d.ts`, **RyanCavanaugh**)

**Add Temporal \(Stage 3\) types**

*Add TypeScript definitions for the Stage 3 Temporal API, including Temporal.Now, Instant, ZonedDateTime, PlainDate, and related types.*

 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/60164#issuecomment-2834408455) **MeesterDev** said "FYI Firefox is shipping Temporal in version 139, planned to be released at the end of May."
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/60164#issuecomment-3418731911) **TomasHubelbauer** noted that Firefox shipped Temporal support months ago and suggested adding types unless cross-browser support is required
 * [later](https://github.com/microsoft/TypeScript/issues/60164#issuecomment-3753413293) **denexapp** said "Chrome 144 added support for Temporal, released on Jan 14. It will be great to see the types in lib.d.ts"

### [Issue microsoft/TypeScript#62333](https://github.com/microsoft/TypeScript/issues/62333) (Open, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **DanielRosenwasser**)

**Enable \`\-\-strict\` by default**

*Enable TypeScript's --strict flag by default in v6.0 to make strict type-checking standard unless disabled.*

 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/62333#issuecomment-3279608356) **phaux** suggested enabling noUncheckedIndexedAccess in strict mode and exactOptionalPropertyTypes, while noting the former might be controversial
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/62333#issuecomment-3281813995) **dlannoye** suggested defaulting strict to true and explicitly setting all strict-related properties to their strict mode values to enforce explicit overrides
 * **typescript-bot** added label `Fix Available`
 * (today) **DanielRosenwasser** closed the issue
 * (today) **jakebailey** reopened the issue

### [Issue microsoft/TypeScript#62966](https://github.com/microsoft/TypeScript/issues/62966) (Open, `Bug`, `Help Wanted`, `Domain: check: Type Circularity`)

**Regression: RangeError: Maximum call stack size exceeded in type instantiation with recursive types and intersections**

*Regression in TypeScript 5.9 causes infinite recursion and a RangeError stack overflow when instantiating recursive intersection types.*

 * (6 days ago) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Type Circularity`

### [PR microsoft/TypeScript#62973](https://github.com/microsoft/TypeScript/pull/62973) (Open, `For Uncommitted Bug`)

**Add explicit type variance specifiers to Promise, Map, Set**

*Add explicit type variance specifiers to Promise, Map, and Set to potentially improve type checking performance.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740810752) **typescript-bot** reported user test results comparing main and merge, noted infrastructure failures and new type errors, and asked to have a look
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740901124) **typescript-bot** posted the performance run results comparing baseline to PR for tsc
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740953606) **typescript-bot** reported comparative build results for the top 400 repos between main and the PR, noted a build error in microsoft/playwright, and requested a review
 * [later](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3754460457) **akaltar** asked whether the built-in variance check failure on a simple Map type was expected or misinterpreted and whether a different context would change the results

### [Issue microsoft/TypeScript#62974](https://github.com/microsoft/TypeScript/issues/62974) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: TypeError: Cannot read properties of undefined \(reading 'flags'\) in isFreshLiteralType during recursive tuple expansion with unresolved identifiers**

*TypeScript compiler crashes with a TypeError reading 'flags' in isFreshLiteralType during recursive tuple expansion with unresolved identifiers*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62974#issuecomment-3740665614) **RyanCavanaugh** said "Repros in TS7 as well"
 * (2 days ago) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Crashes`

### [PR microsoft/TypeScript#62983](https://github.com/microsoft/TypeScript/pull/62983) (Open, `For Backlog Bug`)

**Fixed issues in relater related to tuples with variadic elements**

*Relater now correctly handles comparisons of tuple types containing variadic elements.*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62983#issuecomment-3750949026) **RyanCavanaugh** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/62983#issuecomment-3750949345) **typescript-bot** reported the status and results of automated build jobs
 * [today](https://github.com/microsoft/TypeScript/pull/62983#issuecomment-3751036209) **typescript-bot** notified that the DT test results were ready and unchanged and provided a link to the logs
 * [today](https://github.com/microsoft/TypeScript/pull/62983#issuecomment-3751061626) **typescript-bot** reported infrastructure failures and confirmed that everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/62983#issuecomment-3751187939) **typescript-bot** posted performance run results in a detailed comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/62983#issuecomment-3751301204) **typescript-bot** reported that comparison of top 400 repos build between main and the pull request merge showed everything looked good

### [Issue microsoft/TypeScript#62985](https://github.com/microsoft/TypeScript/issues/62985) (Closed, `Not a Defect`)

**Cannot extract base type from branded intersection**

*Request for a TypeScript mechanism to remove a branded intersection from a type and recover its base type.*

 * created by **shkumbinhasani**
 * [today](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3749270968) **mkantor** suggested using Error instead of any and noted uncertainty why any doesn't work
 * [today](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3750575470) **shkumbinhasani** observed that StripThrows failed to strip Throws<APIError> when APIError has an instance field and asked whether this is due to infer limitations with intersections or if a supported pattern exists
 * [today](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3750926737) **RyanCavanaugh** explained that reverse inference from an intersection is not well-defined in a structural type system and provided an alternative implementation using Omit2 and StripThrows with code examples
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3750977452) **jcalz** noted similarity to issues #54213 and #57918 and suggested filing a feature request for branded-primitive support in Omit instead of treating it as a bug

### [Issue microsoft/TypeScript#62986](https://github.com/microsoft/TypeScript/issues/62986) (Closed, `Duplicate`)

**Only the last overload of a function is considered while inferring**

*Inference for overloaded functions only uses the last signature when inferring return or parameter types instead of uniting all overloads*

 * created by **AFatNiBBa**
 * [today](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3750125156) **MartinJohns** explained that the behavior was working as intended and documented in the TypeScript handbook with a link to conditional types
 * [today](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3750374698) **AFatNiBBa** asked if there was any chance of it getting fixed or if it was impossible to fix
 * [today](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3750434692) **MartinJohns** explained that the issue was long-known, stemmed from overload resolution, required new syntax, and noted that a solution was unlikely soon
 * [today](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3750878939) **jcalz** said "duplicate of #29732, #56430, #56829, and others."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#62987](https://github.com/microsoft/TypeScript/pull/62987) (Closed, `Author: Team`, `For Milestone Bug`, **DanielRosenwasser**)

**Correctly split line endings for \`// @testOption: value\` parsing**

*Improve test harness line splitting to handle mixed CRLF and LF endings and preserve inline option comments.*

 * created by **DanielRosenwasser**
 * (today) **typescript-bot** added labels `Author: Team`, `For Milestone Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/62987#issuecomment-3752247390) **DanielRosenwasser** showed that Corsa defines lineDelimiter using a regex matching optional carriage return and newline
 * [today](https://github.com/microsoft/TypeScript/pull/62987#issuecomment-3752264159) **DanielRosenwasser** guessed it was intentional that CRLF were normalized into LF but not other line endings
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#62988](https://github.com/microsoft/TypeScript/issues/62988) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: Performance`)

**Use LazyBarrel to improve IDE performance**

*Add an experimental LazyBarrel optimization to the TypeScript Language Server to improve IDE performance with barrel files*

 * created by **mgfalzon**
 * [today](https://github.com/microsoft/TypeScript/issues/62988#issuecomment-3753100806) **DanielRosenwasser** explained that full-program loading is necessary for builds and language service features, described optimizations for v7.0, and expressed willingness to consider future enhancements
 * [later](https://github.com/microsoft/TypeScript/issues/62988#issuecomment-3755403191) **mgfalzon** thanked the maintainer and reported that de-barreling led to 27% and 30% reductions in type highlight duration at Atlassian, and said they will de-barrel their component library after migrating to tsgo

### [PR microsoft/TypeScript#62989](https://github.com/microsoft/TypeScript/pull/62989) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Prepare tests for \`\-\-noImplicitAny\`**

*A script prepends // @strict: false to tests whose error outputs changed when enabling default --noImplicitAny.*

 * created by **DanielRosenwasser**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/pull/62989#issuecomment-3753134272) **DanielRosenwasser** said "This history is already a nightmare..."

