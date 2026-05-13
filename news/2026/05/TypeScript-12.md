# Report for 2026-05-12 (Tuesday, May 12th, 2026)

8 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @NullVoxPopuli provided confirmation that issue was resolved on version 119 in [microsoft/TypeScript#63367](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4435028177)
    * @DhineshPonnarasan asked for guidance on how to test the bug in TS 7 language service in [microsoft/TypeScript#63463](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4435004904)
    * @DhineshPonnarasan provided repro steps and screenshot as requested in [microsoft/TypeScript#63463](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4440108994)

## Activity Summary

### [Issue microsoft/TypeScript#44589](https://github.com/microsoft/TypeScript/issues/44589) (Open, `Suggestion`, `Awaiting More Feedback`)

**Ability to extend compilerOptions's paths config**

*Support merging compilerOptions.paths in extended tsconfigs so project-specific mappings don’t overwrite base paths.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/44589#issuecomment-1938317780) **dannyfranca** said "Folks, there has been an ongoing proposal since November 2023. Let's contribute to the discussion to help get it going: https://github.com/microsoft/TypeScript/issues/56436"
 * [38 weeks ago](https://github.com/microsoft/TypeScript/issues/44589#issuecomment-3192573848) **Loque18** said "+1 here feature needed ! "
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/44589#issuecomment-3975020711) **x-keyscore** said "+1 here feature needed !"
 * [later](https://github.com/microsoft/TypeScript/issues/44589#issuecomment-4441112072) **benjamind01** said "This is still needed"

### [Issue microsoft/TypeScript#62294](https://github.com/microsoft/TypeScript/issues/62294) (Open, `Bug`, `Help Wanted`, `Domain: Indexed Access Types`)

**Missing error about inability to access conflicting private properties on generic types involving intersections**

*Accessing conflicting private properties on generic intersection types no longer triggers errors.*

 * (37 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Indexed Access Types`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62294#issuecomment-4434072737) **hesam-oxe** volunteered to investigate private property access on intersection types and review relevant checker.ts logic

### [Issue microsoft/TypeScript#62345](https://github.com/microsoft/TypeScript/issues/62345) (Open, `Bug`, `Help Wanted`, `Domain: check: Type Inference`)

**\`silentNeverType\` leak in contextual parameter types coming from anonymous non\-aliased object type instantiations**

*Anonymous object type instantiations leak a silent never type in contextual parameters, causing inconsistent errors across generic functions.*

 * (36 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: Type Inference`, and removed label `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript/issues/62345#issuecomment-4437380088) **bvanjoi** provided another example demonstrating the type inference error and a working workaround using a type alias

### [Issue microsoft/TypeScript#63367](https://github.com/microsoft/TypeScript/issues/63367) (Closed, `Needs More Info`)

**Stuck in initialization loop on v1\.114 w/ TS 5, also on v1\.113 w/ TS 6**

*VSCode repeatedly loops initializing TypeScript configurations for each project in a large pnpm monorepo on v1.114 with TS 5 or v1.113 with TS 6*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4200542561) **RyanCavanaugh** thanked the user and provided an automatically generated list of similar issues
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4200572460) **RyanCavanaugh** said "It's unlikely this would meet the 6.0 patch bar, but it'd be good to have a repo we could clone and check with just to make sure it's not a more widespread root cause."
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4435028177) **NullVoxPopuli** said "tested on 119 and things seem resolved"
 * (today) **NullVoxPopuli** closed the issue

### [Issue microsoft/TypeScript#63463](https://github.com/microsoft/TypeScript/issues/63463) (Open, `Bug`, `Domain: LS: Completion Lists`)

**\`default\` keyword is offered in expression\-bodied arrow function completions**

*TypeScript’s completion engine incorrectly suggests ‘default’ in expression-bodied arrow function contexts despite it being invalid.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4422368020) **RyanCavanaugh** provided an automated analysis listing similar issues and noting that suggesting 'default' after an arrow appeared to be a bug
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4429650763) **DhineshPonnarasan** asked whether the fix qualified for a maintenance-mode exception
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4431677489) **snarbles2** doubted that the issue would be classified as a bug, noting the AI’s inconsistent assessments
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4432954932) **RyanCavanaugh** said "This is not going to meet the 6.0 patch bar. Does this repro in the TS 7 LS?"
 * [today](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4435004904) **DhineshPonnarasan** asked how to test the bug in TS 7 language service and whether to use a local build, wait for the Playground, or other methods
 * [later](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4438556963) **MartinJohns** said "@DhineshPonnarasan See: https://github.com/microsoft/typescript-go#preview"
 * [later](https://github.com/microsoft/TypeScript/issues/63463#issuecomment-4440108994) **DhineshPonnarasan** confirmed reproduction in TS 7 language service preview and showed that invalid statement-oriented keywords like default appeared in expression-bodied arrow function completions

### [Issue microsoft/TypeScript#63469](https://github.com/microsoft/TypeScript/issues/63469) (Closed, `Needs Investigation`, **joj**)

**"TypeScript for Visual Studio" installer not available for 6\.0**

*Users cannot find the TypeScript 6.0 installer for Visual Studio and request clarification on its availability or discontinuation.*

 * created by **wnayes**
 * [today](https://github.com/microsoft/TypeScript/issues/63469#issuecomment-4432297356) **RyanCavanaugh** provided automated analysis and listed similar issues for duplicate checking
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **joj**
 * [today](https://github.com/microsoft/TypeScript/issues/63469#issuecomment-4434168823) **joj** described discontinuation of the SDK beyond TypeScript 5.9, recommended using the NuGet package instead, and asked if there was a scenario where NuGet could not be used
 * [later](https://github.com/microsoft/TypeScript/issues/63469#issuecomment-4442736824) **joj** said "Closing this (by design). Please do comment if this is blocking in any way."
 * (later) **joj** closed the issue

### [PR microsoft/TypeScript#63472](https://github.com/microsoft/TypeScript/pull/63472) (Closed, `For Backlog Bug`)

**Improve label reference diagnostics**

*Enhance break/continue diagnostics to report targeted errors with label declaration spans for same-function forward references.*

 * created by **MukundaKatta**
 * (yesterday) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63472#issuecomment-4433138521) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar."
 * (today) **RyanCavanaugh** closed the issue

