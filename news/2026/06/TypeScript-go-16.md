# Report for 2026-06-16 (Tuesday, June 16th, 2026)

12 different users commented on 28 different issues.

## Recommended Actions

 * Response Recommended
    * @mrazauskas asked to link to issue #2851 in [microsoft/TypeScript-go#4337](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4726236305)
    * @JoostK reported using .map() failed and that overriding map implementation prevented the issue, suggesting iterator corruption in [microsoft/TypeScript-go#4339](https://github.com/microsoft/TypeScript-go/issues/4339#issuecomment-4721657493)

## Activity Summary

### [Issue microsoft/TypeScript-go#4244](https://github.com/microsoft/TypeScript-go/issues/4244) (Open, `Crash`, `Needs More Info`, **DanielRosenwasser**, **Copilot**)

**Fatal server error: nil Session from \`flushChangesLocked\(\)\`**

*Server crashes with a fatal nil pointer dereference in Session.flushChangesLocked caused by an unexpected nil session.*

 * **DanielRosenwasser** added label `Crash`
 * (1 week ago) **RyanCavanaugh** added label `Needs More Info`, and set milestone to `Post-7.0`
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#4289](https://github.com/microsoft/TypeScript-go/issues/4289) (Closed, **jakebailey**, **Copilot**)

**diagnostics APIs position uses UTF\-8 encoding**

*IPC diagnostics APIs return positions in UTF-8, whereas AST and completion APIs use UTF-16 mapping, causing inconsistency.*

 * created by **jasonlyu123**
 * (4 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4305](https://github.com/microsoft/TypeScript-go/pull/4305) (Open, `dependencies`, `javascript`)

**Bump esbuild from 0\.28\.0 to 0\.28\.1**

*Update esbuild to 0.28.1 to prevent backslash-based path traversal and add integrity checks to the Deno API*

 * (4 days ago) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4308](https://github.com/microsoft/TypeScript-go/pull/4308) (Open)

**API: add the missing position and text getters to Node**

*Add missing position and text getters to the API Node implementation and include tests for them.*

 * created by **oMatheusmol**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4312](https://github.com/microsoft/TypeScript-go/pull/4312) (Closed)

**API: add Signature implementation and improve object caching on client side**

*Implement missing Signature properties and optimize client-side object caching in the API.*

 * created by **piotrtomiak**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4312#issuecomment-4707868740) **piotrtomiak** added implementation for Signature properties, refactored object id handling to fetch objects by id with local caching, and changed omitempty to omitzero to skip empty id handles
 * [today](https://github.com/microsoft/TypeScript-go/pull/4312#issuecomment-4716579778) **piotrtomiak** updated the PR to avoid registering each object sent to the client, retained SnapshotObjectRegistry wiring, added a Signature id field on the Go side, and cleaned up handlers by extracting common methods
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4313](https://github.com/microsoft/TypeScript-go/pull/4313) (Open)

**Assign checkers with import\-aware algorithm**

*Use an import-aware algorithm to assign files to checkers, reducing check time, memory use, and allocations.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4700283231) **jakebailey** said "@typescript-bot perf test this faster"
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4700283391) **typescript-automation[bot]** reported that the perf test started with links to status and results
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4700327043) **typescript-automation[bot]** notified that the requested perf run results were available and included a comparison report
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4723994531) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4723995071) **typescript-automation[bot]** posted a build status update with a table of command status and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4724128046) **typescript-automation[bot]** reported the results of the requested performance run
 * [today](https://github.com/microsoft/TypeScript-go/pull/4313#issuecomment-4724162463) **jakebailey** said "Weird. Simplifying the algorithm to just use text made it a lot worse in time?"

### [Issue microsoft/TypeScript-go#4316](https://github.com/microsoft/TypeScript-go/issues/4316) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**Consider adding \`\.getSourceFile\(\)\` to \`Diagnostic\`**

*Add a .getSourceFile() getter to Diagnostic to retrieve its SourceFile directly instead of passing program context*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4316#issuecomment-4724825055) **andrewbranch** expressed concerns about Diagnostic storing project references leading to stale data and memory leaks, and suggested treating Diagnostics as plain data to balance convenience and resource management
 * [today](https://github.com/microsoft/TypeScript-go/issues/4316#issuecomment-4726887637) **mrazauskas** said "Thanks for your thoughts. Indeed, it makes sense to handle diagnostics at the project level. I will explore this approach instead."
 * (today) **mrazauskas** closed the issue

### [Issue microsoft/TypeScript-go#4319](https://github.com/microsoft/TypeScript-go/issues/4319) (Closed, `Domain: API and Extensibility`, **andrewbranch**, **Copilot**)

**Add \`StringLiteral\`, \`NumberLiteral\` and others to the API**

*Extend the API with distinct literal types, properly support bigint values, and preserve negative bigint signs.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [PR microsoft/TypeScript-go#4326](https://github.com/microsoft/TypeScript-go/pull/4326) (Closed)

**Rebuilt build mode around \`fswatch\` package**

*Rebuilt build mode watcher using fswatch and an event-driven architecture, and extracted shared watch infrastructure into a new internal package*

 * created by **johnfav03**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4328](https://github.com/microsoft/TypeScript-go/pull/4328) (Open, `dependencies`, `javascript`)

**Bump form\-data from 4\.0\.5 to 4\.0\.6**

*Bumps form-data from v4.0.5 to v4.0.6, adding escapes for CR, LF, and quotes in field names and updating dependencies.*

 * (yesterday) **dependabot[bot]** added labels `javascript`, `dependencies`, `javascript`
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4332](https://github.com/microsoft/TypeScript-go/issues/4332) (Open, **jakebailey**, **Copilot**)

**Behavior difference: Type emit inconsistency with dangling block comment in file**

*Dangling block comments in top-level files are incorrectly attached to variables by tsgo while tsc erases them*

 * created by **hkleungai**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4333](https://github.com/microsoft/TypeScript-go/pull/4333) (Open)

**feat\(ast\): implement GetLineStarts and GetLineAndCharacterOfPosition \(\#4215\)**

*Implement GetLineStarts and GetLineAndCharacterOfPosition on Go AST’s SourceFile with unit tests.*

 * created by **ntoulasm**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4333#issuecomment-4718570077) **ntoulasm** said "@microsoft-github-policy-service agree"
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4335](https://github.com/microsoft/TypeScript-go/issues/4335) (Open, `Needs Investigation`, **andrewbranch**, **Copilot**)

**checker\.getBaseTypes panics for type alias to generic interface instantiation**

*checker.getBaseTypes panics with a nil pointer dereference when processing a type alias to a generic interface instantiation*

 * created by **tomquist**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [PR microsoft/TypeScript-go#4336](https://github.com/microsoft/TypeScript-go/pull/4336) (Open, **jakebailey**, **Copilot**)

**Fix JS declaration emit for dangling top\-level block comments**

*Prevent dangling top-level JSDoc comments from attaching to declarations by dropping them when non-declaration code is elided.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4337](https://github.com/microsoft/TypeScript-go/pull/4337) (Open)

**API: add checker methods to get true and false types of a conditional type**

*Add API checker methods for obtaining the true and false branch types of a conditional type.*

 * created by **piotrtomiak**
 * **RyanCavanaugh** added to milestone `Post-7.0`
 * [today](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4726236305) **mrazauskas** asked to link to issue #2851 and suggested adding getTrueType() and getFalseType() to ConditionalType
 * [later](https://github.com/microsoft/TypeScript-go/pull/4337#issuecomment-4731859787) **piotrtomiak** asked what “link” referred to and said they would implement the change after PR 4341 merged due to needing a Type–projectId association

### [Issue microsoft/TypeScript-go#4338](https://github.com/microsoft/TypeScript-go/issues/4338) (Open)

**checker\.getTypeArguments panics for non\-reference types**

*Calling checker.getTypeArguments on non-reference types such as string triggers a nil pointer panic.*

 * created by **tomquist**

### [Issue microsoft/TypeScript-go#4339](https://github.com/microsoft/TypeScript-go/issues/4339) (Open, `Needs Investigation`, **andrewbranch**, **Copilot**)

**RemoteNodeList inherited array methods throw this\.view\.getUint32 is not a function**

*Inherited array methods on RemoteNodeList in @typescript/native-preview throw a “this.view.getUint32 is not a function” error.*

 * created by **tomquist**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4339#issuecomment-4721657493) **JoostK** reported encountering the same issue with .map(), shared an override implementation that worked, and suspected iterator corruption
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [PR microsoft/TypeScript-go#4340](https://github.com/microsoft/TypeScript-go/pull/4340) (Closed)

**Note \`tsc\` for RC and above in README\.me**

*Document in the README that the TypeScript compiler (tsc) is required for RC and later versions.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4341](https://github.com/microsoft/TypeScript-go/pull/4341) (Open)

**API: make object registries project\-specific to avoid id collisions on types and signatures**

*Make object registries project-specific to prevent ID collisions on types and signatures and facilitate checker method refactoring.*

 * created by **piotrtomiak**

### [Issue microsoft/TypeScript-go#4342](https://github.com/microsoft/TypeScript-go/issues/4342) (Open)

**Behavior difference: \(Another\) Type emit issue on non\-const object keys referencing**

*tsgo emits a generic string index signature for constMap instead of preserving literal key types when importing non-const object keys*

 * created by **hkleungai**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [PR microsoft/TypeScript-go#4343](https://github.com/microsoft/TypeScript-go/pull/4343) (Open, **DanielRosenwasser**, **Copilot**)

**Ignore stray close events for unopened files**

*Ignore close events for files without open overlays by treating them as no-ops to prevent snapshot panics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4343#issuecomment-4725100250) **DanielRosenwasser** expressed confusion about receiving a didClose for an already-closed file and speculated editor behavior

### [PR microsoft/TypeScript-go#4344](https://github.com/microsoft/TypeScript-go/pull/4344) (Closed, **andrewbranch**, **Copilot**)

**Add per\-kind literal type interfaces and decode BigInt literal values to \`bigint\` in the API**

*Introduce per-kind literal type interfaces and decode BigInt literal strings into actual bigint values in the native-preview API*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4344#issuecomment-4725005441) **andrewbranch** said "@copilot address review feedback, though the “only call BigInt(...) when the payload value is actually a string” sounds overly defensive to me"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4344#issuecomment-4725077495) **Copilot** addressed review feedback by updating value handling to treat undefined and null as absent, allowing null on the wire, and retaining BigInt decoding keyed on the BigIntLiteral flag

### [PR microsoft/TypeScript-go#4345](https://github.com/microsoft/TypeScript-go/pull/4345) (Open, **andrewbranch**, **Copilot**)

**Fix getBaseTypes panic on type reference instantiations**

*Change getBaseTypes guard flags to exclude plain type references and prevent nil pointer panics on generic instantiations.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4724979237) **andrewbranch** said "@copilot what do you mean this mirrors Strada? I don't see anything like this code in Strada."
 * [today](https://github.com/microsoft/TypeScript-go/pull/4345#issuecomment-4725013121) **Copilot** acknowledged overstatement and corrected the wording, explained the behavioral equivalence and redirect mechanism compared to Strada, and noted the fix in commit 1e9b

### [PR microsoft/TypeScript-go#4346](https://github.com/microsoft/TypeScript-go/pull/4346) (Open, **andrewbranch**, **Copilot**)

**Fix RemoteNodeList inherited array methods throwing \`this\.view\.getUint32 is not a function\`**

*Define Symbol.species on RemoteNodeList to return plain Array so inherited filter, map, and slice methods avoid view.getUint32 errors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [Issue microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347) (Open, `Needs More Info`)

**CPU usage spikes to 80% to 100% when using \`tsgo \-\-lsp \-\-stdio\`**

*tsgo's LSP process uses 80-100% CPU when typing in TypeScript files larger than 100 lines*

 * created by **epicmet**

### [PR microsoft/TypeScript-go#4348](https://github.com/microsoft/TypeScript-go/pull/4348) (Closed)

**Update NOTICE and ensure it's inside packages**

*Ensure the NOTICE file is updated and included inside all package distributions.*

 * created by **jakebailey**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4349](https://github.com/microsoft/TypeScript-go/pull/4349) (Open)

**Collate\-free import sorting**

*Introduce a collate-free import sorting scheme with customizable ordinal and natural case options to replace and deprecate x/text/collate dependency*

 * created by **jakebailey**

