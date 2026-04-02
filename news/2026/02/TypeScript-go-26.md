# Report for 2026-02-26 (Thursday, February 26th, 2026)

27 different users commented on 26 different issues.

## Recommended Actions

 * Response Recommended
    * @arcanis asked if the declaration emit reuse issue would be addressed before tsgo stabilization in [microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3971552911)
    * @dbrxnds asked if the NDA signed by Jake Bailey includes @andrewbranch so he could be invited to the private repository in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3971503830)
    * @Jack-Works provided a heap profile as requested in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3972237831)
    * @jansedlon provided version information in [microsoft/TypeScript-go#2889](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3967865615)
    * @jansedlon asked what the issue means for them and if DrizzleORM should fix it in [microsoft/TypeScript-go#2889](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3968172924)
    * @obedparla reported a regression between versions 7.0.0-dev.20260130.1 and 0.20260226.1 in [microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3972092239)
    * @andzdroid provided additional details about the issue persisting across versions in [microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3972146716)
    * @GGomez99 provided repro steps and asked if cached data/config could be causing the issue in [microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3973086152)
    * @hkleungai asked if they should open a new issue on the ts6 repo in [microsoft/TypeScript-go#2911](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-3971719843)

## Activity Summary

### [Issue microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234) (Open)

**tsgo eagerly resolve the type of inferred function Expression**

*tsgo eagerly resolves inferred function expression types, causing Record<keyof TestInterface, string> to collapse to Record<never, string> without explicit annotations.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614689338) **brokenmass** apologized for misunderstanding 'reusing nodes' and asked for clarification, expressed willingness to provide more info, and argued that the emitter shouldn't resolve keyof an exported interface
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614692174) **jakebailey** observed that the emitter resolved keyof exported interfaces until somewhat recently
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3642213777) **MisterJimson** explained that tsgo failed to apply SST’s module augmentations, causing TS2339 errors on Config.STAGE and Config.API_URL and making tsgo unusable for SST v2 projects
 * [later](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3971552911) **arcanis** asked whether declaration emit reuse would be addressed before tsgo became stable and noted errors persisted in symlinked codebase testing
 * [later](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3971565320) **jakebailey** said "Yes, for sure. You could try #1693 built from source to see."

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3943840500) **justinsmid** reported experiencing excessive memory usage and provided cache stats and a heap profile, noting the project was private but accessible to Jake Bailey
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3945883495) **andrewbranch** noted that the profile showed 9.5 GB of usage, explained that a nil DependencyNames bucket leads to gathering auto-imports from the entire directory, and suggested debugging computeDependenciesForNodeModulesDirectory
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3964094295) **Jack-Works** mentioned that the issue also occurred frequently in their public repository and provided the link
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3970103243) **andrewbranch** requested heap profiles, logs, and repro instructions and reported inability to reproduce memory usage above 171M
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3971503830) **dbrxnds** asked if the NDA signed by Jake Bailey included @andrewbranch so he could be invited to the private repository
 * [later](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-3972237831) **Jack-Works** provided a heap profile link showing tsgo consuming over 20GB and noted inability to capture a profile when memory is exhausted

### [PR microsoft/TypeScript-go#2819](https://github.com/microsoft/TypeScript-go/pull/2819) (Open, **jakebailey**, **Copilot**)

**Port TS PR \#62418: Add diagnostic when rootDir inference changes output layout**

*Add TS5011 diagnostic in Go compiler when inferred rootDir layout differs from computed common source directory.*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2819#issuecomment-3969844310) **jakebailey** asked to look into the submodule for changed tsbuild tests and update the Go versions to match to avoid extra output errors
 * [today](https://github.com/microsoft/TypeScript-go/pull/2819#issuecomment-3969925576) **Copilot** verified all changed tsbuild baselines against the TS submodule and concluded no Go test updates were needed

### [PR microsoft/TypeScript-go#2888](https://github.com/microsoft/TypeScript-go/pull/2888) (Open)

**Fixed a class member completion crash after JSDoc comment with degenerate JSDoc tag in it**

*Resolve class member completion crashes caused by malformed JSDoc tags in comments.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2888#issuecomment-3969424774) **gabritto** said "(I'm looking into the race mode test failure; seems like a flaky test not related to this PR)"

### [Issue microsoft/TypeScript-go#2889](https://github.com/microsoft/TypeScript-go/issues/2889) (Closed)

**Tsgo considers wrong API usage as correct \- difference in typechecking**

*tsgo wrongly treats improper use of orderBy in attachments as valid and infers incorrect types, unlike TypeScript’s stricter checks*

 * created by **jansedlon**
 * **jakebailey** assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3967824282) **RyanCavanaugh** provided a Copilot-reduced repro and verified it
 * **RyanCavanaugh** added label `bug`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3967844150) **RyanCavanaugh** said "Actually, this doesn't repro in 6.0 at latest..."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3967865615) **jansedlon** said "Oh i'm so sorry, i'm on 5.9 actually"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3967875139) **RyanCavanaugh** said "So was I 😅. Worth a bisect to see where this changed so that we can mention it in the 6.0 blog, investigating"
 * (today) **RyanCavanaugh** assigned to **RyanCavanaugh**, and unassigned **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3968006530) **RyanCavanaugh** said "Bisects to microsoft/TypeScript#62722"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3968016620) **RyanCavanaugh** said "Well, that's not explicable. It seems intentional, though. @Andarist any thoughts?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3968116300) **Andarist** explained that KnownKeysOnly only limited top-level properties and demonstrated that the error originated from the reverse mapped type by using an Identity example
 * (today) **RyanCavanaugh** removed label `bug`, and unassigned **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3968123317) **RyanCavanaugh** said "Thanks!"
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3968172924) **jansedlon** said "What does this mean for me exactly? Is this something DrizzleORM should fix on their side?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2889#issuecomment-3968249757) **Andarist** mentioned that a KnownKeysOnly type definition worked in the TS 6.0 playground

### [Issue microsoft/TypeScript-go#2902](https://github.com/microsoft/TypeScript-go/issues/2902) (Closed, `duplicate`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Unique symbol defined as attribute not narrowed**

*A unique symbol assigned as an object property is not properly narrowed within a union type in TypeScript 7.0.*

 * (2 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**, **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2902#issuecomment-3969419894) **ahejlsberg** noted duplicate of issue #1682 and explained intended tsgo behavior, providing a code snippet to preserve the unique symbol type
 * **ahejlsberg** added label `duplicate`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2902#issuecomment-3970345998) **jfdoming** said "I see, sorry! I missed the earlier issue and didn't realize it was intended behaviour."
 * (today) **jfdoming** closed the issue

### [PR microsoft/TypeScript-go#2903](https://github.com/microsoft/TypeScript-go/pull/2903) (Closed, **jakebailey**, **Copilot**)

**Fix unique symbol widening in expando property assignments**

*Unique symbols assigned as expando properties are incorrectly widened to symbol, breaking type narrowing via equality checks.*

 * created by **Copilot**
 * (2 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2910](https://github.com/microsoft/TypeScript-go/issues/2910) (Closed, `Domain: Editor`)

**Abnormal RAM/swap and CPU usage**

*Enabling the experimental tsgo TypeScript server in VSCode consumes excessive CPU and RAM/swap, making macOS sluggish.*

 * created by **Spookywy**
 * **Spookywy** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3967838215) **jakebailey** asked to save a heap profile when this happens
 * [today](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3971305189) **oskarscholander** said "I have the same issue"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3971439866) **jakebailey** requested a reproduction or a version bisection to identify the regression
 * [later](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3972092239) **obedparla** reported that migrating to TSGO succeeded in 7.0.0-dev.20260130.1 but failed in 0.20260226.1, suggesting a regression
 * [later](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3972146716) **andzdroid** reported issue persisted across versions when running tsgo --watch idle after initial build
 * [later](https://github.com/microsoft/TypeScript-go/issues/2910#issuecomment-3973086152) **GGomez99** reproduced excessive memory and CPU usage in the TypeScript-Go LSP, provided reproduction steps, attempted fixes, and a heap profile, and asked if cached data/config might be triggering the issue

### [Issue microsoft/TypeScript-go#2911](https://github.com/microsoft/TypeScript-go/issues/2911) (Open, **jakebailey**, **Copilot**)

**TS4053 happens when public class method adopts imported type from library**

*Public methods in an exported class using an imported library type cause TS4053 errors with tsgo.*

 * created by **hkleungai**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2911#issuecomment-3971719843) **hkleungai** edited the issue description with test results for various subcases and asked if they should open a new issue on the ts6 repo

### [Issue microsoft/TypeScript-go#2912](https://github.com/microsoft/TypeScript-go/issues/2912) (Closed, `Crash`)

**Error importing css files**

*Side-effect import of 'globals.css' in Next.js layout fails type-check with TS2882 after recent commit*

 * created by **pedro757**
 * **pedro757** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2912#issuecomment-3967827693) **jakebailey** questioned the repro given that noUncheckedSideEffectImports wasn't set and reported that setting it fixed the error
 * [today](https://github.com/microsoft/TypeScript-go/issues/2912#issuecomment-3967854783) **pedro757** said "Oh sorry, now I understand, so the default is now true"
 * (today) **pedro757** closed the issue

### [PR microsoft/TypeScript-go#2913](https://github.com/microsoft/TypeScript-go/pull/2913) (Open, **jakebailey**, **Copilot**)

**Fix TS4053 when public method return type uses imported type alias for unexported symbol**

*Add test reproducing TS4053 for public methods returning imported type aliases of unexported symbols and revert flawed alias resolution fix.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2913#issuecomment-3968602566) **jakebailey** said "@copilot This is the wrong fix. See all the failing tests and newly added diffs."

### [PR microsoft/TypeScript-go#2914](https://github.com/microsoft/TypeScript-go/pull/2914) (Open)

**\[WIP\] Adds tracing**

*Implements preliminary tracing to produce types.json and trace.json files as in the TypeScript codebase.*

 * created by **dimitropoulos**

### [PR microsoft/TypeScript-go#2915](https://github.com/microsoft/TypeScript-go/pull/2915) (Closed)

**Add hereby diff task**

*Include a missing diff task in the setup to avoid relying on manually saved difftool paths.*

 * created by **weswigham**
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript-go#2916](https://github.com/microsoft/TypeScript-go/issues/2916) (Closed)

**Different results in local vs CI**

*tsgo reports a type conversion error on Ubuntu CI but not on the local Mac environment.*

 * created by **samsternatmiter**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2916#issuecomment-3970131713) **samsternatmiter** said "Closing this. It was some file not tracked in git. Not sure what, but git clean -fdx && yarn install & yarn tsgo makes local match CI so this is not a tsgo issue."
 * (today) **samsternatmiter** closed the issue

### [Issue microsoft/TypeScript-go#2917](https://github.com/microsoft/TypeScript-go/issues/2917) (Open, `Crash`)

**Memory leak when using recursive type with template literal**

*A recursive template literal conditional type causes the TypeScript compiler to leak memory and OOM.*

 * created by **james-pre**
 * **james-pre** added label `Crash`

### [Issue microsoft/TypeScript-go#2918](https://github.com/microsoft/TypeScript-go/issues/2918) (Closed, **jakebailey**, **Copilot**)

**Spurious new "Property is used before its initialization" error**

*Using --useDefineForClassFields causes an erroneous 'used before initialization' error when accessing a subclass's static property in a base class initializer.*

 * created by **blickly**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2919](https://github.com/microsoft/TypeScript-go/issues/2919) (Closed)

**TS2304: Cannot find name 'T' with JSDoc**

*tsgo 7.0.0-dev incorrectly reports a 'Cannot find name T' error for a JSDoc generic typedef that TypeScript 5.9.3 handles correctly.*

 * created by **jbrimeyer**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2919#issuecomment-3969751928) **jakebailey** explained that under TypeScript <=6.0 the emitted d.ts hoisted the Bar typedef causing T to be undefined and linked a Playground example
 * (today) **jbrimeyer** closed the issue

### [PR microsoft/TypeScript-go#2920](https://github.com/microsoft/TypeScript-go/pull/2920) (Closed, **jakebailey**, **Copilot**)

**Fix spurious TS2729 "Property is used before its initialization" for cross\-class references**

*Add missing return false in tsgo’s PropertyDeclaration case to fix spurious TS2729 error on cross-class references*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2920#issuecomment-3969922652) **jakebailey** said "yep https://github.com/microsoft/typescript-go/pull/2921"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2921](https://github.com/microsoft/TypeScript-go/pull/2921) (Closed)

**fix\(2918\): align property\-declaration stop condition with strada same\-class logic**

*Align property-declaration stop condition to quit only when regular or parameter property declarations originate from the same class.*

 * created by **a-tarasyuk**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2922](https://github.com/microsoft/TypeScript-go/pull/2922) (Closed)

**Update npm deps, dprint**

*Update npm dependencies and include a crash fix from the gofumpt dprint plugin.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2923](https://github.com/microsoft/TypeScript-go/pull/2923) (Closed)

**created agent from minimization prompt**

*Custom replay-minimizer agent uses a multi-step prompt to reduce replay JSON files to minimal reproductions.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#2924](https://github.com/microsoft/TypeScript-go/pull/2924) (Open)

**Delete empty dirs in baseline\-accept task**

*Add automatic deletion of empty directories in the baseline-accept task to streamline comparison results.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2925](https://github.com/microsoft/TypeScript-go/pull/2925) (Closed)

**Misc source map fixes**

*Extract miscellaneous source map fixes from the ES2022 branch to reduce diffs.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2926](https://github.com/microsoft/TypeScript-go/pull/2926) (Open)

**Implement ES decorator transform \(ESNext \-\> ES2022\)**

*Add ESNext-to-ES2022 decorator transform support in tsgo to unblock its adoption.*

 * created by **AlCalzone**

