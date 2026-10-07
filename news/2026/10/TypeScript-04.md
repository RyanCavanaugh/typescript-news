# Report for 2026-10-04 (Sunday, October 4th, 2026)

12 different users commented on 31 different issues.

## Recommended Actions

 * Response Recommended
    * @belentani7 asked if they should investigate the exact code path in the compiler in [microsoft/TypeScript#64628](https://github.com/microsoft/TypeScript/issues/64628#issuecomment-5989252127)

## Activity Summary

### [PR microsoft/TypeScript#64388](https://github.com/microsoft/TypeScript/pull/64388) (Closed, `For Backlog Bug`)

**\[perf\]\[experiment\] fix\(64378\): add a cache to avoid repeated type arg inference**

*Introduce a cache for type argument inference to eliminate repeated inference and significantly improve performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/64388#issuecomment-5780363579) **typescript-automation[bot]** provided the requested perf run results
 * (1 week ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (later) **a-tarasyuk** closed the issue

### [Issue microsoft/TypeScript#64498](https://github.com/microsoft/TypeScript/issues/64498) (Closed, `Bug`, **andrewbranch**)

**Program\.emitToString\(\) silently omits real files due to nondeterministic isSourceFileFromExternalLibrary\(\) misclassification**

*TypeScript’s Program.emitToString sometimes excludes real source files because isSourceFileFromExternalLibrary nondeterministically marks them as external library files.*

 * (4 days ago) **RyanCavanaugh** set milestone to `TypeScript 7.1.1 RC`, and assigned to **andrewbranch**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/64498#issuecomment-5916667448) **RyanCavanaugh** said "@jelical we're interested in how to streamline AI-assisted bug reports like this one. Can you walk me through the human-side workflow that you went through to get to this spot?"
 * [later](https://github.com/microsoft/TypeScript/issues/64498#issuecomment-5990423700) **cplieger** provided the fix reference #64632
 * [later](https://github.com/microsoft/TypeScript/issues/64498#issuecomment-5993634266) **cplieger** described an AI-assisted fix for nondeterministic output in a monorepo, traced the root cause in filesparser.go, and proposed two enhancements to AI-driven issue reporting

### [PR microsoft/TypeScript#64528](https://github.com/microsoft/TypeScript/pull/64528) (Open, `For Uncommitted Bug`)

**Skip combined\-constraint check while measuring variances to avoid unbounded chase**

*Skip combined-constraint checks during variance measurement to prevent infinite type chase and memory exhaustion in TypeScript 7.*

 * (5 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/64528#issuecomment-5892189219) **Amatewasu** verified the fix against a private React 19+R3F+TSX project, reported memory and time benchmarks for unpatched TS7, patched TS7, and TS6, and noted diagnostics parity and caveats
 * [later](https://github.com/microsoft/TypeScript/pull/64528#issuecomment-5992092873) **Amatewasu** said "@microsoft-github-policy-service agree company="BALYO""

### [PR microsoft/TypeScript#64626](https://github.com/microsoft/TypeScript/pull/64626) (Open, `For Backlog Bug`)

**Fix stripInternal handling of unrelated leading comments**

*Update stripInternal to check a declaration’s actual JSDoc tags for @internal instead of arbitrary leading comments to avoid unintended removals.*

 * created by **splincode**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64626#issuecomment-5983058913) **splincode** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#64627](https://github.com/microsoft/TypeScript/issues/64627) (Open, `Bug`)

**\`import defer "\./a\.js"\` is accepted without an error, and the output drops \`defer\`**

*TypeScript incorrectly accepts and strips 'import defer "./a.js"' instead of reporting a syntax error.*

 * created by **leonidaz**

### [Issue microsoft/TypeScript#64628](https://github.com/microsoft/TypeScript/issues/64628) (Open, `Bug`, **weswigham**)

**JSDoc \`@private\` / \`@protected\` are dropped in declaration emit for properties declared by constructor assignment**

*TypeScript 7.0.2 drops JSDoc @private/@protected visibility and types for constructor-assigned properties in declaration files.*

 * created by **tlouisse**
 * [today](https://github.com/microsoft/TypeScript/issues/64628#issuecomment-5989252127) **belentani7** described a declaration emit bug where JSDoc visibility annotations on constructor parameter properties are lost in .d.ts, detailed impact, example, expected output, fix location, and workaround, and asked if they should investigate the compiler code path
 * [later](https://github.com/microsoft/TypeScript/issues/64628#issuecomment-5991294419) **tlouisse** said "Yes, it would be great if we can keep using this jsdoc annotation without having to do workarounds"

### [Issue microsoft/TypeScript#64629](https://github.com/microsoft/TypeScript/issues/64629) (Closed, `Bug`, **andrewbranch**)

**\[api\] createPrograms with a non\-composite projectReferences entry crashes the API server**

*Using createPrograms with a non-composite project reference crashes the TypeScript API server due to a nil pointer dereference*

 * created by **cplieger**

### [Issue microsoft/TypeScript#64630](https://github.com/microsoft/TypeScript/issues/64630) (Closed, `Bug`, **andrewbranch**)

**\[api\] Static and callback module resolutions drop resolvedUsingTsExtension, raising TS2876**

*Static and callback module resolutions drop the resolvedUsingTsExtension flag, resulting in TS2876 errors when using TypeScript’s API.*

 * created by **cplieger**

### [Issue microsoft/TypeScript#64631](https://github.com/microsoft/TypeScript/issues/64631) (Open, `Bug`, **andrewbranch**)

**\[api\] A nested request from a resolveModuleName callback gets another request's answer**

*Nested module resolution requests within a resolveModuleName callback sometimes return other requests’ results, causing incorrect resolutions.*

 * created by **cplieger**

### [PR microsoft/TypeScript#64632](https://github.com/microsoft/TypeScript/pull/64632) (Closed, `For Milestone Bug`, **andrewbranch**)

**Restart a file's imports when a later arrival lowers its node\_modules depth**

*Restart a file's import subtasks when its node_modules depth decreases to ensure consistent library classification and complete emits.*

 * created by **cplieger**
 * (later) **typescript-automation[bot]** added label `For Milestone Bug`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript#64633](https://github.com/microsoft/TypeScript/pull/64633) (Closed, `For Uncommitted Bug`)

**Fix crash in decorator metadata emit for decorated object literal members**

*Fixes a crash in TypeScript’s decorator metadata emission for decorated object literal members.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64633#issuecomment-5990767313) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [Issue microsoft/TypeScript#64634](https://github.com/microsoft/TypeScript/issues/64634) (Open, `Needs Investigation`, **iisaduan**)

**\[api\] Add \`parseConfigFileTextToJson\(\)\` helper**

*Add a parseConfigFileTextToJson() helper to enable consistent diagnostics when parsing JSON config strings.*

 * created by **mrazauskas**

### [Issue microsoft/TypeScript#64635](https://github.com/microsoft/TypeScript/issues/64635) (Open, `Needs Investigation`, **andrewbranch**)

**API server reports TS2345 for a call that tsc accepts on the same project**

*TypeScript’s language server API intermittently reports TS2345 for fitViewportToNodes calls despite tsc compiling the same project without errors.*

 * created by **vivere-dally**

### [PR microsoft/TypeScript#64636](https://github.com/microsoft/TypeScript/pull/64636) (Closed, `For Uncommitted Bug`)

**Fix flaky diagnostic added by emit for \`typeof import\(\)\` type qualifiers**

*Resolve flaky diagnostics during emit for typeof import() type qualifiers.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64636#issuecomment-5992621711) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64637](https://github.com/microsoft/TypeScript/pull/64637) (Closed, `For Milestone Bug`, **andrewbranch**)

**\[api\] Report project reference diagnostics on programs without a config file**

*Prevent API server crashes by handling project reference diagnostics on programs lacking a configuration file*

 * created by **cplieger**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64638](https://github.com/microsoft/TypeScript/pull/64638) (Closed, `For Milestone Bug`, **andrewbranch**)

**\[api\] Skip disk\-layout import diagnostics for customized module resolutions**

*Skip disk-layout import diagnostics (such as TS2876) for customized module resolutions by adding an internal IsCustomResolution flag.*

 * created by **cplieger**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#64639](https://github.com/microsoft/TypeScript/pull/64639) (Open, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] Answer nested requests on the sync connection in stack order**

*SyncConn.Call’s nested requests could interleave and receive incorrect responses, now fixed by enforcing stack-order handling.*

 * created by **cplieger**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [PR microsoft/TypeScript#64640](https://github.com/microsoft/TypeScript/pull/64640) (Open, `For Uncommitted Bug`)

**fix\(64627\): reject deferred imports without namespace bindings**

*The compiler now rejects deferred imports that lack a namespace binding.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64641](https://github.com/microsoft/TypeScript/issues/64641) (Open, `Bug`, **andrewbranch**)

**\[api\] Let a program created with createPrograms use content mappers**

*Add an optional contentMappers option to CreateProgramOptions so createProgram-generated programs can apply configured content mappers.*

 * created by **cplieger**

### [PR microsoft/TypeScript#64642](https://github.com/microsoft/TypeScript/pull/64642) (Open, `For Uncommitted Bug`)

**Fix \`workspace/symbol\` crash on an inferred project without a program**

*workspace/symbol requests crash on inferred TypeScript projects without an associated program.*

 * created by **Andarist**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64642#issuecomment-5995071174) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#64643](https://github.com/microsoft/TypeScript/pull/64643) (Open, `For Backlog Bug`)

**Fix JSX linked editing for incomplete property tags with attributes**

*Implement parser recovery to prevent attributes being consumed in incomplete JSX property tags and restore linked editing functionality.*

 * created by **musatoktas**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64643#issuecomment-5997010581) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **musatoktas** added label `For Uncommitted Bug`
 * (later) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64643#issuecomment-5997164731) **musatoktas** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64644](https://github.com/microsoft/TypeScript/pull/64644) (Open, `For Uncommitted Bug`)

**Fix crash in formatter on comment lookalikes in JSX closing tags**

*A fix for formatter crashes triggered by JSX closing tags resembling comments.*

 * created by **Andarist**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64644#issuecomment-5998060040) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

