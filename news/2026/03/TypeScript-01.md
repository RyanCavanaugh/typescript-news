# Report for 2026-03-01 (Sunday, March 1st, 2026)

8 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @constraintAutomaton asked whether the issue would be considered and users could be linked to the type predicates documentation page in [microsoft/TypeScript#61881](https://github.com/microsoft/TypeScript/issues/61881#issuecomment-3983800930)
    * @ackvf asked what IDE configuration can ensure unused variables are always dimmed regardless of rules or extensions in [microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3983613552)
    * @Arlen22 asked for help debugging a dependency or type issue causing refactoring to fail in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3985103294)

## Activity Summary

### [Issue microsoft/TypeScript#29841](https://github.com/microsoft/TypeScript/issues/29841) (Open, `Needs Investigation`, `Fix Available`, `Rescheduled`, **DanielRosenwasser**)

**Improve typings of Array\.map when called on tuples**

*Enhance Array.map’s TypeScript typings to return a tuple type when mapping over a tuple instead of a generic array.*

 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-2980318799) **marcospgp** said "seeing this issue is still open, is there any chance we can still get proper tuple typing in built in functions like .map()?"
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-3327091081) **Anoesj** requested automatic tuple .map() typing support and suggested a tsconfig option
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-3642875750) **petdomaa100** reported encountering the issue frequently and suggested using a dedicated mapTuple method or utility function as a workaround
 * [today](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-3980542123) **BarthPaleologue** said "That would be a great feature! Maybe the advent of go for TSC will help make this a reality?"

### [Issue microsoft/TypeScript#61881](https://github.com/microsoft/TypeScript/issues/61881) (Open, `Help Wanted`, `Docs`)

**Type Guard Documentation Is Incorrectly Labeled as Deprecated**

*The TypeScript type guard documentation is wrongly flagged as deprecated and directs users to a non-existent replacement page.*

 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/61881#issuecomment-2978769950) **ryanoboril** submitted a pull request for review on the TypeScript-Website repository
 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/61881#issuecomment-2981078322) **RyanCavanaugh** critiqued the Advanced Types page as sprawling and suggested adding per-section deprecation headers
 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/61881#issuecomment-2982733957) **ryanoboril** suggested changing the "Go to New Page" button to direct users to the top-level handbook page instead of the "types of types" section
 * [later](https://github.com/microsoft/TypeScript/issues/61881#issuecomment-3983800930) **constraintAutomaton** said "Hi, I wonder if this issue will be consider and if the users could be linked to that page https://www.typescriptlang.org/docs/handbook/2/narrowing.html#using-type-predicates instead?"

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3952328155) **Renegade334** said "Have opened #63190 for a small interoperability improvement."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3975924546) **DanielRosenwasser** described merging #63190, questioned including plural forms in DateUnit and TimeUnit due to compatibility concerns, and opened issue #63201
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3975960874) **ptomato** explained the rationale for accepting both singular and plural units in duration-related APIs
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3982492021) **justingrant** referenced a previous comment on the revert PR, expressed opposition to the revert, and suggested continuing the discussion in that thread

### [Issue microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add switch to disable \_var unused variable prevention**

*Add a tsconfig option to disable automatic ignoring of underscore-prefixed unused variables so the compiler still reports them to IDE.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3947344632) **guillaumebrunerie** suggested two possible solutions by renaming the variable or enabling the @typescript-eslint/no-unused-vars rule and provided a playground link and screenshot
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3953666515) **ackvf** explained their confusion about eslint unused-variable settings and justified making IDE prefix handling configurable
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3957255323) **guillaumebrunerie** explained that TypeScript errors and ESLint warnings both appear and suggested disabling noUnusedLocals and noUnusedParameters to rely solely on ESLint for consistent styling
 * [later](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3983613552) **ackvf** asked how to configure the IDE to always dim unused variables regardless of disabled extensions or suppressed rules

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * (5 days ago) **RyanCavanaugh** added label `Domain: LS: TSServer`, and set milestone to `Backlog`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3961671540) **Arlen22** said "Ok, this doesn't happen in every project, so it might be more on the typescript side of things. "
 * [later](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3985103294) **Arlen22** described being unable to rename generic type parameters in one part of the project and expressed confusion about an underlying dependency or type issue

### [PR microsoft/TypeScript#63184](https://github.com/microsoft/TypeScript/pull/63184) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.3 to 4\.32\.4 in the github\-actions group**

*Update github/codeql-action from v4.32.3 to v4.32.4 to use the latest CodeQL bundle and improved proxy certificates*

 * (1 week ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63184#issuecomment-3981456935) **dependabot[bot]** said "Looks like github/codeql-action is updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63197](https://github.com/microsoft/TypeScript/issues/63197) (Open)

**Fatal OOM crash on recursive template literal type**

*A recursive template literal type definition causes a fatal out-of-memory crash in TypeScript versions 5.9.3 and 6.0.0-beta.*

 * created by **james-pre**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3975868967) **RyanCavanaugh** requested the actual minimal repro for the issue and noted that long compilation time isn't a security issue
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3975896004) **james-pre** provided environment details, a CI reproduction link, an example type causing the crash, and the tsconfig configuration
 * [later](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3984559138) **mkantor** provided a minimized reproduction case demonstrating the crash

### [Issue microsoft/TypeScript#63198](https://github.com/microsoft/TypeScript/issues/63198) (Closed, `Duplicate`)

**"Pure" Replacement for Enums \(Erasable Constants\)**

*Propose a fully erasable TypeScript enum syntax that compiles to a simple object literal without runtime code.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973393272) **MartinJohns** noted that the proposal would conflict with the Viability Checklist and language Design Goals
 * **RyanCavanaugh** added label `Duplicate`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973939522) **RyanCavanaugh** said "This seems to lack an actual proposal. #60790 is the spirit of what's being implied here."
 * [today](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3981556616) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63201](https://github.com/microsoft/TypeScript/pull/63201) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Revert "discrete pluralizer for lib\.esnext\.temporal unit unions"**

*Revert the discrete pluralizer addition for lib.esnext.temporal unit unions in TypeScript*

 * (2 days ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63201#issuecomment-3982486366) **justingrant** explained the rationale for accepting both singular and plural unit strings in certain Temporal API methods and for using a wrapper type in TypeScript definitions to improve IntelliSense

### [PR microsoft/TypeScript#63205](https://github.com/microsoft/TypeScript/pull/63205) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump the github-actions group in the repository root by upgrading actions/upload-artifact to v7.0.0 and updating github/codeql-action.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

