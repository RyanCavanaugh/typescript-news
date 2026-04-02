# Report for 2025-12-08 (Monday, December 8th, 2025)

25 different users commented on 42 different issues.

## Recommended Actions

 * Response Recommended
    * @BlueNebulaDev asked for assistance implementing capabilities as methods in derived classes in [microsoft/TypeScript#48125](https://github.com/microsoft/TypeScript/issues/48125#issuecomment-3632610169)
    * @Ashish-Ban asked how to configure pnpm projects in VSCode to use the workspace TypeScript version in [microsoft/TypeScript#51684](https://github.com/microsoft/TypeScript/issues/51684#issuecomment-3627842765)
    * @Ashish-Ban provided a solution to use an absolute typescript.tsdk path to resolve symlink issues in [microsoft/TypeScript#51684](https://github.com/microsoft/TypeScript/issues/51684#issuecomment-3627929765)
    * @guest271314 asked how to reliably check TypeScript types given broken TypeScript implementation in [microsoft/TypeScript#62240](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3632852166)
    * @a-non-a-mouse reported type loading order issue and offered to provide a sample repository in [microsoft/TypeScript#62849](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628921409)
    * @a-non-a-mouse provided a sample repository link in [microsoft/TypeScript#62849](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628980514)

## Activity Summary

### [Issue microsoft/TypeScript#15562](https://github.com/microsoft/TypeScript/issues/15562) (Closed, `Bug`, `VS Code Tracked`, `Domain: LS: Quick Fixes`, `7.0 LS Migration`)

**Filling in an implementation using VS Code will expand types**

*VS Code’s quick fix for implementing interfaces replaces a tuple type alias with its expanded literal tuple in method signatures*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/15562#issuecomment-3604485578) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (6 days ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/15562#issuecomment-3629009561) **mjbvz** said "Looks like the implement interface quick fix hasn't been ported yet. Opened https://github.com/microsoft/typescript-go/issues/2280 to track this"

### [Issue microsoft/TypeScript#30919](https://github.com/microsoft/TypeScript/issues/30919) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: shorthand for templated type to extend and default to the same type**

*Add shorthand syntax to declare generic parameters that both extend and default to the same type using 'is' or similar.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3618369276) **bimocd** expressed support for the feature request and noted surprise at lack of response after six years
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3618603965) **RyanCavanaugh** said "There are nearly 3,000 open suggestions, you can't really expect all of them to be in the language. The documentation would be the size of an encyclopedia."
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3618885329) **bimocd** criticized the dismissive reply and defended the suggestion as a simple extension of TypeScript’s existing philosophy
 * [today](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3628508099) **RyanCavanaugh** said "I don't really know you were going for with "Weird even after 6 years, no answer from anyone". What answer was expected, if not to add the feature?"
 * [today](https://github.com/microsoft/TypeScript/issues/30919#issuecomment-3628758057) **bimocd** clarified what they meant by 'no answer in 6 years' and why they were surprised at the lack of discussion

### [Issue microsoft/TypeScript#47044](https://github.com/microsoft/TypeScript/issues/47044) (Closed, `Bug`, `Domain: LS: Smart Indentation`, `7.0 LS Migration`)

**Method signature completion doesn't respect the custom indent size**

*Method signature completion ignores the two-space indentation setting and inserts six spaces instead of four.*

 * (6 days ago) **RyanCavanaugh** closed the issue
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/47044#issuecomment-3604512728) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * [today](https://github.com/microsoft/TypeScript/issues/47044#issuecomment-3628997143) **mjbvz** said "Looks like method snippet completions haven't been ported over yet: https://github.com/microsoft/typescript-go/issues/2279"

### [Issue microsoft/TypeScript#48125](https://github.com/microsoft/TypeScript/issues/48125) (Open, `Suggestion`, `In Discussion`)

**Allow mapped type to declare functions**

*Allow TypeScript mapped types to declare instance method signatures, enabling definitions like handleDog and handleCat.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/48125#issuecomment-2306570359) **BalaM314** said "Same issue, would be nice to just remove that error."
 * [38 weeks ago](https://github.com/microsoft/TypeScript/issues/48125#issuecomment-2714974063) **robbyemmert** said "Does anyone have a workaround?"
 * [38 weeks ago](https://github.com/microsoft/TypeScript/issues/48125#issuecomment-2715037365) **BalaM314** suggested using multiple inheritance and provided a TypeScript playground link
 * [later](https://github.com/microsoft/TypeScript/issues/48125#issuecomment-3632610169) **BlueNebulaDev** described their contrived capabilities use case and mentioned inability to implement capabilities as methods in derived classes due to the issue

### [Issue microsoft/TypeScript#51684](https://github.com/microsoft/TypeScript/issues/51684) (Open, `Needs Investigation`)

**TypeScript type resolve fails for symlinked folders \(pnpm\)**

*VSCode fails to resolve TypeScript types in pnpm symlinked packages, causing missing definitions in react-router-dom.*

 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/51684#issuecomment-1546698597) **xania** asked for a workaround to avoid VS Code restart after symlinked dependency updates and later noted restarting the TypeScript server as an improved solution
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/51684#issuecomment-1546733948) **kamnakis** said "My issue seems to be fixed with Typescript v5.04"
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/51684#issuecomment-1546736545) **xania** reported that the issue still persisted with Typescript v5.04
 * [today](https://github.com/microsoft/TypeScript/issues/51684#issuecomment-3627842765) **Ashish-Ban** reported that the issue still existed and asked how to get pnpm projects in VSCode to use the workspace TypeScript version
 * [today](https://github.com/microsoft/TypeScript/issues/51684#issuecomment-3627929765) **Ashish-Ban** advised using an absolute path for typescript.tsdk in VSCode to resolve symlink issues and described steps to restart the TypeScript server

### [PR microsoft/TypeScript#56182](https://github.com/microsoft/TypeScript/pull/56182) (Closed, `For Uncommitted Bug`, **rbuckton**)

**Include source node inferences in string literal completions deeper in arguments**

*Expand string literal completions to include source node inferences for nested function arguments.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/56182#issuecomment-2676740209) **Andarist** said "@jakebailey with 2 approvals, could this land now? :)"
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/56182#issuecomment-3609378029) **jakebailey** said "@Andarist Can you merge main so CI is fresh?"
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/56182#issuecomment-3611816868) **Andarist** said "@jakebailey done"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#56429](https://github.com/microsoft/TypeScript/pull/56429) (Closed, `For Uncommitted Bug`, **jakebailey**)

**Consistently return \`errorType\` when detecting circularities**

*Ensure the TypeScript compiler consistently returns an errorType when detecting circularities.*

 * [2 years ago](https://github.com/microsoft/TypeScript/pull/56429#issuecomment-1814958307) **jakebailey** confirmed liking both the targeted `if` in #56258 and the general approach
 * [2 years ago](https://github.com/microsoft/TypeScript/pull/56429#issuecomment-1815086938) **typescript-bot** reported that the top-repos suite comparisons between main and the PR passed successfully
 * **sandersn** assigned to **jakebailey**
 * (today) **Andarist** closed the issue

### [Issue microsoft/TypeScript#58930](https://github.com/microsoft/TypeScript/issues/58930) (Closed, `Bug`, `Domain: LS: Refactorings`, `Fix Available`, `7.0 LS Migration`, **iisaduan**)

**Convert params to destructed object: Cannot apply refactoring **

*Convert params to destructured object code action cannot be applied to the static wrap method in buffer.ts.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/58930#issuecomment-3604493925) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * (6 days ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/58930#issuecomment-3628834548) **mjbvz** added context that the 'Convert params to destructed object' refactoring likely wouldn't be part of tsgo, suggested exploring Copilot-based refactorings, and opened issue #2281 to track it

### [Issue microsoft/TypeScript#58944](https://github.com/microsoft/TypeScript/issues/58944) (Open, `Discussion`)

**Isolated Declarations in TS 5\.5: State of the feature**

*A status update on TypeScript 5.5’s experimental --isolatedDeclarations flag, outlining its current stability, effects, and usage guidance.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3192348561) **kirkwaiblinger** explained that using a numeric literal works whereas Infinity relies on a global, and provided a playground link
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3197456987) **dynst** suggested adding documentation for the feature and noted issues with number and RegExp literal type inference
 * [yesterday](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3622389790) **XantreDev** asked what constituted the simple case for isolatedDeclarations and why RegExp literals were excluded from AST-level inference
 * [today](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3628489902) **RyanCavanaugh** explained that the type name RegExp could be locally shadowed and that always emitting globalThis.RegExp would be correct but ugly

### [PR microsoft/TypeScript#60005](https://github.com/microsoft/TypeScript/pull/60005) (Open, `For Backlog Bug`)

**Add source mappings for serialized properties with available declaration**

*Enable generating source mappings for serialized properties in output files when their declarations exist*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3554914218) **jakebailey** requested merging main and inquired about porting to the Go codebase
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3620601531) **dbrxnds** said "Should there be an issue opened in the native repo to track this for the go port? We recently switched to go but would like for this to stick. "
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3620721369) **Andarist** synced the branch with main, noted no issues porting to the Go codebase, offered to prepare a porting PR, and asked about existing test infrastructure
 * [today](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3629396621) **jakebailey** said "We have declaration map tests and go to def baselining, so theoretically it should all be there."
 * [today](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3629398877) **jakebailey** said "But, I don't know what the equivalent to projectReferencesSourcemap.ts is in the Go codebase; maybe @sheetalkamat knows."
 * [today](https://github.com/microsoft/TypeScript/pull/60005#issuecomment-3629440369) **sheetalkamat** said "you should be able to add fourslash test. https://github.com/microsoft/typescript-go/blob/main/internal/fourslash/tests/statedeclarationmaps_test.go"

### [Issue microsoft/TypeScript#61247](https://github.com/microsoft/TypeScript/issues/61247) (Closed, `Duplicate`)

**Unexpected Auto\-Completion Behavior in Type Inference**

*TypeScript’s auto-complete incorrectly restricts transition target suggestions to only the initial state’s key while other states show all keys.*

 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/61247#issuecomment-2686582477) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (40 weeks ago) **typescript-bot** closed the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#61359](https://github.com/microsoft/TypeScript/pull/61359) (Closed, `Author: Team`, `For Uncommitted Bug`, **gabritto**)

**Bring back return type narrowing \+ fixes**

*Restore conditional and indexed return type narrowing while restricting narrowing to primitive types to avoid ambiguous distinctions.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/61359#issuecomment-2744327730) **gabritto** listed tasks to add tests with `typeof param` as a way of accessing the narrowable type parameter and to support parameter properties
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/61359#issuecomment-3226083554) **lgenzelis** said "hi! Not sure where it's the right place to ask this, but are you planning on having this feature re-added in the foreseeable future? Or did you decide to de-prioritize it because of the go port? :) "
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/61359#issuecomment-3226568573) **controversial** quoted discussion about prioritizing conservatism for new features while focusing on the port
 * (today) **gabritto** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/61359#issuecomment-3628656968) **controversial** praised gabritto's work and expressed hope for landing it in Corsa soon

### [Issue microsoft/TypeScript#61862](https://github.com/microsoft/TypeScript/issues/61862) (Open, `Bug`, `Help Wanted`, `Domain: Decorators`)

**Class decorators run before class static side is fully defined when downleveling**

*Decorators for classes in downleveled TypeScript execute before static fields are set, causing decorators to see undefined values.*

 * (25 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Decorators`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/61862#issuecomment-3632036122) **miyaokamarina** explained the correct behavior of decorator and class static initialization order and illustrated it with example code

### [PR microsoft/TypeScript#62189](https://github.com/microsoft/TypeScript/pull/62189) (Closed, `For Uncommitted Bug`)

**Add tests for contextual param type assignment in nested return type inference scenarios**

*Add tests verifying nested return type inference correctly assigns contextual parameter types following PR 61668.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62189#issuecomment-3628241953) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62240](https://github.com/microsoft/TypeScript/issues/62240) (Open, `Docs`)

**Revert ts5\.9 changes for Uint8Array**

*Revert TypeScript 5.9’s generic Uint8Array type changes because they break compatibility with older TS versions.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3624527695) **bradthomasbrown** expressed confusion about TypeScript's default generic types conflicting and suggested alternative default strategies
 * [today](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3627188690) **snarbles2** argued that TypeScript should keep the default generic argument for Uint8Array as ArrayBufferLike, recommended against option A, noted limited appetite for further breaking changes, suggested making the constructor less precise to improve inference, and explained why defaulting to ArrayBuffer would hinder function parameter acceptance
 * [today](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3627644579) **bradthomasbrown** suggested adding a remark to clarify default type parameter differences in TypedArrays to make the error more intuitive
 * [today](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3628370449) **darksabrefr** critiqued the default use of Uint8Array<ArrayBufferLike> and argued that it should be represented as a distributed union of Uint8Array<ArrayBuffer> and Uint8Array<SharedArrayBuffer> based on predominance of real-world usage and TS generics limitations
 * [today](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3628496569) **paulmillr** said "Yeah, I think like 95-99% of all code is ArrayBuffer and not SharedArrayBuffer."
 * [today](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3628745149) **snarbles2** disagreed with using the most-used value as the default, argued that less precise typing is preferable to precise but inaccurate typing, and suggested manual annotations for edge cases
 * [later](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3632540616) **guest271314** clarified that typed arrays can't change their underlying ArrayBuffer unless it's resizable and noted TypeScript's late support for resizable ArrayBuffer types
 * [later](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3632812751) **darksabrefr** clarified that the underlying buffer type remained fixed at construction even for resizable ArrayBuffers
 * [later](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3632841425) **guest271314** stated that Bun didn't use tsc to convert TypeScript to JavaScript and demonstrated ArrayBuffer resizing behavior
 * [later](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3632852166) **guest271314** questioned how to reliably check Microsoft TypeScript types for Uint8Array given a broken TypeScript implementation

### [PR microsoft/TypeScript#62243](https://github.com/microsoft/TypeScript/pull/62243) (Closed, `For Uncommitted Bug`)

**Improve inference by not considering thisless functions to be context\-sensitive**

*Treat object literal methods that don’t reference ‘this’ as non-context-sensitive to improve TypeScript’s type inference and fix related issues.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3181937558) **typescript-bot** reported build errors in several repositories and asked for review
 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3184893222) **Andarist** said "I consider this PR to be fully review-ready now. I commented on the "breaks" above here: https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3172488072 . "
 * **jakebailey** added to milestone `TypeScript 6.0`
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628641857) **jakebailey** requested the TypeScript bot to test and pack
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628642039) **typescript-bot** reported CI jobs started and provided links to their results
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628671618) **typescript-bot** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628672528) **typescript-bot** notified that the DT test run failed and asked to check the log
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628742756) **jakebailey** requested the TypeScript bot to test and pack
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628742983) **typescript-bot** reported statuses of CI jobs with links to build results
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628755699) **typescript-bot** provided installable tgz, playground, and npm module links for testing the TypeScript 6.0.0 insiders build
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628812893) **typescript-bot** reported that DT tests for jqrangeslider failed due to a missing return-type annotation
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628836082) **typescript-bot** ran user tests comparing main and the PR merge, reported one Git clone failure and otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3628919914) **typescript-bot** reported the perf run results requested by @jakebailey
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3629024365) **typescript-bot** reported tsc performance comparison results and noted a build error in steven-tey/novel
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3629456734) **Andarist** said "@gabritto in case you have missed it, I commented on the breaks here"
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3629464729) **jakebailey** said "The perf run shows 5 new errors in vscode; I am not sure why they are not showing up in the top or user tests..."
 * [today](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3629485744) **Andarist** said "@jakebailey thanks for noticing, I'll look into it"
 * [later](https://github.com/microsoft/TypeScript/pull/62243#issuecomment-3632609139) **Andarist** mentioned that PR #282223 should address the VS Code break and proposed a performant version of PR #57421 as a general fix, noting his local prototype was out of scope and only partial

### [PR microsoft/TypeScript#62361](https://github.com/microsoft/TypeScript/pull/62361) (Closed, `For Uncommitted Bug`)

**Make go to definition go to the constraint's properties for object literals in argument positions**

*Enhance the go-to-definition feature to jump from object literals used as arguments directly to their constraint properties.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/62361#issuecomment-3617672118) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Open, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3423408127) **typescript-bot** reported tsc performance comparison results
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3423437591) **bakkot** demonstrated a TypeScript pattern to enforce the “at least one of” constraint for DateLikeObject while cautioning about added complexity
 * [7 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3423494989) **typescript-bot** reported that everything looked good when comparing TypeScript compiler results on the top 400 repos between main and the pull request merge
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3629347917) **jakebailey** said "I know there are existing polyfills for Temporal out there in TS; are these types compatible / based off of those? Or fresh?"
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3629743678) **Renegade334** noted that definitions were de novo with no licensing issues and observed that temporal-polyfill and @js-temporal/polyfill were incompatible with lib.d.ts patterns, offering to run interoperability tests

### [Issue microsoft/TypeScript#62705](https://github.com/microsoft/TypeScript/issues/62705) (Closed, `Docs`, **RyanCavanaugh**)

**FAQ on module specifier rewriting is outdated**

*The TypeScript FAQ's assertion that import specifiers remain unchanged is outdated because v5.7's rewriteRelativeImportExtensions now modifies them.*

 * (5 weeks ago) **RyanCavanaugh** added label `Docs`, and assigned to **RyanCavanaugh**
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62705#issuecomment-3488297225) **RyanCavanaugh** said "🤖 This is an automated response. I looked for things that might help (duplicates, FAQ entries, etc) but didn't find anything. A human will take a look!"
 * [today](https://github.com/microsoft/TypeScript/issues/62705#issuecomment-3628779828) **mkantor** said "I proposed an edit in microsoft/TypeScript-wiki#350."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844) (Closed, `For Milestone Bug`)

**Allow subpath imports that start with \`\#/\`**

*Allow subpath imports starting with '#/' in package.json imports to mirror matching exports entries.*

 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627409807) **andrewbranch** said "Yeah, technically this shouldn’t go in node16. @magic-akari can you gate this on moduleResolution === ModuleResolutionKind.NodeNext?"
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627521315) **Scalahansolo** said "Shouldn't this also work with moduleResolution being bundler?"
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627553198) **magic-akari** acknowledged feedback, said they’d gate the feature on NodeNext and Bundler modes, and asked if a new module resolution mode is needed or if gating behind NodeNext is sufficient
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627734308) **andrewbranch** said "I think gating it is fine for now."
 * [today](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627779295) **andrewbranch** recommended snapping the versioned module resolution at `--moduleResolution node20` and waiting for the backports before merging

### [Issue microsoft/TypeScript#62849](https://github.com/microsoft/TypeScript/issues/62849) (Closed, `Not a Defect`)

**The existence of /// reference directives in dependencies breaks explicit typeRoots ordering**

*Dependencies using triple-slash reference directives load their type definitions before custom typeRoots, ignoring explicit typeRoots ordering.*

 * created by **a-non-a-mouse**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628350267) **RyanCavanaugh** said "I'm not quite sure what you mean by typeRoots ordering being different -- do you mean the order that the types directives get processed? Can you post a sample repo we can look at?"
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628921409) **a-non-a-mouse** described that the /// directive chain was processed before typeRoots, causing @types/node to load before custom types and lead to conflicts, noted that commenting out the vitest import resolved it and that a sample repo would be provided
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628938524) **jakebailey** explained that `typeRoots` only affected resolution of `@types`, noted that types were loaded in reverse dependency order, and suggested avoiding conflicts, patching `@types/node`, or configuring Vite
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628972180) **a-non-a-mouse** explained that they couldn't patch @types/node because Vite includes it before their own types, making conflicting interface overrides impossible, and argued that developers should be allowed to patch inaccurate or too-loose types
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628978098) **jakebailey** suggested sending PRs to DefinitelyTyped or discussing in the DT Discord channel and clarified that typeRoots isn't intended to reorder type files and that only lib.d.ts controls compilation order
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628980514) **a-non-a-mouse** said "sample repo: https://github.com/a-non-a-mouse/0194011212380128310923810"
 * [today](https://github.com/microsoft/TypeScript/issues/62849#issuecomment-3628995187) **a-non-a-mouse** explained that Vite would install @types/node even if not installed and load types globally, causing global type injection issues

### [Issue microsoft/TypeScript#62850](https://github.com/microsoft/TypeScript/issues/62850) (Closed, `Not a Defect`)

**Typescript fail to pick up error with Nullish Coalescing Operator**

*TypeScript incorrectly allows using 'something.tagsArray ?? {}' to assign an optional Tag array to a boolean map without error.*

 * created by **brenhub24**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62850#issuecomment-3623876771) **jcalz** explained that TypeScript infers the union of an array literal and an empty object as {} and thus allows assignment to a weak object type due to missing property normalization not applying to arrays
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/62850#issuecomment-3628000323) **RyanCavanaugh** said "This is admittedly annoying, but I don't see a way to fix it without making something else substantially worse"

### [PR microsoft/TypeScript#62851](https://github.com/microsoft/TypeScript/pull/62851) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 3 updates**

*Upgrade actions/checkout to v6.0.1 and update actions/setup-node and github/codeql-action to their latest versions.*

 * **dependabot[bot]** added label `github_actions`
 * (yesterday) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62853](https://github.com/microsoft/TypeScript/issues/62853) (Closed, `Duplicate`)

**Inconsistent behaviour of Record or Enum and mapped type**

*TypeScript’s Record type does not error on missing enum or const-object keys while equivalent mapped types correctly report errors.*

 * created by **ipva3**
 * [today](https://github.com/microsoft/TypeScript/issues/62853#issuecomment-3626744322) **MartinJohns** said "Duplicate of #62796."
 * [today](https://github.com/microsoft/TypeScript/issues/62853#issuecomment-3627388958) **jcalz** identified the duplication of issue #29698 concerning contravariance of Record<K, V>, provided a minimal example, and noted that issue #62796 was misfocused on noUncheckedIndexedAccess
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#62854](https://github.com/microsoft/TypeScript/issues/62854) (Open, `Bug`, `Help Wanted`)

**\`\_\_setFunctionName\` breaks custom static \`name\` on classes**

*TypeScript's __setFunctionName injection unconditionally overrides custom static name properties on decorated and undecorated classes.*

 * created by **miyaokamarina**

### [PR microsoft/TypeScript#62855](https://github.com/microsoft/TypeScript/pull/62855) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix ContextFlags compile error**

*Enable merge queues to resolve a racing PR issue causing ContextFlags compile errors.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/62855#issuecomment-3628553568) **jakebailey** said "The package-size task doesn't work if main can't also build. So I'm just going to force merge this in."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62856](https://github.com/microsoft/TypeScript/pull/62856) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Reenable fail\-fast in merge queues**

*Re-enable fail-fast in merge queues to abort remaining jobs immediately upon the first failure.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62857](https://github.com/microsoft/TypeScript/issues/62857) (Closed, `Not a Defect`)

**JavaScript IntelliSense does not suggest methods added to built\-in prototypes**

*JavaScript IntelliSense in VS Code fails to suggest custom methods added to built-in prototypes like Promise.log.*

 * created by **sangafabrice**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62858](https://github.com/microsoft/TypeScript/issues/62858) (Closed)

**Expand selection should select comment block**

*Expand Selection in VS Code selects the enclosing scope instead of the comment block when caret is inside JavaScript comments.*

 * (13 weeks ago) **hediet** assigned to **mjbvz**, and unassigned **hediet**
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/62858#issuecomment-3629093154) **hediet** identified an issue with smart select and included a screenshot
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62859](https://github.com/microsoft/TypeScript/issues/62859) (Closed)

**Incorrect conversion to async function**

*VS Code’s async conversion quick fix wrongly injects a parameter into a callback that takes none.*

 * created by **johndoknjas**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62859#issuecomment-3629145632) **vs-code-engineering[bot]** suggested upgrading to the latest stable VS Code version and verifying if the issue persists
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62860](https://github.com/microsoft/TypeScript/issues/62860) (Closed, `Question`)

**TypeScript Auto\-Import Fails for Workspace Package in ESM Monorepo with Project References and Specific Dependencies**

*TypeScript's auto-import suggestions fail for local workspace packages in an ESM monorepo when project dependencies are specified.*

 * created by **hosseinalipour**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62861](https://github.com/microsoft/TypeScript/issues/62861) (Closed, `Fixed`)

**overloaded constructors do not show jsdoc of the class**

*VS Code fails to display class-level JSDoc comments when hovering over overloaded TypeScript constructors.*

 * created by **sw6ueyz**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62862](https://github.com/microsoft/TypeScript/issues/62862) (Closed)

**BUG: \`JavaScript\` / \`TypeScript\` / \`tsx\`: Cannot rename variable**

*Pressing F2 to rename JavaScript/TypeScript variables in VS Code shows “No result.” and fails to apply the rename.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/62862#issuecomment-3629383235) **psnet** provided reproduction steps and asked if the same result occurred when pressing F2 on the variable
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62862#issuecomment-3629383247) **psnet** said "still actual @mjbvz "
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62862#issuecomment-3629383257) **psnet** said "@mjbvz ping"
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62863](https://github.com/microsoft/TypeScript/issues/62863) (Closed, `Working as Intended`, **mjbvz**)

**Selecting property in parameter list after selecting property type definition does not highlight usages of that property**

*Selecting a parameter property after its type annotation in VS Code fails to highlight its usages until clicked twice.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/62863#issuecomment-3629515365) **vbeffa** stated the issue had been present across many VS Code releases
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/62863#issuecomment-3629515372) **vbeffa** said "Confirmed this is still an issue in the latest version."
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62864](https://github.com/microsoft/TypeScript/issues/62864) (Closed)

**Regression: vscode complains 'Could not find a declaration file for module' on some symlinks under node\_modules**

*VS Code 1.97.0 on Linux incorrectly flags modules linked via node_modules symlinks as missing declaration files.*

 * created by **myocytebd**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [PR microsoft/TypeScript#62865](https://github.com/microsoft/TypeScript/pull/62865) (Closed, `For Uncommitted Bug`)

**Move knip args**

*Consolidate knip CLI flags into a single config file and remove obsolete ignore tag and entry point.*

 * created by **webpro**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62865#issuecomment-3630200209) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62865#issuecomment-3630200229) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62866](https://github.com/microsoft/TypeScript/issues/62866) (Closed)

**fsfsdfdsf**

*A placeholder feature suggestion template lacking any substantive details or motivating examples.*

 * created by **UsmanFridi**

### [Issue microsoft/TypeScript#62867](https://github.com/microsoft/TypeScript/issues/62867) (Closed, `Duplicate`)

**Add basic types \<Byte\> and \<Integer\>**

*Introduce built-in Byte and Uint8 types in TypeScript to represent 8-bit unsigned integer values instead of manual unions.*

 * created by **bf**
 * [later](https://github.com/microsoft/TypeScript/issues/62867#issuecomment-3631662400) **MartinJohns** said "Duplicate of #195 / #4639."
 * [later](https://github.com/microsoft/TypeScript/issues/62867#issuecomment-3632357625) **bf** noted that the issue duplicated older issues and suggested adding basic integer validation
 * [later](https://github.com/microsoft/TypeScript/issues/62867#issuecomment-3632565729) **jcalz** said "#54925 is the currently-open issue that encompasses this."

### [Issue microsoft/TypeScript#62887](https://github.com/microsoft/TypeScript/issues/62887) (Open, `Needs Investigation`, **sheetalkamat**)

**TS Server Crash Loop: Copilot Chat virtual files \('vscode\-chat\-code\-block'\) trigger infinite Directory Watcher recursion on InferredProject**

*Copilot Chat’s virtual “vscode-chat-code-block” files cause the TypeScript server to enter infinite directory watcher recursion, spike CPU, and crash repeatedly.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644228259) **worldzb** said "same issue"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644228290) **gmz-price** reported that Copilot Chat conflicted with IntelliSense, making work impossible without disabling Copilot Chat, and referenced a previous issue
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644228310) **cleversonferreira** provided steps to unlock VS Code as a workaround until the bug was fixed
 * [later](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644228323) **iErKy** said "Same problem here, @cleversonferreira fix seems to work (Thanks), hopefully this issue gets fixed because it's hard to work like this."

