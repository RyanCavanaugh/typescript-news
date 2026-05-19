# Report for 2026-05-17 (Sunday, May 17th, 2026)

12 different users commented on 61 different issues.

## Recommended Actions

 * Response Recommended
    * @dragomirtitian asked about why deeper inferred type properties weren't reused in [microsoft/TypeScript-go#3957](https://github.com/microsoft/TypeScript-go/issues/3957#issuecomment-4479170895)
    * @dragomirtitian asked if the parenthesization workaround could be avoided in [microsoft/TypeScript-go#3961](https://github.com/microsoft/TypeScript-go/issues/3961#issuecomment-4479155423)

## Activity Summary

### [PR microsoft/TypeScript-go#3212](https://github.com/microsoft/TypeScript-go/pull/3212) (Open)

**Fix error spans for \`@satisfies\`**

*Fix error span calculation for @satisfies to ensure accurate error highlighting.*

 * created by **Andarist**
 * (1 month ago) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `TypeScript 7.0 RC`
 * [later](https://github.com/microsoft/TypeScript-go/pull/3212#issuecomment-4478733292) **jakebailey** said "This is failing all the tests"

### [PR microsoft/TypeScript-go#3495](https://github.com/microsoft/TypeScript-go/pull/3495) (Open)

**Use JS\-compatible Unicode casing for intrinsic string mappings**

*Implement JavaScript-compatible Unicode casing rules in TypeScript’s intrinsic string mapping functions.*

 * created by **Andarist**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [later](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4476496557) **Andarist** explained that using Go's unicode ranges wasn't possible, added a code comment, and implemented a commitable code generator to keep the output file up to date
 * [later](https://github.com/microsoft/TypeScript-go/pull/3495#issuecomment-4478753309) **jakebailey** said "See also https://github.com/microsoft/typescript-go/pull/3930 which uses x/text for this, though I'm wary of that too..."

### [PR microsoft/TypeScript-go#3877](https://github.com/microsoft/TypeScript-go/pull/3877) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic in getTsConfigObjectLiteralExpression for malformed tsconfig**

*getTsConfigObjectLiteralExpression now checks for object literals to avoid panicking on malformed tsconfig.json values, and a test case was added.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4464433812) **RyanCavanaugh** questioned the theory of the case, asserted that the testcase did not reproduce the problem, noted that tsgo already reported the correct TS5092 error, and mentioned that the call stack indicated a related diagnostic was being computed
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4465771376) **DanielRosenwasser** said "@copilot fix it"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4465830661) **Copilot** acknowledged that the original test didn’t exercise the diagnostic explanation code and updated the test to use an array-literal tsconfig to trigger the crash path
 * [later](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4479412000) **RyanCavanaugh** updated the test to use a specific compilerOptions types array and confirmed that this triggers the tsgo cmdline crash

### [Issue microsoft/TypeScript-go#3887](https://github.com/microsoft/TypeScript-go/issues/3887) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo printer panics during "JSX expressions must have one parent element" recovery**

*The tsgo printer panics during JSX recovery when encountering an unhandled binary expression in a JSX attribute.*

 * **mariusschulz** added label `Crash`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3888](https://github.com/microsoft/TypeScript-go/issues/3888) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics with interface conversion error when a @this appears inside of a @typedef comment**

*Parsing a JSDoc typedef comment that contains a @this tag triggers an interface conversion panic in tsgo.*

 * **mariusschulz** added label `Crash`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3889](https://github.com/microsoft/TypeScript-go/issues/3889) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a @callback / @overload @param has a qualified name**

*tsgo panics with an unhandled QualifiedName case when a @callback or @overload @param uses a qualified name*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3889#issuecomment-4467242662) **jakebailey** said "How are you finding all of these? Is this some specific codebase? Are you fuzzing?"
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3890](https://github.com/microsoft/TypeScript-go/issues/3890) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a @this JSDoc tag is combined with a literal this parameter**

*tsgo panics with an index out of range error when encountering a JSDoc @this tag alongside a literal this parameter*

 * **mariusschulz** added label `Crash`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3892](https://github.com/microsoft/TypeScript-go/issues/3892) (Closed, **jakebailey**, **Copilot**)

**tsgo hangs on large template literal types with combinatorial explosion**

*tsgo hangs indefinitely when compiling large combinatorial template literal types that tsc rejects as too complex.*

 * created by **mariusschulz**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3897](https://github.com/microsoft/TypeScript-go/pull/3897) (Closed, **jakebailey**, **Copilot**)

**Fix JSX entity decoder skipping entities after non\-entity ampersand**

*Update JSX entity decoder to skip intervening non-entity ampersands and correctly decode entities.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3897#issuecomment-4474627711) **jakebailey** said "@copilot+claude-opus-4.6 address comments"

### [Issue microsoft/TypeScript-go#3902](https://github.com/microsoft/TypeScript-go/issues/3902) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics for a contextually typed function with optional and rest params**

*tsgo panics with a makeslice: len out of range error when type-checking a function using optional and rest parameters*

 * **mariusschulz** added label `Crash`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3903](https://github.com/microsoft/TypeScript-go/issues/3903) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics for rest properties in catch binding when targeting ES2017**

*tsgo crashes when transforming object rest properties in catch bindings targeting ES2017 because of an AST conversion error.*

 * **mariusschulz** added label `Crash`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3904](https://github.com/microsoft/TypeScript-go/issues/3904) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a type\-only export is the body of an if statement**

*tsgo crashes with a nil pointer dereference when an if statement’s body is a type-only export.*

 * **mariusschulz** added label `Crash`
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3909](https://github.com/microsoft/TypeScript-go/issues/3909) (Closed, **jakebailey**, **Copilot**)

**tsgo loses all type narrowing in a \`switch \(typeof x\)\` when any clause is \`case ""\`**

*tsgo’s type checker loses type narrowing in a switch(typeof x) when a case uses an empty string, causing incorrect errors.*

 * created by **mariusschulz**
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3920](https://github.com/microsoft/TypeScript-go/pull/3920) (Closed, **jakebailey**, **Copilot**)

**Fix printer panic on unexpected JSX attribute value during error recovery**

*Modify emitJsxAttributeValue to emit arbitrary expression nodes instead of panicking on malformed JSX attributes and add a reproducing test.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3921](https://github.com/microsoft/TypeScript-go/pull/3921) (Closed, **jakebailey**, **Copilot**)

**Fix panic when @this tag appears inside @typedef JSDoc comment**

*Skip non-property JSDoc tags such as @this in typedef comments to avoid parser panics.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3922](https://github.com/microsoft/TypeScript-go/pull/3922) (Closed, **jakebailey**, **Copilot**)

**Fix panic when @callback/@overload @param has a qualified name**

*The reparser treated JSDoc parameters with qualified names as ParameterDeclarations in callback/overload signatures, causing a panic.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3924](https://github.com/microsoft/TypeScript-go/pull/3924) (Closed, **jakebailey**, **Copilot**)

**Fix panic in getRestTypeAtPosition for contextually typed function with optional and rest params**

*getRestTypeAtPosition panics with negative slice length for contextually typed functions with optional and rest parameters.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3925](https://github.com/microsoft/TypeScript-go/pull/3925) (Closed, **jakebailey**, **Copilot**)

**Fix panic when @this JSDoc tag is combined with a literal this parameter**

*tsgo reparser panics on JSDoc @this combined with a literal this parameter because it fails to recognize the this identifier*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3927](https://github.com/microsoft/TypeScript-go/pull/3927) (Closed, **jakebailey**, **Copilot**)

**Fix panic for rest properties in catch binding when targeting ES2017**

*Replaced bitwise check with equality for KindSyntaxList in catch clause rest properties to fix transformer panic.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3928](https://github.com/microsoft/TypeScript-go/pull/3928) (Closed, **jakebailey**, **Copilot**)

**Fix panic in printer when type\-only export is body of an if statement**

*Printer panics when a type-only export is used as an if statement body, now fixed by emitting an empty statement.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3929](https://github.com/microsoft/TypeScript-go/pull/3929) (Closed, **jakebailey**, **Copilot**)

**Fix integer overflow in getCrossProductUnionSize causing hang on large template literal types**

*Add overflow checks to getCrossProductUnionSize to avoid signed integer wraparound and hanging on large template literal unions*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3934](https://github.com/microsoft/TypeScript-go/pull/3934) (Closed, **jakebailey**, **Copilot**)

**Fix typeof switch narrowing broken by \`case ""\` clauses**

*Empty string case clauses in typeof switch statements are misinterpreted as non-literals, aborting type narrowing entirely.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3936](https://github.com/microsoft/TypeScript-go/issues/3936) (Closed, **jakebailey**, **Copilot**)

**tsgo wrongly parses literal object after \`await\`**

*tsgo incorrectly parses object literals after await, resulting in erroneous syntax errors compared to TypeScript 6.0.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3936#issuecomment-4469628013) **Withered-Flower-0422** reported tsgo threw an error when awaiting an empty array that did not occur in TypeScript 6.0
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3937](https://github.com/microsoft/TypeScript-go/pull/3937) (Closed, **jakebailey**, **Copilot**)

**Fix reparseTopLevelAwait diagnostic slicing bug**

*Adjusts the diagnostic range search in reparseTopLevelAwait to prevent initial-parse errors leaking into await reparsing.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3939](https://github.com/microsoft/TypeScript-go/pull/3939) (Closed)

**fix\(printer\): clamp out\-of\-range pos in getLineAndCharacter for source map emit**

*Add a guard in getLineAndCharacter to clamp out-of-range positions and prevent source map panics.*

 * created by **Zelys-DFKH**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3939#issuecomment-4472696043) **jakebailey** said "We already have #3923."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3939#issuecomment-4472704698) **Zelys-DFKH** said "Closing — #3923 already fixes this. Thanks for the quick catch, @jakebailey."
 * (today) **Zelys-DFKH** closed the issue

### [Issue microsoft/TypeScript-go#3940](https://github.com/microsoft/TypeScript-go/issues/3940) (Open, `Domain: Editor`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal server crash at \`loadModuleFromSpecificNodeModulesDirectory\`**

*A fatal server crash occurs in loadModuleFromSpecificNodeModulesDirectory due to a missing nil check on Contents.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Crash`, `Domain: Editor`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3941](https://github.com/microsoft/TypeScript-go/pull/3941) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil dereference crash in loadModuleFromSpecificNodeModulesDirectory**

*Prevent nil dereference in loadModuleFromSpecificNodeModulesDirectory by adding a packageInfo.Exists() guard and a subpath node_modules resolution test case.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4474794206) **DanielRosenwasser** said "The test seems insufficient if this is about race conditions. @copilot is there a better test here? Possibly a server test or a programmatic test of our APIs?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3941#issuecomment-4474873463) **Copilot** replaced the compiler test with a programmatic race condition test and detailed deterministic reproduction steps

### [Issue microsoft/TypeScript-go#3942](https://github.com/microsoft/TypeScript-go/issues/3942) (Open, `Domain: Editor`, `Crash`)

**Fatal server crash at \`markProjectsAffectedByConfigChanges\`**

*Server crashes in markProjectsAffectedByConfigChanges when updating project snapshots after configuration changes.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Domain: Editor`, `Crash`

### [PR microsoft/TypeScript-go#3943](https://github.com/microsoft/TypeScript-go/pull/3943) (Open)

**Fix crash inferring constrained variadic tuples with optional elements**

*Fix compiler crash during inference of constrained variadic tuples with optional elements*

 * created by **Andarist**

### [Issue microsoft/TypeScript-go#3944](https://github.com/microsoft/TypeScript-go/issues/3944) (Closed)

**Request failure for import with non\-textual specifier node**

*Auto-import quick fixes fail to generate edits when using non-textual module specifiers like template literals.*

 * created by **DanielRosenwasser**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3945](https://github.com/microsoft/TypeScript-go/issues/3945) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**importModuleSpecifier: "project\-relative" is ignored by TS Native extension \(forces tsconfig paths instead of relative imports\)**

*The built-in VSCode TypeScript extension ignores 'project-relative' importModuleSpecifier and applies tsconfig path aliases instead of relative imports.*

 * created by **jerePixelgenau**
 * **jerePixelgenau** added label `Domain: Editor`
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3946](https://github.com/microsoft/TypeScript-go/issues/3946) (Open, **jakebailey**, **Copilot**)

**Auto\-import lowercases internal capitals in PascalCase default\-import bindings**

*tsgo’s auto-import incorrectly lowercases internal capitals of PascalCase default-import bindings, unlike TypeScript’s tsc behavior.*

 * created by **SamuelBrucksch**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3947](https://github.com/microsoft/TypeScript-go/pull/3947) (Closed)

**Fix \`getSwitchClauseTypeOfWitnesses\`**

*Provide a simpler fix for getSwitchClauseTypeOfWitnesses to resolve issue #3909.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3948](https://github.com/microsoft/TypeScript-go/pull/3948) (Closed)

**Fix crash on non\-textual module specifiers in auto\-import promote fixes**

*Prevent crash in auto-import promote fixes when handling non-textual module specifiers*

 * created by **Andarist**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3949](https://github.com/microsoft/TypeScript-go/pull/3949) (Open)

**feat: completion snippets**

*Implement code completion snippets to enable quick insertion of commonly used code patterns*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#3950](https://github.com/microsoft/TypeScript-go/issues/3950) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Hovering on type \`const\` does not display the specific type**

*Hovering over an as const literal in VS Code with the tsgo extension fails to show the literal type 42.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3951](https://github.com/microsoft/TypeScript-go/pull/3951) (Open, **jakebailey**, **Copilot**)

**Fix hover on \`const\` in \`as const\` to display the specific type**

*Hovering on const in '42 as const' shows 'const = 42' instead of the generic 'type const'.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3952](https://github.com/microsoft/TypeScript-go/pull/3952) (Open, **jakebailey**, **Copilot**)

**Fix auto\-import lowercasing PascalCase default\-import bindings on case\-insensitive file systems**

*Use moduleFileName for fallback paths to preserve PascalCase default-import identifiers on case-insensitive file systems*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3953](https://github.com/microsoft/TypeScript-go/pull/3953) (Open, **jakebailey**, **Copilot**)

**Fix \`importModuleSpecifier: "project\-relative"\` ignored when tsconfig \`paths\` are configured**

*Project-relative auto-imports were emitting tsconfig alias paths instead of relative paths due to projectDirectory miscalculation and conditional logic gating regressions.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3954](https://github.com/microsoft/TypeScript-go/issues/3954) (Closed)

**JSDoc comment stripped from async private method**

*Private async methods lose JSDoc comments in declaration files generated by tsgo while non-async methods retain theirs.*

 * created by **dragomirtitian**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3955](https://github.com/microsoft/TypeScript-go/issues/3955) (Open, **jakebailey**, **Copilot**)

**JSDoc comment of elided import is preserved**

*tsgo unexpectedly preserves and reassigns JSDoc comments from an elided import to the subsequent export declaration.*

 * created by **dragomirtitian**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3956](https://github.com/microsoft/TypeScript-go/issues/3956) (Open, **jakebailey**, **Copilot**)

**Empty JSDoc comment is removed**

*tsgo removes empty JSDoc comments on exports that TypeScript 6.0 normally preserves*

 * created by **dragomirtitian**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3957](https://github.com/microsoft/TypeScript-go/issues/3957) (Open, `possible improvement`, **jakebailey**, **Copilot**)

**Property names are quoted one level deep in inferred type**

*tsgo preserves quotes on one-level-deep property names in inferred types, unlike TypeScript 6.0 which strips them.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3957#issuecomment-4479141437) **jakebailey** said "This is sort of intentional; we can now actually reuse those deeper nodes and so you're seeing the quoted strings as originally written."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3957#issuecomment-4479170895) **dragomirtitian** noted that reuse applied only to properties one level deep and expressed concern about deeper inferred type properties not being reused
 * [later](https://github.com/microsoft/TypeScript-go/issues/3957#issuecomment-4479189689) **jakebailey** said "Ah, I see what you mean."
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3958](https://github.com/microsoft/TypeScript-go/issues/3958) (Closed)

**Accessors are preserved in inferred object literal type in declarations**

*TypeScript declarations collapse getter and setter accessors into a single property while tsgo preserves them separately.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3958#issuecomment-4479096085) **jakebailey** said "This is actually an intentional choice, though one we didn't exactly document. Is this causing a problem for you?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/3958#issuecomment-4479124518) **dragomirtitian** clarified that they didn’t experience issues, reported the behavior for awareness, and closed the issue as it was intentional
 * (later) **dragomirtitian** closed the issue

### [Issue microsoft/TypeScript-go#3959](https://github.com/microsoft/TypeScript-go/issues/3959) (Closed)

**const assertion does not make methods readonly in declaration files**

*tsgo-generated declaration files treat methods in const-asserted objects as non-readonly, unlike TypeScript 6.0 which marks them readonly.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3959#issuecomment-4479088971) **jakebailey** said "Duplicate of #3907"
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3960](https://github.com/microsoft/TypeScript-go/pull/3960) (Closed)

**fix\(3954\): preserve jsdoc on private async method declarations**

*Preserve JSDoc comments on private async method declarations during transpilation.*

 * created by **a-tarasyuk**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3961](https://github.com/microsoft/TypeScript-go/issues/3961) (Closed, **jakebailey**, **Copilot**)

**Parentheses always added around \`typeof\` type expression**

*tsgo adds redundant parentheses around typeof type expressions in type aliases, altering the original code formatting.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3961#issuecomment-4479133899) **jakebailey** acknowledged a parenthesization difference, noted that adding parentheses resolved problems, and asked if it could be avoided
 * [later](https://github.com/microsoft/TypeScript-go/issues/3961#issuecomment-4479155423) **dragomirtitian** noted that adding parentheses to user code for declaration files seemed strange and asked if it could be avoided
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3962](https://github.com/microsoft/TypeScript-go/pull/3962) (Open, **jakebailey**, **Copilot**)

**Fix empty JSDoc comment \(\`/\*\*\*/\`\) being removed during declaration emit**

*Update the printer's JSDoc length check from >5 to >=5 to preserve empty /***/ comments in declaration files.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3963](https://github.com/microsoft/TypeScript-go/pull/3963) (Open, **jakebailey**, **Copilot**)

**Fix JSDoc comment of elided import being preserved in declaration emit**

*Fixed JSDoc comments being incorrectly preserved for elided imports in declaration emit*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3964](https://github.com/microsoft/TypeScript-go/pull/3964) (Closed, **jakebailey**, **Copilot**)

**Preserve parsed \`typeof X\` in postfix type contexts**

*Declaration emit now preserves parsed typeof expressions without parentheses in array, indexed access, and optional type contexts.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3965](https://github.com/microsoft/TypeScript-go/pull/3965) (Open, **jakebailey**, **Copilot**)

**Normalize reused string\-literal property names to identifiers in declaration emit**

*Declaration emit now normalizes reused string-literal property names into identifiers when the text is a valid identifier.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3966](https://github.com/microsoft/TypeScript-go/issues/3966) (Closed, **jakebailey**, **Copilot**)

**Emojis from inferred types are written as unicode escapes in declaration files**

*Declaration files emit emojis as Unicode escape sequences instead of preserving the original emoji characters.*

 * created by **dragomirtitian**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3967](https://github.com/microsoft/TypeScript-go/pull/3967) (Closed, **jakebailey**, **Copilot**)

**Preserve non\-ASCII characters in declaration emit for string literal types**

*Preserve non-ASCII characters in string literal types in emitted declaration files by applying the no-ASCII-escaping printer flag to reused nodes.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3968](https://github.com/microsoft/TypeScript-go/issues/3968) (Open, **jakebailey**, **Copilot**)

**Type parameters in object literal methods get extra unnecessary suffix in declaration files**

*tsgo adds unnecessary numeric suffixes (e.g., M_1) to identical type parameters in object literal methods of declaration files.*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3968#issuecomment-4479289078) **jakebailey** said "Probably related to #3761 and co"
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3969](https://github.com/microsoft/TypeScript-go/pull/3969) (Open, **jakebailey**, **Copilot**)

**Fix spurious \`\_N\` suffix on type parameters of sibling object\-literal methods in declaration emit**

*Declaration emit incorrectly adds a _N suffix to generic type parameters of sibling object-literal methods due to deferred scope cleanup*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3970](https://github.com/microsoft/TypeScript-go/issues/3970) (Closed)

**Expando function namespaces are not merged in declaration files**

*tsgo generates distinct namespace declarations for each function property instead of merging them into a single namespace in declaration files*

 * created by **dragomirtitian**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3970#issuecomment-4479325033) **jakebailey** explained that they opted not to bring forward the complex behavior and are emitting namespaces to merge without extra work
 * (later) **dragomirtitian** closed the issue

### [Issue microsoft/TypeScript-go#3971](https://github.com/microsoft/TypeScript-go/issues/3971) (Closed, **jakebailey**, **Copilot**)

**Assertion in JSX spread causes missing newline in JS output**

*A type assertion in a JSX spread property causes the emitted JavaScript to remove surrounding newlines when transpiled with tsgo.*

 * created by **dragomirtitian**

