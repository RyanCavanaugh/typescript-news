# Report for 2026-01-26 (Monday, January 26th, 2026)

9 different users commented on 27 different issues.

## Recommended Actions

 * Response Recommended
    * @ffmiruz asked for confirmation of the approach and provided benchmark data in [microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3805742727)

## Activity Summary

### [Issue microsoft/TypeScript-go#1943](https://github.com/microsoft/TypeScript-go/issues/1943) (Closed, `Needs More Info`, **andrewbranch**)

**\`export \* from …\` sometimes behaves differently in \`tsgo\` than in \`tsc\` or \`tsgo\` LSP**

*tsgo in a private monorepo fails to resolve types re-exported with export * from, whereas tsc and the LSP succeed.*

 * **jakebailey** added label `Needs More Info`
 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1943#issuecomment-3558080586) **chriskrycho** confirmed that the repro worked as expected, reported being stumped, and said they would check on a more recent nightly and follow up
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/1943#issuecomment-3786075256) **andrewbranch** said "@chriskrycho do you ever see this anymore?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1943#issuecomment-3800669239) **chriskrycho** said "I just checked the specific files where this was showing up back in October; seems to have been resolved since then. Closing! Thanks!"
 * (today) **chriskrycho** closed the issue

### [Issue microsoft/TypeScript-go#2243](https://github.com/microsoft/TypeScript-go/issues/2243) (Closed, `Crash`, **sheetalkamat**)

**Crash in incremental**

*Tsgo incremental crashes on a specific branch, temporarily fixed by disabling incremental or switching @typescript/native-preview versions.*

 * **jakebailey** added label `Crash`
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2243#issuecomment-3617927202) **jakebailey** said "I have access to this repo, but will need to reclone and so on..."
 * **RyanCavanaugh** assigned to **sheetalkamat**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2243#issuecomment-3801827440) **jakebailey** said "I don't think this is crashing anymore, on main."
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2243#issuecomment-3801828260) **jakebailey** said "@justinsmid "

### [PR microsoft/TypeScript-go#2370](https://github.com/microsoft/TypeScript-go/pull/2370) (Closed)

**Format options \+ fourslash testing \+ fix formatting bugs**

*Links formatting options to user preferences and JS/TS scoped settings, adds fourslash tests with skip flags, and fixes spacing bugs.*

 * created by **iisaduan**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2383](https://github.com/microsoft/TypeScript-go/issues/2383) (Closed, `Domain: Editor`, **gabritto**)

**LSP: Path suggestion missing \(import/export\)**

*Path completion suggestions for import/export statements are missing in tsgo, unlike in TypeScript 5.9.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3657264640) **besserwisser** asked if there was a list of to-dos
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2383#issuecomment-3657318588) **andrewbranch** said "Yes and no; we have a list of failing/differing tests, and I traced these to a function that was empty except for a code comment."
 * **andrewbranch** unassigned **andrewbranch**
 * **DanielRosenwasser** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Open, `Crash`)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3797205714) **jogibear9988** reported that generated TypeScript files lacked linebreaks and that one file exceeded 1MB
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3797224077) **jakebailey** said "I'm sure we can come up with a better way to do this, this code hasn't been optimized. It was never an issue in the old compiler since strings were already UTF-16."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3798254127) **jogibear9988** noted that adding newlines to codegen reduced compilation to 24 seconds with ts-go and sourcemaps but left the issue unresolved in ts-go, suggested leaving the issue open, and mentioned the largest generated file was a js file
 * [later](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3805742727) **ffmiruz** mentioned wanting confirmation of the approach, noted that iterating over bytes was necessary, suggested checking for ASCII-ness for optimization with a rune fallback, and provided benchmark results

### [Issue microsoft/TypeScript-go#2450](https://github.com/microsoft/TypeScript-go/issues/2450) (Closed, `bug`, **iisaduan**)

**Review ported code from formatter**

*The Go port of the TypeScript formatter omitted retrieving the preceding token's parent before falling back to previousParent.*

 * **weswigham** unassigned **weswigham**
 * (2 weeks ago) **DanielRosenwasser** added label `bug`, and assigned to **iisaduan**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2490](https://github.com/microsoft/TypeScript-go/issues/2490) (Closed, `Crash`, **ahejlsberg**, **Copilot**)

**Completions panic \(nil pointer\) in JSDoc union return type of method with params**

*Completions request causes a nil pointer panic in the language server for JSDoc function types with union return types.*

 * (2 weeks ago) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **ahejlsberg** assigned to **ahejlsberg**, and unassigned **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2510](https://github.com/microsoft/TypeScript-go/pull/2510) (Closed)

**Replace regex\-based HTML entity parsing with handwritten code**

*Replace regex-based HTML entity parsing with custom handwritten code to eliminate regex usage.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2510#issuecomment-3801958698) **jakebailey** said "Yeah, that would match other string values and so on..."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2572](https://github.com/microsoft/TypeScript-go/issues/2572) (Closed, `Crash`, `Needs More Info`, **andrewbranch**)

**no project found for URI: textDocument/foldingRange and textDocument/diagnostic**

*Language server folding range and diagnostic requests fail for vitest.config.ts because it’s not included in any TypeScript project*

 * created by **rubnogueira**
 * **rubnogueira** added label `Crash`
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2572#issuecomment-3800785869) **andrewbranch** requested logs from the textDocument/didOpen request and explained tsconfig resolution with composite projects and overlapping directories
 * **andrewbranch** added label `Needs More Info`

### [Issue microsoft/TypeScript-go#2573](https://github.com/microsoft/TypeScript-go/issues/2573) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**Seems like language server can't keep up with changes made in editor**

*The language server can't keep pace with editor changes, reporting outdated errors until it's restarted.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3790702573) **rubnogueira** noted that the issue was already solved in a previous issue but not in the latest release
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3790986872) **jakebailey** said "That should be in 0.20260122.4."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3794486254) **ilbrando** said "Just saw that is the version I have installed and are experiencing the issue on?"
 * **andrewbranch** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3800595990) **andrewbranch** provided instructions to enable LSP tracing, collect output from both typescript-native-preview channels, and email the logs
 * **andrewbranch** added label `Needs More Info`

### [PR microsoft/TypeScript-go#2577](https://github.com/microsoft/TypeScript-go/pull/2577) (Open)

**Add \-\-release flag to emulate real released binaries, rename release to nodebug**

*Add a --release flag to generate stripped release binaries and rename the release build tag to nodebug.*

 * created by **jakebailey**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3793259156) **rubiesonthesky** said "nodebug seems logical flag, but without context, it’s easy to read it as “node bug” 🐛 probably no harm, just funny coincidence. "
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3793261911) **jakebailey** said they thought the name was funny, couldn't think of a better name, suggested leaving it as release and questioned flipping code in release mode
 * [today](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3800621851) **jakebailey** said "Thinking more, we should have a --nodebug like --noembed, except that aliases another flag too. So, it's probably a bad build tag name and release was fine. Maybe..."

### [Issue microsoft/TypeScript-go#2578](https://github.com/microsoft/TypeScript-go/issues/2578) (Closed, `Crash`)

**panic: runtime error: invalid memory address or nil pointer dereference**

*A nil pointer dereference panic occurs in the MetadataTransformer.injectClassTypeMetadata function when processing class declarations.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2579](https://github.com/microsoft/TypeScript-go/pull/2579) (Closed)

**Fix nil modifier list metadata loc**

*Correct the location metadata for nil modifier lists to ensure accurate modifier handling.*

 * created by **Zzzen**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2579#issuecomment-3794372121) **DanielRosenwasser** said "I guess I don't understand how there are no other tests that run into this."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2580](https://github.com/microsoft/TypeScript-go/issues/2580) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**textDocument/completion runtime error: invalid memory address or nil pointer dereference**

*textDocument/completion handler in the TypeScript-Go language server panics with a nil pointer dereference when computing import statement completions.*

 * created by **sanny-io**
 * **sanny-io** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2580#issuecomment-3803674071) **DanielRosenwasser** provided a minimal repro example for completions at `/*$*/` after a keyword
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2580#issuecomment-3803855923) **sanny-io** thanked the maintainer and apologized for not narrowing down the crash context

### [Issue microsoft/TypeScript-go#2581](https://github.com/microsoft/TypeScript-go/issues/2581) (Open, `Domain: Editor`, **DanielRosenwasser**, **andrewbranch**, **Copilot**)

**Autocomplete incorrectly suggests transitive files from monorepo package**

*VS Code’s TypeScript autocomplete inaccurately includes internal files from a transitive monorepo package during auto-import suggestions.*

 * **ericnorris** added label `Domain: Editor`
 * (yesterday) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **DanielRosenwasser** assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#2583](https://github.com/microsoft/TypeScript-go/issues/2583) (Closed, `duplicate`, **ahejlsberg**)

**tsgo fails to report TS2769 for mutually\-exclusive object overloads**

*tsgo does not report TS2769 for mutually exclusive object overloads while tsc correctly flags the error.*

 * created by **r253hmdryou**
 * (today) **ahejlsberg** added label `bug`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#2584](https://github.com/microsoft/TypeScript-go/pull/2584) (Open, **DanielRosenwasser**, **Copilot**)

**Fix autocomplete suggesting unexported internal files from monorepo packages**

*Update auto-import logic to exclude unexported internal files from monorepo packages that define exports.*

 * (yesterday) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3797320611) **ericnorris** noted that having a version field prevented auto-import from leaking transitive files and suggested investigating allowing an empty version field
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3801288843) **andrewbranch** described expected behavior of module.GetResolvedEntrypoints and GetModuleSpecifier, expressed confusion about package.json version relevance, and requested a thorough investigation of the root cause
 * [today](https://github.com/microsoft/TypeScript-go/pull/2584#issuecomment-3801309418) **andrewbranch** said "@copilot try again"

### [PR microsoft/TypeScript-go#2585](https://github.com/microsoft/TypeScript-go/pull/2585) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 2 directories with 3 updates**

*Bump GitHub Actions dependencies across root and .github/actions/setup-go directories by updating actions/checkout, codeql-action, and actions/cache.*

 * (today) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2586](https://github.com/microsoft/TypeScript-go/pull/2586) (Closed)

**Consistently map reparsed JSDoc nodes in \`GetReparsedNodeForNode\`**

*Track and map reparsed JSDoc node clones to ensure GetReparsedNodeForNode and related checker functions use them for consistent symbol assignment*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2586#issuecomment-3802616759) **DanielRosenwasser** said "@copilot try again"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2586#issuecomment-3802617084) **Copilot** said "@DanielRosenwasser I've opened a new pull request, #2588, to work on those changes. Once the pull request is ready, I'll request review from you."
 * [later](https://github.com/microsoft/TypeScript-go/pull/2586#issuecomment-3805820822) **ahejlsberg** explained that checker methods should guard on nodes and retrieve reparsed nodes when relevant, noting only declaration names and type nodes are reparsed and expression nodes need no remapping

### [PR microsoft/TypeScript-go#2587](https://github.com/microsoft/TypeScript-go/pull/2587) (Closed)

**Module specifier completions**

*Port module specifier completion logic to support relative and non-relative imports while planning future registry-based optimizations.*

 * created by **gabritto**

### [PR microsoft/TypeScript-go#2588](https://github.com/microsoft/TypeScript-go/pull/2588) (Closed, **DanielRosenwasser**, **Copilot**)

**\[WIP\] Consistently map reparsed JSDoc nodes in GetReparsedNodeForNode**

*WIP pull request adds consistent mapping of reparsed JSDoc nodes in GetReparsedNodeForNode and incorporates feedback from PR #2586.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2589](https://github.com/microsoft/TypeScript-go/pull/2589) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in import statement completions**

*Add nil check to prevent nil pointer dereference panic in import statement completions after typing keywords.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2590](https://github.com/microsoft/TypeScript-go/issues/2590) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**Completions crash after \`import\` when statement is preceded by JSDoc**

*Requesting completions immediately after an import statement that follows a JSDoc comment triggers a panic crash.*

 * created by **DanielRosenwasser**
 * (later) **DanielRosenwasser** added label `Crash`, and assigned to **Copilot**, **DanielRosenwasser**

### [PR microsoft/TypeScript-go#2591](https://github.com/microsoft/TypeScript-go/pull/2591) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix crash when completing after import preceded by JSDoc**

*Completion requests after an import preceded by JSDoc comments panic due to node.Pos() including comment trivia.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

