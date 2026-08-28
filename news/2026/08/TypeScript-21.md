# Report for 2026-08-21 (Friday, August 21st, 2026)

14 different users commented on 43 different issues.

## Recommended Actions

 * Response Recommended
    * @el-pendeloco provided testing results indicating diagnostics issue with Helix editor in [microsoft/TypeScript#63928](https://github.com/microsoft/TypeScript/issues/63928#issuecomment-5379757974)

## Activity Summary

### [Issue microsoft/TypeScript#61216](https://github.com/microsoft/TypeScript/issues/61216) (Open, `Suggestion`, `Help Wanted`, `Committed`)

**Support source phase imports**

*Enable TC39 source phase imports in TypeScript to allow importing raw WebAssembly modules directly.*

 * **RyanCavanaugh** added label `Help Wanted`
 * **typescript-automation[bot]** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * (today) **RyanCavanaugh** set milestone to `TypeScript 7.1`, and removed from milestone `TypeScript 5.9.0`

### [Issue microsoft/TypeScript#63560](https://github.com/microsoft/TypeScript/issues/63560) (Closed, `Domain: Performance`, `Possible Improvement`)

**Quadratic duplicate declaration accumulation in intersection constructor properties can crash with RangeError**

*Quadratic accumulation of duplicate declarations in intersection constructor types causes RangeError crashes under diamond inheritance*

 * (8 weeks ago) **RyanCavanaugh** added labels `Domain: Performance`, `Possible Improvement`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63757](https://github.com/microsoft/TypeScript/issues/63757) (Closed, `API Request`, **andrewbranch**, **Copilot**)

**\[7\.0 API\] \- Accessing name on a jsdoc link that does not have a valid name produces sibling node**

*In TypeScript 7.0’s API, invalid JSDoc link names produce a sibling node instead of undefined.*

 * created by **dragomirtitian**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63757#issuecomment-5338133199) **MartinJohns** said "Am I missing something? 7.0 doesn't have an API."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63757#issuecomment-5354498996) **dragomirtitian** mentioned that 7.0 has an unstable nightly API
 * (today) **RyanCavanaugh** added label `API Request`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#63760](https://github.com/microsoft/TypeScript/issues/63760) (Closed, `Not a Defect`)

**Improve tsdoc for sort\(\)**

*Update the TSDoc example for sort() in es5.d.ts to include the returned sorted array output.*

 * created by **advinans-dennis**
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63760#issuecomment-5346949701) **RyanCavanaugh** said "This doesn't seem necessary."
 * [today](https://github.com/microsoft/TypeScript/issues/63760#issuecomment-5377105547) **typescript-automation[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63776](https://github.com/microsoft/TypeScript/issues/63776) (Open, `Experimentation Needed`, **RyanCavanaugh**, **Copilot**)

**Inconsistency involving discriminated union and flatMap**

*flatMap callback returning either InputOp[] or remove-only arrays causes a TypeScript discriminated union inference error*

 * (19 weeks ago) **RyanCavanaugh** unassigned **ahejlsberg**, **Copilot**
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/63776#issuecomment-5351498621) **parched** provided a minimal repro showing TS2322 error under TS 7.0.2 when using flatMap with a union array after upgrading from TS 6 and noted it was fixed by adding a type annotation
 * (today) **RyanCavanaugh** added label `Experimentation Needed`, and assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#63784](https://github.com/microsoft/TypeScript/issues/63784) (Open, `Needs Investigation`, **andrewbranch**)

**Support for \`workspace/diagnostic\` from LSP 3\.17**

*Implement LSP 3.17 workspace/diagnostics to provide reliable project-wide diagnostics without opening each file.*

 * created by **versecafe**
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/63784#issuecomment-5351499305) **jakebailey** expressed support for replacing the experimental enableProjectDiagnostics setting with a request-based LSP system
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#63785](https://github.com/microsoft/TypeScript/issues/63785) (Open, `Bug`)

**Completion does not work for generic type extending tuple or array of all partial type**

*VS Code’s TypeScript completion fails to suggest optional properties in generic functions using tuple parameters combined with mapped Record types.*

 * created by **ishowta**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63787](https://github.com/microsoft/TypeScript/issues/63787) (Open, `Bug`)

**Broken property suggestions due to a successfully contextually typed function**

*When using a contextually typed callback in makeRequest, TypeScript infers QueryParam as unknown and provides incorrect property suggestions.*

 * created by **LukeAbby**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63787#issuecomment-5373865292) **RyanCavanaugh** said "To be clear, the bug here is intellisense not working, not that the typecheck itself is wrong"

### [Issue microsoft/TypeScript#63828](https://github.com/microsoft/TypeScript/issues/63828) (Closed, `API Request`, **andrewbranch**)

**Add API to detect wherever a symbol is readonly**

*Add APIs to TypeScript's type checker for detecting whether a symbol is readonly or optional.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `API Request`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#63880](https://github.com/microsoft/TypeScript/issues/63880) (Closed, `Needs Investigation`, **andrewbranch**)

**feat\(contentmapper\): emit declaration maps for mapped inputs**

*Enable generation of declaration maps for content-mapped files by composing transformed-to-authored source mappings and preserving accurate file naming and coordinates.*

 * (1 week ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63880#issuecomment-5351509912) **andrewbranch** said "This is something I want, and think shouldn’t be too difficult, but I don’t consider it a blocker for merging microsoft/typescript-go#4712."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63888](https://github.com/microsoft/TypeScript/issues/63888) (Closed, `Needs Investigation`, **jakebailey**)

**tsc colours diagnostics when stdout is not a TTY, splitting "error TS2304" and breaking output parsing \(regressed in 6\.0\)**

*TypeScript CLI regressed in v6 by emitting ANSI escapes on non-TTY stdout, splitting "error TS2304" and preventing error detection.*

 * **RyanCavanaugh** added to milestone `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63908](https://github.com/microsoft/TypeScript/pull/63908) (Closed, `For Backlog Bug`)

**Deduplicate repeated declarations on union/intersection properties**

*Deduplicate redundant property declarations in union and intersection types to prevent repeated members.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63908#issuecomment-5365072749) **jakebailey** said "@typescript-bot perf test this faster"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63908#issuecomment-5365073207) **typescript-automation[bot]** reported that the perf test build started and provided links to the build and results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63908#issuecomment-5365255753) **typescript-automation[bot]** posted the requested perf run results with detailed tsc comparison metrics
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63928](https://github.com/microsoft/TypeScript/issues/63928) (Open, `Needs Investigation`, **andrewbranch**)

**LSP server sends no per\-file diagnostics to clients without pull diagnostics support**

*Implement push-based per-file diagnostics for LSP clients without pull support by publishing diagnostics on open, change, and close.*

 * created by **christianvuerings**
 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript/issues/63928#issuecomment-5379757974) **el-pendeloco** mentioned that testing tsc’s LSP in the Helix editor didn’t produce diagnostics beyond tsconfig ones

### [PR microsoft/TypeScript#63930](https://github.com/microsoft/TypeScript/pull/63930) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Restore legacy build output ignores**

*Restore legacy build output ignore settings to streamline switching between Strada and traditional builds.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63931](https://github.com/microsoft/TypeScript/pull/63931) (Open, `Author: Team`, `For Uncommitted Bug`, **gabritto**)

**Support import attributes on ambient modules**

*Adds support for declaring pattern ambient modules with import attributes and resolves imports by matching and selecting the most specific attribute subtype.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **gabritto**
 * **gabritto** added to milestone `TypeScript 7.1`

### [PR microsoft/TypeScript#63935](https://github.com/microsoft/TypeScript/pull/63935) (Closed, `Author: Team`, `For Uncommitted Bug`, **johnfav03**)

** Port \`formatDiagnostics\` and \`formatDiagnosticsWithColorAndContext\`**

*Add and expose formatDiagnostics and formatDiagnosticsWithColorAndContext methods on the TypeScript Program API.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63935#issuecomment-5373011141) **andrewbranch** suggested including source file hashes with diagnostics and noted caveats for tsconfig and declaration map files
 * [today](https://github.com/microsoft/TypeScript/pull/63935#issuecomment-5373100856) **gabritto** apologized for late feedback and suggested adding a mechanism to include file version info for DiagnosticResponses retrieved via parseConfigFile
 * [today](https://github.com/microsoft/TypeScript/pull/63935#issuecomment-5373189179) **andrewbranch** said "Good point, I think my suggestion to use file hashes would handle that case."

### [PR microsoft/TypeScript#63936](https://github.com/microsoft/TypeScript/pull/63936) (Closed)

**Content mappers round 2**

*Complete second-round content mappers by removing protocolVersion, requiring diagnostic codes, allowing overlapping spans, correcting API fields, and eliminating fallback navigation.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript#63940](https://github.com/microsoft/TypeScript/pull/63940) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix TypeScript package major\-minor version**

*Correct hardcoded major-minor TypeScript version literal in declarations to support dtslint’s local TS version detection.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63940#issuecomment-5373900892) **jakebailey** said "Updated to also test the other version, just to be safe for now."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63941](https://github.com/microsoft/TypeScript/pull/63941) (Closed, `Author: Team`, `For Milestone Bug`, **jakebailey**)

**Handle FORCE\_COLOR values like Node**

*Handle FORCE_COLOR environment variable values in the TypeScript CLI the same way Node.js does*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63942](https://github.com/microsoft/TypeScript/issues/63942) (Closed, `Question`)

**\`tsc \-b \-w\` won't catch error on file changed across project**

*The TypeScript build watch mode doesn't detect errors in project references when properties in a dependent file are removed.*

 * created by **Withered-Flower-0422**
 * [today](https://github.com/microsoft/TypeScript/issues/63942#issuecomment-5375395073) **RyanCavanaugh** said "If you're using a solution tsconfig then you need a reference from b to a in order for this to work"
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/63942#issuecomment-5376389390) **Withered-Flower-0422** said "Thanks for the explanation."
 * (today) **Withered-Flower-0422** closed the issue

### [PR microsoft/TypeScript#63943](https://github.com/microsoft/TypeScript/pull/63943) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`\.isReadonlySymbol\(\)\` method**

*Add a .isReadonlySymbol() method to the TypeScript checker API for identifying readonly symbols.*

 * (yesterday) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63943#issuecomment-5365861584) **typescript-automation[bot]** said "The TypeScript team hasn't accepted the linked issue #63828. If you can get it accepted, this PR will have a better chance of being reviewed."
 * **typescript-automation[bot]** assigned to **andrewbranch**

### [Issue microsoft/TypeScript#63946](https://github.com/microsoft/TypeScript/issues/63946) (Closed, `Needs Investigation`, **andrewbranch**)

**LSP Panic: overlay not found for changed file**

*LSP panics with ‘overlay not found for changed file’ when editing WSL files in PhpStorm after upgrading to tsserver v7.*

 * created by **uncaught**
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63946#issuecomment-5373176093) **RyanCavanaugh** said "We need either an LSP log, or some way to repro this in a supported editor (VS, VS Code)"

### [PR microsoft/TypeScript#63947](https://github.com/microsoft/TypeScript/pull/63947) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 7 updates**

*Update seven GitHub Actions dependencies in the root directory to their latest versions.*

 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63948](https://github.com/microsoft/TypeScript/pull/63948) (Open, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix discriminated union inference ordering issue with flatMap**

*Introduce a widened-object-literal flag and relax optional-property checks to resolve discriminated union inference ties with flatMap*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63949](https://github.com/microsoft/TypeScript/issues/63949) (Open, `Bug`)

**\[7\.0 regression\] Type parameter default is ignored when the call sits inside a callback passed to a generic function**

*TypeScript 7.0 ignores default type parameters for calls inside callbacks passed to generic functions, causing type errors.*

 * created by **exoRift**

### [PR microsoft/TypeScript#63950](https://github.com/microsoft/TypeScript/pull/63950) (Open, `Author: Team`, `For Uncommitted Bug`, **gabritto**)

**Add \`createProgram\` to API**

*Introduce createProgram API to build or evolve a TypeScript program from root files, compiler options, and optional old program snapshots.*

 * created by **gabritto**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **gabritto**

### [PR microsoft/TypeScript#63951](https://github.com/microsoft/TypeScript/pull/63951) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use "\.ts" suffixed code action kinds**

*Advertise .ts-suffixed code action kinds such as source.fixAll.ts and update tests to use them.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63951#issuecomment-5374833661) **jakebailey** said "Though, now with content mappers exposing other languages, maybe this is cursed"

### [PR microsoft/TypeScript#63952](https://github.com/microsoft/TypeScript/pull/63952) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix binder race**

*A concurrent data race occurs in Binder.setCommonJSModuleIndicator during call expression binding in TypeScript CI.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63953](https://github.com/microsoft/TypeScript/pull/63953) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update Go dependencies**

*Update Go module dependencies, including unused transitive ones, to satisfy Dependabot requirements.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63954](https://github.com/microsoft/TypeScript/pull/63954) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Replace Quill CLI with focused Mach\-O tool**

*Replace Quill CLI with a minimal Mach-O tool that extracts only entitlement data for security alerts and dependency counts.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63954#issuecomment-5378114581) **jakebailey** said "I missed your approval, I should have just left it the way it was"

### [PR microsoft/TypeScript#63955](https://github.com/microsoft/TypeScript/pull/63955) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**)

**Update README social links from Twitter to X**

*Replace two Twitter references in README.md with X to update the social links.*

 * created by **pratyansh-agrawal**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63955#issuecomment-5378282238) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** assigned to **DanielRosenwasser**

### [PR microsoft/TypeScript#63956](https://github.com/microsoft/TypeScript/pull/63956) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`\.getNonMissingTypeOfSymbol\(\)\` method**

*Add getNonMissingTypeOfSymbol method to TypeScript checker to retrieve symbol types with exact optional property types*

 * created by **mrazauskas**
 * (today) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#63957](https://github.com/microsoft/TypeScript/pull/63957) (Closed, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Add \`hasTrailingComma\` getter in the \`RemoteNodeList\` class**

*Adds a hasTrailingComma getter to the RemoteNodeList class to identify trailing commas.*

 * created by **mrazauskas**
 * (later) **typescript-automation[bot]** added label `For Uncommitted Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#63958](https://github.com/microsoft/TypeScript/issues/63958) (Open, `Bug`)

**Declaration emit: JSDoc @typedef/@callback comments are separated from their synthesized type when preceded by another declaration**

*Declaration emit for JS files misplaces JSDoc @typedef/@callback comments, detaching them from their synthesized types when preceded by another declaration.*

 * created by **Abdullah-Builds**

### [Issue microsoft/TypeScript#63959](https://github.com/microsoft/TypeScript/issues/63959) (Open, `Docs`)

**The new \`\-\-lsp\` flag is not mentioned in \`tsc \-\-help\`'s output**

*The new --lsp flag isn’t listed in tsc --help or tsc --help --all output, making it hard to find.*

 * created by **frou**
 * [later](https://github.com/microsoft/TypeScript/issues/63959#issuecomment-5380994473) **MartinJohns** replied that the release notes contained that information

