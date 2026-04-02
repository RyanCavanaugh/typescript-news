# Report for 2026-03-17 (Tuesday, March 17th, 2026)

15 different users commented on 38 different issues.

## Recommended Actions

 * Response Recommended
    * @bradleyayers reported an issue with duplicated comments in exports and provided example test cases in [microsoft/TypeScript-go#2331](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-4080425624)
    * @tian000 asked for an update from @jakebailey in [microsoft/TypeScript-go#3107](https://github.com/microsoft/TypeScript-go/pull/3107#issuecomment-4083620382)

## Activity Summary

### [Issue microsoft/TypeScript-go#1997](https://github.com/microsoft/TypeScript-go/issues/1997) (Closed, `bug`, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**Formatting adds stray space at end of block**

*Range or document formatting of a TypeScript block erroneously leaves a stray space before its closing brace.*

 * created by **DanielRosenwasser**
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1997#issuecomment-3475237375) **DanielRosenwasser** said "Found this at #1995."
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1997#issuecomment-4077300293) **DanielRosenwasser** said "Seems to not happen anymore on this example, but #3119 was just opened."
 * (today) **DanielRosenwasser** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/1997#issuecomment-4077307825) **DanielRosenwasser** said "Actually, I was using Strada."
 * (today) **DanielRosenwasser** added label `bug`, and assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2081](https://github.com/microsoft/TypeScript-go/issues/2081) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**Missing error when reference directive file path doesn't exist**

*tsgo fails to report an error for a nonexistent reference directive file path, unlike tsc which raises TS6053.*

 * **RyanCavanaugh** added label `bug`
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2081#issuecomment-3533962637) **TranNhatHan** said "Is it considered as the new TS design or a bug? I would like to fix this."
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2081#issuecomment-3533996173) **jakebailey** said "Bug, there should be an error; some code is just not ported."
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2331](https://github.com/microsoft/TypeScript-go/pull/2331) (Closed)

**Organize Imports**

*Implement functionality to automatically organize and sort imports within source files.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3825049874) **johnfav03** updated code to handle shebang and indent size, noted LSP sync issue, and explained that require sorting matches TypeScript’s import order
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-3825234891) **jakebailey** said "I think there's a bug in the way we load indent size out of the settings; it's some discrepency i noticed when working on my user prefs refactor. VS Code's setting has a different name than we do."
 * (5 weeks ago) **johnfav03** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/2331#issuecomment-4080425624) **bradleyayers** reported an issue with duplicated comments on exports and provided example test cases

### [PR microsoft/TypeScript-go#2459](https://github.com/microsoft/TypeScript-go/pull/2459) (Closed)

**Port \-\-isolatedDeclarations related node builder logic, with baseline updates**

*Port node builder logic for the --isolatedDeclarations option and apply baseline updates for review.*

 * created by **weswigham**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-3827377748) **Zzzen** described testing the branch and noting the type emit was cleaner, reported still hitting OOM, and asked for tips on pinpointing memory usage
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-3835290600) **Zzzen** reported that setting GOMEMLIMIT=10GiB enabled full compilation and expressed excitement for the PR to land
 * [today](https://github.com/microsoft/TypeScript-go/pull/2459#issuecomment-4077945493) **jakebailey** demonstrated that the smoke test didn’t catch the issue because build mode wasn’t used and reproduced a TS9013 error output

### [Issue microsoft/TypeScript-go#2576](https://github.com/microsoft/TypeScript-go/issues/2576) (Closed, **andrewbranch**, **Copilot**)

**Autocompletions and quick fix suggestions try to import from "@types" packages**

*tsgo quick fixes and autocompletions wrongly import from @types packages instead of real modules*

 * **andrewbranch** assigned to **andrewbranch**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2576#issuecomment-4054083735) **dan-proudfoot-bots** said "Still noticing this as of today - it makes suggestions for external packages basically useless"
 * **andrewbranch** assigned to **Copilot**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2819](https://github.com/microsoft/TypeScript-go/pull/2819) (Closed, **jakebailey**, **Copilot**)

**Port TS PR \#62418: Add diagnostic when rootDir inference changes output layout**

*Add TS5011 diagnostic in Go compiler when inferred rootDir layout differs from computed common source directory.*

 * **Copilot** assigned to **jakebailey**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2819#issuecomment-3969844310) **jakebailey** asked to look into the submodule for changed tsbuild tests and update the Go versions to match to avoid extra output errors
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2819#issuecomment-3969925576) **Copilot** verified all changed tsbuild baselines against the TS submodule and concluded no Go test updates were needed
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3053](https://github.com/microsoft/TypeScript-go/pull/3053) (Closed)

**port linked editing**

*Port linked editing functionality and update its regular and baseline fourslash tests.*

 * created by **iisaduan**
 * (today) **iisaduan** closed the issue

### [PR microsoft/TypeScript-go#3084](https://github.com/microsoft/TypeScript-go/pull/3084) (Open)

**Port LSP update imports on file rename support**

*Adds support to update import paths via LSP when files are renamed or moved to ensure correct relative references.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4069834603) **anchmelev** pinged the reviewer for a review on LSP import updates including file rename/move support and tests
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4070678965) **DanielRosenwasser** asked why the tests didn't use the typical fourslash test harness and whether existing tests from the old compiler were considered for porting
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4071505057) **anchmelev** thanked DanielRosenwasser, moved the semantic workspace/willRenameFiles coverage to the fourslash harness, trimmed direct server tests to LSP wire-up assertions, added relevant getEditsForFileRename coverage for non-relative imports, and omitted directory/tsconfig-specific variants
 * [today](https://github.com/microsoft/TypeScript-go/pull/3084#issuecomment-4076493957) **jakebailey** explained that they avoid adding unit tests for this behavior and expected existing fourslash tests to be converted, since they cannot verify the ported tests otherwise

### [PR microsoft/TypeScript-go#3089](https://github.com/microsoft/TypeScript-go/pull/3089) (Closed, **andrewbranch**, **Copilot**)

**Fix auto\-import suggesting "@types" package specifiers instead of real package names**

*Update auto-import logic to favor actual package names over @types specifiers when both are installed*

 * **Copilot** assigned to **andrewbranch**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3089#issuecomment-4056790526) **andrewbranch** questioned whether the original bug was reproduced or a different bug was fixed, noting that “no suggestions” and “incorrect @types/react specifiers” are distinct behaviors
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3089#issuecomment-4057007192) **Copilot** clarified the distinction between no suggestions and incorrect `@types` specifiers, reproduced the incorrect specifier case in updated tests, and explained the normalization fix
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3107](https://github.com/microsoft/TypeScript-go/pull/3107) (Closed, **jakebailey**, **Copilot**)

**Fix project reference redirect ordering when file belongs to multiple sub\-projects**

*Reverse project reference mapping order to apply parent tsconfig mappings before child projects, preserving customConditions and moduleSuffixes.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3107#issuecomment-4083620382) **tian000** said "@jakebailey any update here!"

### [PR microsoft/TypeScript-go#3113](https://github.com/microsoft/TypeScript-go/pull/3113) (Closed)

**Stop converting lsproto Ranges/Positions to pointers and back**

*Eliminate unnecessary pointer conversions for lsproto Ranges and Positions to simplify code and reduce overhead.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3115](https://github.com/microsoft/TypeScript-go/pull/3115) (Closed)

**Avoid extra allocations for enum inlining comments**

*Use a single builder for enum inlining comments to eliminate extra allocations from replacements and concatenations.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3116](https://github.com/microsoft/TypeScript-go/pull/3116) (Closed)

**Remove gofumpt as go\.mod tool, use dprint**

*Switch code formatting tooling from gofumpt to dprint in go.mod to reduce dependencies and avoid version skew.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3119](https://github.com/microsoft/TypeScript-go/issues/3119) (Closed)

**Formatter adds a space at the end of file containing a class**

*tsgo's formatter adds an unwanted trailing space after a class's closing brace, unlike typescript@6.0 which omits it.*

 * created by **PeterStaev**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3119#issuecomment-4077312569) **DanielRosenwasser** said "Might be the same as #1997, I've kicked something off."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3119#issuecomment-4083576806) **PeterStaev** said "From what I see this has been fixed in the latest version! Thanks for the quick turnaround!"
 * (later) **PeterStaev** closed the issue

### [Issue microsoft/TypeScript-go#3121](https://github.com/microsoft/TypeScript-go/issues/3121) (Open, `Needs More Info`)

**extension gets uninstalled after around an hour on vscodium**

*The TypeScript Native Preview extension installed in VSCodium on Linux is uninstalled after about an hour for being flagged problematic.*

 * created by **huseeiin**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4076484678) **RyanCavanaugh** said "Download from where?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3121#issuecomment-4077173146) **huseeiin** recommended downloading the VSIX via VS Code’s extensions tab instead of VSCodium and provided a screenshot

### [PR microsoft/TypeScript-go#3122](https://github.com/microsoft/TypeScript-go/pull/3122) (Closed)

**Fix issue in \`checkIndexConstraints\`**

*Port fix and tests from an unported pull request to correct index constraint checking in TypeScript*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3123](https://github.com/microsoft/TypeScript-go/pull/3123) (Open)

**Fix auto\-import of subpath imports starting with \`\#/\` in supported module resolution modes**

*Update auto-import handling to recognize subpath imports beginning with '#/' in all supported resolution modes.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3124](https://github.com/microsoft/TypeScript-go/pull/3124) (Closed)

**Add \`globalThis\` name conflict check**

*Port a globalThis name conflict check from the legacy codebase to detect and prevent naming collisions.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3125](https://github.com/microsoft/TypeScript-go/pull/3125) (Closed)

**Fix error type intrinsic name**

*Correct intrinsic error type names to ensure accurate type baselines despite not being exposed to users.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3126](https://github.com/microsoft/TypeScript-go/pull/3126) (Open, **RyanCavanaugh**, **Copilot**)

**Emit TS6053 error for missing reference directive files**

*Emit TS6053 error for missing triple-slash reference files in the Go compiler, align noResolve behavior, and update baselines.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3127](https://github.com/microsoft/TypeScript-go/pull/3127) (Closed)

**Fixed some diagnostic writer divergences**

*Corrects diagnostic writer output to remove several format-diverging diffs.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3127#issuecomment-4077101045) **jakebailey** said "IIRC these were actually intentional differences. Note the lack of extra random newlines."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3127#issuecomment-4077119609) **Andarist** said "Should I add those to the accepted diffs then? what about the change to internal/parser/parser.go? "
 * (later) **Andarist** closed the issue

### [PR microsoft/TypeScript-go#3128](https://github.com/microsoft/TypeScript-go/pull/3128) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix \`anyTokenExcept\` including EOF token in formatting rules**

*Modify anyTokenExcept to use allTokens and exclude EOF, removing unwanted trailing spaces at end of file.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3128#issuecomment-4078512561) **DanielRosenwasser** said "Fixes #1997 and fixes #3119"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3128#issuecomment-4078760684) **DanielRosenwasser** said "@copilot address feedback, also use the right npm scripts to update the list of failing fourslash tests."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3128#issuecomment-4078796670) **Copilot** strengthened the trailing whitespace test and updated the failing tests list, resulting in 40 formatting tests passing
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3129](https://github.com/microsoft/TypeScript-go/pull/3129) (Closed)

**Validate JSON syntax during parse**

*Port missing JSON syntax validation into the parser to enable proper syntax checking.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3130](https://github.com/microsoft/TypeScript-go/pull/3130) (Closed)

**Improve fourslash conversion error reporting**

*Improve fourslash conversion error reporting to provide more detailed and actionable diagnostics*

 * created by **gabritto**
 * (later) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3131](https://github.com/microsoft/TypeScript-go/issues/3131) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Incorrect error diff: tsxElementResolution10**

*The tsxElementResolution10 error diff incorrectly omits the initial error stating '{ x: number }' is not a valid JSX element.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3131#issuecomment-4077855431) **RyanCavanaugh** said "This should also apply to Its return type of the variant message for function components"

### [PR microsoft/TypeScript-go#3132](https://github.com/microsoft/TypeScript-go/pull/3132) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix incorrect eliding of JSX error head messages in property mismatch diagnostics**

*Fix eliding of JSX error head messages in property mismatch diagnostics by adding those messages to suppression exceptions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3132#issuecomment-4078129898) **Copilot** scoped the fix to only the three JSX-related error heads (`Its_instance_type`, `Its_return_type`, `Its_element_type`) and removed three JSX baseline diffs

### [PR microsoft/TypeScript-go#3133](https://github.com/microsoft/TypeScript-go/pull/3133) (Closed, **RyanCavanaugh**, **Copilot**)

**docs: document that Corsa only shows errors for the last function overload**

*Add CHANGES.md entry explaining that Corsa reports only the last function overload error rather than all.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3134](https://github.com/microsoft/TypeScript-go/pull/3134) (Closed)

**Skip all tests that used typescript\.d\.ts**

*Skip all tests using typescript.d.ts since they are inherently broken.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3135](https://github.com/microsoft/TypeScript-go/pull/3135) (Closed)

**Misc CHANGES\.md additions**

*Add miscellaneous changelog entries to CHANGES.md covering most .errors.txt.diffs with submoduleAccepted.txt PR forthcoming.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3136](https://github.com/microsoft/TypeScript-go/pull/3136) (Closed)

**Update dependencies**

*Upgrade project dependencies to their latest stable versions.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3137](https://github.com/microsoft/TypeScript-go/pull/3137) (Closed)

**Fix all writestring analyzer errors**

*Manually ran the gopls writestring analyzer and corrected all reported errors.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3138](https://github.com/microsoft/TypeScript-go/pull/3138) (Closed)

**Reimplement \-\-showConfig**

*Reimplement the --showConfig command in tsoptions instead of JSON dumping, without inferred options printing.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Open, `Needs More Info`)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * created by **vetptzru**

### [Issue microsoft/TypeScript-go#3140](https://github.com/microsoft/TypeScript-go/issues/3140) (Closed)

**Reserved syntax error on generic function parameter**

*tsgo incorrectly flags both generic function declarations with and without trailing commas in .mts files as reserved syntax, unlike TypeScript 6.0.*

 * created by **StyleShit**

### [PR microsoft/TypeScript-go#3141](https://github.com/microsoft/TypeScript-go/pull/3141) (Closed)

**fix\(3140\): align typeParameters grammar check with Strada**

*Updates the conditional logic for typeParameters grammar checks to align with Strada’s implementation.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#3142](https://github.com/microsoft/TypeScript-go/pull/3142) (Closed)

**Match some submodule diagnostics for missing expressions**

*Match submodule diagnostics for missing expressions to eliminate 12 diffs.*

 * created by **Andarist**

