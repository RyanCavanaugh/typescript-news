# Report for 2026-05-13 (Wednesday, May 13th, 2026)

12 different users commented on 35 different issues.

## Recommended Actions

 * Response Recommended
    * @antichris asked for a link to the new issue or PR tracking the resolution in [microsoft/TypeScript-go#2201](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-4445042494)
    * @xuanduc987 asked if the asset bundling constraint is documented in [microsoft/TypeScript-go#3840](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-4448612870)

## Activity Summary

### [Issue microsoft/TypeScript-go#2201](https://github.com/microsoft/TypeScript-go/issues/2201) (Closed, `Domain: Editor`, **Copilot**)

**Bad formatting of multiline ternary expression**

*Formatting multiline ternary expressions with tabs results in inconsistent mixing of tabs and spaces.*

 * (1 month ago) **DanielRosenwasser** closed the issue
 * (1 month ago) **DanielRosenwasser** added label `Domain: Editor`, and removed label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-4445042494) **antichris** asked where the resolution is tracked and requested a link to the new issue or PR
 * [today](https://github.com/microsoft/TypeScript-go/issues/2201#issuecomment-4445210196) **DanielRosenwasser** assumed a formatting/printing PR introduced the change, manually validated the examples, and asked if the issue persisted

### [Issue microsoft/TypeScript-go#3662](https://github.com/microsoft/TypeScript-go/issues/3662) (Closed, `bug`, **iisaduan**)

**Behavior difference: tsgo wrongly allows \`include\` to contain files that is not under \`rootDir\` from tsconfig**

*tsgo incorrectly permits including files outside the configured rootDir in tsconfig without reporting errors.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.0 RC`
 * (5 days ago) **iisaduan** added label `bug`, and removed label `Needs Investigation`
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#3753](https://github.com/microsoft/TypeScript-go/issues/3753) (Open, `bug`, **iisaduan**)

**Missing error for non\-existent root files**

*tsgo silently ignores missing root files specified in tsconfig.json instead of reporting an error.*

 * created by **DanielRosenwasser**
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3753#issuecomment-4401709100) **DanielRosenwasser** said "Found from https://github.com/microsoft/typescript-go/issues/3376"
 * **RyanCavanaugh** added label `bug`
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**

### [PR microsoft/TypeScript-go#3772](https://github.com/microsoft/TypeScript-go/pull/3772) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix panic on bare \`@\` CLI argument**

*tsgo now handles bare '@' CLI arguments without panicking by updating VFS ReadFile to fail non-absolute paths and adding tests.*

 * **Copilot** assigned to **RyanCavanaugh**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3772#issuecomment-4408616683) **RyanCavanaugh** said "@copilot listen to Jake"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3772#issuecomment-4408789264) **RyanCavanaugh** said "@copilot listen to Jake"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3783](https://github.com/microsoft/TypeScript-go/pull/3783) (Closed)

**check that files specified in tsconfig\.json "include" is located in "rootdir"**

*Validate that files listed in tsconfig.json include patterns are located within the configured rootDir.*

 * created by **iisaduan**
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#3793](https://github.com/microsoft/TypeScript-go/issues/3793) (Open, `possible improvement`)

**\[lsp\] make source action kinds more specific**

*Advertise more specific LSP code action kinds with .ts suffixes to enable TypeScript-specific on-save actions without affecting other servers.*

 * created by **rchl**
 * (today) **iisaduan** added label `possible improvement`, and set milestone to `Possible Improvement`

### [Issue microsoft/TypeScript-go#3795](https://github.com/microsoft/TypeScript-go/issues/3795) (Closed, `wontfix`)

**tsc & tsgo difference in project reference build order**

*tsgo’s build order compiles the service project before util’s declaration files are emitted, causing import errors on the first build.*

 * **RyanCavanaugh** added label `wontfix`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3795#issuecomment-4424580108) **RyanCavanaugh** said "We're supposed to have a check that detects this situation and warns you, but I think the nested tsconfig setup here defeats it"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3795#issuecomment-4427512523) **SPGoding** reported that the build passed after moving dependency project references from the parent-level tsconfig.json to the nested src-level tsconfig.json
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3799](https://github.com/microsoft/TypeScript-go/issues/3799) (Closed, `bug`, `Domain: Editor`, `Crash`, **RyanCavanaugh**, **gabritto**, **Copilot**)

**Debug assertion violation for document highlights on \`export =\` in merged namespace**

*Requesting document highlights for an `export =` inside a merged namespace triggers an internal debug assertion failure.*

 * (yesterday) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript-go#3805](https://github.com/microsoft/TypeScript-go/issues/3805) (Closed, `Crash`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Panic if there's a circular reference after \`satisfies\`**

*The TypeScript-Go compiler crashes with a stack overflow when resolving a circular type reference after using the satisfies operator.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3805#issuecomment-4430105271) **ahejlsberg** expressed concern about circularity in error reporting and suggested having TypeToString return '?' on recursive invocation to avoid stack overflows
 * (yesterday) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3807](https://github.com/microsoft/TypeScript-go/pull/3807) (Open, **jakebailey**, **Copilot**)

**Fix stack overflow on circular reference after \`satisfies\`**

*Pass checkMode to skip assignability checks in satisfies expressions during serialization to prevent circular stack overflow*

 * **Copilot** assigned to **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4427875598) **jakebailey** said "@copilot+claude-opus-4.6 is this a porting bug? If not why doesn't Strada hit this?"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4427900074) **Copilot** described the issue as a porting bug and explained why Strada didn’t hit it due to lacking the pseudochecker path, outlining the cyclic call sequence in the Go port
 * [today](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4444350161) **weswigham** explained that the issue arose from creating a fresh node builder on each invocation rather than caching it, compared it to strada's behavior, and suggested caching a single node builder for intra-checker usage

### [Issue microsoft/TypeScript-go#3809](https://github.com/microsoft/TypeScript-go/issues/3809) (Closed, `bug`)

**Enum member after \`NaN\` must have initializer in tsgo, which is not in ts6\.0**

*tsgo incorrectly enforces explicit initializers for enum members after a NaN-valued member, unlike TypeScript 6.0.*

 * created by **Withered-Flower-0422**
 * (yesterday) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3817](https://github.com/microsoft/TypeScript-go/issues/3817) (Closed, `bug`, `Domain: Editor`, `Crash`)

**Diagnostics crash for decorated class with static get accessor**

*Decorated class with static getter accessor triggers a nil pointer panic in the TypeScript-Go LSP diagnostics*

 * (yesterday) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, `Crash`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3818](https://github.com/microsoft/TypeScript-go/pull/3818) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix debug assertion violation for document highlights on \`export =\` in merged namespace**

*Fix document highlights crash caused by debug assertion on export = inside class-namespace merge by skipping non-module declarations*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3818#issuecomment-4445186426) **jakebailey** said "Strada had to have also crashed with this, right?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3818#issuecomment-4445221777) **DanielRosenwasser** confirmed that Strada crashed as well and provided the error output
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3823](https://github.com/microsoft/TypeScript-go/pull/3823) (Closed)

**Don't recursively scan auto\-import packages for non\-main \.d\.ts files unless option is set**

*Default auto-import no longer recursively scans packages without exports for non-main .d.ts entrypoints, improving performance while allowing an opt-in setting.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3824](https://github.com/microsoft/TypeScript-go/pull/3824) (Closed)

**Collect telemetry on recovered notification panics and stderr on unrecovered panics**

*Add telemetry for notification-based recovered panics and capture the last 40 stderr lines on unrecovered panics.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4435820500) **andrewbranch** said "That is not what @DanielRosenwasser told me in chat, unless I misunderstood"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4435875173) **DanielRosenwasser** said "If we can pretty confidently validate that we have a stack trace, we can do some client-side sanitization like we used to. We have some stuff on the endpoint to get rid of PII just in case."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4435891054) **andrewbranch** asked if they could collect everything between the displayed elements and what kind of client-side sanitization was desired
 * [today](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4445323312) **jakebailey** questioned what sanitization would be safe and what would happen to stderr output in case of crashes or OOMs
 * [today](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4445444969) **andrewbranch** described that a specific commit restricted processing to lines between `panic:` and `Server exited` and ported the server-side stack sanitization
 * [today](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4445819430) **jakebailey** said "right, but I'm more thinking about if there's a panic followed by more text that some other goroutine is logging, interleaved. Maybe it just works?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3824#issuecomment-4445903738) **andrewbranch** said "The sanitizer redacts lines that don't match a recognized pattern."

### [PR microsoft/TypeScript-go#3825](https://github.com/microsoft/TypeScript-go/pull/3825) (Closed)

**Avoid repeated realpath in vfsmatch**

*Improve vfsmatch performance by reusing parent directory realpaths and avoiding repeated EvalSymlink calls for non-symlinks.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3826](https://github.com/microsoft/TypeScript-go/pull/3826) (Open)

**Add version & a common session identifier to events from LS clients**

*Include version and common session ID in language server client events to improve version-specific error tracking and correlate diagnostics.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-4442659320) **jakebailey** said "I don't think dotted names are legal names for end users of this?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3826#issuecomment-4444367810) **DanielRosenwasser** noted no indication that dotted names are illegal for end users and acknowledged possible error

### [PR microsoft/TypeScript-go#3827](https://github.com/microsoft/TypeScript-go/pull/3827) (Closed)

**fix\(3817\): diagnostics crash for decorated class with static get accessor**

*TypeScript compiler diagnostics crash when a decorated class has a static get accessor.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3827#issuecomment-4444706016) **DanielRosenwasser** said "Thanks!"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3828](https://github.com/microsoft/TypeScript-go/pull/3828) (Closed)

**fix\(3810\): handle deprecated tags in completions**

*Add support for properly handling deprecated tags in code completions*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3828#issuecomment-4444720376) **DanielRosenwasser** said "Is there some non-converted test that this should fix?"

### [PR microsoft/TypeScript-go#3830](https://github.com/microsoft/TypeScript-go/pull/3830) (Closed)

**fix\(3809\): Enum member after NaN must have initializer in tsgo, which is not in ts6\.0**

*Enum members after NaN require initializers in tsgo but not in TypeScript 6.0.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3831](https://github.com/microsoft/TypeScript-go/pull/3831) (Open)

**fix\(3829\): handle extends tag not attached to a class**

*Ensure extends tags that are not attached to any class declaration are properly handled.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3831#issuecomment-4445053253) **ahejlsberg** suggested relocating JSDoc error issuance to the reparser due to shared host-identification logic and potential for similar checks

### [PR microsoft/TypeScript-go#3832](https://github.com/microsoft/TypeScript-go/pull/3832) (Closed)

**Add recursion limiter for \`TypeToString\`**

*Limit TypeToString recursion to two levels by returning "?" and discarding diagnostics to prevent infinite recursion and stack overflows.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4442288102) **weswigham** described that the node builder already included circularity breaks but that these were problematic and might lead to unstable output and suggested that visitAndTransformType was not bailing as expected
 * [today](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4443332499) **ahejlsberg** asked for better ideas for a general solution and proposed using a private typeToString with recursion count to handle circularities
 * [today](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4443930434) **weswigham** explained that the root cause was allocating a new NodeBuilder on every XToString invocation which defeated circularity guards and opened issue #3833 with a fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/3832#issuecomment-4445661370) **ahejlsberg** said "Closing in favor of #3833."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3833](https://github.com/microsoft/TypeScript-go/pull/3833) (Closed)

**Use one cached nodebuilder for potentially circular internal ops, just like strada**

*Reuse a single cached nodebuilder for internal operations to enable functional circularity and performance as in Strada.*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444354488) **jakebailey** questioned whether they had undone the change due to excessive memory retention
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444383285) **weswigham** said "The only long-term thing the node builder should retain is cached built nodes to avoid doing the work of transforming the same type multiple times. It's a classic memory vs speed tradeoff."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444419313) **ahejlsberg** said "@weswigham I'm not 100% understanding how this PR causes the other baseline changes where structural types change into type aliases. Would you mind explaining?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444468770) **weswigham** explained that cached types were being reused in the node builder from previous invocations, identified a bug in cache busting for the corsa environment, and stated intent to fix it
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444506012) **jakebailey** said "That feels really spooky..."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444515085) **weswigham** said "Transforming a type into a node given the same context and node builder flags should produce the same output every time - makes sense to cache it. 🤷‍♂️"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444544157) **ahejlsberg** asked why using cached types produced different output compared to no cache
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444563764) **weswigham** explained that the quickinfo request includes expandable hover configuration producing a different node than the cached result and suggested including hover context in the cache key
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4444607714) **weswigham** described skipping the cache for expandable hover quickinfo, similar to strada, and noted that further optimizations were likely unnecessary
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4445013970) **jakebailey** referred to #1289 which fixed #988 and cautioned that this PR would undo that fix and cause issues without #3435
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4445141138) **weswigham** asked why corsa holds onto more nodes than strada and whether the node builder's factory should avoid arena allocation
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4445307983) **ahejlsberg** noted that the underlying cause of issue #988 was likely different given the disappearance of deep type instantiation errors and many changes over the last 10 months
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4445451531) **weswigham** suggested using a specific commit to release arenas for garbage collection and requested a repeatable test case
 * [today](https://github.com/microsoft/TypeScript-go/pull/3833#issuecomment-4445491042) **jakebailey** said "I guess we'll find out..."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#3834](https://github.com/microsoft/TypeScript-go/pull/3834) (Open)

**add localization for extension**

*Add localization support to the TypeScript VS Code extension by integrating non-English translation files and enabling pseudo-language testing.*

 * created by **iisaduan**

### [PR microsoft/TypeScript-go#3835](https://github.com/microsoft/TypeScript-go/pull/3835) (Closed)

**Update README with current jsdoc/declarations status**

*Update the README’s JSDoc and type declarations status table with current completion details and encourage bug reports.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#3836](https://github.com/microsoft/TypeScript-go/pull/3836) (Closed)

**fix\(workspace/symbol\): use name span in ProvideWorkspaceSymbols**

*ProvideWorkspaceSymbols now uses the identifier name span rather than the full declaration span to fix VS selection*

 * created by **joj**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3836#issuecomment-4445955151) **andrewbranch** described that the PR makes workspace symbols align with document symbols by including the name range so the cursor snaps to the name

### [PR microsoft/TypeScript-go#3837](https://github.com/microsoft/TypeScript-go/pull/3837) (Open)

**Update snapshot and projects on file close**

*Update snapshots and clear closed projects upon file close to promptly remove stale diagnostics*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#3838](https://github.com/microsoft/TypeScript-go/pull/3838) (Closed)

**Speed up realpath on Linux and macOS**

*Opening files with O_PATH on Linux/macOS avoids EvalSymlinks and reduces realpath latency and memory allocations by over 50%.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3839](https://github.com/microsoft/TypeScript-go/pull/3839) (Closed)

**Don't double count approximateLength during tryReuseExistingNodeHelper**

*Resolve TS7056 error by avoiding double counting of approximateLength in tryReuseExistingNodeHelper*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3839#issuecomment-4447301257) **jakebailey** described the TypeScript call chain traversal and explained how reuse of type nodes failed due to fresh type object identity mismatches
 * [today](https://github.com/microsoft/TypeScript-go/pull/3839#issuecomment-4447560168) **jakebailey** demonstrated that using a recovery boundary to save and restore approximateLength corrected the double-counting issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3839#issuecomment-4448005111) **jakebailey** said "I have maybe a test, but it doesn't work because of the pre/post emit thing I think"

### [PR microsoft/TypeScript-go#3840](https://github.com/microsoft/TypeScript-go/pull/3840) (Open)

**Don't send bundled file watchers to client**

*Filter out bundled TypeScript library file patterns from LSP server watch requests to prevent invalid client watchers.*

 * created by **xuanduc987**
 * [later](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-4448489455) **jakebailey** asked whether there was a test demonstrating the issue and noted that running the server with bundled assets is not expected
 * [later](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-4448612870) **xuanduc987** asked if the asset bundling constraint was documented and offered to raise an issue in nixpkgs
 * [later](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-4448739859) **jakebailey** said "No, but it's just hereby build which does all the work to build it, and the herebyfile contains more info about how we build the releases"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3840#issuecomment-4448742318) **jakebailey** said "I don't think this PR is wrong, but we probably need a test that is conditional on whether or not embedding is enabled"

### [Issue microsoft/TypeScript-go#3841](https://github.com/microsoft/TypeScript-go/issues/3841) (Closed, `wontfix`)

**Behavior difference: tsgo prints namespace in TS2740 but tsc does not**

*tsgo prints namespace-qualified types (fake.Mock) in TS2740 errors, whereas tsc prints unqualified type names (Mock).*

 * created by **hkleungai**

### [Issue microsoft/TypeScript-go#3842](https://github.com/microsoft/TypeScript-go/issues/3842) (Open)

**Missing support for namespaces in JSDoc types**

*Reinstate nested JSDoc typedef namespace support in tsgo, as the .d.ts workaround breaks single-file typing workflows.*

 * created by **remcohaszing**

