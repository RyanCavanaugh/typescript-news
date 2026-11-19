# Report for 2026-11-15 (Sunday, November 15th, 2026)

10 different users commented on 29 different issues.

## Recommended Actions

 * Response Recommended
    * @unixatch reported significant usability issues and requested a simpler type-only import syntax in [microsoft/TypeScript#36812](https://github.com/microsoft/TypeScript/issues/36812#issuecomment-6917076294)
    * @markstone111 asked a maintainer to confirm the proposed approach and assign the issue to them in [microsoft/TypeScript#65457](https://github.com/microsoft/TypeScript/issues/65457#issuecomment-6898492365)

## Activity Summary

### [Issue microsoft/TypeScript#36772](https://github.com/microsoft/TypeScript/issues/36772) (Open, `Bug`, `Domain: check: Control Flow`, `Rescheduled`)

**Type not narrowed by === when equivalent type guard works**

*TypeScript fails to narrow a generic type parameter with a literal equality check, despite equivalent user-defined type guards narrowing it correctly.*

 * **RyanCavanaugh** unassigned **ahejlsberg**
 * **typescript-bot** added label `Fix Available`
 * **jakebailey** removed label `Fix Available`
 * [today](https://github.com/microsoft/TypeScript/issues/36772#issuecomment-6903191130) **gameroman** reported that narrowing only broke when the narrowed generic value was assigned to a new variable, and provided a TypeScript reproduction

### [Issue microsoft/TypeScript#36812](https://github.com/microsoft/TypeScript/issues/36812) (Open, `Suggestion`, `In Discussion`, `Awaiting More Feedback`)

**Add \`import type "mod"\`**

*Add support for `import type 'mod'` to include global declarations and module augmentations without emitting runtime imports.*

 * [6.3 years ago](https://github.com/microsoft/TypeScript/issues/36812#issuecomment-664758660) **xiaoxiangmoe** suggested trying an empty type-only import from `my-lib`
 * [4.6 years ago](https://github.com/microsoft/TypeScript/issues/36812#issuecomment-1065210955) **thw0rted** reported a possible issue where type-only imports prevent module augmentations from applying at runtime, linked issue #48222, and offered to provide a reproduction with guidance
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/36812#issuecomment-2419467445) **mshima** noted that module augmentation could use `export type {} from '../global.js'`
 * [later](https://github.com/microsoft/TypeScript/issues/36812#issuecomment-6917076294) **unixatch** outlined difficulties importing types across declaration files, described cumbersome workarounds and documentation gaps, and suggested adding syntactic sugar for type-only imports

### [Issue microsoft/TypeScript#64891](https://github.com/microsoft/TypeScript/issues/64891) (Closed, `Needs Investigation`, **ahejlsberg**)

**7\.1 regression: declaration order of recursive generic interfaces changes assignability \(TS2322\)**

*TypeScript 7.1 regresses assignability for recursively generic interfaces, with declaration order and mapped key remapping triggering an erroneous TS2322 error.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/64891#issuecomment-6307221109) **shahinsamiur** mentioned investigating the variance calculation changes and developing a solution, with plans to share updates or a PR
 * (3 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#64995](https://github.com/microsoft/TypeScript/issues/64995) (Closed, `Needs Investigation`, **ahejlsberg**)

**Generic class in a reference cycle measured invariant in 7\.1: \`Link\<Sub\>\` no longer assignable to \`Link\<EntityBase\>\` \(@sap\-cloud\-sdk/odata\-common\)**

*TypeScript 7.1 regression incorrectly makes the covariant `Link<Sub>` type unassignable to `Link<EntityBase>` in `@sap-cloud-sdk/odata-common`.*

 * created by **todor-a**
 * (5 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript#65030](https://github.com/microsoft/TypeScript/pull/65030) (Closed, `For Uncommitted Bug`, **ahejlsberg**)

**Preserve reliability flags for cached relations during variance measurement**

*Preserve unmeasurable and unreliable flags when cached relation results are reused during variance measurement to prevent incorrect invariant classifications.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6509414012) **typescript-automation[bot]** reported that the user tests comparing the baseline and PR with tsc passed and everything looked good
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6509830896) **typescript-automation[bot]** reported the requested performance results comparing the baseline and PR, including unchanged compiler metrics in the visible output
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/65030#issuecomment-6510759318) **typescript-automation[bot]** reported that testing the top 400 repositories with `tsc` showed no differences between the baseline and PR and that everything looked good
 * (later) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#65049](https://github.com/microsoft/TypeScript/issues/65049) (Open, `Needs Investigation`, **andrewbranch**)

**sync API: the client and the server spend more time waiting for each other's next message than handling it; a small change to how both wait**

*Reduce sync API round-trip latency by changing client and server wait behavior to avoid costly CPU idle-state wake-ups between messages.*

 * (5 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/65049#issuecomment-6783728997) **andrewbranch** described an experimental branch that improved wall time by about 10% in typescript-eslint benchmarks but substantially increased CPU usage, and expressed concern about imposing the tradeoff or requiring esoteric environment-variable tuning
 * [today](https://github.com/microsoft/TypeScript/issues/65049#issuecomment-6904703698) **WinterYukky** provided cross-platform benchmark results showing adaptive spinning improved performance on hosts with multiple physical cores but could significantly regress single-core systems, and proposed removing the environment variables and enabling adaptive spinning only when at least four logical CPUs are available

### [Issue microsoft/TypeScript#65457](https://github.com/microsoft/TypeScript/issues/65457) (Open, `Bug`, `Domain: API`)

**\`typescript/async\`: getSourceFile\(\) returns a NumberKeyword for a typeToTypeNode\(\) result**

*`typeToTypeNode()` synthesizes a `NumberKeyword` whose `getSourceFile()` incorrectly returns the node itself instead of a `SourceFile`.*

 * created by **mathcovax**
 * [today](https://github.com/microsoft/TypeScript/issues/65457#issuecomment-6898492365) **markstone111** expressed willingness to investigate synthesized node handling in getSourceFile(), add regression tests, and implement a fix

### [Issue microsoft/TypeScript#65516](https://github.com/microsoft/TypeScript/issues/65516) (Open, `Needs Investigation`, **andrewbranch**)

**Content mapper ignore directives need diagnostic\-code selectors**

*Add diagnostic-code selectors to content-mapper ignore directives so framework diagnostics can be suppressed without hiding unrelated errors.*

 * created by **ubugeeei**

### [PR microsoft/TypeScript#65517](https://github.com/microsoft/TypeScript/pull/65517) (Open, `For Uncommitted Bug`)

**feat\(content\-mapper\): add diagnostic\-code selectors**

*Add diagnostic-code selectors to content-mapper directives, enabling code-specific suppression with protocol v10 support and validation for invalid selectors.*

 * created by **ubugeeei**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/65517#issuecomment-6912561753) **ubugeeei** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#65518](https://github.com/microsoft/TypeScript/pull/65518) (Closed, `For Backlog Bug`)

**Exempt declare redeclarations from TS2729 use\-before\-init check**

*Exclude ambient `declare` redeclarations from TS2729 use-before-initialization errors while preserving checks for ordinary redeclarations.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65519](https://github.com/microsoft/TypeScript/pull/65519) (Closed, `For Backlog Bug`)

**Fix object rest for\-of lowering skipping direct body statement transformation**

*Fix for-of lowering to transform direct body statements, correctly handling nested object-rest loops and function declarations for pre-ES2018 targets.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65520](https://github.com/microsoft/TypeScript/pull/65520) (Closed, `For Backlog Bug`)

**Fix indexed\-access base constraint losing explicit bound across checker histories**

*Fix retained-checker history bug where indexed-access base constraints lose explicit bounds, causing order-dependent false TS2339 errors.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65521](https://github.com/microsoft/TypeScript/issues/65521) (Closed)

**Native printer pulls in Windows IPC when used on its own**

*Remove the unused GetProjectReferenceFromSource dependency from printer.EmitHost to prevent importing compiler options and Windows IPC.*

 * created by **arnavdugar**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65522](https://github.com/microsoft/TypeScript/pull/65522) (Closed, `For Uncommitted Bug`)

**Remove GetProjectReferenceFromSource from printer\.EmitHost**

*Remove GetProjectReferenceFromSource from printer.EmitHost to prevent unnecessary dependencies and case-insensitive vendoring conflicts.*

 * created by **zhengdaodeguL**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#65523](https://github.com/microsoft/TypeScript/pull/65523) (Closed, `For Uncommitted Bug`)

**Remove the compiler options dependency from the printer**

*Remove the printer’s redundant compiler-options dependency to prevent Windows IPC imports and cross-platform vendoring conflicts.*

 * created by **arnavdugar**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (later) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/65523#issuecomment-6916825781) **arnavdugar** said "It really is. Thank you so much :)"

### [Issue microsoft/TypeScript#65524](https://github.com/microsoft/TypeScript/issues/65524) (Open, `Bug`, `Domain: JSDoc`)

**\[7\.0 regression\] JSDoc \`@this\` breaks \`@param\` matching for destructured parameter \(TS8024\)**

*TypeScript 7.0 incorrectly treats JSDoc `@this` as a parameter, breaking `@param` typing for destructured JavaScript parameters.*

 * created by **jablonski**

### [Issue microsoft/TypeScript#65525](https://github.com/microsoft/TypeScript/issues/65525) (Closed, `Bug`, **andrewbranch**, **Copilot**)

**Missing content\-mapper fallbacks cause internal LSP errors**

*Unknown script kinds without content-mapper fallbacks trigger internal LSP errors across requests for unsupported documents such as Vue files.*

 * created by **auvred**

### [Issue microsoft/TypeScript#65526](https://github.com/microsoft/TypeScript/issues/65526) (Open, `Bug`, `Domain: LS: Symbol Navigation`, **DanielRosenwasser**, **Copilot**)

**Duplicate callsite ranges for a single method call in callHierarchy/outgoingCalls**

*TypeScript 7.x reports duplicate callsite ranges for a single interface method invocation in callHierarchy/outgoingCalls.*

 * created by **char8x**

