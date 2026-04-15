# Report for 2026-04-09 (Thursday, April 9th, 2026)

10 different users commented on 63 different issues.

## Activity Summary

### [Issue microsoft/TypeScript-go#1017](https://github.com/microsoft/TypeScript-go/issues/1017) (Closed, `wontfix`, **ahejlsberg**)

**Discrepancy inferring widened string type from context**

*Go widens the "c" literal to string in ArrayLike<T> inference, producing string[] that fails to assign to MyEnum[].*

 * (44 weeks ago) **ahejlsberg** added label `wontfix`, and assigned to **ahejlsberg**
 * [43 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1017#issuecomment-2948848984) **Andarist** mentioned an old open PR that fixed the bug and implemented the contextual typing based on index signatures
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1042](https://github.com/microsoft/TypeScript-go/issues/1042) (Open, `Domain: JS`, **sandersn**, **RyanCavanaugh**, **Copilot**)

**Improve \`@overload\` error message to mention name of host function**

*Improve the @overload error message to include the function’s name when missing a return-type annotation.*

 * (1 week ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**, **sandersn**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#1057](https://github.com/microsoft/TypeScript-go/issues/1057) (Open, `Domain: Type Checking`, `Type Ordering`)

**Inconsistency involving discriminated union and flatMap**

*flatMap callback returning either InputOp[] or remove-only arrays causes a TypeScript discriminated union inference error*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1057#issuecomment-4164924448) **jakebailey** said "The above suggestion causes just one break: https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164789350"
 * (1 week ago) **RyanCavanaugh** assigned to **ahejlsberg**, and unassigned **RyanCavanaugh**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1057#issuecomment-4218073370) **RyanCavanaugh** said "The linked PR didn't correctly implement the proposal"
 * (today) **RyanCavanaugh** unassigned **ahejlsberg**, **Copilot**

### [Issue microsoft/TypeScript-go#1094](https://github.com/microsoft/TypeScript-go/issues/1094) (Closed, `bug`, **sandersn**, **Copilot**)

**No error when assigning to getter\-only static class property from another file**

*Assigning to a static getter-only class property from another file does not produce a read-only assignment error as expected.*

 * (43 weeks ago) **RyanCavanaugh** added label `bug`, and assigned to **sandersn**
 * [43 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1094#issuecomment-2951891021) **RyanCavanaugh** explained that two if blocks in isAssignmentToReadonlyEntity were in reverse order compared to Strada and that switching them back triggered module.exports assignment errors
 * [today](https://github.com/microsoft/TypeScript-go/issues/1094#issuecomment-4218110117) **RyanCavanaugh** said "This is fixed"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1116](https://github.com/microsoft/TypeScript-go/issues/1116) (Closed, `Porting PR`, **ahejlsberg**, **Copilot**)

**Port TypeScript PR \#60083: Don't issue implicit any when obtaining the implied type for a binding pattern**

*Port TypeScript PR #60083 to stop issuing implicit any when inferring binding pattern types in the Go port.*

 * (43 weeks ago) **andrewbranch** added label `Porting PR`, assigned to **Copilot**, and unassigned **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1116#issuecomment-4218135329) **RyanCavanaugh** said "Not sure what state this is in, but we have subagents now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1118](https://github.com/microsoft/TypeScript-go/issues/1118) (Closed, `Porting PR`, `blocked`, **weswigham**, **Copilot**)

**Port TypeScript PR \#60195: Assume that type node annotations resolving to error types can be reused**

*Port TypeScript PR #60195 to the Go repository by updating error-type annotation reuse and adjusting baseline tests.*

 * (43 weeks ago) **andrewbranch** assigned to **Copilot**, and unassigned **Copilot**
 * **weswigham** added label `blocked`
 * [today](https://github.com/microsoft/TypeScript-go/issues/1118#issuecomment-4218136264) **RyanCavanaugh** said "Not sure what state this is in, but we have subagents now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1147](https://github.com/microsoft/TypeScript-go/issues/1147) (Closed, `Domain: Editor`, `Needs More Info`)

**vs code typescript go extension taking long time to typecheck for large monorepo**

*TypeScript native preview extension in VS Code experiences prolonged hover type-checking in a large monorepo, whereas normal tsc works fine.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1147#issuecomment-4172933315) **RyanCavanaugh** provided a relevant callstack from the log showing a panic in Node.Expression
 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1147#issuecomment-4173232162) **RyanCavanaugh** said "We need a repro or at least some clues for sure, there doesn't seem to be any way to get into this state"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1147#issuecomment-4218189646) **RyanCavanaugh** said "Please log a new issue if you have a way to repro this. We haven't been able to work backwards to a repro in order to be able to fix anything."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1317](https://github.com/microsoft/TypeScript-go/issues/1317) (Closed, `Domain: CLI`, `Domain: Performance`, **johnfav03**)

**High CPU usage with \-\-watch when idling on MacOS**

*Running tsgo in watch mode on MacOS consumes abnormally high CPU (120–170%) even when idle, unlike tsc -w.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-3928808922) **nfarina** suggested adding fsevents support and a custom watcher.go to improve watch mode CPU usage by building a local tsgo binary
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1317#issuecomment-4124796852) **alexswan93** reported similar idle CPU usage on Windows in watch mode with @typescript/native-preview v7.0.0-dev.20260324.1 and noted using tsgo as a workaround
 * **RyanCavanaugh** assigned to **johnfav03**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#1419](https://github.com/microsoft/TypeScript-go/issues/1419) (Open, `Domain: Editor`, **Copilot**)

**Signature help is wrong for nested calls, has weird applicable ranges**

*Signature help in nested function calls incorrectly applies to call target and trailing whitespace rather than only within parentheses.*

 * (37 weeks ago) **jakebailey** added label `Domain: Editor`, assigned to **Copilot**, and unassigned **Copilot**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#1451](https://github.com/microsoft/TypeScript-go/issues/1451) (Open, `Domain: Porting Meta`, **Copilot**)

**Defer baseline comparisons until end of test**

*Current baselining runs comparisons eagerly, causing tests with in-test edits to remain disabled instead of re-enabling them.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **Copilot**
 * **jakebailey** added label `Domain: Porting Meta`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#1530](https://github.com/microsoft/TypeScript-go/issues/1530) (Closed, `Domain: Type Checking`, `Domain: JSX`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**jsx Prop on \<style\> Tag Not Recognized**

*typescript-go does not recognize the styled-jsx jsx prop on <style> tags despite React interface augmentation*

 * (1 week ago) **RyanCavanaugh** assigned to **weswigham**, **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1530#issuecomment-4218498115) **RyanCavanaugh** said "Based on the linked PR this seems to be fixed. If not, please file a new issue with a more-specific repro so we can ensure we're matching the same steps you're doing."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1570](https://github.com/microsoft/TypeScript-go/issues/1570) (Open, `bug`, `Domain: Declaration Emit`, **weswigham**)

**Nondeterministic declaration emit in test nodeModulesExportsSourceTs**

*The nodeModulesExportsSourceTs (nodenext) test’s baseline comparison is failing due to nondeterministic declaration file emits that omit inner module .d.ts files.*

 * (34 weeks ago) **jakebailey** added labels `bug`, `Domain: Declaration Emit`
 * **RyanCavanaugh** assigned to **weswigham**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [Issue microsoft/TypeScript-go#1609](https://github.com/microsoft/TypeScript-go/issues/1609) (Open, `Domain: Type Checking`, **ahejlsberg**)

**TS2322 error in tsgo but not tsc**

*tsgo incorrectly reports a TS2322 error when spreading a union and assigning E.Foo to E.Bar, even though tsc compiles it successfully.*

 * [32 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1609#issuecomment-3214376523) **ahejlsberg** explained that error elaboration logic incorrectly reported a type mismatch instead of an excess property error because of union type discrimination and type ordering
 * (32 weeks ago) **ahejlsberg** reopened the issue
 * **ahejlsberg** added label `Domain: Type Checking`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#1616](https://github.com/microsoft/TypeScript-go/issues/1616) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**The last overload gave the following error\. Type 'unknown' is not assignable to type 'Foo'**

*After updating the TypeScript native-preview extension, DialogConfig calls fail with unknown not assignable to the expected modal confirmation generic type.*

 * (18 weeks ago) **RyanCavanaugh** added label `Type Ordering`, and assigned to **ahejlsberg**
 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1616#issuecomment-3604417437) **RyanCavanaugh** provided a minimal example that excluded potential red herrings
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#1673](https://github.com/microsoft/TypeScript-go/issues/1673) (Closed, `Crash`, **Copilot**)

**Panic on textDocument/definition**

*A panic occurs during textDocument/definition handling when the requested line number exceeds the document’s line map.*

 * **jakebailey** assigned to **Copilot**
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3738641522) **mustafa519** mentioned also getting similar errors and provided a stack trace
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3792918644) **DanielRosenwasser** said "@mustafa519 I think that is a distinct crash - I filed that here a few weeks ago and it should be fixed now: https://github.com/microsoft/typescript-go/issues/2492"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-4216252577) **jakebailey** said "#3365 will fix this, clamping positions to the allowed ranges (for better or for worse)."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1679](https://github.com/microsoft/TypeScript-go/issues/1679) (Closed, `Domain: Editor`, **iisaduan**)

**Auto import path wrong with symlinks and package\.json exports**

*tsgo auto-import uses the internal symlinked file path instead of the package.json export subpath for the dependency.*

 * **andrewbranch** added label `Domain: Editor`
 * [31 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1679#issuecomment-3255138374) **AlCalzone** said "Possibly related to https://github.com/microsoft/typescript-go/issues/1347 ?"
 * [31 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1679#issuecomment-3255434776) **andrewbranch** said "Probably"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1679#issuecomment-4218450285) **RyanCavanaugh** said "Works now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1682](https://github.com/microsoft/TypeScript-go/issues/1682) (Closed, `Domain: Type Checking`, **ahejlsberg**)

**\`unique symbol\` is now lost when accessed through a property**

*Accessing a unique symbol via a property widens it to symbol in tsgo, causing TS2322 assignment errors.*

 * **RyanCavanaugh** assigned to **ahejlsberg**
 * **jakebailey** added label `Domain: Type Checking`
 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1682#issuecomment-3297401742) **ahejlsberg** explained symbol type widening in mutable locations and identified it as a bug in the old compiler
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#1685](https://github.com/microsoft/TypeScript-go/issues/1685) (Closed, `Domain: Type Checking`, `Domain: JS`, **sandersn**)

**\`ts\-check\` used with \`@typedef\` causes an error on \`module\.exports = \.\.\.\`**

*Combining @ts-check and @typedef in a CommonJS file causes a TS2309 export assignment error with tsgo.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-3470371464) **jakebailey** provided a test case demonstrating the variant of the problem with sample files, compiler errors, and behavior differences when removing module.exports
 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-3470397129) **jakebailey** suggested using `module.exports.nothing = undefined` as a workaround for type-only files to generate separate declarations
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-3921701899) **jbeaudoin-lf** described encountering TS2309 errors when composing modules using require & module.exports under @ts-check and requested that the behavior be supported in the new compiler via compilerOptions
 * [today](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4218381008) **RyanCavanaugh** said "No longer repros with recent changes"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/1685#issuecomment-4218922623) **jbeaudoin-lf** said "Thanks, gonna give it a try tomorrow then !"

### [Issue microsoft/TypeScript-go#1738](https://github.com/microsoft/TypeScript-go/issues/1738) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Error on function type that comes from a function declaration that is declared after usage site**

*tsgo reports an error on arr.map when using typeof on a function declared later in a union, unlike TypeScript 5.8.*

 * [28 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1738#issuecomment-3336750688) **jakebailey** said "Surely this is yet another type ordering problem, since symbols are sorted by declaration location and swapping the order will mean the function sorts earlier..."
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * **ahejlsberg** added label `Type Ordering`
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#1789](https://github.com/microsoft/TypeScript-go/issues/1789) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Inference fails form unions of arrays of different depths \(T\[\] \| T\[\]\[\]\)**

*A generic flat function fails to infer type T for T[]|T[][] arguments under tsgo, though TypeScript 5.8 succeeds.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1789#issuecomment-3378611677) **jakebailey** said "This function is something defined in lib.d.ts. It seems unfortunate that we'd have to define this special type to work around this inference case."
 * [26 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1789#issuecomment-3378695181) **jakebailey** corrected his previous statement and showed the TypeScript lib.d.ts implementation of flat without a union
 * **RyanCavanaugh** assigned to **ahejlsberg**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [PR microsoft/TypeScript-go#1871](https://github.com/microsoft/TypeScript-go/pull/1871) (Closed)

**Persistently cached declaration maps**

*Implement persistent caching of declaration map position mappers within source file snapshots to avoid redundant recomputation across language service requests.*

 * [25 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1871#issuecomment-3407753974) **sheetalkamat** suggested keeping source maps per file until file changes to avoid handling the "--out" scenario and allow cross-project file sharing; explained that past issues with temporary file opens losing source mappers have been fixed in current snapshots
 * [25 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1871#issuecomment-3407756166) **sheetalkamat** said "and yes FAR does do source map jumping"
 * [25 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1871#issuecomment-3412205579) **jakebailey** suggested using per-request caching to avoid persistence and questioned the value of keeping source maps in memory indefinitely for minimal performance gains
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#1882](https://github.com/microsoft/TypeScript-go/issues/1882) (Closed, `Needs More Info`, **johnfav03**)

**Renaming/moving file breaks imports**

*Renaming a TypeScript file in tsgo leads to TS6307 errors due to missing project file listing, unlike TypeScript 5.8.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3633387689) **GitMurf** confirmed correct behavior in VSCode and Neovim and stated intent to update the earlier comment
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1882#issuecomment-3714016968) **Netail** described that renaming a directory or file in VSCode broke alias and relative imports while dependency imports still worked
 * **RyanCavanaugh** assigned to **johnfav03**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#1946](https://github.com/microsoft/TypeScript-go/issues/1946) (Open, `Domain: Editor`, **mjbvz**)

**Support workspace specific typescript version**

*Allow the extension to use a workspace-specific TypeScript version rather than a global one.*

 * (1 week ago) **RyanCavanaugh** added label `Domain: Editor`, removed label `Domain: Editor`, and assigned to **mjbvz**
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#1992](https://github.com/microsoft/TypeScript-go/issues/1992) (Closed, `Crash`, **Copilot**)

**Crash in range formatting when requested on a line that is different from the containing function**

*Range-based formatting on a line outside its containing function panics with a nil pointer dereference.*

 * **DanielRosenwasser** added label `Crash`
 * [22 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1992#issuecomment-3474292889) **DanielRosenwasser** updated the title and explained that requesting formatting ranges after the first line of a function triggered an internal error, provided code examples and the error log
 * **DanielRosenwasser** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/1992#issuecomment-4218602265) **RyanCavanaugh** said "No crash now"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2042](https://github.com/microsoft/TypeScript-go/issues/2042) (Closed, `Crash`, **Copilot**)

**panic handling request textDocument/onTypeFormatting**

*A nil pointer dereference panic occurs in typescript-go LSP's textDocument/onTypeFormatting handler when computing node indentation positions.*

 * **Girbi** added label `Crash`
 * **jakebailey** assigned to **Copilot**
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2042#issuecomment-3677804689) **hitesh-sourcefuse** reported still encountering the same formatting error with the typescriptteam.native-preview extension version 0.20251220.1 and shared the error stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2042#issuecomment-4218622736) **RyanCavanaugh** said "Please log a new issue with a concrete repro; we can't reliably work backwards to what caused this."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2077](https://github.com/microsoft/TypeScript-go/issues/2077) (Closed, `Crash`, **jakebailey**)

**Inlayhint panic**

*The inlay hint provider panics when handling textDocument/inlayHint requests due to an out-of-range line number.*

 * [18 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3607740977) **jakebailey** said "That is an unrelated panic. #2193"
 * **RyanCavanaugh** assigned to **jakebailey**
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3772204936) **rubnogueira** reported experiencing a panic with version 0.20260119.1 but could not reproduce it
 * [today](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-4216253320) **jakebailey** said "#3365 will fix this, clamping positions to the allowed ranges (for better or for worse)."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2086](https://github.com/microsoft/TypeScript-go/issues/2086) (Closed, `bug`, **Copilot**)

**Missing error when shadowing WeakMap/WeakSet in class private field's scope**

*tsgo fails to report reserved-name errors when shadowing WeakMap or WeakSet in class private field scopes.*

 * **RyanCavanaugh** added label `bug`
 * [20 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2086#issuecomment-3530294753) **jakebailey** said "This would be a checker bug; recordPotentialCollisionWithWeakMapSetInGeneratedCode was not ported."
 * **jakebailey** assigned to **Copilot**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#2133](https://github.com/microsoft/TypeScript-go/issues/2133) (Closed, `Domain: Editor`, **gabritto**)

**Renaming a file results in mis\-identifying the right sconfig file**

*Renaming a .spec.ts file in VSCode makes editor apply the base tsconfig instead of the local one, causing persistent errors.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3557143441) **lukpsaxo** provided the same log after restarting tsgo
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2133#issuecomment-3656242346) **PaulRBerg** reported that the issue persisted in the latest version and forced frequent language server restarts
 * **RyanCavanaugh** assigned to **gabritto**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`

### [PR microsoft/TypeScript-go#2272](https://github.com/microsoft/TypeScript-go/pull/2272) (Closed)

**Revamp user preferences serialization/deserialization**

*Refactor user preferences serialization to use struct tags and reflection enabling JSON round-trip and nested configurations.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2272#issuecomment-3634599760) **jakebailey** said "I think I'm going to wait for the other two user pref related PRs to finish and just fix this PR instead of forcing that on everyone."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2272#issuecomment-4209839530) **jakebailey** said "Any opinions on whether or not the typescript/javascript fallback is preserved? Not hard to stick back in."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2272#issuecomment-4209879881) **jakebailey** said "I'm going to restore it, it wasn't really the main point of this change but something I did in the middle of the refactor."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2781](https://github.com/microsoft/TypeScript-go/issues/2781) (Closed, `possible improvement`, **andrewbranch**)

**resolving library types with import assignment \`import = require\(\)\` fails**

*Named and default type exports from @sendgrid/mail included via import assignment work in TypeScript 6.0 but tsgo reports missing members and default-only import errors.*

 * (1 week ago) **RyanCavanaugh** added label `possible improvement`, and assigned to **andrewbranch**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-4145838987) **andrewbranch** explained sendgrid's declaration intent and provided corrected TypeScript export patterns
 * [later](https://github.com/microsoft/TypeScript-go/issues/2781#issuecomment-4225015501) **andrewbranch** verified that mixing named exports and export = has intended limitations and concluded there was nothing more to do on the TS side
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4172657295) **lppedd** suggested dynamically loaded WebAssembly binaries via the WASI Component Model, noted uncertainty about Go's WASI support, and mentioned that Rust appeared to have the edge
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4172677285) **jakebailey** mentioned that Wasm would not help unless a Wasm runtime was shipped or execution was always launched via NAPI
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-4172684436) **lppedd** mentioned that shipping a Wasm runtime in the binary could enable a multilanguage plugin ecosystem and was a reasonable idea
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#2914](https://github.com/microsoft/TypeScript-go/pull/2914) (Open)

**adds tracing \(\-\-generateTrace\)**

*Implement a tracing feature with --generateTrace to output types.json and trace.json files using a context-based approach.*

 * created by **dimitropoulos**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2914#issuecomment-4218382821) **jakebailey** indicated that baselines were unstable and showed a diff with added trace events
 * [today](https://github.com/microsoft/TypeScript-go/pull/2914#issuecomment-4219877730) **dimitropoulos** explained that sampled events were skipped entirely in deterministic mode, leaving only B/E pairs with the deterministic counter to produce stable baselines

### [Issue microsoft/TypeScript-go#2959](https://github.com/microsoft/TypeScript-go/issues/2959) (Closed, `Crash`, **iisaduan**)

**panic handling request textDocument/definition: bad line number**

*The TypeScript Go LSP server panics in textDocument/definition when an out-of-range line number is passed to the line-and-character to position converter.*

 * **Zzzen** added label `Crash`
 * **RyanCavanaugh** assigned to **iisaduan**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2959#issuecomment-4194260358) **samdcoding** provided reproduction steps and logs demonstrating an IDE 'bad line number' error when restoring a modified TS file
 * [today](https://github.com/microsoft/TypeScript-go/issues/2959#issuecomment-4216249686) **jakebailey** said "#3365 will fix this, clamping positions to the allowed ranges (for better or for worse)."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3195](https://github.com/microsoft/TypeScript-go/pull/3195) (Closed)

**API encode/decode fixes**

*Fixed API encoder/decoder by adding missing node properties, assigning a HeritageClause token type, and extending isTypeNode to recognize type keywords.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4163900331) **virtulis** fixed most remaining issues and removed input/output comparison, leaving tests to only check for crashes; noted that namespace blocks become modules after a roundtrip and was unsure of its significance given the confusing AST structure
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4165876279) **andrewbranch** thanked the team and mentioned beginning the "codegen everything" PR ahead of schedule, planning to include the tests for validation
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4168388915) **virtulis** removed code comparing input/output contents after regex cleanup failed, suggested using AST node comparison via a different parser, and requested preview NPM package releases
 * [later](https://github.com/microsoft/TypeScript-go/pull/3195#issuecomment-4225040508) **andrewbranch** said "Landed in #3367"
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3217](https://github.com/microsoft/TypeScript-go/pull/3217) (Closed)

**Watch cli efficiency update**

*Watch CLI efficiency improvements implement debouncing, configuration caching, and dependency parsing to avoid unnecessary recompilations.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4185460956) **andrewbranch** used Copilot to generate tests and discovered multiple race conditions in vfswatch and watcher, linking a commit with detailed results
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4194915866) **johnfav03** thanked for the race tests and added mutexes to the Watcher and FileWatcher structs to fix race conditions and confirmed no race warnings with Copilot tests
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4208738400) **jakebailey** suggested not blocking the PR on LSP support, recommended using dotnet's built-in watcher for manual watch requests, and asked @joj and @navya9singh about feasibility
 * [today](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4215918343) **johnfav03** combined SetWildcardDirectories and UpdateWatchedFiles into UpdateWatchState and stated plans to open a new PR for the second suggestion after feedback

### [PR microsoft/TypeScript-go#3301](https://github.com/microsoft/TypeScript-go/pull/3301) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix type inference ordering inconsistency with discriminated unions and flatMap**

*Replace subtype-based tiebreaker with asymmetric assignability to fix inconsistent discriminated union inference in flatMap.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3301#issuecomment-4164919761) **jakebailey** said "This caused one break: https://github.com/microsoft/TypeScript/pull/63328#issuecomment-4164789350"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3301#issuecomment-4165820632) **typescript-bot** reported that user tests showed one Git clone failure likely unrelated to the change and that everything else looked good
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3307](https://github.com/microsoft/TypeScript-go/pull/3307) (Closed, **RyanCavanaugh**, **Copilot**)

**Add test coverage for styled\-jsx \`jsx\` prop on \`\<style\>\` elements via module augmentation**

*Add a regression test ensuring module augmentation properly recognizes styled-jsx’s jsx and global props on <style> elements without errors.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3315](https://github.com/microsoft/TypeScript-go/pull/3315) (Closed, **RyanCavanaugh**, **Copilot**)

**Improve \`@overload\` error message to include host function name**

*Include the host function name in TS7012 JSDoc @overload error messages for clarity*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3364](https://github.com/microsoft/TypeScript-go/issues/3364) (Open, **DanielRosenwasser**, **andrewbranch**, **mjbvz**, **Copilot**)

**No project found for untitled file**

*VS Code LSP reports a no project found for URI untitled:Untitled-1 error when opening an anonymous unsaved file*

 * created by **DanielRosenwasser**
 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3364#issuecomment-4216990910) **andrewbranch** suggested improving the error message and delaying file removal to handle diagnostic requests after closing an untitled file

### [PR microsoft/TypeScript-go#3365](https://github.com/microsoft/TypeScript-go/pull/3365) (Closed)

**Clamp LSP position conversions**

*Clamp LSP position conversions to handle out-of-range client requests without masking unicode bugs.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3365#issuecomment-4209051843) **jakebailey** said "Uh oh, that test failure is fun, I swear I ran tests locally before!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3365#issuecomment-4212545107) **Andarist** said "I had a similar one here: https://github.com/microsoft/typescript-go/pull/2966 - maybe you could recycle some of its tests or something"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3365#issuecomment-4215459134) **jakebailey** said "Ah, yeah... I truthfully forgot"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3366](https://github.com/microsoft/TypeScript-go/pull/3366) (Closed, **DanielRosenwasser**, **Copilot**)

**Handle 'no project found' gracefully for untitled files**

*Convert missing project errors for untitled LSP files into null responses instead of error notifications*

 * **Copilot** assigned to **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3366#issuecomment-4209741255) **DanielRosenwasser** said "@andrewbranch @jakebailey is this remotely correct? Feels like it's not."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3366#issuecomment-4209761712) **jakebailey** questioned why the client was performing operations on an in-memory file despite no underlying file
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3367](https://github.com/microsoft/TypeScript-go/pull/3367) (Closed)

**Codegen Go and TypeScript SyntaxKinds, ASTs, factories, visitors, type guards, encoders, decoders**

*Implement various updates to Go and TypeScript AST code generation, including SyntaxKind renames, factory adjustments, and structural enhancements.*

 * created by **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3367#issuecomment-4225048512) **andrewbranch** said "There are things that I'd like to improve and additional things I'd like to generate, but need to get some more time-sensitive stuff out of the way first."

### [PR microsoft/TypeScript-go#3368](https://github.com/microsoft/TypeScript-go/pull/3368) (Closed)

**Add go\-osstat to NOTICE\.txt**

*Add the go-osstat dependency to the project's NOTICE.txt file to ensure proper licensing attribution.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3371](https://github.com/microsoft/TypeScript-go/issues/3371) (Closed, `Domain: Editor`, **andrewbranch**, **Copilot**)

**Global keywords in code suggestion shadowed by auto imports with same name**

*Code suggestions for global keywords like "function" are shadowed by same-named module auto-imports, hindering keyword completion.*

 * created by **yume-chan**
 * **yume-chan** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#3372](https://github.com/microsoft/TypeScript-go/issues/3372) (Closed, **jakebailey**, **Copilot**)

**Not having dependency for type should make tsgo error**

*tsgo does not report an error when required Node type definitions are missing despite tsconfig specifying them, unlike tsc.*

 * created by **alexsch01**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3372#issuecomment-4216044558) **jakebailey** said "Hm, we must be missing the code that actually validates that all parts of types can be resolved."
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3373](https://github.com/microsoft/TypeScript-go/pull/3373) (Closed, **jakebailey**, **Copilot**)

**Report "Cannot find type definition file" error for unresolved types in compilerOptions**

*Add diagnostics for failed type directive resolution and fix filesparser propagation to report unresolved type definition errors in tsgo*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3374](https://github.com/microsoft/TypeScript-go/issues/3374) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Code action crash from \`setLastNonTriviaPosition\`**

*A code action crashes the TypeScript printer in setLastNonTriviaPosition while emitting JSX text.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, assigned to **Copilot**, **DanielRosenwasser**, **Copilot**, and unassigned **Copilot**

### [PR microsoft/TypeScript-go#3375](https://github.com/microsoft/TypeScript-go/pull/3375) (Open, **DanielRosenwasser**, **Copilot**)

**Fix index out of bounds panic in setLastNonTriviaPosition for empty strings**

*Add a bounds check to the trailing whitespace loop in setLastNonTriviaPosition to prevent panics on empty strings*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3376](https://github.com/microsoft/TypeScript-go/issues/3376) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**nil pointer dereference during diagnostics request**

*A nil pointer dereference occurs during diagnostics requests when resolving a SourceFile path.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, assigned to **Copilot**, **DanielRosenwasser**, **Copilot**, and unassigned **Copilot**

### [PR microsoft/TypeScript-go#3377](https://github.com/microsoft/TypeScript-go/pull/3377) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in explainRedirectAndImpliedFormat during diagnostics**

*Add an early nil check and cached nil diagnostics in explainRedirectAndImpliedFormat to prevent panics when GetSourceFileByPath returns nil.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#3378](https://github.com/microsoft/TypeScript-go/issues/3378) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**LSP request failure for diagnostics during type serialization**

*The TypeScript language server fails to generate diagnostics during type serialization due to symbol accessibility errors.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3379](https://github.com/microsoft/TypeScript-go/pull/3379) (Open, **DanielRosenwasser**, **Copilot**)

**Fix panic in transformCommonJSExport for named non\-default exports**

*Prevent panic during declaration emit of named non-default CommonJS exports by adding missing symbol accessibility diagnostics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3380](https://github.com/microsoft/TypeScript-go/pull/3380) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in explainRedirectAndImpliedFormat**

*Add nil guard in explainRedirectAndImpliedFormat to prevent panics when GetSourceFileByPath returns nil and add test for case-sensitive file path mismatches.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3380#issuecomment-4217222862) **DanielRosenwasser** said "@copilot try to figure out a test case for this."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3380#issuecomment-4217303834) **Copilot** added a test case for file casing diagnostics on case-sensitive filesystems and verified it reproduced the nil pointer dereference and passed with the fix

### [PR microsoft/TypeScript-go#3381](https://github.com/microsoft/TypeScript-go/pull/3381) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix index out of bounds panic in setLastNonTriviaPosition**

*Prevent index-out-of-bounds panics in setLastNonTriviaPosition’s trailing whitespace trimming by adding a length guard and tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3381#issuecomment-4217217220) **DanielRosenwasser** said "@copilot is there a better repro we can get from a fourslash test? Based on the call stack, probably something to do with leading spaces, or a synthesized JSX text within a JsxElement."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3381#issuecomment-4217232588) **DanielRosenwasser** said "#3375 used the wrong initial prompt, but it looks more promising."
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3382](https://github.com/microsoft/TypeScript-go/pull/3382) (Closed)

**Support LSP \`source\.fixAll\`**

*Enable source.fixAll LSP code action in the TypeScript VS Code extension by porting code and enhancing import handling.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#798](https://github.com/microsoft/TypeScript-go/issues/798) (Open, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**difference in typecheck with 5\.8 \(broken type inference\)**

*TypeScript 5.9 incorrectly reports message.options as possibly undefined in a subscribe callback when using an intersection with {}*

 * [36 weeks ago](https://github.com/microsoft/TypeScript-go/issues/798#issuecomment-3135812443) **birgersp** described encountering a false positive TS18048 error when using parameter properties across packages and provided code examples in version 7.0.0-dev.20250704.1
 * [36 weeks ago](https://github.com/microsoft/TypeScript-go/issues/798#issuecomment-3135856291) **birgersp** observed differing compiled output between tsc and tsgo for a class with a timestamp property and suggested it may not be the same issue
 * [36 weeks ago](https://github.com/microsoft/TypeScript-go/issues/798#issuecomment-3135995938) **jakebailey** said "Not the same issue, no. You're correct to file separately in #1478."
 * (today) **RyanCavanaugh** set milestones to `Post-7.0`, `Possible Improvement`, and removed from milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#799](https://github.com/microsoft/TypeScript-go/issues/799) (Closed, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**difference in typecheck with 5\.8 \(intersection of types breaks some compatibility\)**

*TypeScript 5.9’s stricter inference of intersection types causes compatibility errors in a pipe/map example that previously compiled under 5.8.*

 * **ahejlsberg** removed label `bug`
 * **jakebailey** added label `Type checking`
 * **ahejlsberg** added label `Type Ordering`
 * [today](https://github.com/microsoft/TypeScript-go/issues/799#issuecomment-4218038413) **RyanCavanaugh** said "Closing type ordering problems that don't seem to have a good solution"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#988](https://github.com/microsoft/TypeScript-go/issues/988) (Open, `Domain: Type Checking`, `Type Ordering`, `Domain: Performance`, **jakebailey**)

**tsgo "Type instantiation is excessively deep and possibly infinite" error when using react\-hook\-form**

*tsgo reports excessively deep type instantiation errors on two react-hook-form forms when spreading useForm into FormProvider, unlike tsc.*

 * **jakebailey** added label `Type Ordering`
 * **RyanCavanaugh** assigned to **jakebailey**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/988#issuecomment-4158122110) **jakebailey** said "@justinsmid I haven't looked at this in a while; with #2459 merged it's possible this won't happen anymore. Have you used tsgo recently?"
 * **RyanCavanaugh** added to milestone `Possible Improvement`

### [Issue microsoft/TypeScript-go#993](https://github.com/microsoft/TypeScript-go/issues/993) (Closed, `Domain: JS`, **sandersn**)

**Evolving arrays don't work in JS**

*Declaring an empty array without an explicit type causes TypeScript to infer never[], resulting in errors when pushing numbers.*

 * [34 weeks ago](https://github.com/microsoft/TypeScript-go/issues/993#issuecomment-3168615550) **sandersn** discussed that evolving types in JS now work like TS with noImplicitAny true but not false, questioned the original ad-hoc restriction, and left the bug open for further consideration
 * [34 weeks ago](https://github.com/microsoft/TypeScript-go/issues/993#issuecomment-3168660148) **jakebailey** said "noImplicitAny isn't enabled by default in LS implicit projects, only strictNullChecks and strictFunctionTypes."
 * [21 weeks ago](https://github.com/microsoft/TypeScript-go/issues/993#issuecomment-3504394028) **ahejlsberg** explained that foo’s type varied based on noImplicitAny settings, contrasted Corsa and Strada JS behavior, and highlighted the need to decide whether to align the behaviors
 * [today](https://github.com/microsoft/TypeScript-go/issues/993#issuecomment-4218060142) **RyanCavanaugh** said "This seems fine barring user feedback. Closing for now."
 * (today) **RyanCavanaugh** closed the issue

