# Report for 2026-05-11 (Monday, May 11th, 2026)

16 different users commented on 43 different issues.

## Recommended Actions

 * Response Recommended
    * @AndrewSouthpaw asked what information to collect to help investigate CPU usage issue in [microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4425907817)

## Activity Summary

### [Issue microsoft/TypeScript-go#2193](https://github.com/microsoft/TypeScript-go/issues/2193) (Closed, `Crash`, **jakebailey**)

**"Token cache mismatch: parent" in inlay hints**

*Inlay hints processing panics due to a token cache mismatch for function expression nodes.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2193#issuecomment-3612082813) **IllusionMH** reported concurrent errors for textDocument/inlayHint and textDocument/foldingRange including panic trace for token cache mismatch
 * (20 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2193#issuecomment-4425458229) **jakebailey** said "I think this was fixed by #2789"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3054](https://github.com/microsoft/TypeScript-go/issues/3054) (Closed, `feature parity`, **jakebailey**)

**\`tsgo \-\-generateTrace\` appears unimplemented**

*The tsgo CLI’s documented --generateTrace flag requires an argument but does nothing and fails to produce trace output like tsc.*

 * (6 weeks ago) **RyanCavanaugh** added label `feature parity`, set milestone to `Post-7.0`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3378](https://github.com/microsoft/TypeScript-go/issues/3378) (Open, `Crash`, **jakebailey**, **Copilot**)

**LSP request failure for diagnostics during type serialization**

*The TypeScript language server fails to generate diagnostics during type serialization due to symbol accessibility errors.*

 * (4 days ago) **DanielRosenwasser** set milestone to `TypeScript 7.0 RC`, removed from milestone `Possible Improvement`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3378#issuecomment-4425667471) **jakebailey** said "I have a feeling this was fixed on main already through some other JS related fixes"

### [PR microsoft/TypeScript-go#3379](https://github.com/microsoft/TypeScript-go/pull/3379) (Open, **DanielRosenwasser**, **Copilot**)

**Fix panic in transformCommonJSExport for named non\-default exports**

*Add missing symbol accessibility diagnostic for named non-default CommonJS exports to avoid declaration emit panics and include a test*

 * created by **Copilot**
 * (1 month ago) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3379#issuecomment-4425665109) **jakebailey** said "@copilot+claude-opus-4.7 If you undo your fixes, your test doesn't actually crash."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3379#issuecomment-4425736135) **Copilot** confirmed that reverting the fixes caused the test to pass without crashing, tested various scenarios without reproducing the panic, removed the speculative pre-check, retained the structural fix, adjusted the test to a sanity check, and requested a reproduction case that crashes

### [PR microsoft/TypeScript-go#3435](https://github.com/microsoft/TypeScript-go/pull/3435) (Open)

**Make LS checkers time out after being idle, segment based on use \(take 2\)**

*Reintroduce idle timeouts and usage-based segmentation for language server checkers to improve performance.*

 * (4 days ago) **RyanCavanaugh** set milestone to `Possible Improvement`, and removed from milestone `TypeScript 7.0 RC`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4400627207) **jakebailey** said "It also technically fixes #3638"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4423437253) **gabritto** questioned whether the PR's restriction on concurrent diagnostic requests would matter in practice
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4423528289) **gabritto** said "@typescript-bot test tsserver top200"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4423528862) **typescript-bot** reported CI tests for tsserver top200 as started and provided build and results links
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4425033761) **typescript-bot** reported TS server comparison results showing that the new server no longer reported a panic error and asked to take a look
 * [today](https://github.com/microsoft/TypeScript-go/pull/3435#issuecomment-4425033906) **typescript-bot** reported a panic in textDocument/signatureHelp due to debug assertion "Not a subspan" with accompanying stack trace

### [Issue microsoft/TypeScript-go#3476](https://github.com/microsoft/TypeScript-go/issues/3476) (Closed, `Needs Investigation`, **gabritto**, **Copilot**)

**No error reported when tslib helpers aren't found**

*The TypeScript compiler fails to report errors when tslib helper functions are missing, causing undetected issues.*

 * (6 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * **gabritto** assigned to **Copilot**
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3480](https://github.com/microsoft/TypeScript-go/issues/3480) (Open, `Needs Investigation`, **weswigham**)

**Missing error about jsx\-runtime package**

*Error messages for missing jsx-runtime package are not reported in legacy module detection tests for react-jsx and react-jsxdev*

 * (5 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **weswigham**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3480#issuecomment-4425328982) **weswigham** identified that the jsx import path was not calculable in non-module files, proposed always attempting to add an import in resolveImportsAndModuleAugmentations, and said they would provide a fix after verification

### [Issue microsoft/TypeScript-go#3585](https://github.com/microsoft/TypeScript-go/issues/3585) (Closed, `wontfix`, **weswigham**, **RyanCavanaugh**, **Copilot**)

**Remove extraneous \`declare\` in \.d\.ts output to better match strada**

*Remove extraneous declare modifiers from .d.ts output for both TypeScript and JavaScript*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3585#issuecomment-4409108636) **weswigham** noted that the issue concerned removing all redundant `declare` modifiers from declaration file generation and expressed concern about introducing noisy diffs alongside bugfix changes
 * (3 days ago) **RyanCavanaugh** added label `wontfix`, and removed label `bug`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3638](https://github.com/microsoft/TypeScript-go/issues/3638) (Closed, `Domain: Editor`, `Needs Investigation`, **gabritto**)

**Cannot find name html element\.**

*Closing div tags in .tsx files intermittently trigger “Cannot find name 'div'” errors in VS Code’s TypeScript language server until it’s restarted.*

 * (5 days ago) **RyanCavanaugh** assigned to **gabritto**, and unassigned **andrewbranch**
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3638#issuecomment-4394496405) **jakebailey** said "I suspect #3435 would fix this by way of not sharing checkers."
 * (today) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3692](https://github.com/microsoft/TypeScript-go/issues/3692) (Open, `Needs More Info`)

**Excessive CPU usage**

*WebStorm’s ts-go server often consumes 80-100% CPU when adding new imports in a monorepo frontend until restarted.*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4385893760) **Jelcoo** mentioned that the issue did not occur in VS Code, asked how to manually capture a profile, and noted that CPU spikes halted autocomplete
 * **RyanCavanaugh** added label `Needs More Info`
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4391545891) **RyanCavanaugh** said "We need some clue as to what WebStorm is doing differently - sending different requests, etc?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4425907817) **AndrewSouthpaw** asked what diagnostic information could be collected to help investigate tsgo's high CPU usage
 * [today](https://github.com/microsoft/TypeScript-go/issues/3692#issuecomment-4426707829) **andrewbranch** asked whether the reporter was using WebStorm, suggested reproducing the issue in VS Code and using TypeScript Native Preview commands to gather logs and CPU profiles, and recommended collecting logs and CPU profiles when reproducing in WebStorm

### [PR microsoft/TypeScript-go#3697](https://github.com/microsoft/TypeScript-go/pull/3697) (Closed, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.35\.2 to 4\.35\.4 in the github\-actions group across 1 directory**

*Bump github/codeql-action from version 4.35.2 to 4.35.4 to update the default CodeQL bundle to v2.25.4.*

 * (1 week ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3697#issuecomment-4422603222) **dependabot[bot]** said "Superseded by #3798."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript-go#3703](https://github.com/microsoft/TypeScript-go/pull/3703) (Closed, **jakebailey**)

**Fixes to \-\-generateTrace to make analyze\-trace work**

*Update --generateTrace to use synthetic logical thread IDs for nested events and output per-checker type JSON with mappings for analyze-trace*

 * created by **jakebailey**
 * (4 days ago) **RyanCavanaugh** set milestone to `Possible Improvement`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3705](https://github.com/microsoft/TypeScript-go/pull/3705) (Open, **jakebailey**, **Copilot**)

**Preserve native destructuring for CommonJS exports to keep iterator semantics**

*Preserve native destructuring semantics in CommonJS exports by reusing nodes, suppressing source maps, adding tests, and refining implementation.*

 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4381122415) **blickly** mentioned that they expected destructuring syntax but acknowledged the current version was correct and an improvement
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4381182266) **jakebailey** endorsed the suggestion as it avoids the lexer problem and asked the bots to try it
 * [6 days ago](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4381330720) **Copilot** reworked the code emission to output a lexer-friendly form that preserves array destructuring and emits exports assignments for each declared identifier
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425359927) **jakebailey** said "@copilot+claude-opus-4.7 please consider the review comments"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425437115) **Copilot** addressed three review comments by visiting v.Name() once, adding EFNoSourceMap, and expanding exportDestructuringIterator test cases
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425445877) **jakebailey** said "@copilot+claude-opus-4.7 isn't it a bad idea to reuse the same node twice in the tree? are you sure you've done this correctly?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425472560) **Copilot** explained that the binding pattern node is only placed once and clones are used for export assignments, mirroring existing patterns, and clarified reason for sharing visitedName
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425533988) **jakebailey** said "@copilot+claude-opus-4.6 Address feedback. Also, any new .diff files this PR introduces should be put into submoduleAccepted, with a link back to https://github.com/microsoft/typescript-go/issues/3701"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3705#issuecomment-4425642750) **Copilot** addressed feedback by renaming the `name` parameter to `pattern`, correcting the alias exports comment, relocating new .diff files to submoduleAccepted, and updating submoduleAccepted.txt with a link to issue #3701

### [PR microsoft/TypeScript-go#3731](https://github.com/microsoft/TypeScript-go/pull/3731) (Closed)

**Handle config file diagnostics updates via file watching**

*Enable file-watching for tsconfig.json to update diagnostics for both open and closed projects, ignoring configs outside the workspace or in node_modules.*

 * created by **gabritto**
 * (later) **gabritto** closed the issue

### [Issue microsoft/TypeScript-go#3739](https://github.com/microsoft/TypeScript-go/issues/3739) (Open, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Variable with type \`{}\` can be "wrongly" assigned to Record in tsgo but not in tsc**

*tsgo does not report errors when assigning {} to typed Record<string, ...> types in JavaScript, whereas tsc correctly flags the type mismatch.*

 * **ahejlsberg** assigned to **ahejlsberg**
 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, and set milestone to `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3739#issuecomment-4424583608) **ahejlsberg** described inconsistencies in TS6 and TS7 handling of expando object literals and inferred index signatures
 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3739#issuecomment-4424600997) **ahejlsberg** said "I will put up a PR that consistently implements implied index signatures for expando object literals."

### [Issue microsoft/TypeScript-go#3757](https://github.com/microsoft/TypeScript-go/issues/3757) (Closed, **jakebailey**, **Copilot**)

**Declaration emit renames a method's shadowed type parameter to the outer class generic \(\`Table\` \-\> \`Table\_1\`\)**

*Declaration emit incorrectly renames a method’s shadowed type parameter to the outer class generic, resulting in incorrect .d.ts return types.*

 * created by **Cellule**
 * (4 days ago) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript-go#3761](https://github.com/microsoft/TypeScript-go/pull/3761) (Closed, **jakebailey**, **Copilot**)

**Fix declaration emit renaming a method's shadowed type parameter to the outer generic**

*Declaration emit was renaming a method’s shadowed type parameter to the outer generic due to a missing synthesized-scope check.*

 * created by **Copilot**
 * (4 days ago) **Copilot** assigned to **Copilot**, **jakebailey**
 * **jakebailey** added to milestone `TypeScript 7.0 RC`
 * [today](https://github.com/microsoft/TypeScript-go/pull/3761#issuecomment-4426097444) **jakebailey** said "I'm not sure; I think not? We would have reparsed and not actually operate on these tags."
 * [today](https://github.com/microsoft/TypeScript-go/pull/3761#issuecomment-4426106207) **jakebailey** said "Hm, probably worth sticking in just in case hover gets this"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#3774](https://github.com/microsoft/TypeScript-go/issues/3774) (Closed, `wontfix`)

**Behavior difference: tsgo emit different error codes when it comes to assignability**

*tsgo and tsc produce different TypeScript error codes for identical assignability errors in JavaScript files.*

 * created by **hkleungai**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/3774#issuecomment-4409007324) **RyanCavanaugh** said "This is intended - generally, skipping these produces cleaner output"
 * **RyanCavanaugh** added label `wontfix`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3777](https://github.com/microsoft/TypeScript-go/pull/3777) (Closed)

**Port checks for tslib helpers**

*tslib helper checks now always validate emit helpers and cache requestedExternalEmitHelpers per file for consistent diagnostics.*

 * created by **gabritto**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/3777#issuecomment-4410186212) **jakebailey** said "This seems 1:1 but I think the copilot comments are worth addresssing"
 * (today) **gabritto** closed the issue

### [PR microsoft/TypeScript-go#3781](https://github.com/microsoft/TypeScript-go/pull/3781) (Open, **RyanCavanaugh**, **Copilot**)

**Accept CJS exports pattern baseline diffs**

*Accepted and relocated CommonJS export pattern baseline diffs to reflect new nested export declaration errors.*

 * created by **Copilot**
 * (3 days ago) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4422459647) **jakebailey** said "Alas, merge conflict"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4424382001) **RyanCavanaugh** said "@copilot resolve the merge conflict"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4424518855) **Copilot** resolved the merge conflict in submoduleAccepted.txt by keeping both the late-bound entries from main and the CJS exports entries
 * [today](https://github.com/microsoft/TypeScript-go/pull/3781#issuecomment-4425800473) **jakebailey** said "And then we immediately caused another one"

### [Issue microsoft/TypeScript-go#3791](https://github.com/microsoft/TypeScript-go/issues/3791) (Closed, `Domain: Type Checking`, `Crash`, **ahejlsberg**)

**tsgo panics on a recursive\-mapped\-type \+ intersection \+ generic\-signature pattern**

*tsgo panics during type checking when combining recursive mapped types, intersections, and generic function signatures*

 * (yesterday) **ahejlsberg** added label `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3791#issuecomment-4415501540) **ahejlsberg** said "This assertion failure happens with both tsc and tsgo. A condition that shouldn't be false ends up being so due to an excessive stack depth which the logic doesn't account for."
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#3794](https://github.com/microsoft/TypeScript-go/pull/3794) (Closed)

**Remove assertion that doesn't hold after excessive stack depth overflow**

*Remove assertion that fails after excessive stack depth overflow causing spurious failures*

 * created by **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3794#issuecomment-4420526658) **ahejlsberg** noted that the assertion in reportRelationError can fail due to stack overflows and suggested removing it
 * [today](https://github.com/microsoft/TypeScript-go/pull/3794#issuecomment-4420743416) **ahejlsberg** noted Copilot's successful single-file repro but found it slow and limited to strict:false, decided against adding it to the test suite, and added a cautionary comment about type relation assumptions
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3795](https://github.com/microsoft/TypeScript-go/issues/3795) (Open, `wontfix`)

**tsc & tsgo difference in project reference build order**

*tsgo’s build order compiles the service project before util’s declaration files are emitted, causing import errors on the first build.*

 * created by **SPGoding**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3795#issuecomment-4423010655) **jakebailey** said "This isn't a bug, no? service/src/tsconfig.json does not declare its dependency on the util project, yet uses it."
 * **RyanCavanaugh** added label `wontfix`
 * [today](https://github.com/microsoft/TypeScript-go/issues/3795#issuecomment-4424580108) **RyanCavanaugh** said "We're supposed to have a check that detects this situation and warns you, but I think the nested tsconfig setup here defeats it"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3795#issuecomment-4427512523) **SPGoding** reported that the build passed after moving dependency project references from the parent-level tsconfig.json to the nested src-level tsconfig.json

### [PR microsoft/TypeScript-go#3798](https://github.com/microsoft/TypeScript-go/pull/3798) (Open, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.35\.2 to 4\.35\.4 in the github\-actions group across 1 directory**

*Bump github/codeql-action from version 4.35.2 to 4.35.4 to update the default CodeQL bundle to v2.25.4.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#3799](https://github.com/microsoft/TypeScript-go/issues/3799) (Open, `bug`, `Domain: Editor`, `Crash`)

**Debug assertion violation for document highlights on \`export =\` in merged namespace**

*Requesting document highlights for an `export =` inside a merged namespace triggers an internal debug assertion failure.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, `Crash`

### [Issue microsoft/TypeScript-go#3800](https://github.com/microsoft/TypeScript-go/issues/3800) (Open, `bug`, `Domain: Editor`, `Crash`)

**Error when auto\-importing relative \.css augmentation from ESM file with package\.json**

*Auto-importing a relative CSS augmentation in a NodeNext ESM project triggers a panic due to the unknown .css extension.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, `Crash`

### [Issue microsoft/TypeScript-go#3801](https://github.com/microsoft/TypeScript-go/issues/3801) (Open, `bug`, `Domain: Editor`, `Crash`)

**Unhandled case when auto\-completing decorator on private method under \-\-experimentalDecorators**

*Autocompleting a decorator on a private class method with experimentalDecorators enabled causes a panic due to an unhandled case in getClassElementPropertyKeyType.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `bug`, `Domain: Editor`, `Crash`

### [PR microsoft/TypeScript-go#3802](https://github.com/microsoft/TypeScript-go/pull/3802) (Closed)

**Fix intrinsic jsx tag name case in getTypeAtLocation**

*Remove incorrect identifier checks in getTypeAtLocation for intrinsic JSX tag and attribute names.*

 * created by **gabritto**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3802#issuecomment-4425020623) **DanielRosenwasser** asked whether requesting quick info on `bar` before diagnostics could report that `bar` is not defined
 * (today) **gabritto** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/3802#issuecomment-4425277275) **gabritto** explained that GetTypeOfSymbolAtLocation already adjusts the location to the parent in property access cases

### [PR microsoft/TypeScript-go#3803](https://github.com/microsoft/TypeScript-go/pull/3803) (Open)

**Always generate a jsx implicit import specifier for tsx/jsx files**

*Always generate JSX runtime implicit import specifiers in JSX/TSX files regardless of module status to match Strada*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#3804](https://github.com/microsoft/TypeScript-go/pull/3804) (Open)

**add static property duplicate name check **

*Implement static property duplicate name check to prevent conflicts in property definitions.*

 * created by **iisaduan**

### [Issue microsoft/TypeScript-go#3805](https://github.com/microsoft/TypeScript-go/issues/3805) (Open, `Crash`, **jakebailey**, **Copilot**)

**Panic if there's a circular reference after \`satisfies\`**

*The TypeScript-Go compiler crashes with a stack overflow when resolving a circular type reference after using the satisfies operator.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Crash`
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3805#issuecomment-4430105271) **ahejlsberg** expressed concern about circularity in error reporting and suggested having TypeToString return '?' on recursive invocation to avoid stack overflows

### [Issue microsoft/TypeScript-go#3806](https://github.com/microsoft/TypeScript-go/issues/3806) (Open)

**Intermittent \`TS2307\` on directory imports — \`tsc\` passes, \`tsgo\` intermittently fails on the same tree**

*tsgo intermittently throws TS2307 for parent-directory imports using package.json main with bundler resolution, while tsc passes reliably.*

 * created by **Akshay090**

### [PR microsoft/TypeScript-go#3807](https://github.com/microsoft/TypeScript-go/pull/3807) (Open, **jakebailey**, **Copilot**)

**Fix stack overflow on circular reference after \`satisfies\`**

*Pass checkMode to skip assignability checks in satisfies expressions during serialization to prevent circular stack overflow*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4427875598) **jakebailey** said "@copilot+claude-opus-4.6 is this a porting bug? If not why doesn't Strada hit this?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/3807#issuecomment-4427900074) **Copilot** described the issue as a porting bug and explained why Strada didn’t hit it due to lacking the pseudochecker path, outlining the cyclic call sequence in the Go port

### [PR microsoft/TypeScript-go#3808](https://github.com/microsoft/TypeScript-go/pull/3808) (Open)

**Provide implicit index signatures for JS expando object literals**

*Consistently provide implicit index signatures for JavaScript expando object literals to catch circularity errors with noImplicitAny enabled.*

 * created by **ahejlsberg**

### [Issue microsoft/TypeScript-go#3809](https://github.com/microsoft/TypeScript-go/issues/3809) (Open)

**Enum member after \`NaN\` must have initializer in tsgo, which is not in ts6\.0**

*tsgo incorrectly enforces explicit initializers for enum members after a NaN-valued member, unlike TypeScript 6.0.*

 * created by **Withered-Flower-0422**

### [Issue microsoft/TypeScript-go#3810](https://github.com/microsoft/TypeScript-go/issues/3810) (Open, `Domain: Editor`)

**Deprecated members still shown in dropdown menu with \`editor\.suggest\.showDeprecated\` set to \`false\`**

*Deprecated object member 'a' still appears in the VS Code suggestion dropdown even though editor.suggest.showDeprecated is disabled.*

 * created by **Withered-Flower-0422**
 * **Withered-Flower-0422** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#3811](https://github.com/microsoft/TypeScript-go/issues/3811) (Open, **jakebailey**, **Copilot**)

**\`\.d\.ts\.map\` includes \`sourcesContent\` when \`inlineSources\` is enabled**

*tsgo emits declaration map files containing sourcesContent when inlineSources is enabled, unlike TypeScript which omits them.*

 * created by **jfirebaugh**
 * (later) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#3812](https://github.com/microsoft/TypeScript-go/pull/3812) (Open, **jakebailey**, **Copilot**)

**Exclude sourcesContent from \.d\.ts\.map when inlineSources is enabled**

*Remove inlineSources from the declaration printer options so .d.ts.map files omit sourcesContent when inlineSources is enabled, aligning with TypeScript’s behavior.*

 * created by **Copilot**
 * (later) **Copilot** assigned to **Copilot**, **jakebailey**

### [Issue microsoft/TypeScript-go#3813](https://github.com/microsoft/TypeScript-go/issues/3813) (Open)

**TS2300 on duplicate computed property in type literal, tsc accepts it**

*tsc accepts duplicate computed properties in type literals whereas tsgo incorrectly emits TS2300 errors.*

 * created by **jfirebaugh**

