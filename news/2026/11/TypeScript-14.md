# Report for 2026-11-14 (Saturday, November 14th, 2026)

9 different users commented on 20 different issues.

## Recommended Actions

 * Response Recommended
    * @sundeep8967 asked to be assigned the issue so they could prepare a pull request with regression tests in [microsoft/TypeScript#65414](https://github.com/microsoft/TypeScript/issues/65414#issuecomment-6882653761)

## Activity Summary

### [Issue microsoft/TypeScript#60874](https://github.com/microsoft/TypeScript/issues/60874) (Open, `Bug`, `Domain: Parser`)

**Generic syntax ambiguity is handled incorrectly**

*Parenthesized comparisons involving generic syntax are incorrectly parsed as non-callable expressions instead of evaluating normally.*

 * (1.8 years ago) **RyanCavanaugh** added label `Domain: Parser`, removed label `Help Wanted`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/60874#issuecomment-6891934964) **magic-akari** said "I’m working on a fix for this."

### [Issue microsoft/TypeScript#65414](https://github.com/microsoft/TypeScript/issues/65414) (Open, `Bug`, `Domain: JS Emit`)

**CommonJS emit gives an imported function the wrong \`this\` when the callee is wrapped**

*CommonJS emit incorrectly preserves the imported module object as `this` when an imported function call is wrapped in parentheses or expressions.*

 * created by **trackoor**
 * [today](https://github.com/microsoft/TypeScript/issues/65414#issuecomment-6882653761) **sundeep8967** reported a reproducible emitter issue involving wrapped imported callees and offered to prepare a fix with regression tests

### [PR microsoft/TypeScript#65506](https://github.com/microsoft/TypeScript/pull/65506) (Closed, `For Backlog Bug`)

**Clarify the error when an interface extends a constrained type parameter**

*Update TypeScript to report TS2884 identifying the type parameter when an interface extending a constrained type parameter fails base-type assignability.*

 * created by **Lior-Altarescu**
 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65506#issuecomment-6884129559) **Lior-Altarescu** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#65507](https://github.com/microsoft/TypeScript/issues/65507) (Open, `Bug`, `Domain: JSDoc`)

**JSDoc \`\#\` link resolution behavior broke in TS 7**

*TypeScript 7 incorrectly resolves both JSDoc {@link Foo.member} and {@link Foo#member} links to the static member instead of distinguishing static and instance properties.*

 * created by **Gerrit0**

### [Issue microsoft/TypeScript#65508](https://github.com/microsoft/TypeScript/issues/65508) (Open, `Bug`, `Domain: check: Order Dependence`)

**Go checker: finite indexed\-access constraint loses its explicit bound depending on prior file checking**

*Go checker reports a spurious TS2339 for indexed-access constraints when prior file-checking order causes the explicit bound to be lost.*

 * created by **BleedingDev**

### [Issue microsoft/TypeScript#65509](https://github.com/microsoft/TypeScript/issues/65509) (Closed)

**Control flow analysis: a read in or after a loop gets the type of an unfinished loop analysis**

*Control-flow analysis incorrectly reuses incomplete loop narrowing, causing reads inside or after loops to receive stale, unsound types.*

 * created by **somdoron**
 * (today) **somdoron** closed the issue

### [PR microsoft/TypeScript#65510](https://github.com/microsoft/TypeScript/pull/65510) (Open, `Domain: Performance`, `For Milestone Bug`, `For Backlog Bug`, **johnfav03**)

**Reject structurally incomplete type arguments in expressions**

*Reject structurally incomplete speculative type arguments so relational expressions parse correctly while preserving valid generics, diagnostics, and parser performance.*

 * created by **magic-akari**
 * (later) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Milestone Bug`, and assigned to **johnfav03**

### [PR microsoft/TypeScript#65511](https://github.com/microsoft/TypeScript/pull/65511) (Closed, `Domain: Performance`, `For Backlog Bug`)

**fix: share in\-flight getSourceFile requests in native\-preview async API \(\#65503\)**

*Share concurrent native-preview `getSourceFile` requests per path to prevent redundant server fetches while allowing retries after failures.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65511#issuecomment-6894375032) **zhengdaodeguL** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65512](https://github.com/microsoft/TypeScript/pull/65512) (Closed, `For Backlog Bug`)

**fix: deduplicate rename edits for dynamic imports with \.ts specifiers**

*Deduplicate duplicate dynamic-import rename edits for `.ts` specifiers to prevent language server overlap panics.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65513](https://github.com/microsoft/TypeScript/issues/65513) (Open, `Bug`)

**Object\-rest for\-of lowering skips transformations on direct body statements**

*Object-rest lowering skips transformations for direct statements in for-of bodies, producing invalid loop initializers and broken function declarations.*

 * created by **Vl4dC**

### [Issue microsoft/TypeScript#65514](https://github.com/microsoft/TypeScript/issues/65514) (Open, `Bug`, `Domain: classes`)

**TS2729 when a field initializer reads an inherited property redeclared with \`declare\`**

*TypeScript incorrectly reports TS2729 when a derived field initializer reads an inherited property redeclared with `declare`, despite the property being initialized by the base class.*

 * created by **mizchi**

### [PR microsoft/TypeScript#65515](https://github.com/microsoft/TypeScript/pull/65515) (Closed, `For Backlog Bug`)

**fix: resolve JSDoc '\#' links to instance members**

*Fix JSDoc `#` links to resolve instance members instead of static members, matching TS 6 behavior and adding regression coverage.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

