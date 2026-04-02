# Report for 2025-12-04 (Thursday, December 4th, 2025)

28 different users commented on 46 different issues.

## Recommended Actions

 * Response Recommended
    * @johnpyp reported that the issue persists for workspace dependencies despite a fix for external dependencies in [microsoft/TypeScript-go#1034](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3614387030)
    * @justinsmid provided repro steps and a workaround in [microsoft/TypeScript-go#1465](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3615895910)
    * @eamodio reported discrepancy in reference counts between CodeLens and find-all-references in versions 5.9 and 7.0 in [microsoft/TypeScript-go#2177](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3613785267)
    * @thaoula provided real source files as requested in [microsoft/TypeScript-go#2212](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3615023529)
    * @HolgerJeromin reported that changing module to moduleDetection 'legacy' did not fix compilation in [microsoft/TypeScript-go#2215](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3613054881)
    * @brokenmass suggested changing the condition in canHaveLiteralInitializer from '!= 0' to '== 0' in [microsoft/TypeScript-go#2217](https://github.com/microsoft/TypeScript-go/issues/2217#issuecomment-3613206466)
    * @brokenmass suggested marking this issue as a duplicate of issue #989 in [microsoft/TypeScript-go#2217](https://github.com/microsoft/TypeScript-go/issues/2217#issuecomment-3613483406)
    * @jbrimeyer-leepfrog asked how to provide more information to track down the issue in [microsoft/TypeScript-go#2218](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3613398372)
    * @jbrimeyer-leepfrog reported a tsgo panic and provided repro steps in [microsoft/TypeScript-go#2218](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3613574354)
    * @brokenmass provided a code-based solution fixing the type inference issue in [microsoft/TypeScript-go#2220](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3614655373)
    * @darklight9811 asked if it would be easier for @jakebailey and @chase to work on this since it was related to another issue in [microsoft/TypeScript-go#2222](https://github.com/microsoft/TypeScript-go/issues/2222#issuecomment-3613971528)
    * @brokenmass asked if the provided information was sufficient in [microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614591815)
    * @brokenmass asked for clarification on 'reusing nodes' in [microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614689338)
    * @damiangreen reported failed imports and provided their tsconfig.json in [microsoft/TypeScript-go#518](https://github.com/microsoft/TypeScript-go/issues/518#issuecomment-3615107376)

## Activity Summary

### [Issue microsoft/TypeScript-go#1032](https://github.com/microsoft/TypeScript-go/issues/1032) (Open, `Domain: Type Checking`, `Type Ordering`)

**Change in inference from tuple to array**

*tsgo 7.0.0-dev changes tuple inference so Object.entries mapping yields string[][] instead of [string,string][], causing TS2345 type errors.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1032#issuecomment-2940876391) **jakebailey** said "@ahejlsberg I know you marked this as wontfix, but do you think there's likely to be a generic fix to this class of problem? AFAIK this is union subtype reduction, right?"
 * **ahejlsberg** added label `Type Ordering`
 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1032#issuecomment-2994223243) **ahejlsberg** explained that the type inference failure was caused by picking the first candidate and proposed using InferencePriorityReturnType to produce a union type, and stated intent to create a PR
 * **jakebailey** removed label `wontfix`

### [Issue microsoft/TypeScript-go#1034](https://github.com/microsoft/TypeScript-go/issues/1034) (Closed, `Domain: Declaration Emit`, **weswigham**)

**\[pnpm\] Error 2742 The inferred type of xxx cannot be named**

*Using tsgo instead of tsc triggers TS2742 errors about non-portable inferred types requiring explicit annotations.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612549496) **rubnogueira** said "I was having some issues with moment and some specific dependencies, and 7.0.0-dev.20251204.1 solved it for me. Thanks :) "
 * [today](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612581053) **jakebailey** mentioned updating the pnpm monorepo to 7.0.0-dev.20251204.1, noted that 200 type errors remain despite fewer errors, and suggested filing new issues or treating remaining tasks as bug-level work
 * [today](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612582814) **emanuel-lundman** reported that 7.0.0-dev.20251204.1 with bun solved the errors and yielded a 2x speedup (16s vs 33s and 19s vs 44s) for noEmit type checks on Apple Silicon M1 Max and thanked the effort
 * [today](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3614387030) **johnpyp** said "It looks like 7.0.0-dev.20251204.1 has solved the issue for external dependencies, but not solved it for workspace dependencies (using project references)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3614471012) **jakebailey** said "Please file issues for the cases you're seeing; we need repros."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3614493501) **johnpyp** said "apologies! made here: https://github.com/microsoft/typescript-go/issues/2233"

### [Issue microsoft/TypeScript-go#1431](https://github.com/microsoft/TypeScript-go/issues/1431) (Closed, `Domain: Module Resolution`, `Domain: Porting Meta`)

**baseUrl removal caused multiple libraries to fail**

*Removal of baseUrl support in tsgo breaks NX and Storybook path resolution, preventing monorepo updates.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-3168283925) **ristomatti** described encountering swc's baseUrl dependency issue on a NestJS project and shared a solution by adding .swcrc with baseUrl './'
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-3168311676) **hamidrezahanafi** described a workaround by creating tsconfig.tsgo.json with baseUrl set to null for type checking
 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-3168671427) **ristomatti** explained that implicit detection of tsconfig.json files was needed for WebStorm TS 7.0 support in a monorepo
 * [today](https://github.com/microsoft/TypeScript-go/issues/1431#issuecomment-3613964953) **jakebailey** closed the issue due to no work required, noted tsgo hard error and TS 6.0 deprecation, and linked a migration tool supporting TS 4.1+
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1465](https://github.com/microsoft/TypeScript-go/issues/1465) (Closed, `Crash`, `Domain: Program`, **sheetalkamat**)

**Intermittent crash with \-\-incremental**

*tsgo intermittently crashes when run with --incremental on large projects in frequent CI pipelines*

 * [16 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3180367544) **robw-mercury** asked if the user had a test repository with many files and offered to pair on a call to reproduce the error
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3272538693) **paperclover** reported that after rebasing onto master, tsgo now consistently triggered a stack overflow and provided the commit range that caused it
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3572146695) **sheetalkamat** said "Can you please use nightly and see if this is fixed. "
 * [later](https://github.com/microsoft/TypeScript-go/issues/1465#issuecomment-3615895910) **justinsmid** described encountering the issue consistently on a specific branch after switching to tsgo, provided reproduction steps, and noted that disabling incremental or changing the @typescript/native-preview version worked around it

### [PR microsoft/TypeScript-go#1966](https://github.com/microsoft/TypeScript-go/pull/1966) (Open)

**Add Yarn PnP support**

*Implement native Yarn Plug'n'Play support in TypeScript Go with PnP VFS, API, and manifest handling.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3456508357) **GGomez99** said "@microsoft-github-policy-service agree company="Datadog""
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3457072757) **GGomez99** said "I see my tests are not passing in CI, looking into it 🙇 "
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3604090437) **adrian-gierakowski** said "is this kept up to date with master? I would like to try it out on a monorepo at work. Thanks!"
 * [later](https://github.com/microsoft/TypeScript-go/pull/1966#issuecomment-3616833735) **GGomez99** offered to update the PR to keep it in sync with master and invited further feedback

### [Issue microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162) (Open, `Domain: Type Checking`, **ahejlsberg**)

**Type inference lost for callback parameter**

*Using ts-go configuration causes TypeScript to lose type inference for the organization plugin's sendInvitationEmail callback parameter.*

 * created by **Azzerty23**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3610135477) **jakebailey** described that only the first `data` parameter was implicitly typed as any in the better-auth example and that removing the return type of `organization` in favor of any made the parameter type work
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3610164033) **jakebailey** provided a minimal TypeScript reproduction of the issue with betterAuth and organization plugin options
 * (today) **jakebailey** added label `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3614826616) **Azzerty23** provided a TypeScript code example demonstrating type inference differences in BetterAuth plugin options and related generic functions

### [Issue microsoft/TypeScript-go#2175](https://github.com/microsoft/TypeScript-go/issues/2175) (Closed, `Domain: Editor`)

**tsgo doesn't suggest \(autoimport\) of packages in monorepo and tries to use relative path in vscode**

*tsgo’s autoimport in a monorepo bypasses configured package paths and suggests incorrect deep relative imports instead of package names.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2175#issuecomment-3606234082) **cbovis** said "Same issue here in a pnpm monorepo."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2175#issuecomment-3610055139) **jakebailey** said "I would suspect this was fixed by #1902; I would retry with the next nightly build tomorrow."
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2175#issuecomment-3613213110) **darklight9811** said "@jakebailey it did fix for me"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2175#issuecomment-3613220148) **jakebailey** said "Great, thanks."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2177](https://github.com/microsoft/TypeScript-go/issues/2177) (Closed, `Domain: Editor`, **Copilot**)

**Differences/issues with Code Lens references**

*CodeLens shows 70 references in TS mode but only 31 in TSGO mode for the same GitLens file, indicating inconsistent reference counts.*

 * **eamodio** added label `Domain: Editor`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3609416929) **DanielRosenwasser** explained the difference between client-side and server-side find-all-references implementations and asked if the user saw 70ish references in 5.9 vs 31ish in 7.0
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3609419007) **DanielRosenwasser** said "(the other reason it might differ is the way that we support IncludeDeclarations: false, and how that might differ with filtering out the isDefinition property that the Strada codebase has)"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3613785267) **eamodio** said "So in 5.9, I see 70 references in the CodeLens, and 71 in find-all-references, in 7.0, I see 31 references in the CodeLens, and 71 in find-all-references"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3614149905) **DanielRosenwasser** suggested wiring up find-all-references across projects similarly to server requests and provided a sample fourslash test as a starting example
 * **DanielRosenwasser** assigned to **Copilot**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3614212798) **sheetalkamat** said "I am working on cross project implememtations and code lens right now"

### [Issue microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189) (Open, `Domain: Editor`, **andrewbranch**)

**LSP doesn't offer auto\-importing packages**

*VS Code’s TypeScript LSP does not offer auto-import suggestions for installed packages like `typescript-result`, only built-in modules*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3607794925) **GeordiD** reported that the experimental server didn't suggest imports for external packages or via quick-fix, and offered to create a reproduction with provided version details
 * **RyanCavanaugh** assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3611385456) **jansedlon** mentioned that PR 1902 fixed most tsgo issues, noted slow autocomplete in a medium-sized project, and asked why autocomplete was slower in apps/web compared to TypeScript native
 * [today](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3613871889) **andrewbranch** explained redesigning the auto-import backend and asked if the project was open source for testing on monorepos
 * [today](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3614124821) **jansedlon** answered that the project was closed-source

### [Issue microsoft/TypeScript-go#2196](https://github.com/microsoft/TypeScript-go/issues/2196) (Closed, `Domain: Editor`, **Copilot**)

**No "recommended" completion entry when outer context is incomplete ternary conditional operator**

*TypeScript suggests the wrong enum (Bar instead of Foo) when invoking completions in an incomplete ternary expression.*

 * created by **mjbvz**
 * (yesterday) **jakebailey** added label `Domain: Editor`, and assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2211](https://github.com/microsoft/TypeScript-go/pull/2211) (Closed, **jakebailey**, **Copilot**)

**Fix completion preselection in ternary conditional expressions**

*Fix code completion to preselect the expected contextual type within incomplete ternary conditionals in function calls.*

 * created by **Copilot**
 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2212](https://github.com/microsoft/TypeScript-go/issues/2212) (Open)

**Incorrect import elision when enum value references another enum from a different module**

*tsgo wrongly elides imports when an enum references values from another module's enum, causing undefined runtime errors.*

 * created by **thaoula**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3614257195) **a-tarasyuk** asked whether version 5.9 emitted require calls or only the evaluated values
 * [today](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3615023529) **thaoula** provided the real source files to correct the previous code and acknowledged that @a-tarasyuk was correct
 * [today](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3615034725) **thaoula** said "I have updated my original post because my cut down example was actually incorrect"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3617371086) **a-tarasyuk** asked whether the extracted evaluator should evaluate the expression or preserve imports, noting that entity evaluation currently didn’t support alias resolution or import preservation
 * [later](https://github.com/microsoft/TypeScript-go/issues/2212#issuecomment-3617384891) **jakebailey** explained that enums were initially handled without const inlining but recommended restoring the previous behavior

### [Issue microsoft/TypeScript-go#2214](https://github.com/microsoft/TypeScript-go/issues/2214) (Open)

**TS2304 when consuming a non\-module global namespace object**

*tsgo fails to resolve a non-module global namespace defined in a referenced composite project, causing TS2304 in the consuming module.*

 * [today](https://github.com/microsoft/TypeScript-go/issues/2214#issuecomment-3612585349) **jakebailey** explained that 'none' as a module setting was removed and asked if moduleDetection=legacy was intended
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/2214#issuecomment-3613017603) **HolgerJeromin** thanked the previous commenter and explained switching from module:none to moduleDetection:legacy didn't resolve the namespace issue, and noted that module:none was removed as per issue #2085

### [Issue microsoft/TypeScript-go#2215](https://github.com/microsoft/TypeScript-go/issues/2215) (Open)

**TS1323: Dynamic imports are not supported when targeting \`"module": "None"\`**

*tsgo reports TS1323 when using dynamic imports in a project with module 'None' despite TypeScript 5.9 support.*

 * created by **HolgerJeromin**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3612604119) **jakebailey** said "See also https://github.com/microsoft/typescript-go/issues/2214#issuecomment-3612585349"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3612606763) **jakebailey** said "I don't quite understand "module none" yet using imports. Why not another mode?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3613054881) **HolgerJeromin** explained migrating code to modules with backwards compatibility, using dynamic imports for mixed module and non-module code, and reported that updating to moduleDetection: 'legacy' did not resolve the compile error

### [Issue microsoft/TypeScript-go#2216](https://github.com/microsoft/TypeScript-go/issues/2216) (Open, `Domain: Declaration Emit`, **weswigham**)

**TS4094 exported anonymous class type may not be private or protected**

*tsgo throws TS4094 errors when exporting a function using the Region type from wavesurfer.js because its anonymous class includes private or protected members.*

 * created by **nil1511**
 * (later) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2217](https://github.com/microsoft/TypeScript-go/issues/2217) (Closed, `Domain: Declaration Emit`, **weswigham**)

**Readonly properties do not use constant type**

*tsgo generates readonly properties with overly broad types instead of preserving their constant literal or enum member types.*

 * created by **brokenmass**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2217#issuecomment-3613185112) **ahejlsberg** said "This looks to be a problem in emit. The checker infers the correct literal types for the properties."
 * (today) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2217#issuecomment-3613206466) **brokenmass** identified incorrect comparison in util.go and suggested changing '!= 0' to '== 0' in canHaveLiteralInitializer
 * [today](https://github.com/microsoft/TypeScript-go/issues/2217#issuecomment-3613407244) **jakebailey** said "Yes indeed, thanks! https://github.com/microsoft/typescript-go/pull/2219"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2217#issuecomment-3613483406) **brokenmass** said "I just noticed this issue : https://github.com/microsoft/typescript-go/issues/989 it should be a duplicated. "
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2218](https://github.com/microsoft/TypeScript-go/issues/2218) (Closed, `Domain: Type Checking`, `Crash`, **ahejlsberg**, **Copilot**)

**Panic on initial attempt of existing JavaScript \+ JSDoc project**

*typescript-go crashes with a nil pointer dereference panic when processing an existing JavaScript and JSDoc project.*

 * created by **jbrimeyer-leepfrog**
 * **jbrimeyer-leepfrog** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3613380876) **jakebailey** said "I don't think this is enough information for us to investigate. Do you have the code?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3613398372) **jbrimeyer-leepfrog** said "I do, but I cannot provide the source here. Suggestions on how to provide more information to track this down?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3613416246) **jakebailey** said "You'll probably need to start deleting code out of your project until you find the code that's breaking things."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3613574354) **jbrimeyer-leepfrog** provided a code snippet and repro steps that triggered a tsgo panic
 * **jakebailey** assigned to **Copilot**
 * (later) **ahejlsberg** added label `Domain: Type Checking`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#2219](https://github.com/microsoft/TypeScript-go/pull/2219) (Closed)

**Fix canHaveLiteralInitializer misport**

*Fix misported canHaveLiteralInitializer logic to correctly handle literal initializers.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2219#issuecomment-3613475940) **brokenmass** said "LGTM, thanks !"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2220](https://github.com/microsoft/TypeScript-go/issues/2220) (Open)

**\[pnpm\] The inferred type of 'xxx' cannot be named without a reference to '\.pnpm/xxx'**

*tsgo 7.0.0-dev errors on inferring return types from PNPM-installed packages, requiring explicit annotations due to unnameable ".pnpm" path references.*

 * created by **aramissennyeydd**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3614121652) **samdcoding** said "+1 we are seeing quite a few of these errors as well"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2220#issuecomment-3614655373) **brokenmass** showed that updating the customRender signature removed the error and detailed the inferred versus expected types

### [PR microsoft/TypeScript-go#2221](https://github.com/microsoft/TypeScript-go/pull/2221) (Closed, **jakebailey**, **Copilot**)

**Fix panic by restricting @overload to legal contexts in JSDoc**

*Restrict JSDoc @overload to function, class, and interface methods to prevent AST panics and report errors for invalid contexts.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3613801808) **jakebailey** noted that the fix was just a band-aid and suggested that the reparser's overload handling was causing an incorrect AST node hierarchy
 * [today](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3613902307) **Copilot** stated that the reparser was incorrectly creating synthetic MethodDeclaration nodes for @overload tags and fixed it in commit 7d45569 by keeping overload information in the JSDoc structure
 * [today](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3613919781) **jakebailey** questioned whether overloads on object literal methods are allowed in TypeScript and if they should be banned in JS

### [Issue microsoft/TypeScript-go#2222](https://github.com/microsoft/TypeScript-go/issues/2222) (Closed, `Domain: Editor`)

**autocomplete references packages don't exist in context on a monorepo**

*In a monorepo, packages without declared dependencies lack autocompletion in TypeScript 5.9, and tsgo suggestions lead to missing dependency errors.*

 * created by **darklight9811**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2222#issuecomment-3613971528) **darklight9811** said "@jakebailey @chase I don't know if its easier for you to work on this since its related to the other issue"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2222#issuecomment-3613983304) **jakebailey** said "@andrewbranch is completely rewriting the auto import system, so I would not expect this to be worked on until that is in (and it may not even reproduce)."
 * **jakebailey** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2222#issuecomment-3614108181) **andrewbranch** said "I'm going to consider #2189 the canonical issue for this"
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#2223](https://github.com/microsoft/TypeScript-go/issues/2223) (Open, `Domain: Editor`)

**Request textDocument/foldingRange failed\.**

*The TypeScript language server panics with a token cache mismatch error when requesting folding ranges in a compiled JavaScript file.*

 * created by **eamodio**
 * **eamodio** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2223#issuecomment-3614758634) **jakebailey** described also encountering the issue in a .ncurc.cjs file and struggling to integrate it into a fourslash test suite

### [PR microsoft/TypeScript-go#2224](https://github.com/microsoft/TypeScript-go/pull/2224) (Closed, **sheetalkamat**, **Copilot**)

**Store processing diagnostics on task instead of includeProcessor during file loading**

*Refactor file loading to accumulate processing diagnostics on tasks rather than in the includeProcessor.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript-go#2225](https://github.com/microsoft/TypeScript-go/pull/2225) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix CodeLens references to search across project references**

*Modify CodeLens to count references across projects by using a unified multi-project search helper.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2225#issuecomment-3614946561) **Copilot** refactored the code to extract multi-project search logic into a reusable helper and updated handlers to use it

### [Issue microsoft/TypeScript-go#2226](https://github.com/microsoft/TypeScript-go/issues/2226) (Closed)

**tsgo not respecting skipLibCheck**

*tsgo ignores skipLibCheck and reports interface extension errors that tsc normally suppresses.*

 * created by **joshcartme**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2226#issuecomment-3614210124) **joshcartme** said "I did some searching and this started happening with the Nov 21 release."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2226#issuecomment-3614225636) **jakebailey** clarified that errors should be issued regardless of file check order, discouraged using skipLibCheck to silence errors, recommended using ts-expect-error in user code, and noted error positioning can vary by editor behavior
 * [today](https://github.com/microsoft/TypeScript-go/issues/2226#issuecomment-3614609697) **joshcartme** said "@jakebailey makes sense!  We'll either fix our busted types or expect an error.  Thanks"
 * (today) **joshcartme** closed the issue

### [Issue microsoft/TypeScript-go#2227](https://github.com/microsoft/TypeScript-go/issues/2227) (Open, `Domain: Editor`)

**Port \`move to file\` refactoring**

*Reintroduce the Move to file refactoring from TypeScript 6 into the language server to restore essential automated code relocation functionality.*

 * created by **mjbvz**

### [Issue microsoft/TypeScript-go#2228](https://github.com/microsoft/TypeScript-go/issues/2228) (Open, `Domain: Editor`, **gabritto**)

**No JS Doc template completions**

*The ts-go extension lacks support for the JSDoc template completion feature introduced in TypeScript 6.0 for VSCode.*

 * created by **mjbvz**

### [Issue microsoft/TypeScript-go#2229](https://github.com/microsoft/TypeScript-go/issues/2229) (Open, `Domain: Editor`, **Copilot**)

**Should not allow renaming keywords**

*TS-go erroneously permits renaming on keywords and parentheses instead of failing early via prepareRename*

 * created by **mjbvz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2229#issuecomment-3614402370) **mjbvz** said "In 6.0 we do allow triggering renames on class and similar keywords but this shifts the rename to the class name instead"
 * **jakebailey** assigned to **Copilot**

### [Issue microsoft/TypeScript-go#2230](https://github.com/microsoft/TypeScript-go/issues/2230) (Open, `Domain: Editor`, **Copilot**)

**Should not allow renaming parts of the standard library**

*Prevent users from renaming built-in standard library functions like setTimeout.*

 * created by **mjbvz**
 * (today) **mjbvz** added label `Crash`, and removed label `Crash`
 * **jakebailey** assigned to **Copilot**

### [PR microsoft/TypeScript-go#2231](https://github.com/microsoft/TypeScript-go/pull/2231) (Open, **jakebailey**, **Copilot**)

**Prevent renaming keywords by validating in handleRename**

*Implement validation in handleRename to block renames on keywords or invalid targets, return localized errors, and update tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2232](https://github.com/microsoft/TypeScript-go/pull/2232) (Open, **jakebailey**, **Copilot**)

**Prevent renaming standard library symbols**

*Add early validation to detect and block rename operations on symbols defined in TypeScript’s standard library, aligning with TypeScript’s rename semantics.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2233](https://github.com/microsoft/TypeScript-go/issues/2233) (Open, `Domain: Declaration Emit`, **weswigham**)

**Project references indirect dependencies: Error 2742 Inferred type of xxx \.\.\.**

*tsgo reports a TS2742 error when a package infers a type from an indirect project reference without directly referencing the originating package*

 * created by **johnpyp**
 * (later) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#2234](https://github.com/microsoft/TypeScript-go/issues/2234) (Open)

**tsgo eagerly resolve the type of inferred function Expression**

*tsgo eagerly resolves inferred function expression types, causing Record<keyof TestInterface, string> to collapse to Record<never, string> without explicit annotations.*

 * created by **brokenmass**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614546319) **jakebailey** said "This isn't enough info... in what context are you looking at this? Is this an output problem? what is the tsconfig?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614591815) **brokenmass** apologized for connectivity issues and asked if the provided information was sufficient, and noted that issue #2220 might be related
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614657122) **jakebailey** clarified that the linked issue was unrelated, asked if it referred to declaration emit, and noted missing declaration emit reuse nodes
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614667144) **brokenmass** clarified that the issue is the same as previously shown and explained that tsgo should copy fully annotated functions without additional resolution
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614675362) **jakebailey** said "They are "the same" in that they both involve the fact that declaration emit used to reuse nodes when possible, but currently does not. But the underlying cause is not the same, no."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614689338) **brokenmass** apologized for misunderstanding 'reusing nodes' and asked for clarification, expressed willingness to provide more info, and argued that the emitter shouldn't resolve keyof an exported interface
 * [today](https://github.com/microsoft/TypeScript-go/issues/2234#issuecomment-3614692174) **jakebailey** observed that the emitter resolved keyof exported interfaces until somewhat recently

### [PR microsoft/TypeScript-go#2235](https://github.com/microsoft/TypeScript-go/pull/2235) (Closed)

**Implementations, CodeLens, IncomingCalls across projects**

*Enable CodeLens, Implementations, and IncomingCalls features to work across multiple projects.*

 * created by **sheetalkamat**

### [Issue microsoft/TypeScript-go#2236](https://github.com/microsoft/TypeScript-go/issues/2236) (Open, `Crash`)

**Crashing when project path contains Chinese characters\.**

*VSCode TypeScript Native plugin crashes with a regex compile error when project paths include Chinese characters*

 * created by **CryUshio**
 * **CryUshio** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2236#issuecomment-3615214493) **jakebailey** said "Likely this would be fixed by #1947."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2236#issuecomment-3615214820) **jakebailey** said "A full backtrace would be helpful."

### [Issue microsoft/TypeScript-go#2238](https://github.com/microsoft/TypeScript-go/issues/2238) (Open, `Crash`)

**fatal error: concurrent map read and map write**

*A fatal concurrent map read/write panic occurs in the Typescript-Go link store while resolving import aliases.*

 * created by **charlag**
 * **charlag** added label `Crash`

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Open, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * created by **maxired**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3617221627) **jakebailey** said "Do you have a repo where this reproduces?"

### [PR microsoft/TypeScript-go#2240](https://github.com/microsoft/TypeScript-go/pull/2240) (Closed)

**Fix concurrent map access panic in LinkStore**

*Introduce a read-write mutex and double-check locking in LinkStore to avoid concurrent map access panics.*

 * created by **codeErrorSleep**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2240#issuecomment-3616803819) **codeErrorSleep** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2240#issuecomment-3617133969) **ahejlsberg** pointed out that the submitted fix was incorrect because LinkStore should be local and the panic comes from unintended concurrent checker access
 * [later](https://github.com/microsoft/TypeScript-go/pull/2240#issuecomment-3617300568) **jakebailey** said "Yeah, the fix for this will be totally different; checkers are not concurrency safe."
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2241](https://github.com/microsoft/TypeScript-go/issues/2241) (Closed, `Crash`, **gabritto**, **Copilot**)

**Crash when code contains disposer logic\. Request textDocument/inlayHint failed\.**

*The TypeScript Go LSP panics on inlayHint requests for disposer logic code after encountering an unexpected PropertyAccessExpression.*

 * created by **jinliming2**
 * **jinliming2** added label `Crash`

### [Issue microsoft/TypeScript-go#518](https://github.com/microsoft/TypeScript-go/issues/518) (Open, `Domain: Module Resolution`, `node10 resolution`)

**Cannot find module '??' or its corresponding type declarations\.**

*A dependency’s package.json exports configuration omits a default types mapping, causing TypeScript to fail finding its type declarations.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/issues/518#issuecomment-3009126440) **Cellule** described encountering a similar issue when importing a file not defined in package.json exports and demonstrated a workaround
 * [23 weeks ago](https://github.com/microsoft/TypeScript-go/issues/518#issuecomment-3010022891) **jakebailey** noted that mizchi’s repro matched issue #904 and was fixed; noted that prochri’s and Cellule’s repros used the old node10 resolution and that switching to nodenext surfaces the same TS 5.8 errors, attributing the issue to not supporting node10 resolution
 * **jakebailey** added label `node10 resolution`
 * [today](https://github.com/microsoft/TypeScript-go/issues/518#issuecomment-3615107376) **damiangreen** described following the instructions from the TypeScript blog but encountered a wall of failed imports in a NextJS app and NestJS backend and shared their tsconfig.json
 * [today](https://github.com/microsoft/TypeScript-go/issues/518#issuecomment-3615142974) **jakebailey** said "You can see there are errors in tsconfig.json; baseUrl has been removed. See https://github.com/microsoft/TypeScript/issues/62508#issuecomment-3348649259."

### [Issue microsoft/TypeScript-go#989](https://github.com/microsoft/TypeScript-go/issues/989) (Closed, `Domain: Declaration Emit`)

**d\.ts content different with tsc**

*tsgo outputs static readonly ID typed as string in .d.ts instead of preserving the literal 'XXX' type as tsc does*

 * [26 weeks ago](https://github.com/microsoft/TypeScript-go/issues/989#issuecomment-2922438355) **futurist** observed that tsgo added `| undefined` to an optional constructor parameter in the d.ts output compared to tsc
 * **jakebailey** added label `Declaration emit`
 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/issues/989#issuecomment-3091923365) **futurist** said "any update?"
 * (today) **jakebailey** closed the issue

