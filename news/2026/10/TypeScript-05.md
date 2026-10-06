# Report for 2026-10-05 (Monday, October 5th, 2026)

17 different users commented on 34 different issues.

## Recommended Actions

 * Response Recommended
    * @musatoktas provided reproduction steps and performance measurements in [microsoft/TypeScript#62230](https://github.com/microsoft/TypeScript/issues/62230#issuecomment-6017645478)
    * @leonidaz reported missing Organize Imports edits in the API session in [microsoft/TypeScript#63879](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-6004984124)
    * @njmarsh provided repro steps as requested in [microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-6002184086)

## Activity Summary

### [Issue microsoft/TypeScript#62230](https://github.com/microsoft/TypeScript/issues/62230) (Closed, `Help Wanted`, `Domain: Performance`, `Possible Improvement`)

**TypeScript Language Features: \`Analyzing '\.\.\.' and its dependencies\` takes crazy long time\!**

*VS Code's TypeScript language service takes excessively long to analyze an empty TypeScript file and its large dependencies.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/62230#issuecomment-3208338589) **andrewbranch** asked if turning the setting to off improved things
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/62230#issuecomment-3212297128) **babakfp** confirmed that turning the setting to off improved things
 * **RyanCavanaugh** added label `Domain: Performance`
 * [later](https://github.com/microsoft/TypeScript/issues/62230#issuecomment-6017645478) **musatoktas** measured auto-import performance in TS 5.9.3 versus native implementation using a large export package and found quadratic scaling in TS and linear scaling in native
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*Roadmap for TypeScript 7.1 detailing milestones and features across compiler, editor productivity, and performance enhancements.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5553421244) **stavalfi-oasis** said "great work thank you!! are you also planning to fix all memory leaks? latest version gets to 30-40+ GB RAM quite often (from vscode)"
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5553473110) **jakebailey** said "Please file an issue if you have something that reproduces."
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5554066590) **earthboundkid** reminded participants to keep comments on-topic and focus on 7.1 progress
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6005102141) **DanielRosenwasser** said "Due to a lot of infrastructure issues, we'll be at least a few days late on beta."

### [Issue microsoft/TypeScript#63879](https://github.com/microsoft/TypeScript/issues/63879) (Open, `Suggestion`)

**feat\(contentmapper\): support whole\-symbol rename edit projection**

*Support safe whole-symbol rename projections in the Content Mapper protocol to correctly map renamed symbols between authored and generated code*

 * (5 weeks ago) **RyanCavanaugh** added label `Suggestion`, and removed label `Needs Investigation`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-5971241226) **leonidaz** explained that TSRX syntax compiles to virtual TSX and that no printer can reconstruct the original formatting, illustrating the issue with code examples
 * [today](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-5999263358) **andrewbranch** refuted that separate language servers would be required, stating that the API provides access to the existing TypeScript language server process and its state
 * [today](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-6004984124) **leonidaz** tested the 7.1.0-dev server and observed that extensions can connect and see unsaved changes but receive no Organize Imports edits or code fixes
 * [today](https://github.com/microsoft/TypeScript/issues/63879#issuecomment-6007343299) **andrewbranch** requested that the commenter engage in discussion in a personal, concise voice rather than through lengthy AI-generated text

### [Issue microsoft/TypeScript#63928](https://github.com/microsoft/TypeScript/issues/63928) (Open, `Needs Investigation`, **andrewbranch**)

**LSP server sends no per\-file diagnostics to clients without pull diagnostics support**

*Implement push-based per-file diagnostics for LSP clients without pull support by publishing diagnostics on open, change, and close.*

 * **RyanCavanaugh** added label `Needs Investigation`
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/63928#issuecomment-5379757974) **el-pendeloco** mentioned that testing tsc’s LSP in the Helix editor didn’t produce diagnostics beyond tsconfig ones
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/63928#issuecomment-5391898251) **KiYugadgeter** said "It also affect to vim-lsp too."
 * [today](https://github.com/microsoft/TypeScript/issues/63928#issuecomment-5998475535) **stefnotch** reported that vim-lsp now supports pull diagnostics, shared a Helix pull request link, and noted Helix hasn’t had a recent release

### [PR microsoft/TypeScript#63972](https://github.com/microsoft/TypeScript/pull/63972) (Closed, `For Uncommitted Bug`)

**Fix crash on malformed object destructuring assignment**

*Ensure TypeScript no longer crashes when parsing malformed object destructuring assignments.*

 * created by **Andarist**
 * (6 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **Andarist** closed the issue

### [PR microsoft/TypeScript#63973](https://github.com/microsoft/TypeScript/pull/63973) (Closed, `For Uncommitted Bug`)

**Fix crash on malformed super destructuring**

*Fix a TypeScript compiler crash when super destructuring is malformed.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **Andarist** closed the issue

### [Issue microsoft/TypeScript#64037](https://github.com/microsoft/TypeScript/issues/64037) (Open, `Needs More Info`)

**npx tsc \-w is triggering itself after each build**

*npx tsc --watch enters a build loop because output JavaScript files alongside TypeScript sources continuously retrigger compilation.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5429365937) **RyanCavanaugh** said "We need a concrete repro in order to investigate"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5441005231) **msab-john** said "I'll see if I can make a small and simple one..."
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-5527566209) **nstepien** described a simple repro of tsc --watch triggering on new directory creation and noted missing logging of the trigger source
 * [today](https://github.com/microsoft/TypeScript/issues/64037#issuecomment-6002184086) **njmarsh** provided a reproduction case on 7.0.2 showing that writes under excluded directories still triggered rebuilds in watch mode

### [PR microsoft/TypeScript#64411](https://github.com/microsoft/TypeScript/pull/64411) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Preserve primitive literal union origins without special intersections**

*Preserve literal union origins for string, number, and bigint in completions and quick info without special intersections.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-5802862985) **weswigham** explained that origin metadata loss during control-flow filtering and nested union composition was intentional and described current quick info limitations and potential future enhancements
 * [later](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6019356961) **jakebailey** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64411#issuecomment-6019359564) **typescript-automation[bot]** posted updates on build jobs starting

### [Issue microsoft/TypeScript#64450](https://github.com/microsoft/TypeScript/issues/64450) (Closed, `Needs Investigation`, **johnfav03**)

**createWatchProgram\(\)\.close\(\) does not cancel the pending program update timer**

*close() does not cancel the pending program update timer in createWatchProgram, causing updates to run after closure and preventing process exit.*

 * **RyanCavanaugh** assigned to **johnfav03**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64450#issuecomment-5950681585) **skywalkersPadawan** opened PR #64587 targeting release-6.0 that cleared the pending timerToUpdateProgram in createWatchProgram().close with a regression test and asked if the issue needs linking or different triage
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/64450#issuecomment-5957580501) **jakebailey** said "I do not think we're going to be patching or releasing TS 6.0."
 * (today) **johnfav03** closed the issue

### [PR microsoft/TypeScript#64472](https://github.com/microsoft/TypeScript/pull/64472) (Closed, `For Uncommitted Bug`)

**Fix crash on malformed object destructuring assignment in decorated class**

*Correct compiler crash caused by malformed object destructuring assignments within decorated classes.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64472#issuecomment-5849059261) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **Andarist** closed the issue

### [Issue microsoft/TypeScript#64498](https://github.com/microsoft/TypeScript/issues/64498) (Closed, `Bug`, **andrewbranch**)

**Program\.emitToString\(\) silently omits real files due to nondeterministic isSourceFileFromExternalLibrary\(\) misclassification**

*TypeScript’s Program.emitToString sometimes excludes real source files because isSourceFileFromExternalLibrary nondeterministically marks them as external library files.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/64498#issuecomment-5916667448) **RyanCavanaugh** said "@jelical we're interested in how to streamline AI-assisted bug reports like this one. Can you walk me through the human-side workflow that you went through to get to this spot?"
 * [today](https://github.com/microsoft/TypeScript/issues/64498#issuecomment-5990423700) **cplieger** provided the fix reference #64632
 * [today](https://github.com/microsoft/TypeScript/issues/64498#issuecomment-5993634266) **cplieger** described an AI-assisted fix for nondeterministic output in a monorepo, traced the root cause in filesparser.go, and proposed two enhancements to AI-driven issue reporting
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64583](https://github.com/microsoft/TypeScript/pull/64583) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**Allow other VS Code extensions to install LSP middleware on language feature responses**

*Enable third-party VS Code extensions to register custom LSP middleware for TypeScript language feature responses*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (3 days ago) **andrewbranch** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64583#issuecomment-5971044194) **insilications** said "@andrewbranch Thanks so much for support this use case! This will unlock a lot of interesting things."
 * [today](https://github.com/microsoft/TypeScript/pull/64583#issuecomment-5999107866) **andrewbranch** said "@insilications can I ask what extension you’re working on and how you plan to use this?"

### [PR microsoft/TypeScript#64604](https://github.com/microsoft/TypeScript/pull/64604) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update DOM types**

*Add and refine TypeScript DOM types to support new Web APIs, HTML sanitization, CSS and animation features, and compatibility changes*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5959901336) **jakebailey** noted that fetch accepting extra parameters caused confusion among implementers unfamiliar with its signature and expressed uncertainty about resolving the issue
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5961950897) **saschanaz** said "Should we back it out and investigate the options? "
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5962132954) **jakebailey** said "Yeah, I think that would be wise"
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5999819379) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-5999821003) **typescript-automation[bot]** posted an automated update on test jobs start and results
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6000221845) **typescript-automation[bot]** notified that the DT test run failed and requested checking the log for details
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6000263420) **typescript-automation[bot]** posted the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6000307241) **typescript-automation[bot]** provided user test results comparing baseline and pr and noted a TS2345 error in lodash
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6001070316) **typescript-automation[bot]** reported that running the top 400 repos tsc comparison between baseline and pr succeeded without issues
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6001195121) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6001196505) **typescript-automation[bot]** announced that jobs were starting and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6001590231) **typescript-automation[bot]** reported DT test results showing type errors in d3-fetch and d3-fetch/v2 regarding the crossOrigin property
 * [today](https://github.com/microsoft/TypeScript/pull/64604#issuecomment-6002390913) **jakebailey** said "I guess this is all pretty expected. crossOrigin is the big break now."

### [PR microsoft/TypeScript#64620](https://github.com/microsoft/TypeScript/pull/64620) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Remove legacy localization handbacks**

*Remove legacy localization handbacks since OneLoc now provides translations.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64624](https://github.com/microsoft/TypeScript/pull/64624) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix idle cache clean timer never being stored on Session**

*The idle cache clean timer isn't saved to session, so cancelIdleCacheClean can't stop it and Close blocks until it fires.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64625](https://github.com/microsoft/TypeScript/issues/64625) (Open, `Possible Improvement`, **weswigham**)

**Declaration emit re\-walks a package\.json \`exports\` map for every declaration \(module specifier cache not shared across node builders\)**

*Declaration emit repeatedly walks the package.json exports map for each declaration, causing significant performance regressions.*

 * created by **novacoole**
 * (today) **weswigham** added label `Possible Improvement`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript/issues/64625#issuecomment-5999865209) **weswigham** said "I've been meaning to get back to this architectural TODO for a bit - I'll clean it up, since someone actually came forward with a project it has outsized impact for."

### [Issue microsoft/TypeScript#64627](https://github.com/microsoft/TypeScript/issues/64627) (Open, `Bug`)

**\`import defer "\./a\.js"\` is accepted without an error, and the output drops \`defer\`**

*TypeScript incorrectly accepts and strips 'import defer "./a.js"' instead of reporting a syntax error.*

 * created by **leonidaz**
 * **RyanCavanaugh** added label `Bug`

### [PR microsoft/TypeScript#64632](https://github.com/microsoft/TypeScript/pull/64632) (Closed, `For Milestone Bug`, **andrewbranch**)

**Restart a file's imports when a later arrival lowers its node\_modules depth**

*Restart a file's import subtasks when its node_modules depth decreases to ensure consistent library classification and complete emits.*

 * created by **cplieger**
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64646](https://github.com/microsoft/TypeScript/pull/64646) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Fix flaky diagnostic on JS constructor\-defined properties**

*Enforce type checking for all JavaScript constructor-defined properties to prevent flaky implicit any diagnostics.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#64647](https://github.com/microsoft/TypeScript/pull/64647) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Expose API client modules from VS Code extension**

*Expose TypeScript API client modules via the VS Code extension so third-party extensions resolve matching client versions for LSP servers.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64648](https://github.com/microsoft/TypeScript/pull/64648) (Open, `Author: Team`, `For Uncommitted Bug`, **ahejlsberg**)

**Add cache to \`getSimplifiedConditionalType\`**

*Add caching for conditional types in getSimplifiedType to improve performance and ensure consistency.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6001635450) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6001636783) **typescript-automation[bot]** posted automated build status updates for multiple commands
 * [today](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6001942905) **typescript-automation[bot]** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6002023310) **typescript-automation[bot]** posted performance run results for the requested perf run
 * [today](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6002061254) **typescript-automation[bot]** provided tsc user test results and indicated everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6002735350) **typescript-automation[bot]** reported successful tsc comparison between baseline and pr on the top 400 repos
 * [today](https://github.com/microsoft/TypeScript/pull/64648#issuecomment-6004798872) **ahejlsberg** said "No measurable effect on perf tests, likely because we don't have react tests which is where it's supposed to help."

### [PR microsoft/TypeScript#64649](https://github.com/microsoft/TypeScript/pull/64649) (Open, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Cache one nodebuilder per emit resolver, make emit resolver emit context scoped**

*Cache one NodeBuilder per emit resolver and scope each emit resolver to its specific emit context.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, and assigned to **weswigham**

### [Issue microsoft/TypeScript#64650](https://github.com/microsoft/TypeScript/issues/64650) (Open)

**Auto\-import should not offer a barrel to files inside same package**

*TypeScript auto-import offers barrel exports for internal package files, leading to accidental circular imports.*

 * created by **lonix1**

### [PR microsoft/TypeScript#64651](https://github.com/microsoft/TypeScript/pull/64651) (Open, `For Uncommitted Bug`)

**Fix crashes on malformed destructuring assignments during emit**

*Allow processing of malformed destructuring AST nodes by removing strict asserts to prevent emit crashes.*

 * created by **Andarist**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64651#issuecomment-6011076868) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64652](https://github.com/microsoft/TypeScript/pull/64652) (Open, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20261006092133433 to main**

*Automated pull request merges localized lcls changes from lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20261006092133433 branch into main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64653](https://github.com/microsoft/TypeScript/issues/64653) (Open)

**Windows: module resolution fails for paths containing a \`con/\` directory segment \(reserved device name\)**

*TypeScript native on Windows cannot resolve imports from a directory named con, resulting in TS2307 errors after upgrading beyond 6.0.3.*

 * created by **itrapashko**

### [PR microsoft/TypeScript#64654](https://github.com/microsoft/TypeScript/pull/64654) (Open, `For Uncommitted Bug`, **ahejlsberg**)

**check the target of a type reference in isWeakType**

*Modify isWeakType to check the target of type references instead of instantiating generic members, reducing memory usage by 19%.*

 * created by **maschwenk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64654#issuecomment-6017564102) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **jakebailey** assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#64655](https://github.com/microsoft/TypeScript/issues/64655) (Open)

**Hover ignores the JSDoc written on an \`import f = a\.f\` alias**

*Hover and completion info for import aliases incorrectly show the original declaration's JSDoc instead of the alias's own documentation.*

 * created by **patrickkettner**

### [Issue microsoft/TypeScript#64656](https://github.com/microsoft/TypeScript/issues/64656) (Open)

**Declaration emit errors \(TS5088\) on anonymous cyclic types that 6\.0 elided to \`any\`**

*TypeScript 7’s declaration emitter now errors on anonymous cyclic types instead of eliding them to any, causing breaking changes.*

 * created by **ssalbdivad**

