# Report for 2026-05-15 (Friday, May 15th, 2026)

10 different users commented on 89 different issues.

## Recommended Actions

 * Response Recommended
    * @Jelcoo asked if there's a built-in way to CPU profile in WebStorm and reported issues with lsp4ij in [microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4463720030)

## Activity Summary

### [Issue microsoft/TypeScript-go#1042](https://github.com/microsoft/TypeScript-go/issues/1042) (Open, `Domain: JS`, **sandersn**, **RyanCavanaugh**, **Copilot**)

**Improve \`@overload\` error message to mention name of host function**

*Improve the @overload error message to include the function’s name when missing a return-type annotation.*

 * (6 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **RyanCavanaugh**, **sandersn**
 * (today) **RyanCavanaugh** assigned to **Copilot**, and unassigned **Copilot**

### [Issue microsoft/TypeScript-go#1419](https://github.com/microsoft/TypeScript-go/issues/1419) (Closed, `Domain: Editor`, **Copilot**)

**Signature help is wrong for nested calls, has weird applicable ranges**

*Signature help in nested function calls incorrectly applies to call target and trailing whitespace rather than only within parentheses.*

 * (29 weeks ago) **jakebailey** assigned to **Copilot**, and unassigned **Copilot**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#1949](https://github.com/microsoft/TypeScript-go/pull/1949) (Closed, **jakebailey**, **Copilot**)

**Fix signature help applicable span for nested calls**

*Improves signature help applicable span for nested function calls to correctly handle empty argument lists and prioritize outer calls.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3608039844) **Copilot** fixed formatting by running npx hereby format in commit 41f4bca
 * (1 month ago) **RyanCavanaugh** set milestones to `TypeScript 7.0 RC`, `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#2280](https://github.com/microsoft/TypeScript-go/issues/2280) (Closed, `Domain: Editor`, **gabritto**)

**Port \`implement interface\` quick fix**

*Port the implement interface quick fix from TypeScript to TS-Go to provide automated interface implementation support.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3644087661) **a-tarasyuk** said "@Tyriar, I'm curious, what are some other quick fixes that are among the top five most commonly used? :slightly_smiling_face:"
 * [22 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2280#issuecomment-3644200857) **Tyriar** said "I'm not sure I have 5 commonly used ones actually. It's hard to remember them off the top of my head, I use the promise  await conversion one occasionally is one that comes to mind."
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2443](https://github.com/microsoft/TypeScript-go/issues/2443) (Closed, `documentation`, **RyanCavanaugh**)

**\[Doc\]: paths map value points to removed baseUrl value**

*Inline documentation incorrectly references the removed baseUrl option for computing paths map values.*

 * (7 weeks ago) **RyanCavanaugh** added label `documentation`, set milestone to `TypeScript 7.0 RC`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2443#issuecomment-4462067021) **RyanCavanaugh** said "Fixed in the linked PR above"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3242](https://github.com/microsoft/TypeScript-go/issues/3242) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**No error for values named 'Object' \(in CommonJS\)**

*TypeScript incorrectly permits a class named Object to be used with object spread in CommonJS modules without reporting an error.*

 * **RyanCavanaugh** assigned to **RyanCavanaugh**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/3242#issuecomment-4248107590) **RyanCavanaugh** said "#2087"
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, removed from milestone `TypeScript 7.0 RC`, assigned to **Copilot**, and unassigned **Copilot**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3499](https://github.com/microsoft/TypeScript-go/pull/3499) (Closed)

**feat\(2280\): Port implement interface quick fix**

*Port the implement interface quick fix feature to support automatic interface implementation.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3499#issuecomment-4401910486) **jakebailey** said "Though I asked copilot to help me find missing tests (since it's hard to do by hand) and it started trying to implement them, so, maybe it is possible 😄 "
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3499#issuecomment-4402886388) **jakebailey** shared a diff that added filename prefixes for allowed rangeAfterCodeFix tests and updated validateCodeFixCommands to accept a filename
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3499#issuecomment-4405520208) **a-tarasyuk** thanked Jake Bailey and mentioned pushing changes that add .not.codeFixAvailable support and remove unrelated generated tests
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3543](https://github.com/microsoft/TypeScript-go/issues/3543) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **RyanCavanaugh**, **Copilot**)

**Baselines: CJS \`module\.exports = {}\` now emits \`export = \_default\` with inlined object type instead of named exports**

*CJS module.exports patterns now emit export = _default with inlined object types instead of named exports, requiring semantic validation*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3543#issuecomment-4399985812) **weswigham** explained that merging namespaces was unnecessary and local name swaps were nonfunctional, and suggested retriaging or opening a PR to adjust the emitted name
 * (1 week ago) **weswigham** assigned to **RyanCavanaugh**, and unassigned **weswigham**
 * **RyanCavanaugh** assigned to **Copilot**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3676](https://github.com/microsoft/TypeScript-go/issues/3676) (Closed, **gabritto**)

**tsconfig diagnostics not refreshed if no TS/JS files are open**

*Diagnostic errors for a removed 'baseUrl' option in tsconfig.json fail to clear when no TS or JS files are open.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3676#issuecomment-4360656283) **DanielRosenwasser** said "Maybe we can do something custom with our extension's client when a config file changes?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3676#issuecomment-4360821353) **jakebailey** recommended pushing an empty diagnostic set when a project became unreferenced after all files were closed
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692) (Closed)

**Excessive CPU usage**

*WebStorm’s ts-go server often consumes 80-100% CPU when adding new imports in a monorepo frontend until restarted.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4391545891) **RyanCavanaugh** said "We need some clue as to what WebStorm is doing differently - sending different requests, etc?"
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4425907817) **AndrewSouthpaw** asked what diagnostic information could be collected to help investigate tsgo's high CPU usage
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4426707829) **andrewbranch** asked whether the reporter was using WebStorm, suggested reproducing the issue in VS Code and using TypeScript Native Preview commands to gather logs and CPU profiles, and recommended collecting logs and CPU profiles when reproducing in WebStorm
 * [today](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4463720030) **Jelcoo** noted that WebStorm had no built-in CPU profiling and that using lsp4ij caused issues and failed to initialize the project

### [Issue microsoft/TypeScript-go#3701](https://github.com/microsoft/TypeScript-go/issues/3701) (Open, **jakebailey**, **Copilot**)

**When using \`module=commonjs\`, Array destructuring is transpiled with wrong \(non\-iterator\) behavior**

*Compiling with module=commonjs wrongly transpiles exported array destructuring into fixed index access instead of iterator logic.*

 * **jakebailey** assigned to **jakebailey**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3701#issuecomment-4455680011) **jakebailey** asked for an explanation of necessity and queried if it was due to dropping ES5 and downlevelIteration
 * [today](https://github.com/microsoft/TypeScript-go/issues/3701#issuecomment-4464739228) **blickly** said "We set downlevelIteration even when targetting ES2015+ since we need iterator support.  With downlevelIteration going away, we don't want to lose support for iterators."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3701#issuecomment-4464760179) **jakebailey** expressed confusion about how the option had any effect and declared issue #3705 ready to go

### [Issue microsoft/TypeScript-go#3758](https://github.com/microsoft/TypeScript-go/issues/3758) (Open, `bug`, **RyanCavanaugh**, **Copilot**)

**File argument of \`@\` crashes CLI**

*Providing `@` with no file path to tsgo crashes the CLI with a “path "" is not absolute” panic.*

 * (1 week ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3758#issuecomment-4461879124) **RyanCavanaugh** reported that the panic occurred for any file and that the path wasn't processed correctly before reading
 * (today) **RyanCavanaugh** assigned to **Copilot**, and unassigned **Copilot**

### [Issue microsoft/TypeScript-go#3768](https://github.com/microsoft/TypeScript-go/issues/3768) (Closed, `Crash`, **andrewbranch**, **Copilot**)

**Panic in overlayfs\.go when switching back to a TS file after saving package\.json**

*Saving package.json then switching back to a TypeScript file triggers a panic in typescript-go’s overlayFS due to a missing overlay.*

 * (yesterday) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, assigned to **andrewbranch**, and unassigned **RyanCavanaugh**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3800](https://github.com/microsoft/TypeScript-go/issues/3800) (Closed, `bug`, `Domain: Editor`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Error when auto\-importing relative \.css augmentation from ESM file with package\.json**

*Auto-importing a relative CSS augmentation in a NodeNext ESM project triggers a panic due to the unknown .css extension.*

 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3806](https://github.com/microsoft/TypeScript-go/issues/3806) (Open, `Needs More Info`)

**Intermittent \`TS2307\` on directory imports — \`tsc\` passes, \`tsgo\` intermittently fails on the same tree**

*tsgo intermittently throws TS2307 for parent-directory imports using package.json main with bundler resolution, while tsc passes reliably.*

 * created by **Akshay090**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3806#issuecomment-4464392347) **RyanCavanaugh** said "If you can confirm repro on latest we can try another round of synthesizing a repro, or if you can come up with a concrete repro that'd be great."

### [Issue microsoft/TypeScript-go#3814](https://github.com/microsoft/TypeScript-go/issues/3814) (Closed, `wontfix`)

**\`skipLibCheck\` does not suppress TS2430 for interface merging errors originating in user code**

*Using skipLibCheck with tsgo fails to suppress TS2430 interface merging errors in user code.*

 * created by **jfirebaugh**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3814#issuecomment-4433187187) **RyanCavanaugh** said "This seems like a bug in 6.0 more than anything. It's super weird that you could put an invalid declaration in user code and not get an error just because skipLibCheck is on."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3814#issuecomment-4433206174) **jakebailey** said "This is definitely an intentional change, because we issue the errors on whichever thing we see first and therefore this is not deterministic, so we issue it everywhere"
 * **RyanCavanaugh** added label `wontfix`

### [Issue microsoft/TypeScript-go#3815](https://github.com/microsoft/TypeScript-go/issues/3815) (Closed, `wontfix`)

**\`skipLibCheck\` does not suppress TS2320 when module augmentation in \`\.ts\` triggers interface merging conflict from \`\.d\.ts\`**

*skipLibCheck doesn't suppress TS2320 error caused by module augmentation in .ts exposing conflicting check signatures from .d.ts*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433258910) **jakebailey** said "Is it just the = any?"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433834754) **jfirebaugh** said "It repros without = any."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4456030799) **Okanlawon2259** said "It's just any seem others are perfect "
 * **RyanCavanaugh** added label `wontfix`

### [PR microsoft/TypeScript-go#3821](https://github.com/microsoft/TypeScript-go/pull/3821) (Closed)

**Adding signature help tooltip coloring support for VS**

*Enable colored signature help tooltips in Visual Studio’s Corsa LSP by adding a displayPartsWriter to produce Roslyn classifications.*

 * created by **navya9singh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3821#issuecomment-4462157739) **jakebailey** said "I think we should try to test this, but otherwise LGTM"
 * (today) **navya9singh** closed the issue

### [PR microsoft/TypeScript-go#3836](https://github.com/microsoft/TypeScript-go/pull/3836) (Closed)

**fix\(workspace/symbol\): use name span in ProvideWorkspaceSymbols**

*ProvideWorkspaceSymbols now uses the identifier name span rather than the full declaration span to fix VS selection*

 * created by **joj**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3836#issuecomment-4445955151) **andrewbranch** described that the PR makes workspace symbols align with document symbols by including the name range so the cursor snaps to the name
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3836#issuecomment-4452730448) **jakebailey** said "You modified generated tests which isn't allowed; the top of the generated tests says how to manually modify them."
 * (today) **joj** closed the issue

### [PR microsoft/TypeScript-go#3837](https://github.com/microsoft/TypeScript-go/pull/3837) (Closed)

**Update snapshot and projects on file close**

*Update snapshots and clear closed projects upon file close to promptly remove stale diagnostics*

 * created by **gabritto**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3837#issuecomment-4453306181) **andrewbranch** asked how tsconfig diagnostics work in relation to project closure behavior in Strada
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3837#issuecomment-4453590148) **gabritto** noted that Strada did not clean up config diagnostics when a project closed
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3845](https://github.com/microsoft/TypeScript-go/pull/3845) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic when auto\-importing relative \.css augmentation from ESM file**

*Auto-importing ESM .css module augmentations panicked due to unrecognized extension, fixed by leaving filenames unchanged.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3849](https://github.com/microsoft/TypeScript-go/pull/3849) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix panic in overlayfs when saving a file without an overlay**

*Update overlayfs to gracefully treat saves on files without overlays as disk changes instead of panicking and add a test.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3855](https://github.com/microsoft/TypeScript-go/pull/3855) (Closed, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Accept CJS \`module\.exports = {}\` baseline diffs**

*Relocate 15 CommonJS `module.exports = {}` baseline diffs from the triaged to accepted group and remove the original triaged entries following review.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **weswigham**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3856](https://github.com/microsoft/TypeScript-go/issues/3856) (Closed, **jakebailey**, **Copilot**)

**Infinite hang in tsgo for invalid UTF\-8 in /u or /v regex**

*tsgo hangs indefinitely when processing regex literals containing invalid UTF-8 sequences with the u or v flag*

 * created by **mariusschulz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3857](https://github.com/microsoft/TypeScript-go/pull/3857) (Closed, **jakebailey**, **Copilot**)

**Fix infinite hang in regex parser for invalid UTF\-8 with unicode flag**

*The regex parser hung on invalid UTF-8 input in unicode mode because it failed to advance past the invalid byte.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3858](https://github.com/microsoft/TypeScript-go/issues/3858) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panic: slice bounds out of range in sliceTupleType**

*tsgo panics with a slice bounds out of range error in sliceTupleType during type checking.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3859](https://github.com/microsoft/TypeScript-go/pull/3859) (Open, **RyanCavanaugh**, **Copilot**)

**Fix panic when passing \`@\` response file argument to CLI**

*Normalize response file paths before reading to avoid tsgo panics when using '@' or relative '@filename' arguments.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3859#issuecomment-4462641033) **RyanCavanaugh** said "@copilot address CR comments"

### [Issue microsoft/TypeScript-go#3860](https://github.com/microsoft/TypeScript-go/issues/3860) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panic: SIGSEGV when JSX\.LibraryManagedAttributes / JSX\.ElementType has unexpected type**

*tsgo panics with a SIGSEGV segmentation fault when encountering unexpected types for JSX.LibraryManagedAttributes or JSX.ElementType.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3861](https://github.com/microsoft/TypeScript-go/pull/3861) (Closed, **jakebailey**, **Copilot**)

**Fix SIGSEGV in instantiateAliasOrInterfaceWithDefaults for non\-interface JSX types**

*instantiateAliasOrInterfaceWithDefaults panics when JSX.LibraryManagedAttributes or ElementType are declared as enums due to unguarded interface access.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3862](https://github.com/microsoft/TypeScript-go/issues/3862) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo deadlocks on a tsconfig \`extends\` cycle**

*tsgo deadlocks when parsing tsconfig files with a circular extends reference*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3863](https://github.com/microsoft/TypeScript-go/issues/3863) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics on CLI \`\-\-typeRoots \<relative\>\` when typeRoots is consulted**

*tsgo panics when a relative path is passed to the --typeRoots CLI option because the virtual file system requires absolute paths*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3863#issuecomment-4461940252) **jakebailey** said "Probably missing a path resolve somewhere?"
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3864](https://github.com/microsoft/TypeScript-go/pull/3864) (Closed, **jakebailey**, **Copilot**)

**Fix deadlock on tsconfig \`extends\` cycle**

*Prevent deadlock from circular tsconfig extends by tracking canonical paths and bypassing the cache on detected cycles.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3865](https://github.com/microsoft/TypeScript-go/pull/3865) (Closed, **jakebailey**, **Copilot**)

**Fix panic in sliceTupleType when tuple is shorter than pattern**

*Added bounds checking in sliceTupleType to return an empty tuple rather than panic when slicing a smaller tuple*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3866](https://github.com/microsoft/TypeScript-go/pull/3866) (Closed, **jakebailey**, **Copilot**)

**Fix panic on CLI \`\-\-typeRoots\` with relative path**

*Normalize relative --typeRoots CLI option values by extending ConvertOptionToAbsolutePath to handle []any lists and prevent panic*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3867](https://github.com/microsoft/TypeScript-go/issues/3867) (Closed)

**TestPushDiagnostics/publishes\_global\_diagnostics\_after\_checking is racy**

*The TestPushDiagnostics test intermittently fails due to a race condition preventing global diagnostics from being published on tsconfig.json.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3868](https://github.com/microsoft/TypeScript-go/issues/3868) (Closed, **jakebailey**, **Copilot**)

**tsgo parser bug: \`using\` followed by a newline ignores \[no LineTerminator here\] grammar restriction**

*tsgo parser erroneously allows a newline after the 'using' keyword, violating grammar rules and generating incorrect JavaScript.*

 * created by **mariusschulz**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3869](https://github.com/microsoft/TypeScript-go/pull/3869) (Closed, **jakebailey**, **Copilot**)

**Fix \`using\` followed by newline ignoring \[no LineTerminator here\] grammar restriction**

*Adding parentheses to the parser condition fixes misparsing of using followed by newline into two expression statements instead of a declaration.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3870](https://github.com/microsoft/TypeScript-go/pull/3870) (Closed, **RyanCavanaugh**, **Copilot**)

**Report CommonJS top\-level \`Object\` value collisions in checker**

*Adds a TypeScript checker to report collisions when top-level value declarations are named Object in CommonJS modules*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3870#issuecomment-4462729155) **RyanCavanaugh** said "@copilot see Jake's comment"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3870#issuecomment-4462876367) **Copilot** addressed compiler coverage location in testdata compiler cases/baselines in commit 804cb7f6
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3871](https://github.com/microsoft/TypeScript-go/pull/3871) (Open, **sandersn**, **RyanCavanaugh**, **Copilot**)

**Use named\-function overload diagnostic for JSDoc \`@overload\` return\-type omissions**

*Change JSDoc @overload return-type omission diagnostics to report function names (TS7010) for named functions instead of generic TS7012 errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** assigned to **sandersn**

### [PR microsoft/TypeScript-go#3872](https://github.com/microsoft/TypeScript-go/pull/3872) (Open, **RyanCavanaugh**, **Copilot**)

**Reclassify \`nodeModulesAllowJsImportAssignment\` JS emit diffs as accepted baselines**

*Reclassify nodeModulesAllowJsImportAssignment JS emit diffs as accepted baselines reflecting export import changes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3873](https://github.com/microsoft/TypeScript-go/issues/3873) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal crash in \`\(\*Program\)\.SingleThreaded\` on snapshot update**

*The compiler’s Program.SingleThreaded method crashes fatally when updating project snapshots in the language server.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3874](https://github.com/microsoft/TypeScript-go/pull/3874) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer crash in Program\.SingleThreaded on snapshot update**

*Prevent nil pointer crash by adding nil checks in SingleThreaded and skipping CreateProgram when CommandLine is unset.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4462933487) **RyanCavanaugh** said "@copilot why didn't you follow the PR instructions here? https://github.com/microsoft/typescript-go/blob/main/.github/copilot-instructions.md#pr-template"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4463078701) **Copilot** updated the PR description to follow the template and noted that build, test, lint, and format checks passed
 * [today](https://github.com/microsoft/TypeScript-go/pull/3874#issuecomment-4463100044) **jakebailey** said "no it doesn't, not at all"

### [PR microsoft/TypeScript-go#3875](https://github.com/microsoft/TypeScript-go/pull/3875) (Closed)

**Fix global diag test flake**

*Stabilize the global diagnostic test by addressing and resolving intermittent flakiness.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3876](https://github.com/microsoft/TypeScript-go/issues/3876) (Closed, `bug`, `Domain: Editor`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Error when retrieving diagnostics**

*Retrieving diagnostics in the TypeScript language server fails due to an error parsing object literal expressions.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Domain: Editor`, `Crash`, `bug`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3877](https://github.com/microsoft/TypeScript-go/pull/3877) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix panic in getTsConfigObjectLiteralExpression for malformed tsconfig**

*getTsConfigObjectLiteralExpression now checks for object literals to avoid panicking on malformed tsconfig.json values, and a test case was added.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4464433812) **RyanCavanaugh** questioned the theory of the case, asserted that the testcase did not reproduce the problem, noted that tsgo already reported the correct TS5092 error, and mentioned that the call stack indicated a related diagnostic was being computed
 * [today](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4465771376) **DanielRosenwasser** said "@copilot fix it"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3877#issuecomment-4465830661) **Copilot** acknowledged that the original test didn’t exercise the diagnostic explanation code and updated the test to use an array-literal tsconfig to trigger the crash path

### [Issue microsoft/TypeScript-go#3878](https://github.com/microsoft/TypeScript-go/issues/3878) (Open, `bug`, `Crash`, **DanielRosenwasser**, **Copilot**)

**Crash via \`checkExternalEmitHelpers\`**

*TypeScript crashes in checkExternalEmitHelpers while resolving external helper modules during decorator processing.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3879](https://github.com/microsoft/TypeScript-go/pull/3879) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil dereference in resolveHelpersModule via checkExternalEmitHelpers**

*Prevent nil dereference in resolveHelpersModule by falling back to file.AsNode when checkExternalEmitHelpers runs without an import specifier.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3880](https://github.com/microsoft/TypeScript-go/pull/3880) (Open)

**Re\-add diagnostics consistency check**

*Re-add diagnostics consistency check after resolving emit errors and symbol lookup issues, dropping redundant diagnostics.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#3881](https://github.com/microsoft/TypeScript-go/pull/3881) (Open)

**Expose ImportAdder to IPC API**

*Expose ImportAdder via the IPC API to allow external processes to add imports programmatically.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3882](https://github.com/microsoft/TypeScript-go/pull/3882) (Open)

**feat: unused identifier**

*The implementation of the unused identifier codefix (and other individual codefixes) has not been ported.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#3883](https://github.com/microsoft/TypeScript-go/issues/3883) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when inferring \[\.\.\.rest, \.\.\.T\] from a tuple shorter than fixed\-arity constraint**

*tsgo panics from slice bounds error when inferring rest and generic types from too-short tuples*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3884](https://github.com/microsoft/TypeScript-go/issues/3884) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a JS class has @augments or @extends JSDoc and empty extends clause**

*tsgo panics when a JS class uses @augments or @extends JSDoc with an empty extends clause*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3885](https://github.com/microsoft/TypeScript-go/issues/3885) (Closed, `Crash`)

**tsgo panics when a get/set accessor with an illegal async modifier contains for\-await\-of**

*tsgo panics when checking a get/set accessor illegally declared async containing a for-await-of loop*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3886](https://github.com/microsoft/TypeScript-go/issues/3886) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo printer panics when emitting declarations for CommonJS files with numeric export names**

*tsgo printer panics when emitting declarations for CommonJS files with numeric export names*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3887](https://github.com/microsoft/TypeScript-go/issues/3887) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo printer panics during "JSX expressions must have one parent element" recovery**

*The tsgo printer panics during JSX recovery when encountering an unhandled binary expression in a JSX attribute.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3888](https://github.com/microsoft/TypeScript-go/issues/3888) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics with interface conversion error when a @this appears inside of a @typedef comment**

*Parsing a JSDoc typedef comment that contains a @this tag triggers an interface conversion panic in tsgo.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3889](https://github.com/microsoft/TypeScript-go/issues/3889) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a @callback / @overload @param has a qualified name**

*tsgo panics with an unhandled QualifiedName case when a @callback or @overload @param uses a qualified name*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3889#issuecomment-4467242662) **jakebailey** said "How are you finding all of these? Is this some specific codebase? Are you fuzzing?"

### [Issue microsoft/TypeScript-go#3890](https://github.com/microsoft/TypeScript-go/issues/3890) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a @this JSDoc tag is combined with a literal this parameter**

*tsgo panics with an index out of range error when encountering a JSDoc @this tag alongside a literal this parameter*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3891](https://github.com/microsoft/TypeScript-go/issues/3891) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when an anonymous class declaration has a member decorator when downleveling to ES2022**

*tsgo panics with a debug assertion failure when downleveling anonymous classes with member decorators to ES2022*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3892](https://github.com/microsoft/TypeScript-go/issues/3892) (Closed, **jakebailey**, **Copilot**)

**tsgo hangs on large template literal types with combinatorial explosion**

*tsgo hangs indefinitely when compiling large combinatorial template literal types that tsc rejects as too complex.*

 * created by **mariusschulz**

### [Issue microsoft/TypeScript-go#3893](https://github.com/microsoft/TypeScript-go/issues/3893) (Closed)

**tsgo emits broken JS when a \.tsx file's only JSX element is self\-closing**

*When transpiling a TSX file containing only a self-closing JSX element, tsgo omits the necessary jsx import, producing invalid JavaScript.*

 * created by **mariusschulz**

### [Issue microsoft/TypeScript-go#3894](https://github.com/microsoft/TypeScript-go/issues/3894) (Closed, **jakebailey**, **Copilot**)

**tsgo JSX entity decoder skips entities that follow a non\-entity ampersand**

*tsgo’s JSX entity decoder fails to decode valid entities immediately following a standalone ampersand, resulting in literal entity strings in the output.*

 * created by **mariusschulz**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3894#issuecomment-4467303139) **jakebailey** said "Could be my code was wrong in https://github.com/microsoft/typescript-go/pull/2510"
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3895](https://github.com/microsoft/TypeScript-go/issues/3895) (Open, **jakebailey**, **Copilot**)

**tsgo's Uppercase/Lowercase intrinsic types don't apply Unicode special case mappings**

*tsgo's Uppercase and Lowercase intrinsic types omit Unicode special case mappings, causing incorrect type errors for characters like ß.*

 * created by **mariusschulz**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3895#issuecomment-4467314515) **jakebailey** said "This is effectively https://github.com/microsoft/typescript-go/issues/3489"

### [Issue microsoft/TypeScript-go#3896](https://github.com/microsoft/TypeScript-go/issues/3896) (Open, **jakebailey**, **Copilot**)

**tsgo emits \-NaN for enum members with NaN value in declaration output**

*tsgo outputs -NaN instead of normalizing NaN values when emitting enum member declarations initialized with -NaN.*

 * created by **mariusschulz**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3896#issuecomment-4467305977) **jakebailey** said "I'm not sure this is really a bug, but rather an improvement in node reuse"

### [PR microsoft/TypeScript-go#3897](https://github.com/microsoft/TypeScript-go/pull/3897) (Closed, **jakebailey**, **Copilot**)

**Fix JSX entity decoder skipping entities after non\-entity ampersand**

*Update JSX entity decoder to skip intervening non-entity ampersands and correctly decode entities.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3898](https://github.com/microsoft/TypeScript-go/issues/3898) (Closed, **jakebailey**, **Copilot**)

**tsgo creates a distinct enum literal type for each NaN\-valued enum member**

*tsgo treats NaN-valued enum members as distinct literal types, causing assignment errors between them*

 * created by **mariusschulz**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3898#issuecomment-4467309242) **jakebailey** said "That or NaN is not NaN and is being keyed somewhere (Go maps hash every NaN as new items)"

### [Issue microsoft/TypeScript-go#3899](https://github.com/microsoft/TypeScript-go/issues/3899) (Open, **jakebailey**, **Copilot**)

**tsgo breaks type soundness for lone\-surrogate string literals**

*tsgo improperly accepts assignments between different lone-surrogate string literals, breaking TypeScript’s type soundness.*

 * created by **mariusschulz**

### [Issue microsoft/TypeScript-go#3900](https://github.com/microsoft/TypeScript-go/issues/3900) (Open, `Crash`, **jakebailey**, **Copilot**)

**tsgo source\-map emit panics for an unclosed block**

*Emitting source maps in tsgo causes a slice bounds panic when encountering an unclosed code block.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3901](https://github.com/microsoft/TypeScript-go/issues/3901) (Closed, `Crash`)

**tsgo panics when emitting a \`do\` statement with no \`while\`**

*tsgo panics with slice bounds out of range when printing a do statement missing its while clause*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3902](https://github.com/microsoft/TypeScript-go/issues/3902) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics for a contextually typed function with optional and rest params**

*tsgo panics with a makeslice: len out of range error when type-checking a function using optional and rest parameters*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3903](https://github.com/microsoft/TypeScript-go/issues/3903) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics for rest properties in catch binding when targeting ES2017**

*tsgo crashes when transforming object rest properties in catch bindings targeting ES2017 because of an AST conversion error.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3904](https://github.com/microsoft/TypeScript-go/issues/3904) (Closed, `Crash`, **jakebailey**, **Copilot**)

**tsgo panics when a type\-only export is the body of an if statement**

*tsgo crashes with a nil pointer dereference when an if statement’s body is a type-only export.*

 * created by **mariusschulz**
 * **mariusschulz** added label `Crash`

### [Issue microsoft/TypeScript-go#3905](https://github.com/microsoft/TypeScript-go/issues/3905) (Closed, `Crash`)

**tsgo panics when destructuring pattern has no leaf pattern and targeting ES2017**

*tsgo panics with index-out-of-range error when destructuring pattern has no leaf on ES2017 target*

 * created by **mariusschulz**

