# Report for 2025-12-12 (Friday, December 12th, 2025)

15 different users commented on 33 different issues.

## Recommended Actions

 * Response Recommended
    * @marioparaschiv asked about the priority on user preferences for the LSP in [microsoft/TypeScript-go#1708](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3647571345)
    * @loynoir requested support for `go install fork` in [microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3648897284)

## Activity Summary

### [Issue microsoft/TypeScript-go#1708](https://github.com/microsoft/TypeScript-go/issues/1708) (Open, `Domain: Editor`)

**tsgo preview: import suggestions are not aware of paths**

*tsgo preview in Zed lacks path-aware import suggestions provided by vtsls, making it unusable.*

 * **jakebailey** added label `Domain: Editor`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3389747399) **robertbenjamin** reported encountering a 'Cannot find module' error for '@pubsub/events', shared their tsconfig paths configuration, asked if path alias support was not yet available, and said they would track the issue
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3390528659) **jakebailey** said "That is unrelated; please file a new issue with a repro."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3647571345) **marioparaschiv** said "What's the priority on user preferences for the LSP? "
 * [today](https://github.com/microsoft/TypeScript-go/issues/1708#issuecomment-3647674267) **jakebailey** asked about the priority and requested repro steps if the issue persisted

### [PR microsoft/TypeScript-go#1808](https://github.com/microsoft/TypeScript-go/pull/1808) (Closed)

**Add option for overriding \`GOMEMLIMIT\`**

*Provide a configuration option to override the GOMEMLIMIT environment variable.*

 * created by **maschwenk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/1808#issuecomment-3648125290) **jakebailey** expressed desire to merge the changes to enable testing and noted that a merge from main was required
 * [today](https://github.com/microsoft/TypeScript-go/pull/1808#issuecomment-3648129981) **maschwenk** said "@jakebailey on it!"

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open)

**Add Yarn PnP support**

*Implement native Yarn Plug'n'Play support in TypeScript Go with PnP VFS, API, and manifest handling.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3457072757) **GGomez99** said "I see my tests are not passing in CI, looking into it 🙇 "
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3604090437) **adrian-gierakowski** said "is this kept up to date with master? I would like to try it out on a monorepo at work. Thanks!"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3616833735) **GGomez99** offered to update the PR to keep it in sync with master and invited further feedback
 * [today](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3648897284) **loynoir** suggested supporting `go install fork` due to go install limitations, referenced related issue and PR, and provided error logs and VSCode config

### [Issue microsoft/TypeScript-go#2245](https://github.com/microsoft/TypeScript-go/issues/2245) (Closed, `Domain: JS`, `Crash`, **ahejlsberg**)

**Folding range crash in JS file for \`exports\.property = CallExpression\(ObjectLiteral\)\`**

*The TypeScript Go LSP panics computing folding ranges for an export assignment call expression with an object literal.*

 * (4 days ago) **RyanCavanaugh** added label `Crash`, and assigned to **navya9singh**
 * **DanielRosenwasser** added label `Domain: JS`
 * (today) **ahejlsberg** assigned to **ahejlsberg**, and unassigned **navya9singh**

### [Issue microsoft/TypeScript-go#2306](https://github.com/microsoft/TypeScript-go/issues/2306) (Closed, `Domain: Editor`, **ahejlsberg**)

**The \`@see\` JSDoc tag cannot create links from URLs**

*Hover tooltips for JSDoc @see URLs are rendered incorrectly and not clickable in the TS Native Preview extension.*

 * **jakebailey** added label `Domain: Editor`
 * **ahejlsberg** assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2306#issuecomment-3643148468) **ahejlsberg** said "This is in code that I wrote, and I've got a fix ready."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2343](https://github.com/microsoft/TypeScript-go/pull/2343) (Closed)

**\-\-experimentalDecorators and \-\-emitDecoratorMetadata**

*Implement decorator and metadata emit flags in TypeScript-Go, resolve sourcemap test mismatches, and review pending feature emits.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3643430727) **tmm1** said "Thank you for tackling this 🙏 "
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3644427188) **tmm1** suggested a sourcemap visualization tool at https://evanw.github.io/source-map-visualization
 * [today](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3645640415) **weswigham** clarified that the removal of !!! emitDecoratorMetadata had already occurred and was replaced by an error requiring emitDecoratorMetadata alongside experimentalDecorators
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2343#issuecomment-3647587892) **jycouet** said "Great news 🎉"

### [Issue microsoft/TypeScript-go#2346](https://github.com/microsoft/TypeScript-go/issues/2346) (Closed, `Crash`, **ahejlsberg**)

**Crash for completion for property in JSDoc \`/\*\* @type \*/\` tag**

*TypeScript-Go language server crashes with a nil pointer panic when requesting completions inside a JSDoc @type property tag.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **ahejlsberg** assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#2347](https://github.com/microsoft/TypeScript-go/pull/2347) (Closed)

**Use \`go test \-json\` in updateFailing, detect baseline errors**

*Enhance updateFailing to use go test -json and parse test failures for missing baseline errors.*

 * created by **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2347#issuecomment-3644387545) **jakebailey** said "I need to think about this harder; I have to go manually merge this into one of my branches to get it to test so it's annoying to figure out."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2347#issuecomment-3645000890) **jakebailey** said "No, this does seem to work, I just merged the two PRs together wrong."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2349](https://github.com/microsoft/TypeScript-go/issues/2349) (Closed, `Domain: Editor`, **ahejlsberg**)

**Support JSDoc \`\<caption\>\` tags for IntelliSense**

*Add support for multiline JSDoc <caption> tags in IntelliSense to match single-line behavior.*

 * created by **mjbvz**
 * (today) **jakebailey** added label `Domain: Editor`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#2350](https://github.com/microsoft/TypeScript-go/issues/2350) (Closed, **gabritto**)

**Differentiate between crashing vs failing tests**

*Differentiate recovered crash events from standard test failures to enable targeted tracking and resolution.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2350#issuecomment-3644320421) **jakebailey** said "It doesn't fail with "nil response" anymore, it should fail with the actual errors. But, they are not tracked separately."
 * **gabritto** assigned to **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2351](https://github.com/microsoft/TypeScript-go/issues/2351) (Open, `Domain: Emit`)

**Implement es2017\-\>es2016 transform \(async/await\)**

*Add support for ES2016 targets by transforming async functions and await expressions via the newAsyncTransformer.*

 * created by **DanielRosenwasser**
 * **jakebailey** added label `Domain: Emit`

### [Issue microsoft/TypeScript-go#2352](https://github.com/microsoft/TypeScript-go/issues/2352) (Open, `Domain: Emit`)

**Implement es2018\-\>es2017 transform \(for await & object rest/spread\)**

*Add transformation for async iteration (for-await-of) to enable targeting ES2017*

 * created by **DanielRosenwasser**
 * **jakebailey** added label `Domain: Emit`

### [Issue microsoft/TypeScript-go#2353](https://github.com/microsoft/TypeScript-go/issues/2353) (Open, `Domain: Emit`)

**Implement es2023\-\>es2022 transform \(class fields and class static blocks\)**

*Add support for transforming ES2023 class static blocks and class fields to ES2022 using new transformers.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2353#issuecomment-3644350760) **tmm1** said "related https://github.com/microsoft/typescript-go/pull/1542"
 * **jakebailey** added label `Domain: Emit`

### [Issue microsoft/TypeScript-go#2354](https://github.com/microsoft/TypeScript-go/issues/2354) (Open, `Domain: Emit`)

**Implement esnext\-\>es2022 transformer \(ES decorators, \`using\` declarations\)**

*Implement ES decorator transformations to enable --target es2022 support in the esnext->es2022 transformer.*

 * created by **DanielRosenwasser**
 * **jakebailey** added label `Domain: Emit`

### [Issue microsoft/TypeScript-go#2356](https://github.com/microsoft/TypeScript-go/issues/2356) (Closed)

**Omit numeric separators when targeting es2020**

*Numeric separators are retained in output when targeting ES2020, requiring modification to strip or transform them.*

 * created by **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2357](https://github.com/microsoft/TypeScript-go/pull/2357) (Closed)

**List crashing tests**

*Lists tests that are crashing and solicits suggestions for the best way to present this information.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue
 * (today) **gabritto** reopened the issue
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2358](https://github.com/microsoft/TypeScript-go/pull/2358) (Closed)

**fix\(2356\): omit numeric separators when targeting es2020**

*Omit numeric separators in generated code when targeting ES2020.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2359](https://github.com/microsoft/TypeScript-go/pull/2359) (Closed)

**Permit URLs in \`@see\` tags and make links for name references**

*Allow URLs in @see JSDoc tags and auto-generate links for referenced identifiers*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2360](https://github.com/microsoft/TypeScript-go/issues/2360) (Closed, `wontfix`, `Domain: Editor`)

**Setting useTsgo=true with the plugin disabled will prevent you from jumping to the type definition in Cursor**

*Enabling typescript.experimental.useTsgo with the TypeScript Native Preview plugin disabled prevents jumping to type definitions.*

 * created by **wygkzqa**
 * **wygkzqa** added label `Domain: Editor`
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2360#issuecomment-3647478665) **RyanCavanaugh** advised disabling the TypeScript (Native Preview) plugin and setting typescript.experimental.useTsgo to true in settings.json to avoid misconfiguration
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#2363](https://github.com/microsoft/TypeScript-go/pull/2363) (Closed)

**Cache name table on SourceFile**

*Enable caching of the nameTable property on SourceFile by initializing it on first access.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2364](https://github.com/microsoft/TypeScript-go/issues/2364) (Open)

**Provide document links in tsconfig/jsconfig files**

*Enable TypeScript to provide document links for extends, files, and references in tsconfig/jsconfig to improve IntelliSense consistency and reduce bugs.*

 * created by **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2364#issuecomment-3647749264) **jakebailey** suggested adding JSON file patterns to the document selector to limit tsconfig JSON files

### [PR microsoft/TypeScript-go#2365](https://github.com/microsoft/TypeScript-go/pull/2365) (Closed)

**Use xxh3\.HashString128 instead of converting to byte slice**

*Use xxh3.HashString128 for string input instead of converting to byte slices to reduce memory allocations and improve performance.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2366](https://github.com/microsoft/TypeScript-go/issues/2366) (Open)

**Diagnostics not shown in file peek views**

*Reference peek views in TypeScript no longer display diagnostics such as deprecation warnings across files.*

 * created by **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3648002251) **jakebailey** said "We don't control this; is VS Code / the LSP client not opening that file and asking for diagnostics?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2366#issuecomment-3648014391) **mjbvz** said "Yes maybe an lsp issue? cc @dbaeumer "

### [Issue microsoft/TypeScript-go#2367](https://github.com/microsoft/TypeScript-go/issues/2367) (Open, **Copilot**)

**References code lens does not include imports as references**

*The references code lens fails to count imports as references, showing zero references despite TypeScript 6.0 support.*

 * created by **mjbvz**
 * **jakebailey** assigned to **Copilot**

### [PR microsoft/TypeScript-go#2368](https://github.com/microsoft/TypeScript-go/pull/2368) (Open, **jakebailey**, **Copilot**)

**Fix references code lens to include imports as references**

*Modify the Go code lens references feature to include import statements as valid references, matching TypeScript’s implementation.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2368#issuecomment-3648358830) **Copilot** reverted the incorrect fix in commit aaefcb7a, kept the test to demonstrate the issue, and noted that a proper fix requires deeper analysis of TypeScript vs Go behaviors

### [Issue microsoft/TypeScript-go#2369](https://github.com/microsoft/TypeScript-go/issues/2369) (Open, `Domain: Editor`)

**Code Lens provider registration error after switching tsdk location**

*Switching TypeScript SDK paths triggers a duplicate code lens command registration error and launches two language server instances.*

 * created by **andrewbranch**
 * **andrewbranch** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#2370](https://github.com/microsoft/TypeScript-go/pull/2370) (Open)

**Format options \+ fourslash testing \+ fix formatting bugs**

*Introduces server formatting options for JS/TS, refactors formatCodeSettings, adds fourslash tests with skip flags, and fixes extra-space bugs.*

 * created by **iisaduan**

### [PR microsoft/TypeScript-go#2371](https://github.com/microsoft/TypeScript-go/pull/2371) (Open)

**Fix getTokenAtPos in JSDoc trivia position**

*getTokenAtPosition incorrectly scans JSDoc trivia gaps, causing AST position mismatches, so we now track the next node to constrain scanning.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#2372](https://github.com/microsoft/TypeScript-go/pull/2372) (Closed)

**Reparse fixes**

*Revise AST reparsing for @type and @satisfies to retain original expressions and only flag cloned type nodes.*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2372#issuecomment-3649566615) **ahejlsberg** explained that PR 2371 became simpler because tracking of special reparsed nodes was no longer needed and shouldVisitNode just checks that a node isn't reparsed

### [PR microsoft/TypeScript-go#2373](https://github.com/microsoft/TypeScript-go/pull/2373) (Open)

**Switch dprint to new gofumpt Wasm plugin**

*Adopt the new gofumpt Wasm plugin in dprint to improve formatting performance by over 67× and fix Windows reliability issues.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#648](https://github.com/microsoft/TypeScript-go/issues/648) (Open, `Domain: API and Extensibility`)

**Support embedded JavaScript/TypeScript**

*Enable built-in handling of embedded JavaScript/TypeScript in languages such as MDX, Vue, Svelte, Astro, and Markdown in the Go rewrite.*

 * created by **remcohaszing**
 * [30 weeks ago](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-2878040905) **NullVoxPopuli** suggested that emitting type definitions would be beneficial for library authoring and for interacting with typedoc and other tsc-using tools
 * **jakebailey** added label `Domain: API and Extensibility`
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3649410246) **silverwind** suggested supporting common embedder formats like .vue SFCs and .mdx directly without plugins, noted that markdown code blocks may not need type-checking, described extracting TypeScript blocks via regex, and mentioned a tsgo workaround by stubbing .vue exports
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3649420466) **NullVoxPopuli** warned against using regex and recommended a real parser, citing 40+ bugs from a previous regex-based parser and describing Ember's volar plugin approach
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3649443016) **silverwind** agreed that regex is too crude and suggested using a proper parser with an example of nested script tags
 * [later](https://github.com/microsoft/TypeScript-go/issues/648#issuecomment-3649445924) **segevfiner** explained that type checking Vue SFC requires handling template expressions and that vue-tsc uses a monkey patch in TypeScript due to tsc's lack of a plugin API

### [Issue microsoft/TypeScript-go#914](https://github.com/microsoft/TypeScript-go/issues/914) (Closed, `Domain: Emit`)

**Not transpiling decorators**

*The compiler emits decorators unchanged in both experimental and regular modes instead of transpiling them.*

 * [24 weeks ago](https://github.com/microsoft/TypeScript-go/issues/914#issuecomment-2993482657) **mlarabi** asked why decorator was not included in the list or if the list only showed planned or ongoing features
 * [24 weeks ago](https://github.com/microsoft/TypeScript-go/issues/914#issuecomment-2993643918) **jakebailey** said "Emit is marked as "in progress"."
 * [24 weeks ago](https://github.com/microsoft/TypeScript-go/issues/914#issuecomment-2993718315) **tmm1** pointed to where the feature would need to be implemented in transformer.go
 * (today) **weswigham** closed the issue

