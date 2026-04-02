# Report for 2026-01-30 (Friday, January 30th, 2026)

12 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @fisker asked for clarification on the desired error message in [microsoft/TypeScript#63065](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3827912099)

## Activity Summary

### [Issue microsoft/TypeScript#62196](https://github.com/microsoft/TypeScript/issues/62196) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **jakebailey**)

**Deprecate \`\-\-target es5\`, make lowest target \`es2015\`**

*Deprecate --target es5 in TypeScript 6.0, raise the minimum target to ES2015, and update library inclusion and downlevel iteration handling.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3795468983) **EliasVal** mentioned that 96.23% of internet users support ES6 and that maintaining ES5 support for the remaining 3% is not worth the cost
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3807001264) **guilhermesimoes** criticized the suggestion that PS4 browser usage is rare as ignorant, noted apps on PS4/PS5 have millions of users in Europe and Africa but declined to share exact figures, and deferred the ES5 support cost decision to the TypeScript team
 * **typescript-bot** added label `Fix Available`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62198](https://github.com/microsoft/TypeScript/issues/62198) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **jakebailey**)

**Change default \`\-\-target\` to latest ECMAScript version**

*Change TypeScript’s default target from ES5 to the latest ECMAScript version to promote modern runtime support.*

 * (1 week ago) **RyanCavanaugh** assigned to **jakebailey**, and unassigned **RyanCavanaugh**
 * **typescript-bot** added label `Fix Available`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62338](https://github.com/microsoft/TypeScript/pull/62338) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Deprecate \`\-\-moduleResolution node10\`**

*Deprecate --moduleResolution node10, change default commonjs resolution to bundler, update tests, and fix module specifier completions bug.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62338#issuecomment-3422605018) **andrewbranch** said "@typescript-bot cherry-pick this to tsgo-port"
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62338#issuecomment-3422605624) **typescript-bot** reported that a cherry-pick job to tsgo-port had started and provided build status links
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62338#issuecomment-3422622900) **typescript-bot** said "Hey, @andrewbranch! I've created #62637 for you."
 * **jakebailey** added label `Breaking Change`

### [PR microsoft/TypeScript#62391](https://github.com/microsoft/TypeScript/pull/62391) (Closed, `Breaking Change`, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Switch \`libReplacement\` to \`false\` by default and fix condition logic**

*Change libReplacement default to false and adjust condition logic and test baselines to make lib replacement opt-in.*

 * [20 weeks ago](https://github.com/microsoft/TypeScript/pull/62391#issuecomment-3276843047) **typescript-bot** provided the performance run results as requested
 * [20 weeks ago](https://github.com/microsoft/TypeScript/pull/62391#issuecomment-3276893702) **typescript-bot** reported the results of running tsc on the top 400 repos comparing main and the PR merge and said everything looked good
 * (20 weeks ago) **jakebailey** closed the issue
 * **jakebailey** added label `Breaking Change`

### [PR microsoft/TypeScript#62477](https://github.com/microsoft/TypeScript/pull/62477) (Closed, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**Add \-\-ignoreConfig and dont allow specifying files on commandline without it if there is config file present**

*Introduce --ignoreConfig option and block file arguments when a config file exists unless the flag is used*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/62477#issuecomment-3572462583) **sheetalkamat** said "I just realised that this was marked as draft unintentionally for many days. Sorry about that."
 * (9 weeks ago) **sheetalkamat** closed the issue
 * **jakebailey** added label `Breaking Change`

### [PR microsoft/TypeScript#62509](https://github.com/microsoft/TypeScript/pull/62509) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Deprecate baseUrl**

*Mark the baseUrl compiler option as deprecated to guide users toward alternative configuration methods.*

 * **typescript-bot** added label `For Milestone Bug`
 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/62509#issuecomment-3348068639) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * (17 weeks ago) **andrewbranch** closed the issue
 * **jakebailey** added label `Breaking Change`

### [PR microsoft/TypeScript#62669](https://github.com/microsoft/TypeScript/pull/62669) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Deprecate \`\-\-module amd\`, \`umd\`, \`system\`, \`none\`; \`\-\-moduleResolution classic\`; change defaults**

*Deprecate amd, umd, system, and none modules and classic resolution, default to bundler for ES targets, and update tests accordingly.*

 * (14 weeks ago) **andrewbranch** closed the issue
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62669#issuecomment-3445051530) **typescript-bot** reported inability to cherry-pick the PR and provided a link to the logs
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62669#issuecomment-3445053364) **andrewbranch** remarked that they would investigate Azure Data Studio and VS Code usage of `--module none`, explained that the option was being deprecated due to inconsistent and weird behavior in Strada, and suggested it could be reinstated if a strong case emerges
 * **jakebailey** added label `Breaking Change`

### [PR microsoft/TypeScript#62876](https://github.com/microsoft/TypeScript/pull/62876) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Deprecate \`module\` syntax**

*Deprecate and error on all ‘module’ and ‘declare module’ syntax forms in TypeScript*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3643824331) **typescript-bot** initiated test job run and posted build status and result links
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3644259333) **typescript-bot** reported that everything looked good after running tsc on the top 800 repositories comparing main and the pull request merge
 * (7 weeks ago) **RyanCavanaugh** closed the issue
 * **jakebailey** added label `Breaking Change`

### [PR microsoft/TypeScript#62981](https://github.com/microsoft/TypeScript/pull/62981) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Deprecate \`\-\-outFile\`**

*Deprecate the --outFile compiler option as part of the fix for issue #62980.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741343885) **typescript-bot** reported user test comparisons between main and the merge pull request, noted infrastructure failures, and affirmed everything else looked good
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/62981#issuecomment-3741688191) **typescript-bot** reported that running tsc on the top 800 repos comparing main and the PR merge produced no issues
 * (2 weeks ago) **RyanCavanaugh** closed the issue
 * **jakebailey** added label `Breaking Change`

### [PR microsoft/TypeScript#63030](https://github.com/microsoft/TypeScript/pull/63030) (Closed, `Breaking Change`, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Deprecate alwaysStrict: false in TypeScript 6\.0**

*TypeScript 6.0 deprecates alwaysStrict=false, emitting warnings and requiring ignoreDeprecations to silence them ahead of its removal in 7.0.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787619893) **typescript-bot** provided the requested performance run results
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787685188) **typescript-bot** provided results of running tsc on the top 400 repos comparing main and the pull request merge and reported that everything looked good
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3791464828) **jakebailey** noted that the PR would not detect the problem because alwaysStrict can be disabled by setting strict to false and suggested forcing alwaysStrict when strict is false
 * **jakebailey** added label `Breaking Change`

### [Issue microsoft/TypeScript#63050](https://github.com/microsoft/TypeScript/issues/63050) (Open, `Help Wanted`, `Domain: Error Messages`, `Fix Available`, `Possible Improvement`)

**Double error message when referencing variable of type union of string literals from ambient declaration**

*TypeScript 4.0.5 duplicates the same error message when assigning an ambient string-literal union to a number.*

 * created by **devanshj**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63050#issuecomment-3798773309) **Andarist** pointed out the location where the source gets generalized and noted that the code is not union-aware and stems from a TypeScript PR
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63050#issuecomment-3809323001) **AdyaTech** explained why duplicate error messages appeared by describing TypeScript's internal simplification of union types and contrasting behavior with TS 3.9.7
 * (today) **RyanCavanaugh** added labels `Help Wanted`, `Possible Improvement`, set milestones to `Backlog`, `Dormant`, and removed from milestone `Backlog`
 * **typescript-bot** added label `Fix Available`

### [PR microsoft/TypeScript#63054](https://github.com/microsoft/TypeScript/pull/63054) (Open, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Set default \`types\` array to \`\[\]\`; support \`"\*"\` wildcard**

*Set the default types array to an empty list and implement '*' wildcard support.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836286) **typescript-bot** reported missing type definition errors in raineorshine/npm-check-updates from the top 800 repos suite
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836321) **typescript-bot** reported errors in reduxjs/redux-toolkit from running the top 800 repos suite
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836369) **typescript-bot** reported additional build failures from running the top 800 repos suite against the old tsc, detailing errors in various theatre-js/theatre package configurations
 * **jakebailey** added label `Breaking Change`
 * (today) **typescript-bot** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63058](https://github.com/microsoft/TypeScript/issues/63058) (Closed, `Not a Defect`)

**Partial\<\> with generics is throwing: Type 'xxx' is not assignable to type 'Partial\<T\>'\.**

*TypeScript rejects returning `{ time: 0 }` from a generic getPartial<T extends Timed>() as Partial<T> while the same literal assignment to a Partial<T> variable compiles.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63058#issuecomment-3811349951) **MartinJohns** explained why the error was correct for getPartial and identified an issue in getPartial2 while referencing issue #9825
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63058#issuecomment-3811843827) **jcalz** mentioned a StackOverflow question and issue #51645 related to getPartial(), explained that indexing a generic variable with a specific key widens it to its constraint causing unsoundness, and noted no specific issue exists
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63058#issuecomment-3827133886) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63065](https://github.com/microsoft/TypeScript/issues/63065) (Closed, `Question`)

**Is \`\`class A extends \(B\<T\>\)\<T\> {}\`\` valid code?**

*Asking whether the syntax `class A extends (B<T>)<T> {}` is valid TypeScript code without errors.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818619126) **fisker** clarified that the playground didn't refuse to parse despite showing multiple errors
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3818645780) **fisker** asked if the two class definitions were equivalent
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3819291024) **RyanCavanaugh** asked for clarification on what was being requested, noting it was already a semantic error
 * **RyanCavanaugh** added label `Question`
 * [later](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3827912099) **fisker** asked for a more specific error message instead of the generic "Cannot find name X"
 * [later](https://github.com/microsoft/TypeScript/issues/63065#issuecomment-3827967756) **bradzacher** identified two problematic TypeScript behaviors related to parentheses in class heritage and invalid generic instantiation syntax

### [PR microsoft/TypeScript#63067](https://github.com/microsoft/TypeScript/pull/63067) (Closed, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Default \`target\` to "latest standard", deprecate ES5**

*Set the default compilation target to the latest standardized ECMAScript version and deprecate ES5, updating tests accordingly.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821769199) **typescript-bot** reported the requested performance run results to @jakebailey
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821801870) **typescript-bot** reported DT test results including branch-only errors in activex-wia package
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3821818337) **typescript-bot** reported results of running the top 400 repos with tsc comparing main and pull request merge and noted an interesting change
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3826361341) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3826362047) **typescript-bot** started jobs and posted initial build status table
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3826463315) **typescript-bot** reported DT test failures for wallabyjs and react packages
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3826747988) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3826748714) **typescript-bot** reported that jobs started and provided links to build status and results
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3826909096) **typescript-bot** reported DT test results showing a compile error in the react package
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3826975853) **jakebailey** said "Shoot, I still didn't get react fixed"
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3827111088) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3827111476) **typescript-bot** reported that CI jobs started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/63067#issuecomment-3827144256) **typescript-bot** notified that the DT test results were ready and unchanged
 * **jakebailey** added label `Breaking Change`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63068](https://github.com/microsoft/TypeScript/issues/63068) (Closed, `Working as Intended`)

**"translate" property is yes/no not boolean**

*The dom.lib.d.ts file incorrectly defines the HTML translate attribute as boolean rather than string 'yes' or 'no'.*

 * created by **kkmuffme**
 * [today](https://github.com/microsoft/TypeScript/issues/63068#issuecomment-3824110965) **IllusionMH** clarified that the link referred to an HTML attribute rather than the JS DOM API, referenced the MDN HTMLElement.translate page, and provided example code
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63068#issuecomment-3826608865) **kkmuffme** said "Thanks for pointing that out, I totally missed that!"
 * (today) **kkmuffme** closed the issue

### [Issue microsoft/TypeScript#63069](https://github.com/microsoft/TypeScript/issues/63069) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`)

**Make standard library types more polyfills‑friendly**

*Propose enhancing TypeScript’s standard library declarations with interfaces, readonly properties, and conditional types to support polyfills.*

 * created by **slowcheetah**

### [PR microsoft/TypeScript#63070](https://github.com/microsoft/TypeScript/pull/63070) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Be more lenient about iteration when \`lib=es5\` / \`noLib\`**

*Enable array and string iteration under lib=es5 or noLib with ES2015+ targets by falling back to ES5 semantics*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63071](https://github.com/microsoft/TypeScript/pull/63071) (Open, `Breaking Change`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Deprecate downlevelIteration**

*Deprecate the downlevelIteration compiler flag in TypeScript 7.0 since it’s redundant for ES2015+ targets.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3825937537) **jakebailey** said "@typescript-bot test top400"
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3825937843) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3825938039) **typescript-bot** provided an automated build status update
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3826337952) **typescript-bot** reported build comparison results for top 400 repos between main and the PR and highlighted deprecation errors in three projects
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3826585042) **DanielRosenwasser** wondered if deprecating was worthwhile and pointed out that the issue stemmed from packages compiling to ES5 rather than the current project
 * [today](https://github.com/microsoft/TypeScript/pull/63071#issuecomment-3826592442) **jakebailey** noted that deprecated options already behaved this way, that setting it to null would not help when TS 7.0 arrives, and that the option felt pointless

### [PR microsoft/TypeScript#63072](https://github.com/microsoft/TypeScript/pull/63072) (Open, `For Uncommitted Bug`)

**Fix incorrectly reported 2689 error**

*TypeScript wrongly reports a TS2689 interface extension error when using valid generic type assertion syntax.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript/pull/63072#issuecomment-3825951609) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-bot** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63073](https://github.com/microsoft/TypeScript/issues/63073) (Closed, `Duplicate`)

**Argument of type 'string \| String' is not assignable to parameter of type 'string'\.**

*TypeScript does not collapse a 'string | String' union to 'string' after type checks, causing RegExp.test to error.*

 * created by **kkmuffme**
 * [today](https://github.com/microsoft/TypeScript/issues/63073#issuecomment-3826627617) **RyanCavanaugh** said "This is basically #2361"
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63073#issuecomment-3826636795) **RyanCavanaugh** pointed out that since String and Boolean both undergo identical conversion in .test(), treating Boolean input as valid is as questionable as using true directly

### [Issue microsoft/TypeScript#63074](https://github.com/microsoft/TypeScript/issues/63074) (Open, `Not a Defect`)

**\`x is any\` type guard widens \`unknown\` type even after the relevant scope has been exited**

*Custom type guard isAny incorrectly widens unknown types to any beyond the guard’s scope*

 * created by **coreywoodfield**
 * [today](https://github.com/microsoft/TypeScript/issues/63074#issuecomment-3827797037) **MartinJohns** said "Why would you ever write a x is any type guard?"

### [PR microsoft/TypeScript#63075](https://github.com/microsoft/TypeScript/pull/63075) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove ES5 references, misc cleanup**

*Remove non-test ES5 references, clean up dead code, and simplify enum identifier emission to ES2015+ in baselines.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63076](https://github.com/microsoft/TypeScript/pull/63076) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update implied default for module based on target**

*Default module format now follows the ECMAScript target (commonjs, es2015, es2020, es2022, or esnext).*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63076#issuecomment-3827654717) **jakebailey** triggered the TypeScript bot to run tests
 * [today](https://github.com/microsoft/TypeScript/pull/63076#issuecomment-3827654852) **typescript-bot** posted an automated build status update
 * [today](https://github.com/microsoft/TypeScript/pull/63076#issuecomment-3827695007) **typescript-bot** notified that DT test results were ready and everything looked the same
 * [later](https://github.com/microsoft/TypeScript/pull/63076#issuecomment-3827887922) **typescript-bot** reported that TypeScript compilation results for the top 800 repositories matched between main and the pull request merge

### [Issue microsoft/TypeScript#9726](https://github.com/microsoft/TypeScript/issues/9726) (Open, `Suggestion`, `Awaiting More Feedback`)

**Way of specifying non\-enumerable properties**

*Propose nonenum property annotations and an enumsof utility to ensure Object.assign’s types only include enumerable members.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/9726#issuecomment-1740932909) **snarfblam** suggested conveying non-enumerable properties via a 'flavor' type and using helper types to strip them, providing a code example
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/9726#issuecomment-1947323994) **c-vetter** asked how to construct the proper output type without enumsof and the value of nonenum, argued that nonenumerability should be the annotated variant due to default enumerability, explained that manual assertions are the main workaround and referred to @snarfblam's solution, and engaged with @MichaelScheffenacker's question about tracking outer type issues
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/9726#issuecomment-1992668286) **iameli** asked if the issue explains why properties can be spread onto unsupported objects despite typing and noted a related TypeScript issue
 * [later](https://github.com/microsoft/TypeScript/issues/9726#issuecomment-3828119738) **adjerbetian** suggested that a `noenum` keyword could enforce branded types to prevent improper object creation

