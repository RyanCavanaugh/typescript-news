# Report for 2026-09-16 (Wednesday, September 16th, 2026)

19 different users commented on 51 different issues.

## Recommended Actions

 * Response Recommended
    * @alshdavid requested direct type references from esm.sh to avoid npm installs in [microsoft/TypeScript#63115](https://github.com/microsoft/TypeScript/issues/63115#issuecomment-5706769124)
    * @NullVoxPopuli requested a wasm build for adding TS 7.1/nightly to the REPL in [microsoft/TypeScript#63813](https://github.com/microsoft/TypeScript/issues/63813#issuecomment-5700532141)
    * @typescript-automation[bot] provided build comparison results and requested review in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132673)
    * @typescript-automation[bot] provided build failure details from the top 1000 repos suite in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132806)
    * @typescript-automation[bot] provided build error details from the top 1000 repos suite in [microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132906)
    * @NullVoxPopuli-ai-agent provided a patch for content mappers and suggested README updates in [microsoft/TypeScript#64174](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703088159)
    * @NullVoxPopuli asked about standards around globalThis.fs and suggested fs access options in [microsoft/TypeScript#64174](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703651081)
    * @chenxin-yan provided environment details and reproduction context in [microsoft/TypeScript#64300](https://github.com/microsoft/TypeScript/issues/64300#issuecomment-5707036878)

## Activity Summary

### [Issue microsoft/TypeScript#63115](https://github.com/microsoft/TypeScript/issues/63115) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support loading remote types**

*Enable TypeScript to load remote type definitions in config files via URLs, removing the need for type-only dependencies.*

 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/63115#issuecomment-3882810476) **guillaumebrunerie** clarified that devDependencies is the perfect solution since tools like eslint must be installed and type definitions should match the project version
 * (30 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63115#issuecomment-5706769124) **alshdavid** described a JIT transpilation setup using http-server-rs, expressed annoyance at needing npm type installs, and requested support for direct type references via esm.sh to streamline scratch projects
 * [later](https://github.com/microsoft/TypeScript/issues/63115#issuecomment-5711377835) **danciudev** clarified that devDependencies ensured type safety for regularly used tools but occasional-use tools like Knip could be run via pnpm dlx without installing them

### [Issue microsoft/TypeScript#63708](https://github.com/microsoft/TypeScript/issues/63708) (Closed, `Possible Improvement`, **ahejlsberg**)

**It is possible to violate generic constraints when distributing union types**

*Distributive union types in TypeScript can bypass generic constraints, allowing invalid B extends A combinations without error.*

 * **ahejlsberg** added label `Possible Improvement`
 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63708#issuecomment-5624424809) **ahejlsberg** said "A fix is now available in #64237."
 * **ahejlsberg** added to milestone `TypeScript 7.1.0 Beta`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63813](https://github.com/microsoft/TypeScript/issues/63813) (Open, `Suggestion`, `Committed`, **jakebailey**)

**Wasm build**

*Request for a WebAssembly build of tsgo to enable experimentation in the online playground.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/63813#issuecomment-5700532141) **NullVoxPopuli** said "With 7.1 nearing - available in nightly, and content-mappers, I'd also like a wasm build so I can add TS 7.1/nightly to my REPL <3"
 * [today](https://github.com/microsoft/TypeScript/issues/63813#issuecomment-5700716758) **jakebailey** said "@NullVoxPopuli Can you try #64174 and see if it works for your needs? Early feedback would be appreciated."

### [PR microsoft/TypeScript#63902](https://github.com/microsoft/TypeScript/pull/63902) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update to Go 1\.27**

*Upgrade the project to Go version 1.27 to incorporate the latest language features and improvements.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (3 weeks ago) **jakebailey** added labels `Author: Team`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63926](https://github.com/microsoft/TypeScript/pull/63926) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Negated Types**

*Add support for a 'not T' negated type operator with canonical simplification rules and enhanced control flow handling*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566356) **typescript-automation[bot]** reported more changes from running the top 1000 repos suite, showing TS2322 errors in several tsconfig files for stablyai/orca
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566504) **typescript-automation[bot]** reported build errors for tldraw/tldraw, showing TS2322 type assignment failures in multiple files
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5688566632) **typescript-automation[bot]** reported type errors in trailhq/Graft, triggerdotdev/trigger.dev, and umami-software/umami from running the top 1000 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5705323884) **weswigham** requested the TypeScript bot to run top1000 and DefinitelyTyped tests
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5705324877) **typescript-automation[bot]** announced that CI jobs had started and included status links
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132673) **typescript-automation[bot]** reported build result differences when comparing main with the pull request merge across the top 1000 repos and highlighted a failure in advaitpaliwal/feynman
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132806) **typescript-automation[bot]** reported build failures from the top 1000 repos suite showing TS2322 errors in corsairdev/corsair tsconfig files
 * [today](https://github.com/microsoft/TypeScript/pull/63926#issuecomment-5706132906) **typescript-automation[bot]** reported build errors for diegosouzapw/OmniRoute from the top 1000 repos suite

### [PR microsoft/TypeScript#64088](https://github.com/microsoft/TypeScript/pull/64088) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Restore go\-to\-definition for triple\-slash lib references**

*Restore go-to-definition for triple-slash lib references in TypeScript by resolving and indexing referenced libraries.*

 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64088#issuecomment-5484252368) **DanielRosenwasser** said "@copilot I actually think the origin selection range should be the text - I dunno, check what strada did"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/64088#issuecomment-5484446580) **Copilot** verified that FileReference.TextRange is populated from the parser's pragma argument range and that updated baselines reflect the correct range
 * [today](https://github.com/microsoft/TypeScript/pull/64088#issuecomment-5705010677) **DanielRosenwasser** said "@copilot what if libFiles was a map instead?"
 * [today](https://github.com/microsoft/TypeScript/pull/64088#issuecomment-5705318600) **Copilot** implemented libFiles as a filename-to-source-file map and retained libFilesByPath for path-keyed metadata consumers

### [PR microsoft/TypeScript#64140](https://github.com/microsoft/TypeScript/pull/64140) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-uri from 3\.1\.5 to 3\.1\.7**

*Upgrade fast-uri from version 3.1.5 to 3.1.7 to address multiple high-severity security vulnerabilities*

 * (2 weeks ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64140#issuecomment-5703844056) **dependabot[bot]** said "Looks like fast-uri is no longer a dependency, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#64159](https://github.com/microsoft/TypeScript/pull/64159) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Strongly type file paths**

*Add branded types for absolute, normalized file and directory paths to enforce path invariants and reduce normalization overhead.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64159#issuecomment-5702887286) **jakebailey** said "I guess I can try and flip the API side back to strings, but there's a bunch of conversions we get to skip because of it, and some of the bugs found were on the API side outside the Go code."

### [PR microsoft/TypeScript#64174](https://github.com/microsoft/TypeScript/pull/64174) (Open, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Add wasip1 support, enabling CLI, API, browser, sync/async**

*Add experimental WASI Preview1 support in tsc.wasm, providing CLI, LSP server, and sync/async API access in Node.js and browsers.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703088159) **NullVoxPopuli-ai-agent** reported testing tsc LSP in a browser worker with a WASI shim, noted two setup requirements for stdin and SharedArrayBuffer, observed content mappers failing on wasip1, and provided a patch to implement a host-process path for mappers
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703137909) **NullVoxPopuli** said "apologies if this is way off base. I literally don't know golang :("
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703191969) **jakebailey** said "Thanks for the feedback; it's alright to not know Go, just trying it in a real project (agent or not) is good!"
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703265395) **jakebailey** noted that content mappers didn’t exist when they began the work and admitted unfamiliarity with execing and using an existing tsconfig without node
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5703651081) **NullVoxPopuli** expressed surprise at the globalThis.fs interface, asked about standards, and suggested passing fs access options or using a global mock fs
 * [today](https://github.com/microsoft/TypeScript/pull/64174#issuecomment-5704509646) **NullVoxPopuli** indicated that the feature worked somewhat and attached screenshots

### [PR microsoft/TypeScript#64210](https://github.com/microsoft/TypeScript/pull/64210) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix case sensitivity fswatch and users**

*Implement system-based case matching and a watchalias package on macOS to correctly handle case sensitivity in file watchers.*

 * (1 week ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5691848244) **jakebailey** said "This is nasty, I'm going to try and simplify it, but I think it can only be simpler by doing less precise tracking..."
 * [today](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5702061437) **jakebailey** said "It doesn't save much code to simplify it, with much worse downsides, sadly."
 * [today](https://github.com/microsoft/TypeScript/pull/64210#issuecomment-5702140819) **jakebailey** said "The FS overlay stuff very much conflicted, so, I have to figure that out"

### [PR microsoft/TypeScript#64226](https://github.com/microsoft/TypeScript/pull/64226) (Open, `For Uncommitted Bug`)

**fix: report optional\-chain tagged templates after non\-null assertions**

*Ensure tagged template expressions following non-null assertions in optional chains correctly trigger TS1358 errors.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5686441164) **typescript-automation[bot]** reported user test results showing infrastructure failures but otherwise everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5686691128) **typescript-automation[bot]** shared results of compiling top 400 repos comparing main and the pull request merge and reported everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5692273915) **camc314** noted missing logs and assumed they were fine
 * [today](https://github.com/microsoft/TypeScript/pull/64226#issuecomment-5701182760) **jakebailey** said "The DT runner is currently broken in TS7+, so can be ignored."

### [Issue microsoft/TypeScript#64229](https://github.com/microsoft/TypeScript/issues/64229) (Closed, `Design Limitation`)

**nullish types not narrowed in if block**

*Optional chaining and nullish coalescing conditions do not narrow nullish types within if blocks in TypeScript.*

 * **RyanCavanaugh** added label `Design Limitation`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5666272111) **RyanCavanaugh** observed no generalizable pattern and illustrated with an alternative example
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5667133353) **snarbles2** explained that numeric comparison of null is erroneous and that TypeScript should type-check and error on such cases
 * [today](https://github.com/microsoft/TypeScript/issues/64229#issuecomment-5707002284) **typescript-automation[bot]** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [PR microsoft/TypeScript#64237](https://github.com/microsoft/TypeScript/pull/64237) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Distinguish between non\-distributed and distributed type parameters**

*TypeScript now differentiates distributed and non-distributed type parameters in conditional types, reports constraint violations accordingly, and marks distributed parameters with a (distributed) hover indicator.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642382933) **typescript-automation[bot]** reported user test results comparing main and refs/pull/64237/merge, noted two package install failures and one git clone failure likely unrelated to the change, and confirmed everything else looked good
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5642708165) **typescript-automation[bot]** reported build comparison results for the top 1000 repos between main and pull/64237/merge and highlighted failures in triggerdotdev/trigger.dev
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64237#issuecomment-5668480185) **ahejlsberg** said "Tests are clean. Two top 1000 projects have new errors, but those errors are expected."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64242](https://github.com/microsoft/TypeScript/issues/64242) (Closed, `Needs Investigation`, **andrewbranch**)

**Sporadic \`context canceled\` in \`stderr\` when running TypeScript API in subprocess tests**

*Intermittent 'context canceled' output appears in stderr instead of empty when testing a CLI using TypeScript's API on Ubuntu CI.*

 * (2 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64242#issuecomment-5674451129) **mrazauskas** noted that the issue also surfaced in CI runs of typescript-eslint and linked to the relevant logs
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64246](https://github.com/microsoft/TypeScript/pull/64246) (Closed, `For Milestone Bug`, **andrewbranch**)

**fix\(syncChannel\): give child process time to exit before kill in close\(\)**

*Modify the syncChannel close() method to wait briefly for child processes to exit gracefully before force-killing them.*

 * (2 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Uncommitted Bug`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/pull/64246#issuecomment-5701145851) **andrewbranch** said "Thanks, but fixed a different way in #64276"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64251](https://github.com/microsoft/TypeScript/issues/64251) (Open, `Possible Improvement`)

**Object with all context\-sensitive properties requires at least one non\-context\-sensitive property for inference to work**

*createMachine type inference for context and state fails when all state properties are context-sensitive unless a dummy property is added*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5670374974) **RyanCavanaugh** said "@Andarist any thoughts (on this or the PR) ?"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5670580961) **RyanCavanaugh** said "Copilot cites #48798 as prior work in this area, with #54029 as a superset of the linked PR"
 * [today](https://github.com/microsoft/TypeScript/issues/64251#issuecomment-5703861215) **Andarist** referenced pull request 54029 as a duplicate of the issue, noted it didn't cover all cases, and mentioned preparing a revised PR for TS Go

### [PR microsoft/TypeScript#64269](https://github.com/microsoft/TypeScript/pull/64269) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Refactor requestfilesystem into a stackable layer so it can be used as the top layer above editor overlays**

*Refactor the requestfilesystem API to return a stackable FileSystemLayer so API file changes override editor overlays correctly.*

 * (2 days ago) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64276](https://github.com/microsoft/TypeScript/pull/64276) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Ignore sync api\.close\(\)’s SIGTERM for purposes of error printing and exit status**

*Ignore the SIGTERM signal sent by sync api.close() when determining error output and process exit status.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64279](https://github.com/microsoft/TypeScript/issues/64279) (Closed, **jakebailey**, **Copilot**)

**JSDoc \`@type\` on a function: the type in a type predicate is never checked \(unused \`@import\` reported, missing names not reported\)**

*TypeScript 7.0.2+ erroneously flags imported types used solely in JSDoc @type function type predicates as unused, causing TS6196 errors.*

 * created by **ljharb**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5686218786) **arslivinski** explained that TS 7 JSDoc uses @param and @return for function statements and @type for overloading, and that arrow functions or function expressions can use @type
 * [today](https://github.com/microsoft/TypeScript/issues/64279#issuecomment-5706943362) **jakebailey** said "No, this form should still work, I'm pretty sure."
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript#64282](https://github.com/microsoft/TypeScript/issues/64282) (Closed)

**Dev Container postCreateCommand can hang when npx hereby runs concurrently with npm ci**

*Concurrent postCreateCommand steps can cause npx hereby to hang when npm ci hasn’t completed.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64282#issuecomment-5686190500) **DanielRosenwasser** pointed out that the Herebyfile should list pprof in the tools map and suggested splitting install steps into separate JSON5 entries
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64282#issuecomment-5686292072) **jakebailey** said "You can just do go tool pprof. The only reason to install it separately is to get bugfixes from upstream early."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64282#issuecomment-5688408457) **noamaanMulla-03** updated the branch to split the independent Go dependency setup, removed the separate pprof install in favor of go tool pprof, and offered to raise a PR if acceptable
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64283](https://github.com/microsoft/TypeScript/pull/64283) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update dependencies**

*Update all dependencies to vsce v4 to drop over 150 modules, with an adm-zip CVE fix pending*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64285](https://github.com/microsoft/TypeScript/pull/64285) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Move requestFileSystem into project**

*Move the requestFileSystem API into the project module in a smaller, more concrete refactoring.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#64292](https://github.com/microsoft/TypeScript/pull/64292) (Closed, `For Uncommitted Bug`, **andrewbranch**, **Copilot**)

**Implement Program resolution mode APIs**

*Add and expose Program.getModeForUsageLocation and getModeForResolutionAtIndex APIs in TypeScript with protocol handlers, async/sync/generator support, index resolution, and validation.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64292#issuecomment-5700036435) **Copilot** notified that custom setup steps failed during the Copilot code review run and suggested fixing the configuration and re-requesting a review
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#64296](https://github.com/microsoft/TypeScript/issues/64296) (Closed, `Bug`)

**SEGV nil pointer dereference in tsc/internal/checker/checker\.go**

*TypeScript compiler panics with a nil pointer dereference in checker.go when processing an import declaration conflicting with a type alias.*

 * created by **YuanchengJiang**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64297](https://github.com/microsoft/TypeScript/pull/64297) (Closed, `For Backlog Bug`)

**fix\(64296\): prevent crash when checking merged import aliases**

*Prevent compiler crashes when type checking merged import aliases.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64298](https://github.com/microsoft/TypeScript/pull/64298) (Closed, `For Uncommitted Bug`)

**Fix dev container post\-create command ordering**

*Combine npm ci and npx hereby install-tools in devcontainer, keep Go module and Graphviz separate, and use go tool pprof.*

 * created by **noamaanMulla-03**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64299](https://github.com/microsoft/TypeScript/pull/64299) (Open, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Provide module resolution overrides**

*Provide createModuleResolver API to perform standalone module resolutions with customizable static overrides and fallback logic*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#64300](https://github.com/microsoft/TypeScript/issues/64300) (Open)

**\[TS7 LSP\] Panic on document URI "file://" \(empty path\): vfs: path "tsconfig\.json" is not absolute**

*TypeScript 7 Go LSP panics on a 'file://' URI with an empty path because it expects an absolute tsconfig.json path.*

 * created by **chenxin-yan**
 * [today](https://github.com/microsoft/TypeScript/issues/64300#issuecomment-5706934663) **jakebailey** said "How did you find this? (I can't imagine any client trying to use an empty file URI?)"
 * [today](https://github.com/microsoft/TypeScript/issues/64300#issuecomment-5707036878) **chenxin-yan** described using tsc lsp with Neovim and how vim.lsp.enable auto-attached to buffers with empty names causing the error

### [PR microsoft/TypeScript#64301](https://github.com/microsoft/TypeScript/pull/64301) (Open, `For Uncommitted Bug`)

**Add support for importing JSON modules "as const"**

*Introduce an opt-in importJsonAsConst compiler option to import JSON modules with const-like immutability.*

 * created by **james-pre**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64301#issuecomment-5704686592) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #32063. If you can get it accepted, this PR will have a better chance of being reviewed."

### [PR microsoft/TypeScript#64302](https://github.com/microsoft/TypeScript/pull/64302) (Closed, `Author: Team`, `For Uncommitted Bug`, **weswigham**)

**Add childrenIter method to API nodes**

*Add an async generator-based childrenIter method to API nodes for child traversal.*

 * created by **weswigham**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **weswigham**

### [PR microsoft/TypeScript#64303](https://github.com/microsoft/TypeScript/pull/64303) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Check JSDoc function type predicates**

*Fully validate JSDoc @type function predicate signatures to correctly resolve predicate types and imports.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64304](https://github.com/microsoft/TypeScript/pull/64304) (Open, `For Milestone Bug`)

**Improve error message for accessing instance properties via super**

*Improve error message to clarify that superclass instance properties must be accessed via this instead of super.*

 * created by **raveviner**
 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64304#issuecomment-5709516643) **raveviner** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64305](https://github.com/microsoft/TypeScript/pull/64305) (Closed, `For Uncommitted Bug`)

**perf: avoid duplicate symbol link lookup in \`GetNameTypeOfSymbol\`**

*Remove redundant TryGet call in GetNameTypeOfSymbol to avoid duplicate symbol link lookup and improve performance.*

 * created by **camc314**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64305#issuecomment-5709911469) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64306](https://github.com/microsoft/TypeScript/pull/64306) (Closed, `For Uncommitted Bug`)

**perf: preallocate instantiated symbol table**

*Preallocate the instantiated symbol table to its known size to avoid intermediate reallocations.*

 * created by **camc314**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64306#issuecomment-5710355492) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64307](https://github.com/microsoft/TypeScript/pull/64307) (Open, `For Uncommitted Bug`)

**Normalize distributed type parameters in conditional type relationships**

*Normalize distributed type parameters on both source and target sides in conditional type relationships to resolve asymmetry and fix a regression*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64307#issuecomment-5712772919) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64308](https://github.com/microsoft/TypeScript/issues/64308) (Closed, `Working as Intended`)

**typescript version 7 complains about unused generic type even though version 6 does not**

*TypeScript 7 incorrectly reports an unused generic parameter error in overloaded createRef definitions under noUnusedParameters, unlike version 6.*

 * created by **sudo-barun**
 * [later](https://github.com/microsoft/TypeScript/issues/64308#issuecomment-5715673074) **MartinJohns** said "But.. it is unused. So it's actually a bugfix."
 * [later](https://github.com/microsoft/TypeScript/issues/64308#issuecomment-5716862153) **jakebailey** said "Yes, this is a bug that was noticed in the port."
 * **RyanCavanaugh** added label `Working as Intended`

### [Issue microsoft/TypeScript#64309](https://github.com/microsoft/TypeScript/issues/64309) (Closed)

**Please add android arm64 build target**

*Add support for cross-compiling binaries targeting Android on ARM64 architecture.*

 * created by **mgholam**
 * [later](https://github.com/microsoft/TypeScript/issues/64309#issuecomment-5716848210) **jakebailey** said "This is already done and will be present in the next version. https://github.com/microsoft/typescript-go/pull/4734"
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64310](https://github.com/microsoft/TypeScript/pull/64310) (Open, `For Uncommitted Bug`)

**Normalize distributed type parameters during conditional type inference**

*Normalize distributed type parameters during conditional type inference to address a regression introduced in PR 64237*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64310#issuecomment-5717056601) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

