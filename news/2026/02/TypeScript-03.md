# Report for 2026-02-03 (Tuesday, February 3rd, 2026)

12 different users commented on 87 different issues.

## Recommended Actions

 * Response Recommended
    * @aweebit provided a workaround for the issue in [microsoft/TypeScript#39600](https://github.com/microsoft/TypeScript/issues/39600#issuecomment-3842737535)
    * @Ayoub-glitsh asked to be assigned the issue to start working on it in [microsoft/TypeScript#63082](https://github.com/microsoft/TypeScript/issues/63082#issuecomment-3842777187)

## Activity Summary

### [Issue microsoft/TypeScript#39600](https://github.com/microsoft/TypeScript/issues/39600) (Open, `Bug`, `Domain: check: Type Inference`)

**\`void\` parameter type produced from generic inference doesn't allow skipping as argument**

*Generic void parameter types incorrectly require arguments, unlike explicit void parameters which can be omitted.*

 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/39600#issuecomment-673996025) **maxim-grishaev** said "@jcalz Yes, to me it looks like the same issue"
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/39600#issuecomment-2062326197) **kalkronline** provided a minimal example demonstrating that calling comp_ck<void>() errors while void_ck() does not
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [today](https://github.com/microsoft/TypeScript/issues/39600#issuecomment-3842737535) **aweebit** provided a minimal reproducible example of the TypeScript issue and suggested a workaround using conditional rest parameters

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation List**

*Proposed deprecations of outdated TypeScript 6.0 compiler options, with full removal planned for version 7.0.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3745453163) **RyanCavanaugh** explained that useDefineForClassFields would remain supported in v6/v7 due to widespread dependencies and migration difficulty
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3764353180) **danilofuchs** asked whether noUncheckedIndexAccess would be enabled by default in strict mode
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3774124466) **RyanCavanaugh** stated that noUncheckedIndexAccess would not be enabled by default in strict mode
 * [today](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3843337972) **RyanCavanaugh** said "Edited to add target: es5 and downlevelIteration (entirely) being deprecated."

### [Issue microsoft/TypeScript#56497](https://github.com/microsoft/TypeScript/issues/56497) (Open, `Suggestion`, `Help Wanted`, `Experience Enhancement`, `Effort: Casual`)

**\[Rename symbol command\] Remove unnecessary named import**

*The Rename Symbol command in VS Code produces redundant import aliases like bar as bar instead of simplifying imports.*

 * (2.1 years ago) **andrewbranch** added labels `Experience Enhancement`, `Effort: Casual`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/56497#issuecomment-3843731310) **pabloosabaterr** said "Hi! can I get to work on this ? seems like the last time approached was on 25 Feb 2025 and the pr doesnt contain an actual fix."
 * [today](https://github.com/microsoft/TypeScript/issues/56497#issuecomment-3843793702) **pabloosabaterr** read contributing guidelines, noted that development is winding down and code changes should target typescript-go, and declined to participate

### [Issue microsoft/TypeScript#61648](https://github.com/microsoft/TypeScript/issues/61648) (Closed, `Planning`)

**TypeScript 5\.9 Iteration Plan**

*Outline of TypeScript 5.9 release timeline and planned compiler, editor, and performance enhancements.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/61648#issuecomment-3577315757) **ghiscoding** explained TypeScript's release numbering and asked when 6.0 would be released and if it would include major breaking changes
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/61648#issuecomment-3577471172) **RyanCavanaugh** said "Stay tuned for a blog post (probably in the next week or so), but 6.0 will be later than the usual cadence. The issues you linked outline all our planned breaking changes for that release."
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/61648#issuecomment-3577717045) **jogibear9988** said "you can also look here: https://github.com/microsoft/TypeScript/issues/62785"
 * [today](https://github.com/microsoft/TypeScript/issues/61648#issuecomment-3843924696) **DanielRosenwasser** said "The 6.0 iteration plan was just posted over at https://github.com/microsoft/TypeScript/issues/63085."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62160](https://github.com/microsoft/TypeScript/pull/62160) (Closed, **weswigham**)

**Add format to update baselines/fix lints task**

*Add a formatting task to automatically update baselines and fix trivially auto-fixable lint issues.*

 * created by **weswigham**
 * (26 weeks ago) **weswigham** closed the issue
 * **typescript-bot** assigned to **weswigham**

### [PR microsoft/TypeScript#62162](https://github.com/microsoft/TypeScript/pull/62162) (Closed, **DanielRosenwasser**)

**Bump version to 6\.0**

*Update the application’s version number to 6.0.*

 * created by **DanielRosenwasser**
 * [26 weeks ago](https://github.com/microsoft/TypeScript/pull/62162#issuecomment-3141554535) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * (26 weeks ago) **DanielRosenwasser** closed the issue
 * **typescript-bot** assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript#62163](https://github.com/microsoft/TypeScript/pull/62163) (Closed, **weswigham**)

**Intentionally regress one buggy declaration output to an older version**

*Temporarily revert the buggy #field type member output in TypeScript 5.9 to prior syntactically valid internal symbol naming.*

 * created by **weswigham**
 * (26 weeks ago) **weswigham** closed the issue
 * **typescript-bot** assigned to **weswigham**

### [PR microsoft/TypeScript#62191](https://github.com/microsoft/TypeScript/pull/62191) (Closed, **johnfav03**)

**added john favret to pr\_owners\.txt**

*Add John Favret to the list of PR owners in pr_owners.txt.*

 * created by **johnfav03**
 * (26 weeks ago) **jakebailey** closed the issue
 * **typescript-bot** assigned to **johnfav03**

### [Issue microsoft/TypeScript#62333](https://github.com/microsoft/TypeScript/issues/62333) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **DanielRosenwasser**)

**Enable \`\-\-strict\` by default**

*Enable TypeScript's --strict flag by default in v6.0 to make strict type-checking standard unless disabled.*

 * **typescript-bot** added label `Fix Available`
 * (2 weeks ago) **DanielRosenwasser** closed the issue
 * (2 weeks ago) **jakebailey** reopened the issue
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62556](https://github.com/microsoft/TypeScript/pull/62556) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] tsgo compat changes**

*Introduce a boolean toggle to enable tsgo compatibility updates combining changes from PRs 61399 and 61420.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3378301100) **jakebailey** said "@typescript-bot test top800"
 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3378301362) **typescript-bot** reported CI jobs started and provided status table
 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3378742523) **typescript-bot** reported build comparison results for the top 800 repositories between main and the pull request, highlighting several build failures
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842702677) **jakebailey** requested the TypeScript bot to test and pack
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842703045) **typescript-bot** posted CI job statuses with links to started builds and results
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842725481) **typescript-bot** provided an installable tgz link and usage instructions for testing the build via npm, playground, and npm module
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842806060) **typescript-bot** ran user tests with tsc comparing main and pull request merge, reported one package install failure, one git clone failure, and new type errors in lodash and npmlog
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842806140) **typescript-bot** posted TypeScript error output from running the user tests suite on webpack
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842870941) **typescript-bot** reported DT test results indicating errors in json-logic-js, trellopowerup, and codemirror packages
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842999875) **typescript-bot** provided the perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3843105177) **typescript-bot** reported tsc build comparison results for the top 400 repos between `main` and the PR merge, noting interesting changes and build failures in several projects

### [PR microsoft/TypeScript#62730](https://github.com/microsoft/TypeScript/pull/62730) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**DOM update**

*Update the DOM to incorporate numerous recent changes.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639794378) **typescript-bot** reported build results for top 400 repos and highlighted new TS2345 errors in microsoft/vscode comparing main and the pull request
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3643825924) **jakebailey** said "Hm, I guess the generated Navigator is missing a few things"
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3648441269) **Renegade334** identified that the @types/dom-navigation package clashed with the new Navigation API
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843025165) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843025458) **typescript-bot** reported CI job statuses and results for the pull request
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843106510) **typescript-bot** reported that user tests comparison on main and the pull request merge had two infrastructure failures but otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843117883) **typescript-bot** reported that the DT tests results were ready and showed compile errors in the deno package due to identifier conflicts and type mismatches
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843277985) **jakebailey** said "The GPU types get bigger, and so more conflicts..."
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843279804) **typescript-bot** posted the requested perf run results comparing baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843366710) **typescript-bot** reported that the top 400 repos’ tsc build results comparing main and the PR looked good

### [Issue microsoft/TypeScript#62785](https://github.com/microsoft/TypeScript/issues/62785) (Closed, `Question`)

**Iteration Plan for Typescript 5\.10/6\.0 ?**

*Request for an iteration plan specifying timeline and feature roadmap for the upcoming TypeScript 5.10 and 6.0 releases.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/62785#issuecomment-3560139353) **DanielRosenwasser** apologized for the missing iteration plan issue and outlined the roadmap for versions 6.0 and 7.0, including release timelines and preview options
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/62785#issuecomment-3567340001) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (10 weeks ago) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62785#issuecomment-3844378561) **DanielRosenwasser** said "See https://github.com/microsoft/TypeScript/issues/63085"

### [Issue microsoft/TypeScript#62960](https://github.com/microsoft/TypeScript/issues/62960) (Open, `Needs More Info`)

**Initializing tsconfig\.json hangs**

*VS Code hangs indefinitely initializing tsconfig.json for Vue projects on network shares, disabling IntelliSense and error reporting.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3756234243) **uli-a** described debugging the forEachAncestorDirectory function and asked if the loop should stop at the workspace or network share root to avoid slow traversal
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3757316720) **uli-a** revealed that directoryProbablyExists in loadModuleFromImmediateNodeModulesDirectory was slow, questioned whether always searching outside the workspace should be configurable, and noted a workaround using an empty network share
 * [today](https://github.com/microsoft/TypeScript/issues/62960#issuecomment-3844511912) **RyanCavanaugh** explained module resolution behavior and requested a reproduction to confirm

### [Issue microsoft/TypeScript#62963](https://github.com/microsoft/TypeScript/issues/62963) (Open, `Meta-Issue`)

**Transition to 6\.0 Maintenance Mode**

*TypeScript 6.0 is entering maintenance mode with only critical fixes, deprecations, and compatibility changes accepted to accelerate the transition to the Go-based 7.0 release.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3723323514) **puppy0cam** said "If we amended our PRs to take out code changes but keep the test(s) created, would such a PR be accepted?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3724470262) **RyanCavanaugh** replied that test-only PRs would be accepted after 7.0 but currently no due to large ongoing PRs causing merge conflicts
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3787149661) **KnorpelSenf** asked whether regressions from 4.7 to 4.8 and imported bugs would be fixed after the 7.0 release
 * [today](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3842750039) **RyanCavanaugh** said "@KnorpelSenf yep!"

### [PR microsoft/TypeScript#62973](https://github.com/microsoft/TypeScript/pull/62973) (Closed, `For Uncommitted Bug`)

**Add explicit type variance specifiers to Promise, Map, Set**

*Add explicit type variance specifiers to Promise, Map, and Set to potentially improve type checking performance.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740901124) **typescript-bot** posted the performance run results comparing baseline to PR for tsc
 * [3 weeks ago](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3740953606) **typescript-bot** reported comparative build results for the top 400 repos between main and the PR, noted a build error in microsoft/playwright, and requested a review
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/62973#issuecomment-3754460457) **akaltar** asked whether the built-in variance check failure on a simple Map type was expected or misinterpreted and whether a different context would change the results
 * (later) **akaltar** closed the issue

### [Issue microsoft/TypeScript#63004](https://github.com/microsoft/TypeScript/issues/63004) (Open, `Bug`, `Domain: check: Control Flow`)

**Explicit \`never\` return type in \`catch\` block & condition in \`finally\` marks the whole \`finally\` block as unreachable**

*TypeScript incorrectly flags a conditional finally block as unreachable when a catch handler calls a function declared to return never.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63004#issuecomment-3774685680) **RyanCavanaugh** generated an automated response listing similar issues
 * (1 week ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Control Flow`

### [Issue microsoft/TypeScript#63019](https://github.com/microsoft/TypeScript/issues/63019) (Open, `Help Wanted`, `Domain: check: Type Inference`, `Possible Improvement`)

**Regression: Generic function returning union of tuples is not assignable to identical type since v4\.2**

*TypeScript 4.2 regression incorrectly widens generics causing identical generic functions returning unions of tuples to be unassignable.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63019#issuecomment-3774685877) **RyanCavanaugh** provided an automated analysis listing similar issues
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63019#issuecomment-3774797524) **mkantor** disputed the previous AI explanation and demonstrated that an example factoring out the return type into a type alias also has no type errors
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63019#issuecomment-3775290136) **Andarist** explained that inference matches type aliases and theorized that inferToMultipleTypes fails to align discriminated unions, causing incorrect inference from R | undefined to R
 * (today) **RyanCavanaugh** added labels `Help Wanted`, `Possible Improvement`, `Domain: check: Type Inference`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63030](https://github.com/microsoft/TypeScript/pull/63030) (Closed, `Breaking Change`, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Deprecate alwaysStrict: false in TypeScript 6\.0**

*TypeScript 6.0 deprecates alwaysStrict=false, emitting warnings and requiring ignoreDeprecations to silence them ahead of its removal in 7.0.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3791464828) **jakebailey** noted that the PR would not detect the problem because alwaysStrict can be disabled by setting strict to false and suggested forcing alwaysStrict when strict is false
 * **jakebailey** added label `Breaking Change`
 * **DanielRosenwasser** added to milestone `TypeScript 6.0.0`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63033](https://github.com/microsoft/TypeScript/issues/63033) (Open, `Bug`, `Domain: LS: Auto-import`, `Corsa`)

**Autocomplete incorrectly suggests transitive files from monorepo package**

*Autocomplete incorrectly suggests unexported internal files from a monorepo package despite its exports configuration.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3787420587) **ericnorris** verified that the bug was not present in TS 7, replicated the behaviour with a fourslash test, suggested adding a test to prevent regression, and asked if a separate issue should be filed in the typescript-go repository
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3795824983) **ericnorris** reproduced the issue in TS 7, linked it to the related issue, and asked if a fix for TS 6 would be accepted
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3806478101) **RyanCavanaugh** replied that a fix for TS 6 would not be accepted and referenced issue #62963
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: LS: Auto-import`
 * [today](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3842746319) **RyanCavanaugh** said "Yell at me if I accidently auto-close this with a script"
 * **RyanCavanaugh** added label `Corsa`

### [Issue microsoft/TypeScript#63039](https://github.com/microsoft/TypeScript/issues/63039) (Open, `Bug`, `Domain: This-Typing`)

**Regression of \`this is\` type predicate for intersection of unions from 4\.7 to 4\.8**

*TypeScript 4.8 regression prevents this is type predicates from correctly narrowing intersection of union types that worked in 4.7*

 * created by **KnorpelSenf**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63039#issuecomment-3792416694) **JosXa** said "Hey OpenCode, can you take a stab at this?"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63039#issuecomment-3792579763) **JosXa** investigated and identified a regression in TypeScript 4.8 where type predicate narrowing on unions with conflicting property types produced a never intersection
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: This-Typing`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63040](https://github.com/microsoft/TypeScript/issues/63040) (Open, `Bug`, `Domain: check: Type Circularity`, **ahejlsberg**)

**RangeError: Maximum call stack size exceeded in getTypeFromTypeNode when resolving recursive tuple rest with intersection**

*TypeScript crashes with a call stack overflow when resolving a recursive tuple rest type intersected with boolean.*

 * created by **na7ure-a**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63040#issuecomment-3788854014) **Andarist** said "It seems to date back to the OG: https://github.com/microsoft/TypeScript/pull/40002"
 * [today](https://github.com/microsoft/TypeScript/issues/63040#issuecomment-3842802361) **RyanCavanaugh** noted a syntax error in the original post and provided corrected code that crashes in TS7 as well
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: check: Type Circularity`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63050](https://github.com/microsoft/TypeScript/issues/63050) (Open, `Help Wanted`, `Domain: Error Messages`, `Fix Available`, `Possible Improvement`)

**Double error message when referencing variable of type union of string literals from ambient declaration**

*TypeScript 4.0.5 duplicates the same error message when assigning an ambient string-literal union to a number.*

 * (4 days ago) **RyanCavanaugh** set milestone to `Dormant`, and removed from milestone `Backlog`
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: Error Messages`

### [Issue microsoft/TypeScript#63051](https://github.com/microsoft/TypeScript/issues/63051) (Open, `Bug`, `Domain: check: Type Inference`, `Corsa`, **ahejlsberg**)

**tsgo fails to report TS2769 for mutually\-exclusive object overloads**

*tsgo does not report TS2769 for mutually exclusive object overloads while tsc correctly flags the error.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63051#issuecomment-3796895410) **jcalz** said "Question for TS team... is https://tsgo.sxzz.dev is an acceptable playground for tsgo? "
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63051#issuecomment-3796914886) **r253hmdryou** filed a duplicate issue in microsoft/typescript-go to track tsgo-specific behavior
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63051#issuecomment-3806620084) **RyanCavanaugh** asked if tsgo.sxzz.dev was an acceptable playground for tsgo
 * (today) **RyanCavanaugh** added labels `Bug`, `Corsa`, `Domain: check: Type Inference`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63059](https://github.com/microsoft/TypeScript/issues/63059) (Open, `Suggestion`, `Awaiting More Feedback`)

**Narrow object property indexed by another object's property of unique symbol type \(like \`Symbol\.iterator\`\)**

*Allow TypeScript’s type narrowing to work for bracket notation property access when the key is a unique symbol property of an object*

 * created by **jcalz**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63061](https://github.com/microsoft/TypeScript/issues/63061) (Closed, `Not a Defect`)

**\`export type\` vs \`export { type }\` with augmentations**

*export { type } re-exports do not allow module augmentations to access types, unlike export type*

 * created by **skirtles-code**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3817254000) **mkantor** said "I just tested typescript-go and the behavior is the same there (perhaps this issue should be filed in that repository; see #62827)."
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3842786736) **RyanCavanaugh** explained reasons for allowing a local type to be exported by name without reuse and that module rules include only the lexical scope of explicitly exported names, consistent with file-level behavior

### [Issue microsoft/TypeScript#63065](https://github.com/microsoft/TypeScript/issues/63065) (Closed, `Question`)

**Is \`class A extends \(B\<T\>\)\<T\> {}\` valid code?**

*Investigating whether the unusual generic subclass syntax 'class A extends (B<T>)<T> {}' is valid TypeScript code.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3838333823) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (yesterday) **typescript-bot** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3838572718) **bradzacher** said "@typescript-bot we were waiting for the TS team to respond..."
 * [today](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3843434813) **RyanCavanaugh** questioned the action items and asked for clarification on the ambiguity around parentheses in extends clauses and the semantic validity of certain generic expressions

### [Issue microsoft/TypeScript#63069](https://github.com/microsoft/TypeScript/issues/63069) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`)

**Make standard library types more polyfills‑friendly**

*Propose enhancing TypeScript’s standard library declarations with interfaces, readonly properties, and conditional types to support polyfills.*

 * created by **slowcheetah**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `In Discussion`, `Domain: lib.d.ts`

### [PR microsoft/TypeScript#63071](https://github.com/microsoft/TypeScript/pull/63071) (Closed, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Deprecate downlevelIteration**

*Deprecate the downlevelIteration compiler flag in TypeScript 7.0 since it’s redundant for ES2015+ targets.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3826337952) **typescript-bot** reported build comparison results for top 400 repos between main and the PR and highlighted deprecation errors in three projects
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3826585042) **DanielRosenwasser** wondered if deprecating was worthwhile and pointed out that the issue stemmed from packages compiling to ES5 rather than the current project
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3826592442) **jakebailey** noted that deprecated options already behaved this way, that setting it to null would not help when TS 7.0 arrives, and that the option felt pointless
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3843176589) **jakebailey** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3843176860) **typescript-bot** started test top800 build job and provided status and results links
 * **jakebailey** added label `Breaking Change`
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3843827126) **typescript-bot** reported the results of running the top 800 repositories with tsc comparing `main` and the pull request merge and noted an interesting change

### [Issue microsoft/TypeScript#63080](https://github.com/microsoft/TypeScript/issues/63080) (Closed, `Needs More Info`)

**\[Bug\]: Intersection of imported conditional types becomes overly permissive and accepts invalid properties**

*Intersections of imported type aliases in TypeScript lose strictness and accept invalid properties, unlike same-file intersections.*

 * created by **Uanela**
 * [today](https://github.com/microsoft/TypeScript/issues/63080#issuecomment-3839918479) **MartinJohns** pointed out that TypeScript allows additional properties and that excess property checks are a linter feature, and suggested the issue stems from using a weak type
 * [today](https://github.com/microsoft/TypeScript/issues/63080#issuecomment-3842305750) **jcalz** noted absence of conditional types in the example code and marked cross-union-member excess property checking as a duplicate of issue #20863
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63080#issuecomment-3842650659) **RyanCavanaugh** noted no error in the same-file example, observed the same behavior on the command line, and asked for clarification
 * [today](https://github.com/microsoft/TypeScript/issues/63080#issuecomment-3843647548) **Uanela** found the issue was related to complex generics he was building
 * (today) **Uanela** closed the issue
 * (today) **Uanela** reopened the issue
 * (today) **Uanela** closed the issue

### [PR microsoft/TypeScript#63081](https://github.com/microsoft/TypeScript/pull/63081) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Hide omitted expression types in type baselines**

*Move suppression of omitted-expression types from tsgo-port to main to align type baselines with tsgo behavior.*

 * (yesterday) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63082](https://github.com/microsoft/TypeScript/issues/63082) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add support for OSC8 hyperlinks in TTY output**

*Support OSC8 hyperlinks in TypeScript build output to enable reliable clickable file paths in terminal emulators*

 * created by **matthieusieben**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63082#issuecomment-3842777187) **Ayoub-glitsh** offered to help and requested assignment to investigate and propose an implementation

### [Issue microsoft/TypeScript#63083](https://github.com/microsoft/TypeScript/issues/63083) (Closed)

**Fixs**

*A vague request to “Fix” the issue with no further details provided.*

 * created by **gitme1-ym**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63084](https://github.com/microsoft/TypeScript/pull/63084) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add \-\-stableTypeOrdering for TS7 ordering compat**

*Add a hidden --stableTypeOrdering flag that enables TS7’s deterministic type, symbol, and node ordering algorithm for tsgo-port compatibility.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3843701996) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3843702728) **jakebailey** checked that the flag was disabled and requested a faster perf test
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3843703025) **typescript-bot** provided initial CI build status update
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3843939535) **typescript-bot** posted the results of the requested performance run

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Planning`
 * [later](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3847560316) **petamoriken** said "I've submitted a PR to add the ES2025 target (#63046), but will this not be included in TypeScript 6.0?"
 * [later](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3848220188) **jakebailey** said "You can lump that in with lib.d.ts updates."

### [PR microsoft/TypeScript#63086](https://github.com/microsoft/TypeScript/pull/63086) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix some tests that should have stayed ES5**

*Several tests were inadvertently converted to newer JavaScript syntax and need to be reverted to ES5.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63087](https://github.com/microsoft/TypeScript/pull/63087) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **DanielRosenwasser**)

**Switch the default of \`\-\-strict\` to \`true\`**

*Change the default value of the --strict flag to true to enable strict checking by default.*

 * created by **DanielRosenwasser**
 * (today) **typescript-bot** added labels `Author: Team`, `For Milestone Bug`, and assigned to **DanielRosenwasser**
 * **jakebailey** added label `Breaking Change`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63088](https://github.com/microsoft/TypeScript/issues/63088) (Open)

**Function property in union does not get parameter type inferred from result of type narrowing**

*TypeScript does not infer a function property’s parameter type from narrowed union discriminants, defaulting to any.*

 * created by **dyantako**

### [PR microsoft/TypeScript#63089](https://github.com/microsoft/TypeScript/pull/63089) (Closed, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Deprecate \`alwaysStrict: false\`**

*Deprecate alwaysStrict: false in TypeScript to enforce strict mode by default.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/63089#issuecomment-3845658482) **jakebailey** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript/pull/63089#issuecomment-3845658727) **typescript-bot** announced that the test top800 job started and provided status and results links
 * [later](https://github.com/microsoft/TypeScript/pull/63089#issuecomment-3846213662) **typescript-bot** reported build comparison results between main and the pull request for the top 800 repositories and flagged an interesting change

### [Issue microsoft/TypeScript#63090](https://github.com/microsoft/TypeScript/issues/63090) (Open)

**Crash: RangeError: Maximum call stack size exceeded during type serialization of recursive distributive mapped types**

*Recursive distributive mapped types trigger a compiler stack overflow error in TypeScript 5.7.3 and later.*

 * created by **na7ure-a**

### [Issue microsoft/TypeScript#63091](https://github.com/microsoft/TypeScript/issues/63091) (Closed, `Fix Available`)

**Crash: RangeError: Maximum call stack size exceeded when destructuring undefined/unknown as identifiers in parameter list**

*TypeScript crashes with a maximum call stack error when destructuring undefined and unknown in function parameters under strict mode.*

 * created by **na7ure-a**

### [Issue microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092) (Open)

**Crash: RangeError: Maximum call stack size exceeded in isReachableFlowNodeWorker with complex for loop headers**

*TypeScript's compiler crashes with a maximum call stack size exceeded error when analyzing reachability in complex for loop headers.*

 * created by **na7ure-a**

### [Issue microsoft/TypeScript#63093](https://github.com/microsoft/TypeScript/issues/63093) (Closed, `Fix Available`)

**Crash: RangeError: Maximum call stack size exceeded in checkExpression when resolving property access on parenthesized type assertions with generic\-like syntax**

*TypeScript compiler overflows the call stack when resolving property access on a parenthesized generic-like type assertion in strict mode.*

 * created by **na7ure-a**

### [Issue microsoft/TypeScript#63094](https://github.com/microsoft/TypeScript/issues/63094) (Open)

**Crash: Debug Failure\. False expression in getArgumentArityError when resolving overloaded decorators with \-\-experimentalDecorators**

*TypeScript crashes with a 'Debug Failure. False expression' error in getArgumentArityError when resolving overloaded decorators under --experimentalDecorators.*

 * created by **na7ure-a**

