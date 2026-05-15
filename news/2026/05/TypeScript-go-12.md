# Report for 2026-05-12 (Tuesday, May 12th, 2026)

13 different users commented on 42 different issues.

## Recommended Actions

 * Response Recommended
    * @jfirebaugh provided repro details clarifying that the issue reproduces without `= any` in [microsoft/TypeScript-go#3815](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433834754)
    * @hkleungai asked whether TS8022 is marked as `wontfix` in [microsoft/TypeScript-go#3829](https://github.com/microsoft/TypeScript-go/issues/3829#issuecomment-4440059685)

## Activity Summary

### [Issue microsoft/TypeScript-go#2857](https://github.com/microsoft/TypeScript-go/issues/2857) (Closed, `Domain: Editor`, `Needs Investigation`, **andrewbranch**)

**Formatters get stuck**

*The extension’s LSP-based formatter intermittently hangs during format-on-save on MacOS, never returning a response.*

 * **DanielRosenwasser** assigned to **andrewbranch**
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4138974027) **DanielRosenwasser** said "I haven't seen this in a while - maybe with assertions on we'll uncover more of these."
 * **andrewbranch** added label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2857#issuecomment-4433419691) **mjbvz** said "Also haven't seen this recently. I think the root cause may be a misbehaving debugger extension maxing out ext host cpu so that TS's commands never got processed "
 * (today) **mjbvz** closed the issue

### [Issue microsoft/TypeScript-go#3480](https://github.com/microsoft/TypeScript-go/issues/3480) (Closed, `Needs Investigation`, **weswigham**)

**Missing error about jsx\-runtime package**

*Error messages for missing jsx-runtime package are not reported in legacy module detection tests for react-jsx and react-jsxdev*

 * (6 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3480#issuecomment-4425328982) **weswigham** identified that the jsx import path was not calculable in non-module files, proposed always attempting to add an import in resolveImportsAndModuleAugmentations, and said they would provide a fix after verification
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3484](https://github.com/microsoft/TypeScript-go/issues/3484) (Closed, `bug`, **iisaduan**)

**Static property conflicts with built\-in Function properties \(TS2699\) no longer reported when useDefineForClassFields is false**

*TypeScript does not report TS2699 errors for static class properties conflicting with built-in Function properties when useDefineForClassFields is false.*

 * (6 days ago) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#3545](https://github.com/microsoft/TypeScript-go/issues/3545) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: CJS export alias and element access patterns changed**

*Declaration output now differs for CommonJS export aliases and module.exports element access patterns, including duplicate assignments.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3545#issuecomment-4408235998) **RyanCavanaugh** said "@copilot make a PR to accept these baselines (add to submoduleAccepted.txt with a brief summary of the above comment)"
 * (4 days ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3551](https://github.com/microsoft/TypeScript-go/issues/3551) (Closed, `bug`, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**)

**Baselines: Output file ordering changed \+ declaration types resolve to any instead of typeof references**

*Declaration emit with package exports tests now reorder output file sections and produce declaration types as any rather than typeof references*

 * **RyanCavanaugh** assigned to **weswigham**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3551#issuecomment-4400735718) **weswigham** highlighted that file reordering was unimportant but the ': any' on package self-name import references was important, asked whether another issue existed for messed-up self-name refs, and noted that this issue required investigation as it indicated a checking pipeline problem
 * **weswigham** added label `bug`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3551#issuecomment-4434528305) **weswigham** explained that the issue was caused by Strada ignoring the outDir option and stated plans to fix the test and accept submodule diffs
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3559](https://github.com/microsoft/TypeScript-go/issues/3559) (Closed, `Domain: Declaration Emit`, `Needs Investigation`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Baselines: CJS exports pattern changes in declaration emit**

*CommonJS declaration emit restructuring changed baselines, causing some files to lose exports entirely.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3559#issuecomment-4408871073) **weswigham** explained that this was an intentional change and that a new declaration emit error for nested CommonJS export constructs exists, noting that the first example test didn't show it due to ts-nocheck
 * (4 days ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621) (Closed, `Crash`, `Needs More Info`)

**Panic Alert Notification when Cursor edits some file and opening that file causes panic\.**

*Opening or editing a file causes a panic in the semanticTokens request because a token improperly spans multiple lines.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4369143872) **CarlosZiegler** said "Observing same issue in cursor too. "
 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4373908974) **RyanCavanaugh** suggested opening in VS Code with the TypeScript Native Preview to verify whether the issue persisted and asked for a minimal LSP trace to reproduce the crash
 * [later](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4440078505) **Swiftwork** said "I believe that Cursor uses OpenVSX which has an out of date native preview. So you probably need to manually update it to the latest version."

### [PR microsoft/TypeScript-go#3781](https://github.com/microsoft/TypeScript-go/pull/3781) (Closed, **RyanCavanaugh**, **Copilot**)

**Accept CJS exports pattern baseline diffs**

*Accepted and relocated CommonJS export pattern baseline diffs to reflect new nested export declaration errors.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4424382001) **RyanCavanaugh** said "@copilot resolve the merge conflict"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4424518855) **Copilot** resolved the merge conflict in submoduleAccepted.txt by keeping both the late-bound entries from main and the CJS exports entries
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4425800473) **jakebailey** said "And then we immediately caused another one"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4433075606) **RyanCavanaugh** said "@copilot resolve the merge conflict"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4433149804) **Copilot** resolved the merge conflict by keeping both sets of tslib helper entries from #3777
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3782](https://github.com/microsoft/TypeScript-go/issues/3782) (Closed)

**\[ServerErrors\]\[JavaScript\] main vs **

*A main-branch pipeline run analyzing 300 popular TypeScript repositories encountered 15 interesting changes, 28 timeouts, one clone failure, and 18 unknown failures out of 253 successful analyses.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162371) **typescript-bot** reported a premature server connection closure error and provided repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162410) **typescript-bot** reported a server connection closed prematurely error and provided related logs, affected repo, old server result, and last requests
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3782#issuecomment-4410162452) **typescript-bot** reported a panic handling textDocument/diagnostic due to an unhandled case in Node.Initializer
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3784](https://github.com/microsoft/TypeScript-go/issues/3784) (Closed)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch error-delta pipeline encountered server errors, timeouts, and failures while analyzing 300 repositories and detected 20 changes.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588530) **typescript-bot** reported server connection closed prematurely error for babel/babel and provided logs and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588561) **typescript-bot** reported a server connection closed prematurely: undefined for the socketio/socket.io repo and provided last requests and repro steps
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3784#issuecomment-4410588597) **typescript-bot** reported server connection closed prematurely for the n8n-io/n8n CI run
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3787](https://github.com/microsoft/TypeScript-go/issues/3787) (Open, `Needs More Info`)

**tsgo and tsc diverge on incomplete composite\-ref declaration cache: TS2305 vs filterable TS6305**

*tsgo reports TS2305 errors instead of TS6305 missing-declaration errors when the composite declaration cache is incomplete.*

 * created by **XavierGeerinck**
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript-go#3799](https://github.com/microsoft/TypeScript-go/issues/3799) (Closed, `bug`, `Domain: Editor`, `Crash`, **RyanCavanaugh**, **gabritto**, **Copilot**)

**Debug assertion violation for document highlights on \`export =\` in merged namespace**

*Requesting document highlights for an `export =` inside a merged namespace triggers an internal debug assertion failure.*

 * (yesterday) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, `Crash`
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **gabritto**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#3801](https://github.com/microsoft/TypeScript-go/issues/3801) (Open, `bug`, `Domain: Editor`, `Crash`, **RyanCavanaugh**, **gabritto**, **Copilot**)

**Unhandled case when auto\-completing decorator on private method under \-\-experimentalDecorators**

*Autocompleting a decorator on a private class method with experimentalDecorators enabled causes a panic due to an unhandled case in getClassElementPropertyKeyType.*

 * (yesterday) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, `Crash`
 * (today) **RyanCavanaugh** assigned to **gabritto**, **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3803](https://github.com/microsoft/TypeScript-go/pull/3803) (Closed)

**Always generate a jsx implicit import specifier for tsx/jsx files**

*Always generate JSX runtime implicit import specifiers in JSX/TSX files regardless of module status to match Strada*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3804](https://github.com/microsoft/TypeScript-go/pull/3804) (Closed)

**add static property duplicate name check **

*Implement static property duplicate name check to prevent conflicts in property definitions.*

 * created by **iisaduan**
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#3805](https://github.com/microsoft/TypeScript-go/issues/3805) (Closed, `Crash`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Panic if there's a circular reference after \`satisfies\`**

*The TypeScript-Go compiler crashes with a stack overflow when resolving a circular type reference after using the satisfies operator.*

 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3805#issuecomment-4430105271) **ahejlsberg** expressed concern about circularity in error reporting and suggested having TypeToString return '?' on recursive invocation to avoid stack overflows
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript-go#3809](https://github.com/microsoft/TypeScript-go/issues/3809) (Closed, `bug`)

**Enum member after \`NaN\` must have initializer in tsgo, which is not in ts6\.0**

*tsgo incorrectly enforces explicit initializers for enum members after a NaN-valued member, unlike TypeScript 6.0.*

 * created by **Withered-Flower-0422**
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#3811](https://github.com/microsoft/TypeScript-go/issues/3811) (Closed, **jakebailey**, **Copilot**)

**\`\.d\.ts\.map\` includes \`sourcesContent\` when \`inlineSources\` is enabled**

*tsgo emits declaration map files containing sourcesContent when inlineSources is enabled, unlike TypeScript which omits them.*

 * created by **jfirebaugh**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3812](https://github.com/microsoft/TypeScript-go/pull/3812) (Closed, **jakebailey**, **Copilot**)

**Align declaration emit printer options with strada**

*Synchronize declaration emit printer options with strada's implementation and add a test for inlineSources in declaration maps.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3812#issuecomment-4433277646) **jakebailey** said "@weswigham Surprised we didn't include maps on d.ts files but it does seem that we didn't before."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3813](https://github.com/microsoft/TypeScript-go/issues/3813) (Closed, `wontfix`)

**TS2300 on duplicate computed property in type literal, tsc accepts it**

*tsc accepts duplicate computed properties in type literals whereas tsgo incorrectly emits TS2300 errors.*

 * created by **jfirebaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3813#issuecomment-4434261215) **ahejlsberg** said "This is an intended change and effectively a bug in TS6. The declaration contains a duplicate member and we want to report that."
 * **ahejlsberg** added label `wontfix`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3814](https://github.com/microsoft/TypeScript-go/issues/3814) (Open)

**\`skipLibCheck\` does not suppress TS2430 for interface merging errors originating in user code**

*Using skipLibCheck with tsgo fails to suppress TS2430 interface merging errors in user code.*

 * created by **jfirebaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3814#issuecomment-4433187187) **RyanCavanaugh** said "This seems like a bug in 6.0 more than anything. It's super weird that you could put an invalid declaration in user code and not get an error just because skipLibCheck is on."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3814#issuecomment-4433206174) **jakebailey** said "This is definitely an intentional change, because we issue the errors on whichever thing we see first and therefore this is not deterministic, so we issue it everywhere"

### [Issue microsoft/TypeScript-go#3815](https://github.com/microsoft/TypeScript-go/issues/3815) (Open)

**\`skipLibCheck\` does not suppress TS2320 when module augmentation in \`\.ts\` triggers interface merging conflict from \`\.d\.ts\`**

*skipLibCheck doesn't suppress TS2320 error caused by module augmentation in .ts exposing conflicting check signatures from .d.ts*

 * created by **jfirebaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433253772) **jakebailey** said "We have to issue it this way due to the multi-checker constraint; before it was nondeterministic which location we reported this, so now we report this consistently no matter the ordering."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433258910) **jakebailey** said "Is it just the = any?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3815#issuecomment-4433834754) **jfirebaugh** said "It repros without = any."

### [PR microsoft/TypeScript-go#3816](https://github.com/microsoft/TypeScript-go/pull/3816) (Closed)

**Add local test launch to launch template**

*Add a built-in local test launch configuration to the launch template to prevent repeated manual copying.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#3817](https://github.com/microsoft/TypeScript-go/issues/3817) (Closed, `bug`, `Domain: Editor`, `Crash`)

**Diagnostics crash for decorated class with static get accessor**

*Decorated class with static getter accessor triggers a nil pointer panic in the TypeScript-Go LSP diagnostics*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, `Crash`

### [PR microsoft/TypeScript-go#3818](https://github.com/microsoft/TypeScript-go/pull/3818) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix debug assertion violation for document highlights on \`export =\` in merged namespace**

*Fix document highlights crash caused by debug assertion on export = inside class-namespace merge by skipping non-module declarations*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3819](https://github.com/microsoft/TypeScript-go/pull/3819) (Open, **RyanCavanaugh**, **Copilot**)

**Fix panic in getClassElementPropertyKeyType for private identifiers**

*Add KindPrivateIdentifier case to getClassElementPropertyKeyType to prevent panics when completing decorators on private class members.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#3820](https://github.com/microsoft/TypeScript-go/pull/3820) (Closed)

**Add fixed copy of self name declaration emit test, accept baselines otherwise**

*Add a fixed copy of the self-name declaration emit test and accept existing baselines.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3821](https://github.com/microsoft/TypeScript-go/pull/3821) (Open)

**Adding signature help tooltip coloring support for VS**

*Enable colored signature help tooltips in Visual Studio’s Corsa LSP by adding a displayPartsWriter to produce Roslyn classifications.*

 * created by **navya9singh**

### [PR microsoft/TypeScript-go#3822](https://github.com/microsoft/TypeScript-go/pull/3822) (Closed)

**Prefer identifiers over strings when transforming JS export assignments**

*Prefer identifiers over string literals for JavaScript export assignments and suppress errors on string names in declaration files.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3823](https://github.com/microsoft/TypeScript-go/pull/3823) (Closed)

**Don't recursively scan auto\-import packages for non\-main \.d\.ts files unless option is set**

*Default auto-import no longer recursively scans packages without exports for non-main .d.ts entrypoints, improving performance while allowing an opt-in setting.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3824](https://github.com/microsoft/TypeScript-go/pull/3824) (Closed)

**Collect telemetry on recovered notification panics and stderr on unrecovered panics**

*Add telemetry for notification-based recovered panics and capture the last 40 stderr lines on unrecovered panics.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4435808782) **jakebailey** said "I'm not sure we can send the stderr raw; is there specific text we think we are going to find that we can look for?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4435820500) **andrewbranch** said "That is not what @DanielRosenwasser told me in chat, unless I misunderstood"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4435875173) **DanielRosenwasser** said "If we can pretty confidently validate that we have a stack trace, we can do some client-side sanitization like we used to. We have some stuff on the endpoint to get rid of PII just in case."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4435891054) **andrewbranch** asked if they could collect everything between the displayed elements and what kind of client-side sanitization was desired

### [PR microsoft/TypeScript-go#3825](https://github.com/microsoft/TypeScript-go/pull/3825) (Closed)

**Avoid repeated realpath in vfsmatch**

*Improve vfsmatch performance by reusing parent directory realpaths and avoiding repeated EvalSymlink calls for non-symlinks.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3826](https://github.com/microsoft/TypeScript-go/pull/3826) (Open)

**Add version & a common session identifier to events from LS clients**

*Include version and common session ID in language server client events to improve version-specific error tracking and correlate diagnostics.*

 * created by **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-4442659320) **jakebailey** said "I don't think dotted names are legal names for end users of this?"

### [PR microsoft/TypeScript-go#3827](https://github.com/microsoft/TypeScript-go/pull/3827) (Closed)

**fix\(3817\): diagnostics crash for decorated class with static get accessor**

*TypeScript compiler diagnostics crash when a decorated class has a static get accessor.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#3828](https://github.com/microsoft/TypeScript-go/pull/3828) (Closed)

**fix\(3810\): handle deprecated tags in completions**

*Add support for properly handling deprecated tags in code completions*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript-go#3829](https://github.com/microsoft/TypeScript-go/issues/3829) (Open, `Needs Investigation`, **ahejlsberg**)

**Behavior difference: tsgo fails to report TS8022 as tsc does**

*tsgo does not emit TS8022 errors for JSDoc '@extends' on non-class declarations in JavaScript files, unlike tsc*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3829#issuecomment-4440059685) **hkleungai** mentioned that TS8022 appears to be a known issue and asked whether it is marked as `wontfix`

### [PR microsoft/TypeScript-go#3830](https://github.com/microsoft/TypeScript-go/pull/3830) (Closed)

**fix\(3809\): Enum member after NaN must have initializer in tsgo, which is not in ts6\.0**

*Enum members after NaN require initializers in tsgo but not in TypeScript 6.0.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#3831](https://github.com/microsoft/TypeScript-go/pull/3831) (Open)

**fix\(3829\): handle extends tag not attached to a class**

*Ensure extends tags that are not attached to any class declaration are properly handled.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#3832](https://github.com/microsoft/TypeScript-go/pull/3832) (Closed)

**Add recursion limiter for \`TypeToString\`**

*Limit TypeToString recursion to two levels by returning "?" and discarding diagnostics to prevent infinite recursion and stack overflows.*

 * created by **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4442288102) **weswigham** described that the node builder already included circularity breaks but that these were problematic and might lead to unstable output and suggested that visitAndTransformType was not bailing as expected

