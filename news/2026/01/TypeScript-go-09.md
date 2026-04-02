# Report for 2026-01-09 (Friday, January 9th, 2026)

10 different users commented on 31 different issues.

## Recommended Actions

 * Response Recommended
    * @jfirebaugh provided repro steps as requested in [microsoft/TypeScript-go#2223](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3730907291)
    * @pouyarezvani asked what the explanation meant and reported that setting useTsgo breaks go to definitions in [microsoft/TypeScript-go#2360](https://github.com/microsoft/TypeScript-go/issues/2360#issuecomment-3731121124)
    * @rubnogueira asked if the provided repro was sufficient or if they should create a new one in [microsoft/TypeScript-go#2460](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730068931)

## Activity Summary

### [PR microsoft/TypeScript-go#1098](https://github.com/microsoft/TypeScript-go/pull/1098) (Closed)

**Add handling for 2\-3 invalid overload candidates**

*Restores two- to three-argument overload handling to resolve issue #1088, though error descriptions still mislabel overloads with 'new (' prefixes.*

 * [30 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1098#issuecomment-2953266502) **muglug** explained that moving lines invalidated existing `@ts-expect-error` comments and suggested applying specific changes from microsoft/typescript-go to maintain backwards compatibility and minimize diffs
 * [30 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1098#issuecomment-2956914322) **jakebailey** suggested porting the error positioning change into 5.9 and recommended using casts or 'as Foo satisfies Foo' instead of ts-ignore or ts-expect-error
 * [29 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1098#issuecomment-2981739735) **jakebailey** mentioned that the PR wouldn't be taken as-is and that the changes were intentional and possibly should be backported to Strada; noted that @ahejlsberg would look at the linked issue to assess error positioning
 * (today) **muglug** closed the issue

### [PR microsoft/TypeScript-go#1135](https://github.com/microsoft/TypeScript-go/pull/1135) (Closed)

**Attempt to fix commonjs module resolution weirdness**

*Proposed changes attempt to resolve inconsistencies in CommonJS module resolution.*

 * created by **muglug**
 * [today](https://github.com/microsoft/TypeScript-go/pull/1135#issuecomment-3731600072) **muglug** said "[ ] "
 * (today) **muglug** closed the issue

### [Issue microsoft/TypeScript-go#1677](https://github.com/microsoft/TypeScript-go/issues/1677) (Closed, `Crash`, **andrewbranch**)

**panic handling request textDocument/completion \(autoimports\)**

*The TypeScript-Go language server panics during textDocument/completion auto-imports when it cannot find the InternalIdentifier symbol in lodash’s type definitions*

 * created by **lukpsaxo**
 * **lukpsaxo** added label `Crash`
 * **RyanCavanaugh** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#1952](https://github.com/microsoft/TypeScript-go/issues/1952) (Closed, `Crash`, `Needs More Info`, **DanielRosenwasser**, **weswigham**)

**Declaration emit crash**

*The declaration emitter panics with ‘Unknown parent for parameter: KindArrowFunction’ during compilation.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3494573284) **mmichels-brex** said "Having the same error here in the latest tsgo build"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3589398392) **trueadm** provided a minimal reproduction and noted it worked fine with tsc
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3675234201) **trueadm** said "@DanielRosenwasser if you get time, please could you let me know if that repro is of any use, if not, I can try and come up with another."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3730952976) **jakebailey** said "@trueadm I tried out your repro on main and it did not crash. Is this fixed for you in the past few weeks?"

### [Issue microsoft/TypeScript-go#2143](https://github.com/microsoft/TypeScript-go/issues/2143) (Closed, `Crash`, **andrewbranch**)

**Panic handling request completionItem/resolve Some exportInfo should match the specified exportMapKey**

*TypeScript-Go language server panics on completionItem/resolve when exportInfo does not match the given exportMapKey*

 * **pedro757** added label `Crash`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2143#issuecomment-3643298196) **jakebailey** reported a panic in handling completionItem/resolve along with a stack trace
 * **RyanCavanaugh** assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189) (Closed, `Domain: Editor`, **andrewbranch**)

**LSP doesn't offer auto\-importing packages**

*VS Code’s TypeScript LSP does not offer auto-import suggestions for installed packages like `typescript-result`, only built-in modules*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3627394893) **andrewbranch** said "@kieranm that would be great! If you need an email for me, you can use my first name dot last name @microsoft.com."
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3629567310) **rubnogueira** reproduced the issue in a monorepo with PNPM where imports were suggested on Ctrl + Space but not inserted until restarting the IDE
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3655512275) **dalisoft** said "Same problem. You can check with this monorepo https://github.com/dalisoft/airlight"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2223](https://github.com/microsoft/TypeScript-go/issues/2223) (Open, `Domain: Editor`)

**Request textDocument/foldingRange failed\.**

*The TypeScript language server panics with a token cache mismatch error when requesting folding ranges in a compiled JavaScript file.*

 * created by **eamodio**
 * **eamodio** added label `Domain: Editor`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3614758634) **jakebailey** described also encountering the issue in a .ncurc.cjs file and struggling to integrate it into a fourslash test suite
 * [today](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3730907291) **jfirebaugh** provided a minimal reproduction snippet

### [Issue microsoft/TypeScript-go#2301](https://github.com/microsoft/TypeScript-go/issues/2301) (Closed, `Crash`, **andrewbranch**)

**Crash for value usage of type\-only import**

*TypeScript language service crashes when completing or resolving a type-only import used as a value.*

 * **DanielRosenwasser** assigned to **andrewbranch**
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2301#issuecomment-3633621249) **DanielRosenwasser** suggested commenting out lines 2181-2183 in completions.go and leaving a // !!! comment
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2301#issuecomment-3634818717) **andrewbranch** said "This will all be deleted soon"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2360](https://github.com/microsoft/TypeScript-go/issues/2360) (Closed, `wontfix`, `Domain: Editor`)

**Setting useTsgo=true with the plugin disabled will prevent you from jumping to the type definition in Cursor**

*Enabling typescript.experimental.useTsgo with the TypeScript Native Preview plugin disabled prevents jumping to type definitions.*

 * **RyanCavanaugh** added label `wontfix`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/2360#issuecomment-3647478665) **RyanCavanaugh** advised disabling the TypeScript (Native Preview) plugin and setting typescript.experimental.useTsgo to true in settings.json to avoid misconfiguration
 * (1 month ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2360#issuecomment-3731121124) **pouyarezvani** questioned the meaning of the previous comment and noted that enabling useTsgo broke go-to definitions
 * [today](https://github.com/microsoft/TypeScript-go/issues/2360#issuecomment-3731172796) **RyanCavanaugh** said "You can't turn on the "use the tsgo plugin" setting while also disabling the tsgo plugin and expect that to work"

### [Issue microsoft/TypeScript-go#2369](https://github.com/microsoft/TypeScript-go/issues/2369) (Closed, `Domain: Editor`, **DanielRosenwasser**)

**Code Lens provider registration error after switching tsdk location**

*Switching TypeScript SDK paths triggers a duplicate code lens command registration error and launches two language server instances.*

 * created by **andrewbranch**
 * **andrewbranch** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731050188) **DanielRosenwasser** said "I can fix this in this case, but the lifecycle around start/restart is a little weird because it doesn't dispose of the previous instance at all."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731054431) **DanielRosenwasser** said "And it's also a bit odd because LanguageClients can't synchronously dispose/stop either..."
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731107235) **jakebailey** said "The command doesn't use the client at all. It should just be registered outside Client, unconditionally on extension activation."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731130662) **DanielRosenwasser** said "Sure, that one does and that's easy. I'm working on other stuff that the Client needs to manage though."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2369#issuecomment-3731135262) **jakebailey** said "All in all, I would personally say we should just require there only be one Client at a time, then use globals or something"

### [PR microsoft/TypeScript-go#2390](https://github.com/microsoft/TypeScript-go/pull/2390) (Closed)

**New auto\-import infrastructure**

*Redesigns TypeScript's auto-import collection infrastructure to support snapshot-based LSP, parallelized data collection, and improved caching.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3685967528) **jansedlon** said "This looks solid. I'm wondering why is the difference in subsequent completion so small between TS and Go implementation. Do you think the gap widens with project size?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3686389797) **rubnogueira** reported that upgrading to the latest master broke auto-imports and related features in their pnpm mono/polyrepo, requiring a revert, and said they looked forward to testing the fixes when time permitted
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3705657539) **andrewbranch** expressed uncertainty about why the performance difference was small, noted how fast TS-based completions were, mentioned opportunities to optimize Go completions, and removed all profile hot spots for the auto-import path
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418) (Open)

**\[BUG\] tsgo list more files than tsc**

*tsgo’s --listFilesOnly output includes extra files compared to tsc, breaking basic tsgo --noEmit CI checks.*

 * created by **HananoshikaYomaru**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3678181840) **jakebailey** said "Can you use --explainFiles to check?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3678525881) **HananoshikaYomaru** attached two log files and thanked @jakebailey for reviewing them
 * [today](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3730926809) **jakebailey** asked for an example of an unexpected file, tsconfig settings, project details, and to compare against TS 6.0

### [Issue microsoft/TypeScript-go#2427](https://github.com/microsoft/TypeScript-go/issues/2427) (Open, `bug`)

**\`isolatedDeclarations\` is not yet implemented**

*tsgo does not implement the isolatedDeclarations compiler option, so it fails to report missing annotations unlike tsc 5.9.*

 * created by **so1ve**
 * **DanielRosenwasser** added label `bug`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3720630512) **jakebailey** said "See also #1693, #2459"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2427#issuecomment-3731130416) **jakebailey** said "To be clear, the linked issue adds some of the code to start getting us there, but not the errors."

### [Issue microsoft/TypeScript-go#2441](https://github.com/microsoft/TypeScript-go/issues/2441) (Closed)

**using tsgo fails with pnpx**

*Invoking tsgo via pnpx with @typescript/native-preview fails with a spawnSync ENOENT error because tsgo.exe cannot be found.*

 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3712297789) **JoostK** doubted that pnpx had a bug and explained that the tsgo JS wrapper spawned a native binary at a too-long path
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3720254684) **jakebailey** said "Yes, we just do execFileSync with the path name. Not super clear to me why pnpx/npx/etc could do better here for binaries (in general) since surely those paths would be long too."
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2441#issuecomment-3720405992) **jakebailey** said "I think #2448 should fix it"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2448](https://github.com/microsoft/TypeScript-go/pull/2448) (Closed)

**Handle long paths in native\-preview tsgo entrypoint**

*Enable the native-preview tsgo entrypoint to correctly handle long file paths.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2450](https://github.com/microsoft/TypeScript-go/issues/2450) (Open, `bug`, **iisaduan**)

**Review ported code from formatter**

*The Go port of the TypeScript formatter omitted retrieving the preceding token's parent before falling back to previousParent.*

 * **DanielRosenwasser** assigned to **weswigham**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2450#issuecomment-3725912447) **weswigham** said "Fixed by #2370 - https://github.com/microsoft/typescript-go/pull/2370/files#diff-57e4e12e0839091e4dde6c1f5e10e1438c3d3cd4f4eabdd7ea07530f0aac185dR306"
 * **weswigham** unassigned **weswigham**
 * (today) **DanielRosenwasser** added label `bug`, and assigned to **iisaduan**

### [PR microsoft/TypeScript-go#2451](https://github.com/microsoft/TypeScript-go/pull/2451) (Closed)

**Port the \`jsxClosingTag\` command**

*Port the jsxClosingTag command in the TypeScript Go plugin to resolve issues 2369 and 2399.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2451#issuecomment-3731398708) **DanielRosenwasser** considered redoing the feature as a server-to-client request and opted for a custom command due to testing infrastructure concerns

### [Issue microsoft/TypeScript-go#2454](https://github.com/microsoft/TypeScript-go/issues/2454) (Closed, **ahejlsberg**)

**\`tsgo\` slow \- too much type and type instantiation without \`\-\-singleThreaded\` options**

*Excessive type instantiation in tsgo results in much slower builds than tsc unless using --singleThreaded.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726599817) **jakebailey** advised that the linked PR would only partially improve the issue and cautioned about uploading private project files
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726604290) **noelkim-prestolabs** said "I understand, I'll prepare the repro If i can"
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2454#issuecomment-3726653619) **noelkim-prestolabs** prepared repro and shared repository link
 * (today) **ahejlsberg** removed label `Needs More Info`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2458](https://github.com/microsoft/TypeScript-go/pull/2458) (Closed)

**Preallocate types slice in getLiteralTypeFromProperties**

*Preallocate the types slice in getLiteralTypeFromProperties to reduce allocations and improve performance.*

 * created by **jakebailey**
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2460](https://github.com/microsoft/TypeScript-go/issues/2460) (Open, `Crash`)

**textDocument/inlayHint: Cannot create token from reparsed node of kind KindFunctionExpression**

*textDocument/inlayHint request panics due to inability to create a token from a reparsed function expression node*

 * created by **rubnogueira**
 * **rubnogueira** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730012281) **jakebailey** said "Do you have a repro we can test?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730026130) **a-tarasyuk** provided a minimal repro code example
 * [today](https://github.com/microsoft/TypeScript-go/issues/2460#issuecomment-3730068931) **rubnogueira** asked if the provided repro was sufficient or if they should create a new one, and reported an intermittent inlayHint error when opening JS files

### [PR microsoft/TypeScript-go#2461](https://github.com/microsoft/TypeScript-go/pull/2461) (Open, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#62950: Ignore computed name parents when looking up containing functions**

*Port PR #62950 to skip computed name nodes when finding containing functions, preventing recursion and fixing yield/await errors in Go.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2462](https://github.com/microsoft/TypeScript-go/pull/2462) (Open, **RyanCavanaugh**, **Copilot**)

**Port PR \#61376: Fix spurious "used before being assigned" errors in for of/in loops**

*Port TypeScript PR to fix misleading "used before being assigned" errors for variables in for-in and for-of loops.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2463](https://github.com/microsoft/TypeScript-go/pull/2463) (Closed, **RyanCavanaugh**, **Copilot**)

**Port TypeScript PR \#62789: Fix "never nullish" diagnostic missing expressions wrapped in parentheses**

*Port a fix to ensure parenthesized operands in TypeScript nullish coalescing chains correctly trigger 'never nullish' diagnostics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript-go#2464](https://github.com/microsoft/TypeScript-go/pull/2464) (Closed)

**Also clean CI runner for smoke test**

*Smoke tests are failing after a large auto-imports PR due to CI caching, suggesting cleaning the runner or disabling caching.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2465](https://github.com/microsoft/TypeScript-go/pull/2465) (Closed)

**Update LSP client to 10\.0\.0\-next\.19**

*Upgrade the LSP client to version 10.0.0-next.19 to resolve issue #2366.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2466](https://github.com/microsoft/TypeScript-go/pull/2466) (Closed)

**Cache types computed by \`getLiteralTypeFromProperties\`**

*Introduces caching for repeated keyof computations on large object types, reducing compiler check times drastically.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2466#issuecomment-3731627608) **ahejlsberg** said "We might consider back-porting this to 6.0."
 * (today) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2466#issuecomment-3731842023) **ahejlsberg** noted a 24x performance opportunity and explained that the bottleneck was computing the sorted key for a union type due to concurrency-stable type ordering

