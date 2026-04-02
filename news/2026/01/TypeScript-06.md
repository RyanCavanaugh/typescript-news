# Report for 2026-01-06 (Tuesday, January 6th, 2026)

17 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @nnmrts asked why TypeScript handles empty and whitespace strings differently in [microsoft/TypeScript#46109](https://github.com/microsoft/TypeScript/issues/46109#issuecomment-3716204473)
    * @niedzielski asked how to override typing for .json and .schema.json files separately in [microsoft/TypeScript#62924](https://github.com/microsoft/TypeScript/issues/62924#issuecomment-3715894338)
    * @niedzielski explained that they cannot use the suggested workaround and clarified their use case in [microsoft/TypeScript#62924](https://github.com/microsoft/TypeScript/issues/62924#issuecomment-3716377751)
    * @anflext suggested adding an overload for 'X25519' to avoid compile errors for beginners in [microsoft/TypeScript#62926](https://github.com/microsoft/TypeScript/issues/62926#issuecomment-3716873994)
    * @marqdouj asked for suggestions on better configurations in [microsoft/TypeScript#62948](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3715927881)
    * @marqdouj provided setup instructions in [microsoft/TypeScript#62948](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3717118188)
    * @lgarron provided reproduction steps and debug status in [microsoft/TypeScript#62951](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3716073496)
    * @hkleungai asked if there is an ongoing issue to refer to for updates in [microsoft/TypeScript#62959](https://github.com/microsoft/TypeScript/issues/62959#issuecomment-3717831471)

## Activity Summary

### [Issue microsoft/TypeScript#46109](https://github.com/microsoft/TypeScript/issues/46109) (Open, `Needs Investigation`, `Rescheduled`, **ahejlsberg**)

**Do not allow surrounding spaces to be counted as part of ${number} templates in template index strings **

*Prevent surrounding spaces from being included in template literal placeholder matches within TypeScript template index signatures.*

 * (1.4 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [48 weeks ago](https://github.com/microsoft/TypeScript/issues/46109#issuecomment-2628360982) **HansBrende** expressed confusion over the interpretation of 'finite' in string numeric templates, demonstrated inconsistent behavior with Infinity, and suggested adjusting the definition or widening the type to include Infinity
 * [today](https://github.com/microsoft/TypeScript/issues/46109#issuecomment-3716204473) **nnmrts** asked why TypeScript handled empty and whitespace strings differently in number template literal type checks

### [Issue microsoft/TypeScript#46184](https://github.com/microsoft/TypeScript/issues/46184) (Closed, `Suggestion`, `Awaiting More Feedback`)

**Assert value type guard for dynamic object properties**

*Enhance TypeScript assertion type guards to support dynamic object properties and include property names in error messages.*

 * (4.2 years ago) **andrewbranch** added labels `Awaiting More Feedback`, `Suggestion`
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/46184#issuecomment-933868600) **andrewbranch** explained that the request was essentially to recognize `value` as the narrowed type within the assertion operation
 * (later) **cristianrgreco** closed the issue

### [Issue microsoft/TypeScript#62030](https://github.com/microsoft/TypeScript/issues/62030) (Closed, `Needs More Info`)

**VS Code removes trailing comma in export statement**

*VS Code with Format on Save enabled removes the trailing comma in ES module export statements in .mjs files.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3608365001) **craxal** confirmed reproduction of the issue, ran a bisect that did not identify an extension cause, and attached a screenshot
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3662802948) **craxal** said "@RyanCavanaugh Can you reopen this issue, please? As I said above, it still reproduces, and the bisect found nothing."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3697678468) **craxal** said "@RyanCavanaugh Can you please reopen the issue?"
 * [today](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3715653129) **RyanCavanaugh** said "@craxal please set up a repo or something with the needed user settings that repro this in a fresh VS Code install. I still can't repro it locally"
 * [today](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3715694723) **craxal** provided their VS Code user settings and offered to set up a repo later

### [Issue microsoft/TypeScript#62337](https://github.com/microsoft/TypeScript/issues/62337) (Closed)

**Bug in VSCode and Typescript \- TSServer exited\. Code: null\. Signal: SIGTERM \- Even on empty project while tsc build works**

*VSCode’s TypeScript server exits with SIGTERM on startup for any project, including empty ones, despite successful tsc builds*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/62337#issuecomment-3291292619) **Megabyteceer** said "@eliezra236 this extension caused SIGTERM in my case. https://marketplace.visualstudio.com/items?itemName=neotan.vscode-auto-restart-typescript-eslint-servers"
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/62337#issuecomment-3291345983) **eliezra236** said "@Megabyteceer I had this extension in the past, but I uninstalled it, maybe it has some traces"
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/62337#issuecomment-3716602787) **RyanCavanaugh** said "Closing due to language service rewrite. Please log a new issue if this repros in the native preview."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62857](https://github.com/microsoft/TypeScript/issues/62857) (Closed, `Not a Defect`)

**JavaScript IntelliSense does not suggest methods added to built\-in prototypes**

*JavaScript IntelliSense in VS Code fails to suggest custom methods added to built-in prototypes like Promise.log.*

 * (3 weeks ago) **typescript-bot** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3712337535) **MarkMoretto** asked if missing createElement suggestions in VSCode were related to his settings or if it needed its own issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3713529074) **sangafabrice** suggested opening a new issue, explained that VS Code intentionally suggests React-related functions without the package installed, and reported successful testing on Windows 10 with VS Code 1.107.1
 * [later](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3717877495) **sangafabrice** noted that from a vanilla JavaScript perspective method augmentation via prototype felt like a missing feature

### [Issue microsoft/TypeScript#62903](https://github.com/microsoft/TypeScript/issues/62903) (Open, `Needs Investigation`, **andrewbranch**)

**erasableSyntaxOnly: support commonjs require/exports in \.cts files**

*Allow CommonJS require and module.exports syntax inside .cts files when erasableSyntaxOnly is enabled.*

 * created by **Knagis**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#62905](https://github.com/microsoft/TypeScript/issues/62905) (Open, `Suggestion`, `Awaiting More Feedback`)

**Provide a new, simple 'browser' moduleResolution mode for Browser, ESM\-based, non\-bundled projects\.**

*Add a TypeScript Browser moduleResolution mode for ESM projects that only resolves relative and tsconfig-mapped paths and errors otherwise.*

 * created by **freshp86**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62905#issuecomment-3676611464) **HolgerJeromin** expressed surprise that the browser native approach was poorly supported and noted they could not find an eslint rule to catch incorrect auto imports without file extensions
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#62910](https://github.com/microsoft/TypeScript/issues/62910) (Closed, `Not a Defect`)

**\`as\` type assertion fails for \`ReadonlyArray\<T\>\` but succeeds for \`T\[\]\` with identical object literal**

*TypeScript rejects 'as ReadonlyItems' assertions with ReadonlyArray properties but accepts identical 'as MutableItems' assertions.*

 * created by **raymondwang**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62910#issuecomment-3672530315) **Andarist** explained that the underlying cause was the same as in a provided code example, highlighted mismatched nested properties, and linked a related issue
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/62910#issuecomment-3715695939) **RyanCavanaugh** clarified that type assertions only worked when the asserted type subtyped or supertyped the expression type to prevent incorrect assertions

### [Issue microsoft/TypeScript#62919](https://github.com/microsoft/TypeScript/issues/62919) (Open, `Suggestion`, `Awaiting More Feedback`)

**Feature: Const\-literal typing for import\-attribute imports**

*Enable import-attribute imports to infer and preserve constant literal types for JSON modules rather than producing widened types*

 * created by **sinclairzx81**
 * [today](https://github.com/microsoft/TypeScript/issues/62919#issuecomment-3715849479) **RyanCavanaugh** said "What's the difference between this suggestion and #32063? It seems identical in terms of what functionality is being requested?"
 * [today](https://github.com/microsoft/TypeScript/issues/62919#issuecomment-3716196829) **sinclairzx81** clarified that imported JSON attribute types should be treated as constant structures preserving the full document shape, illustrated with examples contrasting union arrays versus fixed tuples, referenced related issues for context, and explained the motivation for parsing JSON as sized constant structures
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#62924](https://github.com/microsoft/TypeScript/issues/62924) (Open, `Suggestion`, `Awaiting More Feedback`)

**Module resolution: ambient JSON wildcard module doesn't override \`resolveJsonModule\` typing**

*Ambient JSON wildcard module declarations (*.schema.json) are overridden by default resolveJsonModule type definitions*

 * created by **niedzielski**
 * [today](https://github.com/microsoft/TypeScript/issues/62924#issuecomment-3715839389) **RyanCavanaugh** questioned what the defect was supposed to be regarding resolveJsonModule behavior
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/62924#issuecomment-3715894338) **niedzielski** described inability to override typing for .json extensions and requested separate typings for plain JSON and schema JSON files
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`, and removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/62924#issuecomment-3716110483) **RyanCavanaugh** explained that wildcard declarations must take priority due to large JSON file size, suggested declaring specific ones instead, and noted that reversing the priority order is unlikely to be implemented
 * [today](https://github.com/microsoft/TypeScript/issues/62924#issuecomment-3716377751) **niedzielski** explained that wildcard declarations did not take priority when resolveJsonModule was enabled and that hardcoding filenames was not feasible

### [Issue microsoft/TypeScript#62926](https://github.com/microsoft/TypeScript/issues/62926) (Closed, `Suggestion`, `Help Wanted`, `Domain: lib.d.ts`, `Experience Enhancement`)

**Add generateKey X25519 CryptoKeyPair**

*Add generateKey support for X25519 algorithm returning CryptoKeyPair to TypeScript DOM definitions to avoid missing publicKey property errors*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62926#issuecomment-3690868058) **anflext** said "💯 OK. I hope soon I don't need hack the extension and node module code."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62926#issuecomment-3691195257) **MartinJohns** explained that the method returns CryptoKey or CryptoKeyPair and suggested using instanceof or a type assertion to access publicKey
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62926#issuecomment-3691855372) **anflext** praised the explanation, mentioned using implicit type conversion and suggested declaring X25519 similarly to Ed25519 to help beginners, and shared an image
 * [today](https://github.com/microsoft/TypeScript/issues/62926#issuecomment-3715806203) **RyanCavanaugh** noted that an overload existed for "Ed25519" and agreed to add one for "X25519" as well
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Help Wanted`, `Domain: lib.d.ts`, `Experience Enhancement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62926#issuecomment-3716873994) **anflext** said "💯  Excelent! If add an overload for "X25519", later new beginner will not break by the compile check error."

### [Issue microsoft/TypeScript#62933](https://github.com/microsoft/TypeScript/issues/62933) (Open, `Bug`, `Domain: check: Type Circularity`)

**Maximum call stack size exceeded in isTypeAssignableTo when using recursive template literal types in a generic context**

*Using recursive template literal types inside a generic context causes checker.isTypeAssignableTo to exceed the maximum call stack size.*

 * created by **mdm317**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62933#issuecomment-3708138963) **Andarist** demonstrated that the same issue could be triggered when typechecking a recursive string literal type example
 * [today](https://github.com/microsoft/TypeScript/issues/62933#issuecomment-3716440620) **RyanCavanaugh** said "Confirmed Andarist's crash repros in TS7"
 * **RyanCavanaugh** added label `Bug`

### [Issue microsoft/TypeScript#62944](https://github.com/microsoft/TypeScript/issues/62944) (Closed, `Suggestion`, `Declined`)

**Allow inferred object literal optional properties**

*Introduce syntax for inferring optional object literal properties (e.g. prop2?) to allow marking certain properties optional during type inference.*

 * (yesterday) **RyanCavanaugh** added labels `Suggestion`, `Declined`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3711959335) **RyanCavanaugh** agreed that zod handles the scenario well and preferred using the partial function as a sufficient workaround
 * [later](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3718672026) **rtcpw** explained encountering optionality issues with zod’s transform when renaming fields, acknowledged a workaround using partial, and noted that TypeScript’s expressiveness feels lacking
 * [later](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3719568811) **MartinJohns** clarified that using z.optional in a transform with renaming lost optionality and that the proposed b?: syntax wouldn’t change the outcome, then acknowledged in an edit that the suggestion could apply to the transform argument

### [Issue microsoft/TypeScript#62948](https://github.com/microsoft/TypeScript/issues/62948) (Closed, `Needs Investigation`, **joj**)

**TypeScript MSBuild Target named GetTypeScriptOutputForPublishing should not include the removed Content files**

*The GetTypeScriptOutputForPublishing MSBuild target ignores Content Remove directives and re-includes generated .js and .d.ts files in the package.*

 * created by **marqdouj**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3707876032) **MartinJohns** advised using fewer search terms and stated the behavior worked correctly with a viable workaround
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3707923154) **marqdouj** reported that after months of troubleshooting a Microsoft engineer helped and planned to submit a ticket to the TypeScript team, and suggested mentioning the solution in the TypeScript documentation
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **joj**
 * [today](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3715699023) **joj** asked whether they were packing TypeScript or JavaScript files and suggested removing GeneratedJavaScript instead of Content or not using the nuget package
 * [today](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3715707838) **joj** clarified that Remove from Content deletes items entirely, proposed a DontInclude item pattern, and asked why generated js is needed if not added to any collection
 * [today](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3715927881) **marqdouj** described experimenting with a TypeScript NuGet package and webpack in a Blazor Azure Maps SDK project, noted loss of IDE features after removing the NuGet package, and asked for configuration suggestions
 * [today](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3716023322) **joj** explained that they use the NuGet package for both IDE support and building and suggested setting `TypeScriptCompileBlocked` to true to prevent compilation and generated files
 * [today](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3716031679) **marqdouj** asked where the TypeScriptCompileBlocked property was, then added it, observed that node_modules stayed visible but the tsgen output folder did not, and said he liked reviewing the generated js
 * [today](https://github.com/microsoft/TypeScript/issues/62948#issuecomment-3717118188) **marqdouj** provided steps to configure a hybrid webpack + ts-loader + tsc build by updating package.json and .csproj

### [Issue microsoft/TypeScript#62951](https://github.com/microsoft/TypeScript/issues/62951) (Closed, `Needs More Info`)

**Preventing \`importScripts\(…\)\` \(ambient declaration\) from being suggested ahead of import statements\.**

*Add a preference to always place import statement completions before ambient importScripts suggestions or remove importScripts from suggestions.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3710282461) **lgarron** described issues with VS Code auto imports and TypeScript file context detection, including missing suggestions, misindexed files, and import completion errors
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3710541153) **guillaumebrunerie** described how to configure TypeScript to recognize web worker files using a separate tsconfig with the WebWorker lib
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3710760059) **lgarron** stated that lib.d.ts includes WebWorker among its default references and listed them
 * [today](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3715745647) **RyanCavanaugh** observed importScripts below import as requested and suggested that another configuration might be causing the issue
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3716073496) **lgarron** described non-deterministic ordering behavior and debug steps involving resetting VS Code settings
 * [today](https://github.com/microsoft/TypeScript/issues/62951#issuecomment-3716103930) **lgarron** closed the issue until a consistent repro was available and thanked @RyanCavanaugh
 * (today) **lgarron** closed the issue

### [Issue microsoft/TypeScript#62952](https://github.com/microsoft/TypeScript/issues/62952) (Closed, `Bug`, `Fixed`)

**Crash: RangeError: Maximum call stack size exceeded in containsReference when a generic ImportType has malformed arguments in a nested conditional**

*TypeScript crashes with a maximum call stack overflow when nested conditional types reference an improperly parameterized import type.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/62952#issuecomment-3716487469) **RyanCavanaugh** reported that the issue was fixed in TS7 but now produces a TS2314 error
 * (today) **RyanCavanaugh** added labels `Bug`, `Fixed`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62956](https://github.com/microsoft/TypeScript/issues/62956) (Closed)

**Wrong warning about Duplicate identifier defined by js\-doc**

*VS Code incorrectly warns of a duplicate identifier for a JSDoc typedef when followed immediately by an IIFE in a JavaScript file.*

 * created by **saeed-serpooshan**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/62956#issuecomment-3715767655) **RyanCavanaugh** said they couldn't reproduce the issue and asked to log a new issue with a reproducible repo
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62957](https://github.com/microsoft/TypeScript/issues/62957) (Closed, `Bug`, `Fixed`)

**Regression: inferred return types in recursive functions are checked incorrectly**

*TypeScript 5.8.3’s regression fails to error when a string-returning callback is passed to a number-returning parameter in recursive functions.*

 * created by **mkantor**
 * [today](https://github.com/microsoft/TypeScript/issues/62957#issuecomment-3716418622) **RyanCavanaugh** said "Bisects to #60208"
 * [today](https://github.com/microsoft/TypeScript/issues/62957#issuecomment-3716432610) **RyanCavanaugh** noted that the bug reproduced in 6.0 nightly but not in 7.0 and suggested marking it fixed in 7.0 instead of reverting the PR
 * **RyanCavanaugh** added label `Fixed`
 * [today](https://github.com/microsoft/TypeScript/issues/62957#issuecomment-3716433884) **RyanCavanaugh** said "cc @ahejlsberg in case you care. Kind of interesting."
 * **RyanCavanaugh** added label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/62957#issuecomment-3716466548) **RyanCavanaugh** said "This all started because of #3276 😵‍💫"
 * [today](https://github.com/microsoft/TypeScript/issues/62957#issuecomment-3716506408) **ahejlsberg** described reworking and simplification of call resolution error logic and confirmed the issue was resolved for 7.0
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62958](https://github.com/microsoft/TypeScript/pull/62958) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Test updates for strict initialization**

*Modifies tests to prevent 'variable used before assignment' errors under default strict initialization through declarations, assertions, initializers, or toggling strictness.*

 * created by **DanielRosenwasser**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**

### [Issue microsoft/TypeScript#62959](https://github.com/microsoft/TypeScript/issues/62959) (Closed)

**Variable with partial record type does not lose its partial\-ness after all its inner attributes are assigned**

*A variable typed as Partial<Record<'a'|'b', {key:string}[]>> retains its partial type after assigning all properties, preventing assignment to a full Record.*

 * created by **hkleungai**
 * [today](https://github.com/microsoft/TypeScript/issues/62959#issuecomment-3717431218) **MartinJohns** marked the issue as a duplicate of #20918 and explained that assigning properties does not create a new type for original, so a Partial<T> can be assigned to a T
 * [later](https://github.com/microsoft/TypeScript/issues/62959#issuecomment-3717831471) **hkleungai** asked if there was an ongoing issue to refer to for updates
 * [later](https://github.com/microsoft/TypeScript/issues/62959#issuecomment-3718105445) **MartinJohns** said "I'm not sure there is one. There's simply nothing they can do. It would be computationally VERY expensive. The compiler would need to track every assignment and create new types upon every assignment."
 * [later](https://github.com/microsoft/TypeScript/issues/62959#issuecomment-3718294998) **MartinJohns** said "#42384 is semi-related, but would very likely happen first."
 * [later](https://github.com/microsoft/TypeScript/issues/62959#issuecomment-3718970294) **jcalz** referred to issue #42384 as the relevant feature request, noted that its implementation would allow property narrowing to propagate to containing objects for free, but warned that it would be expensive and complicate control flow analysis

