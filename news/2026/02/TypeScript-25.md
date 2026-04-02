# Report for 2026-02-25 (Wednesday, February 25th, 2026)

18 different users commented on 39 different issues.

## Recommended Actions

 * Response Recommended
    * @mohammadazeemwani provided a workaround for linking to the documentation file in [microsoft/TypeScript#47718](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-3963918316)
    * @andriyor asked if the PR will be merged in [microsoft/TypeScript#58495](https://github.com/microsoft/TypeScript/pull/58495#issuecomment-3961472425)
    * @DominoPivot reported that the example is wrong and suggested using Map.groupBy in [microsoft/TypeScript#61706](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-3962612851)
    * @FrameMuse suggested hiding Function properties/methods in hints similar to Object ones in [microsoft/TypeScript#63150](https://github.com/microsoft/TypeScript/issues/63150#issuecomment-3966078239)
    * @polson136 suggested clarifying documentation regarding when file extensions are required in [microsoft/TypeScript#63162](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3960435679)
    * @Chklang asked why the linter isn't part of the TypeScript compiler and why optional chaining non-null assertion isn't checked at compile time in [microsoft/TypeScript#63191](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3960302693)
    * @jogibear9988 asked if React's "use server"/"use client" was similar in [microsoft/TypeScript#63194](https://github.com/microsoft/TypeScript/issues/63194#issuecomment-3967379989)

## Activity Summary

### [Issue microsoft/TypeScript#47718](https://github.com/microsoft/TypeScript/issues/47718) (Open, `Suggestion`, `In Discussion`)

**Provide way to link to other files from JSDoc comments **

*Include the source file path in quickInfo documentation responses to enable editors to resolve relative JSDoc file links.*

 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-3274806833) **davidpcaldwell** explained that EmilyRosina's suggestion made clickable tooltip links but not editor links, questioned whether file://-style links were also intended, and proposed a combined syntax to make links clickable in both contexts
 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-3285406966) **tresorama** tried EmilyRosina’s solution but found it only worked within the file defining the JSDocs and not from other files, speculating that the link path is computed from the active file rather than the JSDoc file
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-3607486150) **crlmrlck** asked how to link directly to specific symbols using JSDoc @link
 * [today](https://github.com/microsoft/TypeScript/issues/47718#issuecomment-3963918316) **mohammadazeemwani** reported that heading references weren't working and provided a workaround to link directly to the file

### [PR microsoft/TypeScript#58495](https://github.com/microsoft/TypeScript/pull/58495) (Open, `For Uncommitted Bug`)

**Infer AssertsIdentifier type predicates**

*Add support for inferring 'asserts identifier' type predicates in function declarations by analyzing return-site types.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/pull/58495#issuecomment-2113498053) **typescript-bot** provided the requested perf run results
 * [1.7 years ago](https://github.com/microsoft/TypeScript/pull/58495#issuecomment-2113600568) **typescript-bot** reported that the comparison of the top 400 repositories between main and the pull request merge looked good
 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/58495#issuecomment-2406369705) **dgreensp** praised the work and asked if it allows a function to assert things about multiple parameters
 * [today](https://github.com/microsoft/TypeScript/pull/58495#issuecomment-3961472425) **andriyor** said "Is there any chance it will be merged?"

### [Issue microsoft/TypeScript#61706](https://github.com/microsoft/TypeScript/issues/61706) (Open, `Suggestion`, `Awaiting More Feedback`)

**\`Object\.groupBy\` should not return \`Partial\<Record\<string, T\>\>\` or \`Partial\<Record\<number, T\>\>\`**

*Object.groupBy's type definitions unnecessarily return Partial<Record<string|number, T>> for unrestricted keys, causing false undefined errors.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-3431185657) **TiAlRo** proposed adjusting groupBy’s return type to Record<K, T[]> and modifying Record for union-literal keys to permit omitted keys at runtime with T | undefined while preserving autocompletion and existing string-key behavior
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-3432033532) **TiAlRo** said "Additionally, the type Partial> should be assignable to the type Record because there is no difference."
 * [today](https://github.com/microsoft/TypeScript/issues/61706#issuecomment-3962612851) **DominoPivot** corrected the example by noting Object.groupBy returns a null-prototype object, explained TypeScript optional index signature issue, and suggested using Map.groupBy

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868792183) **typescript-bot** said "Hey, @DanielRosenwasser! I've created release-6.0 with version 6.0.0-beta for you."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3944591376) **HolgerJeromin** noted that the PR also deprecated --module=none and questioned whether it is less-used in the wild
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3959254158) **erictheswift** asked about updates on the RC/test build arrival and whether an existing dev build could be considered test-quality
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3962487549) **DanielRosenwasser** apologized for the delay, said the release candidate should arrive within a week, and mentioned that dev and nightly builds are available via npm and the VS Code Marketplace

### [Issue microsoft/TypeScript#63090](https://github.com/microsoft/TypeScript/issues/63090) (Open, `Bug`, `Help Wanted`, `Domain: check: Type Circularity`)

**Crash: RangeError: Maximum call stack size exceeded during type serialization of recursive distributive mapped types**

*Recursive distributive mapped types trigger a compiler stack overflow error in TypeScript 5.7.3 and later.*

 * (1 week ago) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Type Circularity`

### [Issue microsoft/TypeScript#63092](https://github.com/microsoft/TypeScript/issues/63092) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**Crash: RangeError: Maximum call stack size exceeded in isReachableFlowNodeWorker with complex for loop headers**

*TypeScript's compiler crashes with a maximum call stack size exceeded error when analyzing reachability in complex for loop headers.*

 * (1 week ago) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: check: Control Flow`

### [Issue microsoft/TypeScript#63094](https://github.com/microsoft/TypeScript/issues/63094) (Open, `Bug`, `Help Wanted`, `Domain: Decorators`)

**Crash: Debug Failure\. False expression in getArgumentArityError when resolving overloaded decorators with \-\-experimentalDecorators**

*TypeScript crashes with a 'Debug Failure. False expression' error in getArgumentArityError when resolving overloaded decorators under --experimentalDecorators.*

 * (1 week ago) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Decorators`

### [Issue microsoft/TypeScript#63149](https://github.com/microsoft/TypeScript/issues/63149) (Open)

**\[TS\]: Incorrect handling of \`JSDoc\` description of interface property**

*VS Code incorrectly strips parentheses-enclosed JSX tags from interface property JSDoc descriptions in hover tooltips.*

 * **mjbvz** unassigned **mjbvz**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3940793235) **darshjme-codes** said "Triage: JSDoc description handling bug Labels: Bug, JSDoc, Language Service | Impact: Documentation display issues in editors"
 * [today](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3957875823) **adhnannp** said "i will work on this, could you assign this to me @psnet "
 * [today](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3961175857) **RyanCavanaugh** provided an automated analysis listing similar issues

### [Issue microsoft/TypeScript#63150](https://github.com/microsoft/TypeScript/issues/63150) (Open, `Suggestion`, `Experience Enhancement`)

**\[JavaScript/TypeScript Language Hints\] Hide default \`Function\` properties/methods until manually typed just like in Rust\.**

*Add an option to hide default Function properties in JavaScript/TypeScript code completions until manually typed.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63150#issuecomment-3953420539) **RyanCavanaugh** suggested picking up the feature for classes in TS7 since it was already done for Object but not functions
 * (yesterday) **RyanCavanaugh** added labels `Suggestion`, `Experience Enhancement`
 * [later](https://github.com/microsoft/TypeScript/issues/63150#issuecomment-3966078239) **FrameMuse** acknowledged mixing up Object with Function and suggested hiding Function properties and methods in hints like Object ones

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * (yesterday) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: LS: TSServer`
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3961671540) **Arlen22** said "Ok, this doesn't happen in every project, so it might be more on the typescript side of things. "

### [Issue microsoft/TypeScript#63159](https://github.com/microsoft/TypeScript/issues/63159) (Open, `Bug`, `Domain: LS: TSServer`)

**False positive "Private field \.\.\. must be declared in an enclosing class\."**

*VS Code wrongly reports private field must be declared errors in a second JavaScript file due to cross-tab state pollution.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3940793141) **darshjme-codes** said "Triage: False positive "Private field must be initialized" Labels: Bug, Strictness, Private Fields | Type: Control flow analysis gap"
 * (yesterday) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: LS: TSServer`

### [Issue microsoft/TypeScript#63162](https://github.com/microsoft/TypeScript/issues/63162) (Closed, `Duplicate`)

**Module resolution: Extension required when moduleResolution=bundler and imports/exports used**

*TypeScript's bundler moduleResolution requires explicit .js extensions for imports and exports, causing build-time failures despite working in Vite.*

 * (yesterday) **andrewbranch** removed label `Needs Investigation`, and unassigned **andrewbranch**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3953610741) **andrewbranch** argued that '#src/imported-file' is not a relative path and that naming a resolution mode 'bundler' is problematic because bundlers differ, so TypeScript should follow the Node.js spec
 * [today](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3960435679) **polson136** agreed that bundlers were at fault and suggested clarifying the documentation regarding when file extensions are required

### [Issue microsoft/TypeScript#63173](https://github.com/microsoft/TypeScript/issues/63173) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: Maximum call stack size exceeded when declare const enum has a computed property named \[object\] followed by an object member**

*The compiler overflows the call stack when a const enum has a computed [object] member followed by an object member.*

 * (yesterday) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: Crashes`

### [Issue microsoft/TypeScript#63185](https://github.com/microsoft/TypeScript/issues/63185) (Open, `Bug`, `Domain: Source Maps`, **weswigham**)

**tsgo producing source maps that cause functions to appear uncovered in tests**

*tsgo 7.0.0-dev’s generated source maps unexpectedly include inline sources, causing code coverage tools to misreport covered functions as uncovered.*

 * created by **isaacs**
 * (yesterday) **RyanCavanaugh** added label `Bug`, and assigned to **weswigham**
 * **RyanCavanaugh** added label `Domain: Source Maps`

### [Issue microsoft/TypeScript#63189](https://github.com/microsoft/TypeScript/issues/63189) (Open)

**Incorrect reference \`this\` in static context with \`experimentalDecorators\` enabled**

*With experimentalDecorators enabled TypeScript incorrectly emits static `this` references as undefined rather than the class.*

 * created by **yavanosta**
 * [today](https://github.com/microsoft/TypeScript/issues/63189#issuecomment-3961176209) **RyanCavanaugh** provided an auto-generated list of similar issues to assist the user

### [PR microsoft/TypeScript#63190](https://github.com/microsoft/TypeScript/pull/63190) (Closed, `For Uncommitted Bug`)

**discrete pluralizer for lib\.esnext\.temporal unit unions**

*Restrict DateUnit and TimeUnit unions to singular names and use a pluralizer helper for js-temporal compatibility.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3954299849) **Renegade334** provided a link to the relevant type definition in the polyfill
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3954356867) **jakebailey** said "Ah, but the mapped type doesn't exist?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3954648935) **Renegade334** noted that a T | PluralUnit<T> union was used wherever plurals appear and that the bikeshed remained open
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3961416016) **jakebailey** said "In a way I wish it were just PluralizeUnits, but I'm not the greatest namer out there."
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3961773716) **Renegade334** said "Comme ça ?"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63191](https://github.com/microsoft/TypeScript/issues/63191) (Closed, `Suggestion`, `Declined`)

**The "?" operator would be forbidden before the "\!" operator**

*Request to disallow combining optional chaining (?) with non-null assertion (!) in TypeScript to prevent unsafe undefined values.*

 * created by **Chklang**
 * [today](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3958771161) **MartinJohns** clarified the runtime semantics difference between the optional chaining operator and the non-null assertion operator
 * [today](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3959094360) **nmain** said "If that's how you feel, there's a lint rule for this: https://typescript-eslint.io/rules/no-non-null-asserted-optional-chain"
 * [today](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3960302693) **Chklang** asked why the linter wasn’t integrated into the TypeScript compiler and why optional chaining with non-null assertion isn’t treated as non-null at compile time
 * [today](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3960433164) **MartinJohns** clarified that the null assertion operator indicates ignoring the nullable possibility and reduces type checks
 * [today](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3960760106) **RyanCavanaugh** explained that disallowing non-null assertions when undefined/null wasn’t in the operand would render the operator pointless and illustrated using `a?.b!` to satisfy an incorrectly declared function signature
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Declined`

### [Issue microsoft/TypeScript#63192](https://github.com/microsoft/TypeScript/issues/63192) (Open, `Bug`, `Domain: check: Type Circularity`)

**RangeError: Maximum call stack size exceeded when trying to infer type of a variable reassigned in a loop**

*TypeScript crashes with a maximum call stack size exceeded error when inferring types for a variable reassigned in a loop.*

 * created by **afarnsworth-valve**
 * [today](https://github.com/microsoft/TypeScript/issues/63192#issuecomment-3962608814) **RyanCavanaugh** provided a simplified reproducer that repros in TS7
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63193](https://github.com/microsoft/TypeScript/pull/63193) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] merge iterable decls in DOM**

*Experimentally merge iterable declarations in the TypeScript DOM library generator in preparation for pull request 2431*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63193#issuecomment-3962813671) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63193#issuecomment-3962814457) **typescript-bot** posted CI job status updates for various test commands
 * [today](https://github.com/microsoft/TypeScript/pull/63193#issuecomment-3962909833) **typescript-bot** reported DT test errors for the w3c-css-typed-object-model-level-1 and resize-observer-browser packages
 * [today](https://github.com/microsoft/TypeScript/pull/63193#issuecomment-3962928246) **typescript-bot** reported test results comparing main and the pull request merge and noted infrastructure failures and new type errors in effect and puppeteer-core
 * [today](https://github.com/microsoft/TypeScript/pull/63193#issuecomment-3963040036) **typescript-bot** provided the requested performance run results for the PR
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63193#issuecomment-3963099870) **typescript-bot** reported build failures in top 400 repos comparing main and the pull request, highlighting errors in react-window, RSSNext/Folo, and tldraw

### [Issue microsoft/TypeScript#63194](https://github.com/microsoft/TypeScript/issues/63194) (Open, `Suggestion`, `Awaiting More Feedback`)

**🚀 Proposal: Cross\-Context Function Annotation \(for APIs like \`page\.evaluate\` of playwright\)**

*Introduce an isolated function annotation for cross-context APIs like page.evaluate to prevent closure captures and invalid global access.*

 * created by **jogibear9988**
 * [later](https://github.com/microsoft/TypeScript/issues/63194#issuecomment-3966878590) **nmain** observed that Playwright's function stringification and custom evals in a separate environment are too specialized for TypeScript to model
 * [later](https://github.com/microsoft/TypeScript/issues/63194#issuecomment-3967379989) **jogibear9988** asked whether React's "use server"/"use client" directive was similar

### [Issue microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195) (Open, `Needs More Info`)

**Debug Failure: "No error for last overload signature" crash when CustomTypeOptions\.resources uses typeof on a large \(~10k line\) JSON file**

*TypeScript crashes with 'No error for last overload signature' when using typeof on a large JSON for i18next CustomTypeOptions.resources.*

 * created by **shahanahmed86**

### [Issue microsoft/TypeScript#7770](https://github.com/microsoft/TypeScript/issues/7770) (Open, `Suggestion`, `Needs Proposal`)

**add a modifier for pure functions**

*Add a pure modifier to guarantee functions are immutable and side-effect-free*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/7770#issuecomment-1107645568) **brundonsmith** announced starting work on a TS-like language enforcing function purity and shared its GitHub link
 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/7770#issuecomment-3049412038) **ackvf** noted that the discussion was bogged down in edge cases and expressed a desire for a mechanism to denote functions that only operate on parameters without accessing closures, and commented on readonly parameters and side-effect arguments not breaking purity
 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/7770#issuecomment-3303866904) **yonootz321** suggested extending the pure keyword with capability support similar to Hack contexts and provided example code
 * [later](https://github.com/microsoft/TypeScript/issues/7770#issuecomment-3967159952) **andyearnshaw** argued that TypeScript could infer function purity without new syntax, discussed React memoization workarounds with default frozen arrays, and suggested read-only types by default

