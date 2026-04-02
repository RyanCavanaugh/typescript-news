# Report for 2026-03-16 (Monday, March 16th, 2026)

14 different users commented on 14 different issues.

## Recommended Actions

 * Moderation
    * @snarbles2 posted unrelated content in [microsoft/TypeScript#63257](https://github.com/microsoft/TypeScript/issues/63257#issuecomment-4074445457)
 * Response Recommended
    * @ManishPrakkash asked if the issue was still open for a PR and offered help with requested changes in [microsoft/TypeScript#10285](https://github.com/microsoft/TypeScript/issues/10285#issuecomment-4069907897)
    * @ManishPrakkash asked if the issue was still open for a PR and offered help with requested changes in [microsoft/TypeScript#20183](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-4069910721)
    * @ManishPrakkash asked if the issue was still open for a PR and offered help with requested changes in [microsoft/TypeScript#22467](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-4069921460)
    * @ManishPrakkash asked if the issue was still open for a PR and offered help with requested changes in [microsoft/TypeScript#27910](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-4069922982)
    * @nvmnghia asked if this was deferred until 7.0 in [microsoft/TypeScript#62350](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-4075129195)

## Activity Summary

### [Issue microsoft/TypeScript#10285](https://github.com/microsoft/TypeScript/issues/10285) (Open, `Suggestion`, `Help Wanted`, `Domain: lib.d.ts`, `Good First Issue`)

**Scope of this is lost when passing a member function to setInterval**

*TypeScript loses the ‘this’ context when passing a class member function directly to setInterval, resulting in undefined instance properties unless an arrow function or explicit binding is used.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/10285#issuecomment-1903641297) **paskozdilar** suggested TypeScript should warn when methods are passed without their instance
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/10285#issuecomment-2498322403) **AudreyKj** said "Is this issue still open? I'm happy to work on this!"
 * [32 weeks ago](https://github.com/microsoft/TypeScript/issues/10285#issuecomment-3148610904) **julien98Qc** stated that this behavior is expected and suggested adding a warning only when the callback method uses `this`
 * [today](https://github.com/microsoft/TypeScript/issues/10285#issuecomment-4069907897) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"

### [Issue microsoft/TypeScript#20183](https://github.com/microsoft/TypeScript/issues/20183) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Domain: LS: Completion Lists`, `VS Code Tracked`, `PursuitFellowship`)

**Sort jsdoc parameter suggestions by argument position **

*JSDoc parameter suggestions triggered after @param should be sorted by their position in the function signature.*

 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-702422044) **shonnungar** said "Looking into this issue"
 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-1848271459) **ckcherry23** said "Hi @mjbvz, I'm a first-time contributor. Is this issue still relevant to take up?"
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-2600577963) **RafaelMeir4** asked if the issue was still a priority and requested guidance to the relevant implementation files
 * [today](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-4069910721) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"

### [Issue microsoft/TypeScript#22467](https://github.com/microsoft/TypeScript/issues/22467) (Open, `Bug`, `Help Wanted`, `Domain: API`, `Good First Issue`, `PursuitFellowship`)

**getDefinitionAtPosition doesn't distinguish different kinds in a merged declaration**

*getDefinitionAtPosition incorrectly reports all merged declarations as class rather than distinguishing module, class, and interface*

 * [3 years ago](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-1421971471) **KostiantynPopovych** described debugging issue with symbol kind detection in TypeScript tests and asked for guidance on obtaining the correct symbol condition
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-2641282213) **ardentechne** reproduced the bug and provided detailed reproduction steps and sample code
 * **RyanCavanaugh** added label `Domain: API`
 * [today](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-4069921460) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"

### [Issue microsoft/TypeScript#27910](https://github.com/microsoft/TypeScript/issues/27910) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Domain: Error Messages`, `Experience Enhancement`, `PursuitFellowship`)

**TS2367: This condition will always return 'false' since the types 'Constructor\<T\>' and 'typeof Child' have no overlap\.**

*Comparing a generic constructor type Constructor<T> to the specific Child class always fails due to incompatible types, causing TS2367.*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-720793820) **millsp** asked why t === '' errors for unbound generic T but works when T extends unknown and asked if they should open a separate issue
 * [5.1 years ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-761886530) **ETARAZ** demonstrated a working code snippet assigning t and using a ternary operator
 * [4.8 years ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-836730432) **vsDizzy** provided better illustrations with two images
 * [today](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-4069922982) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"

### [Issue microsoft/TypeScript#31090](https://github.com/microsoft/TypeScript/issues/31090) (Open, `Suggestion`, `Awaiting More Feedback`)

**Import type over generic argument**

*Allow import() types to use a generic string argument to infer module export types from dynamic paths.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/31090#issuecomment-2451695724) **pi0** said "This feature could also be useful for jiti to allow typing jiti.import(id)."
 * [48 weeks ago](https://github.com/microsoft/TypeScript/issues/31090#issuecomment-2789040833) **louwers** provided another use case for dependency injection of functions serializable to web workers
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/31090#issuecomment-3001769736) **jkomyno** described a use case for inferring the type of a dynamic import within a Webpack 5–compatible function and showed that the TypeScript definitions currently evaluate to any
 * [today](https://github.com/microsoft/TypeScript/issues/31090#issuecomment-4069332050) **exoRift** said "I would like to use this for defining typed methods for calling API endpoints on a file-based router"

### [PR microsoft/TypeScript#62350](https://github.com/microsoft/TypeScript/pull/62350) (Open, `For Uncommitted Bug`)

**Control flow analysis for destructured rests**

*Control flow analysis now correctly handles destructured rest properties in TypeScript.*

 * [27 weeks ago](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-3247688202) **typescript-bot** ran tsc validation on the top 400 repos and reported that everything looked good
 * [23 weeks ago](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-3353643706) **jakebailey** said "I feel fairly good about this PR, though I'm a bit shocked it didn't net anything in the extended tests."
 * [23 weeks ago](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-3358443286) **jakebailey** said "@ahejlsberg Curious what you think of this."
 * [later](https://github.com/microsoft/TypeScript/pull/62350#issuecomment-4075129195) **nvmnghia** said "is this deferred until 7.0?"

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050263019) **jakebailey** said "You'd need the nightly extension, or to set the tsdk VS Code option to point to your local repo."
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4050281506) **ekalkutin** thanked jakebailey and reported that he got it working with a settings.json configuration
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4055902206) **paigefletcher1282-code** thanked and confirmed that the issue was fixed
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4070560511) **DanielRosenwasser** said "@typescript-bot bump release-6.0"
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4070560893) **typescript-bot** updated build status for bump release-6.0 jobs
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4070606069) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.2 for you."

### [PR microsoft/TypeScript#63224](https://github.com/microsoft/TypeScript/pull/63224) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Upgrade GitHub Actions by bumping actions/setup-node from 6.2.0 to 6.3.0 and updating the github/codeql-action.*

 * (1 week ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63250](https://github.com/microsoft/TypeScript/issues/63250) (Closed, `Not a Defect`)

**\# Bug Report: \`Omit\`\-based assertion narrowing fails to override method return types on classes with private members**

*Assertion narrowing using Omit on a class with private members fails to update its method's return type.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63250#issuecomment-4058761505) **RyanCavanaugh** explained that assertion narrowings can't widen types so Client remains intersected, affecting overload resolution, and outlined why altering the process would break other behaviors
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63250#issuecomment-4060965643) **khalidsaidi** noted that A2ABench had an accepted answer for the imported thread and provided its details
 * [today](https://github.com/microsoft/TypeScript/issues/63250#issuecomment-4071752461) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63251](https://github.com/microsoft/TypeScript/issues/63251) (Open, `Suggestion`, `Needs Proposal`)

**Mechanism to specify input source location to find \`package\.json\` instead of output source location when determining module format**

*Provide a mechanism to use source directory instead of output directory when locating package.json for NodeNext module resolution*

 * created by **monsanto**
 * [today](https://github.com/microsoft/TypeScript/issues/63251#issuecomment-4068800089) **andrewbranch** explained that due to project references remapping .ts to .d.ts and module resolution based on output files, declaration files in an outDir outside a module-type package are treated as CommonJS and noted that improving input/output awareness will require work beyond a pre-6.0 patch
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Needs Proposal`
 * [today](https://github.com/microsoft/TypeScript/issues/63251#issuecomment-4069551483) **monsanto** said "Okay, I can workaround this."

### [Issue microsoft/TypeScript#63253](https://github.com/microsoft/TypeScript/issues/63253) (Closed, `Docs`, **DanielRosenwasser**)

**Typo in TS 6\.0 blog post: \`temporal\.esnext\` should be \`esnext\.temporal\`**

*The TypeScript 6.0 blog post mistakenly instructs using temporal.esnext instead of the valid esnext.temporal library.*

 * created by **lgarron**
 * (today) **RyanCavanaugh** added label `Docs`, and assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript#63256](https://github.com/microsoft/TypeScript/pull/63256) (Open)

**fix: improve confusing TS1107 error for mislabeled jump targets**

*The compiler now only emits TS1107 for jump labels crossing function boundaries, otherwise emitting missing label errors.*

 * created by **AkaHarshit**
 * [today](https://github.com/microsoft/TypeScript/pull/63256#issuecomment-4070141715) **microsoft-github-policy-service[bot]** requested the contributor to sign the CLA by replying with the agree command

### [Issue microsoft/TypeScript#63257](https://github.com/microsoft/TypeScript/issues/63257) (Closed, `Working as Intended`)

**Clauses instead of Classes**

*The TypeScript handbook mistakenly uses “Clauses” instead of “Classes” in its documentation.*

 * created by **VitaliiZemliakov**
 * [later](https://github.com/microsoft/TypeScript/issues/63257#issuecomment-4073039951) **MartinJohns** asked to fill out the issue template completely and corrected terminology to 'clauses'
 * [later](https://github.com/microsoft/TypeScript/issues/63257#issuecomment-4074445457) **snarbles2** quoted the dictionary definition of “clause”
 * **RyanCavanaugh** added label `Working as Intended`
 * [later](https://github.com/microsoft/TypeScript/issues/63257#issuecomment-4075982744) **RyanCavanaugh** said "Not a typo; when you type class C implements Y, the implements Y part is called a "clause"."
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63258](https://github.com/microsoft/TypeScript/issues/63258) (Closed)

**Unexpected inferred type when inferred constraint is union \[T extends \(infer I extends number \| infer U extends string\)\]**

*Conditional types using a union of infer constraints unexpectedly infer the string fallback instead of never.*

 * created by **seetyewsiang**
 * (later) **seetyewsiang** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63258#issuecomment-4075288801) **seetyewsiang** stated that adding parentheses fixed the issue and provided a TypeScript Playground link

