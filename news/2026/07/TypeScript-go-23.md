# Report for 2026-07-23 (Thursday, July 23rd, 2026)

17 different users commented on 28 different issues.

## Recommended Actions

 * Moderation
    * @revskill10 posted rude content in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5070774783)
 * Response Recommended
    * @hkleungai suggested a code fix for the export syntax issue in [microsoft/TypeScript-go#4525](https://github.com/microsoft/TypeScript-go/issues/4525#issuecomment-5062019310)
    * @mikearnaldi provided a real-world use case for lifting the limitation in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5060836860)
    * @mikearnaldi provided feedback about needing to enable semantic tokens in [microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5063344000)
    * @thunder-coding asked how the native Go binary is built for npm packaging and suggested adding a build-from-source option in [microsoft/TypeScript-go#4715](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062216492)
    * @thunder-coding asked about packaging as a separate package or using package.json scripts to download and build from the git tarball in [microsoft/TypeScript-go#4715](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5068954049)
    * @HuzaifaAbdulRehman asked for review of the checker fix in [microsoft/TypeScript-go#4728](https://github.com/microsoft/TypeScript-go/pull/4728#issuecomment-5069950942)

## Activity Summary

### [PR microsoft/TypeScript-go#4407](https://github.com/microsoft/TypeScript-go/pull/4407) (Open, **jakebailey**, **Copilot**)

**Restore tsgo noEmit exit status semantics**

*Restore tsgo’s noEmit exit status semantics by porting tsc’s handleNoEmitOptions logic to ensure exit code 2 for type errors*

 * **Copilot** assigned to **jakebailey**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-4781670224) **jakebailey** criticized the implementation as random and hacky and said the test case was not valid
 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-4782003646) **Copilot** identified the root cause as the EmitSkipped value, ported handleNoEmitOptions into Program.Emit, reverted the cmd/tsgo hack and its test, and added a tsc command-line test
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5063909048) **jakebailey** said "@copilot merge main and bring the baselines up to date"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4407#issuecomment-5064115508) **Copilot** merged main and updated the stale baseline for tsc/projectReferences/when-project-references-have-invalid-fields

### [Issue microsoft/TypeScript-go#4525](https://github.com/microsoft/TypeScript-go/issues/4525) (Open, `possible improvement`, `Needs Investigation`, **weswigham**)

**Follow\-up on issues/4254: \`typeof\` emit does not happen in \`export const { \.\.\. } = default\`**

*tsgo’s declaration emitter incorrectly inlines function signatures instead of using typeof when destructuring and exporting properties from a default export.*

 * (6 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4525#issuecomment-5061625407) **weswigham** asked if there was no bug and if the proposal was to stop flattening binding patterns in declaration emit
 * [today](https://github.com/microsoft/TypeScript-go/issues/4525#issuecomment-5062019310) **hkleungai** acknowledged correctness of current implementation, questioned the legitimacy of the export declare syntax, and suggested a code fix to avoid duplicating the bar declaration that breaks typeof emit reuse
 * **weswigham** added label `possible improvement`

### [Issue microsoft/TypeScript-go#4527](https://github.com/microsoft/TypeScript-go/issues/4527) (Closed, `bug`, `meta-issue`, **weswigham**)

**Investigate inconsistent diagnostic output in baselines & make builds with inconsistent diagnostic output fail tests**

*Investigate inconsistent diagnostic outputs in baselines caused by checker order dependence and enforce build failures on detection.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4527#issuecomment-4870977001) **weswigham** mentioned that strada also contained TS-1 diagnostics in three additional baselines and proposed making TS-1 errors fail the build as the issue's completion criteria
 * (2 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4574](https://github.com/microsoft/TypeScript-go/pull/4574) (Closed)

**Add ability to get emit output from the API**

*Add an API feature that allows users to programmatically retrieve emitted output.*

 * created by **dragomirtitian**
 * (later) **dragomirtitian** closed the issue

### [Issue microsoft/TypeScript-go#4581](https://github.com/microsoft/TypeScript-go/issues/4581) (Open)

**TS2719/TS2322 false positive on a generic type forwarded through an interface \`extends\` boundary \(tsc clean, tsgo fails\)**

*tsgo wrongly reports a TS2719/TS2322 type mismatch when extending and forwarding a library’s generic props interface despite tsc accepting it*

 * created by **alekseigoloviichuk**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4581#issuecomment-5066070667) **alscotty-fox** said "+1 on this issue"

### [PR microsoft/TypeScript-go#4592](https://github.com/microsoft/TypeScript-go/pull/4592) (Open)

**Improve responsiveness of \`tsc build\` to interruption**

*Enhance tsc build responsiveness to SIGINT and SIGTERM by threading cancellation contexts through compilation, exiting with proper codes, and adding tests.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-4939873881) **lukesandberg** agreed that the company was Vercel
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5036518306) **jakebailey** questioned whether Ctrl+C was handled previously or was unhandled in the old compiler
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5049741466) **lukesandberg** asked if Ctrl+C was handled by default in the old compiler and suggested removing the signal handlers given that interruption reports success in watch mode
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5063525613) **jakebailey** said "The further this goes, the more I wonder if we should simply stop handling signals except in the LS or something. Obviously we never set up any signal handlers in tsc, right?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4592#issuecomment-5064330139) **lukesandberg** noted that skipping signal handlers causes crashes with partial outputs and suggested propagating context.Context for LSP timeouts for consistency

### [PR microsoft/TypeScript-go#4660](https://github.com/microsoft/TypeScript-go/pull/4660) (Closed, **DanielRosenwasser**, **Copilot**)

**Respect configured TypeScript diagnostic locale**

*Respect js/ts.locale and typescript.locale overrides for TypeScript diagnostics, restart the language server on changes, and fallback to auto display language.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5052112712) **DanielRosenwasser** said "Sure, @copilot do what Jake suggested."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5052157543) **Copilot** implemented locale resolution once in Client.start(), passed it to NativePreviewLanguageClient, optimized getLocale(), and ensured client restart picks up locale changes
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5053242677) **jakebailey** said "It didn't understand what I said, I meant the Client in the server, as in project.Client"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5063874660) **DanielRosenwasser** said "@copilot sounds like you need to make some adjustments."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5064034993) **Copilot** enumerated changes to support dynamic locale updates, including adding GetLocale to project.Client, implementing GetLocale on the Server, updating diagnostic publishing with locale context, and removing the extension restart handler
 * [today](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5064105934) **jakebailey** criticized the proposed solution as incorrect and recommended implementing a UserPreference to read the locale with a Client callback for setting a new locale
 * [today](https://github.com/microsoft/TypeScript-go/pull/4660#issuecomment-5064280433) **Copilot** stated that the initial approach was wrong and described the fix implemented in commit e83a1d7d

### [PR microsoft/TypeScript-go#4699](https://github.com/microsoft/TypeScript-go/pull/4699) (Closed)

**API emit**

*Add program.emit, program.emitToString, getJavaScriptEmit, and getDeclarationEmit methods for flexible file system and in-memory emissions.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5056103727) **pfumagalli** said "@andrewbranch, shall I then close #3616 as it's incorporated into this one? So looking forward for this to hit the registries!!!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5059826896) **andrewbranch** said "@pfumagalli yes, go ahead, thanks!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5063044729) **andrewbranch** noted that source maps were already included in program.emit and program.emitToString outputs, added tests, and asked whether getters for source map emit and declaration source map emit should be added
 * [today](https://github.com/microsoft/TypeScript-go/pull/4699#issuecomment-5063469921) **jakebailey** said "Would anyone ever want the source map for a file output they don't have? I assume not, so those two wouldn't be needed?"

### [PR microsoft/TypeScript-go#4708](https://github.com/microsoft/TypeScript-go/pull/4708) (Closed)

**Add lint rule for identifying common patterns in the checker that lead to inconsistent diagnostic output**

*Add a lint rule to detect and fix inherited TS-1 diagnostic inconsistencies by always checking children for consistent error reporting*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4708#issuecomment-5053743419) **typescript-automation[bot]** posted CI job status updates with links for test top400 and perf test this faster
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4708#issuecomment-5053877415) **typescript-automation[bot]** posted the requested performance run results
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4708#issuecomment-5054169607) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the PR merge returned no issues
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Add support for external content mapper packages in TypeScript configuration to transform unsupported file types into valid TypeScript syntax.*

 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5056511449) **nikelborm** said "Hi, @ryanrasti, I think this would land perfectly for your typenix project"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5056997160) **mikearnaldi** said "Are the limitations of Emit temporary or intentional? it would be helpful to have TS emit both JS and mapped declarations so one could build foo.X to foo.d.ts / foo.js"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5059453768) **andrewbranch** asked for real-world use cases before lifting the limitation, suggested using --rewriteRelativeImportExtensions, and noted that TS content in Vue components may not produce useful JS output
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5060836860) **mikearnaldi** described experimenting with a custom Effect DSL using Volar that compiled to TypeScript
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5061558382) **andrewbranch** demonstrated a demo-quality Vue transform in the editor, tested hover types for script and template refs, showcased navigation projections, auto-import behavior, and error grouping via screenshots, and noted areas for improvement
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5063344000) **mikearnaldi** mentioned working on a similar experiment, shared a link, and noted needing to enable semantic tokens
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5070266955) **mikearnaldi** provided a quick update on found issues and shared patch locations, noting that patch 0005 introduced a new API outside the PR scope
 * [later](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5070774783) **revskill10** insulted VSCode as a piece of shit and demanded a fix

### [Issue microsoft/TypeScript-go#4715](https://github.com/microsoft/TypeScript-go/issues/4715) (Open, **jakebailey**)

**Request for support for Android**

*Enable straightforward installation and execution of the TypeScript compiler via npm in Android Termux without extra workarounds*

 * created by **robertkirkman**
 * **jakebailey** assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062216492) **thunder-coding** asked how the native Go binary was built for npm packaging and suggested adding support for always compiling it from source
 * [today](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062294465) **jakebailey** explained that the build pipeline is currently private but will become public after moving repos, noted uncertainty about implementing from-source builds, stated that binaries are reproducible except on Windows due to signing, and clarified intent to add Android platform support
 * [today](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062577036) **robertkirkman** explained that if code was compiled with Android NDK r27d, r29, or r30 while avoiding three specified dependency patterns, the resulting binaries would be compatible with Termux
 * [today](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062606171) **thunder-coding** noted that the build pipeline is defined in Herebyfile.mjs, suggested adding the missing platform configuration and implementing a source-built-binary fallback similar to sharp
 * [today](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5062840275) **jakebailey** said "There's basically no way we're going to ship the entire repo in the package."
 * [later](https://github.com/microsoft/TypeScript-go/issues/4715#issuecomment-5068954049) **thunder-coding** suggested packaging the repo separately or adding package.json scripts to download and build from the git tarball via gitHead

### [Issue microsoft/TypeScript-go#4719](https://github.com/microsoft/TypeScript-go/issues/4719) (Open, **jakebailey**, **Copilot**)

**tsgo reports type errors in external\-library \(node\_modules\) source files that tsc suppresses**

*tsgo reports type errors in .ts and .tsx files within external dependencies despite skipLibCheck, while tsc suppresses them.*

 * created by **golden-eng-beers**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4719#issuecomment-5063509787) **jakebailey** pointed out that non-declaration files from node_modules seemed incorrect and suggested the error was a new ordering issue unrelated to node_modules

### [Issue microsoft/TypeScript-go#4720](https://github.com/microsoft/TypeScript-go/issues/4720) (Open)

**Auto import suggestions break with circular workspace dependencies**

*Auto-import suggestions in tsgo fail for relative imports within workspaces involved in a circular dependency chain.*

 * created by **iansan5653**

### [PR microsoft/TypeScript-go#4721](https://github.com/microsoft/TypeScript-go/pull/4721) (Open, **jakebailey**, **Copilot**)

**Honor ts\-ignore directives on multiline JSX in dependencies**

*Extend ts-ignore directive matching to properly suppress multiline JSX attribute errors in dependency source files.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#4722](https://github.com/microsoft/TypeScript-go/issues/4722) (Open, **jakebailey**, **Copilot**)

**Nested nullish coalescing \+ comment \+ ES2018 causes function body to be ignored**

*Transpiling nested nullish coalescing with comments targeting ES2018 misplaces the return statement causing function body to be ignored*

 * created by **kamsar**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4723](https://github.com/microsoft/TypeScript-go/pull/4723) (Open, **jakebailey**, **Copilot**)

**Preserve comments when downleveling arrow expression bodies**

*Maintain leading comments in arrow function expression bodies when downleveling optional chaining by attaching them before the synthesized return statement.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4724](https://github.com/microsoft/TypeScript-go/pull/4724) (Closed)

**\[api\] Add proper ParsedCommandLine type, provide APIs for getting config source files**

*Add a ParsedCommandLine property to projects and program APIs to list and retrieve configuration file names and AST source files.*

 * created by **andrewbranch**

### [PR microsoft/TypeScript-go#4725](https://github.com/microsoft/TypeScript-go/pull/4725) (Closed)

**Show repopulate info in readable buildinfo**

*Include repopulate information in readable buildinfo baselines, as it is currently missing.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4726](https://github.com/microsoft/TypeScript-go/pull/4726) (Open)

**Skip declaration emit without a prior signature**

*Skip emitting TypeScript declaration files for declarations that lack an existing signature*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#4727](https://github.com/microsoft/TypeScript-go/issues/4727) (Closed, `bug`, **ahejlsberg**)

**Panic in propertiesRelatedTo for recursive variadic tuple constraint**

*TypeScript-Go native-preview panics with an index out of range error in propertiesRelatedTo while inferring recursive variadic tuple types*

 * created by **HuzaifaAbdulRehman**

### [PR microsoft/TypeScript-go#4728](https://github.com/microsoft/TypeScript-go/pull/4728) (Closed)

**Fix variadic tuple relation position mapping**

*Fix tuple mapping logic to align fixed and variadic tuple sections correctly and prevent out-of-bounds indexing.*

 * created by **HuzaifaAbdulRehman**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4728#issuecomment-5069950942) **HuzaifaAbdulRehman** requested review of a checker fix addressing the panic in issue 4727 and adding regression coverage, and offered to address feedback

### [PR microsoft/TypeScript-go#4729](https://github.com/microsoft/TypeScript-go/pull/4729) (Open)

**add android prebuilt binary support**

*Add Android prebuilt binary support by requiring the Android NDK in PATH and hardcoding the nativePreviewReleaseVersion to build all targets.*

 * created by **thunder-coding**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4729#issuecomment-5069922440) **jakebailey** said "We're not going to have any of this NDK stuff on the build machine. I'm a bit confused why any of this is required, but maybe esbuild has been dealing with this too."

### [PR microsoft/TypeScript-go#4730](https://github.com/microsoft/TypeScript-go/pull/4730) (Open, `dependencies`, `javascript`)

**Bump linkify\-it from 5\.0\.1 to 5\.0\.2**

*Upgrade linkify-it dependency from 5.0.1 to 5.0.2 to fix a mailto: DoS issue and enforce user/pass length limits.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

