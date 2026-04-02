# Report for 2025-12-03 (Wednesday, December 3rd, 2025)

31 different users commented on 51 different issues.

## Recommended Actions

 * Response Recommended
    * @sebastienbarre asked if changes were pushed nightly to npm in [microsoft/TypeScript-go#1034](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3609733899)
    * @samhh asked if the new version includes the closing PR in [microsoft/TypeScript-go#1034](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3611651624)
    * @v-bilyavskiy reported a regression in the latest dev build in [microsoft/TypeScript-go#1034](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612502023)
    * @IllusionMH asked if there was an easy way to compare 'Find all references' results in VS Code using both TS versions in [microsoft/TypeScript-go#1219](https://github.com/microsoft/TypeScript-go/issues/1219#issuecomment-3609061887)
    * @GeordiD provided additional debugging information and offered to create a reproduction in [microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3607794925)
    * @jansedlon asked why autocomplete was slower in apps/web compared to TypeScript native in [microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3611385456)
    * @IllusionMH reported two LSP errors and provided full stack trace in [microsoft/TypeScript-go#2193](https://github.com/microsoft/TypeScript-go/issues/2193#issuecomment-3612082813)

## Activity Summary

### [Issue microsoft/TypeScript-go#1034](https://github.com/microsoft/TypeScript-go/issues/1034) (Closed, `Domain: Declaration Emit`, **weswigham**)

**\[pnpm\] Error 2742 The inferred type of xxx cannot be named**

*Using tsgo instead of tsc triggers TS2742 errors about non-portable inferred types requiring explicit annotations.*

 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3493135338) **dbartholomae** said "Thanks, but I'm not using VSCode, and this wouldn't prevent CI from failing when it checks TypeScript"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3506824110) **colelawrence** reported experiencing the same issue with bun, suspected it was the same underlying problem, and requested that any fix for pnpm-symlinked node_modules also apply to .bun or that an option be provided to ignore the specific error
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3508996659) **JCMais** said "#1902 will fix this for those that are having this error due to pnpm or similar package managers that use symlinks."
 * (today) **andrewbranch** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3609733899) **sebastienbarre** asked if changes were pushed nightly to npm and confirmed they solved their pnpm issues
 * [today](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3609740302) **jakebailey** said "Yes."
 * [later](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3611651624) **samhh** reported updating their pnpm monorepo and asked whether the new version included the closing PR
 * [later](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3611997491) **mithataydogmus** said "Latest release works with pnpm monorepo + react + ts + vite in my case, thanks for all your efforts!"
 * [later](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612502023) **v-bilyavskiy** reported that version 7.0.0-dev.20251204.1 introduced many errors while version 7.0.0-dev.20251203.1 did not under the same cache-clearing conditions
 * [later](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612508042) **codingthat** said "7.0.0-dev.20251204.1 with bun solved the errors here, many thanks!"
 * [later](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612539425) **dbartholomae** said "Solved all of them for me as well"
 * [later](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612549496) **rubnogueira** said "I was having some issues with moment and some specific dependencies, and 7.0.0-dev.20251204.1 solved it for me. Thanks :) "
 * [later](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612581053) **jakebailey** mentioned updating the pnpm monorepo to 7.0.0-dev.20251204.1, noted that 200 type errors remain despite fewer errors, and suggested filing new issues or treating remaining tasks as bug-level work
 * [later](https://github.com/microsoft/TypeScript-go/issues/1034#issuecomment-3612582814) **emanuel-lundman** reported that 7.0.0-dev.20251204.1 with bun solved the errors and yielded a 2x speedup (16s vs 33s and 19s vs 44s) for noEmit type checks on Apple Silicon M1 Max and thanked the effort

### [Issue microsoft/TypeScript-go#1112](https://github.com/microsoft/TypeScript-go/issues/1112) (Closed, `Domain: Editor`, **Copilot**)

**Go\-to\-def on object literal shorthand misbehaves**

*Go-to-definition on object literal shorthand incorrectly navigates to the literal property instead of the parameter or interface definition.*

 * **jakebailey** added label `Domain: Editor`
 * [1 month ago](https://github.com/microsoft/TypeScript-go/issues/1112#issuecomment-3477469773) **jakebailey** said "The correct behavior is to return both the parameter and the interface property; checked against tsserver."
 * **jakebailey** assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1219](https://github.com/microsoft/TypeScript-go/issues/1219) (Closed, `Domain: Editor`)

**\[lsp\]\[bug\] fails to find all references within a single project**

*Finding all references for a symbol used 16k+ times in a 98k-file TypeScript project returns no results.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1219#issuecomment-3092594700) **flazouh** stated that they also didn't see references anymore
 * [7 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1219#issuecomment-3408845213) **mjames-c** provided an update that find refs now returned a partial set of results based on opened editor files
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1219#issuecomment-3564815005) **jakebailey** said "It would be worth it to try again tomorrow in the next nightly; #1991 just fixed a bunch of stuff."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1219#issuecomment-3609061887) **IllusionMH** asked if there was an easy way to compare 'Find all references' results in VS Code using both TS versions
 * [today](https://github.com/microsoft/TypeScript-go/issues/1219#issuecomment-3609067571) **jakebailey** said "No, only one is registered at a time. If you are finding differences and can repro, an issue with that would be very appreciated, because we do not have any repros for these."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1219#issuecomment-3609134262) **mjames-c** said "This seems to be more or less fixed. Closing it out in favour of: https://github.com/microsoft/typescript-go/issues/2204"
 * (today) **mjames-c** closed the issue

### [Issue microsoft/TypeScript-go#1347](https://github.com/microsoft/TypeScript-go/issues/1347) (Closed, `Domain: Declaration Emit`, **Copilot**)

**Destructuring re\-exports using type from symlinked node\-modules results in relative paths used in \`import\(\)\` type**

*Destructuring and re-exporting a function typed by a symlinked module causes TypeScript to emit relative import paths in .d.ts instead of the package specifier.*

 * (22 weeks ago) **jakebailey** added label `Domain: Declaration Emit`, and assigned to **Copilot**
 * [22 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1347#issuecomment-3028196835) **jakebailey** said "Thanks for reporting these, especially for coming up with actual compiler tests."
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#1575](https://github.com/microsoft/TypeScript-go/pull/1575) (Closed)

**perf\(tspath\): avoid string copy in ToFileNameLowerCase**

*Optimize ToFileNameLowerCase by replacing byte slice to string conversion with unsafe.String, boosting performance by 10% and halving allocations.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1575#issuecomment-3194539248) **Gobd** asked whether the new green tea GC in Go 1.25 helps with GC performance
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/pull/1575#issuecomment-3194541428) **camc314** mentioned that the greenteagc flag is still experimental and might not be suitable for production and noted that GC overhead remains high so optimizations are still worthwhile
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1575#issuecomment-3605011875) **jakebailey** said "Old PR, but if you merge main I think we could probably take it..."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#1657](https://github.com/microsoft/TypeScript-go/issues/1657) (Closed, `Domain: Editor`, **iisaduan**)

**tsgo preview: fails to show import suggestions for node modules and packages that are linked through PNPM workspaces**

*tsgo preview fails to suggest imports for node_modules and PNPM workspace packages, unlike TypeScript 5.8.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1657#issuecomment-3429519569) **iisaduan** said "@shinichy This issue was next on my list after what I was currently working on. Thanks for your draft! I will start taking a look at it/will be working on symlink support now"
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1657#issuecomment-3429587547) **tmm1** thanked the previous commenter and referenced a more fleshed-out version by @chase in issue #1902
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1657#issuecomment-3429772600) **iisaduan** said "@tmm1 Thanks for tagging me! I'm beginning to review that one now"
 * (today) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#1902](https://github.com/microsoft/TypeScript-go/pull/1902) (Closed, **iisaduan**)

**Fix \#1034: Improve symlink resolution in module specifier generation**

*Improve module specifier generation by refactoring and extending symlink resolution, including caching, detection, and path handling.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3564831167) **jakebailey** asked if the missing symlink fixes were the code commented out in #1793
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3571573643) **andrewbranch** said "My auto-imports rewrite is not going to go through the same code path, so I’m not sure if it matters much right now. Can you give me an example of a test you’re thinking of?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3574190990) **jakebailey** referenced the skipped tests file for auto import fixes
 * [today](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3608919862) **andrewbranch** explained that those features relied on the package.json auto import provider, bypassed the symlink cache, and were blocked on the auto-imports rewrite that needs to handle symlinks separately
 * [today](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3608945903) **andrewbranch** said "Thank you for getting this started, @shinichy and @chase!"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3609074488) **jakebailey** said "Hm, this ended up failing all of the tests."
 * [today](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3609089007) **andrewbranch** said "Oops, I committed the removal of t.Skip on the test I was debugging"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3609295964) **jakebailey** noted that three tests were being fixed and mentioned that linting needed to be addressed
 * [today](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3609332958) **chase** thanked contributors for completing the work while they got organized
 * [today](https://github.com/microsoft/TypeScript-go/pull/1902#issuecomment-3609597684) **nnnnoel** said "Really appreciate you all guys!! It would be wonderful innovation for pnpm ecosystem 🫶 "
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#1946](https://github.com/microsoft/TypeScript-go/issues/1946) (Open, `Domain: Editor`)

**Support workspace specific typescript version**

*Allow the extension to use a workspace-specific TypeScript version rather than a global one.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3449257178) **deathemperor** clarified that they meant the workspace-specific tsdk and thanked @jakebailey
 * [today](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3605882941) **thien-do** reported that typescript.native-preview.tsdk wasn't being picked up with the nightly compiler and offered a dangerous workaround
 * [today](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3605893813) **thien-do** corrected that it should be the directory rather than the file
 * [today](https://github.com/microsoft/TypeScript-go/issues/1946#issuecomment-3607681749) **jakebailey** said "You shouldn't have to put the platform specific things in there; unless there's a bug, it should work to point it to node_modules/@typescript/native-preview itself..."

### [PR microsoft/TypeScript-go#1949](https://github.com/microsoft/TypeScript-go/pull/1949) (Open, **jakebailey**, **Copilot**)

**Fix signature help applicable span for nested calls**

*Improves signature help applicable span for nested function calls to correctly handle empty argument lists and prioritize outer calls.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3599507732) **Copilot** acknowledged a misunderstanding, clarified that signature help should appear inside inner call parentheses, noted that TestSignatureHelpWithTriggers02 was failing, and said they would investigate and fix the span calculation for empty argument lists
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3604873836) **jakebailey** encouraged copilot to continue and suggested using print debugging with go test -v
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3604913495) **Copilot** fixed the empty argument list span, extended it to include a position, made all signature help tests pass, and planned to add tests for nested calls from issue #1419
 * [today](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3608003427) **jakebailey** said "@copilot your PR is not formatted"
 * [today](https://github.com/microsoft/TypeScript-go/pull/1949#issuecomment-3608039844) **Copilot** fixed formatting by running npx hereby format in commit 41f4bca

### [PR microsoft/TypeScript-go#2000](https://github.com/microsoft/TypeScript-go/pull/2000) (Closed, **jakebailey**, **Copilot**)

**Fix go\-to\-definition for object literal shorthand properties**

*Enable go-to-definition on shorthand object literal properties to include both parameter and interface property declarations.*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2000#issuecomment-3607968978) **jakebailey** said "The fourslash update raced with this, so I had to fix this PR again."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2077](https://github.com/microsoft/TypeScript-go/issues/2077) (Open, `Crash`)

**Inlayhint panic**

*The inlay hint provider panics when handling textDocument/inlayHint requests due to an out-of-range line number.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3558670505) **jakebailey** said "The logs would be super helpful. You can send them to jabaile at microsoft.com."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3567847077) **lukpsaxo** said "I sent full logs+lsp for a panic on friday and then full logs+lsp for the line mismatch panic today. Subject line contains "Logs for tsgo issue 2077""
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3603910306) **rubnogueira** reported a panic with 'Token cache mismatch: parent' error and included a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2077#issuecomment-3607740977) **jakebailey** said "That is an unrelated panic. #2193"

### [Issue microsoft/TypeScript-go#2084](https://github.com/microsoft/TypeScript-go/issues/2084) (Closed, `bug`, **Copilot**)

**Missing error when JS file compiled without allowJs on**

*tsgo silently accepts JavaScript files when allowJs is disabled, missing the expected TS6504 error.*

 * **RyanCavanaugh** added label `bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2084#issuecomment-3536798509) **jakebailey** said "I assume this is https://github.com/microsoft/typescript-go/blob/05f4d69f81d416946ce46a374d91b78c0fbd37c8/testdata/baselines/reference/submodule/compiler/checkJsFiles6.errors.txt.diff#L5"
 * **jakebailey** assigned to **Copilot**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2104](https://github.com/microsoft/TypeScript-go/pull/2104) (Closed, **jakebailey**, **Copilot**)

**Add missing TS6504 diagnostic for JavaScript files without allowJs**

*Add diagnostic TS6504 for JavaScript files when allowJs is disabled in all inclusion scenarios.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3599606585) **jakebailey** reported a data race in includeProcessor concurrent use and provided the stack trace
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3604865836) **jakebailey** said "@copilot See above. Make includeProcessor safe for concurrent use."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3604920586) **Copilot** fixed includeProcessor for concurrent use by adding mutex protection to shared fields, added helper methods for safe access, and verified tests passed with the race detector
 * [today](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3608556883) **jakebailey** said "@copilot Address the comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2104#issuecomment-3608716412) **jakebailey** said "Cleaned this up; PTAL 🙂 "
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2161](https://github.com/microsoft/TypeScript-go/issues/2161) (Closed)

**Inferred function return type is different from TS 5\.9\.3**

*TypeScript 5.9 correctly narrows getItem’s return type, but tsgo erroneously infers it as never causing property access errors.*

 * created by **In3luki**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2161#issuecomment-3607308419) **Andarist** highlighted inconsistency in return type inference introduced by PR #244 and recommended merging an older PR (#58910) to align behaviors
 * [today](https://github.com/microsoft/TypeScript-go/issues/2161#issuecomment-3608575737) **jakebailey** said "Going to close this now; https://github.com/microsoft/TypeScript/pull/58910 is merged and 6.0 will match."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162) (Open, `Domain: Type Checking`, **ahejlsberg**)

**Type inference lost for callback parameter**

*Using ts-go configuration causes TypeScript to lose type inference for the organization plugin's sendInvitationEmail callback parameter.*

 * created by **Azzerty23**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3610135477) **jakebailey** described that only the first `data` parameter was implicitly typed as any in the better-auth example and that removing the return type of `organization` in favor of any made the parameter type work
 * [today](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3610164033) **jakebailey** provided a minimal TypeScript reproduction of the issue with betterAuth and organization plugin options

### [Issue microsoft/TypeScript-go#2175](https://github.com/microsoft/TypeScript-go/issues/2175) (Closed, `Domain: Editor`)

**tsgo doesn't suggest \(autoimport\) of packages in monorepo and tries to use relative path in vscode**

*tsgo’s autoimport in a monorepo bypasses configured package paths and suggests incorrect deep relative imports instead of package names.*

 * created by **darklight9811**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2175#issuecomment-3606234082) **cbovis** said "Same issue here in a pnpm monorepo."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2175#issuecomment-3610055139) **jakebailey** said "I would suspect this was fixed by #1902; I would retry with the next nightly build tomorrow."
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2177](https://github.com/microsoft/TypeScript-go/issues/2177) (Closed, `Domain: Editor`, **Copilot**)

**Differences/issues with Code Lens references**

*CodeLens shows 70 references in TS mode but only 31 in TSGO mode for the same GitLens file, indicating inconsistent reference counts.*

 * created by **eamodio**
 * **eamodio** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3609416929) **DanielRosenwasser** explained the difference between client-side and server-side find-all-references implementations and asked if the user saw 70ish references in 5.9 vs 31ish in 7.0
 * [today](https://github.com/microsoft/TypeScript-go/issues/2177#issuecomment-3609419007) **DanielRosenwasser** said "(the other reason it might differ is the way that we support IncludeDeclarations: false, and how that might differ with filtering out the isDefinition property that the Strada codebase has)"

### [Issue microsoft/TypeScript-go#2187](https://github.com/microsoft/TypeScript-go/issues/2187) (Open, `Domain: Editor`)

**Broken property suggestions due to a successfully contextually typed function**

*When using a contextually typed callback in makeRequest, TypeScript infers QueryParam as unknown and provides incorrect property suggestions.*

 * created by **LukeAbby**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2188](https://github.com/microsoft/TypeScript-go/issues/2188) (Open, `Domain: Editor`)

**Mixins Overrides Drop Documentation**

*TypeScript fails to inherit JSDoc comments when a mixin-derived class overrides a static method.*

 * created by **LukeAbby**
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189) (Open, `Domain: Editor`, **andrewbranch**)

**LSP doesn't offer auto\-importing packages**

*VS Code’s TypeScript LSP does not offer auto-import suggestions for installed packages like `typescript-result`, only built-in modules*

 * created by **jansedlon**
 * **jansedlon** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3607794925) **GeordiD** reported that the experimental server didn't suggest imports for external packages or via quick-fix, and offered to create a reproduction with provided version details
 * **RyanCavanaugh** assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3611385456) **jansedlon** mentioned that PR 1902 fixed most tsgo issues, noted slow autocomplete in a medium-sized project, and asked why autocomplete was slower in apps/web compared to TypeScript native

### [Issue microsoft/TypeScript-go#2190](https://github.com/microsoft/TypeScript-go/issues/2190) (Closed)

**Different Behavior of Overriding Global Interface**

*Adding an optional 'cache' property to the global ImportAttributes interface errors in tsgo but not TypeScript 5.9.*

 * created by **sxzz**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2190#issuecomment-3607572729) **jakebailey** mentioned that the index signature error reproduced in a standalone file matched the old compiler behavior and likely represents a bugfix related to issue #2134
 * [today](https://github.com/microsoft/TypeScript-go/issues/2190#issuecomment-3607595563) **sxzz** said "I see, thanks for your answer!"
 * (today) **sxzz** closed the issue

### [PR microsoft/TypeScript-go#2191](https://github.com/microsoft/TypeScript-go/pull/2191) (Closed)

**fix: Enable getExePath to work on Node 16**

*Enable getExePath compatibility on Node 16 to restore tsgo preview functionality*

 * created by **aapoalas**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3606482159) **aapoalas** said "@microsoft-github-policy-service agree company="Valmet Automation""
 * [today](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3607527921) **jakebailey** said "I guess we could do this, but you should also update package.json's engines."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3607606185) **aapoalas** noted that the package.json file had no engines field
 * [today](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3607619015) **jakebailey** said "There is, in _packages/native-preview/package.json."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2191#issuecomment-3610150040) **aapoalas** thanked for pointing out the file location and fixed the package.json and formatting check

### [PR microsoft/TypeScript-go#2192](https://github.com/microsoft/TypeScript-go/pull/2192) (Closed)

**Don't ask for checker immediately in ProvideCodeActions**

*Remove the unused checker invocation in ProvideCodeActions leftover from a previous iteration.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2193](https://github.com/microsoft/TypeScript-go/issues/2193) (Open, `Crash`)

**"Token cache mismatch: parent" in inlay hints**

*Inlay hints processing panics due to a token cache mismatch for function expression nodes.*

 * created by **jakebailey**
 * **jakebailey** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2193#issuecomment-3612082813) **IllusionMH** reported concurrent errors for textDocument/inlayHint and textDocument/foldingRange including panic trace for token cache mismatch

### [Issue microsoft/TypeScript-go#2194](https://github.com/microsoft/TypeScript-go/issues/2194) (Open, `Domain: Editor`, **Copilot**)

**Destructured interface members lack inherited JSDoc comments**

*Destructured interface members in VS Code fail to display inherited JSDoc hover comments.*

 * created by **Bertie690**
 * **Bertie690** added label `Domain: Editor`
 * **jakebailey** assigned to **Copilot**

### [PR microsoft/TypeScript-go#2195](https://github.com/microsoft/TypeScript-go/pull/2195) (Open, **jakebailey**, **Copilot**)

**Fix missing JSDoc comments on destructured interface properties**

*Display inherited JSDoc comments for destructured interface properties when hovering over them.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2196](https://github.com/microsoft/TypeScript-go/issues/2196) (Closed, `Domain: Editor`, **Copilot**)

**No "recommended" completion entry when outer context is incomplete ternary conditional operator**

*TypeScript suggests the wrong enum (Bar instead of Foo) when invoking completions in an incomplete ternary expression.*

 * created by **mjbvz**
 * (today) **jakebailey** added label `Domain: Editor`, and assigned to **Copilot**

### [PR microsoft/TypeScript-go#2197](https://github.com/microsoft/TypeScript-go/pull/2197) (Closed)

**Make Program diagnostic API clearer**

*Restructure the Program diagnostic API by reducing redundant binding calls, improving diagnostic comparison, and limiting parallel checkers to non-Project programs.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2198](https://github.com/microsoft/TypeScript-go/issues/2198) (Closed, `Crash`)

**InternalError: panic handling request textDocument/foldingRange with jsx using dot notation**

*TypeScript Go language server panics when handling foldingRange requests for JSX code using dot notation property access.*

 * created by **dsafa**
 * **dsafa** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2198#issuecomment-3608741885) **jakebailey** suggested using scanner.GetTextOfNode instead of Text() or implementing Text() on property access expressions
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2199](https://github.com/microsoft/TypeScript-go/pull/2199) (Closed)

**Fix JSX name in folding ranges**

*Restores correct JSX name handling in folding ranges after a previous PR inadvertently broke it.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#2200](https://github.com/microsoft/TypeScript-go/pull/2200) (Closed)

**Use golangci\-lint 2\.7\.0**

*Upgrade to golangci-lint version 2.7.0, removing the workaround introduced in issue #2181.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2201](https://github.com/microsoft/TypeScript-go/issues/2201) (Open, `Crash`, **Copilot**)

**Bad formatting of multiline ternary expression**

*Formatting multiline ternary expressions with tabs results in inconsistent mixing of tabs and spaces.*

 * created by **mjbvz**
 * **mjbvz** added label `Crash`
 * **jakebailey** assigned to **Copilot**

### [PR microsoft/TypeScript-go#2203](https://github.com/microsoft/TypeScript-go/pull/2203) (Open, **jakebailey**, **Copilot**)

**Fix multiline ternary expression formatting with tabs**

*Ensure consistent tab-based indentation for multiline ternary expressions to prevent mixed tabs and spaces.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2203#issuecomment-3609061306) **jakebailey** said "@copilot You forgot to run test/format/lint/etc"
 * [today](https://github.com/microsoft/TypeScript-go/pull/2203#issuecomment-3609108881) **Copilot** fixed formatting, linting, and tests in commit a38bd7ab and confirmed all checks passed

### [Issue microsoft/TypeScript-go#2204](https://github.com/microsoft/TypeScript-go/issues/2204) (Closed, `Domain: Editor`)

**\[bug\] TSGO fails to follow re\-exports when finding references**

*TSGO does not follow re-exports when finding references, preventing accurate cross-module symbol resolution.*

 * created by **mjames-c**
 * **mjames-c** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2205](https://github.com/microsoft/TypeScript-go/issues/2205) (Open, `Domain: Editor`)

**TSGO doesnt read vscode settings json**

*TSGO extension fails to apply VS Code’s typescript.preferences.importModuleSpecifier and updateImportsOnFileMove settings.*

 * created by **lokeshrj**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2205#issuecomment-3609186268) **jakebailey** said "The first one is #1793. The latter is for a feature we don't implement."
 * **jakebailey** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2206](https://github.com/microsoft/TypeScript-go/issues/2206) (Open, `Crash`)

**tried to delete a non\-existent entry  / nil pointer deref on diagnostics**

*A nil pointer dereference panic occurs when attempting to delete a non-existent diagnostics entry during file closure in typescript-go.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`

### [PR microsoft/TypeScript-go#2207](https://github.com/microsoft/TypeScript-go/pull/2207) (Closed)

**Port document symbol tests \+ fixes**

*Port Strada document symbol tests to Corsa baselines, fix failures, support expandos and name truncation, and document remaining differences.*

 * created by **gabritto**

### [Issue microsoft/TypeScript-go#2208](https://github.com/microsoft/TypeScript-go/issues/2208) (Open, `Crash`)

**crash on initial load of a large react\-native/expo project**

*The tsgo language server panics with a nil pointer dereference on initial load of a large React Native/Expo project.*

 * created by **OneOfOne**
 * **OneOfOne** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2208#issuecomment-3609801339) **jakebailey** provided a better-formatted panic stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/2208#issuecomment-3609805062) **jakebailey** noted that in the provided code snippet p.typingsWatch must be nil

### [Issue microsoft/TypeScript-go#2209](https://github.com/microsoft/TypeScript-go/issues/2209) (Open, `Domain: Editor`, **Copilot**)

**\[lsp\] Go to Definition missing getter when property returns callable interface**

*Go to Definition in TypeScript Go Native only returns the callable interface signature, omitting the getter definition.*

 * created by **imbant**
 * (today) **jakebailey** added label `Domain: Editor`, and assigned to **Copilot**

### [PR microsoft/TypeScript-go#2210](https://github.com/microsoft/TypeScript-go/pull/2210) (Open, **jakebailey**, **Copilot**)

**Fix Go to Definition for getters returning callable interfaces**

*Go to Definition on properties returning callable interfaces shows both the call signature and the getter declaration by preserving accessors.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2211](https://github.com/microsoft/TypeScript-go/pull/2211) (Closed, **jakebailey**, **Copilot**)

**Fix completion preselection in ternary conditional expressions**

*Fix code completion to preselect the expected contextual type within incomplete ternary conditionals in function calls.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#2212](https://github.com/microsoft/TypeScript-go/issues/2212) (Open)

**Incorrect import elision when enum value references another enum from a different module**

*tsgo wrongly elides imports when an enum references values from another module's enum, causing undefined runtime errors.*

 * created by **thaoula**

### [Issue microsoft/TypeScript-go#2213](https://github.com/microsoft/TypeScript-go/issues/2213) (Open, `Domain: Editor`)

**unable to restart the tsgo language server, getting timeout**

*Restarting the tsgo language server via VS Code times out and breaks TypeScript features until the extension is disabled.*

 * created by **shmdhussain**
 * **shmdhussain** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#2214](https://github.com/microsoft/TypeScript-go/issues/2214) (Open)

**TS2304 when consuming a non\-module global namespace object**

*tsgo fails to resolve a non-module global namespace defined in a referenced composite project, causing TS2304 in the consuming module.*

 * created by **HolgerJeromin**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2214#issuecomment-3612585349) **jakebailey** explained that 'none' as a module setting was removed and asked if moduleDetection=legacy was intended
 * (later) **jakebailey** closed the issue
 * (later) **jakebailey** reopened the issue

### [Issue microsoft/TypeScript-go#2215](https://github.com/microsoft/TypeScript-go/issues/2215) (Open)

**TS1323: Dynamic imports are not supported when targeting \`"module": "None"\`**

*tsgo reports TS1323 when using dynamic imports in a project with module 'None' despite TypeScript 5.9 support.*

 * created by **HolgerJeromin**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3612604119) **jakebailey** said "See also https://github.com/microsoft/typescript-go/issues/2214#issuecomment-3612585349"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2215#issuecomment-3612606763) **jakebailey** said "I don't quite understand "module none" yet using imports. Why not another mode?"

### [Issue microsoft/TypeScript-go#2216](https://github.com/microsoft/TypeScript-go/issues/2216) (Open, `Domain: Declaration Emit`, **weswigham**)

**TS4094 exported anonymous class type may not be private or protected**

*tsgo throws TS4094 errors when exporting a function using the Region type from wavesurfer.js because its anonymous class includes private or protected members.*

 * created by **nil1511**

