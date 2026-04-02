# Report for 2026-02-21 (Saturday, February 21st, 2026)

6 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @jogibear9988 asked about plans for a WASM version of TypeScript 7.0 and its integration in [microsoft/TypeScript#62963](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3940657202)

## Activity Summary

### [Issue microsoft/TypeScript#23911](https://github.com/microsoft/TypeScript/issues/23911) (Open, `Suggestion`, `In Discussion`)

**Experiment with always using parameters from base types for derived methods**

*Automatically inherit base method parameter types in derived classes to eliminate redundant signatures and prevent implicit any issues.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/23911#issuecomment-1780327203) **tadhgmister** criticized using an arrow function override because it lost prototype reference and class optimizations, provided an alternative implementation using Parameters and ReturnType generics, and suggested supporting issue #36165
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/23911#issuecomment-2079145023) **hediet** suggested covering the `override` case first and provided a simple TypeScript reference implementation using `Parameters` and `ReturnType` utilities
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/23911#issuecomment-3877871522) **ghost** proposed a syntax for typing non-arrow function methods to maintain prototype chains and avoid generic issues with Parameters<> and ReturnType<>
 * [today](https://github.com/microsoft/TypeScript/issues/23911#issuecomment-3939333243) **tadhgmister** demonstrated that assigning a subclass method via Foo.prototype outside the class remained semantically equivalent to in-class definitions in vanilla JavaScript and preserved runtime performance, noted potential decorator limitations, and advocated for issue #36165

### [Issue microsoft/TypeScript#62963](https://github.com/microsoft/TypeScript/issues/62963) (Open, `Meta-Issue`)

**Transition to 6\.0 Maintenance Mode**

*TypeScript 6.0 is entering maintenance mode with only critical fixes, deprecations, and compatibility changes accepted to accelerate the transition to the Go-based 7.0 release.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3724470262) **RyanCavanaugh** replied that test-only PRs would be accepted after 7.0 but currently no due to large ongoing PRs causing merge conflicts
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3787149661) **KnorpelSenf** asked whether regressions from 4.7 to 4.8 and imported bugs would be fixed after the 7.0 release
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3842750039) **RyanCavanaugh** said "@KnorpelSenf yep!"
 * [later](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3940657202) **jogibear9988** asked whether there was a plan for a WASM version of TypeScript 7.0 and how it would integrate into the Monaco editor or client-side websites

### [Issue microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add switch to disable \_var unused variable prevention**

*Add a tsconfig option to disable automatic ignoring of underscore-prefixed unused variables so the compiler still reports them to IDE.*

 * created by **ackvf**
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3905192485) **guillaumebrunerie** suggested using an underscore suffix rather than a prefix to avoid variable shadowing, noted TypeScript's standalone usage invalidates IDE-only error filtering, and recommended configuring ESLint’s no-unused-variables rule
 * [later](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3940793267) **darshjme-codes** said "Triage: Feature request: Disable unused variable warnings for _var prefix Labels: Suggestion, Strictness, Compiler Options | Similar: _unused pattern convention"

### [Issue microsoft/TypeScript#63149](https://github.com/microsoft/TypeScript/issues/63149) (Open)

**\[TS\]: Incorrect handling of \`JSDoc\` description of interface property**

*VS Code incorrectly strips parentheses-enclosed JSX tags from interface property JSDoc descriptions in hover tooltips.*

 * created by **psnet**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [later](https://github.com/microsoft/TypeScript/issues/63149#issuecomment-3940793235) **darshjme-codes** said "Triage: JSDoc description handling bug Labels: Bug, JSDoc, Language Service | Impact: Documentation display issues in editors"

### [Issue microsoft/TypeScript#63159](https://github.com/microsoft/TypeScript/issues/63159) (Open, `Bug`, `Domain: LS: TSServer`)

**False positive "Private field \.\.\. must be declared in an enclosing class\."**

*VS Code wrongly reports private field must be declared errors in a second JavaScript file due to cross-tab state pollution.*

 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3924091663) **bkatzung** said ""
 * **mjbvz** unassigned **mjbvz**
 * [later](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3940793141) **darshjme-codes** said "Triage: False positive "Private field must be initialized" Labels: Bug, Strictness, Private Fields | Type: Control flow analysis gap"

### [Issue microsoft/TypeScript#63161](https://github.com/microsoft/TypeScript/issues/63161) (Closed, `Suggestion`, `Declined`)

**Make compiler option values case sensitive**

*Propose deprecating and removing case-insensitive compiler option values to enforce consistent casing in tsconfig.json.*

 * created by **remcohaszing**
 * [later](https://github.com/microsoft/TypeScript/issues/63161#issuecomment-3940793095) **darshjme-codes** said "Triage: Compiler option values case sensitivity Labels: Suggestion, Compiler Options, Breaking Change | Impact: Would require major version"

### [Issue microsoft/TypeScript#63162](https://github.com/microsoft/TypeScript/issues/63162) (Closed, `Duplicate`)

**Module resolution: Extension required when moduleResolution=bundler and imports/exports used**

*TypeScript's bundler moduleResolution requires explicit .js extensions for imports and exports, causing build-time failures despite working in Vite.*

 * created by **polson136**
 * [later](https://github.com/microsoft/TypeScript/issues/63162#issuecomment-3940793062) **darshjme-codes** said "Triage: Module resolution error requiring extension Labels: Bug, Module Resolution, Suggestion | Context: ESM/CJS interop issue"

### [Issue microsoft/TypeScript#63173](https://github.com/microsoft/TypeScript/issues/63173) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: Maximum call stack size exceeded when declare const enum has a computed property named \[object\] followed by an object member**

*The compiler overflows the call stack when a const enum has a computed [object] member followed by an object member.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/63173#issuecomment-3938428643) **knowltonn287-source** posted a code snippet illustrating a const enum with conflicting member names
 * [later](https://github.com/microsoft/TypeScript/issues/63173#issuecomment-3940793033) **darshjme-codes** said "Triage: Stack overflow crash Labels: Bug, Crash, Compiler | Priority: High (crashes prevent compilation)"

### [PR microsoft/TypeScript#63176](https://github.com/microsoft/TypeScript/pull/63176) (Closed, `For Backlog Bug`)

**fix\(checker\): mark getter/setter as deprecated when any declaration has @deprecated**

*Restore marking of getter/setter pairs as deprecated when either accessor includes a @deprecated tag.*

 * created by **TheAbMehta**
 * **typescript-bot** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63176#issuecomment-3938363379) **TheAbMehta** said "@microsoft-github-policy-service agree"
 * (today) **TheAbMehta** closed the issue

### [PR microsoft/TypeScript#63177](https://github.com/microsoft/TypeScript/pull/63177) (Open, `For Backlog Bug`)

**fix\(25083\): allow element access expressions with string or numeric literal arguments as computed properties**

*Enable element access expressions with literal string or numeric arguments to be treated as computed properties.*

 * created by **hayatexe**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63177#issuecomment-3939577492) **hayatexe** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#63178](https://github.com/microsoft/TypeScript/pull/63178) (Open, `For Backlog Bug`)

**Fix Debug Failure crash when resolving overloaded decorators with explicit tuple rest parameters**

*Correct getLegacyDecoratorArgumentCount to use getParameterCount instead of signature.parameters.length to avoid crashes resolving overloaded decorators with tuple rest parameters*

 * created by **hayatexe**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63178#issuecomment-3940936150) **Andarist** said "There is already an open PR fixing this: https://github.com/microsoft/TypeScript/pull/63098"

### [PR microsoft/TypeScript#63179](https://github.com/microsoft/TypeScript/pull/63179) (Open, `For Backlog Bug`)

**Fix startup crash when redefining global Array with @noLib**

*Prevent startup crashes under --noLib when redefining Array by falling back to an empty generic type for array resolution.*

 * created by **hayatexe**
 * **typescript-bot** added label `For Backlog Bug`

### [PR microsoft/TypeScript#63180](https://github.com/microsoft/TypeScript/pull/63180) (Open, `For Milestone Bug`)

**Fix duplicate error message for literal union types**

*Suppress duplicate generalization in error messages for literal unions whose members all share a base type.*

 * created by **erdinccurebal**
 * **typescript-bot** added label `For Milestone Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63180#issuecomment-3940759815) **erdinccurebal** said "@microsoft-github-policy-service agree"

