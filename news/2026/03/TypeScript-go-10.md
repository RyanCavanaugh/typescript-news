# Report for 2026-03-10 (Tuesday, March 10th, 2026)

12 different users commented on 30 different issues.

## Recommended Actions

 * Response Recommended
    * @huseeiin explained that the issue no longer reproduces after migrating to Debian in [microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4039686371)
    * @microsoft-github-policy-service asked the user to agree to the CLA in [microsoft/TypeScript-go#3057](https://github.com/microsoft/TypeScript-go/pull/3057#issuecomment-4035805099)

## Activity Summary

### [Issue microsoft/TypeScript-go#1389](https://github.com/microsoft/TypeScript-go/issues/1389) (Closed, `Domain: Editor`, `Crash`, **Copilot**)

**lsp\(vscode\): panic when formatting a file with multi\-byte characters and trailing 2\+ newlines**

*VSCode's TypeScript (Native Preview) extension panics when formatting files containing multi-byte characters and at least two trailing newlines*

 * (34 weeks ago) **jakebailey** added label `Crash`, and assigned to **Copilot**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1389#issuecomment-3910670391) **apendua** said "I couldn't reproduce it with the latest version from main branch. Could it be that some other fix also resolved this issue? Can you double check?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/1389#issuecomment-4036558993) **heguro** confirmed that the issue was fixed by #1920 and #2370 and explained the root cause and reproduction conditions
 * (today) **heguro** closed the issue

### [PR microsoft/TypeScript-go#2926](https://github.com/microsoft/TypeScript-go/pull/2926) (Closed)

**Implement ES decorator transform \(ESNext \-\> ES2022\)**

*Implement ESNext to ES2022 decorator transformation in tsgo to resolve issue #2354 blocking its adoption.*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4014779355) **jakebailey** asked whether @AlCalzone still wanted to finish the work or if they should push fixes instead
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4015138380) **jakebailey** said "I think I have fixes for a lot of these, very annoying substitutions "
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4016311903) **AlCalzone** offered that others could push changes or take over and asked how to proceed
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4034227613) **jakebailey** requested a re-review after fixing comments, reordering functions, and removing NewNodeVisitor calls outside of construction
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4034277712) **jakebailey** thanked AlCalzone for sending the changes and said everything else seemed good
 * [today](https://github.com/microsoft/TypeScript-go/pull/2926#issuecomment-4036844555) **AlCalzone** said "Thanks for pushing it closer to the finish line!"

### [Issue microsoft/TypeScript-go#3018](https://github.com/microsoft/TypeScript-go/issues/3018) (Closed, `bug`, `Domain: Editor`, **ahejlsberg**)

**No quick info for properties accessed via index signature**

*TypeScript 7.0 fails to show quick info on indexed Record<string,string> properties, expected string|undefined.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3018#issuecomment-4025489330) **ahejlsberg** said "I will be putting up a PR this fixes this as I describe here."
 * (yesterday) **ahejlsberg** added labels `bug`, `Domain: Editor`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3022](https://github.com/microsoft/TypeScript-go/pull/3022) (Closed)

**Provide type\-based quick info on symbol\-less nodes**

*Enable quick info tooltips showing inferred type information for code nodes without associated symbols.*

 * created by **Andarist**
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4025483658) **ahejlsberg** explained that the current fix approach was incorrect and that existing infrastructure for synthetic symbols wasn’t working properly, and said he would submit a PR to fix it
 * [later](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4039906916) **jakebailey** said "is this still needed after #3018?"
 * [later](https://github.com/microsoft/TypeScript-go/pull/3022#issuecomment-4040054101) **Andarist** described the branch as a pure port from Strada, removed failingTests, and noted it was based on issue #3018 so the diff was current

### [Issue microsoft/TypeScript-go#3026](https://github.com/microsoft/TypeScript-go/issues/3026) (Closed, `Domain: Editor`)

**TypeScript Native Preview VS Code extension status bar color is confusing**

*The TypeScript Native Preview VS Code extension shows a yellow status bar for subdirectory projects despite correct tsconfig resolution.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3026#issuecomment-4020459388) **connorshea** asked if the status bar always used the warning color even when nothing was wrong
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3026#issuecomment-4021355125) **DanielRosenwasser** explained that the warning always appeared when native previews were enabled and mentioned plans to replace it with a new non-warning status item
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3026#issuecomment-4021367208) **connorshea** recommended using the beaker icon for experimental status and suggested moving it into the language status with a changed background after assuming it was broken
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3032](https://github.com/microsoft/TypeScript-go/issues/3032) (Closed, `Domain: Editor`, `Needs More Info`)

**tsgo \-\-lsp memory leak on large projects / triggers OOM**

*The tsgo LSP process in the TypeScript Native Preview extension leaks memory when handling large projects, causing OOM on low-RAM Linux machines.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4027150933) **andrewbranch** asked for a heap profile
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4027155579) **andrewbranch** said "Also, please let us know exactly how much memory the native preview is using after loading vs. the exact same set of open files with native preview disabled."
 * **andrewbranch** added label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript-go/issues/3032#issuecomment-4039686371) **huseeiin** reported that the issue no longer reproduced after migrating from Arch to Debian
 * (later) **andrewbranch** closed the issue

### [PR microsoft/TypeScript-go#3037](https://github.com/microsoft/TypeScript-go/pull/3037) (Closed)

**Move extension status entirely into language status bar, drop warning color**

*Integrate extension status into the language status bar without warning color, but struggle with default pinning and visibility.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/3037#issuecomment-4040020713) **jakebailey** admitted should have tested with a real version and noted the result looked bad

### [PR microsoft/TypeScript-go#3038](https://github.com/microsoft/TypeScript-go/pull/3038) (Closed)

**Delete failed lookup locations**

*Remove unused per-import failed lookup location tracking to reduce memory consumption in the compiler host.*

 * created by **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript-go#3040](https://github.com/microsoft/TypeScript-go/issues/3040) (Open, `Domain: Declaration Emit`, **weswigham**)

**\`TS7056\` for exported generic arrow function with return type \(arrow\-only\)**

*Exporting a generic arrow function with a complex return type triggers TS7056 serialization errors under tsgo but not in TypeScript 6.0 or for function declarations.*

 * created by **rubenferreira97**
 * (today) **ahejlsberg** added label `Domain: Declaration Emit`, and assigned to **weswigham**

### [Issue microsoft/TypeScript-go#3043](https://github.com/microsoft/TypeScript-go/issues/3043) (Closed, **jakebailey**, **Copilot**)

**Template literal type inference slices multi\-byte characters by byte instead of UTF\-16 code unit**

*Template literal type inference slices multi-byte characters by byte boundaries rather than UTF-16 code units, causing incorrect type inference.*

 * created by **314systems**
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3044](https://github.com/microsoft/TypeScript-go/issues/3044) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Regex parsing/validation isn't implemented yet**

*tsgo does not report syntax errors in invalid regular expressions that TypeScript 6.0 catches due to missing regex parsing validation*

 * (today) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3044#issuecomment-4032702691) **jakebailey** said "I'm pretty sure this is a part of the unported regex errors and can't be done individually."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3044#issuecomment-4033032398) **Andarist** said "FWIW, I'm working on porting this for some time already: https://github.com/Andarist/typescript-go/tree/port/55600 ;p"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3044#issuecomment-4033046373) **jakebailey** said "Same except I gave up 😄 "

### [Issue microsoft/TypeScript-go#3046](https://github.com/microsoft/TypeScript-go/issues/3046) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Different error from TS6 for unused type parameter**

*TypeScript 6 reports error TS6133 for an unused type parameter while tsgo reports TS6196 instead.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3046#issuecomment-4032864002) **ahejlsberg** said "That was an intended change I made. The old error message didn't make sense. I mean, how do exactly you read the value of a type parameter?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3046#issuecomment-4032877914) **RyanCavanaugh** said "Good point!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3047](https://github.com/microsoft/TypeScript-go/pull/3047) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix unused type parameter diagnostic to use TS6133 instead of TS6196**

*Change unused type parameter diagnostics to use TS6133 and adjust reporting spans and conditions to match TypeScript behavior.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3048](https://github.com/microsoft/TypeScript-go/pull/3048) (Closed)

**Fix Quick Info for element accesses based on index signatures**

*Enhance Quick Info to correctly display types for element access expressions based on index signatures.*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3048#issuecomment-4033298417) **Copilot** said "@ahejlsberg I've opened a new pull request, #3051, to work on those changes. Once the pull request is ready, I'll request review from you."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3049](https://github.com/microsoft/TypeScript-go/issues/3049) (Closed, `bug`, **RyanCavanaugh**, **Copilot**)

**Missing constraint violation message at front of error chain**

*tsgo output omits the initial TS2344 generic constraint violation and directly displays only the missing-property TS2741 error.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** added label `bug`, and assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3049#issuecomment-4032935658) **jakebailey** said "Pretty sure this was also an intentional change"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3049#issuecomment-4032943521) **RyanCavanaugh** said "Why?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3049#issuecomment-4032974779) **jakebailey** said "IIRC because it doesn't communicate anything extra that the last message doesn't, but maybe @ahejlsberg has a better view."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3049#issuecomment-4033844845) **RyanCavanaugh** said "Working as intended"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3050](https://github.com/microsoft/TypeScript-go/pull/3050) (Closed, **RyanCavanaugh**, **Copilot**)

**Fix missing constraint violation error at front of error chain**

*Save and use the original head message in reportRelationError to display explicit constraint violation errors before default messages*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3051](https://github.com/microsoft/TypeScript-go/pull/3051) (Closed, **ahejlsberg**, **Copilot**)

**Add regression test for quick info on index signature mapped type property access**

*Added hover.go fallback and regression test to show quick info for mapped type index signature property access.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3052](https://github.com/microsoft/TypeScript-go/pull/3052) (Closed, **jakebailey**, **Copilot**)

**Fix template literal type inference slicing multi\-byte characters by byte**

*Template literal type inference advanced by bytes instead of runes, causing incorrect slicing of multi-byte characters.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3052#issuecomment-4034308164) **jakebailey** said "@copilot+claude-opus-4.6 Fix the review comments."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3052#issuecomment-4034353490) **Copilot** noted that they fixed review comments in commit f40afd65 by caching getSourceText(seg) in a local variable and regenerating baselines
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3053](https://github.com/microsoft/TypeScript-go/pull/3053) (Open)

**port linked editing**

*Port linked editing functionality and update its regular and baseline fourslash tests.*

 * created by **iisaduan**

### [Issue microsoft/TypeScript-go#3054](https://github.com/microsoft/TypeScript-go/issues/3054) (Open)

**\`tsgo \-\-generateTrace\` appears unimplemented**

*The tsgo CLI’s documented --generateTrace flag requires an argument but does nothing and fails to produce trace output like tsc.*

 * created by **DorianListens**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3054#issuecomment-4035059255) **jakebailey** referred to issue #2914 and suggested trying --pprofDir . while noting it might not be specific enough

### [PR microsoft/TypeScript-go#3055](https://github.com/microsoft/TypeScript-go/pull/3055) (Closed)

**Fix JSX runtime indirect calls**

*Update the JSX runtime to correctly mark indirect calls for proper handling.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3056](https://github.com/microsoft/TypeScript-go/pull/3056) (Closed)

**Replace const with var in CJS emit**

*visitTopLevelExportDeclaration in CJS emit always uses var declarations instead of const, causing inconsistency with other emit paths*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3057](https://github.com/microsoft/TypeScript-go/pull/3057) (Open)

**fix: invalidate symlinked packages in auto\-import cache**

*Auto-import cache now invalidates correctly for symlinked packages by including them in its tracking map.*

 * created by **ericnorris**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3057#issuecomment-4035805099) **microsoft-github-policy-service[bot]** prompted the user to read and agree to the Contributor License Agreement by replying with the appropriate template

### [Issue microsoft/TypeScript-go#3058](https://github.com/microsoft/TypeScript-go/issues/3058) (Closed)

**panic: program not found in counter**

*A panic occurs in programCounter.Deref with 'program not found in counter' when running internal fourslash manual tests*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3058#issuecomment-4036413153) **jakebailey** said "Looking at commits, this began with #2905. @Andarist "
 * [today](https://github.com/microsoft/TypeScript-go/issues/3058#issuecomment-4036481076) **jakebailey** said "go test -count=100 ./internal/fourslash/tests/manual repros it for me fairly consistently."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3058#issuecomment-4036554520) **jakebailey** used GODEBUG to generate a stack trace showing a panic ‘program not found in counter’
 * [later](https://github.com/microsoft/TypeScript-go/issues/3058#issuecomment-4036953105) **jakebailey** said "I have a very complicated fix"

### [PR microsoft/TypeScript-go#3059](https://github.com/microsoft/TypeScript-go/pull/3059) (Closed)

**Fix double deref, races**

*Lock reference counting and snapshot retrieval to prevent races, ensure proper ref/unref handling, and add negative count assertions.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#3060](https://github.com/microsoft/TypeScript-go/pull/3060) (Closed)

**Fix jsnum's Remainder and Exponentiate funcs**

*Update jsnum’s remainder function to handle rounding correctly and refine exponentiation accuracy with Node.js tests.*

 * created by **jakebailey**

