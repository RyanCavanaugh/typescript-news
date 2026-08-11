# Report for 2026-08-04 (Tuesday, August 4th, 2026)

9 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @glav-git requested a built-in flag to limit CPU usage in [microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-5185662214)
    * @xpd confirmed the fix resolves the issue and provided detailed reproduction evidence in [microsoft/TypeScript-go#4819](https://github.com/microsoft/TypeScript-go/issues/4819#issuecomment-5186614993)

## Activity Summary

### [Issue microsoft/TypeScript-go#2824](https://github.com/microsoft/TypeScript-go/issues/2824) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**API usage patterns for complex editor extensions**

*Exploring IPC-based API features for a Go TS server to replace TS Server plugins and support Vue editor extensions*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5166713919) **Mad-Kat** described migrating TS Server plugins and distribution challenges, contrasted current tsconfig-based integration with LSP-plus-editor extensions, and asked if a sidecar model would be on the table
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5170503808) **Princesseuh** apologized for the late answer and explained how multiple TS/JS script blocks in an Astro file share scope or isolate modules and compile to a single default export
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5170697901) **NullVoxPopuli** explained Ember component format in glimmer-ts preserving block scope semantics and provided code examples
 * [later](https://github.com/microsoft/TypeScript-go/issues/2824#issuecomment-5193510895) **andrewbranch** asked for confirmation about the need for multiple virtual backing files due to global script scope across multiple HTML-like files

### [Issue microsoft/TypeScript-go#4347](https://github.com/microsoft/TypeScript-go/issues/4347) (Closed)

**CPU usage spikes to 80% to 100% when using \`tsgo \-\-lsp \-\-stdio\`**

*tsgo's LSP process uses 80-100% CPU when typing in TypeScript files larger than 100 lines*

 * **RyanCavanaugh** removed label `Needs More Info`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-4791728842) **RyanCavanaugh** said "Thanks! The CPU spikes are definitely a lot easier to notice when the server is capable of using all cores. Makes sense."
 * (5 weeks ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4347#issuecomment-5185662214) **glav-git** described using cpulimit to limit tsgo LSP CPU usage and requested a built-in flag

### [PR microsoft/TypeScript-go#4712](https://github.com/microsoft/TypeScript-go/pull/4712) (Open)

**Content mappers**

*Support external content mappers in tsconfig to transform and map unsupported file types into valid TypeScript*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5109758000) **remcohaszing** praised the PR's start and offered feedback on content-mapped file emission, suggesting handling for MDX and declaration maps, questioning how emit should work with mapped files, and noting SpanMapping length differences and potential Volar compatibility issues
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5175223764) **jasonlyu123** described issues with completion position mapping and span mapping constraints in Svelte transformations and asked for feedback on treating completion positions as range ends and on overlapping segment rules
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5180574756) **andrewbranch** acknowledged the same mapping issue, noted a stashed fix, thanked for the example, asked if spans should be broken into tokens or kept contiguous, and recommended using minimal spans
 * [today](https://github.com/microsoft/TypeScript-go/pull/4712#issuecomment-5185808920) **andrewbranch** updated the PR description, replaced SpanMapPurpose with per-LSP-feature bit flags, and added two ways to inject extra configuration options into content mappers

### [PR microsoft/TypeScript-go#4813](https://github.com/microsoft/TypeScript-go/pull/4813) (Closed)

**Avoid false symlink mappings for physical dependencies**

*Declaration emit incorrectly reused unrelated JSDoc imports after physical dependencies were falsely mapped as symlinks, now fixed.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5150134780) **typescript-automation[bot]** reported that running tsc on the top 400 repos showed no differences between main and the PR merge
 * (yesterday) **weswigham** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5173745809) **platypii** said "thanks for fixing this so quickly! this fixes the issue I was hitting with my published libraries 🙌 "
 * [today](https://github.com/microsoft/TypeScript-go/pull/4813#issuecomment-5181564232) **gabritto** agreed to make strings a union of empty and non-empty

### [Issue microsoft/TypeScript-go#4814](https://github.com/microsoft/TypeScript-go/issues/4814) (Open, `bug`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript’s main branch CI pipeline encountered server errors and timeouts analyzing 300 popular GitHub repositories, processing only 190.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473447) **typescript-automation[bot]** reported a panic while handling textDocument/diagnostic with stack trace and affected repository details
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473477) **typescript-automation[bot]** reported a panic handling textDocument/diagnostic request and provided a stack trace
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/4814#issuecomment-5148473518) **typescript-automation[bot]** reported a panic due to an unhandled KindBinaryExpression node kind in a JSX initializer
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `Post-7.0`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4818](https://github.com/microsoft/TypeScript-go/issues/4818) (Open, `Needs Investigation`, **gabritto**)

**internal/ls: getContextNodeForNodeEntry returns nil for module\-specifier literals \(stock returns the enclosing import statement\)**

*getContextNodeForNodeEntry returns nil for module-specifier literals in tsgo, unlike stock TypeScript which returns the enclosing import statement.*

 * created by **johnsoncodehk**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **gabritto**

### [Issue microsoft/TypeScript-go#4819](https://github.com/microsoft/TypeScript-go/issues/4819) (Closed)

**tsgo never terminates on a single three\.js TSL method call \(works in 5\.9\.3 and 6\.0\.3\)**

*tsgo 7.x hangs indefinitely on a single three.js TSL vec3(...).mul(2) call, while TypeScript 5.9.3 and 6.0.3 complete quickly*

 * created by **alexcz-a11y**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4819#issuecomment-5170414607) **RyanCavanaugh** guessed the issue stemmed from using a conditional type instead of a lookup type and linked to the relevant code segment
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4819#issuecomment-5175031885) **ahejlsberg** said "Looks related to (if not a duplicate of) #4528."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4819#issuecomment-5182312555) **RyanCavanaugh** said "Yep. Sent a DT PR"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/4819#issuecomment-5186614993) **xpd** confirmed the root cause at real-world scale and verified that the @types/three@0.185.2 fix resolves it fully, providing setup and benchmark details

### [PR microsoft/TypeScript-go#4820](https://github.com/microsoft/TypeScript-go/pull/4820) (Closed)

**Order variance computation by associated type symbol**

*Variance computation is now ordered by associated type symbol to ensure stable results for circular generic types.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5175461343) **typescript-automation[bot]** reported CI jobs status and provided results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5175676225) **typescript-automation[bot]** provided the perf run results requested by @ahejlsberg
 * [today](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5176061745) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the pull request merge showed everything looked good
 * [later](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5189134598) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5189135428) **typescript-automation[bot]** reported the start and status of build jobs with result links
 * [later](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5189383192) **typescript-automation[bot]** reported the requested perf run results to @ahejlsberg
 * [later](https://github.com/microsoft/TypeScript-go/pull/4820#issuecomment-5189882951) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and the pull request merge showed everything looked good

### [PR microsoft/TypeScript-go#4821](https://github.com/microsoft/TypeScript-go/pull/4821) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix TS1308 suppressed for \`await\` in computed property names of exported namespace classes**

*TS1308 errors were incorrectly suppressed for await in computed property names of exported namespace classes.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4821#issuecomment-5182339184) **RyanCavanaugh** said "Bad fix"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4822](https://github.com/microsoft/TypeScript-go/issues/4822) (Open, `Needs Investigation`, **andrewbranch**)

**Add batched assignability checks into the \`Checker API\`**

*Add batched type assignability checks and optional quantifiers to the Checker API for improved performance.*

 * created by **artem1458**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Possible Improvement`, and assigned to **andrewbranch**

### [PR microsoft/TypeScript-go#4823](https://github.com/microsoft/TypeScript-go/pull/4823) (Closed, **RyanCavanaugh**, **Copilot**)

**Preserve await context for exported classes in nested containers**

*Restrict await context for exported classes to top-level declarations while preserving it within async functions and generators.*

 * (yesterday) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5171393580) **Copilot** explained that export class was removed from invalid test locations and updated tests to use plain class in nested contexts while retaining export class only where syntactically legal
 * [today](https://github.com/microsoft/TypeScript-go/pull/4823#issuecomment-5182341856) **RyanCavanaugh** said "This fixes microsoft/TypeScript#63712"

### [Issue microsoft/TypeScript-go#4824](https://github.com/microsoft/TypeScript-go/issues/4824) (Open, `bug`, **jakebailey**)

**ram use regression from new @deprecated diagnostics**

*A recent @deprecated diagnostics change nearly doubled tsgo’s memory usage causing OOM errors on large monorepos.*

 * created by **walkerdb**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4824#issuecomment-5172376557) **jakebailey** demonstrated that issue #4309 triggered unexpected diagnostics and provided a test case
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript-go#4826](https://github.com/microsoft/TypeScript-go/issues/4826) (Open, `bug`, **RyanCavanaugh**, **iisaduan**, **Copilot**)

**\[lsp\] Go to Definition returns sources\[0\] of the declaration map instead of the mapped source file**

*Go to Definition returns the first declaration map source instead of the mapped source file in TypeScript LSP.*

 * created by **flosrn**
 * (today) **RyanCavanaugh** added label `bug`, set milestone to `TypeScript 7.1`, and assigned to **iisaduan**, **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4827](https://github.com/microsoft/TypeScript-go/issues/4827) (Closed, `Type Ordering`)

**Generic type argument inferred from the wrong inference slot \(cyclic union\-of\-intersections\); larger programs show scheduling\-dependent diagnostics**

*tsgo incorrectly infers a generic type argument from the wrong inference slot in a cyclic union-of-intersections, leading to inconsistent diagnostics in larger programs.*

 * created by **bel0v**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4827#issuecomment-5182662042) **RyanCavanaugh** said "This errors under tsc 6 with --stableTypeOrdering"
 * **RyanCavanaugh** added label `Type Ordering`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4829](https://github.com/microsoft/TypeScript-go/pull/4829) (Open, **RyanCavanaugh**, **Copilot**)

**Fix go\-to\-definition for multi\-source declaration maps**

*When declaration maps reference different source files, go-to-definition now prioritizes the identifier mapping file to correct erroneous file links.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript-go#4830](https://github.com/microsoft/TypeScript-go/issues/4830) (Open, `Domain: API and Extensibility`)

**API feature roadmap**

*Proposed API roadmap for TypeScript 7.1 detailing TS Server plugin replacements and top-level utility API features.*

 * created by **andrewbranch**
 * **andrewbranch** added label `Domain: API and Extensibility`

### [Issue microsoft/TypeScript-go#4831](https://github.com/microsoft/TypeScript-go/issues/4831) (Open, `Needs More Info`)

**High CPU Usage in Editor \(and Controls for LSP\)**

*Wants a built-in CPU usage limit flag for tsgo's LSP mode to prevent high CPU spikes on low-end laptops.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4831#issuecomment-5188485799) **DanielRosenwasser** said "@glav-git have you taken a profile to see what the cause is? Totally freezing your machine is extreme and unexpected."
 * **DanielRosenwasser** added label `Needs More Info`

