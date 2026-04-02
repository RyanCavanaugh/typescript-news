# Report for 2026-03-02 (Monday, March 2nd, 2026)

14 different users commented on 40 different issues.

## Recommended Actions

 * Response Recommended
    * @JacobNWolf offered to help debug under NDA in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3986620084)
    * @goloveychuk reported that hovering on the Browser symbol causes the LSP to hang and spike memory usage in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3991640806)
    * @goloveychuk asked if the resolver searched all files for symbols in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3991968372)
    * @atscott suggested that the CLI add a mechanism to push virtual file updates similar to the LSP in [microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3987350807)

## Activity Summary

### [PR microsoft/TypeScript-go#1542](https://github.com/microsoft/TypeScript-go/pull/1542) (Closed)

**Port class fields transformer**

*The classFieldsTransformer is ported from Strada into the codebase, with the privateNameHashCharName test fixed and confirmation requested before further work.*

 * created by **chengcyber**
 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1542#issuecomment-3169528386) **chengcyber** thanked the reviewer for feedback, explained that the transformer was more complex than expected, described the original intent to fix a single test case and solicit early input, and said they would take time to align with the project's design and narrow the PR's scope
 * [28 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1542#issuecomment-3193381734) **chengcyber** introduced a dedicated classPrivateFieldsTransformer as a proof of concept and asked for feedback
 * [today](https://github.com/microsoft/TypeScript-go/pull/1542#issuecomment-3988423593) **jakebailey** said "Thanks for sending this; there was enough to change that I opted to just do it from scratch in #2956. So, closing this one."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2692](https://github.com/microsoft/TypeScript-go/issues/2692) (Closed, **jakebailey**, **Copilot**)

**tsgo does not respect \`esModuleInterop\` in certain cases**

*tsgo ignores the esModuleInterop setting when importing named exports from CommonJS JavaScript files with allowJs enabled, causing TS2497 errors.*

 * (3 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3981831054) **zurmokeeper** said "@jakebailey When might this issue be resolved? It's been quite some time now. For TypeScript code referencing common.js, TypeScript 7's type checking fails outright, rendering it completely unusable."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3985694793) **jakebailey** said "JS stuff continues to be in flux. The pattern you used with module.exports = { foo } is not one that we handled. It's possible #2946 will help this, but I have not tested yet."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3987233355) **jakebailey** said "This is 100% https://github.com/microsoft/typescript-go/issues/1054, FWIW; I didn't click to see the repro there but it's the same."

### [PR microsoft/TypeScript-go#2757](https://github.com/microsoft/TypeScript-go/pull/2757) (Open, **jakebailey**, **Copilot**)

**Port TypeScript PR \#62320: Allow \-\-module commonjs \-\-moduleResolution bundler**

*Port PR #62320 to permit bundler module resolution with CommonJS by adjusting compiler checks in program.go and updating error and output baselines.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2757#issuecomment-3987516677) **jakebailey** said "Going to wait to merge this around the same time as the node10 deprecation error."

### [PR microsoft/TypeScript-go#2759](https://github.com/microsoft/TypeScript-go/pull/2759) (Closed, **jakebailey**, **Copilot**)

**Error on esModuleInterop=false and allowSyntheticDefaultImports=false \(removed in TS7\)**

*Marking esModuleInterop and allowSyntheticDefaultImports as removed when false in TS7 by defaulting them to true and emitting errors.*

 * created by **Copilot**
 * (2 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3970103243) **andrewbranch** requested heap profiles, logs, and repro instructions and reported inability to reproduce memory usage above 171M
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3971503830) **dbrxnds** asked if the NDA signed by Jake Bailey included @andrewbranch so he could be invited to the private repository
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3972237831) **Jack-Works** provided a heap profile link showing tsgo consuming over 20GB and noted inability to capture a profile when memory is exhausted
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3986620084) **JacobNWolf** reported experiencing the same issue at beehiiv that crashed his Mac until he disabled the TypeScript Native extension, described his large PNPM monorepo setup, and offered to help debug under NDA
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3991640806) **goloveychuk** reported that hovering on the Browser symbol caused the LSP to hang and consume excessive memory in a pnpm layout under Yarn
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3991968372) **goloveychuk** reported that the patch fixed the issue for them, shared the output after waiting, and asked if it searched all files for symbols

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3947458101) **andrewbranch** clarified that they meant injecting types via TypeScript syntax in virtual files that don’t exist on disk, rather than inserting types directly into type resolution via a JS object API
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3963097012) **johnsoncodehk** suggested a pull-based plugin mechanism for CLI and LSP to resolve non-standard files, outlined cross-language and mapping challenges, and mentioned a concrete PR
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3965169605) **remcohaszing** suggested using JSON-RPC over IPC, avoiding stdout, and adding an initialize call for plugins to register file extensions, noting uncertainty about the Next.js TypeScript plugin’s functionality
 * [today](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-3987350807) **atscott** described Angular’s reliance on generating virtual TypeScript files and explained the re-engineering challenges introduced by the proposed TS Go API direction

### [PR microsoft/TypeScript-go#2904](https://github.com/microsoft/TypeScript-go/pull/2904) (Closed)

**\[@typescript/api\] Port scanner and token navigation utils to API client, include JSDoc in encoded ASTs, add more SourceFile properties**

*Integrate port scanner and token navigation into the TypeScript API client with JSDoc in encoded ASTs and more SourceFile properties.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#2922](https://github.com/microsoft/TypeScript-go/pull/2922) (Closed)

**Update npm deps, dprint**

*Update npm dependencies and include a crash fix from the gofumpt dprint plugin.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2926](https://github.com/microsoft/TypeScript-go/pull/2926) (Open)

**Implement ES decorator transform \(ESNext \-\> ES2022\)**

*Add ESNext-to-ES2022 decorator transform support in tsgo to unblock its adoption.*

 * created by **AlCalzone**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3975214922) **AlCalzone** said "Thanks for the thorough review - I'll see what I can do about it."
 * [later](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3989835921) **AlCalzone** said "@weswigham @jakebailey I think I've addressed everything now."

### [Issue microsoft/TypeScript-go#2927](https://github.com/microsoft/TypeScript-go/issues/2927) (Closed)

**"removeComments" may not work correctly in an if block\.**

*tsgo fails to remove comments inside if statements when removeComments is enabled, unlike the TypeScript compiler.*

 * created by **sgjm**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2927#issuecomment-3974111276) **sgjm** provided another case comparing tsc and tsgo outputs to illustrate comment handling differences
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2927#issuecomment-3974118999) **jakebailey** said "Yeah, i'm pretty sure this is just a simple emit bug where we are not checking removeComments; I fixed this in a branch but could send it early."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2934](https://github.com/microsoft/TypeScript-go/pull/2934) (Closed)

**fix\(2932\): handle parameter\-property ref to method with same name**

*Ensure parameter-property references to methods with the same name are resolved correctly.*

 * created by **a-tarasyuk**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2934#issuecomment-3986255673) **DanielRosenwasser** said "It seems with the latest commits, we're no longer testing find-all-refs on usages as well."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2934#issuecomment-3986428480) **a-tarasyuk** said "@DanielRosenwasser, I updated test to use ranges. Did you mean this, or were you referring to adding the additional cases?"

### [Issue microsoft/TypeScript-go#2935](https://github.com/microsoft/TypeScript-go/issues/2935) (Closed, `Crash`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Stack overflow in type instantiation with recursive function and generic type params**

*A recursive generic camelCase transformation using type-fest triggers a tsgo stack overflow from v4.38.0 onward, while tsc compiles it.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3978651671) **wadjoh** provided a 3-line example with type-fest@4.38.0, updated the initial description, and confirmed that TS 6.0.0-beta with --stableTypeOrdering still compiled successfully
 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **jakebailey** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3987301887) **jakebailey** mentioned that issue #2940 implied they were running out of stack where they hadn’t before and speculated this could be due to heavy stack allocation for performance unlike JS’s nursery allocations

### [PR microsoft/TypeScript-go#2938](https://github.com/microsoft/TypeScript-go/pull/2938) (Closed, `dependencies`, `javascript`)

**Bump minimatch from 10\.2\.1 to 10\.2\.4**

*Update minimatch dependency from version 10.2.1 to 10.2.4 to apply performance optimizations, bug fixes, and a ReDoS warning.*

 * (2 days ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * [today](https://github.com/microsoft/TypeScript-go/pull/2938#issuecomment-3987202865) **dependabot[bot]** said "Looks like minimatch is up-to-date now, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript-go#2939](https://github.com/microsoft/TypeScript-go/pull/2939) (Closed)

**fix\(2927\): add missing commentsDisabled checks to prevent emitting comments**

*Add missing commentsDisabled checks to prevent comments from being emitted when disabled.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2941](https://github.com/microsoft/TypeScript-go/pull/2941) (Closed)

**Remove and simplify code related to allowSyntheticDefaultImports/esModuleInterop**

*Remove and simplify allowSyntheticDefaultImports and esModuleInterop code paths now always enabled and error when false.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2943](https://github.com/microsoft/TypeScript-go/pull/2943) (Closed)

**fix\(api\): DocumentIdentifier JSON unmarshaling panic**

*Save JSON object keys before reading values and handle "fileName" to fix DocumentIdentifier unmarshal panic.*

 * created by **ajmacd**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2943#issuecomment-3989087477) **ajmacd** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2943#issuecomment-3989097248) **ajmacd** thanked the reviewer for catching the missing fileName field, added a test for documentation, and asked if it should be removed

### [PR microsoft/TypeScript-go#2947](https://github.com/microsoft/TypeScript-go/pull/2947) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 2 updates**

*Bump the github-actions group in the repository root by upgrading actions/upload-artifact to v7.0.0 and updating github/codeql-action.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2948](https://github.com/microsoft/TypeScript-go/pull/2948) (Closed)

**Don't re\-do \`merge\_group\` work on \`push: main\`**

*Avoid re-running merge_group work on pushes to the main branch.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2948#issuecomment-3985152514) **jakebailey** noted that jobs differ between PRs, merge queues, and pushes to main, pointed out that the change would cease macOS testing, and asked what motivated it
 * [today](https://github.com/microsoft/TypeScript-go/pull/2948#issuecomment-3985514341) **Andarist** said "I noticed a lot of work between those is being redone, but I have missed it's not an exact overlap."
 * (today) **Andarist** closed the issue

### [PR microsoft/TypeScript-go#2949](https://github.com/microsoft/TypeScript-go/pull/2949) (Closed)

**Fix formatting panic when first line is all whitespace**

*Formatting in TypeScript-Go panics if the first line contains only whitespace.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2950](https://github.com/microsoft/TypeScript-go/pull/2950) (Closed)

**Fix formatting crash on files with tab indentation near end of file**

*Fix formatting crash triggered by files that end with tab-based indentation.*

 * created by **Andarist**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2952](https://github.com/microsoft/TypeScript-go/pull/2952) (Closed)

**Fixed a go\-to\-def crash on decorators attached to invalid targets**

*Fixed a go-to-definition crash triggered by decorators attached to invalid targets.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2952#issuecomment-3985784294) **jakebailey** said "CI is failing, unfortunately."
 * [later](https://github.com/microsoft/TypeScript-go/pull/2952#issuecomment-3989797672) **Andarist** said "@jakebailey that was just caused by my last-minute test file renaming 😬 I fixed that, it should be good to go now"

### [Issue microsoft/TypeScript-go#2953](https://github.com/microsoft/TypeScript-go/issues/2953) (Open, `Crash`, **DanielRosenwasser**, **Copilot**)

**Inlay hints triggers crash during checker initialization**

*Inlay hints cause the TypeScript checker to crash during initialization in the editor.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [PR microsoft/TypeScript-go#2954](https://github.com/microsoft/TypeScript-go/pull/2954) (Open, **andrewbranch**, **Copilot**)

**Port scanner/token navigation fixes from PR \#2888 to \`\_packages/ast\`**

*Port PR #2888 fixes to the TypeScript AST package, refining JSDoc comment scanning and EOF navigation for unterminated nodes.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#2955](https://github.com/microsoft/TypeScript-go/pull/2955) (Closed)

**Clean up disk file caches more often, force GC**

*Propose more frequent disk file cache cleanup and forced garbage collection to reduce memory usage and prevent open files backlog in agent mode sessions.*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2955#issuecomment-3987869693) **jakebailey** said "I think we could do the GC without any options, yeah."

### [PR microsoft/TypeScript-go#2956](https://github.com/microsoft/TypeScript-go/pull/2956) (Closed)

**Port class fields transform \(ES2022\)**

*Ports ES2022 class fields transform with static block support into TypeScript, removes obsolete flags, and corrects UseDefineForClassFields behavior.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2957](https://github.com/microsoft/TypeScript-go/pull/2957) (Closed)

**Log runtime/metrics on UpdateSnapshot**

*Add runtime and metrics logging to UpdateSnapshot to help diagnose memory issues.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript-go#2958](https://github.com/microsoft/TypeScript-go/issues/2958) (Closed)

**Regression from Strada: IntelliSense does not work properly inside \`{}\` following \`@throws\`**

*IntelliSense suggestions for error types inside braces after an @throws annotation are missing in tsgo but present in TypeScript 6.0.*

 * created by **tats-u**

### [Issue microsoft/TypeScript-go#2959](https://github.com/microsoft/TypeScript-go/issues/2959) (Open, `Crash`)

**panic handling request textDocument/definition: bad line number**

*The TypeScript Go LSP server panics in textDocument/definition when an out-of-range line number is passed to the line-and-character to position converter.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`

### [PR microsoft/TypeScript-go#2960](https://github.com/microsoft/TypeScript-go/pull/2960) (Closed)

**Fixes a crash when requesting implementations on a tripleslash directive**

*Requesting code implementations for a tripleslash directive caused the compiler to crash and this update prevents it.*

 * created by **Andarist**

