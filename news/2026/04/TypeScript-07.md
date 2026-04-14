# Report for 2026-04-07 (Tuesday, April 7th, 2026)

10 different users commented on 23 different issues.

## Recommended Actions

 * Response Recommended
    * @denis-migdal suggested updating the DeepReadonly type definition in [microsoft/TypeScript#14471](https://github.com/microsoft/TypeScript/issues/14471#issuecomment-4204043464)
    * @ArsenArsen suggested a new feature for aligning JS definitions with .d.ts types and declaration merging in [microsoft/TypeScript#29056](https://github.com/microsoft/TypeScript/issues/29056#issuecomment-4201771881)
    * @DDD-fx asked for this feature for combineLates in [microsoft/TypeScript#41173](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-4204447521)

## Activity Summary

### [Issue microsoft/TypeScript#11920](https://github.com/microsoft/TypeScript/issues/11920) (Open, `Suggestion`, `Awaiting More Feedback`, `Has Repro`)

**disallow comparing to null and undefined unless they are valid cases in strict null mode**

*Require TypeScript’s strictNullChecks to flag comparisons to null or undefined for values whose types cannot include them.*

 * [2 years ago](https://github.com/microsoft/TypeScript/issues/11920#issuecomment-2032537244) **ersjim** described encountering an infinite loop when peek returned an empty string instead of null and noted the type system didn’t catch the mismatch
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/11920#issuecomment-2088726193) **skondrashov** noted being able to compare a Date to null, expressed confusion why TypeScript allowed it, and asked how to enable type checking for this or add that feature
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/11920#issuecomment-2419744971) **lauraharker** asked whether a purely syntactic check could disallow impossible null/undefined comparisons like `typeof foo === undefined`
 * [today](https://github.com/microsoft/TypeScript/issues/11920#issuecomment-4204144136) **denis-migdal** proposed enhancements to require explicit boolean casts for conditions and loops containing only true or false and suggested flags or keywords to enforce this

### [Issue microsoft/TypeScript#14471](https://github.com/microsoft/TypeScript/issues/14471) (Open, `Needs Investigation`)

**Using \`undefined\` as a discriminator within a mapped type yields erroneous types when primitive intersections are involved**

*TypeScript erroneously infers types when using undefined as a discriminator in mapped types involving primitive intersections.*

 * (6.2 years ago) **RyanCavanaugh** set milestone to `Backlog`, removed from milestone `TypeScript 3.8.1`, and unassigned **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/14471#issuecomment-4204043464) **denis-migdal** suggested that the issue was in the DeepReadonly type definition and provided an updated implementation and playground link

### [Issue microsoft/TypeScript#29056](https://github.com/microsoft/TypeScript/issues/29056) (Open, `Suggestion`, `Awaiting More Feedback`)

**Allow local \.js/\.ts files to be typed by their corresponding \.d\.ts file**

*Allow local JavaScript and TypeScript files to derive types from matching .d.ts files, preventing implicit any errors and enabling intellisense*

 * [5 years ago](https://github.com/microsoft/TypeScript/issues/29056#issuecomment-802094735) **id-ekaagr** said "This is a must have feature. Flow has it."
 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/29056#issuecomment-1116247025) **frank-dspeed** mentioned having full IntelliSense in .js files via tsconfig settings, noted issues with incorrectly packaged types, and acknowledged that the project's .d.ts file wasn't authoritative
 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/29056#issuecomment-1116253751) **frank-dspeed** proposed reopening and renaming the issue to focus on tsconfig.json types lookup priority, explained scenarios where .ts/.js or .d.ts should be authoritative, and suggested using declaration=false with include .d.ts, allowJs, checkJs, and noEmit to avoid overwrite errors
 * [today](https://github.com/microsoft/TypeScript/issues/29056#issuecomment-4201771881) **ArsenArsen** suggested adding an option to treat JS definitions as if declared with types from the corresponding .d.ts and to support declaration merging to reduce repetition
 * [later](https://github.com/microsoft/TypeScript/issues/29056#issuecomment-4207408316) **ustun** thanked ArsenArsen for bumping the thread, unsubscribed due to feeling old, and reminisced about an earlier comment

### [Issue microsoft/TypeScript#41173](https://github.com/microsoft/TypeScript/issues/41173) (Open, `Suggestion`, `Awaiting More Feedback`)

**Accept de\-structured elements in type predicates**

*Allow destructured parameters in TypeScript type predicate functions to enable more concise and readable type checks.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-2740322844) **mariusaarsnes** said "Any updates here?"
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-2750780227) **adam-marshall** said "Any news?"
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-3733647068) **ljharb** expressed frustration that TypeScript required literal argument names and prevented destructuring
 * [later](https://github.com/microsoft/TypeScript/issues/41173#issuecomment-4204447521) **DDD-fx** expressed support and requested the feature for combineLates

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4187144985) **ArfanFahad** reported having a persistent warning and a watcher compilation failure after applying IntelliSense fix
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4187271405) **jakebailey** said "There's no problem. This is very intentional. Remove that option."
 * [today](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4197912770) **SOMONSOUM** suggested removing the baseUrl setting and adding a paths configuration
 * [later](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4205504780) **ArfanFahad** removed baseUrl and confirmed it worked after adding paths

### [Issue microsoft/TypeScript#63231](https://github.com/microsoft/TypeScript/issues/63231) (Open, `Needs More Info`)

**exports subpath with array types is not autocompleting**

*VS Code’s JavaScript/TypeScript language server does not autocomplete import paths for subpaths when exports.types is defined as an array*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4040628071) **RyanCavanaugh** said "@unional can you check this in TS 7 (native preview) and tell me if it still repros?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4041227902) **unional** said "Hi @RyanCavanaugh, sure will give that a try when I get a chance to. "
 * [today](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4204245115) **unional** confirmed the issue also existed in tsgo
 * [today](https://github.com/microsoft/TypeScript/issues/63231#issuecomment-4204282083) **unional** provided examples of wildcard exports not being autocompleted and described import map bloat mitigation using explicit file extensions

### [Issue microsoft/TypeScript#63342](https://github.com/microsoft/TypeScript/issues/63342) (Open, `Experimentation Needed`, `Domain: check: Big Unions`, `Possible Improvement`)

**type checking complexity with multiple template literals in unions**

*TypeScript’s type checking time scales exponentially with unions of template literal types in dynamic route definitions.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4180398717) **eps1lon** asked what the conclusion was after discussions fizzled over memory concerns and offered to investigate the benchmarks further
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4180447400) **jakebailey** said "The conclusion was "we didn't come to a conclusion before this codebase became closed to new PRs": https://github.com/microsoft/TypeScript#contribute"
 * [today](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4197960180) **eps1lon** said "There's a Go port: https://github.com/microsoft/typescript-go/pull/3331"
 * (today) **RyanCavanaugh** added labels `Experimentation Needed`, `Possible Improvement`

### [Issue microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346) (Closed, `Question`)

**Experimental \(deprecated\) decorators are included by default**

*The ESNext library includes legacy experimental decorator types by default, causing conflicts with new decorator definitions.*

 * created by **OldStarchy**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4193336835) **RyanCavanaugh** thanked the user and provided a list of similar issues
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4200850258) **RyanCavanaugh** said "The error message means what it says; you are missing the export modifier on your type alias"

### [Issue microsoft/TypeScript#63352](https://github.com/microsoft/TypeScript/issues/63352) (Closed, `Bug`, `Domain: lib.d.ts`)

**Trivial: typo**

*Corrects the misspelling of “parameter” as “paramater” in the es5.d.ts definitions file.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63352#issuecomment-4188736423) **deepnav4** expressed interest in working on the issue
 * (yesterday) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: lib.d.ts`

### [Issue microsoft/TypeScript#63353](https://github.com/microsoft/TypeScript/issues/63353) (Closed)

**Declaration emit references imported type without importing it when inheriting static methods via CommonJS \`require\`**

*Declaration emitter omits import for a referenced typedef and emits an unused require import when inheriting static methods via CommonJS.*

 * created by **avivkeller**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63353#issuecomment-4193336982) **RyanCavanaugh** provided automated analysis with links to similar issues
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63353#issuecomment-4193365190) **avivkeller** clarified that the referenced issues correspond to regressions in different TypeScript versions and identified one as unrelated
 * [today](https://github.com/microsoft/TypeScript/issues/63353#issuecomment-4200714633) **RyanCavanaugh** said "Doesn't repro in TS 7"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63357](https://github.com/microsoft/TypeScript/issues/63357) (Open, `Domain: check: Contextual Types`, `Possible Improvement`)

**Error on function return is less useful than it should be**

*TypeScript reports return-type mismatches on function assignments rather than at the actual return statement, making errors harder to diagnose.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63357#issuecomment-4193147732) **RyanCavanaugh** said "This is basically because of #241, but maybe we could special case it? Not sure"
 * (yesterday) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Dormant`
 * **RyanCavanaugh** added label `Domain: check: Contextual Types`

### [Issue microsoft/TypeScript#63358](https://github.com/microsoft/TypeScript/issues/63358) (Open, `Bug`, `Domain: JSX/TSX`)

**TSX error location error with location and JSX comment**

*A preceding JSX comment causes TypeScript to report a non-ReactNode type error on the comment instead of the expression.*

 * (yesterday) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63358#issuecomment-4194330994) **RyanCavanaugh** said "Repro confirmed in TS7"
 * **RyanCavanaugh** added label `Domain: JSX/TSX`

### [Issue microsoft/TypeScript#63363](https://github.com/microsoft/TypeScript/issues/63363) (Open, `Needs Investigation`)

**Inside a generic function with a remapped type as parameter, elements are wrongfully inferred as {}\.**

*Indexed access of remapped generic type properties in a generic function leads to them being inferred as {} instead of their defined type.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4193188506) **RyanCavanaugh** said "Why are you writing the function signature this way in the first place?"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4193519030) **denis-migdal** provided a minimal reproducible example and shared the real code signature with a playground link
 * [today](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4200106490) **denis-migdal** provided TypeScript examples comparing different mapped type key remappings and noted which caused fewer inference issues
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Dormant`

### [Issue microsoft/TypeScript#63367](https://github.com/microsoft/TypeScript/issues/63367) (Open, `Needs More Info`)

**Stuck in initialization loop on v1\.114 w/ TS 5, also on v1\.113 w/ TS 6**

*VSCode repeatedly loops initializing TypeScript configurations for each project in a large pnpm monorepo on v1.114 with TS 5 or v1.113 with TS 6*

 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4195761326) **NullVoxPopuli** said "if it helps, I do not have this issue with neovim, the built in LSP, and tsserver"
 * [today](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4200542561) **RyanCavanaugh** thanked the user and provided an automatically generated list of similar issues
 * [today](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4200572460) **RyanCavanaugh** said "It's unlikely this would meet the 6.0 patch bar, but it'd be good to have a repo we could clone and check with just to make sure it's not a more widespread root cause."
 * **RyanCavanaugh** added label `Needs More Info`

### [PR microsoft/TypeScript#63368](https://github.com/microsoft/TypeScript/pull/63368) (Closed)

**Harden ATA package name filtering**

*Restrict ATA package names to alphanumeric characters, underscores, periods, and hyphens to prevent shell-related validation issues.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63368#issuecomment-4200840842) **jakebailey** said "@typescript-bot cherry-pick this to release-6.0"
 * [today](https://github.com/microsoft/TypeScript/pull/63368#issuecomment-4200841325) **typescript-bot** reported that CI jobs started and completed for the 'cherry-pick this to release-6.0' command and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/63368#issuecomment-4200853561) **typescript-bot** said "Hey, @jakebailey! I've created #63372 for you."

### [Issue microsoft/TypeScript#63370](https://github.com/microsoft/TypeScript/issues/63370) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add a \`redeclare\` keyword to redeclare class attributes, behaving like \`override \!:\` while keeping type modifiers\.**

*Add a new `redeclare` keyword in TypeScript to override and declare class properties while preserving or adjusting existing type modifiers.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63370#issuecomment-4200542701) **RyanCavanaugh** provided an automated response listing similar issues and suggesting duplicates
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63370#issuecomment-4200861418) **denis-migdal** enumerated three related issues and explained how they relate to his redeclare proposal

### [PR microsoft/TypeScript#63372](https://github.com/microsoft/TypeScript/pull/63372) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63368 \(Harden ATA package name filtering\) into release\-6\.0**

*Apply PR #63368’s hardened ATA package name filtering to the release-6.0 branch pending review and merge.*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63373](https://github.com/microsoft/TypeScript/issues/63373) (Open)

**tsserver hangs in Yarn PnP projects — incorrect directory watcher due to unchecked indexOf returning \-1**

*tsserver in Yarn PnP projects hangs because unchecked indexOf on non-node_modules paths produces incorrect directory watcher paths.*

 * created by **sebaspf**

