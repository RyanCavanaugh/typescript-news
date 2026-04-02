# Report for 2026-02-08 (Sunday, February 8th, 2026)

16 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @diegohb asked if the change would not happen in [microsoft/TypeScript#55788](https://github.com/microsoft/TypeScript/issues/55788#issuecomment-3869275143)
    * @skirtles-code asked whether there are other cases where the difference would be observable in [microsoft/TypeScript#63061](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3867564681)
    * @dyantako asked for documentation around how this works in [microsoft/TypeScript#63088](https://github.com/microsoft/TypeScript/issues/63088#issuecomment-3868511011)

## Activity Summary

### [Issue microsoft/TypeScript#47658](https://github.com/microsoft/TypeScript/issues/47658) (Closed, `Suggestion`, `Out of Scope`)

**TypeScript Bytecode Interpreter / Runtime Types**

*Proposal for TypeScript runtime type reflection with layered granularity and bytecode interpreter to enhance type availability and performance.*

 * [2.7 years ago](https://github.com/microsoft/TypeScript/issues/47658#issuecomment-1548959747) **sinclairzx81** said "@marcj Hey, still subbed to this thread. TypeRunner looks amazing. Do you plan on publishing a specification for the bytecode?"
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/47658#issuecomment-1906350668) **marcj** said not to plan a bytecode spec, noted having a standardized Deepkit subset, asked what use case was intended for a full TypeRunner-like spec, and explained differences between stack and register machine designs and optimizations
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/47658#issuecomment-1924122984) **M-jerez** proposed a simple reflect API for TypeScript to enable runtime reflection while preserving erasability
 * [later](https://github.com/microsoft/TypeScript/issues/47658#issuecomment-3872359468) **burdiyan** said "Came here to suggest exactly what's described in https://github.com/microsoft/TypeScript/issues/47658#issuecomment-1924122984. Such a shame that this is a non-goal for TypeScript."

### [Issue microsoft/TypeScript#55788](https://github.com/microsoft/TypeScript/issues/55788) (Open, `Suggestion`, `Awaiting More Feedback`)

**Reflect Metadata not supported for TC39 decorators**

*TypeScript does not support retrieving design-time metadata via Reflect.getMetadata for TC39 decorators when experimentalDecorators and emitDecoratorMetadata are disabled.*

 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/55788#issuecomment-1963033322) **artberri** suggested exposing design-time type information in the new TC39 decorator metadata when emitDecoratorMetadata is true because the reflect-metadata API is no longer being standardized after Decorators and Decorator Metadata reached Stage 3 and were implemented in TS >=5.2
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/55788#issuecomment-2041528754) **bcheidemann** agreed with artberri and explained that Decorators and Decorator Metadata reached Stage 3 and are implemented in TS >=5.2, suggested exposing design-time type information with emitDecoratorMetadata in the new TC39 decorator metadata, and mentioned raising a PoC PR requiring minimal changes
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/55788#issuecomment-2092649104) **ianzone** said "Mark https://github.com/nestjs/nest/issues/11414"
 * [today](https://github.com/microsoft/TypeScript/issues/55788#issuecomment-3869275143) **diegohb** said "I take it this will not happen?"
 * [later](https://github.com/microsoft/TypeScript/issues/55788#issuecomment-3871606909) **bcheidemann** referenced a previous comment and noted that decorator metadata in ES decorators is very unlikely

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3863884548) **DanielRosenwasser** thanked justingrant and others for reviewing Temporal, discussed whether polyfill declaration files should be integrated into lib.d.ts, reflected on differing declaration patterns and his oversight in not seeking feedback, and mentioned plans to ship the 6.0 beta soon and address differences thereafter
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3864504776) **Renegade334** asked why bakkot's suggestion didn't work and explained that using type aliases in lib.d.ts hinders forward extensibility, then discussed potential workarounds
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3865491719) **justingrant** expressed support for TS integrating Temporal and suggested contributing polyfill declaration types to lib.d.ts for compatibility, citing existing Temporal TS types and recommending tagging proposal champions
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3867787970) **justingrant** inquired where MDN showed content about custom calendars
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3867845545) **jakebailey** clarified that they had confused custom calendars with non-Gregorian calendars

### [Issue microsoft/TypeScript#63061](https://github.com/microsoft/TypeScript/issues/63061) (Closed, `Not a Defect`)

**\`export type\` vs \`export { type }\` with augmentations**

*export { type } re-exports do not allow module augmentations to access types, unlike export type*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3857354651) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (3 days ago) **typescript-bot** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3864341176) **mkantor** asked for clarification on 'file level' with an example and provided a TypeScript reproduction illustrating module declaration scoping issues
 * [today](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3867564681) **skirtles-code** thanked responders, elaborated with code examples the distinction between local and exported type names in TypeScript, and asked whether other observable differences exist for inline exports

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * **DanielRosenwasser** added label `Planning`
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3847560316) **petamoriken** said "I've submitted a PR to add the ES2025 target (#63046), but will this not be included in TypeScript 6.0?"
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3848220188) **jakebailey** said "You can lump that in with lib.d.ts updates."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868769997) **DanielRosenwasser** said "@typescript-bot create release-6.0"
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868770106) **typescript-bot** reported build jobs starting and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-3868792183) **typescript-bot** said "Hey, @DanielRosenwasser! I've created release-6.0 with version 6.0.0-beta for you."

### [Issue microsoft/TypeScript#63088](https://github.com/microsoft/TypeScript/issues/63088) (Open)

**Function property in union does not get parameter type inferred from result of type narrowing**

*TypeScript does not infer a function property’s parameter type from narrowed union discriminants, defaulting to any.*

 * created by **dyantako**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63088#issuecomment-3848949611) **jcalz** described the issue as possibly a duplicate of #53033 and #47599 and explained that Options isn’t a discriminated union so TypeScript’s narrowing doesn’t apply early enough
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63088#issuecomment-3849859741) **RyanCavanaugh** provided an automated list of similar issues
 * [today](https://github.com/microsoft/TypeScript/issues/63088#issuecomment-3868511011) **dyantako** said "Thanks @jcalz, I suspected that might be the case but I wasn't sure. Is there any documentation around how this works so I can  confirm next time whether something is a bug or behaving as expected?"

### [Issue microsoft/TypeScript#63111](https://github.com/microsoft/TypeScript/issues/63111) (Closed)

**Release announcement post for 4\.5 is broken**

*The TypeScript 4.5 announcement post’s layout on devblogs.microsoft.com is broken due to a missing closing div tag causing formatting errors.*

 * created by **mkantor**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63111#issuecomment-3864434748) **mkantor** noted that the release-notes page didn’t appear broken and asked if the issue should be moved to the microsoft/TypeScript-Website repository
 * [today](https://github.com/microsoft/TypeScript/issues/63111#issuecomment-3868793365) **DanielRosenwasser** acknowledged styling issue, updated announcement posts from 4.5 back to at least 4.2 (possibly 4.1), and noted potential HTTP request trouble
 * [later](https://github.com/microsoft/TypeScript/issues/63111#issuecomment-3871876278) **mkantor** said "The page looks unbroken for me now, thanks!"
 * (later) **mkantor** closed the issue

### [PR microsoft/TypeScript#63113](https://github.com/microsoft/TypeScript/pull/63113) (Closed, `For Backlog Bug`)

**Fix \#13948: preserve narrow types for computed property keys with union literal types**

*Computed property keys with union literal types now distribute over each member, preserving narrow types instead of widening to string.*

 * **typescript-bot** added label `For Backlog Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63113#issuecomment-3866215466) **DukeDeSouth** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63113#issuecomment-3867024821) **mkantor** questioned why the change was desirable given it would typecheck code that causes a runtime error and suggested the type should be a union
 * [today](https://github.com/microsoft/TypeScript/pull/63113#issuecomment-3868235669) **DukeDeSouth** acknowledged an unsoundness issue with computed property types and explained the decision to close the PR
 * (today) **DukeDeSouth** closed the issue

### [PR microsoft/TypeScript#63116](https://github.com/microsoft/TypeScript/pull/63116) (Open, `For Uncommitted Bug`)

**Free \`preProgram\` early in the test harness**

*Freeing preProgram memory early in the test harness to prevent out-of-memory errors when running the full program.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63116#issuecomment-3867403340) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63116#issuecomment-3867683143) **jakebailey** noted no performance benefit and provided before/after psrecord plots
 * [today](https://github.com/microsoft/TypeScript/pull/63116#issuecomment-3868117085) **Andarist** explained that profiling the whole test suite only made the preProgram collectable early within a single test case and that they encountered an OOM when the second program exceeded available heap space because the preProgram was retained by the closure
 * [today](https://github.com/microsoft/TypeScript/pull/63116#issuecomment-3868393278) **Andarist** provided verification steps to reproduce the OOM issue

### [PR microsoft/TypeScript#63117](https://github.com/microsoft/TypeScript/pull/63117) (Open, `For Uncommitted Bug`)

**Properly account for intersections in \`getKeyPropertyName\`**

*Enable getKeyPropertyName to account for intersections and optimize union constituent matching with key properties*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63117#issuecomment-3867720467) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63117#issuecomment-3867729744) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63117#issuecomment-3867729844) **typescript-bot** reported build statuses for four test jobs in a table
 * [today](https://github.com/microsoft/TypeScript/pull/63117#issuecomment-3867779061) **typescript-bot** informed that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/63117#issuecomment-3867795504) **typescript-bot** reported test results comparing main and the PR merge, noted one infrastructure failure but said everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63117#issuecomment-3867915107) **typescript-bot** provided the requested perf run results
 * [today](https://github.com/microsoft/TypeScript/pull/63117#issuecomment-3867997417) **typescript-bot** reported that running the top 400 repos with tsc on main versus the pull request merge showed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63117#issuecomment-3869736934) **Andarist** noted that benchmarks didn't conclusively show an improvement and provided metrics showing reduced assignability cache usage

### [Issue microsoft/TypeScript#63118](https://github.com/microsoft/TypeScript/issues/63118) (Closed)

**type checking only**

*Introduce a tsc --check option that enables cached incremental type checking without emitting any output files.*

 * created by **valler**
 * [today](https://github.com/microsoft/TypeScript/issues/63118#issuecomment-3868112859) **valler** said "Closing. The solution is noEmit in combination with incremental. The combo seams to be supported since 4.0."
 * (today) **valler** closed the issue

### [PR microsoft/TypeScript#63119](https://github.com/microsoft/TypeScript/pull/63119) (Open, `For Uncommitted Bug`)

**Deduplicate repeated declarations on union/intersection properties**

*Exponential cross-product of union/intersection types causes massive duplicate property declarations leading to OOM errors.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63119#issuecomment-3868144933) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63119#issuecomment-3869747792) **Andarist** noted CI timeouts and OOM issues with a union type test, suggested removing it and asked for feedback

### [PR microsoft/TypeScript#63120](https://github.com/microsoft/TypeScript/pull/63120) (Open, `For Backlog Bug`)

**Lift computed property union literal types to union of object types**

*Computed property names with union literal types now yield a union of single-property object types instead of an index signature.*

 * created by **DukeDeSouth**
 * **typescript-bot** added label `For Backlog Bug`

### [Issue microsoft/TypeScript#63121](https://github.com/microsoft/TypeScript/issues/63121) (Open)

**Display files with errors summary in \`\-\-watch\` mode**

*Enhance tsc --watch to display a summary of files with errors and their counts after each compilation*

 * created by **dwjohnston**

### [PR microsoft/TypeScript#63122](https://github.com/microsoft/TypeScript/pull/63122) (Open, `For Uncommitted Bug`)

**Don't attempt to report signature candidate errors on relation overflows**

*Revalidating overload signatures after a complexity-limit overflow can succeed due to warmed caches, causing assertion failures in error reporting.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63122#issuecomment-3868515120) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#63123](https://github.com/microsoft/TypeScript/pull/63123) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.32\.0 to 4\.32\.2 in the github\-actions group**

*Upgrade the github-actions group’s github/codeql-action from version 4.32.0 to 4.32.2 to update the default CodeQL bundle.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63124](https://github.com/microsoft/TypeScript/pull/63124) (Closed, `For Uncommitted Bug`)

**feat\(watch\): show file\-level error summary in watch mode**

*Update watch mode to display a detailed per-file error summary using getErrorSummaryText and a new diagnostic message*

 * created by **suvendukungfu**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63124#issuecomment-3871128563) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

