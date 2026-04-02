# Report for 2026-02-24 (Tuesday, February 24th, 2026)

13 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @54145a reported that TS2611 is raised when overriding an @abstract property with accessors in [microsoft/TypeScript#17227](https://github.com/microsoft/TypeScript/issues/17227#issuecomment-3959317844)
    * @erictheswift asked about when the RC/test build would arrive and whether a current dev build qualifies in [microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3959254158)
    * @adhnannp asked to be assigned the issue in [microsoft/TypeScript#63149](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3957875823)

## Activity Summary

### [Issue microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`, `Fix Available`)

**Array\.isArray type narrows to any\[\] for ReadonlyArray\<T\>**

*Array.isArray fails to correctly narrow a union including ReadonlyArray<T>, resulting in an any[] type instead of ReadonlyArray<T>.*

 * [46 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-2787918238) **oconnorjoseph** said "Our team just ran into this issue with the readonly keyword as well. We would very much appreciate for this to work natively."
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3784982171) **spalt08** offered another workaround using Array.isArray to define a readonly array type guard
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3786996167) **cahnory** provided an alternative workaround using a type assertion for Array.isArray
 * [later](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3958701606) **niklasholm** suggested using `unknown` and augmenting ArrayConstructor.isArray via global declaration to avoid `any` or type assertions

### [Issue microsoft/TypeScript#17227](https://github.com/microsoft/TypeScript/issues/17227) (Open, `Suggestion`, `Domain: JavaScript`, `Experience Enhancement`)

**Support \`@abstract\` JSDoc tag**

*TypeScript nightly does not enforce the @abstract JSDoc tag, allowing instantiation of classes marked abstract without error.*

 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/17227#issuecomment-1011535497) **sandersn** said "@trusktr I didn't think to see how many people were creating abstract classes/methods without using @abstract. Can you describe how your code indicates abstractness?"
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/17227#issuecomment-1729909551) **dec0dOS** said "Any updates on this?  Is there a way to retrieve the content from https://github.com/microsoft/TypeScript/pull/42186?"
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/17227#issuecomment-1730719728) **trusktr** described using a base-class method that throws an error to indicate abstractness and expressed a preference for terser type and doc comments over JSDoc
 * [later](https://github.com/microsoft/TypeScript/issues/17227#issuecomment-3959317844) **54145a** reported that TS2611 was still raised when overriding an @abstract JSDoc property with a getter/setter pair and suggested that full @abstract support would suppress the error

### [Issue microsoft/TypeScript#62963](https://github.com/microsoft/TypeScript/issues/62963) (Open, `Meta-Issue`)

**Transition to 6\.0 Maintenance Mode**

*TypeScript 6.0 is entering maintenance mode with only critical fixes, deprecations, and compatibility changes accepted to accelerate the transition to the Go-based 7.0 release.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3787149661) **KnorpelSenf** asked whether regressions from 4.7 to 4.8 and imported bugs would be fixed after the 7.0 release
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3842750039) **RyanCavanaugh** said "@KnorpelSenf yep!"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3940657202) **jogibear9988** asked whether there was a plan for a WASM version of TypeScript 7.0 and how it would integrate into the Monaco editor or client-side websites
 * [today](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3956082889) **RyanCavanaugh** said "WASM is definitely possible. The perf today is not super -- about on par with the JS codebase -- but it would hopefully get better over time as Go and/or browsers get better at it."

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868770106) **typescript-bot** reported build jobs starting and provided links to status and results
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868792183) **typescript-bot** said "Hey, @DanielRosenwasser! I've created release-6.0 with version 6.0.0-beta for you."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3944591376) **HolgerJeromin** noted that the PR also deprecated --module=none and questioned whether it is less-used in the wild
 * [later](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3959254158) **erictheswift** asked about updates on the RC/test build arrival and whether an existing dev build could be considered test-quality

### [Issue microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add switch to disable \_var unused variable prevention**

*Add a tsconfig option to disable automatic ignoring of underscore-prefixed unused variables so the compiler still reports them to IDE.*

 * (yesterday) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3947344632) **guillaumebrunerie** suggested two possible solutions by renaming the variable or enabling the @typescript-eslint/no-unused-vars rule and provided a playground link and screenshot
 * [today](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3953666515) **ackvf** explained their confusion about eslint unused-variable settings and justified making IDE prefix handling configurable
 * [today](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3957255323) **guillaumebrunerie** explained that TypeScript errors and ESLint warnings both appear and suggested disabling noUnusedLocals and noUnusedParameters to rely solely on ESLint for consistent styling

### [Issue microsoft/TypeScript#63149](https://github.com/microsoft/TypeScript/issues/63149) (Open)

**\[TS\]: Incorrect handling of \`JSDoc\` description of interface property**

*VS Code incorrectly strips parentheses-enclosed JSX tags from interface property JSDoc descriptions in hover tooltips.*

 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3940793235) **darshjme-codes** said "Triage: JSDoc description handling bug Labels: Bug, JSDoc, Language Service | Impact: Documentation display issues in editors"
 * [later](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3957875823) **adhnannp** said "i will work on this, could you assign this to me @psnet "

### [Issue microsoft/TypeScript#63150](https://github.com/microsoft/TypeScript/issues/63150) (Open, `Suggestion`, `Experience Enhancement`)

**\[JavaScript/TypeScript Language Hints\] Hide default \`Function\` properties/methods until manually typed just like in Rust\.**

*Add an option to hide default Function properties in JavaScript/TypeScript code completions until manually typed.*

 * created by **FrameMuse**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63150#issuecomment-3953420539) **RyanCavanaugh** suggested picking up the feature for classes in TS7 since it was already done for Object but not functions
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Experience Enhancement`

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922816633) **Arlen22** said "Adding the offending file (prisma.config.ts) to my project tsconfg.json file also seems to be fixing it. "
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922834193) **Arlen22** provided additional log entries that might be relevant
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3946105193) **Arlen22** noted that the issue occurred with any external file, provided environment details, and asked how to measure project size
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63152](https://github.com/microsoft/TypeScript/issues/63152) (Closed, `Duplicate`)

**\.call selects the wrong overload, resulting in ts2554**

*Using .call on XMLHttpRequest.prototype.open incorrectly selects the longer overload and triggers a TS2554 error.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3920845934) **nmain** suggested augmenting the Function type with fake variadic overloads and provided a Playground link and code snippet
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3922916941) **jcalz** suggested widening xhrOpen's type using an intermediate variable and provided example code
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3923237925) **joshcartme** thanked everyone and complimented @jcalz's solution, then suggested closing the issue
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63159](https://github.com/microsoft/TypeScript/issues/63159) (Open, `Bug`, `Domain: LS: TSServer`)

**False positive "Private field \.\.\. must be declared in an enclosing class\."**

*VS Code wrongly reports private field must be declared errors in a second JavaScript file due to cross-tab state pollution.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3924091663) **bkatzung** said ""
 * **mjbvz** unassigned **mjbvz**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3940793141) **darshjme-codes** said "Triage: False positive "Private field must be initialized" Labels: Bug, Strictness, Private Fields | Type: Control flow analysis gap"
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63160](https://github.com/microsoft/TypeScript/issues/63160) (Closed, `Duplicate`)

**Inferring from setter returns getter value**

*TypeScript's conditional type inference picks the getter's return type instead of the setter's parameter type.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3926391137) **MartinJohns** said "Duplicate of #62943."
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3928849152) **LukeAbby** clarified that issue #62943 had been closed as a duplicate of #60162, #43729, and #60954, none involving infer, and noted that #60162 suggested adding a new intrinsic for dynamic props
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3928911901) **MartinJohns** clarified that the first issue involved infer and was marked as a duplicate by a team member
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63161](https://github.com/microsoft/TypeScript/issues/63161) (Closed, `Suggestion`, `Declined`)

**Make compiler option values case sensitive**

*Propose deprecating and removing case-insensitive compiler option values to enforce consistent casing in tsconfig.json.*

 * created by **remcohaszing**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63161#issuecomment-3940793095) **darshjme-codes** said "Triage: Compiler option values case sensitivity Labels: Suggestion, Compiler Options, Breaking Change | Impact: Would require major version"
 * [today](https://github.com/microsoft/TypeScript/issues/63161#issuecomment-3953304340) **RyanCavanaugh** said "@darshjme-codes don't do this"
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Declined`
 * [today](https://github.com/microsoft/TypeScript/issues/63161#issuecomment-3953325484) **RyanCavanaugh** rejected the JSON schema argument and argued that writing separate schema descriptions for NodeNext and nodenext was sufficient and that breaking half of existing config files lacked sufficient upside
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63162](https://github.com/microsoft/TypeScript/issues/63162) (Closed, `Duplicate`)

**Module resolution: Extension required when moduleResolution=bundler and imports/exports used**

*TypeScript's bundler moduleResolution requires explicit .js extensions for imports and exports, causing build-time failures despite working in Vite.*

 * created by **polson136**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3940793062) **darshjme-codes** said "Triage: Module resolution error requiring extension Labels: Bug, Module Resolution, Suggestion | Context: ESM/CJS interop issue"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3941291226) **MartinJohns** said "@darshjme-codes Please don't let your AI trash script run on this repository, spamming issues with pointless comments."
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue
 * (today) **andrewbranch** added label `Duplicate`, removed label `Needs Investigation`, and unassigned **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3953610741) **andrewbranch** argued that '#src/imported-file' is not a relative path and that naming a resolution mode 'bundler' is problematic because bundlers differ, so TypeScript should follow the Node.js spec

### [Issue microsoft/TypeScript#63173](https://github.com/microsoft/TypeScript/issues/63173) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: Maximum call stack size exceeded when declare const enum has a computed property named \[object\] followed by an object member**

*The compiler overflows the call stack when a const enum has a computed [object] member followed by an object member.*

 * created by **na7ure-a**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63173#issuecomment-3938428643) **knowltonn287-source** posted a code snippet illustrating a const enum with conflicting member names
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63173#issuecomment-3940793033) **darshjme-codes** said "Triage: Stack overflow crash Labels: Bug, Crash, Compiler | Priority: High (crashes prevent compilation)"
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63182](https://github.com/microsoft/TypeScript/pull/63182) (Open, `For Backlog Bug`)

**Fixed a crash related to computed enum member keys**

*Fix crash from computed enum member keys by checking non-dynamic names instead of bindable names*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63182#issuecomment-3942796818) **jakebailey** said "Can you explain the fix?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63182#issuecomment-3943375100) **Andarist** said "@jakebailey sure, edited the PR summary"
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63185](https://github.com/microsoft/TypeScript/issues/63185) (Open, `Bug`, `Domain: Source Maps`, **weswigham**)

**tsgo producing source maps that cause functions to appear uncovered in tests**

*tsgo 7.0.0-dev’s generated source maps unexpectedly include inline sources, causing code coverage tools to misreport covered functions as uncovered.*

 * created by **isaacs**
 * (today) **RyanCavanaugh** added label `Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#63190](https://github.com/microsoft/TypeScript/pull/63190) (Closed, `For Uncommitted Bug`)

**discrete pluralizer for lib\.esnext\.temporal unit unions**

*Restrict DateUnit and TimeUnit unions to singular names and use a pluralizer helper for js-temporal compatibility.*

 * created by **Renegade334**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3952317584) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3954299849) **Renegade334** provided a link to the relevant type definition in the polyfill
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3954356867) **jakebailey** said "Ah, but the mapped type doesn't exist?"
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3954648935) **Renegade334** noted that a T | PluralUnit<T> union was used wherever plurals appear and that the bikeshed remained open

### [Issue microsoft/TypeScript#63191](https://github.com/microsoft/TypeScript/issues/63191) (Closed, `Suggestion`, `Declined`)

**The "?" operator would be forbidden before the "\!" operator**

*Request to disallow combining optional chaining (?) with non-null assertion (!) in TypeScript to prevent unsafe undefined values.*

 * created by **Chklang**
 * [later](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3958771161) **MartinJohns** clarified the runtime semantics difference between the optional chaining operator and the non-null assertion operator
 * [later](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3959094360) **nmain** said "If that's how you feel, there's a lint rule for this: https://typescript-eslint.io/rules/no-non-null-asserted-optional-chain"

