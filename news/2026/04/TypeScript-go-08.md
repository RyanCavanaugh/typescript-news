# Report for 2026-04-08 (Wednesday, April 8th, 2026)

9 different users commented on 24 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#2272](https://github.com/microsoft/TypeScript-go/pull/2272) (Closed)

**Revamp user preferences serialization/deserialization**

*Refactor user preferences serialization to use struct tags and reflection enabling JSON round-trip and nested configurations.*

 * created by **jakebailey**
 * [17 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2272#issuecomment-3634599760) **jakebailey** said "I think I'm going to wait for the other two user pref related PRs to finish and just fix this PR instead of forcing that on everyone."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2272#issuecomment-4209839530) **jakebailey** said "Any opinions on whether or not the typescript/javascript fallback is preserved? Not hard to stick back in."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2272#issuecomment-4209879881) **jakebailey** said "I'm going to restore it, it wasn't really the main point of this change but something I did in the middle of the refactor."

### [PR microsoft/TypeScript-go#2966](https://github.com/microsoft/TypeScript-go/pull/2966) (Closed)

**Clamp received \`lsproto\.Position\`s**

*Clamp received lsproto.Position values to valid line and character boundaries.*

 * created by **Andarist**
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2966#issuecomment-3993975441) **DanielRosenwasser** noted that they plan to possibly implement this or silently error in the future but currently want to identify issues in request handling or the VS Code language server client
 * [later](https://github.com/microsoft/TypeScript-go/pull/2966#issuecomment-4212534855) **Andarist** said "superseded by https://github.com/microsoft/typescript-go/pull/3365"
 * (later) **Andarist** closed the issue

### [Issue microsoft/TypeScript-go#3139](https://github.com/microsoft/TypeScript-go/issues/3139) (Open, `Needs More Info`)

**runtime: failed to create new OS thread**

*Running tsgo on a large macFUSE-mounted TypeScript project exhausts OS threads and crashes the Go runtime.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4170466384) **vetptzru** dug into the codebase and identified that the file parser spawns unbounded goroutines which block on readSema, causing OS thread exhaustion on slow filesystems, and suggested using a pre-spawn semaphore approach
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4170683318) **jakebailey** questioned how the cause was determined and challenged the explanation of the Go scheduler
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4206708107) **vetptzru** admitted that readSema did not hold an OS thread, proposed that unbounded module resolution goroutines making FileExists/DirectoryExists syscalls could exhaust threads on slow filesystems, and requested correction if mistaken
 * [today](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4209932096) **jakebailey** proposed testing pull request 3369 to address potential thread limit issues due to blocking syscalls on macFUSE
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4215019134) **vetptzru** reported that the fix resolved crashes and reduced the macFUSE thread count to under 26
 * [later](https://github.com/microsoft/TypeScript-go/issues/3139#issuecomment-4215101482) **jakebailey** said "I'm not sure if that's going to be the fix, as it very much hurts everyone else's perf."

### [PR microsoft/TypeScript-go#3217](https://github.com/microsoft/TypeScript-go/pull/3217) (Closed)

**Watch cli efficiency update**

*Watch CLI efficiency improvements implement debouncing, configuration caching, and dependency parsing to avoid unnecessary recompilations.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4143654633) **andrewbranch** expressed that the commit wasn’t sufficient for wildcard watching, asked what “incremental skips emit for new unreferenced file” means, and suggested reading the directory recursively to detect new files
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4185460956) **andrewbranch** used Copilot to generate tests and discovered multiple race conditions in vfswatch and watcher, linking a commit with detailed results
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4194915866) **johnfav03** thanked for the race tests and added mutexes to the Watcher and FileWatcher structs to fix race conditions and confirmed no race warnings with Copilot tests
 * [today](https://github.com/microsoft/TypeScript-go/pull/3217#issuecomment-4208738400) **jakebailey** suggested not blocking the PR on LSP support, recommended using dotnet's built-in watcher for manual watch requests, and asked @joj and @navya9singh about feasibility

### [PR microsoft/TypeScript-go#3257](https://github.com/microsoft/TypeScript-go/pull/3257) (Closed)

**Add perf / project telemetry**

*Add togglable events for project metadata and periodic performance telemetry, including file counts, compiler options, memory usage, and GC metrics.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3349](https://github.com/microsoft/TypeScript-go/pull/3349) (Closed)

**Add Go to Source Definition**

*Add Go to Source Definition feature using a no-dts resolver with client-side commands, server-side toggles, and tests*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3357](https://github.com/microsoft/TypeScript-go/issues/3357) (Open, `Crash`, **DanielRosenwasser**, **weswigham**, **Copilot**)

**Nil pointer derefence in \`\(\*NodeBuilderImpl\)\.addPropertyToElementList\` with  \`\-\-tsBuildInfoFile\`**

*A nil pointer dereference occurs in NodeBuilderImpl.addPropertyToElementList when running with the --tsBuildInfoFile option.*

 * **LukeAbby** added label `Crash`
 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **weswigham**

### [PR microsoft/TypeScript-go#3361](https://github.com/microsoft/TypeScript-go/pull/3361) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in addPropertyToElementList**

*Add nil guard for propertySymbol.Parent in addPropertyToElementList to avoid crashes with synthetic union/intersection properties*

 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3361#issuecomment-4202878806) **DanielRosenwasser** said "@copilot go."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3361#issuecomment-4208150468) **DanielRosenwasser** said "@copilot?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3361#issuecomment-4208303140) **Copilot** explained how the previous test didn't crash, described a new mixin-based test that triggered the crash, and confirmed its failure without the fix and success with it
 * [today](https://github.com/microsoft/TypeScript-go/pull/3361#issuecomment-4208959118) **Copilot** added a test file with --incremental and --tsBuildInfoFile directives confirming the crash in the incremental compilation path

### [PR microsoft/TypeScript-go#3362](https://github.com/microsoft/TypeScript-go/pull/3362) (Open)

**Replace most ID usage with pointers**

*Propose replacing most ID fields with pointers in Go to leverage pointer comparability and reduce overhead.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4208295994) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4208296421) **typescript-bot** reported starting jobs and provided build status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4208449180) **typescript-bot** provided the performance run results for the requested baseline vs pr comparison

### [PR microsoft/TypeScript-go#3363](https://github.com/microsoft/TypeScript-go/pull/3363) (Open)

**Make LS checkers time out after being idle, segment based on use**

*Implement ephemeral, configurable diagnostic and query checkers that automatically time out and use channel-based synchronization.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#3364](https://github.com/microsoft/TypeScript-go/issues/3364) (Open, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**No project found for untitled file**

*VS Code LSP reports a no project found for URI untitled:Untitled-1 error when opening an anonymous unsaved file*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#3365](https://github.com/microsoft/TypeScript-go/pull/3365) (Closed)

**Clamp LSP position conversions**

*Clamp LSP position conversions to handle out-of-range client requests without masking unicode bugs.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3365#issuecomment-4209051843) **jakebailey** said "Uh oh, that test failure is fun, I swear I ran tests locally before!"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3365#issuecomment-4212545107) **Andarist** said "I had a similar one here: https://github.com/microsoft/typescript-go/pull/2966 - maybe you could recycle some of its tests or something"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3365#issuecomment-4215459134) **jakebailey** said "Ah, yeah... I truthfully forgot"

### [PR microsoft/TypeScript-go#3366](https://github.com/microsoft/TypeScript-go/pull/3366) (Closed, **DanielRosenwasser**, **Copilot**)

**Handle 'no project found' gracefully for untitled files**

*Convert missing project errors for untitled LSP files into null responses instead of error notifications*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3366#issuecomment-4209741255) **DanielRosenwasser** said "@andrewbranch @jakebailey is this remotely correct? Feels like it's not."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3366#issuecomment-4209761712) **jakebailey** questioned why the client was performing operations on an in-memory file despite no underlying file

### [PR microsoft/TypeScript-go#3367](https://github.com/microsoft/TypeScript-go/pull/3367) (Closed)

**Codegen Go and TypeScript SyntaxKinds, ASTs, factories, visitors, type guards, encoders, decoders**

*Implement various updates to Go and TypeScript AST code generation, including SyntaxKind renames, factory adjustments, and structural enhancements.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#3368](https://github.com/microsoft/TypeScript-go/pull/3368) (Closed)

**Add go\-osstat to NOTICE\.txt**

*Add the go-osstat dependency to the project's NOTICE.txt file to ensure proper licensing attribution.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Open)

**Limit loader/emitter to GOMAXPROCS**

*Limit loader and emitter concurrency to GOMAXPROCS to reduce overhead from excessive parallelism*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4209932906) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4209933293) **typescript-bot** notified that perf test jobs started and provided result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4210064624) **typescript-bot** posted the requested performance run results comparing baseline and PR metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4210075226) **jakebailey** expressed suspicion and requested perf testing by @typescript-bot
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4210075529) **typescript-bot** reported that perf test jobs started and provided links to the build and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4210183826) **typescript-bot** posted the requested performance run results

### [Issue microsoft/TypeScript-go#3370](https://github.com/microsoft/TypeScript-go/issues/3370) (Open, `duplicate`)

**Bad inference for param of type T\[\] \| T\[\]\[\]**

*tsgo misinfers the generic type as an extra array level when narrowing T[] | T[][]*

 * created by **jsnajdr**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3370#issuecomment-4213268869) **JoostK** said "Sounds like https://github.com/microsoft/typescript-go/issues/1789"

