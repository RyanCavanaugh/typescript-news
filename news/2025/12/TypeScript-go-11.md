# Report for 2025-12-11 (Thursday, December 11th, 2025)

14 different users commented on 41 different issues.

## Recommended Actions

 * Response Recommended
    * @Knagis provided performance metrics and observations for tsgo 7.0.0-dev.20251212.1 as requested in [microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647019868)
    * @Knagis asked about using an NDA path to share access in [microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647124648)
    * @jfirebaugh provided repro steps as requested in [microsoft/TypeScript-go#2278](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3646839251)
    * @gggdomi asked which commits correspond to the two releases in [microsoft/TypeScript-go#2341](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3642966388)

## Activity Summary

### [Issue microsoft/TypeScript-go#1080](https://github.com/microsoft/TypeScript-go/issues/1080) (Open, `Domain: Program`)

**Deduplicate doubly\-installed packages**

*Duplicated installations of the same npm package across workspaces lead to instances TypeScript tolerates but break Go type compatibility.*

 * [24 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3005503133) **jakebailey** said "I guess a "good thing" is that whatever we do cannot be worse than the current situation, given we already load all files without deduplication and people are happy with the perf."
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3457417471) **chriskrycho** added a real-world example showing that disabling deduplication prevents runtime errors due to unique symbols across dependencies and suggested maintaining the behavior with an opt-in migration flag
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3458576531) **jakebailey** referred to PR 62684 showing minimal breakage, described a potential implementation of a load plus dedupe pass, and expressed preference not to reintroduce the idea
 * [today](https://github.com/microsoft/TypeScript-go/issues/1080#issuecomment-3644998431) **jakebailey** asked users to try building PR #2361 from source to see if it fixed their issues

### [Issue microsoft/TypeScript-go#1622](https://github.com/microsoft/TypeScript-go/issues/1622) (Open, `Crash`, `Domain: Program`, `Domain: Performance`, **sheetalkamat**)

**\[bug\] \`tsgo \-\-build\` uses extreme amounts of memory**

*tsgo --build exhausts over 100GB of memory and crashes when building large monorepos with thousands of TypeScript projects*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3638634504) **jakebailey** requested that they try build mode with `--builders 1`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3638700009) **maxkostow** said "Is that expected to impact the LSP or should there be a separate issue for the LSP?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3638704557) **jakebailey** dismissed that as unrelated to the thread, clarified that build mode wasn't part of the language server, pointed to issue #2239, and suggested filing separate issues for distinct cases
 * [later](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647019868) **Knagis** reported performance metrics and observations for tsgo 7.0.0-dev.20251212.1 using different builder configurations
 * [later](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647062740) **jakebailey** said "Is this codebase public? That definitely sounds like the opposite of how it should behave."
 * [later](https://github.com/microsoft/TypeScript-go/issues/1622#issuecomment-3647124648) **Knagis** suggested using an NDA path to share the private codebase and described its structure as React TSX files, Jest and Playwright specs, declaration-only emits, with few symlinks and path aliases

### [Issue microsoft/TypeScript-go#2143](https://github.com/microsoft/TypeScript-go/issues/2143) (Open, `Crash`)

**Panic handling request completionItem/resolve Some exportInfo should match the specified exportMapKey**

*TypeScript-Go language server panics on completionItem/resolve when exportInfo does not match the given exportMapKey*

 * created by **pedro757**
 * **pedro757** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2143#issuecomment-3643298196) **jakebailey** reported a panic in handling completionItem/resolve along with a stack trace

### [Issue microsoft/TypeScript-go#2245](https://github.com/microsoft/TypeScript-go/issues/2245) (Closed, `Domain: JS`, `Crash`, **ahejlsberg**)

**Folding range crash in JS file for \`exports\.property = CallExpression\(ObjectLiteral\)\`**

*The TypeScript Go LSP panics computing folding ranges for an export assignment call expression with an object literal.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2245#issuecomment-3621034523) **jakebailey** said "Yes, I think the astnav caching is incorrect given it's only based on positions"
 * (3 days ago) **RyanCavanaugh** added label `Crash`, and assigned to **navya9singh**
 * **DanielRosenwasser** added label `Domain: JS`

### [Issue microsoft/TypeScript-go#2253](https://github.com/microsoft/TypeScript-go/issues/2253) (Open, `Domain: JS`, `Crash`, **Copilot**)

**Crash completing beginning of property name when preceded by JSDoc**

*Completion requests at the start of a JSDoc-preceded property name cause a nil pointer dereference crash in the TypeScript service.*

 * created by **DanielRosenwasser**
 * (5 days ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**
 * **DanielRosenwasser** added label `Domain: JS`

### [Issue microsoft/TypeScript-go#2260](https://github.com/microsoft/TypeScript-go/issues/2260) (Open, `Domain: Editor`)

**Inherited methods not merging JSDoc comments**

*tsgo fails to merge inherited JSDoc comments into overridden methods, showing only new @remarks tags.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3628460459) **jakebailey** said "FWIW there is a PR for this in #2262. @LukeAbby does it do what you expect?"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3628872763) **LukeAbby** indicated that the PR didn't fully work due to literal JSDoc concatenation and suggested restoring old behavior or adding an opt-in for merging docs with @inheritDoc
 * **jakebailey** added label `Domain: Editor`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3645658993) **a-tarasyuk** provided a test case and sample QuickInfo output demonstrating JSDoc inheritDocTag behavior

### [Issue microsoft/TypeScript-go#2278](https://github.com/microsoft/TypeScript-go/issues/2278) (Open)

**TS2305: Module '"@stylexjs/babel\-plugin"' has no exported member 'Options'\.**

*tsgo compilation reports TS2305 error saying '@stylexjs/babel-plugin' has no exported 'Options' member while TypeScript 5.9 does not*

 * created by **jfirebaugh**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3628947678) **jakebailey** said "This package looks quite broken. https://arethetypeswrong.github.io/?p=%40stylexjs%2Fbabel-plugin%400.17.2"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3628955187) **jakebailey** said "But, 5.9 and 6.0 do not seem to complain."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3643232296) **DanielRosenwasser** said "Does 5.9/6.0 run into an issue with "module": "nodenext"?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2278#issuecomment-3646839251) **jfirebaugh** said "No errors with 5.9 or 6.0 when adding "module": "nodenext" to the above repro."

### [Issue microsoft/TypeScript-go#2280](https://github.com/microsoft/TypeScript-go/issues/2280) (Open, `Domain: Editor`, **gabritto**)

**Port \`implement interface\` quick fix**

*Port the implement interface quick fix from TypeScript to TS-Go to provide automated interface implementation support.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3632504763) **Tyriar** said "This is up there with most used quick fixes."
 * **jakebailey** added label `Domain: Editor`
 * **gabritto** assigned to **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3644087661) **a-tarasyuk** said "@Tyriar, I'm curious, what are some other quick fixes that are among the top five most commonly used? :slightly_smiling_face:"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3644200857) **Tyriar** said "I'm not sure I have 5 commonly used ones actually. It's hard to remember them off the top of my head, I use the promise  await conversion one occasionally is one that comes to mind."

### [Issue microsoft/TypeScript-go#2289](https://github.com/microsoft/TypeScript-go/issues/2289) (Closed, `Domain: JS`, `Crash`, **ahejlsberg**)

**Completions crash in JSDoc object type literal**

*Requesting completions inside a JSDoc object type literal crashes the TypeScript server due to a token cache mismatch.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **DanielRosenwasser** added label `Domain: JS`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2289#issuecomment-3643508281) **DanielRosenwasser** reported a crash outside the object in a typedef and included a code snippet and panic stack trace
 * **DanielRosenwasser** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#2290](https://github.com/microsoft/TypeScript-go/issues/2290) (Open, `Domain: JS`, `Crash`)

**Crash for completions after JSDoc \`\*\` on line following string\-named property signature**

*TypeScript Go language server panics when requesting completions after a JSDoc asterisk following a string-named property signature.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **DanielRosenwasser** added label `Domain: JS`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2290#issuecomment-3644048426) **DanielRosenwasser** suggested it was the same issue and provided a code snippet and stack trace showing a panic in textDocument/completion

### [Issue microsoft/TypeScript-go#2306](https://github.com/microsoft/TypeScript-go/issues/2306) (Closed, `Domain: Editor`, **ahejlsberg**)

**The \`@see\` JSDoc tag cannot create links from URLs**

*Hover tooltips for JSDoc @see URLs are rendered incorrectly and not clickable in the TS Native Preview extension.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637583842) **csvn** said "Ah, sorry. I hadn't read that part 😅 "
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3637913437) **maishivamhoo123** apologized for missing the CONTRIBUTING.md point, confirmed reading the issue-claiming section, and stated intent to open a PR if able to fix it
 * **jakebailey** added label `Domain: Editor`
 * **ahejlsberg** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3643148468) **ahejlsberg** said "This is in code that I wrote, and I've got a fix ready."

### [Issue microsoft/TypeScript-go#2325](https://github.com/microsoft/TypeScript-go/issues/2325) (Closed, `Domain: Emit`)

**Extra parentheses added when type assertion is used in arrow function with object literal**

*tsgo incorrectly adds an extra pair of parentheses around object literals when type assertions are used in arrow functions.*

 * created by **dragomirtitian**
 * **jakebailey** added label `Domain: Emit`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2330](https://github.com/microsoft/TypeScript-go/pull/2330) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#62844: Gate \`\#/\` subpath imports on NodeNext and Bundler**

*Enable '#/' subpath imports for NodeNext and Bundler modes while preserving Node16 compatibility via a new feature flag.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639506353) **Copilot** added compiler test cases from the original PR and did not port the requested fourslash test
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639698114) **magic-akari** asked whether combining the error cases into a single test would be better
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2330#issuecomment-3639731399) **jakebailey** said "Yeah, it makes separate baselines, so is a pretty good solution to this."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2333](https://github.com/microsoft/TypeScript-go/pull/2333) (Closed)

**Add token flags parameter to token creation functions**

*Implement a token flags parameter in token creation functions, propagate flags as in Strada, and prevent issues like #2326.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2338](https://github.com/microsoft/TypeScript-go/pull/2338) (Closed)

**Fix unquote**

*Fix the misported regex in the unquote implementation.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2339](https://github.com/microsoft/TypeScript-go/pull/2339) (Closed)

**Port many more fourslash functions**

*Port a suite of missing fourslash testing functions for error counting, existence checks at ranges and markers, and content validation.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2341](https://github.com/microsoft/TypeScript-go/issues/2341) (Open)

**Performance regression with \`\-\-incremental\` between \`native\-preview\-0\.20251211\.1\` and \`0\.20251209\.1\`**

*First-run incremental type checking in native-preview-0.20251211.1 is three times slower than in native-preview-0.20251209.1.*

 * created by **gggdomi**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3642663676) **jakebailey** said "There were many changes in between these two versions. Could you build from source and git bisect?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3642966388) **gggdomi** asked for the commits corresponding to the two releases because they couldn't find tags or publish commits
 * [today](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3642984643) **jakebailey** explained that the npm package included the setting in package.json but the VS Code extension did not, citing commit range 8372401975e9 to ddf0b72580c2
 * [today](https://github.com/microsoft/TypeScript-go/issues/2341#issuecomment-3642986737) **jakebailey** said "If it's #2314 I'm going to be very sad"

### [PR microsoft/TypeScript-go#2343](https://github.com/microsoft/TypeScript-go/pull/2343) (Closed)

**\-\-experimentalDecorators and \-\-emitDecoratorMetadata**

*Implement decorator and metadata emit flags in TypeScript-Go, resolve sourcemap test mismatches, and review pending feature emits.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3643406043) **jakebailey** said "The only other thing is to remove !!! emitDecoratorMetadata from program.go where we would have emitted an error on this option."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3643430727) **tmm1** said "Thank you for tackling this 🙏 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3644427188) **tmm1** suggested a sourcemap visualization tool at https://evanw.github.io/source-map-visualization
 * [later](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3645640415) **weswigham** clarified that the removal of !!! emitDecoratorMetadata had already occurred and was replaced by an error requiring emitDecoratorMetadata alongside experimentalDecorators

### [PR microsoft/TypeScript-go#2344](https://github.com/microsoft/TypeScript-go/pull/2344) (Closed)

**Skip fourslash at runtime instead of statically**

*Switch fourslash tests to be skipped at runtime rather than modifying each test file with Skip() calls.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2345](https://github.com/microsoft/TypeScript-go/pull/2345) (Closed)

**fix\(2325\): Extra parentheses added when type assertion is used in arrow function with object literal**

*Using type assertions in arrow functions that return object literals incorrectly inserts extra parentheses.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2346](https://github.com/microsoft/TypeScript-go/issues/2346) (Closed, `Crash`, **ahejlsberg**)

**Crash for completion for property in JSDoc \`/\*\* @type \*/\` tag**

*TypeScript-Go language server crashes with a nil pointer panic when requesting completions inside a JSDoc @type property tag.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [PR microsoft/TypeScript-go#2347](https://github.com/microsoft/TypeScript-go/pull/2347) (Closed)

**Use \`go test \-json\` in updateFailing, detect baseline errors**

*Enhance updateFailing to use go test -json and parse test failures for missing baseline errors.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2347#issuecomment-3644387545) **jakebailey** said "I need to think about this harder; I have to go manually merge this into one of my branches to get it to test so it's annoying to figure out."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2347#issuecomment-3645000890) **jakebailey** said "No, this does seem to work, I just merged the two PRs together wrong."

### [PR microsoft/TypeScript-go#2348](https://github.com/microsoft/TypeScript-go/pull/2348) (Open)

**Don't set folding range collapsed text if client doesn't want it**

*Provide folding range collapsed text only when the client requests it, because VS Code neither requests nor tests this feature.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2349](https://github.com/microsoft/TypeScript-go/issues/2349) (Closed, `Domain: Editor`, **ahejlsberg**)

**Support JSDoc \`\<caption\>\` tags for IntelliSense**

*Add support for multiline JSDoc <caption> tags in IntelliSense to match single-line behavior.*

 * created by **mjbvz**

### [Issue microsoft/TypeScript-go#2350](https://github.com/microsoft/TypeScript-go/issues/2350) (Closed, **gabritto**)

**Differentiate between crashing vs failing tests**

*Differentiate recovered crash events from standard test failures to enable targeted tracking and resolution.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2350#issuecomment-3644320421) **jakebailey** said "It doesn't fail with "nil response" anymore, it should fail with the actual errors. But, they are not tracked separately."
 * **gabritto** assigned to **gabritto**

### [Issue microsoft/TypeScript-go#2351](https://github.com/microsoft/TypeScript-go/issues/2351) (Open, `Domain: Emit`)

**Implement es2017\-\>es2016 transform \(async/await\)**

*Add support for ES2016 targets by transforming async functions and await expressions via the newAsyncTransformer.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2352](https://github.com/microsoft/TypeScript-go/issues/2352) (Open, `Domain: Emit`)

**Implement es2018\-\>es2017 transform \(for await & object rest/spread\)**

*Add transformation for async iteration (for-await-of) to enable targeting ES2017*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2353](https://github.com/microsoft/TypeScript-go/issues/2353) (Open, `Domain: Emit`)

**Implement es2023\-\>es2022 transform \(class fields and class static blocks\)**

*Add support for transforming ES2023 class static blocks and class fields to ES2022 using new transformers.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2353#issuecomment-3644350760) **tmm1** said "related https://github.com/microsoft/typescript-go/pull/1542"

### [Issue microsoft/TypeScript-go#2354](https://github.com/microsoft/TypeScript-go/issues/2354) (Open, `Domain: Emit`)

**Implement esnext\-\>es2022 transformer \(ES decorators, \`using\` declarations\)**

*Implement ES decorator transformations to enable --target es2022 support in the esnext->es2022 transformer.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2356](https://github.com/microsoft/TypeScript-go/issues/2356) (Closed)

**Omit numeric separators when targeting es2020**

*Numeric separators are retained in output when targeting ES2020, requiring modification to strip or transform them.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2357](https://github.com/microsoft/TypeScript-go/pull/2357) (Closed)

**List crashing tests**

*Lists tests that are crashing and solicits suggestions for the best way to present this information.*

 * created by **gabritto**
 * (later) **gabritto** closed the issue
 * (later) **gabritto** reopened the issue

### [PR microsoft/TypeScript-go#2358](https://github.com/microsoft/TypeScript-go/pull/2358) (Closed)

**fix\(2356\): omit numeric separators when targeting es2020**

*Omit numeric separators in generated code when targeting ES2020.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#2359](https://github.com/microsoft/TypeScript-go/pull/2359) (Closed)

**Permit URLs in \`@see\` tags and make links for name references**

*Allow URLs in @see JSDoc tags and auto-generate links for referenced identifiers*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#2360](https://github.com/microsoft/TypeScript-go/issues/2360) (Closed, `wontfix`, `Domain: Editor`)

**Setting useTsgo=true with the plugin disabled will prevent you from jumping to the type definition in Cursor**

*Enabling typescript.experimental.useTsgo with the TypeScript Native Preview plugin disabled prevents jumping to type definitions.*

 * created by **wygkzqa**
 * **wygkzqa** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2361](https://github.com/microsoft/TypeScript-go/pull/2361) (Open)

**Add "package deduplication", \-\-disablePackageDeduplication**

*Implement package deduplication in the new compiler by replacing duplicate package ASTs during collection and adding a --disablePackageDeduplication flag.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2362](https://github.com/microsoft/TypeScript-go/issues/2362) (Open)

**LSP diagnostics not working in Emacs's eglot**

*tsgo LSP server fails to publish diagnostics to Emacs’s eglot unlike typescript-language-server, possibly due to client capabilities mismatch.*

 * created by **edkolev**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2362#issuecomment-3647016225) **jakebailey** noted that only pull diagnostics are supported and asked whether eglot supports push diagnostics

