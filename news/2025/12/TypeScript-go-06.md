# Report for 2025-12-06 (Saturday, December 6th, 2025)

8 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @aem asked for feedback on a potential performance bottleneck in .d.ts emission in [microsoft/TypeScript-go#1507](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621274405)
    * @aem reported source map functions consuming significant CPU time despite being disabled in [microsoft/TypeScript-go#1507](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621277862)

## Activity Summary

### [Issue microsoft/TypeScript-go#1507](https://github.com/microsoft/TypeScript-go/issues/1507) (Open, `Needs More Info`, `Domain: Performance`)

**TypeScript\-Go Performance Issue in ci \(github action\)**

*TypeScript-Go’s GitHub Actions CI build runs only 28% faster (57s vs 79s) than tsc instead of the expected 10× speedup*

 * **jakebailey** added label `Domain: Performance`
 * [15 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3201982113) **ChrisWiles** said "So running locally on my mac (2.4 GHz 8-Core Intel Core i9) it is 450% faster, so only slow in ci"
 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3287173503) **hsource** mentioned resolving memory usage issues by using --singleThreaded and tuning GOGC and GOMEMLIMIT settings
 * [today](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621274405) **aem** reported migrating a large codebase to tsgo, observed slower CI performance compared to local, and shared profiling analysis indicating a potential .d.ts emission bottleneck
 * [today](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621277862) **aem** noted that source map-related functions consumed significant CPU time despite being disabled and provided profiling data
 * [today](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621363638) **jakebailey** said "Everyone is posting different problems in this thread. If you are having perf issues, I would suggest opening a new issue and also uploading the profiles created by --pprofDir."
 * [today](https://github.com/microsoft/TypeScript-go/issues/1507#issuecomment-3621450307) **aem** offered to open a new issue and explained the CI vs local resource constraint differences

### [Issue microsoft/TypeScript-go#2218](https://github.com/microsoft/TypeScript-go/issues/2218) (Closed, `Domain: Type Checking`, `Crash`, **ahejlsberg**, **Copilot**)

**Panic on initial attempt of existing JavaScript \+ JSDoc project**

*typescript-go crashes with a nil pointer dereference panic when processing an existing JavaScript and JSDoc project.*

 * **ahejlsberg** added label `Domain: Type Checking`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3617748744) **jakebailey** mentioned dumping method overloads into the source file for object methods and questioned whether TypeScript legally supports that syntax
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3617788907) **sandersn** said "I am against hacks. It should be added as a TS language feature in 7.1 if it's important enough of a feature, and then the jsdoc reparsing can be fixed up as needed then for it to work in JS."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3620720064) **ahejlsberg** described the planned fix to ignore `@overload` tags except on function, method, or constructor declarations outside object literals

### [PR microsoft/TypeScript-go#2221](https://github.com/microsoft/TypeScript-go/pull/2221) (Closed, **jakebailey**, **Copilot**)

**Fix panic by restricting @overload to legal contexts in JSDoc**

*Restrict JSDoc @overload to function, class, and interface methods to prevent AST panics and report errors for invalid contexts.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3617909725) **Copilot** reported that the fix was applied in commit cf45e9c, restricting @overload to function declarations and class/interface methods, ignoring object literal methods, and restoring function overload baselines
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3617930092) **jakebailey** said "@copilot This should not be a silent error. We have a mechanism to issue JSDoc errors in parsing; use that."
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2221#issuecomment-3618123001) **Copilot** described the fix that now reports error TS8110 for @overload on object literal methods using the PCObjectLiteralMembers parsing context
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2245](https://github.com/microsoft/TypeScript-go/issues/2245) (Open, `Domain: JS`, `Crash`, **navya9singh**)

**Folding range crash in JS file for \`exports\.property = CallExpression\(ObjectLiteral\)\`**

*The TypeScript Go LSP panics computing folding ranges for an export assignment call expression with an object literal.*

 * created by **DanielRosenwasser**
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2245#issuecomment-3618910449) **DanielRosenwasser** noted a similar issue using module.exports = {} that caused a token cache mismatch error
 * [today](https://github.com/microsoft/TypeScript-go/issues/2245#issuecomment-3620827969) **DanielRosenwasser** said "Maybe something related to how we re-parse JS constructs for TS?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2245#issuecomment-3621034523) **jakebailey** said "Yes, I think the astnav caching is incorrect given it's only based on positions"

### [Issue microsoft/TypeScript-go#2253](https://github.com/microsoft/TypeScript-go/issues/2253) (Open, `Domain: JS`, `Crash`, **Copilot**)

**Crash completing beginning of property name when preceded by JSDoc**

*Completion requests at the start of a JSDoc-preceded property name cause a nil pointer dereference crash in the TypeScript service.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **DanielRosenwasser** assigned to **Copilot**

### [Issue microsoft/TypeScript-go#2254](https://github.com/microsoft/TypeScript-go/issues/2254) (Closed, `Crash`, **Copilot**)

**Completions crash in call to \`new Map\(\.\.\.\)\`\.**

*Requesting completions at array element positions in new Map(...) triggers an index-out-of-range panic in the typescript-go LSP server.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Crash`
 * **DanielRosenwasser** assigned to **Copilot**

### [PR microsoft/TypeScript-go#2258](https://github.com/microsoft/TypeScript-go/pull/2258) (Closed, **DanielRosenwasser**, **Copilot**)

**Fix completions crash and enable contextual type completions in array literals**

*Prevent completions panic inside array literals (e.g., in Map constructors), enable contextual type-based suggestions for array elements and tuple contexts, and remove incorrect '-1' property completions.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3621466169) **DanielRosenwasser** questioned whether this change belonged in the language service layer and described undesirable completions behavior for union literals
 * [today](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3621466298) **DanielRosenwasser** said "@copilot try to address."
 * [today](https://github.com/microsoft/TypeScript-go/pull/2258#issuecomment-3621474913) **Copilot** addressed completion issues after '[' in array literals by adding special handling for OpenBracketToken and CommaToken in the language service, preventing invalid tokens from reaching the checker and enabling string literal completions, all fixed in commit 90ca278a

### [PR microsoft/TypeScript-go#2259](https://github.com/microsoft/TypeScript-go/pull/2259) (Open, **DanielRosenwasser**, **Copilot**)

**Fix nil pointer dereference in completion at property start after JSDoc**

*Fixed a nil pointer panic when requesting completions at a JSDoc-preceded property start by correcting variable shadowing, adding a nil check, and adding a regression test.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**

### [Issue microsoft/TypeScript-go#2260](https://github.com/microsoft/TypeScript-go/issues/2260) (Open, `Domain: Editor`)

**Inherited methods not merging JSDoc comments**

*tsgo fails to merge inherited JSDoc comments into overridden methods, showing only new @remarks tags.*

 * created by **LukeAbby**
 * [later](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3621939537) **ahejlsberg** agreed that derived methods without JSDoc should inherit from base but cautioned against always merging inherited documentation due to potential confusion
 * [later](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3621953805) **ahejlsberg** explained that the old language service processed summary and remarks sections independently, causing mismatched inherited JSDoc and noted preference for the new behavior

### [Issue microsoft/TypeScript-go#2261](https://github.com/microsoft/TypeScript-go/issues/2261) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**regression in 7\.0\.0\-dev\.20251203\.1 \- TS2694 no exported member on namespace**

*Version 7.0.0-dev.20251203.1 of tsgo regresses by reporting TS2694 errors for missing lodash namespace members Dictionary and MutableList.*

 * created by **lukeapage**
 * (later) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, and assigned to **ahejlsberg**

### [PR microsoft/TypeScript-go#2262](https://github.com/microsoft/TypeScript-go/pull/2262) (Open)

**fix\(2260\): Inherited methods not merging JSDoc comments**

*Inherited methods fail to merge their JSDoc comments, resulting in missing inherited documentation.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript-go#2263](https://github.com/microsoft/TypeScript-go/pull/2263) (Closed)

**Process \`@overload\` tags only in limited contexts**

*Restrict synthetic overload declarations to functions, methods, and constructors with @overload tags outside object literals and correct parsingContexts flag logic.*

 * created by **ahejlsberg**

