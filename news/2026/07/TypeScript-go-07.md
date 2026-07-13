# Report for 2026-07-07 (Tuesday, July 7th, 2026)

6 different users commented on 28 different issues.

## Activity Summary

### [PR microsoft/TypeScript-go#4239](https://github.com/microsoft/TypeScript-go/pull/4239) (Open, `No linked issue`)

**Replace ForEachReturnStatement closure with direct kind\-switched walk**

*Replace ForEachReturnStatement closure with a direct kind-switched recursive function to reduce allocations and improve performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4791564716) **jakebailey** said "@typescript-bot perf test this"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4791565226) **typescript-automation[bot]** notified that performance test jobs had started and would update the comment with build status and results
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4791792033) **typescript-automation[bot]** reported the results of the requested performance run with detailed comparison metrics
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4906347760) **jakebailey** said "In #4395 I optimized ForEachChild to avoid the interfaces; is this still helpful?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4906526669) **DanielRosenwasser** said "This would still save the closure allocation and visit fewer child nodes, right?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4239#issuecomment-4906575654) **jakebailey** said "No, this should get stack allocated"

### [PR microsoft/TypeScript-go#4296](https://github.com/microsoft/TypeScript-go/pull/4296) (Closed)

**Simple linear probing hash tables for \`Node\` and \`Symbol\` links**

*Implement simple linear probing hash tables for Node and Symbol links to replace map-based storage incompatible with paged arrays*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4296#issuecomment-4695564789) **typescript-automation[bot]** reported starting perf test jobs and provided status links
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4296#issuecomment-4695631877) **typescript-automation[bot]** reported that running tsc on the top 400 repos comparing main and refs/pull/4296/merge yielded no issues
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/4296#issuecomment-4695701278) **typescript-automation[bot]** provided the requested perf run results including a comparison report table
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#4369](https://github.com/microsoft/TypeScript-go/issues/4369) (Open, **jakebailey**)

**Publish an "other" platform VSIX**

*Publish a generic VSIX for unsupported platforms that omits TypeScript bundling and uses configured tsdk*

 * created by **jakebailey**
 * (2 weeks ago) **jakebailey** set milestone to `TypeScript 7.0 Stable`, and assigned to **jakebailey**
 * (today) **jakebailey** set milestone to `Post-7.0`, and removed from milestone `TypeScript 7.0 Stable`

### [PR microsoft/TypeScript-go#4449](https://github.com/microsoft/TypeScript-go/pull/4449) (Open)

**restore JSDoc member name check for private identifier references**

*Restores the JSDoc member name validation for private identifiers in isValidReferencePosition by implementing the missing helper.*

 * created by **aamoghS**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4805882923) **jakebailey** said "This needs tests that show this does something; it might not due to reparsing"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4449#issuecomment-4906335658) **jakebailey** said "What is this for? You're making the baselines worse?"

### [Issue microsoft/TypeScript-go#4459](https://github.com/microsoft/TypeScript-go/issues/4459) (Open, `Needs Investigation`, **johnfav03**)

**\[ServerErrors\]\[TypeScript\] main vs **

*The TypeScript main branch pipeline analyzed 300 repositories and reported 12 changes alongside timeouts, clone failures, and other errors.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4459#issuecomment-4814130126) **typescript-automation[bot]** reported a premature server connection closure for babel/babel with error details, replay commands, and repro steps
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4459#issuecomment-4814130163) **typescript-automation[bot]** reported a server connection closed prematurely with undefined error for nuxt/nuxt
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4459#issuecomment-4814130201) **typescript-automation[bot]** reported server connection closed prematurely with undefined error and provided error logs, last requests, and repro steps for n8n-io/n8n
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **johnfav03**

### [Issue microsoft/TypeScript-go#4461](https://github.com/microsoft/TypeScript-go/issues/4461) (Closed, `Needs Investigation`, **weswigham**)

**Behavior difference: Inconsistency when supplying \(internal\) expando function to another generic function call for exports**

*tsgo inconsistently omits .propTypes for memoized function components in .js and .tsx files compared to tsc*

 * created by **hkleungai**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#4462](https://github.com/microsoft/TypeScript-go/issues/4462) (Open, `bug`, **ahejlsberg**)

**Regression \(7\.0\.0\-dev\.20260624\.1\): intersection type member dropped in generic position — TanStack Router \`stripSearchParams\` rejected \(TS2322\), clean in tsc \+ 20260623\.1**

*Upgrading to @typescript/native-preview 7.0.0-dev.20260624.1 drops members from intersection types in generics, triggering TS2322 errors in TanStack Router.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4462#issuecomment-4822638054) **meabed** provided a runnable reproduction repository with instructions demonstrating the error
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4462#issuecomment-4823299573) **jakebailey** said "Bisects to #4389 @ahejlsberg "
 * **ahejlsberg** assigned to **ahejlsberg**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4464](https://github.com/microsoft/TypeScript-go/issues/4464) (Closed, `Type Ordering`)

**Wrong type\-argument inference from a union of arrays when one member is absorbed by a fixed arm of the target**

*tsgo infers V as MyError instead of {event:number} by absorbing the MyError[] arm into Error in a union of arrays*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4464#issuecomment-4827716621) **jakebailey** said "You should test 6.0 with --stableTypeOrdering"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4464#issuecomment-4831897515) **shkreios** said "testing 6.0 with --stableTypeOrdering reproduces it exactly. So this isn't tsgo-specific; it's the stable type ordering that tsgo defaults to."
 * **ahejlsberg** added label `Type Ordering`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4465](https://github.com/microsoft/TypeScript-go/issues/4465) (Closed, `Type Ordering`)

**False TS2321 "Excessive stack depth comparing types" for a hand\-rolled UnionToTuple recursion evaluated in a generic context**

*tsgo incorrectly reports an excessive stack depth error for a generic UnionToTuple recursion that tsc accepts*

 * created by **shkreios**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4465#issuecomment-4831896563) **shkreios** said "testing 6.0 with --stableTypeOrdering reproduces it exactly. So this isn't tsgo-specific; it's the stable type ordering that tsgo defaults to."
 * **ahejlsberg** added label `Type Ordering`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#4481](https://github.com/microsoft/TypeScript-go/issues/4481) (Open, `Domain: Editor`, **DanielRosenwasser**, **Copilot**)

**Auto\-imports hits unimplemented \`GetSourceOfProjectReferenceIfOutputIncluded\`**

*The auto-import process crashes with a stack trace due to the unimplemented GetSourceOfProjectReferenceIfOutputIncluded method.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4481#issuecomment-4840687832) **DanielRosenwasser** said "Probably similar to #4322"
 * (1 week ago) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * **RyanCavanaugh** added to milestone `Post-7.0`

### [Issue microsoft/TypeScript-go#4484](https://github.com/microsoft/TypeScript-go/issues/4484) (Open, `bug`)

**project reference { "path": "" } is ignored**

*tsgo build ignores project references with an empty path (""), while tsc correctly includes them unless changed to "./".*

 * created by **HolgerJeromin**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4484#issuecomment-4845719290) **jakebailey** suggested not silently ignoring an empty string and instead erroring or using "." or "./"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/4484#issuecomment-4850821788) **HolgerJeromin** agreed with the suggestion and noted that fixing is quick and poses no problem
 * (today) **RyanCavanaugh** added label `bug`, and set milestone to `Post-7.0`

### [Issue microsoft/TypeScript-go#4521](https://github.com/microsoft/TypeScript-go/issues/4521) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**SourceFile text does not include BOM**

*SourceFile.getText and getFullText omit the UTF-8 BOM while node start and end positions include it, causing misaligned text slices.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4521#issuecomment-4867571296) **acutmore** noted BOM stripping in ts-blank-space tests and pointed out a technical difference from Strada's behavior
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4521#issuecomment-4867639424) **jakebailey** assumed that reading via ts.sys.readFile removed the BOM and suggested dropping the BOM elsewhere
 * **DanielRosenwasser** added label `Domain: API and Extensibility`
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript-go#4527](https://github.com/microsoft/TypeScript-go/issues/4527) (Open, `bug`, `meta-issue`, **weswigham**)

**Investigate inconsistent diagnostic output in baselines & make builds with inconsistent diagnostic output fail tests**

*Investigate inconsistent diagnostic outputs in baselines caused by checker order dependence and enforce build failures on detection.*

 * (5 days ago) **weswigham** added labels `bug`, `meta-issue`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/4527#issuecomment-4870977001) **weswigham** mentioned that strada also contained TS-1 diagnostics in three additional baselines and proposed making TS-1 errors fail the build as the issue's completion criteria
 * (today) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **weswigham**

### [PR microsoft/TypeScript-go#4541](https://github.com/microsoft/TypeScript-go/pull/4541) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Bump GitHub CodeQL actions init, autobuild, and analyze to version 4.36.3 in the root directory.*

 * (yesterday) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4548](https://github.com/microsoft/TypeScript-go/issues/4548) (Closed, `Domain: API and Extensibility`, **andrewbranch**)

**NodeList loop performance**

*Array iteration methods inherited by RemoteNodeList behave in quadratic time due to linked list access, while forEachNode provides linear iteration.*

 * created by **acutmore**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4548#issuecomment-4901398372) **acutmore** said "Fixed in #4549"
 * (today) **andrewbranch** added label `Domain: API and Extensibility`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4549](https://github.com/microsoft/TypeScript-go/pull/4549) (Closed)

**\[api\] Optimize RemoteNodeList child access**

*RemoteNodeList access is optimized by reading raw buffer next pointers and caching them to improve iteration from O(n²) to O(n).*

 * created by **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4549#issuecomment-4901474940) **acutmore** said "Nice fix! Applying this patch locally I can confirm it fixes the benchmark case in #4548"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#4550](https://github.com/microsoft/TypeScript-go/pull/4550) (Closed)

**Set up stable / nightly extension split, other prep**

*Configure separate stable and nightly extension builds and related preparatory work, currently disabled.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#4553](https://github.com/microsoft/TypeScript-go/issues/4553) (Open, `Domain: API and Extensibility`, **andrewbranch**, **Copilot**)

**Add \`\.getConstraint\(\)\` and \`\.getDefault\(\)\` getter to \`TypeParameter\`**

*Add getConstraint() and getDefault() methods to TypeParameter for consistency with other type classes.*

 * created by **mrazauskas**
 * (today) **RyanCavanaugh** added label `Domain: API and Extensibility`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * **andrewbranch** assigned to **Copilot**

### [PR microsoft/TypeScript-go#4554](https://github.com/microsoft/TypeScript-go/pull/4554) (Closed)

**Move dprint plugins to npm**

*Publish dprint plugins to npm to circumvent firewall restrictions and eliminate manual pre-seeding in Copilot agent setup.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4555](https://github.com/microsoft/TypeScript-go/pull/4555) (Open)

**Add batched version for several API functions\.**

*Add batched versions of several API functions to reduce IPC overhead and improve performance.*

 * created by **dragomirtitian**

### [PR microsoft/TypeScript-go#4556](https://github.com/microsoft/TypeScript-go/pull/4556) (Open, **andrewbranch**, **Copilot**)

**Add getConstraint\(\) and getDefault\(\) getters to TypeParameter**

*Add asynchronous getConstraint() and getDefault() methods to the TypeParameter API for direct retrieval of type parameter constraints and defaults*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**

### [PR microsoft/TypeScript-go#4557](https://github.com/microsoft/TypeScript-go/pull/4557) (Open)

**Get incremental mode closer to Strada**

*Align tsgo's incremental build file tracking and performance reporting with tsc's Strada mode to fix accounting mismatches.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#4558](https://github.com/microsoft/TypeScript-go/pull/4558) (Closed)

**Prepare main for 7\.1 nightly builds**

*Update main to publish TypeScript 7.1 nightly builds as typescript@next and vscode-typescript-nightly while retiring the native-preview extension.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#4559](https://github.com/microsoft/TypeScript-go/pull/4559) (Closed)

**Luchta fixups**

*Apply minor fixes and adjustments to the Luchta codebase.*

 * created by **dobesv**
 * (later) **dobesv** closed the issue

### [Issue microsoft/TypeScript-go#4560](https://github.com/microsoft/TypeScript-go/issues/4560) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Extension does not follow symlinks when resolving the tsdk path \(breaks pnpm virtual store\)**

*TypeScript native-preview extension ignores pnpm tsdk symlinks, fails to locate platform binary, and falls back to the bundled version.*

 * created by **ya-woodcutter**
 * **ya-woodcutter** added label `Domain: Editor`
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#4561](https://github.com/microsoft/TypeScript-go/pull/4561) (Open, **jakebailey**, **Copilot**)

**Resolve native\-preview tsdk symlinks before locating platform package**

*Resolve file-based tsdk symlinks with realpath to correctly locate TypeScript platform packages in pnpm virtual stores.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

