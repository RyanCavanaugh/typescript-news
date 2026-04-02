# Report for 2026-03-05 (Thursday, March 5th, 2026)

19 different users commented on 65 different issues.

## Recommended Actions

 * Response Recommended
    * @xiongemi reported that the issue might be fixed in the linked nx PR in [microsoft/TypeScript-go#1431](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-4012445101)
    * @caomingpei provided detailed analysis of recursive type expansion root cause in [microsoft/TypeScript-go#2125](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4010014443)
    * @dougludlow requested an upper limit safeguard for memory usage in [microsoft/TypeScript-go#2125](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4011388398)
    * @Jack-Works asked if the nightly refers to the 'TypeScript (Native Preview)' VSCode plugin in [microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4006344592)

## Activity Summary

### [Issue microsoft/TypeScript-go#1431](https://github.com/microsoft/TypeScript-go/issues/1431) (Closed, `Domain: Module Resolution`, `Domain: Porting Meta`)

**baseUrl removal caused multiple libraries to fail**

*Removal of baseUrl support in tsgo breaks NX and Storybook path resolution, preventing monorepo updates.*

 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-3168671427) **ristomatti** explained that implicit detection of tsconfig.json files was needed for WebStorm TS 7.0 support in a monorepo
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-3613964953) **jakebailey** closed the issue due to no work required, noted tsgo hard error and TS 6.0 deprecation, and linked a migration tool supporting TS 4.1+
 * (13 weeks ago) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-4012445101) **xiongemi** said "this might be fixed from nx side in pull request https://github.com/nrwl/nx/pull/34453"
 * [later](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-4012488587) **hamidrezahanafi** tested the fix on version 22.5, confirmed it works, and closed their related issue

### [PR microsoft/TypeScript-go#2043](https://github.com/microsoft/TypeScript-go/pull/2043) (Closed, **jakebailey**, **Copilot**)

**Fix nil pointer panic in FormatOnEnter**

*Prevent nil pointer panics in FormatOnEnter by adding nil checks when deriving indentation from AST node lists.*

 * **Copilot** assigned to **jakebailey**
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2043#issuecomment-3602933187) **jakebailey** said "@copilot the panic in https://github.com/microsoft/typescript-go/issues/2042 is clearly not in this function"
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2043#issuecomment-3603021388) **Copilot** acknowledged the panic was in getStartLineAndCharacterForNode and added nil checks in that function and its callers
 * [today](https://github.com/microsoft/TypeScript-go/pull/2043#issuecomment-4006484871) **jakebailey** said "I don't like where this is going. Nodes should never be nil inside node lists! Even when missing!"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2085](https://github.com/microsoft/TypeScript-go/issues/2085) (Closed, `bug`)

**Missing config error for using module=none**

*tsgo with the --module none option fails to report the TS1148 error for exports that tsc correctly emits.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2085#issuecomment-3530151552) **jakebailey** said "none should be deprecated, right? in Corsa we use that as the "unset" value (not good)."
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2085#issuecomment-3530162159) **RyanCavanaugh** identified the Strada bug and noted it explained why Corsa matches it, and stated not recalling any discussion about deprecating it
 * **RyanCavanaugh** added label `bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2125](https://github.com/microsoft/TypeScript-go/issues/2125) (Open)

**Unbounded memory consumption with recursive conditional types causes compilation OOM**

*Recursive conditional types on large numeric and string unions lead the TypeScript compiler to run out of memory and crash.*

 * created by **caomingpei**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4006450858) **jakebailey** said "@caomingpei Can you recheck? I suspect #2987 helped with this."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4007882510) **RyanCavanaugh** noted that tsc's performance guarantees aren't security boundaries and recommended adding a watchdog for untrusted code
 * [today](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4009902071) **caomingpei** noted that tsc and ts-go had different default memory limits, causing tsc to abort earlier at the V8 heap limit while ts-go continued until a system-level OOM
 * [today](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4010014443) **caomingpei** explained that recursive type expansion led to unbounded growth and compared behavior of tsc and ts-go, linking to related issues
 * [later](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4011388398) **dougludlow** suggested adding an upper memory usage limit to terminate the tsgo process when it grows unbounded, reporting that it used 20–30+ GB and caused daily unresponsiveness
 * [later](https://github.com/microsoft/TypeScript-go/issues/2125#issuecomment-4011601474) **jakebailey** said "Editor growth is probably unrelated, and if you have a repro that would be very appreciated in a new issue."

### [Issue microsoft/TypeScript-go#2215](https://github.com/microsoft/TypeScript-go/issues/2215) (Closed)

**TS1323: Dynamic imports are not supported when targeting \`"module": "None"\`**

*tsgo reports TS1323 when using dynamic imports in a project with module 'None' despite TypeScript 5.9 support.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3612604119) **jakebailey** said "See also https://github.com/microsoft/typescript-go/issues/2214#issuecomment-3612585349"
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3612606763) **jakebailey** said "I don't quite understand "module none" yet using imports. Why not another mode?"
 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3613054881) **HolgerJeromin** explained migrating code to modules with backwards compatibility, using dynamic imports for mixed module and non-module code, and reported that updating to moduleDetection: 'legacy' did not resolve the compile error
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2229](https://github.com/microsoft/TypeScript-go/issues/2229) (Open, `Domain: Editor`, **jakebailey**, **Copilot**)

**Should not allow renaming keywords**

*TS-go erroneously permits renaming on keywords and parentheses instead of failing early via prepareRename*

 * [13 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2229#issuecomment-3614402370) **mjbvz** said "In 6.0 we do allow triggering renames on class and similar keywords but this shifts the rename to the class name instead"
 * (13 weeks ago) **jakebailey** added label `Domain: Editor`, and assigned to **Copilot**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**, and unassigned **Copilot**

### [Issue microsoft/TypeScript-go#2230](https://github.com/microsoft/TypeScript-go/issues/2230) (Open, `Domain: Editor`)

**Should not allow renaming parts of the standard library**

*Prevent users from renaming built-in standard library functions like setTimeout.*

 * **mjbvz** removed label `Crash`
 * (13 weeks ago) **jakebailey** added label `Domain: Editor`, and assigned to **Copilot**
 * **jakebailey** unassigned **Copilot**

### [PR microsoft/TypeScript-go#2231](https://github.com/microsoft/TypeScript-go/pull/2231) (Closed, **jakebailey**, **Copilot**)

**Prevent renaming keywords by validating in handleRename**

*Implement validation in handleRename to block renames on keywords or invalid targets, return localized errors, and update tests.*

 * created by **Copilot**
 * (13 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2232](https://github.com/microsoft/TypeScript-go/pull/2232) (Closed, **jakebailey**, **Copilot**)

**Prevent renaming standard library symbols**

*Add early validation to detect and block rename operations on symbols defined in TypeScript’s standard library, aligning with TypeScript’s rename semantics.*

 * created by **Copilot**
 * (13 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2353](https://github.com/microsoft/TypeScript-go/issues/2353) (Closed, `Domain: Emit`)

**Implement es2023\-\>es2022 transform \(class fields and class static blocks\)**

*Add support for transforming ES2023 class static blocks and class fields to ES2022 using new transformers.*

 * created by **DanielRosenwasser**
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2353#issuecomment-3644350760) **tmm1** said "related https://github.com/microsoft/typescript-go/pull/1542"
 * **jakebailey** added label `Domain: Emit`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2368](https://github.com/microsoft/TypeScript-go/pull/2368) (Closed, **jakebailey**, **Copilot**)

**Fix references code lens to include imports as references**

*Modify the Go code lens references feature to include import statements as valid references, matching TypeScript’s implementation.*

 * (11 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2368#issuecomment-3648358830) **Copilot** reverted the incorrect fix in commit aaefcb7a, kept the test to demonstrate the issue, and noted that a proper fix requires deeper analysis of TypeScript vs Go behaviors
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2408](https://github.com/microsoft/TypeScript-go/pull/2408) (Closed, **jakebailey**, **Copilot**)

**Fix declaration emit to retain imports for unresolved type aliases**

*Retain imports for unresolved type aliases in declaration emit with --noResolve when using as casts.*

 * [11 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3668764482) **Copilot** acknowledged test failures were caused by his changes and refined the fix to only add import tracking for unresolved symbols without changing type serialization, improved the baseline to include foo3's Unresolved import, and confirmed all tests passed
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3880194584) **jumbosushi** said "@jakebailey sorry for the ping, but just checking in on this 👀 is there anything I can do to help move it forward? also ran into the referenced issue"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2408#issuecomment-3880250353) **jakebailey** said "I don't think this PR is correct, unfortunately"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2446](https://github.com/microsoft/TypeScript-go/issues/2446) (Closed, **jakebailey**, **Copilot**)

**\`tsgo\` emits invalid code for decorated class methods with \`Symbol\` names**

*When compiling decorated class methods with computed Symbol names, tsgo emits invalid code referencing _a, causing a ReferenceError.*

 * created by **KostyaTretyak**
 * (8 weeks ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2621](https://github.com/microsoft/TypeScript-go/issues/2621) (Open, `bug`, **iisaduan**, **Copilot**)

**Fourslash is broken when making requests in unconfigured \.js files**

*Fourslash requests in unconfigured .js files fail with “no project found” errors, breaking tests such as auto-import completion.*

 * (1 month ago) **iisaduan** assigned to **Copilot**, **iisaduan**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2621#issuecomment-3825894034) **DanielRosenwasser** reported that restarting the extension while a .js file was open produced a 'no project found for URI' diagnostic error
 * **RyanCavanaugh** added label `bug`

### [Issue microsoft/TypeScript-go#2638](https://github.com/microsoft/TypeScript-go/issues/2638) (Closed)

**tsgo emits class field declarations for conditionally assigned fields that tsc doesn't**

*tsgo emits explicit class field declarations for optional or conditionally initialized properties that tsc omits, causing different runtime behavior.*

 * created by **psm14**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2638#issuecomment-3836274653) **jakebailey** said "Yes, this transform is not yet implemented"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2654](https://github.com/microsoft/TypeScript-go/issues/2654) (Closed, `wontfix`)

**Empty array can now be assigned to a bespoke property on a function**

*tsgo allows assigning an empty array to an undeclared function property inferring never[], whereas TypeScript 5.9 reports error TS7008*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2654#issuecomment-3842382017) **jakebailey** said "Why is it expected that this errors?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2654#issuecomment-3873255780) **ahejlsberg** explained that tsc infers any[] but tsgo infers never[] in strict mode and any[] in non-strict mode and endorsed tsgo's behavior
 * **ahejlsberg** added label `wontfix`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2678](https://github.com/microsoft/TypeScript-go/issues/2678) (Open, `Needs More Info`)

**\`tsgo \-\-build\` hangs indefinitely**

*After upgrading from @sinclair/typebox 0.34.48 to typebox 1.0.81, tsgo --build hangs indefinitely during type-checking and declaration emission.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3848715309) **rubenferreira97** reported that `--pprofDir` only created a 0KB profile file when tsgo finished and asked how to profile a hanging process, noting that build #2459 still hung
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3848719531) **jakebailey** said "It does, yeah. Sorry, I realized the implication of it hanging after I replied."
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2678#issuecomment-3849135940) **rubenferreira97** suggested adding a flag to capture a specific initial duration for debugging and offered further assistance
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript-go#2692](https://github.com/microsoft/TypeScript-go/issues/2692) (Closed, **jakebailey**, **Copilot**)

**tsgo does not respect \`esModuleInterop\` in certain cases**

*tsgo ignores the esModuleInterop setting when importing named exports from CommonJS JavaScript files with allowJs enabled, causing TS2497 errors.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3981831054) **zurmokeeper** said "@jakebailey When might this issue be resolved? It's been quite some time now. For TypeScript code referencing common.js, TypeScript 7's type checking fails outright, rendering it completely unusable."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3985694793) **jakebailey** said "JS stuff continues to be in flux. The pattern you used with module.exports = { foo } is not one that we handled. It's possible #2946 will help this, but I have not tested yet."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-3987233355) **jakebailey** said "This is 100% https://github.com/microsoft/typescript-go/issues/1054, FWIW; I didn't click to see the repro there but it's the same."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2692#issuecomment-4006464606) **jakebailey** said "#1054 is closed, so closing this too."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2709](https://github.com/microsoft/TypeScript-go/pull/2709) (Closed, **jakebailey**, **Copilot**)

**Implement TS5011 migration diagnostic for common source directory mismatch**

*Add TS5011 diagnostic to tsgo to alert when include patterns referencing parent directories cause output directory mismatches.*

 * created by **Copilot**
 * (3 weeks ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2709#issuecomment-4006718602) **jakebailey** said "#2819"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2721](https://github.com/microsoft/TypeScript-go/issues/2721) (Closed, `Type Ordering`)

**Variance resolution differs from tsc for recursive generic types \(@tanstack/react\-table\)**

*tsgo’s variance resolution for recursive generic types in @tanstack/react-table differs from tsc’s, producing order-dependent errors.*

 * **RyanCavanaugh** added label `Type Ordering`
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2721#issuecomment-3879961666) **RyanCavanaugh** clarified that tsgo matches `tsc --stableTypeOrdering` and requires a variance annotation rather than being a bug
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2721#issuecomment-3880239746) **Faithfinder** explained that tsgo matches tsc with --stableTypeOrdering, noted a minimal repro difference, and stated tsgo's consistent behavior is preferable and reported it for awareness
 * [today](https://github.com/microsoft/TypeScript-go/issues/2721#issuecomment-4008459434) **RyanCavanaugh** noted that subtle changes due to type ordering are the only expected differences between tsc and tsgo, and thanked the contributor for verifying it could have been a legitimate bug
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#2778](https://github.com/microsoft/TypeScript-go/issues/2778) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260212\.1 vs **

*The linux-x64-7.0.0-dev.20260212.1 TypeScript error-delta pipeline run experienced 158 timeouts, five git clone failures, and one unknown failure while analyzing 300 popular repositories.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2778#issuecomment-3898324478) **gabritto** suggested that server connection closed prematurely errors were due to OOMs based on pipeline logs
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2778#issuecomment-3898535476) **gabritto** summarized Copilot-produced possible existing crash issues and their statuses in a table
 * **jakebailey** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2780](https://github.com/microsoft/TypeScript-go/issues/2780) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**High memory consumption in a large pnpm monorepo**

*PR #2502 causes minor edits in a large pnpm monorepo to spike the TypeScript extension memory from ~700MB to ~35GB.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4002312683) **shinichy** said "I tried the latest nightly, but it doesn't fix the issue for me."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4005082708) **justinsmid** reported that after upgrading to the latest nightly yesterday afternoon, they have not observed memory usage spikes though lacking a consistent reproduction path
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4005159769) **dbrxnds** reported memory usage improvements with averages of 3-5GB and reduced peaks to 10-15GB, clearing faster than the previous 40-50GB
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4006344592) **Jack-Works** asked if they meant the "TypeScript (Native Preview)" VSCode plugin
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4006364171) **andrewbranch** explained that the VS Code extension ships daily and that users can use either its bundled version or point to the latest @typescript/native-preview versions via the typescript.native-preview.tsdk preference
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4006434882) **andrewbranch** described different causes for high memory usage, mentioned a pending PR with optimizations, and asked @shinichy about signing an NDA and sharing their repo for offline debugging
 * [today](https://github.com/microsoft/TypeScript-go/issues/2780#issuecomment-4009619194) **shinichy** said "@andrewbranch I'm not sure if an NDA is possible at my company, but I'll look into it. I'll send an email anyway. Thanks for your help!"

### [PR microsoft/TypeScript-go#2783](https://github.com/microsoft/TypeScript-go/pull/2783) (Closed)

**Configure agentic workflow for new crashes report**

*Configure an agentic workflow to automatically summarize new TypeScript-bot error reports against existing issues.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2829](https://github.com/microsoft/TypeScript-go/issues/2829) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260218\.1 vs **

*The linux-x64-7.0.0-dev.20260218.1 TypeScript pipeline reported 76 interesting changes, 59 unchanged results, 6 clone failures, 158 timeouts, and 1 unknown failure when analyzing 300 popular repositories.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924126975) **gabritto** said ""panic handling request completionItem/resolve: completion list needs auto imports" is in #2827"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2829#issuecomment-3924192677) **gabritto** noted that 'Server connection closed prematurely: undefined' errors seemed to be OOMs and said they would update the message accordingly, pointed to PR #2826 for debugging replays, and described manual fixes to replay files due to a fuzzer issue
 * **jakebailey** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2871](https://github.com/microsoft/TypeScript-go/issues/2871) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260222\.1 vs **

*The linux-x64 TypeScript 7.0.0-dev pipeline run encountered multiple errors—including timeouts, clone failures, and unknown failures—while analyzing popular repositories.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898776) **typescript-bot** reported a premature server connection closure error and supplied reproduction steps for the HumanSignal/label-studio repo
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2871#issuecomment-3941898803) **typescript-bot** reported that the server connection closed prematurely with undefined and listed affected repos and logs
 * **jakebailey** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#2881](https://github.com/microsoft/TypeScript-go/issues/2881) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[JavaScript\] linux\-x64\-7\.0\.0\-dev\.20260223\.1 vs **

*The linux-x64-7.0.0-dev.20260223.1 pipeline on 300 TypeScript repos detected three interesting changes, two clone failures, nineteen timeouts, and three unknown failures.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2881#issuecomment-3947789265) **typescript-bot** reported server connection closed prematurely with undefined error and listed the affected repository and recent requests
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2881#issuecomment-3947789311) **typescript-bot** reported a server connection closed prematurely error with affected repository details, last requests, and repro steps
 * **jakebailey** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2888](https://github.com/microsoft/TypeScript-go/pull/2888) (Closed)

**Fixed a class member completion crash after JSDoc comment with degenerate JSDoc tag in it**

*Resolve class member completion crashes caused by malformed JSDoc tags in comments.*

 * created by **Andarist**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2888#issuecomment-3969424774) **gabritto** said "(I'm looking into the race mode test failure; seems like a flaky test not related to this PR)"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2926](https://github.com/microsoft/TypeScript-go/pull/2926) (Closed)

**Implement ES decorator transform \(ESNext \-\> ES2022\)**

*Implement ESNext to ES2022 decorator transformation in tsgo to resolve issue #2354 blocking its adoption.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3989835921) **AlCalzone** said "@weswigham @jakebailey I think I've addressed everything now."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3992277016) **jakebailey** said "I want to wait for #2956 before looking into this; there is some overlap and that one is basically complete."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-3993216772) **AlCalzone** said "Cool, let me know when that PR is done and I'll see what I need to change here."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4007972403) **AlCalzone** fixed two more issues with ES decorators and default export function naming, and updated the submodule to reflect the changes
 * [later](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4010723492) **weswigham** suggested having the esDecorator transformer do nothing when experimentalDecorators is set and noted that class fields transformer options logic could be moved later

### [PR microsoft/TypeScript-go#2930](https://github.com/microsoft/TypeScript-go/pull/2930) (Closed, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Port changes from TypeScript pull request 63200**

*Port TypeScript PR 63200 by adding symbol name to unsafe import error messages and introducing a new TS2883 diagnostic.*

 * created by **Copilot**
 * (6 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2930#issuecomment-4008746875) **jakebailey** said "we did this in #2931"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2932](https://github.com/microsoft/TypeScript-go/issues/2932) (Closed, `Crash`, **DanielRosenwasser**)

**Panic on find\-all\-refs when a parameter property is preceded by a non\-property member\.**

*Invoking find-all-references on a constructor parameter property after a non-property class member causes a panic.*

 * created by **DanielRosenwasser**
 * (6 days ago) **DanielRosenwasser** added label `Crash`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2934](https://github.com/microsoft/TypeScript-go/pull/2934) (Closed)

**fix\(2932\): handle parameter\-property ref to method with same name**

*Ensure parameter-property references to methods with the same name are resolved correctly.*

 * (yesterday) **a-tarasyuk** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2934#issuecomment-4001051841) **DanielRosenwasser** said "@a-tarasyuk you don't have to close the PR, I just wanted to spend a bit longer understanding it"
 * (today) **a-tarasyuk** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2934#issuecomment-4007012571) **DanielRosenwasser** said "Thank you!"
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2940](https://github.com/microsoft/TypeScript-go/pull/2940) (Closed, **jakebailey**, **Copilot**)

**Fix stack overflow in type relation checking with recursive generic types**

*TypeScript’s recursive generic type checking causes unbounded recursion and stack overflow, mitigated by a compiler-level depth counter.*

 * created by **Copilot**
 * (5 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2942](https://github.com/microsoft/TypeScript-go/issues/2942) (Closed, `Crash`)

**tsgo \-\-api: DocumentIdentifier JSON unmarshaling panics**

*tsgo’s API panics when trying to unmarshal a DocumentIdentifier from JSON due to an invalid jsontext.Token*

 * created by **ajmacd**
 * **ajmacd** added label `Crash`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2942#issuecomment-3980818345) **ajmacd** said "Looks like this should fix it: https://github.com/microsoft/typescript-go/pull/2943"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2945](https://github.com/microsoft/TypeScript-go/issues/2945) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] linux\-x64\-7\.0\.0\-dev\.20260301\.1 vs **

*Automated linux-x64-7.0.0-dev.20260301.1 build on 300 popular TypeScript repositories reported errors, timeouts, and clone failures.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326680) **typescript-bot** reported that the server connection closed prematurely with an undefined error and listed affected repos and recent requests
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2945#issuecomment-3981326706) **typescript-bot** reported server connection closed prematurely and provided error details, affected repository links, recent requests, and repro steps
 * **jakebailey** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2956](https://github.com/microsoft/TypeScript-go/pull/2956) (Closed)

**Port class fields transform \(ES2022\)**

*Ports ES2022 class fields transform with static block support into TypeScript, removes obsolete flags, and corrects UseDefineForClassFields behavior.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2961](https://github.com/microsoft/TypeScript-go/pull/2961) (Closed)

**Skip all tests with alwaysStrict=false**

*Skip all variant tests marked alwaysStrict=false because they do not affect coverage.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2964](https://github.com/microsoft/TypeScript-go/issues/2964) (Closed, `Domain: Editor`)

**\[ServerErrors\]\[JavaScript\] linux\-x64\-7\.0\.0\-dev\.20260303\.1 vs **

*The linux-x64-7.0.0-dev.20260303.1 CI run reported 12 notable changes among 216 successful analyses and various failures across 300 TypeScript repositories.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188145) **typescript-bot** reported server connection closed prematurely error with repro steps and artifacts for videojs/video.js
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2964#issuecomment-3993188217) **typescript-bot** reported that the TS server connection closed prematurely with undefined error during analysis of mui/material-ui
 * **jakebailey** added label `Domain: Editor`
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2967](https://github.com/microsoft/TypeScript-go/pull/2967) (Closed)

**Fix various namespace diffs**

*Several fixes address import elision errors and other inconsistencies in namespace handling.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2988](https://github.com/microsoft/TypeScript-go/issues/2988) (Open, `Domain: Editor`)

**\[ServerErrors\]\[TypeScript\] main vs **

*TypeScript main pipeline encountered server errors in 62 of 300 repos and detected 163 interesting changes among the 238 analyzed.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339501) **typescript-bot** reported a panic handling request for textDocument/rangeFormatting due to a debug failure
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4001339552) **typescript-bot** reported a panic during textDocument/rangeFormatting with a debug failure and stack trace
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4006497130) **gabritto** summarized issues found by PR and request with panic messages and links
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4007294528) **gabritto** listed occurrences of 'Token end is child end' errors by node kind with counts and links
 * [today](https://github.com/microsoft/TypeScript-go/issues/2988#issuecomment-4008560677) **Andarist** noted that most issues referred to range formatting and likely would be fixed by PR 3000, and said they would still investigate the JsxAttribute issue

### [PR microsoft/TypeScript-go#2989](https://github.com/microsoft/TypeScript-go/pull/2989) (Closed)

**Fixed a crash when reformatting \`JsxNamespacedName\`**

*Resolves a crash when reformatting JsxNamespacedName nodes in the code formatter.*

 * created by **Andarist**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#2991](https://github.com/microsoft/TypeScript-go/pull/2991) (Closed)

**Auto import memory optimizations**

*Auto-import memory optimizations reduce heap usage by deduplicating package extraction and replacing string sets with bitflags.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2991#issuecomment-4008036950) **goloveychuk** attached an image found by AI with their own assumption

### [PR microsoft/TypeScript-go#2992](https://github.com/microsoft/TypeScript-go/pull/2992) (Closed)

**Fix string concats within string builder WriteString**

*Fix inline string concatenations in StringBuilder.WriteString calls to resolve editor warnings.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2993](https://github.com/microsoft/TypeScript-go/issues/2993) (Open, `bug`, `Domain: Editor`, **iisaduan**)

**Auto import does not get its own line**

*Auto-importing readFileSync inserts its import on the same line as the previous import instead of a new line.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, and assigned to **iisaduan**

### [PR microsoft/TypeScript-go#2994](https://github.com/microsoft/TypeScript-go/pull/2994) (Closed)

**Stop parsing module=none entirely**

*Reject the deprecated module=none setting during parsing because it is broken and unimplemented.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2994#issuecomment-4007192822) **jakebailey** said "Terrible timing since es2022 just merged, sorry"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2995](https://github.com/microsoft/TypeScript-go/pull/2995) (Closed)

**Fix call hierarchy crash on anonymous classes/functions**

*Call hierarchy was crashing for anonymous classes or functions and has now been fixed.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#2996](https://github.com/microsoft/TypeScript-go/pull/2996) (Closed)

**Fix test parser case for marker end next to jsdoc end**

*The test parser misinterprets marker end sequences followed by JSDoc comment ends as marker opens, and now prevents such reuse.*

 * created by **gabritto**
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#2997](https://github.com/microsoft/TypeScript-go/pull/2997) (Closed)

**Fixed a find reference crash related to JSDoc function types in TS files**

*A fix to resolve crashes occurring during find-reference operations on JSDoc function types in TypeScript files.*

 * created by **Andarist**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2997#issuecomment-4008534886) **Andarist** said "Hm, I have manually removed fourslash.SkipIfFailing(t) calls which is apperently not something I should do - that's why the CI failed on the previous commit. This has to be re-approved now"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2997#issuecomment-4008540912) **jakebailey** said "Correct, the gen dir is 100% generated and should never be touched by hand. My bad for not noticing."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2998](https://github.com/microsoft/TypeScript-go/pull/2998) (Closed)

**Fix crash in variance computation for recursive template literal types**

*Fixes a crash from runaway recursion in variance computation for recursive CamelCase template literal types when assigning between CamelCase<T> instantiations.*

 * created by **ahejlsberg**
 * (later) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2999](https://github.com/microsoft/TypeScript-go/pull/2999) (Open, **jakebailey**, **Copilot**)

**\[WIP\] Fix issue preventing renaming of keywords in TS\-go**

*Add early prepareRename validation in TS-go to prevent renaming of keywords and punctuation tokens*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2999#issuecomment-4009883793) **jakebailey** said "@copilot+claude-opus-4.6 something bad happened. Look at all of my comments and try again"

### [PR microsoft/TypeScript-go#3000](https://github.com/microsoft/TypeScript-go/pull/3000) (Closed)

**Fixed a range formatting crash after template literal**

*Fix range formatting crash occurring after a template literal.*

 * created by **Andarist**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript-go#3001](https://github.com/microsoft/TypeScript-go/pull/3001) (Closed)

**Implement missing deprecated property check**

*Implements the missing deprecated property check, updates fourslash deprecation tests, and marks two tests manual due to improved signature messages.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3002](https://github.com/microsoft/TypeScript-go/pull/3002) (Closed)

**Finish porting reportMergeSymbolError**

*Finalize the reportMergeSymbolError migration by deleting outdated commented code, keeping IsPlainJSFile checks, and clearing all TODO(TS-TO-GO) comments.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3002#issuecomment-4009741103) **connorshea** joked that they should close the issue tracker since they did it

### [Issue microsoft/TypeScript-go#3003](https://github.com/microsoft/TypeScript-go/issues/3003) (Closed)

**Standalone language server**

*Request for the command to run tsgo’s language server as a standalone process equivalent to typescript-language-server --stdio.*

 * created by **jcalve**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3003#issuecomment-4010181415) **jakebailey** said "tsgo --lsp --stdio"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3004](https://github.com/microsoft/TypeScript-go/pull/3004) (Closed)

**Fixed parsing of multiline string JSX attributes with whitespace present after \`=\`**

*The parser now handles multiline JSX string attributes with whitespace after '=' without crashing.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3005](https://github.com/microsoft/TypeScript-go/pull/3005) (Closed)

**Allow start and end positions to be in different files in \`getMappedLocation\`**

*Allow getMappedLocation to map start and end positions across separate files to prevent crashes.*

 * created by **Andarist**

