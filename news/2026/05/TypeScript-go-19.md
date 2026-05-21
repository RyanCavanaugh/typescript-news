# Report for 2026-05-19 (Tuesday, May 19th, 2026)

17 different users commented on 62 different issues.

## Recommended Actions

 * Response Recommended
    * @Zelys-DFKH reported lack of PR reviews and perceived the project as closed to outside contributions in [microsoft/TypeScript-go#3982](https://github.com/microsoft/TypeScript-go/pull/3982#issuecomment-4493150832)
    * @blickly asked if they should close this as WAI in [microsoft/TypeScript-go#3988](https://github.com/microsoft/TypeScript-go/issues/3988#issuecomment-4491654490)

## Activity Summary

### [PR microsoft/TypeScript-go#3232](https://github.com/microsoft/TypeScript-go/pull/3232) (Closed)

**Speed up lookupSymbolChain**

*Optimize lookupSymbolChain by caching alias-only symbol lists per table and refining iteration logic, reducing CPU time by 61%.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3232#issuecomment-4129842233) **jakebailey** drafted a comment admitting overexcitement and lamenting the lack of tests to prove the change wrong
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/3232#issuecomment-4270043008) **jakebailey** said "To be clear, I pushed to this PR with an updated solution which I believe is as fast and should be correct at the cost of another bit out of the key."
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3491](https://github.com/microsoft/TypeScript-go/issues/3491) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Excess\-property check fires on a nested object literal that is later assigned to an annotated return type, where tsc 6\.0 does not**

*TS7 incorrectly flags excess-property errors on nested object literals assigned via an untyped variable to a typed return, unlike TS6*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3491#issuecomment-4296214357) **Andarist** described having a fix for the issue, provided sample code illustrating the problem, and reconsidered when to call getWidenedType before submitting the PR
 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * (today) **ahejlsberg** added labels `Domain: Type Checking`, `Type Ordering`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3491#issuecomment-4491479178) **ahejlsberg** said "This appears to be a type ordering issue. Error also occurs with TS6 when compiled with --stableTypeOrdering."

### [Issue microsoft/TypeScript-go#3563](https://github.com/microsoft/TypeScript-go/issues/3563) (Closed, `wontfix`, **ahejlsberg**)

**Baselines: definiteAssignment shorthand in object literal loses optional modifier**

*Optional method properties in object literal shorthand lose their optional modifier when emitted with definite assignment assertions.*

 * **ahejlsberg** assigned to **ahejlsberg**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3563#issuecomment-4393068890) **ahejlsberg** asked whether to handle '?' modifiers on object literal properties and noted uncertainty about declaration emit behavior
 * **ahejlsberg** added label `wontfix`
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3618](https://github.com/microsoft/TypeScript-go/pull/3618) (Open)

**fix: prevent wildcard pattern from overriding exact match in FindBestPatternMatch**

*Assign math.MaxInt for exact matches in FindBestPatternMatch to ensure wildcard patterns cannot override exact matches.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4323606759) **jakebailey** said "This will require a test, preferably one we can cross check with the old code to double check it"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4331007584) **DanielRosenwasser** said "As far as I remember, this code path isn't supposed to be hit for an exact match. Did you actually run into a problem with a specific project?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4411656223) **kuishou68** identified that the Go port compared StarIndex instead of prefixLength, causing wildcard matches to overwrite exact matches, and offered to add a side-by-side test to verify the fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/3618#issuecomment-4492416380) **DanielRosenwasser** asked why the user was tracing tsconfig.json resolution for paths and reiterated that the pattern list wasn't supposed to be passed

### [PR microsoft/TypeScript-go#3673](https://github.com/microsoft/TypeScript-go/pull/3673) (Closed, **RyanCavanaugh**, **Copilot**)

**Bound \`createAnonymousTypeNodeEx\` reuse for recursive instantiation expression types**

*Wrap tryReuseExistingNonParameterTypeNode in createAnonymousTypeNodeEx with a visitedTypes guard to avoid infinite recursion on recursive instantiation expression types*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3701](https://github.com/microsoft/TypeScript-go/issues/3701) (Closed, **jakebailey**, **Copilot**)

**When using \`module=commonjs\`, Array destructuring is transpiled with wrong \(non\-iterator\) behavior**

*Compiling with module=commonjs wrongly transpiles exported array destructuring into fixed index access instead of iterator logic.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3701#issuecomment-4455680011) **jakebailey** asked for an explanation of necessity and queried if it was due to dropping ES5 and downlevelIteration
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3701#issuecomment-4464739228) **blickly** said "We set downlevelIteration even when targetting ES2015+ since we need iterator support.  With downlevelIteration going away, we don't want to lose support for iterators."
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3701#issuecomment-4464760179) **jakebailey** expressed confusion about how the option had any effect and declared issue #3705 ready to go
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3705](https://github.com/microsoft/TypeScript-go/pull/3705) (Closed, **jakebailey**, **Copilot**)

**Preserve native destructuring for CommonJS exports to keep iterator semantics**

*Preserve native destructuring semantics in CommonJS exports by reusing nodes, suppressing source maps, adding tests, and refining implementation.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4455898533) **blickly** questioned the need to follow both the iterator protocol and export ordering, noted that TypeScript 6 already had the same timing caveats with downlevelIteration, and asked for clarification on the meaning of 'the current (array-assuming) emit.'
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4456069964) **jakebailey** suggested using destructuring and dummy zero-based assignments to declare exports similar to esbuild
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4456094511) **jakebailey** noted that the complex code wasn’t needed and suggested using simple destructuring for exports since they are already declared
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3796](https://github.com/microsoft/TypeScript-go/pull/3796) (Closed)

**Hoist named class/function expressions assigned to module\.exports in JS declaration emit**

*Fix JS declaration emit to synthesize and hoist named classes or functions assigned to module.exports instead of default fallback.*

 * created by **inq**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3796#issuecomment-4420076536) **inq** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3796#issuecomment-4490549578) **weswigham** said "I think we'll be working on this over at #3850 instead, sorry!"
 * (today) **weswigham** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3796#issuecomment-4494073197) **inq** said "Great! Thank you!"

### [Issue microsoft/TypeScript-go#3829](https://github.com/microsoft/TypeScript-go/issues/3829) (Closed, `wontfix`, **ahejlsberg**)

**Behavior difference: tsgo fails to report TS8022 as tsc does**

*tsgo does not emit TS8022 errors for JSDoc '@extends' on non-class declarations in JavaScript files, unlike tsc*

 * (5 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3829#issuecomment-4491302350) **ahejlsberg** said "We discussed and we're going to close this as won't fix. In general we don't error on JSDoc tags occurring in places where they have no meaning and it seems odd to single out @extends here."
 * (today) **ahejlsberg** added label `wontfix`, and removed label `Needs Investigation`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3831](https://github.com/microsoft/TypeScript-go/pull/3831) (Closed)

**fix\(3829\): handle extends tag not attached to a class**

*Ensure extends tags that are not attached to any class declaration are properly handled.*

 * created by **a-tarasyuk**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3831#issuecomment-4445053253) **ahejlsberg** suggested relocating JSDoc error issuance to the reparser due to shared host-identification logic and potential for similar checks
 * (later) **a-tarasyuk** closed the issue

### [Issue microsoft/TypeScript-go#3842](https://github.com/microsoft/TypeScript-go/issues/3842) (Open, `Needs Investigation`, **ahejlsberg**)

**Missing support for namespaces in JSDoc types**

*Reinstate nested JSDoc typedef namespace support in tsgo, as the .d.ts workaround breaks single-file typing workflows.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3842#issuecomment-4453095244) **DanielRosenwasser** addressed conflict by suggesting using a non-declaration TypeScript file containing only ambient/emitless code
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3842#issuecomment-4454048561) **DanielRosenwasser** said "In this code, are you relying on others on the outside to reference simplematter as a type? Or is it just for local clarity?"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3842#issuecomment-4458520862) **remcohaszing** explained that declaration emit permits a non-declaration TypeScript file with ambient code but doesn’t allow merging value and type-only namespaces in exports; justified exporting related types alongside values for import convenience; noted the dual role of @typedef and suggested TypeScript 7 could introduce local-only type support via a breaking change
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#3873](https://github.com/microsoft/TypeScript-go/issues/3873) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal crash in \`\(\*Program\)\.SingleThreaded\` on snapshot update**

*The compiler’s Program.SingleThreaded method crashes fatally when updating project snapshots in the language server.*

 * (4 days ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3878](https://github.com/microsoft/TypeScript-go/issues/3878) (Open, `bug`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Crash via \`checkExternalEmitHelpers\`**

*TypeScript crashes in checkExternalEmitHelpers while resolving external helper modules during decorator processing.*

 * (4 days ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** assigned to **Copilot**, and unassigned **Copilot**

### [Issue microsoft/TypeScript-go#3895](https://github.com/microsoft/TypeScript-go/issues/3895) (Closed, `duplicate`, **jakebailey**, **Copilot**)

**tsgo's Uppercase/Lowercase intrinsic types don't apply Unicode special case mappings**

*tsgo's Uppercase and Lowercase intrinsic types omit Unicode special case mappings, causing incorrect type errors for characters like ß.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3895#issuecomment-4467314515) **jakebailey** said "This is effectively https://github.com/microsoft/typescript-go/issues/3489"
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added label `duplicate`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3899](https://github.com/microsoft/TypeScript-go/issues/3899) (Open, **jakebailey**, **Copilot**)

**tsgo breaks type soundness for lone\-surrogate string literals**

*tsgo improperly accepts assignments between different lone-surrogate string literals, breaking TypeScript’s type soundness.*

 * created by **mariusschulz**
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3900](https://github.com/microsoft/TypeScript-go/issues/3900) (Open, `Crash`, **jakebailey**, **Copilot**)

**tsgo source\-map emit panics for an unclosed block**

*Emitting source maps in tsgo causes a slice bounds panic when encountering an unclosed code block.*

 * **mariusschulz** added label `Crash`
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3907](https://github.com/microsoft/TypeScript-go/issues/3907) (Closed, **jakebailey**, **Copilot**)

**tsgo declaration emit drops readonly from method shorthands and outer properties in \`as const\` object literal**

*tsgo’s declaration emitter drops readonly modifiers on methods and outer properties in as const object literals.*

 * created by **mariusschulz**
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3908](https://github.com/microsoft/TypeScript-go/issues/3908) (Open, **jakebailey**, **Copilot**)

**tsgo incorrectly renames arguments destructuring property when targeting ES2015**

*When targeting ES2015, tsgo wrongly renames destructured property 'arguments' to 'arguments_1' in async functions.*

 * created by **mariusschulz**
 * (3 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#3933](https://github.com/microsoft/TypeScript-go/pull/3933) (Closed, **jakebailey**, **Copilot**)

**Fix declaration emit dropping readonly from \`as const\` object literal properties**

*Ensure TypeScript declaration emit correctly preserves readonly modifiers on object literal properties specified with as const.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3933#issuecomment-4490526336) **jakebailey** said "@copilot+gpt-5.5 merge main and resolve conflicts and update baselines"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3933#issuecomment-4490713284) **Copilot** merged origin/main, resolved baseline conflict, refreshed baselines, and reran validation
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3938](https://github.com/microsoft/TypeScript-go/issues/3938) (Open, `Needs Investigation`, **andrewbranch**)

**Result of getTypeOfLocation for \`PropertyAccessExpression\` and \`ElementAccessExpression\` may be different between 6 and 7**

*Parenthesized and nested property accesses yield incorrect object types in tsgo v7’s getTypeAtLocation compared to TypeScript 6.*

 * created by **jet2jet**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#3940](https://github.com/microsoft/TypeScript-go/issues/3940) (Open, `Domain: Editor`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal server crash at \`loadModuleFromSpecificNodeModulesDirectory\`**

*A fatal server crash occurs in loadModuleFromSpecificNodeModulesDirectory due to a missing nil check on Contents.*

 * (2 days ago) **DanielRosenwasser** added labels `Crash`, `Domain: Editor`, and assigned to **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#3942](https://github.com/microsoft/TypeScript-go/issues/3942) (Open, `Domain: Editor`, `Crash`, **RyanCavanaugh**, **Copilot**)

**Fatal server crash at \`markProjectsAffectedByConfigChanges\`**

*Server crashes in markProjectsAffectedByConfigChanges when updating project snapshots after configuration changes.*

 * created by **DanielRosenwasser**
 * (2 days ago) **DanielRosenwasser** added labels `Domain: Editor`, `Crash`
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3945](https://github.com/microsoft/TypeScript-go/issues/3945) (Closed, `Domain: Editor`, **jakebailey**, **Copilot**)

**importModuleSpecifier: "project\-relative" is ignored by TS Native extension \(forces tsconfig paths instead of relative imports\)**

*The built-in VSCode TypeScript extension ignores 'project-relative' importModuleSpecifier and applies tsconfig path aliases instead of relative imports.*

 * **jerePixelgenau** added label `Domain: Editor`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3946](https://github.com/microsoft/TypeScript-go/issues/3946) (Closed, `possible improvement`, **jakebailey**, **Copilot**)

**Auto\-import lowercases internal capitals in PascalCase default\-import bindings**

*tsgo’s auto-import incorrectly lowercases internal capitals of PascalCase default-import bindings, unlike TypeScript’s tsc behavior.*

 * created by **SamuelBrucksch**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3950](https://github.com/microsoft/TypeScript-go/issues/3950) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Hovering on type \`const\` does not display the specific type**

*Hovering over an as const literal in VS Code with the tsgo extension fails to show the literal type 42.*

 * **Withered-Flower-0422** added label `Domain: Editor`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#3952](https://github.com/microsoft/TypeScript-go/pull/3952) (Closed, **jakebailey**, **Copilot**)

**Fix auto\-import lowercasing PascalCase default\-import bindings on case\-insensitive file systems**

*Use moduleFileName for fallback paths to preserve PascalCase default-import identifiers on case-insensitive file systems*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3953](https://github.com/microsoft/TypeScript-go/pull/3953) (Closed, **jakebailey**, **Copilot**)

**Fix \`importModuleSpecifier: "project\-relative"\` ignored when tsconfig \`paths\` are configured**

*Project-relative auto-imports were emitting tsconfig alias paths instead of relative paths due to projectDirectory miscalculation and conditional logic gating regressions.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3955](https://github.com/microsoft/TypeScript-go/issues/3955) (Closed, `possible improvement`, **jakebailey**, **Copilot**)

**JSDoc comment of elided import is preserved**

*tsgo unexpectedly preserves and reassigns JSDoc comments from an elided import to the subsequent export declaration.*

 * created by **dragomirtitian**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `Possible Improvement`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3956](https://github.com/microsoft/TypeScript-go/issues/3956) (Closed, **jakebailey**, **Copilot**)

**Empty JSDoc comment is removed**

*tsgo removes empty JSDoc comments on exports that TypeScript 6.0 normally preserves*

 * created by **dragomirtitian**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3962](https://github.com/microsoft/TypeScript-go/pull/3962) (Closed, **jakebailey**, **Copilot**)

**Fix empty JSDoc comment \(\`/\*\*\*/\`\) being removed during declaration emit**

*Update the printer's JSDoc length check from >5 to >=5 to preserve empty /***/ comments in declaration files.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3963](https://github.com/microsoft/TypeScript-go/pull/3963) (Closed, **jakebailey**, **Copilot**)

**Fix JSDoc comment of elided import being preserved in declaration emit**

*Fixed JSDoc comments being incorrectly preserved for elided imports in declaration emit*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3968](https://github.com/microsoft/TypeScript-go/issues/3968) (Closed, `possible improvement`, **jakebailey**, **Copilot**)

**Type parameters in object literal methods get extra unnecessary suffix in declaration files**

*tsgo adds unnecessary numeric suffixes (e.g., M_1) to identical type parameters in object literal methods of declaration files.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3968#issuecomment-4479289078) **jakebailey** said "Probably related to #3761 and co"
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** added label `possible improvement`, and set milestone to `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3969](https://github.com/microsoft/TypeScript-go/pull/3969) (Closed, **jakebailey**, **Copilot**)

**Fix spurious \`\_N\` suffix on type parameters of sibling object\-literal methods in declaration emit**

*Declaration emit incorrectly adds a _N suffix to generic type parameters of sibling object-literal methods due to deferred scope cleanup*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3973](https://github.com/microsoft/TypeScript-go/issues/3973) (Closed, `Type Ordering`, **ahejlsberg**)

**Variance check skipped on union of intersections when one branch's recursive cycle goes through a covariant \`TValue\`**

*TypeScript skips variance checking on a union of intersections with a covariant recursive branch, missing type errors.*

 * (yesterday) **RyanCavanaugh** added label `Type Ordering`, and assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3973#issuecomment-4484334937) **RyanCavanaugh** described an analogous variance-cycle issue in tsgo and explained how renaming affected error reporting
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3973#issuecomment-4490347834) **ahejlsberg** noted that variance computation for cyclic types is sensitive to where the computation starts and that using -stableTypeOrdering in TS6 removes the error, concluding there’s little that can be done
 * [today](https://github.com/microsoft/TypeScript-go/issues/3973#issuecomment-4490598889) **IanVS** thanked the reviewer and suggested that @tannerlinsley be made aware of a slight difference in tsc vs tsgo reporting in an edge-case tanstack-table usage
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3974](https://github.com/microsoft/TypeScript-go/pull/3974) (Closed)

**fix\(checker\): check type expressions on unmatched JSDoc @param tags**

*Enable checking of type expressions on unmatched JSDoc @param tags in JavaScript files to ensure generic type errors are reported.*

 * created by **Zelys-DFKH**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3974#issuecomment-4492454032) **RyanCavanaugh** said "Closing automated PRs; please don't run automated coding tools against this repo. We're fully able to do that ourselves."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3976](https://github.com/microsoft/TypeScript-go/issues/3976) (Closed, `bug`, **ahejlsberg**)

**tsgo does not correctly infer array type assignment on callable type with fields since 20260503\.1**

*Since 20260503.1 tsgo incorrectly rejects assigning [] to a callable type’s array field due to broken inference.*

 * created by **chriskrycho**
 * **jakebailey** assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3976#issuecomment-4482730647) **Zelys-DFKH** pointed out the root cause was a circular type resolution path that settled [] as never[] before the annotation check and announced a tested fix with a forthcoming PR
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.0 RC`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3979](https://github.com/microsoft/TypeScript-go/pull/3979) (Closed)

**fix\(checker\): suppress false TS7008 for empty array assigned to annotated expando property**

*Suppress the TS7008 "implicitly has any[]" error for empty array assignments to explicitly annotated expando properties on callable types.*

 * created by **Zelys-DFKH**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3979#issuecomment-4489361131) **ahejlsberg** said "@Zelys-DFKH Appreciate the effort, but I have a simpler fix in #3986."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3979#issuecomment-4491477158) **Zelys-DFKH** thanked the reviewer and noted that they had re-derived through the AST what symbol.Parent already captures, learning the importance of starting from the right layer

### [PR microsoft/TypeScript-go#3982](https://github.com/microsoft/TypeScript-go/pull/3982) (Closed)

**Fix repeated path component in exports completions after directory separator**

*Export path completions incorrectly repeat the last directory for trailing slashes, so the fix strips the typed fragment.*

 * created by **Zelys-DFKH**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3982#issuecomment-4492454630) **RyanCavanaugh** said "Closing automated PRs; please don't run automated coding tools against this repo. We're fully able to do that ourselves."
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3982#issuecomment-4493097692) **Zelys-DFKH** acknowledged Ryan's point, addressed Daniel's feedback by adding a regression test and removing extra trailing separators, and pushed the update
 * [today](https://github.com/microsoft/TypeScript-go/pull/3982#issuecomment-4493150832) **Zelys-DFKH** mentioned that four PRs in a day looked automated, noted none received review, and stated they would maintain their work in a fork

### [Issue microsoft/TypeScript-go#3984](https://github.com/microsoft/TypeScript-go/issues/3984) (Open, `documentation`)

**Bloomberg feedback for 7\.0 beta**

*Bloomberg feedback highlights tsgo vs tsc declaration emit and type-checking discrepancies in the 7.0 beta, most fixed or minor.*

 * created by **dragomirtitian**
 * (today) **RyanCavanaugh** added label `documentation`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3984#issuecomment-4489787909) **RyanCavanaugh** said "Great report! Thanks for all the hard work investigating this. Glad to hear things are going well."

### [Issue microsoft/TypeScript-go#3985](https://github.com/microsoft/TypeScript-go/issues/3985) (Closed, `wontfix`)

**\`@typedef\` in jsdoc must have an identifier in tsgo; not in ts6\.0**

*tsgo reports an 'Identifier expected' error for JSDoc @typedef without an identifier unlike TypeScript 6.0.*

 * created by **Withered-Flower-0422**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3985#issuecomment-4491226876) **ahejlsberg** explained that Strada supports Closure-style name inference for nameless @typedefs attached to identifiers or variable declarations, but Corsa doesn’t and documented this behavior in CHANGES.md
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3986](https://github.com/microsoft/TypeScript-go/pull/3986) (Closed)

**No widening to \`any\[\]\` when parent of expando has type annotation**

*Empty array literals assigned to expando properties on type-annotated objects no longer widen to any[], matching Strada behavior.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3987](https://github.com/microsoft/TypeScript-go/pull/3987) (Open, **RyanCavanaugh**, **Copilot**)

**Avoid fatal panic on stale config\-retainer project paths in project rebuild flow**

*Prevent panic in markProjectsAffectedByConfigChanges by skipping stale project paths and add a regression test to verify safe handling.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3988](https://github.com/microsoft/TypeScript-go/issues/3988) (Closed, `Domain: Type Checking`, `Type Ordering`)

**New "Argument of type 'null' is not assignable to parameter of type 'void'\." errors**

*tsgo rejects null for a void parameter that TypeScript 6.0 accepts.*

 * created by **blickly**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3988#issuecomment-4490512995) **jakebailey** said "Flip on --stableTypeOrdering and you'll get this error in 6.0"
 * (today) **ahejlsberg** added labels `Domain: Type Checking`, `Type Ordering`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3988#issuecomment-4491654490) **blickly** said "Nice, I didn't realize that affected diagnostics as well rather than just the emit.  Should I close this as WAI then?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3988#issuecomment-4492137995) **ahejlsberg** explained that the behavior was working as intended by demonstrating the error when flipping union type constituents and provided a playground link
 * [today](https://github.com/microsoft/TypeScript-go/issues/3988#issuecomment-4493242768) **blickly** said "Makes sense. Thanks for the quick response!"
 * (today) **blickly** closed the issue

### [PR microsoft/TypeScript-go#3989](https://github.com/microsoft/TypeScript-go/pull/3989) (Open)

**lsp: emit VS\-internal HiddenInEditor tag for unnecessary diagnostics**

*Emit Visual Studio’s HiddenInEditor tag for Unnecessary diagnostics when vs_supportsVisualStudioExtensions is enabled so unused code fades in the editor*

 * created by **joj**

### [PR microsoft/TypeScript-go#3990](https://github.com/microsoft/TypeScript-go/pull/3990) (Open, **joj**, **Copilot**)

**lsproto: separate VS diagnostic tag constant from CodeActionKind block**

*Relocate VSDiagnosticTagHiddenInEditor from the CodeActionKind constant block into a dedicated DiagnosticTag block to improve protocol organization.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **joj**

### [PR microsoft/TypeScript-go#3991](https://github.com/microsoft/TypeScript-go/pull/3991) (Closed)

**fix\(3985\): allow empty typedef name**

*Update the typedef parser to accept declarations with empty names, resolving issue 3985.*

 * created by **a-tarasyuk**
 * (today) **a-tarasyuk** closed the issue

### [PR microsoft/TypeScript-go#3992](https://github.com/microsoft/TypeScript-go/pull/3992) (Closed)

**fix\(project\): release stale retainingProjects entries when program drops a reference**

*Add logic to remove obsolete project reference entries after program rebuilds to prevent stale entries causing errors.*

 * created by **Zelys-DFKH**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3992#issuecomment-4492453505) **RyanCavanaugh** said "Closing automated PRs; please don't run automated coding tools against this repo. We're fully able to do that ourselves."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3993](https://github.com/microsoft/TypeScript-go/pull/3993) (Closed)

**Move \`definiteAssignmentAssertionsWithObjectShortHand\.js\.diff\` file to accepted**

*Relocate the definiteAssignmentAssertionsWithObjectShortHand.js.diff file to the accepted directory to fix issue #3563.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3994](https://github.com/microsoft/TypeScript-go/pull/3994) (Open, **DanielRosenwasser**, **Copilot**)

**Fix external helper crash after module\-status updates**

*Treating module-indicator changes as non-reusable to force rebuilds and prevent missing tslib-import crashes after updates.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4492292470) **DanielRosenwasser** said "Perfect - can you write this as a fourslash test instead? Make sure the fourslash test actually fails without the fix."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4492293827) **DanielRosenwasser** said "@copilot"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3994#issuecomment-4492417437) **Copilot** addressed the request by adding a fourslash test and verifying it failed without the production fix

### [PR microsoft/TypeScript-go#3995](https://github.com/microsoft/TypeScript-go/pull/3995) (Closed)

**fix\(declarations\): strip synthesized namespace for @internal expando functions**

*With stripInternal enabled, remove synthesized namespaces for @internal expando functions in declaration output.*

 * created by **Zelys-DFKH**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3995#issuecomment-4492452751) **RyanCavanaugh** said "Closing automated PRs; please don't run automated coding tools against this repo. We're fully able to do that ourselves."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3996](https://github.com/microsoft/TypeScript-go/pull/3996) (Open)

**Extract tscInput tests to individual per\-scenario files with imperative edits to improve debuggability**

*Extract tscInput tests into individual scenario files with imperative edits, remove intra-test parallelism, simplify debugging while preserving original tests.*

 * created by **weswigham**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-4496173212) **jakebailey** said "Not sure I like this, but at the very least I think the filenames shouldn't start with capital T"

### [PR microsoft/TypeScript-go#3997](https://github.com/microsoft/TypeScript-go/pull/3997) (Closed)

**Warn against AI botting**

*Port AI botting warning guidance from Strada’s contributing.md into the current project.*

 * created by **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3998](https://github.com/microsoft/TypeScript-go/issues/3998) (Open, `bug`, **andrewbranch**)

**Intermittent \`tsgo \-\-build\` TS2345: \`paths\` \+ \`@types/\*\` conflict \(\`tsc\` accepts\)**

*tsgo --build randomly fails with TS2345 errors caused by conflicting path aliases and @types/react types while tsc builds and single-threaded tsgo builds consistently succeed.*

 * created by **adamnreed**

### [PR microsoft/TypeScript-go#3999](https://github.com/microsoft/TypeScript-go/pull/3999) (Closed)

**Handle empty response file name in command line parser**

*The command line parser now checks for empty response file names and reports a diagnostic instead of panicking.*

 * created by **LeSingh1**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3999#issuecomment-4495601959) **jakebailey** said "The right fix is in https://github.com/microsoft/typescript-go/pull/3859; the issue is wider than empty strings "
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4000](https://github.com/microsoft/TypeScript-go/issues/4000) (Open, `enhancement`)

**Make typedef exporting explicit**

*Propose introducing a new @export JSDoc tag to explicitly mark exported typedefs and type re-exports in TypeScript 7*

 * created by **remcohaszing**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4000#issuecomment-4497729784) **ahejlsberg** rejected the suggestion to add new JSDoc features and recommended writing the code in TypeScript
 * **ahejlsberg** added label `enhancement`

### [Issue microsoft/TypeScript-go#4001](https://github.com/microsoft/TypeScript-go/issues/4001) (Closed, `wontfix`)

**Behavior difference: TS2447 points to the operator in tsgo, but points to the \(first\) operand in tsc**

*tsgo reports TS2447 errors by pointing to the boolean operator, whereas tsc highlights the first operand instead.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4001#issuecomment-4497688068) **ahejlsberg** said "This is an intended difference. In a large expression this makes it a lot easier to identify the problematic operator."
 * **ahejlsberg** added label `wontfix`
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4002](https://github.com/microsoft/TypeScript-go/issues/4002) (Closed, `Domain: Editor`, `Needs More Info`)

**Image JSX type**

*The VS Code extension incorrectly treats the global Image constructor as a valid JSX element type.*

 * created by **Netail**
 * **Netail** added label `Domain: Editor`

