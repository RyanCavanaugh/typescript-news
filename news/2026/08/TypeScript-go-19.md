# Report for 2026-08-19 (Wednesday, August 19th, 2026)

5 different users commented on 53 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Closed, `No linked issue`, `Unmigrated PR`)

**Add Yarn PnP support**

*Integrate official Yarn Plug’n’Play support into the TypeScript Go compiler to optimize large-scale monorepo builds.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4905614254) **proyectoramirez** said "What is a good way to try this PR in a yarn project?"
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-4926997057) **GGomez99** suggested cloning the repository and following the How to build and run section of the contributing doc
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-5351585811) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3297](https://github.com/microsoft/TypeScript-go/pull/3297) (Closed, `No linked issue`, `Unmigrated PR`, **weswigham**)

**Allow global Symbol computed names during pseudochecker object literal serialization**

*Support global Symbol computed property names in pseudochecker object literal serialization to match Strada’s behavior.*

 * (10 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **weswigham**
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3297#issuecomment-5351586092) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3331](https://github.com/microsoft/TypeScript-go/pull/3331) (Closed, `Unmigrated PR`)

**Use trie for removeStringLiteralsMatchedByTemplateLiterals**

*Adopt a trie-based implementation for removeStringLiteralsMatchedByTemplateLiterals to resolve TypeScript issue 63342.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5297608752) **typescript-automation[bot]** started build jobs and posted status and results links
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5297880991) **typescript-automation[bot]** posted perf run results for the requested tsc performance comparison
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5351586367) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/3331#issuecomment-5353633973) **eps1lon** said "@jakebailey  Continued in https://github.com/microsoft/TypeScript/pull/63900"

### [PR microsoft/TypeScript-go#3362](https://github.com/microsoft/TypeScript-go/pull/3362) (Closed, `Unmigrated PR`)

**Replace most ID usage with pointers**

*Propose replacing most ID fields with pointers in Go to leverage pointer comparability and reduce overhead.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870100315) **typescript-automation[bot]** reported that performance tests had started and provided links to build status and results
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-4870283060) **typescript-automation[bot]** reported the performance comparison results for the requested perf run
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3362#issuecomment-5351586616) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3369](https://github.com/microsoft/TypeScript-go/pull/3369) (Closed, `No linked issue`, `Unmigrated PR`)

**Limit loader/emitter to GOMAXPROCS**

*Limit parsing and emitting workloads to a GOMAXPROCS-sized goroutine pool to prevent unbounded concurrency and stack growth.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847634796) **typescript-automation[bot]** reported that performance test jobs started and provided links to build status and results
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-4847820197) **typescript-automation[bot]** provided the perf run results as requested
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3369#issuecomment-5351586867) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3385](https://github.com/microsoft/TypeScript-go/pull/3385) (Closed, `Unmigrated PR`)

**Restore CommaListExpression support**

*Proposal to restore the CommaListExpression optimization removed in PR #3367 that prevented excessively nested comma binary expressions.*

 * created by **jakebailey**
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3385#issuecomment-5351587151) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3619](https://github.com/microsoft/TypeScript-go/pull/3619) (Closed, `No linked issue`, `Unmigrated PR`)

**perf: Make \`NodeArray\` no longer inherit from \`Array\`**

*Detach NodeArray from Array prototype to prevent direct array method usage and achieve significant performance gains.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-5296902234) **jakebailey** said "Is this still needed? Did we end up doing this another way?"
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-5297822444) **andrewbranch** described making improvements to preserve array element access while noting the proposal still performs better but sacrifices direct indexing
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3619#issuecomment-5351587435) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3690](https://github.com/microsoft/TypeScript-go/pull/3690) (Closed, `Unmigrated PR`)

**fix: handle symlink workspace roots in project reference redirects**

*Ensure project reference redirects correctly resolve symlinked workspace roots in TypeScript*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/3690#issuecomment-5321197739) **jakebailey** described asking Copilot locally to implement the parent directory realpath cache, noted it worked well, and suggested reopening on the main TS repo if this repo closes first
 * **jakebailey** added label `Unmigrated PR`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3690#issuecomment-5332256532) **jakebailey** shared a diff patch that added a realpathDirectoryCache field to projectReferenceParser and initialized it in initMapper
 * [today](https://github.com/microsoft/TypeScript-go/pull/3690#issuecomment-5351587684) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3726](https://github.com/microsoft/TypeScript-go/pull/3726) (Closed, `Unmigrated PR`, **DanielRosenwasser**, **Copilot**)

**Preserve original stack traces in cross\-project panic handling**

*Add PanicWithStack to wrap and re-panic panics with their original stack traces in cross-project goroutine recovery for accurate logging.*

 * (5 days ago) **jakebailey** closed the issue
 * (5 days ago) **jakebailey** reopened the issue
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3726#issuecomment-5351587929) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3728](https://github.com/microsoft/TypeScript-go/pull/3728) (Closed, `No linked issue`, `Unmigrated PR`)

**Fix keyof deferred for non\-generic substitution types \(\#2186\)**

*Resolve keyof immediately for non-generic substitution types instead of deferring, fixing indexed access assignability and quick info.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298657492) **typescript-automation[bot]** reported performance run results for the requested baseline..pr comparison, including errors, symbols, types, memory usage, and memory allocations
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5298948718) **typescript-automation[bot]** reported that everything looked good after comparing main and the pull request across the top 400 repositories with tsc
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3728#issuecomment-5351588203) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3935](https://github.com/microsoft/TypeScript-go/pull/3935) (Closed, `No linked issue`, `Unmigrated PR`)

**Narrow keyword completions for concise arrow expression bodies**

*Port keyword completion filtering to Go so concise arrow function bodies only suggest expression keywords.*

 * **RyanCavanaugh** added label `No linked issue`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/3935#issuecomment-5298337051) **jakebailey** said "I think this PR would have been fine, had it added a test for what it was trying to do."
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3935#issuecomment-5351588426) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3943](https://github.com/microsoft/TypeScript-go/pull/3943) (Closed, `No linked issue`, `Unmigrated PR`)

**Fix crash inferring constrained variadic tuples with optional elements**

*Fix compiler crash during inference of constrained variadic tuples with optional elements*

 * (10 weeks ago) **RyanCavanaugh** added label `Unmigrated PR`, set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3943#issuecomment-5351588701) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3996](https://github.com/microsoft/TypeScript-go/pull/3996) (Closed, `No linked issue`, `Unmigrated PR`)

**Extract tscInput tests to individual per\-scenario files with imperative edits to improve debuggability**

*Extract tscInput tests into individual scenario files with imperative edits, remove intra-test parallelism, simplify debugging while preserving original tests.*

 * (11 weeks ago) **RyanCavanaugh** added labels `No linked issue`, `Unmigrated PR`, and set milestone to `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3996#issuecomment-5351588981) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4102](https://github.com/microsoft/TypeScript-go/pull/4102) (Closed, `Unmigrated PR`)

**Cache alias candidates for symbol accessibility**

*Cache alias candidate symbols to speed up symbol accessibility checks*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298328172) **typescript-automation[bot]** posted a build status update with job start and result links
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5298557303) **typescript-automation[bot]** provided the requested performance run results in a detailed report
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4102#issuecomment-5351589210) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4197](https://github.com/microsoft/TypeScript-go/pull/4197) (Closed, `No linked issue`, `Unmigrated PR`)

**prevent bundled library paths from being watched in resolution lookup**

*Skip watching embedded bundled library paths in resolution lookup glob patterns while still including real library directories.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4197#issuecomment-4696402624) **RyanCallahan312** tracked down the issue to a project using Effect-TS/tsgo and decided to disable neovim's workspace.didChangeWatchedFiles.dynamicRegistration as the solution
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4197#issuecomment-4696430103) **jakebailey** said "They're patching us and then shipping the code? If so, they really need to ship us properly."
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4197#issuecomment-5351589443) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4200](https://github.com/microsoft/TypeScript-go/pull/4200) (Closed, `Unmigrated PR`)

**Negated Types**

*Introduce 'not T' negated types to capture type complements and preserve conditional false-branch information for improved control flow analysis.*

 * created by **weswigham**
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4200#issuecomment-5351589702) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4211](https://github.com/microsoft/TypeScript-go/pull/4211) (Closed, `Unmigrated PR`)

**Optimize bin by replacing node\_modules/\.bin/tsgo with a symlink**

*Use symlinks instead of shims for node_modules/.bin/tsgo to improve startup performance.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4211#issuecomment-4638058619) **JoostK** proposed spawning native tsgo before attempting optimization to avoid unnecessary optimizeBin overhead, noted this isn’t feasible with process.execve not forking, and questioned whether the overhead is significant
 * [10 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4211#issuecomment-4638069692) **JoostK** suggested invoking tsgo with an --optimize-bin flag to move optimization into the native binary, but noted it was probably not worth it
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4211#issuecomment-5351590033) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4297](https://github.com/microsoft/TypeScript-go/pull/4297) (Closed, `Unmigrated PR`)

**Push per\-file diagnostics for clients without pull diagnostics support**

*Implement per-file push diagnostics for clients with publishDiagnostics but no pull support, sending open/change/close updates without affecting pull-capable clients.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4297#issuecomment-4744853071) **christianvuerings** asked @jakebailey to take a look at the PR and noted that Claude code didn't support pull diagnostics and TypeScript Go didn't support push diagnostics
 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4297#issuecomment-4745627690) **jakebailey** said "We haven't had time to test it; we'd have to disable pull diags and test in VS Code and make sure it works. Push diagnostics get tricky when dealing with LS restarts and other racy ish conditions."
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4297#issuecomment-5351590270) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4418](https://github.com/microsoft/TypeScript-go/pull/4418) (Closed, `Unmigrated PR`)

**Infer void for statement\-less function bodies in \`isolatedDeclarations\` syntactic inference**

*Syntactically infer void return types for statement-less functions to avoid isolatedDeclarations errors.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-4984582065) **andrewbranch** recalled that they omitted this originally to allow room for future design changes around issue 42709 without breaking third-party isolatedDeclarations emitters
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-4984961465) **weswigham** considered that changing the inference would require updating the isolatedDeclarations rule and wouldn't be worse for third-party emitters or preclude future changes
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4418#issuecomment-5351590464) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4422](https://github.com/microsoft/TypeScript-go/pull/4422) (Closed, `Unmigrated PR`)

**Use auto\-imports for \`isolatedDeclarations\` fixes**

*Add auto-import suggestions for fixes applied to code under the isolatedDeclarations setting.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5333889443) **DanielRosenwasser** said "@copilot make sure build/test/format is clean and working."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5334043216) **Copilot** confirmed build, test, and lint passed, noted formatting check failure due to DNS blockage in sandbox, verified Go formatting compliance with gofmt and gofumpt
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4422#issuecomment-5351590704) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4440](https://github.com/microsoft/TypeScript-go/pull/4440) (Closed, `Unmigrated PR`, **andrewbranch**)

**API: add getChildren and token getters to Node**

*Extend the Node API with getChildren, getChildCount, getChildAt, getFirstToken, and getLastToken methods.*

 * created by **oMatheusmol**
 * **jakebailey** assigned to **andrewbranch**
 * **andrewbranch** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4440#issuecomment-5351590925) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4446](https://github.com/microsoft/TypeScript-go/pull/4446) (Closed, `Unmigrated PR`)

**fix: Corsa differences in \`export=\` module augmentation**

*Corsa’s emit-phase visibility marking skips export= namespaces, leaving type T invisible and causing a false TS4060 error.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4804157001) **typescript-automation[bot]** reported the requested performance run results for tsc comparing baseline and PR
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-4804369952) **pratheeknathani** pushed a commit removing a stale submoduleTriaged.txt entry to fix CI failures and verified tests locally
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4446#issuecomment-5351591142) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4496](https://github.com/microsoft/TypeScript-go/pull/4496) (Closed, `Unmigrated PR`)

**fix\(lsp\): support TypeScript source action kinds**

*Advertise and support TypeScript-specific source action kinds suffixed with .ts in the LSP server while maintaining generic kinds for backward compatibility.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-4848251335) **TorinAsakura** rechecked vscode and explained that the PR targets multi-server LSP scenarios rather than matching the current extension and wires actual handling to support generic source.removeUnusedImports as an escape hatch for clients
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5321335781) **jakebailey** observed that only the TypeScript language server and similar JS tools add these suffixes, while pyright/pylance, gopls, and rust-analyzer do not
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5333253192) **TorinAsakura** asked where to land with the PR and suggested using .ts
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5347350532) **jakebailey** suggested simplifying the implementation by stripping the `.ts` prefix and exposing `.ts` names, noted the imminent repo move, and offered to reopen the PR on the main TS repo or implement it himself
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5347874870) **TorinAsakura** explained the need to preserve the .ts suffix and described how the PR handles it, then asked for either a concrete alternative or a decision to accept the current implementation or move the issue to the main TypeScript repo
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5347889994) **jakebailey** said "Are you an agent, or are you pasting agent output into the comments? ☹️ "
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5349389853) **TorinAsakura** expressed annoyance at the other user’s requests and complained about unclear expectations
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5349412211) **TorinAsakura** clarified that he was Russian and used a translator for complex thoughts, and asked to focus on solving problems instead of criticizing his writing
 * [today](https://github.com/microsoft/TypeScript-go/pull/4496#issuecomment-5351591373) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4555](https://github.com/microsoft/TypeScript-go/pull/4555) (Closed, `Unmigrated PR`, **andrewbranch**)

**Add batched version for several API functions\.**

*Add batched versions of several API functions to reduce IPC overhead and improve performance.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4555#issuecomment-5134149432) **weswigham** explained that using a single checker/LS instance for the whole batch caches diagnostics and negates benefits of a bespoke entrypoint
 * **jakebailey** assigned to **andrewbranch**
 * **andrewbranch** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4555#issuecomment-5351591597) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4596](https://github.com/microsoft/TypeScript-go/pull/4596) (Closed, `Unmigrated PR`)

**Fixed mapped types not being considered as homomorphic with substitution constraints**

*Mapped types are now correctly recognized as homomorphic when using substitution constraints in TypeScript.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5334725057) **jakebailey** said "Hmmmm, this is a break?"
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5340259588) **Andarist** explained that distributive homomorphic types require a specific mapped type form, demonstrated a repro case, noted that the PR fix changed behavior and broke type-fest’s implementation, added tests and workarounds, and offered to submit a type-fest fix once merged
 * [today](https://github.com/microsoft/TypeScript-go/pull/4596#issuecomment-5351591798) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4597](https://github.com/microsoft/TypeScript-go/pull/4597) (Closed, `Unmigrated PR`)

**Normalize \`NoInfer\`red tuple types in rest/spread positions**

*Normalize NoInferred tuple types used in rest and spread operations to resolve related TypeScript inference issues.*

 * created by **Andarist**
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4597#issuecomment-5351592179) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4600](https://github.com/microsoft/TypeScript-go/pull/4600) (Closed, `Unmigrated PR`)

**Deduplicate repeated declarations on union/intersection properties**

*Remove duplicate property declarations from union and intersection types.*

 * created by **Andarist**
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4600#issuecomment-5351592428) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4653](https://github.com/microsoft/TypeScript-go/pull/4653) (Closed, `Unmigrated PR`)

**Error with a suggestion of '\.' for empty project reference paths**

*A new TS18052 diagnostic reports empty project reference paths and suggests using '.' instead of the generic TS18051 error.*

 * created by **KlyneChrysler**
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4653#issuecomment-5351592624) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4666](https://github.com/microsoft/TypeScript-go/pull/4666) (Closed, `Voight-Kampff Anomaly`, `Unmigrated PR`)

**POC: ambient module declarations keyed on import attributes**

*Proof-of-concept for ambient module declarations keyed by import attributes to support text or bytes file imports in TypeScript's Go port.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4666#issuecomment-5004893772) **bartlomieju** said "@microsoft-github-policy-service agree"
 * (1 month ago) **RyanCavanaugh** added labels `Voight-Kampff Anomaly`, `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4666#issuecomment-5351592854) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4674](https://github.com/microsoft/TypeScript-go/pull/4674) (Closed, `Voight-Kampff Anomaly`, `Unmigrated PR`)

**Preserve JSDoc @property comments when reconstructing typedef types**

*Ensure JSDoc @property comments on typedefs are preserved when tsgo inlines types into declaration files*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/pull/4674#issuecomment-5016285782) **veksa** said "@microsoft-github-policy-service agree"
 * (1 week ago) **RyanCavanaugh** added labels `Voight-Kampff Anomaly`, `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4674#issuecomment-5351593064) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Closed)

**Content mappers**

*Implement content mappers that enable TypeScript to include unsupported file types by transforming them via tsconfig settings.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5334123430) **escaton** challenged the given safety examples, arguing that any CLI command is risky regardless of flags and noting that agents would simply re-run commands with the --runExternalCode flag
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5334280074) **andrewbranch** asserted that running tsc on untrusted code is safe since it doesn’t execute code, contrasted it with npm install and the unsafe --runExternalCode flag, and described plans for a diagnostic to require human acknowledgment for agent scenarios
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5339365820) **remcohaszing** appreciated the explanation of security considerations and suggested adding a shorthand option '-x' for execute external
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4716](https://github.com/microsoft/TypeScript-go/pull/4716) (Closed, `Unmigrated PR`)

**Restore Strada\-style escaped symbol names**

*Revert to Strada-style symbol name escaping and benchmark its performance and usability for valid string serialization.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059239589) **typescript-automation[bot]** reported that performance tests started and provided status links
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5059531138) **typescript-automation[bot]** reported the perf run results requested by jakebailey
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4716#issuecomment-5351593335) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4722](https://github.com/microsoft/TypeScript-go/issues/4722) (Closed, `bug`, **jakebailey**, **Copilot**)

**Nested nullish coalescing \+ comment \+ ES2018 causes function body to be ignored**

*Transpiling nested nullish coalescing with comments targeting ES2018 misplaces the return statement causing function body to be ignored*

 * (3 weeks ago) **RyanCavanaugh** added label `bug`, and set milestone to `TypeScript 7.1`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4722#issuecomment-5243143457) **smerrill** apologized for opening a duplicate issue and clarified that a single level of optional chaining triggers the issue
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4723](https://github.com/microsoft/TypeScript-go/pull/4723) (Closed, **jakebailey**, **Copilot**)

**Preserve comments when downleveling arrow expression bodies**

*Adjust arrow function downleveling to preserve comment placement by applying original source ranges to synthesized return statements.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5318108076) **jakebailey** said "You're definitely right, but Strada double sets too: https://github.com/microsoft/TypeScript/blob/5848bc5157b22ff7f4e3369f4645a514a433b15f/src/compiler/factory/nodeConverters.ts#L54-L60"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5334711884) **jakebailey** said "@copilot+gpt-5.6-sol Please address the above :)"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4723#issuecomment-5334941134) **Copilot** addressed suggestions in commits aca5f3b0 and 70c3165f, shared ConvertToFunctionBlock between VisitFunctionBody and the async transform while preserving async-only node attribution, and covered the regression test case in commit de6d68f6 with verbatim inclusion and comment placement validation
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4726](https://github.com/microsoft/TypeScript-go/pull/4726) (Closed, `Unmigrated PR`)

**Skip declaration emit without a prior signature**

*Skip emitting TypeScript declaration files for declarations that lack an existing signature*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297615606) **typescript-automation[bot]** reported that the performance test job started and provided status and results links
 * [5 days ago](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5297865842) **typescript-automation[bot]** posted the performance run results for the requested comparison
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4726#issuecomment-5351593554) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4733](https://github.com/microsoft/TypeScript-go/pull/4733) (Closed, `Unmigrated PR`)

**Add wasip1 npm build target**

*Adds a wasip1-based NPM build target for tsc.wasm that omits lib.d.ts bundling and relies on external file mounting*

 * created by **jakebailey**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4733#issuecomment-5073968665) **jakebailey** said "wasip1 lacks os.Executable, so this breaks, currently."
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4733#issuecomment-5351593777) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4779](https://github.com/microsoft/TypeScript-go/pull/4779) (Closed, `Unmigrated PR`)

**Fix incremental builder re\-emitting entire import closure on non\-shape\-changing edits**

*Incremental builder computes real .d.ts signatures on fresh builds to avoid re-emitting full import closures on non-shape-changing edits.*

 * created by **johnfav03**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4779#issuecomment-5243834859) **jakebailey** said "Eagerly doing dts emit seems scary, but I don't quite know if I can tell if that gut feeling is wrong or not"
 * **johnfav03** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4779#issuecomment-5351594028) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4841](https://github.com/microsoft/TypeScript-go/pull/4841) (Closed, `Unmigrated PR`, **weswigham**)

**Fix false\-positive TS2354 for native private class field access with importHelpers at dated targets**

*With importHelpers enabled and a dated ECMAScript target, the Go port of TypeScript wrongly reports TS2354 on native private class field access.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4841#issuecomment-5209140467) **astegmaier** noted that the PR contained the discussed bug fix and disclosed that the reproduction was hand-crafted while the PR itself was agent-generated
 * **RyanCavanaugh** assigned to **weswigham**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4841#issuecomment-5222455672) **astegmaier** verified a regression, pushed a fix restoring the check for native class decorators with static private/auto-accessor elements, retained the original improvements, and added three new tests
 * **RyanCavanaugh** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4841#issuecomment-5351594266) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4846](https://github.com/microsoft/TypeScript-go/pull/4846) (Closed, `Unmigrated PR`)

**Fix crash when a call signature's type parameter cannot be reused**

*TypeScript Go printer crashes when reuseNode fails and inserts a nil type parameter into a call signature.*

 * **RyanCavanaugh** added label `Unmigrated PR`
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5334713140) **weswigham** said "Rough, looks like some semantic merge conflicts with main. This might have to get reopened post repo migration."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5340578727) **nikeedw** reported pushing a fix that reduced TS2527 errors, updated the baseline, and requested a CI approval run
 * [today](https://github.com/microsoft/TypeScript-go/pull/4846#issuecomment-5351594601) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4858](https://github.com/microsoft/TypeScript-go/pull/4858) (Closed, `Unmigrated PR`)

**Keep JSDoc on expando hosts declared as arrows or function expressions**

*JSDoc on expando hosts declared as arrow functions or function expressions is omitted in generated .d.ts files.*

 * created by **yogesh968**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4858#issuecomment-5333573893) **jakebailey** said "We can't really do anything with this unless the CLA is signed"
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4858#issuecomment-5351594879) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4865](https://github.com/microsoft/TypeScript-go/pull/4865) (Closed, `Unmigrated PR`)

**Avoid expensive incremental reconciliation after dependency paths move**

*Detect moved dependency paths in the TypeScript compiler's incremental builds and perform a cold-build snapshot to avoid expensive reconciliation.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4865#issuecomment-5243653489) **jakebailey** asked to split the changes into two commits and expressed uncertainty about the heuristic approach
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4865#issuecomment-5244367310) **johnfav03** split the changes into two commits and explained that the pre-fix baseline forced .d.ts computation and signature updates while the post-fix cold-build baseline showed no signature reconciliation
 * **johnfav03** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4865#issuecomment-5351595084) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4877](https://github.com/microsoft/TypeScript-go/pull/4877) (Closed)

**Gate ES2025 regex syntax behind target**

*Compiler enforces ES2025 regex syntax gating for the 'v' flag and duplicate named capture groups based on target.*

 * **RyanCavanaugh** added label `Unmigrated PR`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4877#issuecomment-5322215945) **dayongkr** said "@jakebailey license/cla has been stuck in pending and never reported back. (CLA is signed on my end)"
 * (2 days ago) **jakebailey** closed the issue
 * **jakebailey** removed label `Unmigrated PR`

### [Issue microsoft/TypeScript-go#4899](https://github.com/microsoft/TypeScript-go/issues/4899) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Crash at \`GetSourceFilePathInNewDir\`**

*TypeScript 7.0.2 unexpectedly crashes in GetSourceFilePathInNewDir during program creation with no reproducible steps.*

 * (6 days ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4900](https://github.com/microsoft/TypeScript-go/pull/4900) (Closed, **DanielRosenwasser**, **Copilot**)

**Prevent crash when computing emit output paths**

*Prevent panics in computing emit output paths by delegating to a canonical prefix-based worker and removing invalid containment checks*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5336656981) **DanielRosenwasser** said "@typescript-bot perf test this"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5336657446) **typescript-automation[bot]** announced that the 'perf test this' job started and provided status and results links
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5336853630) **typescript-automation[bot]** reported the requested performance run results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5346322717) **jakebailey** said "@weswigham Do you have any last comments on this?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4900#issuecomment-5347619058) **weswigham** identified two additional occurrences in the PR and suggested a systemic bounds-checking issue with string slices
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4902](https://github.com/microsoft/TypeScript-go/pull/4902) (Closed, `Unmigrated PR`)

**Fix transpile test diffs**

*Urgently fix the newly introduced transpile test diffs before they are deleted.*

 * created by **jakebailey**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4902#issuecomment-5320675150) **jakebailey** said "I'm not confident enough at this stage. I don't like that we will lose the diffs but we can just do some trickery I guess in a separate PR to try and fix the bugs."
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4902#issuecomment-5351595304) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4903](https://github.com/microsoft/TypeScript-go/pull/4903) (Closed, `Unmigrated PR`)

**Remove AST node self pointers**

*Remove self-referencing pointers from AST nodes now that unsafe code is confined to generated code.*

 * **jakebailey** added label `Unmigrated PR`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5317644096) **DanielRosenwasser** said "I wonder why the compiler self builds seem to use more memory, and why xstate still gets slower in checking."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5317984406) **jakebailey** said "Yeah, those are the primary problems"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4903#issuecomment-5351595515) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4911](https://github.com/microsoft/TypeScript-go/pull/4911) (Closed, `Unmigrated PR`)

**Better handle signals in tsc CLI**

*Enhance the TypeScript compiler CLI to properly handle operating system signals and interruptions*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321296935) **lukesandberg** said "I don't have permissions to open PRs anymore"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321319271) **jakebailey** said "If you restore the branch in microsoft/typescript-go#4592, I can reopen it"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5321374632) **lukesandberg** mentioned that the commit was on a different branch and suggested cherry-picking it
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5346136703) **jakebailey** said "I'm going to just defer this until after the repo move."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4911#issuecomment-5351595712) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4914](https://github.com/microsoft/TypeScript-go/pull/4914) (Closed, `Unmigrated PR`)

**createProgram**

*Introduce a createProgram API that constructs or incrementally updates TypeScript programs using snapshots and optional oldProgram changes.*

 * created by **gabritto**
 * **gabritto** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4914#issuecomment-5351595944) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4915](https://github.com/microsoft/TypeScript-go/pull/4915) (Closed)

**Generate TS API from Go source**

*Auto-generate a strongly typed TypeScript API client by parsing Go Session HandleRequest methods and custom annotations*

 * created by **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4915#issuecomment-5346337816) **jakebailey** said "How do we want to reconcile this and #4712; that PR first?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4915#issuecomment-5346371385) **jakebailey** said "Can we wait to do this after the repo move?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4915#issuecomment-5347663386) **weswigham** offered to merge and regenerate the API, noted potential need for extra annotations, and suggested that @andrewbranch review before merging
 * [today](https://github.com/microsoft/TypeScript-go/pull/4915#issuecomment-5347680751) **jakebailey** said "If you can be quick then yeah we can do this now!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4915#issuecomment-5347692727) **weswigham** said "Content mappers doesn't actually add any new API endpoints so... maybe no merge conflicts? Let's find out."
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4917](https://github.com/microsoft/TypeScript-go/pull/4917) (Closed)

**Fix test:api on windows**

*Inline the npm test command in Herebyfile.mjs to fix Windows globbing issues and restore API tests.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#4918](https://github.com/microsoft/TypeScript-go/issues/4918) (Open)

**This Repo Has Moved\!**

*The repository has moved back to microsoft/typescript and contributors must reopen their pull requests there.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/4918#issuecomment-5351547813) **RyanCavanaugh** noted that issue and PR creation were disabled due to an upcoming repo move and instructed users to file bugs in the TypeScript repo and hold off on PRs
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4918#issuecomment-5351547844) **jakebailey** explained that the git history will be replayed into the TypeScript repo inside a subdirectory preserving blame and authorship, noted that unmerged code will need manual reapplication and that releases will resume after internal approvals to unblock patch releases
 * [today](https://github.com/microsoft/TypeScript-go/issues/4918#issuecomment-5351547869) **RyanCavanaugh** said "It's done! Open issues will be moved over now, and open PRs will be closed."

### [PR microsoft/TypeScript-go#4919](https://github.com/microsoft/TypeScript-go/pull/4919) (Closed)

**Add closure notice and link to original repo**

*Add a closure notice with archival information and a link to the original repository.*

 * created by **RyanCavanaugh**
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#717](https://github.com/microsoft/TypeScript-go/pull/717) (Closed, `Unmigrated PR`)

**Enable staticcheck**

*Enabling the staticcheck linter raises linting time dramatically, prompting performance investigation and reporting.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript-go/pull/717#issuecomment-3475151354) **jakebailey** said "Perf of this is still pretty bad. A lint run on main in CI takes about 30s, but on this branch takes 4m44s."
 * **RyanCavanaugh** added to milestone `Possible Improvement`
 * **jakebailey** added label `Unmigrated PR`
 * [today](https://github.com/microsoft/TypeScript-go/pull/717#issuecomment-5351585560) **RyanCavanaugh** explained that development moved to the main microsoft/TypeScript repository, closed the PR due to lack of transfer functionality, and asked to reopen the change there
 * (today) **RyanCavanaugh** closed the issue

