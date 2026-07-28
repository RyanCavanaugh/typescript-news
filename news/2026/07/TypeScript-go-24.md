# Report for 2026-07-24 (Friday, July 24th, 2026)

20 different users commented on 28 different issues.

## Recommended Actions

 * Response Recommended
    * @DanielCordell asked if this is still being looked at in [microsoft/TypeScript-go#2282](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-5072328233)
    * @swotvibe asked whether the issue was open and requested feedback on a caching optimization in [microsoft/TypeScript-go#4610](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5077957506)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072314381)
    * @jasonlyu123 asked questions about content mapper feature disablement, IPC API sourcemapping, and a source file parsing API in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5076787506)
    * @thunder-coding asked if adding Android arm64 support without cgo now would be acceptable in [microsoft/TypeScript-go#4729](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5072859877)
    * @typescript-automation[bot] provided requested performance run results in [microsoft/TypeScript-go#4731](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5072854407)
    * @robertkirkman asked if there was a way to download the GitHub Actions CI artifact from the PR in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5075800807)
    * @robertkirkman asked if they could test the changes in [microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5075861964)
    * @typescript-automation[bot] reported a panic in textDocument/formatting that should be investigated in [microsoft/TypeScript-go#4738](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535585)
    * @typescript-automation[bot] reported a CI error with server connection closure in [microsoft/TypeScript-go#4738](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535642)
    * @typescript-automation[bot reported server connection closed prematurely error for babel/babel in [microsoft/TypeScript-go#4738](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535700)
    * @typescript-automation[bot] reported a server connection error for nuxt/nuxt in [microsoft/TypeScript-go#4738](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535744)
    * @typescript-automation[bot] reported server connection closed prematurely error in [microsoft/TypeScript-go#4738](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535782)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4741](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5079144193)

## Activity Summary

### [Issue microsoft/TypeScript-go#2282](https://github.com/microsoft/TypeScript-go/issues/2282) (Open, `possible improvement`, **joj**)

**Request for official prebuilt Windows binaries \(tsgo\.exe\) published via GitHub Releases, without requiring npm\.**

*Officially distribute Windows tsgo.exe binaries via GitHub Releases to enable TypeScript use without npm.*

 * (17 weeks ago) **RyanCavanaugh** added label `possible improvement`, set milestone to `Possible Improvement`, and assigned to **joj**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2282#issuecomment-5072328233) **DanielCordell** said "Is this still something being looked at? Publishing a nuget package with this self-contained would be incredibly useful for environments where we can't use npm or node for one reason or another. @joj "

### [Issue microsoft/TypeScript-go#4017](https://github.com/microsoft/TypeScript-go/issues/4017) (Closed, `Domain: Editor`, `possible improvement`, **DanielRosenwasser**, **Copilot**)

**Extension does not respect \`js/ts\.locale\`**

*The extension ignores js/ts.locale settings and always displays English error messages because it does not send locale to the server.*

 * (1 week ago) **DanielRosenwasser** set milestone to `TypeScript 7.1`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4283](https://github.com/microsoft/TypeScript-go/pull/4283) (Closed)

**Optimize intersections / prop intersections further**

*Optimize intersection and property intersection computations further using insights from profiling data.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4283#issuecomment-4693462016) **typescript-automation[bot]** posted the requested perf run results with a detailed comparison report including metrics for errors, symbols, types, memory usage, and allocations
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4283#issuecomment-4693492104) **jakebailey** said "Uh oh"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4283#issuecomment-4693777408) **typescript-automation[bot]** reported that running the top 400 repos with tsc comparing main and refs/pull/4283/merge succeeded without issues
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4407](https://github.com/microsoft/TypeScript-go/pull/4407) (Open, **jakebailey**, **Copilot**)

**Restore tsgo noEmit exit status semantics**

*Restore tsgo’s noEmit exit status semantics by porting tsc’s handleNoEmitOptions logic to ensure exit code 2 for type errors*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-4782003646) **Copilot** identified the root cause as the EmitSkipped value, ported handleNoEmitOptions into Program.Emit, reverted the cmd/tsgo hack and its test, and added a tsc command-line test
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5063909048) **jakebailey** said "@copilot merge main and bring the baselines up to date"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5064115508) **Copilot** merged main and updated the stale baseline for tsc/projectReferences/when-project-references-have-invalid-fields
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5072701666) **andrewbranch** said "oh no more conflicts"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5072717269) **jakebailey** said "@copilot+gpt-5.6-sol Merge main and fix conflicts, again!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5073004746) **Copilot** merged main and resolved the emit API conflicts, preserved `ForceEmit` through incremental emit option wrapping, and validated all baselines, build, test, lint, and format checks

### [PR microsoft/TypeScript-go#4566](https://github.com/microsoft/TypeScript-go/pull/4566) (Closed)

**Use published packages for stable releases**

*Pull prebuilt npm packages in the release branch instead of rebuilding them to work around npm's platform limitations.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4610](https://github.com/microsoft/TypeScript-go/issues/4610) (Closed, `Domain: Editor`, `Needs Investigation`, **johnfav03**)

**Renaming a file can be very slow in some edge cases**

*VSCode tsgo file renames can be slow because a third-party .d.ts with repeated imports triggers quadratic path-updater scans.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **johnfav03**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4610#issuecomment-5077957506) **swotvibe** asked whether the issue was still open for someone else to pick up and whether memoizing computed import specifiers would resolve the repeated-computation performance issue

### [Issue microsoft/TypeScript-go#4633](https://github.com/microsoft/TypeScript-go/issues/4633) (Open, `Needs Investigation`, **jakebailey**)

**Publish an official wasip1 \(WASI\) build artifact of tsgo**

*Publish an official Go WASI (wasip1) WebAssembly build artifact of tsgo alongside native binaries in releases.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5047893676) **jakebailey** asked about the expectation for distributing a .wasm file on npm, noted that special-casing it is feasible as esbuild does, and suggested falling back to Node's WASI shim when no native binary exists despite observed crashes
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5048059112) **calvinrp** proposed publishing a versioned .wasm package per release and adding CI-built artifacts, and suggested decoupling the Node WASI-shim fallback as a separate issue
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5048946486) **calvinrp** followed up on the shim crash, explained that it was a Node bug fixed in Node 23+, confirmed that the fallback works under node >= 23, and reported that the LSP mode hang was a tsgo-side issue filed as #4706
 * [today](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5073585306) **jakebailey** said "One gotcha here; should that wasm bundle include all of our embedded artifacts? Or just use the same exe location stuff we currently do? I'm kinda unsure."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5074485044) **calvinrp** recommended embedding libraries in WASM builds to produce a self-contained file as the default GOOS=wasip1 build does
 * [today](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5074534872) **jakebailey** noted that editor use was useless because paths were exposed over the wire and pointed nowhere and error messages were misleading, and reported success providing `argv0` in some hosts but that not all hosts allow it
 * [today](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5074614041) **calvinrp** suggested embedding by default and adding a --lib-dir flag or environment variable for editor hosts
 * [today](https://github.com/microsoft/TypeScript-go/issues/4633#issuecomment-5074619906) **jakebailey** said "Not sure, I think it will also depend on what we do in the playground."

### [PR microsoft/TypeScript-go#4660](https://github.com/microsoft/TypeScript-go/pull/4660) (Closed, **DanielRosenwasser**, **Copilot**)

**Respect configured TypeScript diagnostic locale**

*Respect js/ts.locale and typescript.locale overrides for TypeScript diagnostics, restart the language server on changes, and fallback to auto display language.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5064034993) **Copilot** enumerated changes to support dynamic locale updates, including adding GetLocale to project.Client, implementing GetLocale on the Server, updating diagnostic publishing with locale context, and removing the extension restart handler
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5064105934) **jakebailey** criticized the proposed solution as incorrect and recommended implementing a UserPreference to read the locale with a Client callback for setting a new locale
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5064280433) **Copilot** stated that the initial approach was wrong and described the fix implemented in commit e83a1d7d
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4699](https://github.com/microsoft/TypeScript-go/pull/4699) (Closed)

**API emit**

*Add program.emit, program.emitToString, getJavaScriptEmit, and getDeclarationEmit methods for flexible file system and in-memory emissions.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5059826896) **andrewbranch** said "@pfumagalli yes, go ahead, thanks!"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5063044729) **andrewbranch** noted that source maps were already included in program.emit and program.emitToString outputs, added tests, and asked whether getters for source map emit and declaration source map emit should be added
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5063469921) **jakebailey** said "Would anyone ever want the source map for a file output they don't have? I assume not, so those two wouldn't be needed?"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4701](https://github.com/microsoft/TypeScript-go/pull/4701) (Open)

**\[api\] Add \`\.getNonMissingTypeOfSymbol\(\)\` getter**

*Add .getNonMissingTypeOfSymbol() API getter to retrieve a symbol’s non-missing type.*

 * created by **mrazauskas**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4701#issuecomment-5077494102) **mrazauskas** noted inconsistent usage of GetTypeOfSymbol methods between api/session and ls/api and asked if it was an oversight

### [PR microsoft/TypeScript-go#4703](https://github.com/microsoft/TypeScript-go/pull/4703) (Open)

**Store value symbol links inline on checker\-created symbols**

*Value symbol links for checker-created symbols are stored inline to eliminate paged store overhead and improve check performance.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5058461902) **typescript-automation[bot]** reported build jobs starting and provided status and results links
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5058758042) **typescript-automation[bot]** reported the performance run results as requested by jakebailey
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5059253316) **jakebailey** said "Seems like it's in the noise?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072017346) **mds-ant** rebased and reran the benchmark and reported that single-threaded improvements disappeared after merging #4329, but multi-threaded improvements remained
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072036757) **jakebailey** expressed expectation to see a result and requested the typescript-bot to run a perf test
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072037478) **typescript-automation[bot]** reported CI job start and result status with links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072314381) **typescript-automation[bot]** posted the performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4703#issuecomment-5072638607) **jakebailey** said "It does seem 3% faster on vscode, at least."

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Add support for external content mapper packages in TypeScript configuration to transform unsupported file types into valid TypeScript syntax.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5063344000) **mikearnaldi** mentioned working on a similar experiment, shared a link, and noted needing to enable semantic tokens
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5070266955) **mikearnaldi** provided a quick update on found issues and shared patch locations, noting that patch 0005 introduced a new API outside the PR scope
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5070774783) **revskill10** insulted VSCode as a piece of shit and demanded a fix
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5076787506) **jasonlyu123** asked whether the content mapper could specify which editor feature to disable, whether the IPC API would automatically sourcemap request and result positions and include validations, and whether a pure source file parsing API would be provided in the future, while describing Svelte’s current sourcemap and transformation approach
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5076803173) **andrewbranch** thanked the reviewer, explained that patch 0002 was incorrect, and illustrated the ambiguity in mapping end-of-span positions while suggesting left/right affinity context
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5076887616) **andrewbranch** provided an update before vacation and asked for feedback from implementers on the SpanMapPurpose classification
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5078512064) **mikearnaldi** explained that patch 0002 was incomplete, described mapping ambiguity at span boundaries requiring left/right affinity, and noted that his patch enabled completions at file end but might not be correct

### [PR microsoft/TypeScript-go#4724](https://github.com/microsoft/TypeScript-go/pull/4724) (Closed)

**\[api\] Add proper ParsedCommandLine type, provide APIs for getting config source files**

*Add a ParsedCommandLine property to projects and program APIs to list and retrieve configuration file names and AST source files.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#4727](https://github.com/microsoft/TypeScript-go/issues/4727) (Closed, `bug`, **ahejlsberg**)

**Panic in propertiesRelatedTo for recursive variadic tuple constraint**

*TypeScript-Go native-preview panics with an index out of range error in propertiesRelatedTo while inferring recursive variadic tuple types*

 * created by **HuzaifaAbdulRehman**
 * (today) **ahejlsberg** added label `bug`, set milestone to `Post-7.0`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4728](https://github.com/microsoft/TypeScript-go/pull/4728) (Closed)

**Fix variadic tuple relation position mapping**

*Fix tuple mapping logic to align fixed and variadic tuple sections correctly and prevent out-of-bounds indexing.*

 * created by **HuzaifaAbdulRehman**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4728#issuecomment-5069950942) **HuzaifaAbdulRehman** requested review of a checker fix addressing the panic in issue 4727 and adding regression coverage, and offered to address feedback
 * [today](https://github.com/microsoft/TypeScript-go/pull/4728#issuecomment-5072066821) **ahejlsberg** said "This isn't quite the right fix. I will put up a PR with what I think is the solution."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4728#issuecomment-5073648480) **HuzaifaAbdulRehman** said "Thanks for taking a look, @ahejlsberg. Understood — I'll hold off on further changes and study your PR when it's available so I can understand the intended solution."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4728#issuecomment-5074858466) **ahejlsberg** described that their PR #4735 conditionally applied end-of-tuple index mapping only when the tuple contains a rest element and added a bounds check for tuples with variadic elements but no rest element
 * [later](https://github.com/microsoft/TypeScript-go/pull/4728#issuecomment-5078775839) **HuzaifaAbdulRehman** thanked the reviewer, acknowledged the distinction between end-of-tuple mapping and variadic-only targets, and said they would close the PR now that #4735 has landed
 * (later) **HuzaifaAbdulRehman** closed the issue

### [PR microsoft/TypeScript-go#4729](https://github.com/microsoft/TypeScript-go/pull/4729) (Open)

**add android prebuilt binary support**

*Add Android prebuilt binary support by requiring the Android NDK in PATH and hardcoding the nativePreviewReleaseVersion to build all targets.*

 * created by **thunder-coding**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5069922440) **jakebailey** said "We're not going to have any of this NDK stuff on the build machine. I'm a bit confused why any of this is required, but maybe esbuild has been dealing with this too."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5072656165) **thunder-coding** explained that esbuild’s prebuilt android arm64 binaries avoid cgo and described enabling cgo for arm64 Android in the PR for consistency and to fix name-resolution issues via libc’s getaddrinfo
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5072672160) **jakebailey** stated that they would need to install the NDK on the builder but preferred to wait for repo consolidation and pipeline co-location before accepting the PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5072859877) **thunder-coding** thanked for the explanation, noted tsgo's lack of DNS or HTTP requests, proposed adding Android arm64 support without cgo now and other architectures later, and asked if it was acceptable
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5072918994) **jakebailey** confirmed tsgo did not make dns resolutions or http requests and noted that Android arm64 support could be added after #4566
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5072992486) **thunder-coding** noted surprise at the raw handling of syscalls for fanotify and inotify breaking Go portability
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5073026810) **jakebailey** said ""portable" to us meant "we can port our code to it", because our TS was structurally similar to Go. Has nothing to do with platform specific code."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5073653412) **robertkirkman** explained that building the Go binary so its file output matches the given ELF 64-bit LSB shared object for ARM aarch64 built by NDK r29 will work properly
 * [today](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5073663868) **jakebailey** said "I don't think it's required; I am putting up another PR that's the simplified version of this which perhaps you all could check. But, it'll only work for arm64."

### [PR microsoft/TypeScript-go#4731](https://github.com/microsoft/TypeScript-go/pull/4731) (Closed)

**Lazily collect source file identifiers**

*Delay source file identifier collection until requested and eliminate unnecessary interning code to boost performance and reduce memory overhead.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5072626956) **jakebailey** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5072627848) **typescript-automation[bot]** announced that performance tests started and that the comment would update with results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5072854407) **typescript-automation[bot]** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5075318768) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5075319263) **typescript-automation[bot]** posted CI status update with build start and result links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4731#issuecomment-5075541566) **typescript-automation[bot]** provided performance run results requested by @DanielRosenwasser

### [PR microsoft/TypeScript-go#4732](https://github.com/microsoft/TypeScript-go/pull/4732) (Open, `dependencies`, `javascript`)

**Bump fast\-uri from 3\.1\.2 to 3\.1\.4**

*Upgrade fast-uri dependency from version 3.1.2 to 3.1.4 to include security fixes.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

### [PR microsoft/TypeScript-go#4733](https://github.com/microsoft/TypeScript-go/pull/4733) (Open)

**Add wasip1 npm build target**

*Add a wasip1 npm build target that assumes host-mounted tsc.wasm instead of bundling lib.d.ts, fixing issues 4633 and 4706.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4733#issuecomment-5073968665) **jakebailey** said "wasip1 lacks os.Executable, so this breaks, currently."

### [PR microsoft/TypeScript-go#4734](https://github.com/microsoft/TypeScript-go/pull/4734) (Open)

**Add Android ARM64 release target**

*Add Android ARM64 release target to the build configuration*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5075800807) **robertkirkman** said "Is there a way I can download the GitHub Actions CI artifact from this PR?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5075829438) **jakebailey** said "No, but I could temporarily enable that (it'd be too big overall to have on always)"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4734#issuecomment-5075861964) **robertkirkman** said "If it's not too much trouble I would like to test it, but if it would take too long then don't worry about it."

### [PR microsoft/TypeScript-go#4735](https://github.com/microsoft/TypeScript-go/pull/4735) (Closed)

**Fix panic in variadic tuple relationship checking**

*Prevents a panic when checking relationships in variadic tuples.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4735#issuecomment-5075016220) **jakebailey** said "This also closes https://github.com/microsoft/TypeScript/issues/62974, right?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4735#issuecomment-5075604345) **ahejlsberg** confirmed that it also closed issue #62974
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4736](https://github.com/microsoft/TypeScript-go/pull/4736) (Closed)

**Update trademarks section for clarity and consistency**

*Revise trademarks section formatting and wording to improve clarity and consistency.*

 * created by **joaquinjulca26**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4736#issuecomment-5075039360) **jakebailey** said "This is standard verbiage across all MS repos and cannot be edited"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4737](https://github.com/microsoft/TypeScript-go/pull/4737) (Closed)

**Clarify long\-term integration plans for repository**

*Update repository wording to clarify its long-term integration strategy.*

 * created by **joaquinjulca26**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4737#issuecomment-5075057861) **jakebailey** said "These changes are not helpful, please stop"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4738](https://github.com/microsoft/TypeScript-go/issues/4738) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript's main pipeline analyzed 300 popular repos, succeeded on 199, found six interesting changes, and experienced timeouts and clone failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535585) **typescript-automation[bot]** reported a panic handling request textDocument/formatting due to a debug failure and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535642) **typescript-automation[bot]** reported server connection closed prematurely with undefined and provided affected repo details, raw error artifacts, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535700) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repo, error details, last requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535744) **typescript-automation[bot]** reported that the server connection closed prematurely for nuxt/nuxt and provided logs and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4738#issuecomment-5075535782) **typescript-automation[bot]** reported a server connection closed prematurely error and provided affected repository details, logs, and repro steps

### [PR microsoft/TypeScript-go#4739](https://github.com/microsoft/TypeScript-go/pull/4739) (Open)

**Refresh config file diagnostics when a config file is saved**

*Saving tsconfig or jsconfig files now triggers a debounced snapshot update to immediately refresh diagnostics.*

 * created by **UditDewan**

### [Issue microsoft/TypeScript-go#4740](https://github.com/microsoft/TypeScript-go/issues/4740) (Closed, `Domain: Type Checking`, `Type Ordering`)

**Divergence from tsc: assignment accepted by 5\.9/6\.0 is rejected by \`tsgo\` \(recursive DeepPartial \+ contravariant \`this\` \+ UnionToIntersection cycle, reduced from chart\.js\)**

*tsgo rejects an assignment involving a recursive DeepPartial type with contravariant this and a union-to-intersection cycle that is accepted by tsc 5.9/6.0*

 * created by **johanrd**

### [PR microsoft/TypeScript-go#4741](https://github.com/microsoft/TypeScript-go/pull/4741) (Open)

**Allocate node and symbol IDs in per\-checker blocks**

*Allocates node and symbol IDs in per-checker contiguous blocks to reduce contention and memory usage and enhance performance.*

 * created by **mds-ant**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5079034886) **mds-ant** said "cc: @ahejlsberg @jakebailey "
 * [later](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5079055305) **jakebailey** said "@typescript-bot perf test this"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5079055587) **typescript-automation[bot]** reported that perf test jobs started and linked to build and results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4741#issuecomment-5079144193) **typescript-automation[bot]** provided the performance comparison report for the requested perf run

