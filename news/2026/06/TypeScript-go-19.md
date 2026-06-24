# Report for 2026-06-19 (Friday, June 19th, 2026)

10 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @epicmet provided performance trace files and reproduction steps in [microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4756988233)
    * @nikelborm reported that errors no longer occurred and changes propagated properly in [microsoft/TypeScript-go#4372](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4754939390)
    * @Alex-Bond confirmed that PR #4379 resolved the issue in [microsoft/TypeScript-go#4378](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4755249604)
    * @typescript-automation[bot] reported a panic in textDocument/formatting in [microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503367)
    * @typescript-automation[bot] reported server connection closed prematurely in [microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503379)
    * @typescript-automation[bot] reported a server connection error and provided repro steps in [microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503407)
    * @typescript-automation reported a server connection error with logs and repro steps in [microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503431)
    * @typescript-automation[bot] reported that the server connection closed prematurely in [microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503486)

## Activity Summary

### [Issue microsoft/TypeScript-go#4265](https://github.com/microsoft/TypeScript-go/issues/4265) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Fatal error from \`nil\` \`Statements\` in JSON source file**

*Parsing a JSON config file with nil Statements in the source file creation triggers a fatal error.*

 * **DanielRosenwasser** added label `Crash`
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4265#issuecomment-4696292204) **RyanCavanaugh** provided a concrete repro that yielded a similar but not identical callstack and noted the AI couldn't find an exact repro case
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347) (Open, `Needs More Info`)

**CPU usage spikes to 80% to 100% when using \`tsgo \-\-lsp \-\-stdio\`**

*tsgo's LSP process uses 80-100% CPU when typing in TypeScript files larger than 100 lines*

 * created by **epicmet**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4732756773) **DanielRosenwasser** noted that the project’s heavy checker work and allocations were impacting GC, asked if the issue persisted in TypeScript 6, and pointed to performance trace documentation
 * **DanielRosenwasser** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4756988233) **epicmet** confirmed that Typescript 6 didn't reproduce the issue, described CPU usage increase with a large file, and provided performance trace files

### [Issue microsoft/TypeScript-go#4372](https://github.com/microsoft/TypeScript-go/issues/4372) (Closed, **jakebailey**, **Copilot**)

**7\.0\.1\-rc binary in watch mode fails to resolve symlinks in node\_modules**

*TypeScript 7.0.1-rc watch mode fails to resolve or watch symlinked node_modules dependencies, causing fanotify errors.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4752646521) **jakebailey** suggested ensuring that fswatch validated directory paths or ignored non-directory symlinks
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4754782401) **jakebailey** said "If you can, can you build https://github.com/microsoft/typescript-go/pull/4376 and see if it works for you?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4754870819) **nikelborm** said "I'll try :D"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4754939390) **nikelborm** said "It no longer throws errors, and changes propagate between packages properly"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4372#issuecomment-4754941073) **nikelborm** said "Thanks! 🫶 "

### [Issue microsoft/TypeScript-go#4375](https://github.com/microsoft/TypeScript-go/issues/4375) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**Add native\-preview API for capturing \.d\.ts emit output**

*Request for extending the TypeScript native-preview JS API to emit and capture .d.ts declaration output via virtual filesystem callbacks.*

 * created by **hegrec**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4375#issuecomment-4753149490) **jakebailey** said "Related is #3616"

### [PR microsoft/TypeScript-go#4376](https://github.com/microsoft/TypeScript-go/pull/4376) (Closed, **jakebailey**, **Copilot**)

**Fix watches on symlinked directories**

*Fix watch mode on symlinked directories by resolving watch roots to physical paths and preserving symlink paths in events.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4376#issuecomment-4753955393) **jakebailey** reported a Windows test failure in TestWalkDirDoesNotFollowRootSymlinkedDir for root symlinked directory
 * [today](https://github.com/microsoft/TypeScript-go/pull/4376#issuecomment-4754033402) **Copilot** fixed the Windows walkDir root check to reject reparse-point roots to match the generic implementation and test expectations in commit 5b44de91
 * [today](https://github.com/microsoft/TypeScript-go/pull/4376#issuecomment-4754780349) **jakebailey** said "This PR basically just allows directory watches on dirs that are symlinks. It turns out that Node previously allowed such a thing. And TS treats symlinks to dirs as dirs, so it all "worked"."

### [PR microsoft/TypeScript-go#4377](https://github.com/microsoft/TypeScript-go/pull/4377) (Closed)

**Fix nil pointer panic when extending an empty config file**

*Prevent nil pointer panic by using an empty NodeList when extending an empty config file.*

 * created by **oMatheusmol**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4378](https://github.com/microsoft/TypeScript-go/issues/4378) (Open, `Needs Investigation`, **johnfav03**)

**\`tsgo \-\-watch\` error: "error starting FSEvents stream" on large \`node\_modules\` since the fswatch rewrite**

*tsgo watch mode fails to initiate its file watcher on large node_modules directories after the fswatch rewrite in recent 7.0.0-dev builds*

 * created by **Alex-Bond**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4754798937) **jakebailey** suggested improving macOS watcher setup when using fsevents due to kqueue performance issues
 * [today](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4754803327) **jakebailey** said "Random semi-related question; do you use Watchman?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4754852046) **Alex-Bond** answered that they didn’t use Watchman and instead wrote a custom AI-assisted script to start the NestJS server and tsgo watcher to avoid restarts on TypeScript errors, and linked a gist
 * [today](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4754918317) **jakebailey** asked what was meant by LSP not supporting workspace watching, specifically if it referred to full workspace diagnostics
 * [today](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4754922451) **jakebailey** said "Also, can you try https://github.com/microsoft/typescript-go/pull/4379 and see if you're able to use watch mode?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4755249604) **Alex-Bond** confirmed that they meant full workspace diagnostics, noted the LSP diagnosticProvider settings from issue 2169 and that full workspace diagnostics is planned but not in the first release, and confirmed that PR #4379 enabled watch mode and resolved the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4755392077) **jakebailey** asked if the current PR state had been tried and invited filing an issue if needed
 * [today](https://github.com/microsoft/TypeScript-go/issues/4378#issuecomment-4755443201) **Alex-Bond** confirmed compiling and running with commit ce359c1

### [PR microsoft/TypeScript-go#4379](https://github.com/microsoft/TypeScript-go/pull/4379) (Open)

**Fix watch coalescing for FSEvents**

*Coalesce dense directory watch sets into recursive ancestor watches on FSEvents and Windows to reduce per-directory streams.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4379#issuecomment-4754939213) **jakebailey** said "This is doing this in the layer above fswatch, but, going to try and shove it down..."

### [Issue microsoft/TypeScript-go#4380](https://github.com/microsoft/TypeScript-go/issues/4380) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*Server errors occurred in the TypeScript main branch pipeline while analyzing 300 popular GitHub repositories, causing timeouts and other failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503367) **typescript-automation[bot]** reported a panic with debug failure in textDocument/formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503379) **typescript-automation[bot]** reported a server connection closed prematurely error for the t4t5/sweetalert repo
 * [today](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503407) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error and provided affected repos, raw error text, replay commands, previous results, recent requests, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503431) **typescript-automation[bot]** reported server connection closed prematurely and provided error logs and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503460) **typescript-automation[bot]** reported a server connection closed prematurely with undefined for the babel/babel repository
 * [today](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503486) **typescript-automation[bot]** reported a server connection closed prematurely error for nuxt/nuxt
 * [today](https://github.com/microsoft/TypeScript-go/issues/4380#issuecomment-4755503508) **typescript-automation[bot]** reported that the server connection closed prematurely and provided error logs, affected repository details, recent request traces, and reproduction steps

### [Issue microsoft/TypeScript-go#4381](https://github.com/microsoft/TypeScript-go/issues/4381) (Open, **jakebailey**, **Copilot**)

**Behavior difference: \`\.state\` emit is missing on react component**

*tsgo incorrectly omits emitting React component state initializations inside constructors for JavaScript files, unlike tsc.*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#4382](https://github.com/microsoft/TypeScript-go/pull/4382) (Open)

**fix\(relater\): add property comparison cache fast path to avoid false TS2321**

*Add a relation-cache fast path in property-type comparisons to avoid false TS2321 errors for large object literals*

 * created by **maoger**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4757235439) **maoger** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4758527237) **jakebailey** stated that they were not going to be raising any limits

### [PR microsoft/TypeScript-go#4383](https://github.com/microsoft/TypeScript-go/pull/4383) (Open, `dependencies`, `javascript`)

**Bump undici from 7\.27\.1 to 7\.28\.0**

*Upgrade undici dependency to 7.28.0 to apply seven security fixes addressing multiple high-severity CVEs.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

