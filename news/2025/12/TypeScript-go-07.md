# Report for 2025-12-07 (Sunday, December 7th, 2025)

12 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @joprice provided additional details about the type error and workaround in [microsoft/TypeScript-go#1968](https://github.com/microsoft/TypeScript-go/issues/1968#issuecomment-3626585535)
    * @kieranm offered private access to their monorepo for volunteer debugging in [microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3623465376)
    * @abelcha provided a repository where the issue reproduces in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3623769762)
    * @abelcha offered to provide logs or traces if needed in [microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3623812556)

## Activity Summary

### [Issue microsoft/TypeScript-go#1968](https://github.com/microsoft/TypeScript-go/issues/1968) (Closed, `Domain: Type Checking`, `Type Ordering`, **ahejlsberg**)

**Type alias circularly references itself error**

*tsgo incorrectly reports a circular reference error for IndentationSubTree defined via Exclude, despite TypeScript 5.8 compiling it*

 * **ahejlsberg** added label `Type Ordering`
 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1968#issuecomment-3468776138) **ahejlsberg** described a property ordering issue between Strada and Corsa, explained how to reproduce the error in each case, and suggested considering explicitly declared properties before inherited ones in Corsa
 * (5 weeks ago) **ahejlsberg** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/1968#issuecomment-3626585535) **joprice** reported the same compilation error when testing tsgo on react-navigation StaticParamList, noted that moving the declaration or removing intersection members fixed it but hadn't minimized the trigger

### [Issue microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162) (Open, `Domain: Type Checking`, **ahejlsberg**)

**Type inference lost for callback parameter**

*Using ts-go configuration causes TypeScript to lose type inference for the organization plugin's sendInvitationEmail callback parameter.*

 * (3 days ago) **jakebailey** added label `Domain: Type Checking`, and assigned to **ahejlsberg**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3614826616) **Azzerty23** provided a TypeScript code example demonstrating type inference differences in BetterAuth plugin options and related generic functions
 * [later](https://github.com/microsoft/TypeScript-go/issues/2162#issuecomment-3627069093) **ahejlsberg** mentioned that it failed with TS 6.0 nightly and provided a repro link

### [Issue microsoft/TypeScript-go#2189](https://github.com/microsoft/TypeScript-go/issues/2189) (Open, `Domain: Editor`, **andrewbranch**)

**LSP doesn't offer auto\-importing packages**

*VS Code’s TypeScript LSP does not offer auto-import suggestions for installed packages like `typescript-result`, only built-in modules*

 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3611385456) **jansedlon** mentioned that PR 1902 fixed most tsgo issues, noted slow autocomplete in a medium-sized project, and asked why autocomplete was slower in apps/web compared to TypeScript native
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3613871889) **andrewbranch** explained redesigning the auto-import backend and asked if the project was open source for testing on monorepos
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3614124821) **jansedlon** answered that the project was closed-source
 * [today](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3623465376) **kieranm** said "We are seeing a bit of slowness with import suggestions right now too. We have a pnpm monorepo which is closed source but we can give access privately if volunteers are needed!"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2189#issuecomment-3627394893) **andrewbranch** said "@kieranm that would be great! If you need an email for me, you can use my first name dot last name @microsoft.com."

### [Issue microsoft/TypeScript-go#2218](https://github.com/microsoft/TypeScript-go/issues/2218) (Closed, `Domain: Type Checking`, `Crash`, **ahejlsberg**, **Copilot**)

**Panic on initial attempt of existing JavaScript \+ JSDoc project**

*typescript-go crashes with a nil pointer dereference panic when processing an existing JavaScript and JSDoc project.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3617748744) **jakebailey** mentioned dumping method overloads into the source file for object methods and questioned whether TypeScript legally supports that syntax
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3617788907) **sandersn** said "I am against hacks. It should be added as a TS language feature in 7.1 if it's important enough of a feature, and then the jsdoc reparsing can be fixed up as needed then for it to work in JS."
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2218#issuecomment-3620720064) **ahejlsberg** described the planned fix to ignore `@overload` tags except on function, method, or constructor declarations outside object literals
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#2239](https://github.com/microsoft/TypeScript-go/issues/2239) (Open, `Needs More Info`)

**take too much memory**

*tsgo extension consumes about 17GB of RAM on macOS M1, causing heavy swapping and slowing VS Code.*

 * created by **maxired**
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3617221627) **jakebailey** said "Do you have a repo where this reproduces?"
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3623769762) **abelcha** described experiencing the same issue with the bun repository
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3623793210) **jakebailey** said "This codebase isn't in JS, so the runtime you use to run it cannot be the problem "
 * [today](https://github.com/microsoft/TypeScript-go/issues/2239#issuecomment-3623812556) **abelcha** clarified that the codebase includes some JS/TS code, resolved the memory issue by disabling the bundled Node resolver in TypeScript settings, and offered to provide logs or traces if needed

### [Issue microsoft/TypeScript-go#2260](https://github.com/microsoft/TypeScript-go/issues/2260) (Open, `Domain: Editor`)

**Inherited methods not merging JSDoc comments**

*tsgo fails to merge inherited JSDoc comments into overridden methods, showing only new @remarks tags.*

 * created by **LukeAbby**
 * [today](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3621939537) **ahejlsberg** agreed that derived methods without JSDoc should inherit from base but cautioned against always merging inherited documentation due to potential confusion
 * [today](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3621953805) **ahejlsberg** explained that the old language service processed summary and remarks sections independently, causing mismatched inherited JSDoc and noted preference for the new behavior
 * [today](https://github.com/microsoft/TypeScript-go/issues/2260#issuecomment-3623586239) **LukeAbby** mentioned they had assumed the behavior was intentional and requested a way to simulate the old behavior with @inheritDoc, noting the pattern’s extensive use and clarifying the summary/remarks merging behavior

### [Issue microsoft/TypeScript-go#2261](https://github.com/microsoft/TypeScript-go/issues/2261) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**regression in 7\.0\.0\-dev\.20251203\.1 \- TS2694 no exported member on namespace**

*Version 7.0.0-dev.20251203.1 of tsgo regresses by reporting TS2694 errors for missing lodash namespace members Dictionary and MutableList.*

 * (today) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, and assigned to **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2263](https://github.com/microsoft/TypeScript-go/pull/2263) (Closed)

**Process \`@overload\` tags only in limited contexts**

*Restrict synthetic overload declarations to functions, methods, and constructors with @overload tags outside object literals and correct parsingContexts flag logic.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2264](https://github.com/microsoft/TypeScript-go/pull/2264) (Closed)

**Fix empty wildcard match on exports**

*Wildcard package.json exports with empty matches (e.g., './foo/*/index.js') cause a slice bounds out-of-range panic when resolving imports*

 * created by **lauckhart**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2264#issuecomment-3622535929) **lauckhart** agreed with microsoft-github-policy-service

### [Issue microsoft/TypeScript-go#2265](https://github.com/microsoft/TypeScript-go/issues/2265) (Open)

**Sourcemap generation consuming significant resources while sourcemaps are disabled**

*tsgo build spends the majority of CPU time in source map emission functions despite sourceMap and declarationMap being disabled.*

 * created by **aem**

### [PR microsoft/TypeScript-go#2266](https://github.com/microsoft/TypeScript-go/pull/2266) (Closed)

**Get merged symbol after resolving indirection alias**

*Add missing getMergedSymbol invocation in resolveIndirectionAlias to fix symbol merging and revert unintended baseline changes.*

 * created by **ahejlsberg**
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#2267](https://github.com/microsoft/TypeScript-go/pull/2267) (Closed)

**Port \-\-stripInternal**

*Add support for the --stripInternal flag to the compiler to remove internal declarations from generated output.*

 * created by **jakebailey**

### [PR microsoft/TypeScript-go#2268](https://github.com/microsoft/TypeScript-go/pull/2268) (Closed)

**\[CHANGES\.md\] replace bitwise\-OR with logical\-OR for expando declarations**

*Use logical OR instead of bitwise OR for expando declarations in CHANGES.md since the current example is unintended and nonfunctional.*

 * created by **k-yle**

### [PR microsoft/TypeScript-go#2269](https://github.com/microsoft/TypeScript-go/pull/2269) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Update GitHub Actions dependencies in the root directory by bumping actions/checkout, setup-node, and codeql-action versions.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [PR microsoft/TypeScript-go#2270](https://github.com/microsoft/TypeScript-go/pull/2270) (Closed)

**Fix a typo in user preference parsing**

*Fix the casing typo in includeInlayFunctionParameterTypeHints so that the user preference is parsed correctly*

 * created by **indietyp**

