# Report for 2026-03-10 (Tuesday, March 10th, 2026)

11 different users commented on 14 different issues.

## Recommended Actions

 * Moderation
    * @GabenGar posted rude content in [microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-4039208659)

## Activity Summary

### [Issue microsoft/TypeScript#3841](https://github.com/microsoft/TypeScript/issues/3841) (Open, `Suggestion`, `In Discussion`)

**T\.constructor should be of type T**

*Suggest typing instance.constructor as the class type rather than Function to enable direct static property access without casting.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3612606091) **FrameMuse** apologized for confusion and clarified that typeof this does not refer to the constructor inside the class body but does in static methods
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3613012288) **ExE-Boss** corrected the type of C.constructor by explaining it’s globalThis.Function and provided a correct TypeScript definition
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3831017529) **OldStarchy** explained that constructor signatures and call signatures cannot be inherited, suggested using static factory methods as a workaround, and demonstrated typing constructors by picking static members via Pick
 * [today](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-4033575172) **ljharb** argued that static members were equally difficult to reason about because subclasses could avoid inheriting or shadow them

### [Issue microsoft/TypeScript#50050](https://github.com/microsoft/TypeScript/issues/50050) (Open, `Needs Investigation`, **ahejlsberg**)

**Overloaded function with at least one generic overload can be assigned to any function with at least the same number of parameters**

*Overloaded functions containing at least one generic overload are incorrectly assignable to functions with broader parameter types.*

 * **RyanCavanaugh** assigned to **ahejlsberg**
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/50050#issuecomment-1229494757) **ahejlsberg** explained that in overloaded functions the compiler erased type parameters when relating signatures, noted that fixing it would be a breaking change, referenced an unmerged PR addressing the issue, and identified the issue as a duplicate of #26631
 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/50050#issuecomment-1235526919) **niklasholm** reported encountering a similar issue with unsound generic overload signatures and asked if the documentation should mention this limitation
 * [today](https://github.com/microsoft/TypeScript/issues/50050#issuecomment-4036061183) **jcalz** said "crosslinking to #31978"

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation List**

*Proposed deprecations of outdated TypeScript 6.0 compiler options, with full removal planned for version 7.0.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3874952761) **DanielRosenwasser** said "I think we also passed on conditional import fallbacks: https://github.com/microsoft/TypeScript/issues/50762"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3927313490) **HolgerJeromin** expressed concern about the removal of module:none in TypeScript 6.0-beta and its potential to lock projects on older versions
 * [today](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-4029987037) **n9** expressed agreement and mentioned that the amd module format with outFile is useful for enterprise systems serving as foundation for internal DSLs
 * [later](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-4039208659) **GabenGar** mocked the addition of 'enterprise' and suggested allocating budget to address tech debt

### [Issue microsoft/TypeScript#63203](https://github.com/microsoft/TypeScript/issues/63203) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Narrow a ternary expression to unique symbol type**

*Enable TypeScript to infer a unique symbol type from a ternary expression whose runtime result is constant.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4008486650) **mitar** proposed making symbols work like constant string types in a separate namespace and implementing Symbol.for and Symbol() accordingly to match JavaScript behavior
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4024473596) **snarbles2** explained the difference between unique symbols and the global registry and suggested branding symbols for stronger typing
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4024537224) **mkantor** suggested using Symbol.description instead of inventing a custom `_brand` property
 * [later](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-4038728983) **mitar** said "Interesting. Thanks. Thank you everyone. I think this all makes sense in a way. Thank you for all your time to explain things to me."
 * (later) **mitar** closed the issue

### [PR microsoft/TypeScript#63226](https://github.com/microsoft/TypeScript/pull/63226) (Closed)

**Use optional chaining for getMemoryUsage in GcTimer**

*Use optional chaining instead of non-null assertions for getMemoryUsage in GcTimer.run to avoid runtime errors.*

 * created by **phitonias**
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63226#issuecomment-4026613668) **phitonias** said "@microsoft-github-policy-service agree [company="stb"]"
 * [today](https://github.com/microsoft/TypeScript/pull/63226#issuecomment-4030290040) **MartinJohns** said "Your changes don't align with your description."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63227](https://github.com/microsoft/TypeScript/issues/63227) (Open, `Needs Investigation`, **ahejlsberg**)

**Inference from result of generic function no longer produces a union**

*TypeScript 6 regression: deepEqual’s generic inference from compact fails to produce a union of optional and required properties.*

 * created by **dragomirtitian**
 * [today](https://github.com/microsoft/TypeScript/issues/63227#issuecomment-4032636619) **Andarist** said "bisects to https://github.com/microsoft/TypeScript/pull/62502"

### [PR microsoft/TypeScript#63229](https://github.com/microsoft/TypeScript/pull/63229) (Open)

**Fix document registry creating duplicate buckets for projects with different pathsBasePath**

*Document registry erroneously creates separate buckets for projects with identical compiler options but different pathsBasePath, causing duplicate SourceFile instances.*

 * created by **ekazakov14**
 * [today](https://github.com/microsoft/TypeScript/pull/63229#issuecomment-4032693852) **microsoft-github-policy-service[bot]** prompted the user to agree to the Contributor License Agreement by replying with the appropriate command

### [Issue microsoft/TypeScript#63230](https://github.com/microsoft/TypeScript/issues/63230) (Open, `Bug`, `Domain: Crashes`)

**Compiler crash: Debug Failure in visitEachChildOfIndexSignatureDeclaration**

*TypeScript compiler crashes with a Debug Failure in visitEachChildOfIndexSignatureDeclaration when addInitializer uses an invalid index signature annotation*

 * created by **juanjh1**

### [Issue microsoft/TypeScript#63231](https://github.com/microsoft/TypeScript/issues/63231) (Open, `Needs More Info`)

**exports subpath with array types is not autocompleting**

*VS Code’s JavaScript/TypeScript language server does not autocomplete import paths for subpaths when exports.types is defined as an array*

 * created by **unional**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63232](https://github.com/microsoft/TypeScript/issues/63232) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**exactOptionalPropertyTypes shows a warning when strict is undefined in TypeScript 6\.0**

*exactOptionalPropertyTypes emits a warning requiring strictNullChecks when strict is undefined in tsconfig, despite TypeScript 6.0 defaulting strict mode.*

 * created by **nishiikata**

### [Issue microsoft/TypeScript#63233](https://github.com/microsoft/TypeScript/issues/63233) (Closed, `Duplicate`)

**Typescript**

*TypeScript intentionally disregards type narrowings in callbacks and does not reset them after function calls.*

 * created by **angelgsbrielruano**
 * **angelgsbrielruano** added label `Duplicate`

### [Issue microsoft/TypeScript#63234](https://github.com/microsoft/TypeScript/issues/63234) (Closed, `Working as Intended`)

**TypeScript Rename Refactoring Fails to Preserve Object Shorthand Keys in VS Code**

*Renaming a TypeScript variable in an object shorthand with aliases off renames both key and value instead of expanding shorthand.*

 * created by **Hasan-Mir**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63235](https://github.com/microsoft/TypeScript/issues/63235) (Closed, `7.0 LS Migration`)

**Monorepo package exports suggested as relative imports when using re\-exported identifiers**

*VS Code suggests relative file imports for re-exported identifiers instead of using the package’s export path in a monorepo*

 * created by **aryzing**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63236](https://github.com/microsoft/TypeScript/issues/63236) (Closed)

**دمج**

*Request to merge the changes from commit fc13b0193ddb5857c2b805f13023ef893552b05c into the repository*

 * created by **asd585140-glitch**

