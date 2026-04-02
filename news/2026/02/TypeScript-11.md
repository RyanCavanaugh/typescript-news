# Report for 2026-02-11 (Wednesday, February 11th, 2026)

7 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @valler criticized the automated response as useless in [microsoft/TypeScript#63109](https://github.com/microsoft/TypeScript/issues/63109#issuecomment-3887095407)

## Activity Summary

### [Issue microsoft/TypeScript#63109](https://github.com/microsoft/TypeScript/issues/63109) (Open)

**Clarify tsconfig extends resolution**

*Clarify and update tsconfig.json 'extends' resolution documentation to explain Node.js-style specifier handling.*

 * created by **valler**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63109#issuecomment-3880022212) **RyanCavanaugh** provided an auto-generated list of similar issues
 * [today](https://github.com/microsoft/TypeScript/issues/63109#issuecomment-3887095407) **valler** said "About the automated response. Hardly any issue listed is about extends. Those two or three which are, are feature requests or bug reports. None is about documentation or spec. It's (100%) useless."

### [Issue microsoft/TypeScript#63126](https://github.com/microsoft/TypeScript/issues/63126) (Open)

**Overloads should be filtered by unmet constraints of type parameters**

*TypeScript should filter out overloaded signatures with unmet type parameter constraints, showing only the compatible overload.*

 * [today](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884338049) **snarbles2** expressed concern about unintended silent member disappearance and suggested that permissible arguments shouldn't be constrained, illustrating with a code example
 * [today](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884625398) **AFatNiBBa** explained that the call and constructor signatures of `f` are separate, demonstrated with examples how returning a primitive in a constructor is ignored at runtime, and requested a way to express this behavior in `f`’s type
 * [today](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3884682547) **AFatNiBBa** noted that the workaround failed when the function wasn’t called directly, demonstrated the difference in inferred types with original, workaround, and noCtor, and argued that noCtor should work since Array.flatMap doesn’t accept constructors
 * [later](https://github.com/microsoft/TypeScript/issues/63126#issuecomment-3890880558) **jcalz** noted the issue concerned instantiation expressions, stated the behavior was intended and more a missing feature, and marked it as a duplicate of #51694

### [PR microsoft/TypeScript#63127](https://github.com/microsoft/TypeScript/pull/63127) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Ensure node is installed in release publisher**

*Install Node in the release publisher image to restore npm support after it was removed from the base image*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63128](https://github.com/microsoft/TypeScript/pull/63128) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**Fixed a crash related to variadic tuple elements with intersections containing \`InstantiableNonPrimitive\`**

*TypeScript crashes when variadic tuple elements have intersections containing InstantiableNonPrimitive types.*

 * created by **Andarist**
 * (today) **typescript-bot** added label `For Uncommitted Bug`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63129](https://github.com/microsoft/TypeScript/issues/63129) (Open)

**TSC should not error on valid subpath specifier syntax \(TS2877\)**

*TypeScript incorrectly reports TS2877 errors for non-relative .ts subpath specifiers (e.g., import "#alice.ts") despite their validity.*

 * created by **valler**
 * [today](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3886866050) **valler** explained that clients only care about URLs, pointed out that server-side engines happily consume TS files without altering postfix, and illustrated usage with import map and TS import examples
 * [today](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3886967568) **valler** provided an example of a package.json configuration exporting all source files
 * [later](https://github.com/microsoft/TypeScript/issues/63129#issuecomment-3891786865) **jakebailey** said "If you flip your resolution mode to a node-based one (or bundler), I believe this error goes away. The playground is set to esnext by default."

### [Issue microsoft/TypeScript#63130](https://github.com/microsoft/TypeScript/issues/63130) (Open)

**Array\.at\(\) doesn't consider array length**

*TypeScript errors occur when using array.at(-1) after checking non-empty array length, requiring needless optional chaining.*

 * created by **johndeighan**
 * [today](https://github.com/microsoft/TypeScript/issues/63130#issuecomment-3887322770) **MartinJohns** noted that the issue template was not filled out properly and marked the issue as a duplicate of #30406

### [Issue microsoft/TypeScript#63131](https://github.com/microsoft/TypeScript/issues/63131) (Open)

**Allow non\-null assertion operator on destructuring**

*Allow the non-null assertion operator in object destructuring to avoid repeating long property names.*

 * created by **AFatNiBBa**
 * [later](https://github.com/microsoft/TypeScript/issues/63131#issuecomment-3889592788) **MartinJohns** said "Duplicate of #17390."

