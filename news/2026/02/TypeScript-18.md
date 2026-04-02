# Report for 2026-02-18 (Wednesday, February 18th, 2026)

16 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @Hideman42 provided repro steps for the type inference issue in [microsoft/TypeScript#41456](https://github.com/microsoft/TypeScript/issues/41456#issuecomment-3926053636)
    * @Arlen22 reported that the suggested workarounds did not reliably resolve the issue in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922202353)
    * @Arlen22 asked how to debug the VS Code language server issue in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922212556)
    * @Arlen22 provided additional occurrence context in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922274213)
    * @Arlen22 provided information on reproducing the issue by reloading the window after closing offending files in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922806396)
    * @Arlen22 provided a workaround by adding prisma.config.ts to tsconfig.json in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922816633)
    * @Arlen22 provided additional log entries that might be relevant in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922834193)
    * @joshcartme asked to close the issue in [microsoft/TypeScript#63152](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3923237925)
    * @bkatzung provided version details and repro environment info in [microsoft/TypeScript#63159](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3924091654)

## Activity Summary

### [Issue microsoft/TypeScript#41456](https://github.com/microsoft/TypeScript/issues/41456) (Open, `Bug`, `Domain: check: Type Inference`)

**Incomplete infer for generic types**

*TypeScript cannot infer the generic Item type from LoaderConfigByName, defaulting it to unknown instead of string.*

 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/41456#issuecomment-724940206) **RyanCavanaugh** provided a simpler repro for the type inference issue
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/41456#issuecomment-945900704) **zbinlin** asked whether a provided code snippet exhibited the same problem
 * **RyanCavanaugh** added label `Domain: Type Inference`
 * [later](https://github.com/microsoft/TypeScript/issues/41456#issuecomment-3926053636) **Hideman42** reported a similar incomplete auto inference issue with TypeScript and provided a playground example

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation List**

*Proposed deprecations of outdated TypeScript 6.0 compiler options, with full removal planned for version 7.0.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3843337972) **RyanCavanaugh** said "Edited to add target: es5 and downlevelIteration (entirely) being deprecated."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3861434363) **RyanCavanaugh** said "Edited to un-deprecate enum merging and cross-namespace value referencing; these are in 7.0 already and removing them wouldn't produce the upside I had hoped for."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3874952761) **DanielRosenwasser** said "I think we also passed on conditional import fallbacks: https://github.com/microsoft/TypeScript/issues/50762"
 * [later](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3927313490) **HolgerJeromin** expressed concern about the removal of module:none in TypeScript 6.0-beta and its potential to lock projects on older versions

### [PR microsoft/TypeScript#55222](https://github.com/microsoft/TypeScript/pull/55222) (Closed, `Experiment`, `Author: Team`, `For Milestone Bug`, `For Backlog Bug`, **jakebailey**)

**Remove reportErrors check in relateVariances**

*Remove the reportErrors check in relateVariances to prevent inconsistent relation behavior in error and non-error modes.*

 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618194249) **typescript-bot** provided an installable tgz link and installation instructions
 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618259691) **typescript-bot** reported results of running tsc on top 400 repos comparing main and PR merge and noted everything looked good
 * [10 weeks ago](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3618522613) **Andarist** provided a repro snippet illustrating the ember break issue
 * [today](https://github.com/microsoft/TypeScript/pull/55222#issuecomment-3923474022) **jakebailey** said "It's too late to merge this; I'll wait until sometime after 7.0 (when this is going to need to be redone anyway)."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#59666](https://github.com/microsoft/TypeScript/pull/59666) (Open, `For Uncommitted Bug`)

**Add support for "specialize" tag**

*Introduce an @specialize JSDoc tag enabling inline specification of type arguments in JavaScript code.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/59666#issuecomment-2294619352) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59666#issuecomment-2320318946) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #27387. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [1.4 years ago](https://github.com/microsoft/TypeScript/pull/59666#issuecomment-2366972770) **Gerrit0** objected to allowing `<...>` for type arguments and argued for consistency with other type comments using `{number}`
 * [today](https://github.com/microsoft/TypeScript/pull/59666#issuecomment-3924919382) **apendua** said "I've resolved the conflicts and reverted the support for `` delimiters."
 * [today](https://github.com/microsoft/TypeScript/pull/59666#issuecomment-3924933758) **apendua** said "@DanielRosenwasser Do you think there's a chance this will be re-considered at some point?"

### [Issue microsoft/TypeScript#63132](https://github.com/microsoft/TypeScript/issues/63132) (Open, `Needs Investigation`, **ahejlsberg**)

**Regression: Mapped types are no longer homomorphic when wrapped in certain conditional types**

*TypeScript 3.9 regression breaks homomorphic mapped types in conditional types, so KeyMap<number> expands to an object rather than number.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63132#issuecomment-3898262132) **aweebit** thanked Andarist for the fix, explained that the repro was simplified, and provided a real-world TypeScript example demonstrating DeepOptionalize misbehavior on arrays
 * (5 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/issues/63132#issuecomment-3927088101) **darshjme-codes** explained that conditional type wrappers have been breaking TypeScript's homomorphic mapped type detection since v3.9 and provided details of the compiler logic and workarounds

### [PR microsoft/TypeScript#63137](https://github.com/microsoft/TypeScript/pull/63137) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update DOM types**

*Update DOM type definitions to accommodate planned changes for the upcoming 6.0 release.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3916664421) **typescript-bot** reported DT test results showing changed errors for the deno package
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3916697709) **typescript-bot** reported tsc user test results comparing main and the pull request merge, noted one Git clone failure and otherwise everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3916905055) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the pull request merge resulted in no issues
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041859) **Arlen22** provided the preceding log lines and expressed uncertainty about their consistency
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041867) **Arlen22** described a workaround by keeping prisma.config.ts and other non-tsconfig files closed to prevent the issue while noting it was not a solution
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922202353) **Arlen22** said "Keeping those files closed does not reliably prevent it from happening, and restarting TS server after closing all other files does not reliably get back to a working state."
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922212556) **Arlen22** expressed suspicion that the issue wasn't TypeScript related and might originate from VS Code's language server implementation, but noted uncertainty on how to debug it
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922226784) **Arlen22** said "Closing all files and opening one again cleared it this time. Immediately."
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922274213) **Arlen22** said "It seems to occur whenever any non-project files are open."
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922806396) **Arlen22** said "Reloading the window after closing all offending files seems to be fairly consistent. "
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922816633) **Arlen22** said "Adding the offending file (prisma.config.ts) to my project tsconfg.json file also seems to be fixing it. "
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922834193) **Arlen22** provided additional log entries that might be relevant

### [Issue microsoft/TypeScript#63152](https://github.com/microsoft/TypeScript/issues/63152) (Open, `Duplicate`)

**\.call selects the wrong overload, resulting in ts2554**

*Using .call on XMLHttpRequest.prototype.open incorrectly selects the longer overload and triggers a TS2554 error.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3917229422) **joshcartme** thanked MartinJohns and asked for other workarounds due to lib.dom types preventing signature rewrite
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3918753674) **MartinJohns** said "You can either use a type assertion, or you can bind the object like const bound = xhrOpen.bind(this); return bound(method, url); (I don't know if this has any performance implications.)"
 * [today](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3920845934) **nmain** suggested augmenting the Function type with fake variadic overloads and provided a Playground link and code snippet
 * [today](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3922916941) **jcalz** suggested widening xhrOpen's type using an intermediate variable and provided example code
 * [today](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3923237925) **joshcartme** thanked everyone and complimented @jcalz's solution, then suggested closing the issue

### [PR microsoft/TypeScript#63156](https://github.com/microsoft/TypeScript/pull/63156) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update dependencies**

*Update dependencies to the latest ESLint version, remove eslint-autolinkable-stylish, and address some audit issues.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#63157](https://github.com/microsoft/TypeScript/issues/63157) (Closed)

**Extension required when moduleResolution=bundler and imports/exports used**

*TypeScript with bundler module resolution fails to resolve package imports via imports/exports mappings without .js extensions.*

 * created by **polson136**

### [PR microsoft/TypeScript#63158](https://github.com/microsoft/TypeScript/pull/63158) (Closed, `For Uncommitted Bug`)

**Fix spelling in fourslash test comments: separator not seperator**

*Corrects the spelling of “seperator” to “separator” in fourslash test comments.*

 * created by **Sumit3754**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63158#issuecomment-3923336830) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63158#issuecomment-3923341411) **typescript-bot** notified that the pull request updated generated DOM declaration files which should not be edited and that the PR would be closed
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63159](https://github.com/microsoft/TypeScript/issues/63159) (Open, `Bug`)

**False positive "Private field \.\.\. must be declared in an enclosing class\."**

*VS Code wrongly reports private field must be declared errors in a second JavaScript file due to cross-tab state pollution.*

 * created by **bkatzung**
 * [today](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3924091639) **vs-code-engineering[bot]** suggested upgrading to the latest VS Code version and checking if the issue persisted
 * [today](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3924091654) **bkatzung** upgraded to the latest version and reported same results after closing other windows and using a clean profile
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63159#issuecomment-3924091663) **bkatzung** said ""
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63160](https://github.com/microsoft/TypeScript/issues/63160) (Open, `Duplicate`)

**Inferring from setter returns getter value**

*TypeScript's conditional type inference picks the getter's return type instead of the setter's parameter type.*

 * created by **LukeAbby**
 * [later](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3926391137) **MartinJohns** said "Duplicate of #62943."

### [Issue microsoft/TypeScript#63161](https://github.com/microsoft/TypeScript/issues/63161) (Closed, `Suggestion`, `Declined`)

**Make compiler option values case sensitive**

*Propose deprecating and removing case-insensitive compiler option values to enforce consistent casing in tsconfig.json.*

 * created by **remcohaszing**

