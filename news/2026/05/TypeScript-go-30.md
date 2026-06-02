# Report for 2026-05-30 (Saturday, May 30th, 2026)

7 different users commented on 57 different issues.

## Recommended Actions

 * Response Recommended
    * @hkleungai pointed out that this issue is a duplicate of issue #3683 in [microsoft/TypeScript-go#4126](https://github.com/microsoft/TypeScript-go/issues/4126#issuecomment-4586850091)

## Activity Summary

### [Issue microsoft/TypeScript-go#4076](https://github.com/microsoft/TypeScript-go/issues/4076) (Closed, **DanielRosenwasser**, **Copilot**)

**Unexpected errors for modifiers on \`@template\` type parameters**

*Modifiers on JSDoc @template type parameters trigger erroneous TS1274 errors due to missing grammar checking logic.*

 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4076#issuecomment-4582958541) **ahejlsberg** said "#4100 has the correct fix for this issue. The Copilot attempt is just wrong."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4077](https://github.com/microsoft/TypeScript-go/pull/4077) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix grammar checks for modifiers on \`@template\` type parameters**

*Correct JSDoc @template in/out/const modifier grammar checks by resolving the proper host declaration to prevent TS1274 errors.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4086](https://github.com/microsoft/TypeScript-go/issues/4086) (Open, `Crash`, **jakebailey**, **Copilot**)

**Panic on \`"target": null\` \(or any enum\-typed option set to null\) in tsconfig\.json**

*tsconfig.json parsing panics with interface conversion error when an enum option (e.g., target) is null*

 * created by **mds-ant**
 * **mds-ant** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4089](https://github.com/microsoft/TypeScript-go/issues/4089) (Open, **jakebailey**, **Copilot**)

**\`super\.m\(\)\` in a downleveled async function's parameter default survives into the inner \`function\*\`**

*tsgo downlevels async functions incorrectly retain super.m() in default parameters, causing a syntax error in the inner generator.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4090](https://github.com/microsoft/TypeScript-go/issues/4090) (Open, **jakebailey**, **Copilot**)

**Imported/exported identifier used as a shorthand destructuring default initializer is not rewritten**

*Shorthand destructuring default initializers of imported identifiers aren't converted to the module alias, causing undefined reference errors.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4091](https://github.com/microsoft/TypeScript-go/issues/4091) (Open, **jakebailey**, **Copilot**)

**JSX hex entity with uppercase marker decoded by tsgo, left literal by tsc**

*tsgo incorrectly decodes uppercase hexadecimal character entities in JSX to their literal characters, unlike tsc which leaves them intact.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4092](https://github.com/microsoft/TypeScript-go/issues/4092) (Open, **jakebailey**, **Copilot**)

**Lone surrogate in enum member name / const enum value is corrupted to U\+FFFD in emitted JS**

*tsgo emits U+FFFD in place of lone surrogates in enum member names and const enum values in the generated JavaScript*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4093](https://github.com/microsoft/TypeScript-go/issues/4093) (Open, **jakebailey**, **Copilot**)

**design:type metadata for \`bigint\` omits the \`typeof BigInt === "function"\` runtime fallback below ES2020**

*tsgo emits design:type metadata for bigint without the runtime fallback check that TypeScript includes for ES2015 targets*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4095](https://github.com/microsoft/TypeScript-go/issues/4095) (Open, **jakebailey**, **Copilot**)

**Namespace import used only by a type\-only \`export import X = ns\.Y\` is not elided**

*tsgo retains a namespace import used only by a type-only export-import alias instead of eliding it like TypeScript 6.0 does.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4096](https://github.com/microsoft/TypeScript-go/issues/4096) (Open, **jakebailey**, **Copilot**)

**Downleveled async arrow in a static field initializer captures the wrong \`this\`**

*Downleveling a static async arrow function initializer incorrectly captures the outer this rather than the class constructor.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4097](https://github.com/microsoft/TypeScript-go/issues/4097) (Open, **jakebailey**, **Copilot**)

**Enum member named with a Unicode escape emits the raw escape text**

*Using a Unicode escape to name an enum member causes tsgo to emit the raw escape text rather than the actual character, resulting in undefined values.*

 * created by **mds-ant**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4099](https://github.com/microsoft/TypeScript-go/issues/4099) (Open)

**A single legacy \`assert {\.\.\.}\` import suppresses every semantic diagnostic in the program**

*A single legacy import assert in tsgo emits only the assertion deprecation error and suppresses subsequent type-check diagnostics.*

 * created by **mds-ant**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4099#issuecomment-4583382246) **jakebailey** said "Sort of intentional, because we made this a parse error and files with parse errors like this don't get semantic diags"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4099#issuecomment-4583419517) **mds-ant** wondered whether the behavior was intentional and noted it shouldn't be a major issue as users migrate from `assert` to `with`, observing other tools might face similar parse error issues

### [PR microsoft/TypeScript-go#4100](https://github.com/microsoft/TypeScript-go/pull/4100) (Closed)

**Fix grammar checking for \`in\` and \`out\` modifiers in \`@template\` tags**

*Fix grammar checking for in and out modifiers in @template tags.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4101](https://github.com/microsoft/TypeScript-go/issues/4101) (Open)

**Declaration emit spends significant CPU in getAliasForSymbolInContainer / getAlternativeContainingModules**

*Declaration emit spends excessive CPU time in getAlternativeContainingModules and getAliasForSymbolInContainer, causing slow builds.*

 * created by **Zzzen**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4583182120) **jakebailey** assured that the pprof files contain no sensitive information and can be shared as-is
 * [today](https://github.com/microsoft/TypeScript-go/issues/4101#issuecomment-4585528342) **Zzzen** attached a CPU profile file and offered to provide a matching memory profile

### [PR microsoft/TypeScript-go#4103](https://github.com/microsoft/TypeScript-go/pull/4103) (Open, **jakebailey**, **Copilot**)

**Fix async arrow \`this\` capture in static field emit**

*Downleveled async arrow functions in relocated static initializers now avoid capturing ambient this and correctly reference the class constructor.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4104](https://github.com/microsoft/TypeScript-go/pull/4104) (Open, **jakebailey**, **Copilot**)

**Fix downlevel async \`super\` in default parameters**

*Fix async downlevel emit to substitute super calls in default parameter initializers for async methods and arrow functions*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4105](https://github.com/microsoft/TypeScript-go/pull/4105) (Open, **jakebailey**, **Copilot**)

**Handle null enum values in tsconfig parsing**

*Account for null enum values in tsconfig.json parsing by treating them as unset to prevent panics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4106](https://github.com/microsoft/TypeScript-go/pull/4106) (Open, **jakebailey**, **Copilot**)

**Add BigInt fallback for decorator metadata below ES2020**

*Add runtime-safe BigInt fallback in decorator metadata emission when targeting ECMAScript versions below ES2020.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4107](https://github.com/microsoft/TypeScript-go/pull/4107) (Open, **jakebailey**, **Copilot**)

**Fix enum member emit for escaped identifiers**

*Emit enum members with Unicode-escaped names using parsed identifier text instead of raw escapes to ensure correct runtime access.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4108](https://github.com/microsoft/TypeScript-go/pull/4108) (Open, **jakebailey**, **Copilot**)

**Match tsc for JSX uppercase hex entities**

*Ensure JSX numeric hex entities with uppercase X remain literal by decoding only lowercase x like tsc.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4109](https://github.com/microsoft/TypeScript-go/pull/4109) (Open, **jakebailey**, **Copilot**)

**Preserve lone surrogate escapes in string literal emit**

*Preserve lone Unicode surrogate escapes during string literal scanning and emission and add regression tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4110](https://github.com/microsoft/TypeScript-go/pull/4110) (Open, **jakebailey**, **Copilot**)

**Elide namespace imports used only by type\-only export aliases**

*Elide namespace imports used solely by type-only export import aliases to prevent unnecessary runtime imports.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4111](https://github.com/microsoft/TypeScript-go/pull/4111) (Open, **jakebailey**, **Copilot**)

**Fix CommonJS rewrites in shorthand destructuring defaults**

*CommonJS emit logic now properly rewrites imported and exported identifiers in shorthand destructuring default initializers to prevent runtime ReferenceErrors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4112](https://github.com/microsoft/TypeScript-go/pull/4112) (Open)

**Use json/v2 package in Go 1\.27\+**

*Switch to the Go 1.27+ json/v2 package after evaluating compatibility with the tip release.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4113](https://github.com/microsoft/TypeScript-go/pull/4113) (Open)

**Add missing APIs required for WebStorm integration\.**

*Add missing TS-GO service APIs required for WebStorm inspections, find usages, and refactorings to avoid forking.*

 * created by **piotrtomiak**

### [PR microsoft/TypeScript-go#4114](https://github.com/microsoft/TypeScript-go/pull/4114) (Closed)

**fix\(4087\): fix declaration emit modifiers for constructor types**

*Adjusts declaration file emission to correctly include modifiers on constructor types.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#4115](https://github.com/microsoft/TypeScript-go/issues/4115) (Open, **jakebailey**, **Copilot**)

**Exit codes 1 and 2 \(OutputsSkipped vs OutputsGenerated\) are swapped**

*tsgo swaps exit codes 1 and 2 for suppressed versus generated outputs compared to TypeScript 6.0*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4116](https://github.com/microsoft/TypeScript-go/issues/4116) (Open, **jakebailey**, **Copilot**)

**Declaration emit differs for negative numeric const literals**

*tsgo’s declaration emitter transforms negative numeric const literals into -Infinity or approximate values instead of preserving the original literal*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4117](https://github.com/microsoft/TypeScript-go/issues/4117) (Open, **jakebailey**, **Copilot**)

**\`\-\-inlineSourceMap\` leaks into \`\-\-declarationMap\` emit**

*tsgo incorrectly applies inlineSourceMap to declarationMap output, embedding inline maps in .d.ts files*

 * created by **mds-ant**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4118](https://github.com/microsoft/TypeScript-go/issues/4118) (Open)

**Declaration emit drops expando function properties whose assignments are not top\-level expression statements**

*Tsgo's declaration emitter only emits expando function properties assigned as top-level statements and drops those assigned within initializers or blocks.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4119](https://github.com/microsoft/TypeScript-go/issues/4119) (Open)

**U\+2028/U\+2029 inside a multi\-line comment leaves 2 stray bytes in emitted JS \(invalid UTF\-8\)**

*tsgo outputs invalid UTF-8 stray bytes when emitting multi-line comments containing U+2028/U+2029 line separators*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4120](https://github.com/microsoft/TypeScript-go/issues/4120) (Open, **jakebailey**, **Copilot**)

**With multiple \`/\*\* @jsx \*/\` pragmas in one file, tsc uses the first and tsgo uses the last**

*When a file contains multiple /** @jsx */ pragmas, TypeScript’s compiler uses the first pragma but tsgo applies the last.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4121](https://github.com/microsoft/TypeScript-go/issues/4121) (Open, **jakebailey**, **Copilot**)

**Non\-deterministic export specifier order for hoisted exports after a top\-level \`using\`**

*tsgo outputs hoisted export specifiers in random order after a top-level using directive rather than preserving the source declaration order*

 * created by **mds-ant**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4122](https://github.com/microsoft/TypeScript-go/issues/4122) (Open)

**Different emit for import\.defer\(\) in a CommonJS module**

*tsgo emits a Promise.resolve().then wrapper for import.defer in CommonJS modules instead of preserving import.defer calls like TypeScript 6.0*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4123](https://github.com/microsoft/TypeScript-go/issues/4123) (Closed, **jakebailey**, **Copilot**)

**\`in\`/\`out\` variance modifiers on a class member leak into the emitted JS**

*tsgo incorrectly preserves TypeScript ‘in’/‘out’ variance modifiers on class members in the emitted JavaScript instead of stripping them.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4124](https://github.com/microsoft/TypeScript-go/issues/4124) (Closed, **jakebailey**, **Copilot**)

**Different treatment for zero\-byte tsconfig\.json**

*tsgo returns a TS5083 error for a zero-byte tsconfig.json file, unlike TypeScript 6.0 which accepts it.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4125](https://github.com/microsoft/TypeScript-go/issues/4125) (Open, **jakebailey**, **Copilot**)

**'Duplicate function implementation' reported on function redeclaration in checked \.js files**

*tsgo erroneously reports TS2393 duplicate function implementation errors for function redeclarations in checked JavaScript files, whereas TypeScript 6.0 does not.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4126](https://github.com/microsoft/TypeScript-go/issues/4126) (Closed)

**Spurious TS1024 when \`@readonly\` documents a get/set accessor or method in checked JS**

*A JSDoc @readonly on a get accessor in checked JavaScript incorrectly causes a TS1024 error under tsgo.*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4126#issuecomment-4586850091) **hkleungai** said "Seems to be a duplicate of https://github.com/microsoft/typescript-go/issues/3683."

### [Issue microsoft/TypeScript-go#4127](https://github.com/microsoft/TypeScript-go/issues/4127) (Open)

**JSDoc @satisfies on export default is enforced by tsgo but ignored by tsc**

*tsgo enforces JSDoc @satisfies on export default assignments while tsc ignores the type mismatch*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4128](https://github.com/microsoft/TypeScript-go/issues/4128) (Open)

**JSDoc \`@type\` before \`return expr;\` acts as a type assertion in tsgo but is ignored in tsc**

*Tsgo incorrectly treats JSDoc @type annotations before return as type assertions, causing errors ignored by tsc.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4129](https://github.com/microsoft/TypeScript-go/issues/4129) (Open, **jakebailey**, **Copilot**)

**tsgo reports compiler\-option diagnostics even when syntactic errors exist**

*tsgo reports compiler-option errors even when syntactic errors exist, unlike TypeScript which prioritizes syntax diagnostics.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4130](https://github.com/microsoft/TypeScript-go/issues/4130) (Open)

**tsgo reports additional type error when a property is followed by an auto\-accessor of the same name**

*tsgo reports an extra TS2717 error for a property followed by an auto-accessor of the same name.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4131](https://github.com/microsoft/TypeScript-go/issues/4131) (Open, **jakebailey**, **Copilot**)

**tsgo silently swallows JSON syntax errors in an extended tsconfig\.json file**

*tsgo silently ignores JSON syntax errors in extended tsconfig.json files, causing invalid configurations to go unreported.*

 * created by **mds-ant**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4132](https://github.com/microsoft/TypeScript-go/issues/4132) (Open, **jakebailey**, **Copilot**)

**tsgo reports different parameter name for incompatible function types**

*tsgo incorrectly uses the tuple rest parameter name 'args' instead of the declared parameter name when reporting incompatible function types*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4133](https://github.com/microsoft/TypeScript-go/issues/4133) (Open, **jakebailey**, **Copilot**)

**Unquoted tsconfig\.json keys: tsgo reports each TS1327 twice**

*tsgo reports TS1327 errors twice for each unquoted key in tsconfig.json*

 * created by **mds-ant**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4134](https://github.com/microsoft/TypeScript-go/issues/4134) (Open, `bug`, **ahejlsberg**)

**tsgo does not report TS2565 for conditionally\-assigned expando function properties**

*tsgo fails to report TS2565 when accessing a conditionally-assigned expando property on a function, unlike TypeScript 6.0.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4135](https://github.com/microsoft/TypeScript-go/issues/4135) (Closed)

**Nameless \`@param {T}\` tag is a parse error in tsc but silently types the positional parameter in tsgo**

*tsgo silently applies a nameless JSDoc @param tag to the first parameter instead of producing tsc’s parse errors*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4136](https://github.com/microsoft/TypeScript-go/issues/4136) (Closed)

**tsgo does not produce TS6053 for a missing root file**

*tsgo does not emit TS6053 file not found error for a missing root file*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4137](https://github.com/microsoft/TypeScript-go/issues/4137) (Open)

**Single\-character template literal inference consumes a full code point in tsgo vs one UTF\-16 code unit in tsc**

*tsgo incorrectly infers single-character template literals by consuming only a UTF-16 code unit, mis-splitting multi-code-point characters like emojis.*

 * created by **mds-ant**

### [Issue microsoft/TypeScript-go#4138](https://github.com/microsoft/TypeScript-go/issues/4138) (Open, **jakebailey**, **Copilot**)

**tsgo does not reject include spec with \`\.\.\` after a recursive wildcard**

*tsgo does not reject include patterns with '../' following a recursive wildcard, resulting in unintended file emissions.*

 * created by **mds-ant**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4138#issuecomment-4586635441) **jakebailey** said "You've filed so many issues. Can you please say how you're finding these? Through AI? Something else?"

### [PR microsoft/TypeScript-go#4139](https://github.com/microsoft/TypeScript-go/pull/4139) (Open, **jakebailey**, **Copilot**)

**Reject include specs with parent traversal after recursive wildcards**

*Enforce rejection of include patterns containing parent-directory traversals following recursive wildcards and enhance diagnostic handling during tsconfig parsing.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4140](https://github.com/microsoft/TypeScript-go/pull/4140) (Open, **jakebailey**, **Copilot**)

**Align tsconfig JSON key diagnostics with TypeScript**

*Removed duplicate unquoted key TS1327 diagnostics in tsconfig.json, retained parser errors, added TS8009 for optional property tokens, and updated tests.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4141](https://github.com/microsoft/TypeScript-go/pull/4141) (Open, **jakebailey**, **Copilot**)

**Report JSON syntax errors from extended tsconfig files**

*tsgo now surfaces JSON syntax errors in extended tsconfig files and includes regression tests to ensure proper diagnostic attribution.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4142](https://github.com/microsoft/TypeScript-go/pull/4142) (Open, **jakebailey**, **Copilot**)

**Stabilize hoisted export specifier order after top\-level using**

*Stabilize the order of hoisted export specifiers after a top-level using by tracking insertion order and adding a compiler test*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4143](https://github.com/microsoft/TypeScript-go/pull/4143) (Open, **jakebailey**, **Copilot**)

**Prevent inline source maps in declaration map emit**

*Prevent inline source maps in declaration map emit to ensure .d.ts files link to external .d.ts.map files.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

