# Report for 2026-03-18 (Wednesday, March 18th, 2026)

16 different users commented on 68 different issues.

## Recommended Actions

 * Response Recommended
    * @vetptzru asked how to pass the --singleThreaded flag in VS Code in [microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089048689)
    * @vetptzru provided screenshots of the peak thread count before the crash in [microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089083039)

## Activity Summary

### [Issue microsoft/TypeScript-go#1115](https://github.com/microsoft/TypeScript-go/issues/1115) (Closed, `Porting PR`, **jakebailey**, **Copilot**)

**Port TypeScript PR \#59282: Extract node type printer**

*Port the node type printer extraction changes from TypeScript PR #59282 into the Go-based TypeScript repository.*

 * (40 weeks ago) **andrewbranch** added label `Porting PR`, assigned to **Copilot**, and unassigned **Copilot**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1123](https://github.com/microsoft/TypeScript-go/issues/1123) (Closed, `Porting PR`, **andrewbranch**, **Copilot**)

**Port TypeScript PR \#60304: More rigorous ASI prevention when emitting \`return\`/\`yield\`**

*Implement the changes from TypeScript PR #60304 for more rigorous ASI prevention on return/yield in the Go port.*

 * (40 weeks ago) **andrewbranch** added label `Porting PR`, assigned to **Copilot**, and unassigned **Copilot**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#1498](https://github.com/microsoft/TypeScript-go/issues/1498) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**\[lsp\] Typescript generics type error**

*TypeScript LSP plugin lacks generic type completions and inference suggestions for Array<> similar to the existing TS plugin.*

 * [32 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1498#issuecomment-3145719691) **jakebailey** said "This is probably just a completions bug. Generic types are of course supported otherwise."
 * [31 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1498#issuecomment-3173141327) **johnnycheng0210** asked whether the differing hover output for the type parameter T between tsv5 and tsgo was expected
 * [31 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1498#issuecomment-3173254707) **jakebailey** said "That's an unrelated hover bug"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1498#issuecomment-4088111998) **jakebailey** said "This is still unfixed. The popup that appears is signature help, but we are not being requested that."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1498#issuecomment-4088114756) **jakebailey** noted that trigger characters were not set correctly and provided a link and code snippet
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#1725](https://github.com/microsoft/TypeScript-go/issues/1725) (Closed, `Domain: Module Resolution`, `Domain: Type Checking`, **andrewbranch**)

**Module resolution: tsgo resolves package\.json \`exports\` conditions differently than \`tsc\` and errors**

*tsgo resolves package.json exports differently than tsc under nodenext, causing TS2497 errors on default imports.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1725#issuecomment-3305115869) **controversial** explained that their `test.ts` file is actually a `vite.config.ts` transpiled by vite and noted that this prevented the node warning at runtime while acknowledging the setup isn’t optimal but caused a breaking behavior with tsgo
 * (23 weeks ago) **jakebailey** added labels `Domain: Module Resolution`, `Domain: Type Checking`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1725#issuecomment-4086072348) **andrewbranch** said "Fixed by #2969 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#1954](https://github.com/microsoft/TypeScript-go/issues/1954) (Closed, `Domain: JS`, **andrewbranch**)

**Named import against CJS file with \`module\.exports = { \.\.\. }\` errors only with tsgo**

*tsgo erroneously rejects named imports from CommonJS files unless allowSyntheticDefaultImports is enabled, while tsc accepts them.*

 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1954#issuecomment-3447077009) **sapphi-red** provided an additional code example demonstrating the issue
 * **jakebailey** added label `Domain: JS`
 * **ahejlsberg** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1954#issuecomment-4086042317) **andrewbranch** said "Fixed by #2969 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#1994](https://github.com/microsoft/TypeScript-go/issues/1994) (Closed, `Domain: Editor`, **Copilot**)

**Add fourslash support for formatting requests**

*Support LSP formatting, rangeFormatting, and onTypeFormatting commands in fourslash to enable new tests and suite porting.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **Copilot**
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1994#issuecomment-4088118517) **jakebailey** said "I think we have all of these now"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2020](https://github.com/microsoft/TypeScript-go/pull/2020) (Closed)

**Support for custom configurations**

*Enable passing custom tsconfig file names to the tsgo LSP to support solution-style repository configurations.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963848279) **jakebailey** rejected restarting the client and asked Andrew Branch for insight
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-3963951469) **andrewbranch** said "I'm not sure off the top of my head, I'd have to debug and step through."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-4065010535) **sspencer-canva** mentioned that the issue had been on hold for three weeks and asked if there was anything they could do to help
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-4084912118) **jakebailey** stated that the PR needed a merge from main, that they couldn’t explain the behavior seen in testing, and that they were attempting to write a test
 * [today](https://github.com/microsoft/TypeScript-go/pull/2020#issuecomment-4085003788) **jakebailey** said "I think I have a test and a fix. Will push it to the PR so we can get this moving."

### [Issue microsoft/TypeScript-go#2188](https://github.com/microsoft/TypeScript-go/issues/2188) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Mixins Overrides Drop Documentation**

*TypeScript fails to inherit JSDoc comments when a mixin-derived class overrides a static method.*

 * created by **LukeAbby**
 * **jakebailey** added label `Domain: Editor`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2205](https://github.com/microsoft/TypeScript-go/issues/2205) (Closed, `Domain: Editor`)

**TSGO doesnt read vscode settings json**

*TSGO extension fails to apply VS Code’s typescript.preferences.importModuleSpecifier and updateImportsOnFileMove settings.*

 * created by **lokeshrj**
 * [14 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2205#issuecomment-3609186268) **jakebailey** said "The first one is #1793. The latter is for a feature we don't implement."
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2205#issuecomment-4088125812) **jakebailey** said "This should be implemented now. The latter is another feature entirely."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2331](https://github.com/microsoft/TypeScript-go/pull/2331) (Closed)

**Organize Imports**

*Implement functionality to automatically organize and sort imports within source files.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3825234891) **jakebailey** said "I think there's a bug in the way we load indent size out of the settings; it's some discrepency i noticed when working on my user prefs refactor. VS Code's setting has a different name than we do."
 * (5 weeks ago) **johnfav03** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-4080425624) **bradleyayers** reported an issue with duplicated comments on exports and provided example test cases
 * [later](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-4091224193) **johnfav03** said "@bradleyayers Thank you for letting me know! I've put up a PR to fix this: https://github.com/microsoft/typescript-go/pull/3162"

### [Issue microsoft/TypeScript-go#2351](https://github.com/microsoft/TypeScript-go/issues/2351) (Closed, `bug`, `Domain: Emit`, **weswigham**)

**Implement es2017\-\>es2016 transform \(async/await\)**

*Add support for ES2016 targets by transforming async functions and await expressions via the newAsyncTransformer.*

 * **jakebailey** added label `Domain: Emit`
 * (9 weeks ago) **DanielRosenwasser** added label `bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2351#issuecomment-4088093188) **jakebailey** said "I did this in #2853 "
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2352](https://github.com/microsoft/TypeScript-go/issues/2352) (Closed, `bug`, `Domain: Emit`, **weswigham**)

**Implement es2018\-\>es2017 transform \(for await & object rest/spread\)**

*Add transformation for async iteration (for-await-of) to enable targeting ES2017*

 * **jakebailey** added label `Domain: Emit`
 * (9 weeks ago) **DanielRosenwasser** added label `bug`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2352#issuecomment-4088093730) **jakebailey** said "This was finished out in #2861 "
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2382](https://github.com/microsoft/TypeScript-go/issues/2382) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**\[bug\] JS/TS Format Selection can delete comments**

*Formatting a selected portion of a JavaScript or TypeScript block comment unexpectedly removes the comment.*

 * created by **RedCMD**
 * **RedCMD** added label `Domain: Editor`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2445](https://github.com/microsoft/TypeScript-go/issues/2445) (Closed, `bug`, **andrewbranch**, **Copilot**)

**resolvePackageJsonExports false ignored in tsgo, works in v5\.9 and v6**

*tsgo ignores resolvePackageJsonExports:false causing incorrect import paths in generated d.ts files, unlike TypeScript 5.9 and 6 preview*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2445#issuecomment-3719228344) **freshp86** uploaded a minimal repro example
 * (9 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [PR microsoft/TypeScript-go#2459](https://github.com/microsoft/TypeScript-go/pull/2459) (Closed)

**Port \-\-isolatedDeclarations related node builder logic, with baseline updates**

*Port node builder logic for the --isolatedDeclarations option and apply baseline updates for review.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-3827377748) **Zzzen** described testing the branch and noting the type emit was cleaner, reported still hitting OOM, and asked for tips on pinpointing memory usage
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-3835290600) **Zzzen** reported that setting GOMEMLIMIT=10GiB enabled full compilation and expressed excitement for the PR to land
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4077945493) **jakebailey** demonstrated that the smoke test didn’t catch the issue because build mode wasn’t used and reproduced a TS9013 error output
 * [today](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4085847334) **weswigham** suggested that unparsedTests.txt contents might depend on file inode ordering, noting regenerated file differed only in line order from main
 * [today](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4086013319) **jakebailey** mentioned that unparsedTests.txt ordering varied due to inode ordering and suggested adding a sort in the script
 * [today](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4086041403) **gabritto** suggested adding a sort to the script

### [Issue microsoft/TypeScript-go#2573](https://github.com/microsoft/TypeScript-go/issues/2573) (Closed, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**Seems like language server can't keep up with changes made in editor**

*The language server can't keep pace with editor changes, reporting outdated errors until it's restarted.*

 * **andrewbranch** assigned to **andrewbranch**
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3800595990) **andrewbranch** provided instructions to enable LSP tracing, collect output from both typescript-native-preview channels, and email the logs
 * **andrewbranch** added label `Needs More Info`
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2671](https://github.com/microsoft/TypeScript-go/issues/2671) (Closed, `Crash`, **andrewbranch**, **Copilot**)

**LS request crash when \`package\.json\` bizarrely maps specifier to \`\.ts\` file**

*The TypeScript language server crashes resolving imports when package.json’s imports field maps specifiers to .ts files.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2671#issuecomment-3849109195) **andrewbranch** said "It sure looks like this should crash via batch compilation too..."
 * **andrewbranch** assigned to **Copilot**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2671#issuecomment-3849156368) **DanielRosenwasser** said "It looks like it- maybe I wasn't running on a new-enough version of tsgo when I tried."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2671#issuecomment-4086292732) **andrewbranch** said "Fixed by #2680 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2678](https://github.com/microsoft/TypeScript-go/issues/2678) (Closed, `Needs More Info`)

**\`tsgo \-\-build\` hangs indefinitely**

*After upgrading from @sinclair/typebox 0.34.48 to typebox 1.0.81, tsgo --build hangs indefinitely during type-checking and declaration emission.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3848719531) **jakebailey** said "It does, yeah. Sorry, I realized the implication of it hanging after I replied."
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3849135940) **rubenferreira97** suggested adding a flag to capture a specific initial duration for debugging and offered further assistance
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-4086492863) **rubenferreira97** said "This seems to be resolved with the latest main."
 * (today) **rubenferreira97** closed the issue

### [Issue microsoft/TypeScript-go#2708](https://github.com/microsoft/TypeScript-go/issues/2708) (Closed, **jakebailey**, **Copilot**)

**tsgo emits files next to source instead of outDir when include references parent directories via \.\./**

*tsgo emits files from parent-directory includes next to their sources instead of respecting the configured outDir.*

 * (5 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-3864827529) **Cellule** confirmed that setting the rootDir fixed the issue and supposed that the lack of error reporting on tsgo vs tsc v6 was the real problem
 * [today](https://github.com/microsoft/TypeScript-go/issues/2708#issuecomment-4088086784) **jakebailey** said "#2819 was merged, which should add the error in"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2822](https://github.com/microsoft/TypeScript-go/issues/2822) (Closed, `Domain: Editor`, **andrewbranch**)

**Harden LSP against requests for files that don't have open projects**

*Enhance the LSP to gracefully handle requests for files not in open projects to avoid errors.*

 * (1 month ago) **andrewbranch** added label `Domain: Editor`, and assigned to **andrewbranch**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2822#issuecomment-3948026886) **DanielRosenwasser** mentioned that VS Code also requests diagnostics after closing files and provided logs and reproduction steps via 'close others'
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2906](https://github.com/microsoft/TypeScript-go/issues/2906) (Closed, `Crash`)

**Requests failing with \` Message: no project found for URI\`**

*After reloading VS Code, textDocument/codeLens requests fail with ‘no project found for URI’ errors.*

 * created by **mjbvz**
 * **mjbvz** added label `Crash`
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2978](https://github.com/microsoft/TypeScript-go/pull/2978) (Closed, **andrewbranch**, **Copilot**)

**Fix auto\-import type modifier and formatting issues in type\-only import statements**

*Fix inline type modifiers, formatting, indentation, token handling, and import ordering in type-only import statements.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4025998453) **Copilot** fixed the merge by reverting the bad single-parent commit and re-merging origin/main with a proper two-parent merge, resulting in the PR diff showing only the intended 18 changed files
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4049675258) **jakebailey** said "Needs a merge from main and update, it seems"
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4049824447) **andrewbranch** said "I wasn't ready yet!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4087562964) **jakebailey** said "bad main merge?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2978#issuecomment-4090944486) **andrewbranch** said "new test in main asserting incorrect formatting (intended just to assert no crash)"

### [Issue microsoft/TypeScript-go#3010](https://github.com/microsoft/TypeScript-go/issues/3010) (Closed, `Domain: Editor`, `Crash`, **DanielRosenwasser**)

**nil pointer dereference for contextual constraint completions in JSDoc**

*A nil pointer dereference occurs during constraint-based completions in JSDoc-annotated JavaScript files in the TypeScript language service.*

 * (1 week ago) **DanielRosenwasser** added labels `Domain: Editor`, `Crash`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3011](https://github.com/microsoft/TypeScript-go/pull/3011) (Closed)

**Fix completions for contextually constrained types in JSDoc**

*Ensure completions for contextually constrained JSDoc types correctly handle missing reparsed nodes by falling back to syntax node names.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3084](https://github.com/microsoft/TypeScript-go/pull/3084) (Open)

**Port LSP update imports on file rename support**

*Adds support to update import paths via LSP when files are renamed or moved to ensure correct relative references.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4070678965) **DanielRosenwasser** asked why the tests didn't use the typical fourslash test harness and whether existing tests from the old compiler were considered for porting
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4071505057) **anchmelev** thanked DanielRosenwasser, moved the semantic workspace/willRenameFiles coverage to the fourslash harness, trimmed direct server tests to LSP wire-up assertions, added relevant getEditsForFileRename coverage for non-relative imports, and omitted directory/tsconfig-specific variants
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4076493957) **jakebailey** explained that they avoid adding unit tests for this behavior and expected existing fourslash tests to be converted, since they cannot verify the ported tests otherwise
 * [today](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4086273176) **anchmelev** reworked the test conversion to use the converted fourslash path, added verify.getEditsForFileRename support, switched to generated tests for rename cases, fixed a parsing/conversion issue, and confirmed tests passed locally

### [Issue microsoft/TypeScript-go#3098](https://github.com/microsoft/TypeScript-go/issues/3098) (Open, `Domain: Editor`)

**"Peek References" does not show matches in other files**

*Enabling typescript.experimental.useTsgo in Cursor prevents Peek References from showing cross-file TypeScript references.*

 * created by **timephy**
 * **timephy** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3098#issuecomment-4087984253) **DanielRosenwasser** said "Those references are in Svelte files. There is currently no stable API that can be used to reimplement support for Svelte, Vue, Astro, etc., and we won't have one until at least TypeScript 7.1."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3098#issuecomment-4088563318) **timephy** said "That's sad to hear! I was really enjoying the speed tsgo gives me... Looking forward to when existing integrations will work again 🙌🏽"

### [PR microsoft/TypeScript-go#3100](https://github.com/microsoft/TypeScript-go/pull/3100) (Closed)

**Preallocate symbols in getSuggestionForSymbolNameLookup**

*Proposes preallocating the allSymbols array in getSuggestionForSymbolNameLookup to reduce reallocations and improve performance by about 3%.*

 * created by **camchenry**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3100#issuecomment-4067227675) **no-yan** suggested reducing sorting work by first tracking the best candidates for minimum Levenshtein distance and only sorting the final tie set to preserve determinism
 * [today](https://github.com/microsoft/TypeScript-go/pull/3100#issuecomment-4086811486) **camchenry** requested another review and explained that the performance regression was due to tsconfig defaults but that the change still provided a small performance win in error-heavy cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/3100#issuecomment-4087109263) **jakebailey** suggested diverging from sortSymbols to perform a plain sort on names when available
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3106](https://github.com/microsoft/TypeScript-go/issues/3106) (Closed, **jakebailey**, **Copilot**)

**Project reference redirect uses wrong tsconfig when file belongs to multiple sub\-projects \(breaks customConditions/moduleSuffixes\)**

*When a file belongs to multiple composite tsconfigs, tsgo uses the wrong project reference redirect, ignoring customConditions and moduleSuffixes.*

 * created by **tian000**
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3107](https://github.com/microsoft/TypeScript-go/pull/3107) (Closed, **jakebailey**, **Copilot**)

**Fix project reference redirect ordering when file belongs to multiple sub\-projects**

*Reverse project reference mapping order to apply parent tsconfig mappings before child projects, preserving customConditions and moduleSuffixes.*

 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3107#issuecomment-4083620382) **tian000** said "@jakebailey any update here!"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3121](https://github.com/microsoft/TypeScript-go/issues/3121) (Open, `Needs More Info`)

**extension gets uninstalled after around an hour on vscodium**

*The TypeScript Native Preview extension installed in VSCodium on Linux is uninstalled after about an hour for being flagged problematic.*

 * created by **huseeiin**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4076484678) **RyanCavanaugh** said "Download from where?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4077173146) **huseeiin** recommended downloading the VSIX via VS Code’s extensions tab instead of VSCodium and provided a screenshot
 * [today](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4087140542) **mjbvz** asked how they set up the marketplace in vscodium and whether they connected to the official marketplace or a different one

### [PR microsoft/TypeScript-go#3129](https://github.com/microsoft/TypeScript-go/pull/3129) (Closed)

**Validate JSON syntax during parse**

*Port missing JSON syntax validation into the parser to enable proper syntax checking.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3129#issuecomment-4084056636) **RyanCavanaugh** asked what the function was trying to do and noted it accepted comments and hex values but not single-quoted strings, contrary to JSON5 support
 * [today](https://github.com/microsoft/TypeScript-go/pull/3129#issuecomment-4084082260) **jakebailey** said "Do we actually support JSON5? JSONC is different, as is JWCC. I thought we were just "json with commas and comments"."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3131](https://github.com/microsoft/TypeScript-go/issues/3131) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Incorrect error diff: tsxElementResolution10**

*The tsxElementResolution10 error diff incorrectly omits the initial error stating '{ x: number }' is not a valid JSX element.*

 * (yesterday) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3131#issuecomment-4077855431) **RyanCavanaugh** said "This should also apply to Its return type of the variant message for function components"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3132](https://github.com/microsoft/TypeScript-go/pull/3132) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix incorrect eliding of JSX error head messages in property mismatch diagnostics**

*Fix eliding of JSX error head messages in property mismatch diagnostics by adding those messages to suppression exceptions.*

 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3132#issuecomment-4078129898) **Copilot** scoped the fix to only the three JSX-related error heads (`Its_instance_type`, `Its_return_type`, `Its_element_type`) and removed three JSX baseline diffs
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3133](https://github.com/microsoft/TypeScript-go/pull/3133) (Closed, **RyanCavanaugh**, **Copilot**)

**docs: document that Corsa only shows errors for the last function overload**

*Add CHANGES.md entry explaining that Corsa reports only the last function overload error rather than all.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3136](https://github.com/microsoft/TypeScript-go/pull/3136) (Closed)

**Update dependencies**

*Upgrade project dependencies to their latest stable versions.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3137](https://github.com/microsoft/TypeScript-go/pull/3137) (Closed)

**Fix all writestring analyzer errors**

*Manually ran the gopls writestring analyzer and corrected all reported errors.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3138](https://github.com/microsoft/TypeScript-go/pull/3138) (Closed)

**Reimplement \-\-showConfig**

*Reimplement the --showConfig command in tsoptions instead of JSON dumping, without inferred options printing.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Open, `Needs More Info`)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * created by **vetptzru**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4083983621) **jakebailey** questioned how Go could spawn threads beyond physical cores given its threading model
 * **DanielRosenwasser** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4085354173) **DanielRosenwasser** said "I guess on that note, do you see any differences if you pass a flag like --singleThreaded? And how are you building it today? Are you passing something like --watch?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089048689) **vetptzru** described that running with the --singleThreaded flag prevented crashes, mentioned currently building with that flag in VS Code and asked how to pass it there, and stated that they were not using --watch
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4089083039) **vetptzru** provided screenshots showing the peak thread count the tsgo process reached before crashing

### [Issue microsoft/TypeScript-go#3140](https://github.com/microsoft/TypeScript-go/issues/3140) (Closed)

**Reserved syntax error on generic function parameter**

*tsgo incorrectly flags both generic function declarations with and without trailing commas in .mts files as reserved syntax, unlike TypeScript 6.0.*

 * created by **StyleShit**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3140#issuecomment-4084286226) **DanielRosenwasser** said "Context: https://github.com/microsoft/TypeScript/issues/44442"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3141](https://github.com/microsoft/TypeScript-go/pull/3141) (Closed)

**fix\(3140\): align typeParameters grammar check with Strada**

*Updates the conditional logic for typeParameters grammar checks to align with Strada’s implementation.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3141#issuecomment-4084287370) **DanielRosenwasser** said "Context: https://github.com/microsoft/TypeScript/issues/44442"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3141#issuecomment-4085407993) **DanielRosenwasser** said "Thanks!"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3142](https://github.com/microsoft/TypeScript-go/pull/3142) (Closed)

**Match some submodule diagnostics for missing expressions**

*Match submodule diagnostics for missing expressions to eliminate 12 diffs.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3143](https://github.com/microsoft/TypeScript-go/pull/3143) (Closed)

**Match binary\-file scanning on replacement character**

*Detect and treat files containing replacement characters as binary during scanning operations.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3144](https://github.com/microsoft/TypeScript-go/pull/3144) (Closed)

**Ensure language service requests create a project for the requested file if one doesn't already exist**

*Ensure language service requests automatically create an inferred project for files not belonging to any configured project*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3145](https://github.com/microsoft/TypeScript-go/pull/3145) (Closed)

**Refactor debug package to be inlinable, always enabled**

*Refactor Go debug package to always enable inlined debug asserts by eliminating reflect, interface indirection, and un-inlinable tests.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3146](https://github.com/microsoft/TypeScript-go/issues/3146) (Closed, `bug`, `Domain: Emit`, **jakebailey**, **Copilot**)

**experimentalDecorators renames enum accesses with same name as class**

*experimentalDecorators causes enum member accesses sharing a class name to be incorrectly renamed in emitted code*

 * created by **jakebailey**
 * (today) **jakebailey** added labels `bug`, `Domain: Emit`, and assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3147](https://github.com/microsoft/TypeScript-go/pull/3147) (Closed, **jakebailey**, **Copilot**)

**Fix property access name substitution in decorator and class field transformers**

*Add explicit property access expression visitors in decorator and class-field transformers to prevent misrenaming property names that match class identifiers.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3147#issuecomment-4084588388) **jakebailey** asked for a slew of tests to cover potential bugs in ES decorators, class fields, and similar cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/3147#issuecomment-4084713463) **Copilot** confirmed the bug in the class fields transformer, fixed it in commit bd33135f, and added tests covering legacy decorators, class fields (including private fields), and ES decorators

### [Issue microsoft/TypeScript-go#3148](https://github.com/microsoft/TypeScript-go/issues/3148) (Closed, **andrewbranch**)

**Data race between GetFileByPath and MatchesDiskText**

*Concurrent execution of GetFileByPath and MatchesDiskText triggers a data race in the snapshotFSBuilder sync map handling.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3148#issuecomment-4085654340) **jakebailey** provided a data race warning stack trace
 * **jakebailey** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3149](https://github.com/microsoft/TypeScript-go/pull/3149) (Closed)

**Fix regression causing untitled files to crash**

*Fix regression by updating change-event filtering to include untitled file patterns and avoid crashes.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3150](https://github.com/microsoft/TypeScript-go/pull/3150) (Closed)

**Add bitclear analyzer to suggest \`&^= A\` instead of \`&= ^A\`**

*Add an analyzer to identify &= ^A bit-clearing patterns and automatically replace them with the &^= operator.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3151](https://github.com/microsoft/TypeScript-go/pull/3151) (Closed)

**Port string literal references**

*Add handling of string literal references to correct existing diff inconsistencies.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3152](https://github.com/microsoft/TypeScript-go/pull/3152) (Closed)

**Defer diagnostics in order to fix flaky test**

*Defer diagnostics during type resolution to avoid circularity errors and stabilize the flaky for-of29.ts test.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3152#issuecomment-4085530742) **ahejlsberg** noted that the callback passed to someSymbolTableInScope from getWithAlternativeContainers iterated a map, causing random choice when multiple matches existed
 * [later](https://github.com/microsoft/TypeScript-go/pull/3152#issuecomment-4090861496) **ahejlsberg** said "With latest commit we save deferred diagnostics only when doing a full type check. Also, the logic for initiating unused identifier checks now ensures that the check happens only once."

### [PR microsoft/TypeScript-go#3153](https://github.com/microsoft/TypeScript-go/pull/3153) (Closed)

**Fix race in snapshotFSBuilder\.FileExists\(\)**

*Eliminate a race condition in snapshotFSBuilder.FileExists to ensure reliable file existence checks.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3153#issuecomment-4085801376) **jakebailey** said "Thanks!"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3154](https://github.com/microsoft/TypeScript-go/pull/3154) (Closed)

**Sort \`unparsedTests\`**

*Implement sorting for the unparsedTests array to ensure ordered test entries.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3155](https://github.com/microsoft/TypeScript-go/pull/3155) (Closed, **andrewbranch**, **Copilot**)

**Fix \`resolvePackageJsonExports: false\` being ignored in module specifier generation**

*Fix module specifier generation to respect resolvePackageJsonExports:false by changing the guard in tryDirectoryWithPackageJson.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#3156](https://github.com/microsoft/TypeScript-go/pull/3156) (Closed)

**Update \`module: "none"\` cross project references test**

*Revise the module:none cross-project references test to add explicit project references following deprecation of file merging behavior*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#3157](https://github.com/microsoft/TypeScript-go/pull/3157) (Closed)

**Fix named export aliases merging with \`export =\`**

*Combining named export aliases with export = skips alias resolution, resulting in missing errors and silent failures.*

 * created by **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3157#issuecomment-4090825312) **andrewbranch** said "Hey look, a diff was deleted!"

### [PR microsoft/TypeScript-go#3158](https://github.com/microsoft/TypeScript-go/pull/3158) (Closed)

**Stop suggesting @strict in copilot instructions**

*Copilot instructions should no longer suggest @strict as it’s outdated and spams regular pull requests.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3159](https://github.com/microsoft/TypeScript-go/pull/3159) (Open, **jakebailey**, **Copilot**)

**Fix format selection deleting comments when selection ends inside comment trivia**

*Formatting a code selection that ends inside a block comment removes the comment entirely.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3160](https://github.com/microsoft/TypeScript-go/pull/3160) (Closed, **jakebailey**, **Copilot**)

**Add \`\<\` trigger and \`\)\` retrigger characters for signature help**

*Include '<' as a signature help trigger and ')' as a retrigger character to match VS Code's TypeScript extension*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3161](https://github.com/microsoft/TypeScript-go/pull/3161) (Open, **jakebailey**, **Copilot**)

**Fix documentation inheritance for static method overrides on mixin intersection types**

*Overridden static methods on mixin intersection classes lose inherited documentation due to incomplete base type resolution of static members*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3162](https://github.com/microsoft/TypeScript-go/pull/3162) (Closed)

**Organize imports comment duplication**

*OrganizeImports source action duplicated comments above export statements, resulting in repeated comment blocks.*

 * created by **johnfav03**

### [Issue microsoft/TypeScript-go#785](https://github.com/microsoft/TypeScript-go/issues/785) (Closed, `Domain: Emit`)

**support for \`useDefineForClassFields\`**

*Request for guidance to implement support for the TypeScript useDefineForClassFields setting in tsgo to correctly emit class field initializers*

 * [48 weeks ago](https://github.com/microsoft/TypeScript-go/issues/785#issuecomment-2810781594) **jakebailey** explained that getScriptTransformers was the closest available but other transforms were not implemented and the emit feature was not recommended outside limited syntax
 * [46 weeks ago](https://github.com/microsoft/TypeScript-go/issues/785#issuecomment-2837382110) **tmm1** noted that #819 added an `esnext` transform into a new internal package, creating a clear location to add classFields and decorator support in `transformers.GetScriptTransformers`
 * **jakebailey** added label `Domain: Emit`
 * [today](https://github.com/microsoft/TypeScript-go/issues/785#issuecomment-4088092365) **jakebailey** said "I did this in #2956 but forgot to close this."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#843](https://github.com/microsoft/TypeScript-go/issues/843) (Closed, `Domain: Emit`, `Domain: Declaration Emit`, `Domain: JS`, **sandersn**)

**pretty\-printing reparsed JS nodes crashes on GetTypeNodePrecedence**

*Pretty-printing reparsed JSDocTypeExpression and JSDocTypeLiteral nodes triggers crashes in GetTypeNodePrecedence.*

 * (41 weeks ago) **jakebailey** added labels `Domain: Emit`, `Domain: Declaration Emit`, `Domain: JS`
 * [today](https://github.com/microsoft/TypeScript-go/issues/843#issuecomment-4088095905) **jakebailey** said "I'm going to close this for now given formatting is now very heavily tested in fourslash"
 * (today) **jakebailey** closed the issue

