# Report for 2026-02-12 (Thursday, February 12th, 2026)

7 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @nikelborm provided a workaround and detailed the issue for maintainer acknowledgement in [microsoft/TypeScript#43869](https://github.com/microsoft/TypeScript/issues/43869#issuecomment-3892252160)
    * @AFatNiBBa reported a bug with screenshot and explanation in [microsoft/TypeScript#63126](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3896705414)
    * @valler asked if any other configuration could cause the issue in [microsoft/TypeScript#63129](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3892892166)
    * @AFatNiBBa asked whether something has changed since the original decision given criticisms and complexity of alternatives in [microsoft/TypeScript#63131](https://github.com/microsoft/TypeScript/issues/63131#issuecomment-3896667464)
    * @james-boxem provided an additional minimal reproduction in [microsoft/TypeScript#63134](https://github.com/microsoft/TypeScript/issues/63134#issuecomment-3897889937)
    * @james-boxem provided additional information about type-checking behavior under strict options in [microsoft/TypeScript#63134](https://github.com/microsoft/TypeScript/issues/63134#issuecomment-3897900665)

## Activity Summary

### [Issue microsoft/TypeScript#43869](https://github.com/microsoft/TypeScript/issues/43869) (Open, `Bug`, `Effort: Moderate`, `Domain: JSDoc`, `Rescheduled`, **orta**)

**JSDoc @link not resolved across modules**

*JSDoc @link tags referencing imported classes across modules fail to resolve as clickable links.*

 * (1.5 years ago) **RyanCavanaugh** added label `Domain: JSDoc`, set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [today](https://github.com/microsoft/TypeScript/issues/43869#issuecomment-3892252160) **nikelborm** reported facing the same problem and shared a workaround by explicitly exporting referenced local types, and described unsuccessful import type and export type approaches

### [Issue microsoft/TypeScript#63126](https://github.com/microsoft/TypeScript/issues/63126) (Open)

**Overloads should be filtered by unmet constraints of type parameters**

*TypeScript should filter out overloaded signatures with unmet type parameter constraints, showing only the compatible overload.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884625398) **AFatNiBBa** explained that the call and constructor signatures of `f` are separate, demonstrated with examples how returning a primitive in a constructor is ignored at runtime, and requested a way to express this behavior in `f`’s type
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884682547) **AFatNiBBa** noted that the workaround failed when the function wasn’t called directly, demonstrated the difference in inferred types with original, workaround, and noCtor, and argued that noCtor should work since Array.flatMap doesn’t accept constructors
 * [today](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3890880558) **jcalz** noted the issue concerned instantiation expressions, stated the behavior was intended and more a missing feature, and marked it as a duplicate of #51694
 * [later](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3896705414) **AFatNiBBa** reported a bug, noted that documentation states the feature should work, and included a screenshot

### [Issue microsoft/TypeScript#63129](https://github.com/microsoft/TypeScript/issues/63129) (Open)

**TSC should not error on valid subpath specifier syntax \(TS2877\)**

*TypeScript incorrectly reports TS2877 errors for non-relative .ts subpath specifiers (e.g., import "#alice.ts") despite their validity.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3886866050) **valler** explained that clients only care about URLs, pointed out that server-side engines happily consume TS files without altering postfix, and illustrated usage with import map and TS import examples
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3886967568) **valler** provided an example of a package.json configuration exporting all source files
 * [today](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3891786865) **jakebailey** said "If you flip your resolution mode to a node-based one (or bundler), I believe this error goes away. The playground is set to esnext by default."
 * [today](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3892892166) **valler** said "Could it be anything else? I have both module and moduleResolution set to nodenext with resolvePackageJsonExports and resolvePackageJsonImports set to true"

### [Issue microsoft/TypeScript#63131](https://github.com/microsoft/TypeScript/issues/63131) (Open)

**Allow non\-null assertion operator on destructuring**

*Allow the non-null assertion operator in object destructuring to avoid repeating long property names.*

 * created by **AFatNiBBa**
 * [today](https://github.com/microsoft/TypeScript/issues/63131#issuecomment-3889592788) **MartinJohns** said "Duplicate of #17390."
 * [later](https://github.com/microsoft/TypeScript/issues/63131#issuecomment-3896667464) **AFatNiBBa** asked whether anything had changed since the original decision given raised criticisms and complexity of alternatives

### [Issue microsoft/TypeScript#63132](https://github.com/microsoft/TypeScript/issues/63132) (Open)

**Regression: Mapped types are no longer homomorphic when wrapped in certain conditional types**

*TypeScript 3.9 regression breaks homomorphic mapped types in conditional types, so KeyMap<number> expands to an object rather than number.*

 * created by **aweebit**
 * [today](https://github.com/microsoft/TypeScript/issues/63132#issuecomment-3893737004) **Andarist** noted that the example felt artificial but demonstrated a genuine issue where homomorphic mapped types don’t distribute because keyof T becomes a substitution type in the conditional’s true branch

### [PR microsoft/TypeScript#63133](https://github.com/microsoft/TypeScript/pull/63133) (Open, `For Uncommitted Bug`)

**Fixed mapped types not being considered as homomorphic with substitution constraints**

*Mapped types are now correctly recognized as homomorphic when using substitution constraints in TypeScript.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63134](https://github.com/microsoft/TypeScript/issues/63134) (Closed)

**Promise\<T\|undefined\>\.then\(\.\.\.\) accepts wrong type of argument**

*TypeScript erroneously accepts .then callbacks with a number parameter for Promise<number|undefined> without handling undefined.*

 * created by **james-boxem**
 * [later](https://github.com/microsoft/TypeScript/issues/63134#issuecomment-3897883133) **MartinJohns** pointed out that the code example fails type checks and produces an error contrary to the issue description
 * [later](https://github.com/microsoft/TypeScript/issues/63134#issuecomment-3897889937) **james-boxem** observed that type checks passed unexpectedly and provided a more general minimal reproduction
 * [later](https://github.com/microsoft/TypeScript/issues/63134#issuecomment-3897900665) **james-boxem** said "OK, I now see the error if I turn on "strict" mode. But when "strict" is disabled but "strictNullChecks" = true, this passes type checks"
 * [later](https://github.com/microsoft/TypeScript/issues/63134#issuecomment-3897906298) **james-boxem** said "OK, I can turn on "strictFunctionTypes" and the error is caught. Not a bug, my bad."
 * (later) **james-boxem** closed the issue

