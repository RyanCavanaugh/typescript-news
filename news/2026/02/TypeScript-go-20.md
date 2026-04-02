# Report for 2026-02-20 (Friday, February 20th, 2026)

14 different users commented on 44 different issues.

## Recommended Actions

 * Response Recommended
    * @aheber asked if tsgo supports a mechanism to intercept write actions for virtual modules during refactoring in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3936221722)
    * @erengeez asked whether the PR would also fix the issue from #2637 in [microsoft/TypeScript-go#2867](https://github.com/microsoft/TypeScript-go/issues/2867#issuecomment-3938629699)

## Activity Summary

### [PR microsoft/TypeScript-go#2195](https://github.com/microsoft/TypeScript-go/pull/2195) (Closed, **jakebailey**, **Copilot**)

**Fix missing JSDoc comments on destructured interface properties**

*Retrieve JSDoc comments from interface properties for destructured binding elements in hover and signature help aligned with TypeScript implementation*

 * created by **Copilot**
 * (11 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2195#issuecomment-3937388968) **jakebailey** said "@copilot pull and merge main in. when you pull, make sure you have done git submodule update as to not accidentally move the submodule backward. on conflicts, git does not update submodules."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2195#issuecomment-3937481152) **Copilot** merged main into the branch, updated the submodule, and resolved conflicts in hover.go and signaturehelp.go incorporating the commentOnly parameter

### [Issue microsoft/TypeScript-go#2574](https://github.com/microsoft/TypeScript-go/issues/2574) (Closed, `Crash`, **andrewbranch**)

**panic: cache entry not found \[recovered, repanicked\]**

*A panic occurs in typescript-go v7.0.0-dev when cloning project snapshots due to a missing cache entry.*

 * created by **joepjoosten**
 * **joepjoosten** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2577](https://github.com/microsoft/TypeScript-go/pull/2577) (Closed)

**Add \-\-release flag to emulate real released binaries, rename build tag to noassert, test release in CI**

*Add a --release flag to produce stripped binaries, rename the build tag to ‘noassert’, and test release builds in CI.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3855769882) **jakebailey** said "Also TODO, going to add a task which actually exercises the release procedure, for CI testing."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3917589117) **DanielRosenwasser** asked where all the build flags are tracked and if they can be toggled ad-hoc
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3918157955) **jakebailey** described the behavior of `noembed` and `noassert` build tags across default, debug, and release build modes and noted other test-related flags
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2649](https://github.com/microsoft/TypeScript-go/issues/2649) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**LSP Panic: strings: negative Repeat count when formatting JSDoc within nested scope**

*The TypeScript LSP server panics with a negative repeat count error when formatting nested JSDoc comments.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2649#issuecomment-3843883710) **DanielRosenwasser** said "Okay, now that it's properly formatted it repros."
 * (2 weeks ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2719](https://github.com/microsoft/TypeScript-go/pull/2719) (Closed, **jakebailey**, **Copilot**)

**Optimize source map character offset calculation with correct UTF\-16 counting**

*Optimize source map offsets by using an O(1) ASCII path and proper UTF-16 code unit counting to improve compile performance.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2719#issuecomment-3937391139) **jakebailey** said "I'm going to close this, I think it's just not helpful in isolation"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2760](https://github.com/microsoft/TypeScript-go/pull/2760) (Closed, **jakebailey**, **Copilot**)

**Error on modules\-as\-namespaces**

*Enforce parsing errors on module namespace declarations, report one error per dotted name, and update code and tests.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3885934528) **DanielRosenwasser** recommended gracefully parsing and issuing a parse error
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3917568878) **jakebailey** said "@copilot this is failing tests, you didn't run the whole suite"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2760#issuecomment-3917636937) **Copilot** fixed the failing tests by updating the test file to use `namespace` instead of `module` to match the submodule version
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * **andrewbranch** added label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3931729619) **shinichy** reported that tsgo got stuck, did not produce a `custom/saveHeapProfile` response in LSP logs, and missed cache statistics information when following reproduction steps
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3931736730) **shinichy** said "@neo773 Are you able to reproduce this issue in https://github.com/twentyhq/twenty/? I couldn't reproduce this issue in the repo."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3936503506) **andrewbranch** said "@shinichy could you try out #2855 and see if that improves things for you?"

### [PR microsoft/TypeScript-go#2793](https://github.com/microsoft/TypeScript-go/pull/2793) (Closed)

**Fixed a formatting crash on comments inside blocks starting on first line**

*Resolve formatting tool crash caused by comments appearing in code blocks starting on the first line.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2813](https://github.com/microsoft/TypeScript-go/pull/2813) (Closed)

**New IPC API client features**

*Updates the TypeScript IPC API client to use immutable snapshots for state and lifecycle management and adds Go support code.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2813#issuecomment-3918014132) **andrewbranch** said "My handling of SourceFileAffectingOptions needs to be updated after Jake's changes in main. I think it wasn't quite right before, anyway."
 * (2 days ago) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2813#issuecomment-3935041074) **JoostK** said "Will the @typescript/ast/@typescript/api packages become available on NPM during the preview phase?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2813#issuecomment-3935994810) **andrewbranch** clarified that those packages would remain in preview until at least compiler version 7.1 and that it was too early to release API package previews

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3932331598) **remcohaszing** questioned how the --build option related, noted that plugin use implies noEmit, and discussed publishing practices for MDX, CSS, SVG, font, image, Astro, and Vue files
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3932403095) **auvred** provided information on using vue-tsc to emit .vue.d.ts files and noted Ember’s expectations for .d.ts files
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3935034341) **remcohaszing** said "I think this highlights another issue. name.vue.d.ts tells TypeScript there’s a file named name.vue.js. The correct name for a declaration file for a file named name.vue, is name.d.vue.ts."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3935891423) **andrewbranch** asked if his understanding of Svelte project service file discovery was correct and if other languages faced similar situations
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3936069400) **chriskrycho** explained that projects adopt TypeScript’s module resolution semantics and likened the necessary tooling transformations to TSX/JSX syntactic shenanigans
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3936221722) **aheber** described two main actions: dynamically modifying the resolved tsconfig to register module paths and lying about non-JS files as importable modules by intercepting read/write operations; explained desire to avoid on-disk declaration files and tsconfig edits while retaining refactoring support; asked if tsgo’s architecture can support intercepting file write actions for virtual modules

### [Issue microsoft/TypeScript-go#2828](https://github.com/microsoft/TypeScript-go/issues/2828) (Closed)

**"panic: Debug failure\. False expression: Token end is child end" in CI**

*CI panics with 'Token end is child end' assertion failure in the TypeScript-Go formatter, and the failing test is unknown.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2828#issuecomment-3937657081) **jakebailey** reported a panic with debug failure 'False expression: Token end is child end' in the TypeScript-go LSP server
 * [today](https://github.com/microsoft/TypeScript-go/issues/2828#issuecomment-3937667202) **jakebailey** said "I think it's TestWhiteSpaceTrimming4."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2828#issuecomment-3937669709) **jakebailey** explained that the panic originated from a sendNotification call that panicked due to a cancellation
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2833](https://github.com/microsoft/TypeScript-go/pull/2833) (Closed)

**Fix infinite forEachChild loop on some nodes in JS API **

*Caching nodes by text position instead of node index causes an infinite forEachChild loop in the JS API.*

 * created by **auvred**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2835](https://github.com/microsoft/TypeScript-go/pull/2835) (Closed)

**6\.4x speedup of AST materialization in JS API**

*Several optimizations in the JavaScript API speed up AST materialization by 6.4× and correct benchmarks by resetting the source file cache.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2835#issuecomment-3928531012) **auvred** suggested adding an opt-in eager materialization after researching tsgo-powered JS lint rules that touch up to 80% of AST nodes and noting that lazy materialization is slower than parsing with Strada
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2835#issuecomment-3928571317) **andrewbranch** said "Yeah, an option to do that would be great! It makes sense that a linter would want to look at the whole file."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2835#issuecomment-3928909689) **auvred** reverted getOrCreateChildAtNodeIndex to lazy materialization after finding performance nearly equivalent to bulk materialization
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2839](https://github.com/microsoft/TypeScript-go/issues/2839) (Closed, `bug`, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**Cannot "go to definition" of a playwright fixture**

*Editors cannot navigate to definitions of custom Playwright fixtures when using tsgo, though TypeScript 6 supports it.*

 * (yesterday) **DanielRosenwasser** added label `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2842](https://github.com/microsoft/TypeScript-go/pull/2842) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix go\-to\-definition for binding elements in ObjectBindingPattern**

*Add and test go-to-definition support for object destructuring binding elements, including rest patterns, and update test baselines accordingly.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2843](https://github.com/microsoft/TypeScript-go/issues/2843) (Closed, **ahejlsberg**)

**Difference in typechecking results for a TSX file in 7\.0\.0\-dev\.20260218\.1 and later**

*A tsgo regression in v7.0.0-dev.20260218.1+ causes Formik onSubmit handler types to mismatch in TSX files, unlike TS 6.0 or earlier tsgo versions.*

 * **jakebailey** assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2843#issuecomment-3930759122) **ahejlsberg** believed the tsgo error was correct and showed the same error occurred with tsc, noted that PR #2803 was merged to fix type inference and align behavior, and said it would be back-ported to TS 6.0
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2843#issuecomment-3931756312) **DanielRosenwasser** said "We're looking to bring this behavior back to 6.0 https://github.com/microsoft/TypeScript/pull/63163"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2843#issuecomment-3937274156) **connorshea** said "Fair, as long as it's backported to 6.0 that's fine by me :) Thanks!"
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2845](https://github.com/microsoft/TypeScript-go/pull/2845) (Closed)

**Codegen sync API and all enums**

*Replace sync API code (types, implementation, tests, benchmarks) with async-generated counterparts and auto-generate TypeScript enums from Go source.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2846](https://github.com/microsoft/TypeScript-go/pull/2846) (Closed)

**Fix emit for non\-local/merged enum/namespace references**

*Fix code emission for non-local and merged enum and namespace references.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2849](https://github.com/microsoft/TypeScript-go/pull/2849) (Closed)

**Fix parse cache key not found**

*Move auto-imports host disposal after marking program files as referenced to prevent missing parse cache keys.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2850](https://github.com/microsoft/TypeScript-go/issues/2850) (Open, **andrewbranch**)

**Add \`\.getNonPrimitiveType\(\)\` getter**

*The API is missing the recently introduced .getNonPrimitiveType() getter that exists in Strada.*

 * created by **mrazauskas**
 * **jakebailey** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2851](https://github.com/microsoft/TypeScript-go/issues/2851) (Open, **andrewbranch**)

**Add \`\.getTrueType\(\)\` and \`\.getFalseType\(\)\` to \`ConditionalType\`**

*Add getTrueType() and getFalseType() methods to ConditionalType so it returns instantiated true and false branch types.*

 * created by **mrazauskas**
 * **jakebailey** assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#2852](https://github.com/microsoft/TypeScript-go/pull/2852) (Closed)

**Fixed an always\-truthy condition in span\`\.go\` \(porting bug\)**

*A condition in span.go was always true due to a porting bug and has been fixed.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2853](https://github.com/microsoft/TypeScript-go/pull/2853) (Closed)

**Implement ES2017 \(async\) transforms**

*Port ES2017 async transforms with improved argument and super detection, native Promise support, and obsolete diff removal.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2854](https://github.com/microsoft/TypeScript-go/issues/2854) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Panic on find\-all\-references \(or documentHighlights\) for string\-renamed export**

*Invoking find-all-references or documentHighlights on an export alias renamed to a string literal panics internally.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **jakebailey**
 * **jakebailey** assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2855](https://github.com/microsoft/TypeScript-go/pull/2855) (Open)

**Share package\.json cache and skip collecting failed lookup locations in auto\-imports**

*Caching package.json and skipping failed lookup locations in auto-imports reduces memory allocation overhead.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#2856](https://github.com/microsoft/TypeScript-go/pull/2856) (Closed, **jakebailey**, **Copilot**)

**Fix panic on find\-all\-references for string\-renamed export**

*Find-all-references panics on string-renamed exports because helper functions assume identifiers, so widen parameter types and remove casts*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2856#issuecomment-3936759973) **DanielRosenwasser** said "I guess this is fine, but it would have been good if this actually tested a real find-all-references scenario..."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2857](https://github.com/microsoft/TypeScript-go/issues/2857) (Open, `Domain: Editor`)

**Formatters get stuck**

*The extension’s LSP-based formatter intermittently hangs during format-on-save on MacOS, never returning a response.*

 * created by **mjbvz**
 * **mjbvz** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2858](https://github.com/microsoft/TypeScript-go/issues/2858) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Panic when fetching variable of ill\-formatted for\-in declaration list**

*A malformed for-in loop without a variable declaration causes a runtime index-out-of-range panic in the TypeScript-Go checker.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2859](https://github.com/microsoft/TypeScript-go/issues/2859) (Open)

**\`gql\.tada\` performing better with \`\-\-singleThreaded\` than without it**

*tsgo without --singleThreaded runs significantly slower than with it when generating gql.tada types due to union caching inefficiencies.*

 * created by **evsasse**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3937207873) **jakebailey** said "I would suggest using --pprofDir . and upload those profiles."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2859#issuecomment-3937281866) **ahejlsberg** noted that expensive type instantiations jumped from 32M in single-threaded mode to 125M in concurrent mode, indicating each of the four type checkers repeated the same work

### [PR microsoft/TypeScript-go#2860](https://github.com/microsoft/TypeScript-go/pull/2860) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic in \`getForInVariableSymbol\` for empty for\-in declaration list**

*Guard against empty for-in declaration lists in getForInVariableSymbol to prevent index-out-of-range panics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2861](https://github.com/microsoft/TypeScript-go/pull/2861) (Closed)

**Implement for\-await \(ES2018\) transform, fix existing ES2018 issues**

*Implements ES2018 for-await-of syntax transform and resolves existing ES2018 transform issues*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2862](https://github.com/microsoft/TypeScript-go/pull/2862) (Closed)

**Remove install\-extension task**

*Remove the install-extension task to prevent confusing local VSIX installation scenarios.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2863](https://github.com/microsoft/TypeScript-go/pull/2863) (Closed, **jakebailey**, **Copilot**)

**Unskip 14 passing formatting fourslash tests**

*Re-enable 14 skipped fourslash formatting tests after fixing indentation computation, list guard, and JSDoc reparsing bugs.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2864](https://github.com/microsoft/TypeScript-go/pull/2864) (Closed)

**Enable \`noUncheckedSideEffectImports\` by default**

*Port PR 62443 to enable the noUncheckedSideEffectImports compiler option by default.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript-go#2865](https://github.com/microsoft/TypeScript-go/pull/2865) (Closed)

**Don't panic on failed send in recover**

*Modify recover functions to ignore send errors during cancellation and unskip the associated tests.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2866](https://github.com/microsoft/TypeScript-go/pull/2866) (Closed)

**Fix package\.json file watching**

*Update file watcher to respond to any change in existing package.json files rather than only file creation*

 * created by **andrewbranch**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [Issue microsoft/TypeScript-go#2867](https://github.com/microsoft/TypeScript-go/issues/2867) (Closed, **DanielRosenwasser**, **Copilot**)

**tsgo formatter doesn't format imports the same as TS TS**

*tsgo’s formatter does not reformat multi-line import statements like TypeScript’s built-in formatter, causing commit errors.*

 * created by **connor4312**
 * **connor4312** assigned to **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2867#issuecomment-3937802366) **mjbvz** said "I feel like ts-go may also sometimes creates this style of new lines with its auto imports, even when everything was previously all on one line"
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2867#issuecomment-3937900090) **DanielRosenwasser** noted that Strada previously formatted imports with line breaks, while Corsa now left them as-is
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2867#issuecomment-3938629699) **erengeez** said "Automatic importing with autocomplete or Quick Fix actually adds extra newline as I described in #2637 which creates this exact situation. Will the PR fix it also?"

### [PR microsoft/TypeScript-go#2868](https://github.com/microsoft/TypeScript-go/pull/2868) (Closed)

**Don't process \`@link\` JSDoc tags inside backticks**

*Prevent processing of @link JSDoc tags inside backticks.*

 * created by **ahejlsberg**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [PR microsoft/TypeScript-go#2869](https://github.com/microsoft/TypeScript-go/pull/2869) (Closed, **DanielRosenwasser**, **Copilot**)

**fix: formatter correctly moves \`}\` to new line for multiline import braces**

*Ensure the tsgo formatter places the closing brace on a new line for multiline import statements and update relevant tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#648](https://github.com/microsoft/TypeScript-go/issues/648) (Open, `Domain: API and Extensibility`)

**Support embedded JavaScript/TypeScript**

*Enable built-in handling of embedded JavaScript/TypeScript in languages such as MDX, Vue, Svelte, Astro, and Markdown in the Go rewrite.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3699022588) **ItsHarper** asked why extensions couldn't interoperate and explained that compiler forks can’t interoperate without merging all changes
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3699085966) **auvred** suggested that a unified plugin architecture could allow language extensions to run in separate processes and be written in any language and noted that tsgo would be a nicer plugin host
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3928741504) **andrewbranch** opened a related issue (#2824) and requested expert feedback
 * [today](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3935957954) **silverwind** noted community projects emerging to fill missing embedded language support in tsgo

### [Issue microsoft/TypeScript-go#961](https://github.com/microsoft/TypeScript-go/issues/961) (Closed, `bug`, `Domain: Emit`, `Domain: Type Checking`, **jakebailey**)

**tsgo fails to resolve namespace symbols in non\-extends contexts across files**

*tsgo fails to qualify namespace symbols A and Afunc outside extends contexts across files, causing incorrect JS and runtime errors.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3828862365) **dtscd** shared a proof-of-concept change adding outfile support with sourceMaps and a commit link, asserted it worked for their project and challenged the performance argument
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/961#issuecomment-3837656679) **jakebailey** stated that they wouldn't change the behavior and asked for a PR to correct tsgo
 * **jakebailey** added label `bug`
 * (today) **jakebailey** closed the issue

