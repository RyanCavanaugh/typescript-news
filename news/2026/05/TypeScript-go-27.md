# Report for 2026-05-27 (Wednesday, May 27th, 2026)

11 different users commented on 26 different issues.

## Recommended Actions

 * Response Recommended
    * @dimikot asked which version @mscrivo was on when it was working in [microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4560952310)
    * @mscrivo provided repro steps identifying the problematic version in [microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4564424105)
    * @mscrivo provided environment details about where the issue occurs in [microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4564450769)

## Activity Summary

### [Issue microsoft/TypeScript-go#3320](https://github.com/microsoft/TypeScript-go/issues/3320) (Open, `Domain: Editor`, **iisaduan**)

**Missing \`removeUnused\` code fix/code action**

*The removeUnused code action and underlying unused identifier fixes are not implemented for VSCode’s TypeScript codeActionOnSave.*

 * (6 weeks ago) **RyanCavanaugh** added label `Domain: Editor`, and set milestone to `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3320#issuecomment-4554817607) **a-tarasyuk** asked whether implementing support for removeUnused/removeUnusedImports/unusedIdentifier was still considered useful
 * [today](https://github.com/microsoft/TypeScript-go/issues/3320#issuecomment-4558953630) **iisaduan** noted that removeUnusedImports was already implemented and that other code actions would be considered for a post-7.0 release pending feedback

### [Issue microsoft/TypeScript-go#3661](https://github.com/microsoft/TypeScript-go/issues/3661) (Closed, `Needs Investigation`, **iisaduan**)

**Behavior difference: tsgo emits an "extra" TS7006 along with TS2769 at the same line in case of overload mismatch**

*tsgo redundantly emits both TS2769 and TS7006 errors for an overload mismatch call, unlike tsc.*

 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3661#issuecomment-4549508851) **weswigham** said "This, AFAIK, was an intentional strictness improvement to JS signature analysis - it's intentionally no longer lax on argument count in JS to match TS behavior."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3661#issuecomment-4558913734) **iisaduan** said "Agreed, intentional improvement, it now matches the TS behavior."
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#3801](https://github.com/microsoft/TypeScript-go/issues/3801) (Closed, `bug`, `Domain: Editor`, `Crash`, **RyanCavanaugh**, **gabritto**, **Copilot**)

**Unhandled case when auto\-completing decorator on private method under \-\-experimentalDecorators**

*Autocompleting a decorator on a private class method with experimentalDecorators enabled causes a panic due to an unhandled case in getClassElementPropertyKeyType.*

 * (2 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3819](https://github.com/microsoft/TypeScript-go/pull/3819) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix panic in getClassElementPropertyKeyType for private identifiers**

*Add KindPrivateIdentifier case to getClassElementPropertyKeyType to prevent panics when completing decorators on private class members.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#4000](https://github.com/microsoft/TypeScript-go/issues/4000) (Open, `enhancement`)

**Make typedef exporting explicit**

*Propose introducing a new @export JSDoc tag to explicitly mark exported typedefs and type re-exports in TypeScript 7*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4000#issuecomment-4497729784) **ahejlsberg** rejected the suggestion to add new JSDoc features and recommended writing the code in TypeScript
 * **ahejlsberg** added label `enhancement`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4000#issuecomment-4507848992) **remcohaszing** noted the trade-offs between JavaScript and TypeScript and suggested issue #58250 as an alternative solution to type export dependency concerns
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4004](https://github.com/microsoft/TypeScript-go/issues/4004) (Closed, `duplicate`)

**Spurious "multiple properties with the same name" errors for unpaired surrogates**

*tsgo incorrectly reports duplicate property name errors for object literals using unpaired Unicode surrogate keys.*

 * created by **blickly**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4004#issuecomment-4502260136) **RyanCavanaugh** said "Same root cause as #3899"
 * **RyanCavanaugh** added label `duplicate`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4030](https://github.com/microsoft/TypeScript-go/pull/4030) (Closed)

** Add classified text output for VS Find All References**

*Add classified text output for VS Find All References to restore syntax-highlighted definitions and prevent related crashes.*

 * created by **navya9singh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4030#issuecomment-4558278472) **navya9singh** tested omitting MarkerTagType and Style and updated the code generator to use omitzero for null or zero values
 * (today) **navya9singh** closed the issue

### [Issue microsoft/TypeScript-go#4038](https://github.com/microsoft/TypeScript-go/issues/4038) (Closed, `bug`, **ahejlsberg**)

**TS2315 when using \`@template\` more than once in a file**

*tsgo misreports TS2315 'export=' is not generic when a file contains more than one JSDoc @template declaration.*

 * (3 days ago) **ahejlsberg** added label `bug`, and set milestone to `TypeScript 7.0 RC`
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4038#issuecomment-4529508062) **ahejlsberg** explained that resolveEntityName only invoked resolveAlias once and promised a PR to add multiple invocations for CommonJS modules with exported type declarations
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4043](https://github.com/microsoft/TypeScript-go/pull/4043) (Closed)

**Resolve aliases in \`resolveEntityName\` until we find the given meaning**

*Allow resolveEntityName to follow alias chains until the desired symbol meaning is found*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4043#issuecomment-4556634306) **weswigham** confirmed that getTargetOfAliasDeclaration lacked the dontRecursivelyResolve=false default, causing getImmediateAliasedSymbol and resolveAlias to behave identically
 * [today](https://github.com/microsoft/TypeScript-go/pull/4043#issuecomment-4556865031) **ahejlsberg** clarified that resolveAlias resolves until a non-alias meaning while getImmediateAliasedSymbol resolves only a single indirection, and noted that the infrastructure was revised in PR #2168
 * [today](https://github.com/microsoft/TypeScript-go/pull/4043#issuecomment-4556916542) **ahejlsberg** explained that the PR fixes the missing second resolveAlias call needed to obtain the type meaning of an alias layered with a namespace meaning
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4043#issuecomment-4557484303) **weswigham** noted that the recently enabled alias/namespace merge for JS files required multiple resolveAlias calls and that other code assumes a full resolution walk

### [PR microsoft/TypeScript-go#4054](https://github.com/microsoft/TypeScript-go/pull/4054) (Closed)

**Fix configuration lookups and prefer saving as \`js/ts\`**

*Favor workspace-specific TypeScript useTsgo settings over global JS/TS, migrate deprecated keys, and stop server startup when disabled in development.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#4055](https://github.com/microsoft/TypeScript-go/issues/4055) (Closed, `wontfix`, **ahejlsberg**)

**Type recursion limit \(TS2589\) on recursive mapped types**

*The recursive mapped type Draft<T> triggers a TS2589 excessive recursion error when assigning a nested Conversation property due to exceeding TypeScript’s type instantiation depth*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4055#issuecomment-4558346598) **ahejlsberg** clarified that the deep instantiation error was intended, that TS6 sometimes failed to report it, that it was fixed in TS7 by #3445, and that TS6 reports it in the CLI but not in the IDE due to type check ordering
 * (today) **ahejlsberg** added label `wontfix`, and removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4058](https://github.com/microsoft/TypeScript-go/pull/4058) (Open)

**Reparse non\-identifier jsdoc names where possible, error otherwise**

*The parser now reparses non-identifier JSDoc names when possible and errors on unsupported nameless typedef patterns.*

 * created by **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4549523307) **DanielRosenwasser** said "Can we give a more-specialized error message for reserved names?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4058#issuecomment-4556668076) **weswigham** clarified that keywords were allowed as identifiers and that the check concerned only actual allowed characters in JS identifiers

### [Issue microsoft/TypeScript-go#4059](https://github.com/microsoft/TypeScript-go/issues/4059) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**reference directive caused issue with ts\-check**

*Placing a triple-slash reference directive after a // @ts-check comment causes tsgo to bypass type-checking, effectively acting like ts-nocheck.*

 * created by **jasonlyu123**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4060](https://github.com/microsoft/TypeScript-go/issues/4060) (Open, `Crash`)

**Data race in module resolver — SIGSEGV in \`loadModuleFromTargetExportOrImport\` / \`OrderedMap\.Keys\` under concurrent goroutines**

*Concurrent access to OrderedMap.Keys within the module resolver's loadModuleFromTargetExportOrImport triggers a data race causing a SIGSEGV.*

 * created by **mscrivo**
 * **mscrivo** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4560057113) **DanielRosenwasser** requested the reporter to binary-search between the last known good version and 20260518 to identify the problematic version and offered an NDA for private code sharing
 * [today](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4560952310) **dimikot** said "@mscrivo What version were you at when it was working?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4564424105) **mscrivo** identified that the crash started in version 20260515.1 through a binary search and offered to provide repo access
 * [later](https://github.com/microsoft/TypeScript-go/issues/4060#issuecomment-4564450769) **mscrivo** suggested a related PR and noted that the issue only occurred on macOS arm machines, not on Linux CI runners

### [PR microsoft/TypeScript-go#4061](https://github.com/microsoft/TypeScript-go/pull/4061) (Open, **RyanCavanaugh**, **Copilot**)

**Preserve ts\-check across reference directives**

*Triple-slash reference directives were overriding ts-check pragmas and disabling type checking, so check-mode selection is now limited to ts-check/ts-nocheck pragmas*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4062](https://github.com/microsoft/TypeScript-go/pull/4062) (Open)

**Check \`this\` params when comparing pseudotype signatures to type signatures**

*Include `this` parameters in comparisons between pseudotype signatures and actual type signatures.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4063](https://github.com/microsoft/TypeScript-go/pull/4063) (Open)

**Warn on TSServer Plugin Contributions from other extensions**

*Display a warning when non-core extensions contribute TSServer plugins to prevent unexpected conflicts.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4064](https://github.com/microsoft/TypeScript-go/pull/4064) (Closed)

**Emit index components for computed names instead of signatures**

*Modify the compiler to emit index components for computed property names in generated code instead of signatures.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4065](https://github.com/microsoft/TypeScript-go/pull/4065) (Open)

**Revise logic for gathering JSDoc \`@template\` type parameters**

*Revise JSDoc @template parameter gathering logic to fix issue 4037 and document differences in CHANGES.md.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#4066](https://github.com/microsoft/TypeScript-go/issues/4066) (Open, `Domain: Editor`, `Crash`, **DanielRosenwasser**)

**Panic on file rename with solution\-style \`tsconfig\.json\`**

*File renaming with a solution-style tsconfig.json causes a nil pointer dereference panic in the Go-based TypeScript language service.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Domain: Editor`, `Crash`, and assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4067](https://github.com/microsoft/TypeScript-go/pull/4067) (Open)

**Fix file rename crashes when dealing with solution configuration files**

*Prevent crashes when renaming solution configuration files by improving file rename handling.*

 * created by **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4068](https://github.com/microsoft/TypeScript-go/pull/4068) (Open, `dependencies`, `javascript`)

**Bump tmp from 0\.2\.5 to 0\.2\.7**

*Upgrade tmp dependency from version 0.2.5 to 0.2.7 to include input validation and relative path checks.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [PR microsoft/TypeScript-go#4069](https://github.com/microsoft/TypeScript-go/pull/4069) (Open)

**Fix JS bind expando declaration emit**

*Emit bound JS functions as proper function declarations with preserved expando properties instead of const alias types*

 * created by **cjc0013**

### [Issue microsoft/TypeScript-go#4070](https://github.com/microsoft/TypeScript-go/issues/4070) (Open, `Needs Investigation`, **DanielRosenwasser**, **Copilot**)

**typescript\.native\-preview\.tsdk: relative path in committed \.vscode/settings\.json gets overwritten with absolute path when accepting the workspace version prompt**

*Accepting the workspace version prompt for TypeScript Native Preview converts a relative tsdk path to an absolute one, dirtying settings.*

 * created by **Cellule**

