# Report for 2026-05-29 (Friday, May 29th, 2026)

12 different users commented on 39 different issues.

## Recommended Actions

 * Response Recommended
    * @doylio provided a heap profile as requested in [microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4577836639)

## Activity Summary

### [Issue microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032) (Closed, `Domain: Editor`, `Needs More Info`)

**tsgo \-\-lsp memory leak on large projects / triggers OOM**

*The tsgo LSP process in the TypeScript Native Preview extension leaks memory when handling large projects, causing OOM on low-RAM Linux machines.*

 * **andrewbranch** added label `Needs More Info`
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4039686371) **huseeiin** reported that the issue no longer reproduced after migrating from Arch to Debian
 * (11 weeks ago) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4577836639) **doylio** reported experiencing the issue regularly and provided a heap profile
 * [today](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4578621535) **andrewbranch** said "@doylio it seems like that profile got truncated during upload. Can you try again?"

### [PR microsoft/TypeScript-go#3212](https://github.com/microsoft/TypeScript-go/pull/3212) (Closed)

**Fix error spans for \`@satisfies\`**

*Fix error span calculation for @satisfies to ensure accurate error highlighting.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3212#issuecomment-4478733292) **jakebailey** said "This is failing all the tests"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3212#issuecomment-4489235370) **Andarist** apologized that syncing with main introduced test failures
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3842](https://github.com/microsoft/TypeScript-go/issues/3842) (Closed, `bug`, **ahejlsberg**)

**Missing support for namespaces in JSDoc types**

*Reinstate nested JSDoc typedef namespace support in tsgo, as the .d.ts workaround breaks single-file typing workflows.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (yesterday) **ahejlsberg** added label `bug`, and removed label `Needs Investigation`
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4008](https://github.com/microsoft/TypeScript-go/pull/4008) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix intermittent TS2345 with paths \+ @types/\* conflict in concurrent builds**

*Concurrent tsgo builds intermittently fail TS2345 because a race in the packageJsonInfoCache causes path aliases to resolve to @types packages.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4008#issuecomment-4502040125) **Copilot** added a compiler test for path alias trailing slash conflict with @types/react and noted existing unit tests reproducing the cache race
 * (1 week ago) **RyanCavanaugh** closed the issue
 * (today) **andrewbranch** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/4008#issuecomment-4579739549) **Copilot** extracted duplicated directory correction into InfoCacheEntry.WithPackageDirectory with explanatory comment

### [Issue microsoft/TypeScript-go#4037](https://github.com/microsoft/TypeScript-go/issues/4037) (Closed, `bug`, **ahejlsberg**)

**TS2304 when a generic \(@template\) function JSDoc contains @overload**

*Generic functions documented with @template and @overload produce 'Cannot find name T' TS2304 errors in tsgo.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4547708507) **antichris** lamented lack of arrow function overloading support, said they would have to rewrite their overloaded arrow functions as declarations, and thanked the maintainers
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4549213250) **ahejlsberg** proposed a TypeScript overload translation from JSDoc overloads and said they would include it in their PR
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4556263858) **ahejlsberg** explained that the JSDoc @type annotation on the variable and tags on the function expression already worked and suggested recommending that pattern for overloads
 * [today](https://github.com/microsoft/TypeScript-go/issues/4037#issuecomment-4580165398) **antichris** described having to rewrite code around overloaded arrow functions using single-use consts for type checking, deemed it not ideal but workable, and thanked maintainers

### [PR microsoft/TypeScript-go#4065](https://github.com/microsoft/TypeScript-go/pull/4065) (Closed)

**Revise logic for gathering JSDoc \`@template\` type parameters**

*Revise JSDoc @template parameter gathering logic to fix issue 4037 and document differences in CHANGES.md.*

 * created by **ahejlsberg**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4065#issuecomment-4580869494) **ahejlsberg** explained that Strada collects all @template tags across the JSDoc block and provided an example using separate JSDoc comments for individual overload type parameters

### [PR microsoft/TypeScript-go#4072](https://github.com/microsoft/TypeScript-go/pull/4072) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix tsdk relative path overwrite and unnecessary prompt on workspace open**

*Prevent committed relative tsdk paths from being overwritten with absolute paths and suppress redundant workspace version prompts.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4569008721) **Copilot** stated that the issue was fixed in commit 0f8de0c
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4569028963) **DanielRosenwasser** requested more feedback and asked about built-in TS extension behavior with an explicit tsdk even after workspace trust
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4569059752) **Copilot** addressed both reviewer points regarding restart on early-return and multi-root workspaces path resolution and explained the built-in TS extension tsdk prompt behavior
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578280565) **Copilot** acknowledged that useWorkspaceTsdkStorageKey is a trust gate, removed the silent auto-opt-in block, updated the prompt to always fire on fresh clone, ensured that allowing preserves existing tsdk setting, and referenced fix in commit 1cc3f16
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578410938) **andrewbranch** said "@copilot what happens when the user changes their tsdk version away from the workspace version to the built-in one? In the old TypeScript extension, this doesn't persist a JSON settings change."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578463576) **Copilot** explained changes to the “Use Bundled Version” path to toggle a flag instead of updating the tsdk setting in settings.json, avoiding dirtying the file, and noted it was fixed in commit 2506adb
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578683832) **andrewbranch** said "@copilot setting useWorkspaceTsdkStorageKey to false will re-trigger the prompt..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578730648) **Copilot** fixed prompt suppression logic by setting suppressPromptWorkspaceTsdk when selecting bundled TypeScript and clearing it when switching back
 * [today](https://github.com/microsoft/TypeScript-go/pull/4072#issuecomment-4578900164) **Copilot** extracted `relativeWorkspacePath` as a constant and used it for both `joinPath` and the relative tsdk path calculation

### [PR microsoft/TypeScript-go#4073](https://github.com/microsoft/TypeScript-go/pull/4073) (Closed)

**Restore JSDoc namespace declarations**

*Simplifies JSDoc handling and adds reparsed node remapping to restore namespace declarations for Quick Info, find references, and rename support.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4074](https://github.com/microsoft/TypeScript-go/pull/4074) (Closed)

**Fix stale pull diagnostics after document edits**

*Implement request-time document snapshots and freshness checks to avoid applying stale diagnostics after edits.*

 * created by **Kelpy2004**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4074#issuecomment-4575919369) **Kelpy2004** asked whether @jakebailey was the right person to review the follow-up on microsoft/vscode#317522 and offered to adjust the approach
 * [today](https://github.com/microsoft/TypeScript-go/pull/4074#issuecomment-4577393478) **jakebailey** questioned why the requirement was needed and suggested that stale diagnostics were an LSP client bug
 * [today](https://github.com/microsoft/TypeScript-go/pull/4074#issuecomment-4577406329) **jakebailey** said "The comments on the linked issue also mentions the client so I'm not sure where this comes from"
 * (today) **Kelpy2004** closed the issue

### [Issue microsoft/TypeScript-go#4075](https://github.com/microsoft/TypeScript-go/issues/4075) (Closed)

**TS7009 on new of default\-imported untyped CommonJS constructor — passes in tsc 6\.0, fails in tsgo**

*Instantiating a default-imported untyped CommonJS constructor triggers TS7009 in tsgo but succeeds in tsc 6.0.*

 * created by **benasher44**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4075#issuecomment-4582425692) **hkleungai** marked the issue as a duplicate of issue #3715 and confirmed that typechecking legacy JS syntax is out of scope for tsgo

### [Issue microsoft/TypeScript-go#4076](https://github.com/microsoft/TypeScript-go/issues/4076) (Closed, **DanielRosenwasser**, **Copilot**)

**Unexpected errors for modifiers on \`@template\` type parameters**

*Modifiers on JSDoc @template type parameters trigger erroneous TS1274 errors due to missing grammar checking logic.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4076#issuecomment-4582958541) **ahejlsberg** said "#4100 has the correct fix for this issue. The Copilot attempt is just wrong."

### [PR microsoft/TypeScript-go#4077](https://github.com/microsoft/TypeScript-go/pull/4077) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix grammar checks for modifiers on \`@template\` type parameters**

*Correct JSDoc @template in/out/const modifier grammar checks by resolving the proper host declaration to prevent TS1274 errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#4078](https://github.com/microsoft/TypeScript-go/pull/4078) (Closed, **DanielRosenwasser**)

**Quick info & find\-all\-refs tests for JSDoc namespaces**

*Add quick info and find-all-references tests for JSDoc namespaces following issue #4073.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#4079](https://github.com/microsoft/TypeScript-go/issues/4079) (Open)

**Behavior difference: Notable difference regarding optional function argument type emits**

*tsgo outputs extra parentheses and verbose optional argument types unlike tsc’s simpler inferred function signatures.*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#4080](https://github.com/microsoft/TypeScript-go/issues/4080) (Open)

**Add API to detect wherever a symbol is readonly**

*Add APIs to TypeScript's type checker for detecting whether a symbol is readonly or optional.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript-go#4081](https://github.com/microsoft/TypeScript-go/issues/4081) (Open)

**Add API to get symbol type that respects the \`exactOptionalPropertyTypes\` option**

*Propose enhancing TypeScript’s symbol type retrieval API to honor exactOptionalPropertyTypes for both object and mapped types.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript-go#4082](https://github.com/microsoft/TypeScript-go/issues/4082) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Panic in declaration emit for a set accessor with no parameters**

*A set accessor without parameters causes a panic in the typescript-go printer due to an AST node type mismatch.*

 * created by **mds-ant**
 * **mds-ant** added label `Crash`

### [Issue microsoft/TypeScript-go#4083](https://github.com/microsoft/TypeScript-go/issues/4083) (Closed)

**Panic on overlapping wildcard patterns**

*The resolver panics with a slice bounds out of range error when handling overlapping wildcard patterns in module resolution.*

 * created by **mds-ant**
 * (later) **mds-ant** closed the issue

### [Issue microsoft/TypeScript-go#4084](https://github.com/microsoft/TypeScript-go/issues/4084) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Panic in \`tryLoadInputFileForPath\` when an exports/imports target equals the declarationDir/outDir**

*A slice bounds panic occurs in tryLoadInputFileForPath when an exports or imports target matches declarationDir or outDir.*

 * created by **mds-ant**
 * **mds-ant** added label `Crash`

### [Issue microsoft/TypeScript-go#4085](https://github.com/microsoft/TypeScript-go/issues/4085) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Panic on overlapping wildcard patterns**

*A slice bounds out-of-range panic occurs when resolving modules with overlapping wildcard patterns in typescript-go.*

 * created by **mds-ant**
 * **mds-ant** added label `Crash`

### [Issue microsoft/TypeScript-go#4086](https://github.com/microsoft/TypeScript-go/issues/4086) (Closed, `Crash`, **jakebailey**, **Copilot**)

**Panic on \`"target": null\` \(or any enum\-typed option set to null\) in tsconfig\.json**

*tsconfig.json parsing panics with interface conversion error when an enum option (e.g., target) is null*

 * created by **mds-ant**
 * **mds-ant** added label `Crash`

### [Issue microsoft/TypeScript-go#4087](https://github.com/microsoft/TypeScript-go/issues/4087) (Closed)

**Spurious \`export\` modifier injected into a constructor type in \.d\.ts output**

*tsgo incorrectly injects an export modifier into constructor type declarations in generated .d.ts files*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4088](https://github.com/microsoft/TypeScript-go/issues/4088) (Closed, **jakebailey**, **Copilot**)

**Expando function inside a namespace emits \`export declare namespace\`**

*tsgo wrongly emits export declare namespace for a function's expando property inside a namespace, breaking the declaration file.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4089](https://github.com/microsoft/TypeScript-go/issues/4089) (Closed, **jakebailey**, **Copilot**)

**\`super\.m\(\)\` in a downleveled async function's parameter default survives into the inner \`function\*\`**

*tsgo downlevels async functions incorrectly retain super.m() in default parameters, causing a syntax error in the inner generator.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4090](https://github.com/microsoft/TypeScript-go/issues/4090) (Closed, **jakebailey**, **Copilot**)

**Imported/exported identifier used as a shorthand destructuring default initializer is not rewritten**

*Shorthand destructuring default initializers of imported identifiers aren't converted to the module alias, causing undefined reference errors.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4091](https://github.com/microsoft/TypeScript-go/issues/4091) (Closed, **jakebailey**, **Copilot**)

**JSX hex entity with uppercase marker decoded by tsgo, left literal by tsc**

*tsgo incorrectly decodes uppercase hexadecimal character entities in JSX to their literal characters, unlike tsc which leaves them intact.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4092](https://github.com/microsoft/TypeScript-go/issues/4092) (Open, **jakebailey**, **Copilot**)

**Lone surrogate in enum member name / const enum value is corrupted to U\+FFFD in emitted JS**

*tsgo emits U+FFFD in place of lone surrogates in enum member names and const enum values in the generated JavaScript*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4093](https://github.com/microsoft/TypeScript-go/issues/4093) (Closed, **jakebailey**, **Copilot**)

**design:type metadata for \`bigint\` omits the \`typeof BigInt === "function"\` runtime fallback below ES2020**

*tsgo emits design:type metadata for bigint without the runtime fallback check that TypeScript includes for ES2015 targets*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4094](https://github.com/microsoft/TypeScript-go/issues/4094) (Closed, **jakebailey**, **Copilot**)

**Emitted JSX factory differs for @jsx pragma preceded by another @token in the same comment**

*tsgo misparses an @jsx pragma preceded by another token in the same comment, emitting h instead of React.createElement.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4095](https://github.com/microsoft/TypeScript-go/issues/4095) (Closed, **jakebailey**, **Copilot**)

**Namespace import used only by a type\-only \`export import X = ns\.Y\` is not elided**

*tsgo retains a namespace import used only by a type-only export-import alias instead of eliding it like TypeScript 6.0 does.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4096](https://github.com/microsoft/TypeScript-go/issues/4096) (Closed, **jakebailey**, **Copilot**)

**Downleveled async arrow in a static field initializer captures the wrong \`this\`**

*Downleveling a static async arrow function initializer incorrectly captures the outer this rather than the class constructor.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4097](https://github.com/microsoft/TypeScript-go/issues/4097) (Closed, **jakebailey**, **Copilot**)

**Enum member named with a Unicode escape emits the raw escape text**

*Using a Unicode escape to name an enum member causes tsgo to emit the raw escape text rather than the actual character, resulting in undefined values.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4098](https://github.com/microsoft/TypeScript-go/issues/4098) (Closed, **jakebailey**, **Copilot**)

**tsgo drops TS2527 and emits an invalid \.d\.ts when a class member's inferred type is an object literal containing \`this\`**

*tsgo ignores a TS2527 error and produces an invalid .d.ts file when a class method returns an object literal containing this.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4099](https://github.com/microsoft/TypeScript-go/issues/4099) (Closed)

**A single legacy \`assert {\.\.\.}\` import suppresses every semantic diagnostic in the program**

*A single legacy import assert in tsgo emits only the assertion deprecation error and suppresses subsequent type-check diagnostics.*

 * created by **mds-ant**

### [PR microsoft/TypeScript-go#4100](https://github.com/microsoft/TypeScript-go/pull/4100) (Closed)

**Fix grammar checking for \`in\` and \`out\` modifiers in \`@template\` tags**

*Fix grammar checking for in and out modifiers in @template tags.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#4101](https://github.com/microsoft/TypeScript-go/issues/4101) (Open, `Needs More Info`)

**Declaration emit spends significant CPU in getAliasForSymbolInContainer / getAlternativeContainingModules**

*Declaration emit spends excessive CPU time in getAlternativeContainingModules and getAliasForSymbolInContainer, causing slow builds.*

 * created by **Zzzen**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4583182120) **jakebailey** assured that the pprof files contain no sensitive information and can be shared as-is

### [PR microsoft/TypeScript-go#4102](https://github.com/microsoft/TypeScript-go/pull/4102) (Open)

**Cache alias candidates for symbol accessibility**

*Cache alias candidates to optimize symbol accessibility resolution.*

 * created by **Zzzen**

