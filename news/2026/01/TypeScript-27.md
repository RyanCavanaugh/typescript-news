# Report for 2026-01-27 (Tuesday, January 27th, 2026)

18 different users commented on 20 different issues.

## Recommended Actions

 * Moderation
    * @guilhermesimoes posted rude content in [microsoft/TypeScript#62196](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3807001264)
 * Response Recommended
    * @char asked if the project would be interested in his patch as a pull request in [microsoft/TypeScript#33304](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-3807802305)
    * @samal-rasmussen reported issues with negative start values and the 999 limit in [microsoft/TypeScript#43505](https://github.com/microsoft/TypeScript/issues/43505#issuecomment-3810436639)
    * @wjaspers asked when one would naturally use `Promise.all([...]) as const` in day-to-day work in [microsoft/TypeScript#52601](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3807160968)
    * @fidian asked for explanation of inconsistent typing behavior with Promise.all in [microsoft/TypeScript#52601](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3807404862)

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3797000035) **dead-claudia** explained that the alternative Exact util didn't work because TypeScript lacks negated types and showed how the resulting types resolve
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries

### [Issue microsoft/TypeScript#33304](https://github.com/microsoft/TypeScript/issues/33304) (Open, `Suggestion`, `In Discussion`)

**Type safety with \`TemplateStringsArray\` and tag functions**

*Enhance TypeScript’s TemplateStringsArray interface to accept generic types, enabling type-safe tagged template functions.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-2530279595) **DerekZiemba** described the problem with tagged templates losing literal typing due to TemplateStringsArray widening, explained a hack workaround using JSDoc templates, and provided a detailed code example
 * [43 weeks ago](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-2758397463) **martaver** asked to reconsider the previously shelved PR #45310 given new developments like typescript-go's announcement
 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-2914501602) **justinfagnani** described a use case for Zod 4's template literal types and suggested supporting template literal syntax for z.templateLiteral
 * [today](https://github.com/microsoft/TypeScript/issues/33304#issuecomment-3807802305) **char** proposed a patch to the TypeScript type checker enabling Zod-like const template literal schema inference and asked if it would be welcome as a pull request

### [Issue microsoft/TypeScript#43505](https://github.com/microsoft/TypeScript/issues/43505) (Open, `Suggestion`, `In Discussion`)

**Proposal: Interval Types / Inequality Types**

*Proposal to introduce interval types in TypeScript to enforce numeric range constraints via relational operator-based type narrowing.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/43505#issuecomment-2356515457) **vtgn** explained incorrect type narrowing for a specific if expression and advised to file a new issue if none existed
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/43505#issuecomment-2358834522) **FrameMuse** admitted being too lazy to create a new issue and left the bug report here
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/43505#issuecomment-2358878338) **vtgn** expressed frustration and left the bug report in the current issue despite being told to open a new one
 * [later](https://github.com/microsoft/TypeScript/issues/43505#issuecomment-3810436639) **samal-rasmussen** reported problems with negative ranges and an upper limit of 999 in the NumericRange type

### [Issue microsoft/TypeScript#48571](https://github.com/microsoft/TypeScript/issues/48571) (Open, `Suggestion`, `Help Wanted`, `Domain: Formatter`, `Experience Enhancement`)

**Suggestion: Formatting: Disable inserting spaces around leading semicolon**

*Disable inserting spaces before leading semicolons in TypeScript formatting to avoid inconsistent indentation errors*

 * (3.8 years ago) **RyanCavanaugh** added labels `Domain: Formatter`, `Experience Enhancement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/48571#issuecomment-3807840998) **ackvf** said "Oh wow, I was about to create a new issue to add support for formatting with leading semis and look what I found. Not only was the issue already created. I created it 😂👌👌"

### [Issue microsoft/TypeScript#52601](https://github.com/microsoft/TypeScript/issues/52601) (Closed, `Not a Defect`)

**Promise\.all sometimes infers incorrect types**

*Promise.all sometimes fails to unwrap async function results, causing the returned array items to be typed as Promise<Response> instead of Response.*

 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-1418209381) **JavaScriptBach** identified two Promise.all overloads in separate files that caused array types to match the tuple overload, resolved it by merging the definitions with the array overload first, and asked about TypeScript’s overload resolution across files
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-1421313774) **JavaScriptBach** said "@RyanCavanaugh I've attached a repro to the issue. Hope you or someone else on the team could take a look. Thanks!"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3801831890) **wjaspers** reported that the issue still occurred in TypeScript 5.9.3 and provided a Playground example and a related issue link
 * (today) **RyanCavanaugh** added label `Not a Defect`, and removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3806611522) **RyanCavanaugh** denied that the example was a bug and suggested using 'as const' to fix it, providing a code example
 * [today](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3807160968) **wjaspers** explained that they simplified the reproduction to reduce noise, described encountering multiple async calls with mixed return types, and asked when one would naturally use `Promise.all([...]) as const` in day-to-day work
 * [today](https://github.com/microsoft/TypeScript/issues/52601#issuecomment-3807404862) **fidian** asked why TS5.9.3 lost tuple typing with Promise.all for Promise<string[]> and why workarounds like .then, as const, or extracting to a var restored the correct types

### [PR microsoft/TypeScript#60646](https://github.com/microsoft/TypeScript/pull/60646) (Closed, `For Backlog Bug`)

**Add the type of Intl\.DurationFormat to the lib\.**

*Add initial type definitions for the Intl.DurationFormat API to the TypeScript standard library declarations*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3659820449) **developer-bandi** apologized for the delay and reflected the requested changes in the PR
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3794808977) **petamoriken** said "@developer-bandi The format CI is failing. Could you take a look at it?"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3794844061) **petamoriken** offered to add the ES2025 target via a pull request, asked to take over the existing changes to build upon them, and noted having created the PR with a Co-authored-by commit
 * [later](https://github.com/microsoft/TypeScript/pull/60646#issuecomment-3811124030) **developer-bandi** acknowledged limited availability and agreed to close the issue in favor of the PR
 * (later) **developer-bandi** closed the issue

### [Issue microsoft/TypeScript#62196](https://github.com/microsoft/TypeScript/issues/62196) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **jakebailey**)

**Deprecate \`\-\-target es5\`, make lowest target \`es2015\`**

*Deprecate --target es5 in TypeScript 6.0, raise the minimum target to ES2015, and update library inclusion and downlevel iteration handling.*

 * **RyanCavanaugh** unassigned **iisaduan**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3795462617) **EliasVal** challenged the claim that ES5 environments are vanishingly rare by listing devices that only support ES5 and then noted that some statistics might be outdated
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3795468983) **EliasVal** mentioned that 96.23% of internet users support ES6 and that maintaining ES5 support for the remaining 3% is not worth the cost
 * [today](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3807001264) **guilhermesimoes** criticized the suggestion that PS4 browser usage is rare as ignorant, noted apps on PS4/PS5 have millions of users in Europe and Africa but declined to share exact figures, and deferred the ES5 support cost decision to the TypeScript team

### [Issue microsoft/TypeScript#62240](https://github.com/microsoft/TypeScript/issues/62240) (Open, `Docs`)

**Revert ts5\.9 changes for Uint8Array**

*Revert TypeScript 5.9’s generic Uint8Array type changes because they break compatibility with older TS versions.*

 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3632812751) **darksabrefr** clarified that the underlying buffer type remained fixed at construction even for resizable ArrayBuffers
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3632841425) **guest271314** stated that Bun didn't use tsc to convert TypeScript to JavaScript and demonstrated ArrayBuffer resizing behavior
 * [7 weeks ago](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3632852166) **guest271314** questioned how to reliably check Microsoft TypeScript types for Uint8Array given a broken TypeScript implementation
 * [today](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3807982138) **rifont** suggested using eslint-plugin-enforce-uint8array-arraybuffer to auto-fix Uint8Array type declarations to Uint8Array<ArrayBuffer> and provided a related flat config change example

### [PR microsoft/TypeScript#63031](https://github.com/microsoft/TypeScript/pull/63031) (Closed, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Change default of \`types\` to \`\[\]\` in tsconfig\.json**

*Default tsconfig.json types array is now empty, with '*' wildcard support to maintain legacy inclusion and boost performance.*

 * [6 days ago](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3781900715) **jakebailey** said "Annoyingly the use of ` means it's not easy for a potential twoslash comment to target it, since  is for variants, but, I don't even think twoslash supports types` anyway"
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3785910022) **Copilot** reported fixing five tests by adding explicit types arrays and ensuring only expected errors appear in baselines
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3787228978) **Copilot** addressed code review feedback and fixed 13 tests by adding explicit types arrays and resolving unintended errors
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3806501115) **RyanCavanaugh** said "@copilot address the code review comments"
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3806545006) **Copilot** addressed the code review comments and fixed four issues in commit 5b122ff
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3806627149) **RyanCavanaugh** said "@copilot you need to address @jakebailey 's comments too. All of them."
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3806833390) **Copilot** reported that all issues were resolved in commit 361221e and that the three failing tests were fixed with baselines correctly including type arrays
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3806941798) **RyanCavanaugh** said "@copilot fix the comments"
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3806983979) **Copilot** addressed all comments, fixed wildcard checking logic in compiler functions, and updated tests in commit 7f169c1
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3807247167) **Copilot** extracted the types wildcard check, created a typesIncludesWildcard() helper function, and updated six occurrences across multiple files

### [Issue microsoft/TypeScript#63033](https://github.com/microsoft/TypeScript/issues/63033) (Open, `Bug`, `Domain: LS: Auto-import`, `Corsa`)

**Autocomplete incorrectly suggests transitive files from monorepo package**

*Autocomplete incorrectly suggests unexported internal files from a monorepo package despite its exports configuration.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3786538498) **RyanCavanaugh** said "Sure. FWIW we will not be fixing TS 6 LS bugs, so only testing on 7 is relevant in terms of actionable work items"
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3787420587) **ericnorris** verified that the bug was not present in TS 7, replicated the behaviour with a fourslash test, suggested adding a test to prevent regression, and asked if a separate issue should be filed in the typescript-go repository
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3795824983) **ericnorris** reproduced the issue in TS 7, linked it to the related issue, and asked if a fix for TS 6 would be accepted
 * [today](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3806478101) **RyanCavanaugh** replied that a fix for TS 6 would not be accepted and referenced issue #62963

### [Issue microsoft/TypeScript#63050](https://github.com/microsoft/TypeScript/issues/63050) (Open, `Help Wanted`, `Fix Available`, `Possible Improvement`)

**Double error message when referencing variable of type union of string literals from ambient declaration**

*TypeScript 4.0.5 duplicates the same error message when assigning an ambient string-literal union to a number.*

 * created by **devanshj**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63050#issuecomment-3798773309) **Andarist** pointed out the location where the source gets generalized and noted that the code is not union-aware and stems from a TypeScript PR
 * [today](https://github.com/microsoft/TypeScript/issues/63050#issuecomment-3809323001) **AdyaTech** explained why duplicate error messages appeared by describing TypeScript's internal simplification of union types and contrasting behavior with TS 3.9.7

### [Issue microsoft/TypeScript#63051](https://github.com/microsoft/TypeScript/issues/63051) (Open, `Bug`, `Corsa`, **ahejlsberg**)

**tsgo fails to report TS2769 for mutually\-exclusive object overloads**

*tsgo does not report TS2769 for mutually exclusive object overloads while tsc correctly flags the error.*

 * created by **r253hmdryou**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63051#issuecomment-3796895410) **jcalz** said "Question for TS team... is https://tsgo.sxzz.dev is an acceptable playground for tsgo? "
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63051#issuecomment-3796914886) **r253hmdryou** filed a duplicate issue in microsoft/typescript-go to track tsgo-specific behavior
 * [today](https://github.com/microsoft/TypeScript/issues/63051#issuecomment-3806620084) **RyanCavanaugh** asked if tsgo.sxzz.dev was an acceptable playground for tsgo

### [PR microsoft/TypeScript#63054](https://github.com/microsoft/TypeScript/pull/63054) (Open, `Breaking Change`, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Set default \`types\` array to \`\[\]\`; support \`"\*"\` wildcard**

*Set the default types array to an empty list and implement '*' wildcard support.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808319803) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808504254) **jakebailey** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808504414) **typescript-bot** reported that build jobs started and provided status and results links
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836035) **typescript-bot** reported results of running tsc on the top 800 repos comparing main and a pull request merge and requested review of an interesting change
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836066) **typescript-bot** reported compilation errors in DouyinFE/semi-design from the top 800 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836100) **typescript-bot** reported build failures and type definition errors from top 800 repos suite run for firecrawl
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836121) **typescript-bot** reported additional changes from the top 800 repos suite, detailing TS2584 build failures in humanlayer/12-factor-agents due to missing 'console' name and providing related file links
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836148) **typescript-bot** reported interesting changes from running the top 800 repos suite, including multiple TypeScript errors in microsoft/vscode-extension-samples projects
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836179) **typescript-bot** reported more interesting changes from running the top 800 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836219) **typescript-bot** presented more benchmark results showing TypeScript build errors in the prisma/prisma repository
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836251) **typescript-bot** reported build failures and missing global type errors in puppeteer/puppeteer from the top 800 repos suite run
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836286) **typescript-bot** reported missing type definition errors in raineorshine/npm-check-updates from the top 800 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836321) **typescript-bot** reported errors in reduxjs/redux-toolkit from running the top 800 repos suite
 * [today](https://github.com/microsoft/TypeScript/pull/63054#issuecomment-3808836369) **typescript-bot** reported additional build failures from running the top 800 repos suite against the old tsc, detailing errors in various theatre-js/theatre package configurations

### [PR microsoft/TypeScript#63055](https://github.com/microsoft/TypeScript/pull/63055) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Support FORCE\_COLOR**

*Add support for the FORCE_COLOR environment variable to force colored console output.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63056](https://github.com/microsoft/TypeScript/pull/63056) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Eliminate \`tests/lib/lib\.d\.ts\`, fix up fourslash to use real libs and defaults**

*Overhauled fourslash tests by removing tests/lib/lib.d.ts, using real standard libs with caching, and fixing option handling.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63056#issuecomment-3808793633) **jakebailey** said "I'll note that after this, there's no reason to have @libFiles at all; the only uses are for react.d.ts which can be loaded via a triple-slash reference just fine."

### [Issue microsoft/TypeScript#63057](https://github.com/microsoft/TypeScript/issues/63057) (Closed, `Working as Intended`)

**Module resolution: self\-references file are resolved after 5\.7**

*Updating to TypeScript 5.7+ causes self-referenced imports outside the configured rootDir to fail resolution with “file is not under rootDir” errors.*

 * created by **FoundTheWOUT**

### [Issue microsoft/TypeScript#63058](https://github.com/microsoft/TypeScript/issues/63058) (Closed, `Not a Defect`)

**Partial\<\> with generics is throwing: Type 'xxx' is not assignable to type 'Partial\<T\>'\.**

*TypeScript rejects returning `{ time: 0 }` from a generic getPartial<T extends Timed>() as Partial<T> while the same literal assignment to a Partial<T> variable compiles.*

 * created by **jozefchutka**
 * [later](https://github.com/microsoft/TypeScript/issues/63058#issuecomment-3811349951) **MartinJohns** explained why the error was correct for getPartial and identified an issue in getPartial2 while referencing issue #9825
 * [later](https://github.com/microsoft/TypeScript/issues/63058#issuecomment-3811843827) **jcalz** mentioned a StackOverflow question and issue #51645 related to getPartial(), explained that indexing a generic variable with a specific key widens it to its constraint causing unsoundness, and noted no specific issue exists

