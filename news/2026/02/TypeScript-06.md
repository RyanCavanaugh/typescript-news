# Report for 2026-02-06 (Friday, February 6th, 2026)

14 different users commented on 44 different issues.

## Recommended Actions

 * Response Recommended
    * @hybrist asked if the Trusted Types APIs would appear given generator exclusions in [microsoft/TypeScript#30024](https://github.com/microsoft/TypeScript/issues/30024#issuecomment-3863225995)
    * @devanshj suggested closing the issue since it seemed fixed in [microsoft/TypeScript#45217](https://github.com/microsoft/TypeScript/issues/45217#issuecomment-3864546792)
    * @robpalme asked if making existing codebases work with and without the flag first is reasonable as a pre-migration approach in [microsoft/TypeScript#63084](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3864394113)
    * @UnVuTWFu asked if there is a way to enforce using type versus interface based on extraction behavior in [microsoft/TypeScript#63112](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864688383)

## Activity Summary

### [Issue microsoft/TypeScript#30024](https://github.com/microsoft/TypeScript/issues/30024) (Open, `Suggestion`, `Revisit`)

**DOM lib: Add support for Trusted Types API**

*Add TypeScript DOM library definitions for the Trusted Types API, including globals and DOM method signatures for TrustedHTML assignments.*

 * [43 weeks ago](https://github.com/microsoft/TypeScript/issues/30024#issuecomment-2790672424) **freshp86** mentioned that Firefox’s Trusted Types API isn’t enabled by default but can be enabled behind a flag, will likely ship by default soon, and linked to relevant Mozilla and TypeScript issue threads
 * [43 weeks ago](https://github.com/microsoft/TypeScript/issues/30024#issuecomment-2790687664) **koto** said "FWIW it's also enabled in Safari Tech Preview 215 - https://webkit.org/blog/16523/release-notes-for-safari-technology-preview-215/"
 * [43 weeks ago](https://github.com/microsoft/TypeScript/issues/30024#issuecomment-2791679837) **HolgerJeromin** explained that browsers will publish the feature and automated processes will update the MDN compatibility tables, TypeScript lib definitions, and open a bot-generated PR to the TypeScript repo for inclusion in the next TS version
 * [today](https://github.com/microsoft/TypeScript/issues/30024#issuecomment-3863225995) **hybrist** provided research notes on Trusted Types support and noted that the TypeScript DOM lib generator explicitly excludes Trusted* APIs despite spec and MDN support
 * [today](https://github.com/microsoft/TypeScript/issues/30024#issuecomment-3863230203) **jakebailey** explained that the exclusion prevents types from showing up and suggested updating while ensuring compatibility with existing Trusted Types
 * [today](https://github.com/microsoft/TypeScript/issues/30024#issuecomment-3863253808) **hybrist** expressed surprise about inconsistencies in web API patches and mentioned asking on the trusted-types spec repo for clarification

### [Issue microsoft/TypeScript#45217](https://github.com/microsoft/TypeScript/issues/45217) (Closed, `Suggestion`, `Help Wanted`, `Effort: Moderate`, `Domain: Error Messages`, `Experience Enhancement`, `Rescheduled`, **weswigham**)

**Bug: Intellisense shows misleading error when parameter is expected to be a union of an object and a string**

*Intellisense reports "A" as not assignable to "B" instead of flagging the missing property when a parameter union includes both object and string types*

 * (1.9 years ago) **RyanCavanaugh** set milestones to `TypeScript 5.5.0`, `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [later](https://github.com/microsoft/TypeScript/issues/45217#issuecomment-3864546792) **devanshj** said "This seems to be fixed now... not sure by which PR or in which version... but can be closed nonetheless."
 * (later) **devanshj** closed the issue

### [Issue microsoft/TypeScript#54500](https://github.com/microsoft/TypeScript/issues/54500) (Open, `Discussion`, `Fix Available`)

**6\.0 Deprecation List**

*Proposed deprecations of outdated TypeScript 6.0 compiler options, with full removal planned for version 7.0.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3764353180) **danilofuchs** asked whether noUncheckedIndexAccess would be enabled by default in strict mode
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3774124466) **RyanCavanaugh** stated that noUncheckedIndexAccess would not be enabled by default in strict mode
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3843337972) **RyanCavanaugh** said "Edited to add target: es5 and downlevelIteration (entirely) being deprecated."
 * [today](https://github.com/microsoft/TypeScript/issues/54500#issuecomment-3861434363) **RyanCavanaugh** said "Edited to un-deprecate enum merging and cross-namespace value referencing; these are in 7.0 already and removing them wouldn't produce the upside I had hoped for."

### [Issue microsoft/TypeScript#55182](https://github.com/microsoft/TypeScript/issues/55182) (Open, `Suggestion`, `Awaiting More Feedback`)

**Enforce property rules on kebab\-cased JSX attributes**

*Enable TypeScript to enforce property rules on kebab-cased JSX attributes by using template literal types.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-2048229483) **stevematney** noted that Web Components attributes don't require dashes and that TypeScript’s JSX typing makes dashed custom attributes type-unsafe
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-2398912772) **trusktr** suggested adding a strictJsxProps compiler option to prevent silent failures from misspelled JSX props while preserving backwards compatibility
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-3016876530) **JulianCataldo** reported that excess property checks in JSX erroneously bypassed hyphenated custom element attributes, described it as a bug, and proposed a heuristic solution with a TypeScript plugin snippet
 * [today](https://github.com/microsoft/TypeScript/issues/55182#issuecomment-3861385142) **whittede** said "+1 to the original idea in this thread, it would be super useful and would reduce debug time when trying to figure out why attributes are throwing errors or not passing along data."

### [Issue microsoft/TypeScript#56664](https://github.com/microsoft/TypeScript/issues/56664) (Closed, `Bug`, `Help Wanted`, `Fix Available`, `Domain: classes`)

**Can't extend WeakMap in type\-checked JS files**

*Subclassing WeakMap in type-checked JavaScript files fails with TS2510 error due to inconsistent constructor return types.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/issues/56664#issuecomment-1847120913) **ExE-Boss** said "I’ve now opened  (which is the result of rebasing and fixing )."
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: classes`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#56713](https://github.com/microsoft/TypeScript/pull/56713) (Closed, `For Milestone Bug`, `For Backlog Bug`, **sandersn**)

**Un‑consolidate and fix \`WeakMap\` constructor overloads**

*Refactor and correct WeakMap type definitions by separating and fixing its constructor overloads to resolve related issues.*

 * (2.1 years ago) **typescript-bot** added labels `For Backlog Bug`, `For Milestone Bug`, and assigned to **sandersn**
 * [today](https://github.com/microsoft/TypeScript/pull/56713#issuecomment-3862742021) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/56713#issuecomment-3862742262) **typescript-bot** updated CI build job statuses and provided links to results
 * [today](https://github.com/microsoft/TypeScript/pull/56713#issuecomment-3862831054) **typescript-bot** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/56713#issuecomment-3862862210) **typescript-bot** reported test results showing one infrastructure failure and confirming everything else passed
 * [today](https://github.com/microsoft/TypeScript/pull/56713#issuecomment-3862952261) **typescript-bot** provided the requested performance run results comparing baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/56713#issuecomment-3862997980) **typescript-bot** reported that running tsc on the top 400 repos for main versus the pull request merge produced no issues
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#57661](https://github.com/microsoft/TypeScript/pull/57661) (Closed, `For Backlog Bug`, **sandersn**)

**Update Map\.clear and Set\.clear jsdoc in es2015\.collection\.d\.ts**

*Align Map.clear and Set.clear JSDoc in es2015.collection.d.ts with MDN documentation.*

 * **sandersn** assigned to **sandersn**
 * (1.8 years ago) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#57662](https://github.com/microsoft/TypeScript/issues/57662) (Closed, `Suggestion`, `Experience Enhancement`)

**Update Map\.clear and Set\.clear jsdoc in es2015\.collection\.d\.ts**

*Update the JSDoc definitions for Map.clear and Set.clear in the ES2015 collection declarations.*

 * (1.9 years ago) **RyanCavanaugh** added labels `Suggestion`, `Experience Enhancement`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#60164](https://github.com/microsoft/TypeScript/issues/60164) (Closed, `Domain: lib.d.ts`, **RyanCavanaugh**)

**Add Temporal \(Stage 3\) types**

*Add TypeScript definitions for the Stage 3 Temporal API, including Temporal.Now, Instant, ZonedDateTime, PlainDate, and related types.*

 * [40 weeks ago](https://github.com/microsoft/TypeScript/issues/60164#issuecomment-2834408455) **MeesterDev** said "FYI Firefox is shipping Temporal in version 139, planned to be released at the end of May."
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/60164#issuecomment-3418731911) **TomasHubelbauer** noted that Firefox shipped Temporal support months ago and suggested adding types unless cross-browser support is required
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/60164#issuecomment-3753413293) **denexapp** said "Chrome 144 added support for Temporal, released on Jan 14. It will be great to see the types in lib.d.ts"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#60496](https://github.com/microsoft/TypeScript/issues/60496) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`Intl\.Locale\.prototype\.getTimeZones\(\)\` is missing from Intl library definitions**

*TypeScript ESNext Intl library definitions are missing the Intl.Locale.prototype.getTimeZones() method.*

 * (1.2 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#60515](https://github.com/microsoft/TypeScript/issues/60515) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`RegExp\#\[Symbol\.matchAll\]\` should return iterable of \`RegExpExecArray\` instead of \`RegExpMatchArray\`**

*RegExp.prototype[Symbol.matchAll] is mistakenly typed to return an iterable of RegExpMatchArray instead of RegExpExecArray, causing inconsistency with String.prototype.matchAll.*

 * (1.1 years ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: lib.d.ts`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#60516](https://github.com/microsoft/TypeScript/pull/60516) (Closed, `For Backlog Bug`)

**Return iterable of RegExpExecArray from RegExp\#\[Symbol\.matchAll\]**

*Modify RegExp#[Symbol.matchAll] to return an iterable of RegExpExecArray objects as specified.*

 * [31 weeks ago](https://github.com/microsoft/TypeScript/pull/60516#issuecomment-3021327470) **typescript-bot** reported that DT test results were ready and unchanged
 * [31 weeks ago](https://github.com/microsoft/TypeScript/pull/60516#issuecomment-3021331978) **typescript-bot** reported that running the user tests with tsc comparing main and refs/pull/60516/merge looked good
 * [31 weeks ago](https://github.com/microsoft/TypeScript/pull/60516#issuecomment-3021515770) **typescript-bot** reported running the top 400 repos with tsc comparing main and refs/pull/60516/merge and found everything looked good
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#60569](https://github.com/microsoft/TypeScript/pull/60569) (Closed, `For Backlog Bug`)

**Document indexOf return value when not found**

*Document that string and TypedArray indexOf methods return -1 when a search value is not found.*

 * (1.1 years ago) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/60569#issuecomment-2506840894) **Pascal-So** said "@jakebailey ah, thanks for the hint! turns out my problem was that my editor changed some crlf's to lf when I tried to manually copy over the updated files before  :D"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#60570](https://github.com/microsoft/TypeScript/issues/60570) (Closed, `Suggestion`, `Experience Enhancement`)

**Extend documentation of String\.indexOf to mention what happens when substring is not found**

*Document that String.indexOf returns -1 when the substring is not found.*

 * (1.1 years ago) **RyanCavanaugh** added labels `Suggestion`, `Experience Enhancement`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#60608](https://github.com/microsoft/TypeScript/issues/60608) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**\`Intl\.DurationFormat\` missing from library definitions**

*The ESNext library definitions for TypeScript omit Intl.DurationFormat despite its implementation in all browsers.*

 * [43 weeks ago](https://github.com/microsoft/TypeScript/issues/60608#issuecomment-2795786934) **mrleblanc101** said "This API is now baseline, can we add TS Definition for it ?"
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/60608#issuecomment-2817356866) **theuntitled** asked if TypeScript definitions could be added for the now baseline API
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/60608#issuecomment-3425592840) **simonhermann** said "Can somebody explain what's holding this back? It seems quite simple to add."
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#60656](https://github.com/microsoft/TypeScript/pull/60656) (Closed, `For Backlog Bug`)

**Implement Intl Locale Info proposal**

*Implement support for the Intl.LocaleInfo proposal by adding locale metadata APIs to TypeScript.*

 * [1 year ago](https://github.com/microsoft/TypeScript/pull/60656#issuecomment-2596633257) **erlandsona** reported encountering the same issue when updating TypeScript and expressed support for the update
 * (yesterday) **jakebailey** closed the issue
 * (yesterday) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#61078](https://github.com/microsoft/TypeScript/issues/61078) (Closed, `Needs Investigation`, **rbuckton**)

**RegExpIndicesArray type definition incomplete**

*RegExpIndicesArray type definitions in TypeScript should mark group index entries as possibly undefined when capturing groups don’t match*

 * (52 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **rbuckton**
 * [17 weeks ago](https://github.com/microsoft/TypeScript/issues/61078#issuecomment-3380090889) **austinw-fineart** clarified that the spec defines 'indices' as a list of match records or undefined, highlighted that undefined entries still appear in forEach calls, and noted that other spec sequences also use multi-typed elements like PropertyIndexedKeyframes.offset
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#61079](https://github.com/microsoft/TypeScript/pull/61079) (Closed, `For Uncommitted Bug`)

**Fix RegExpIndicesArray by adding undefined to type definition**

*Update RegExpIndicesArray type definition to include undefined for unmatched capture groups.*

 * [52 weeks ago](https://github.com/microsoft/TypeScript/pull/61079#issuecomment-2635027131) **typescript-bot** provided test results showing a new TS2345 error in the azure-sdk codemod
 * [52 weeks ago](https://github.com/microsoft/TypeScript/pull/61079#issuecomment-2635077624) **typescript-bot** reported the results of the requested performance run including metrics such as errors, symbols, types, memory usage, and parse time
 * [52 weeks ago](https://github.com/microsoft/TypeScript/pull/61079#issuecomment-2635165231) **typescript-bot** reported tsc comparisons of main and the PR branch on top 400 repos and highlighted VSCode compile errors
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#61321](https://github.com/microsoft/TypeScript/issues/61321) (Closed, `Bug`, `Domain: lib.d.ts`, `ES Next`)

**Add types for RegExp\.escape**

*Add TypeScript type definitions for the new es2025 RegExp.escape method.*

 * [38 weeks ago](https://github.com/microsoft/TypeScript/issues/61321#issuecomment-2872057073) **jperelli** mentioned that RegExp.escape is now included in Node 24.0.0 and Chrome 136 and provided a TypeScript workaround snippet
 * **RyanCavanaugh** added to milestone `Backlog`
 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/61321#issuecomment-3124430793) **lionel-rowe** noted that RegExp.escape is natively available since May 2025
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#61735](https://github.com/microsoft/TypeScript/issues/61735) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Add ES2025 target and library**

*Add ES2025 as a TypeScript compilation target and library to support upcoming syntax and standard APIs.*

 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/61735#issuecomment-3140226507) **CavaliereDavid** said "Is this a good first issue? I would like to contribute"
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/61735#issuecomment-3794800718) **petamoriken** said "I'll work for this issue"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#61767](https://github.com/microsoft/TypeScript/pull/61767) (Open, `For Uncommitted Bug`, **sandersn**)

**Add IntegerTypedArray type for use with crypto\.getRandomValues**

*Define a new IntegerTypedArray type to correctly constrain crypto.getRandomValues to supported integer array types.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [36 weeks ago](https://github.com/microsoft/TypeScript/pull/61767#issuecomment-2910942114) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [36 weeks ago](https://github.com/microsoft/TypeScript/pull/61767#issuecomment-2910942116) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-bot** assigned to **sandersn**

### [PR microsoft/TypeScript#61817](https://github.com/microsoft/TypeScript/pull/61817) (Open, `For Uncommitted Bug`)

**lib: narrow \`Atomics\.wait\*\` target to SharedArrayBuffer views**

*Restrict Atomics.wait* methods to only accept views over SharedArrayBuffer in their declarations*

 * (yesterday) **jakebailey** reopened the issue
 * [yesterday](https://github.com/microsoft/TypeScript/pull/61817#issuecomment-3858246585) **jakebailey** said "Failed to look at this properly until now. I am shocked this isn't super breaky?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/61817#issuecomment-3858318964) **Renegade334** said "I guess the shared view is often going to appear in a context where its type is inferred, rather than annotated? But yes, somewhat surprising"
 * [today](https://github.com/microsoft/TypeScript/pull/61817#issuecomment-3862456192) **jakebailey** said "I searched github for Atomics.wait, and immediately found places that this will break. Probably going to hold off on this one."

### [Issue microsoft/TypeScript#61960](https://github.com/microsoft/TypeScript/issues/61960) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**NumberFormatPartTypeRegistry doesn't have approximatelySign in it**

*The Intl.NumberFormatPartTypeRegistry type definition omits the 'approximatelySign' part used by formatRangeToParts.*

 * **typescript-bot** added label `Fix Available`
 * (30 weeks ago) **RyanCavanaugh** removed label `Fix Available`, and unassigned **Copilot**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62013](https://github.com/microsoft/TypeScript/pull/62013) (Closed, `For Backlog Bug`, **RyanCavanaugh**, **Copilot**)

**Add approximatelySign to NumberFormatRangePartTypeRegistry for ES2023**

*Add approximatelySign as a range-only part type in the ES2023 NumberFormatRangePartTypeRegistry to support Intl.NumberFormat.formatRangeToParts.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3858253685) **Copilot** created NumberFormatRangePartTypeRegistry, moved approximatelySign there, and updated NumberRangeFormatPart to use NumberFormatRangePartTypes
 * (yesterday) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3862155177) **jakebailey** noted that the proposed change expanded rather than narrowed possible values, showed a TypeScript error, and suggested altering NumberFormatPart or splitting it
 * (today) **typescript-bot** added label `For Uncommitted Bug`, and removed label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62013#issuecomment-3862171124) **Copilot** fixed NumberRangeFormatPart as a standalone interface and confirmed the build and tests passed
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62052](https://github.com/microsoft/TypeScript/pull/62052) (Open, `For Backlog Bug`)

**fix\(Intl\): make Intl\.Collator\.compare a getter that returns a bound function \(\#62048\)**

*Align Intl.Collator.compare in TypeScript’s lib definitions with the ECMAScript specification by making it a getter that returns a bound function*

 * created by **ahsansheikh94**
 * **typescript-bot** added label `For Backlog Bug`
 * [29 weeks ago](https://github.com/microsoft/TypeScript/pull/62052#issuecomment-3065164471) **ahsansheikh94** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/62052#issuecomment-3863246750) **DanielRosenwasser** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/62052#issuecomment-3863246858) **typescript-bot** announced CI jobs started and provided status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/62052#issuecomment-3863288790) **typescript-bot** noted that DT test results were ready and unchanged and provided a log link
 * [today](https://github.com/microsoft/TypeScript/pull/62052#issuecomment-3863312573) **typescript-bot** reported test results and noted an infrastructure failure but otherwise confirmed everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/62052#issuecomment-3863347001) **typescript-bot** provided the performance run results as requested
 * [today](https://github.com/microsoft/TypeScript/pull/62052#issuecomment-3863372164) **typescript-bot** reported that running the top 400 repos with tsc comparing main and the PR merge looked good

### [PR microsoft/TypeScript#62138](https://github.com/microsoft/TypeScript/pull/62138) (Closed, `For Backlog Bug`)

**Add types for \`RegExp\.escape\`**

*Add missing TypeScript type definitions for the proposed RegExp.escape method in library files.*

 * [26 weeks ago](https://github.com/microsoft/TypeScript/pull/62138#issuecomment-3146687980) **i-ayushh18** announced completion of types for `RegExp.escape` in PR #62138 by the AI Assistant
 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/62138#issuecomment-3397206018) **jakebailey** said "This PR has a bunch of conflicts at this point; I'm pretty sure we could get this changed in if fixed"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/62138#issuecomment-3762937312) **fgiering** said "One day.... Maybe... "
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62257](https://github.com/microsoft/TypeScript/issues/62257) (Open, `Bug`, `Domain: Declaration Emit`, `Fix Available`, **DanielRosenwasser**, **weswigham**, **Copilot**)

**Declaration file emits symbol property keys without importing them**

*TypeScript’s declaration file emitter omits imports for unique symbol property keys, causing undefined symbol errors in consumer d.ts files.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/62257#issuecomment-3222856919) **privatenumber** thanked for tagging it as "Fix Available" and asked for a link to the associated PR or commit
 * [23 weeks ago](https://github.com/microsoft/TypeScript/issues/62257#issuecomment-3229329944) **RyanCavanaugh** said "I don't know why the bot did that 🤔"
 * **RyanCavanaugh** added label `Domain: Declaration Emit`
 * (today) **DanielRosenwasser** removed label `Fix Available`, set milestone to `TypeScript 6.0.1`, and removed from milestone `TypeScript 6.0.0`
 * **typescript-bot** added label `Fix Available`
 * (today) **DanielRosenwasser** removed label `Fix Available`, and assigned to **Copilot**, **DanielRosenwasser**
 * (today) **typescript-bot** added labels `Fix Available`, `Fix Available`

### [PR microsoft/TypeScript#62556](https://github.com/microsoft/TypeScript/pull/62556) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] tsgo compat changes**

*Introduce a boolean toggle to enable tsgo compatibility updates combining changes from PRs 61399 and 61420.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842870941) **typescript-bot** reported DT test results indicating errors in json-logic-js, trellopowerup, and codemirror packages
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3842999875) **typescript-bot** provided the perf run results
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3843105177) **typescript-bot** reported tsc build comparison results for the top 400 repos between `main` and the PR merge, noting interesting changes and build failures in several projects
 * [today](https://github.com/microsoft/TypeScript/pull/62556#issuecomment-3863290735) **jakebailey** said "Note that in the latest nightly, you can now do --stableTypeOrdering to emulate this. This PR just shows what happens when it's flipped on."

### [PR microsoft/TypeScript#62612](https://github.com/microsoft/TypeScript/pull/62612) (Closed, `For Uncommitted Bug`)

**Add proposal\-upsert methods to lib\.esnext\.collection**

*Add stage 3 proposal-upsert methods to lib.esnext.collection to support new Map and Set upsert functionality now shipping in major browsers.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/pull/62612#issuecomment-3411791132) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [11 weeks ago](https://github.com/microsoft/TypeScript/pull/62612#issuecomment-3554828959) **jakebailey** said "Do you know how far this is from being out of staging in V8/Chromium? The types themselves seem correct, of course, but I was trying to avoid being premature."
 * [11 weeks ago](https://github.com/microsoft/TypeScript/pull/62612#issuecomment-3554866000) **Renegade334** stated that it was roadmapped for M145
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3629743678) **Renegade334** noted that definitions were de novo with no licensing issues and observed that temporal-polyfill and @js-temporal/polyfill were incompatible with lib.d.ts patterns, offering to run interoperability tests
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3850515921) **jakebailey** mentioned reviewing the PR and noted that MDN hasn't updated to reflect the removal of custom calendar support per the latest spec changes
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3857186615) **jakebailey** said "One thing this PR is missing are updates to getScriptTargetFeatures, though not strictly required to compile."
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3863219313) **DanielRosenwasser** requested docs before the release candidate, suggested a better error message for wrong Temporal lib references, and noted coercion tests were fine but shouldn’t be pushed further
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3863285873) **Renegade334** reported that referencing Temporal without the namespace did not produce the expected error message
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3863766950) **justingrant** thanked maintainers for landing Temporal types, noted original type contributions, apologized for late review, reported a small type mistake, asked why @bakkot’s suggestion for property bag constraints didn’t work, and asked for recommendations on polyfill compatibility
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3863884548) **DanielRosenwasser** thanked justingrant and others for reviewing Temporal, discussed whether polyfill declaration files should be integrated into lib.d.ts, reflected on differing declaration patterns and his oversight in not seeking feedback, and mentioned plans to ship the 6.0 beta soon and address differences thereafter
 * [later](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3864504776) **Renegade334** asked why bakkot's suggestion didn't work and explained that using type aliases in lib.d.ts hinders forward extensibility, then discussed potential workarounds

### [PR microsoft/TypeScript#62726](https://github.com/microsoft/TypeScript/pull/62726) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Always set up host in node builder**

*Configure the node builder to always initialize the host environment during setup.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3855925877) **typescript-bot** reported test results comparing main and PR merge, noting a git clone failure but otherwise success
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3856039129) **typescript-bot** posted the requested perf run results for tsc
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62726#issuecomment-3856141405) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the pull request resulted in no issues
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62730](https://github.com/microsoft/TypeScript/pull/62730) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**DOM update**

*Update the DOM to incorporate numerous recent changes.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843277985) **jakebailey** said "The GPU types get bigger, and so more conflicts..."
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843279804) **typescript-bot** posted the requested perf run results comparing baseline and PR
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3843366710) **typescript-bot** reported that the top 400 repos’ tsc build results comparing main and the PR looked good
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3863121077) **jakebailey** said "Going to take these as-is for now. We update DOM before the RC too, so if something's still missing it's fixable."
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62970](https://github.com/microsoft/TypeScript/issues/62970) (Closed, `Bug`, `Domain: lib.d.ts`)

**\`Intl\.CollatorOptions\['collation'\]\` is missing value \`'default'\`**

*TypeScript's Intl.CollatorOptions type omits the 'default' collation value.*

 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62970#issuecomment-3746083320) **RyanCavanaugh** clarified that passing default to Intl.Collator was sensible since resolvedOptions showed default
 * **RyanCavanaugh** added to milestone `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#62971](https://github.com/microsoft/TypeScript/pull/62971) (Closed, `For Backlog Bug`)

**add \`collation\` to \`Intl\.CollatorOptions\`**

*Add the collation property to Intl.CollatorOptions to enable specifying string comparison rules for different locales*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62971#issuecomment-3849048791) **jakebailey** said "@typescript-bot run dt"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62971#issuecomment-3849049482) **typescript-bot** reported CI job start and linked build results
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62971#issuecomment-3849162440) **typescript-bot** informed that the DT test results were ready and unchanged and linked the logs
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63046](https://github.com/microsoft/TypeScript/pull/63046) (Closed, `For Backlog Bug`)

**Introduce ES2025 target & Add missing ScriptTargetFeatures**

*Introduce ES2025 compilation target and add missing type definitions for RegExp.escape and Intl.DurationFormat in TypeScript.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3858449556) **petamoriken** explained writing the type inline within DurationFormatOptions might make the changes harder to review and apologized for the inconvenience
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3858489090) **petamoriken** offered to have the intl changes pushed directly to the PR if the release timing requires it
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3858774558) **petamoriken** described that in es2023.intl.d.ts and es2022.intl.d.ts types are defined inline within options interfaces, while in es2020.intl.d.ts types like RelativeTimeFormatUnit and RelativeTimeFormatUnitSingular are explicitly defined
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3861724357) **jakebailey** suggested retaining explicit duration format type definitions as a middle-ground approach
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3861878686) **jakebailey** said "Ah, I just pushed to this, but didn't notice you were around to react. Well, I think it's in a good state now?"
 * [today](https://github.com/microsoft/TypeScript/pull/63046#issuecomment-3861889120) **jakebailey** noted that GitHub was not showing a specific commit in the PR and that gh pr checkout did not pull it
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63061](https://github.com/microsoft/TypeScript/issues/63061) (Closed, `Not a Defect`)

**\`export type\` vs \`export { type }\` with augmentations**

*export { type } re-exports do not allow module augmentations to access types, unlike export type*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3842786736) **RyanCavanaugh** explained reasons for allowing a local type to be exported by name without reuse and that module rules include only the lexical scope of explicitly exported names, consistent with file-level behavior
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3857354651) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (yesterday) **typescript-bot** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63061#issuecomment-3864341176) **mkantor** asked for clarification on 'file level' with an example and provided a TypeScript reproduction illustrating module declaration scoping issues

### [PR microsoft/TypeScript#63084](https://github.com/microsoft/TypeScript/pull/63084) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add \-\-stableTypeOrdering for TS7 ordering compat**

*Add a hidden --stableTypeOrdering flag that enables TS7’s deterministic type, symbol, and node ordering algorithm for tsgo-port compatibility.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3849906953) **jakebailey** said "@typescript-bot pack this"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3849907364) **typescript-bot** posted a build status update with links for the pack this command
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3849927246) **typescript-bot** provided an installable tgz link and instructions for testing by referencing it in package.json and running npm install
 * (today) **jakebailey** closed the issue
 * [later](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3864394113) **robpalme** said "Is it reasonable pre-migration approach to try to first make existing codebases work with and without this flag?"

### [Issue microsoft/TypeScript#63109](https://github.com/microsoft/TypeScript/issues/63109) (Open)

**Clarify tsconfig extends resolution**

*Clarify and update tsconfig.json 'extends' resolution documentation to explain Node.js-style specifier handling.*

 * created by **valler**

### [PR microsoft/TypeScript#63110](https://github.com/microsoft/TypeScript/pull/63110) (Open, `For Milestone Bug`, **DanielRosenwasser**, **Copilot**)

**Fix declaration emit for symbol property keys from external modules**

*Declaration emit emits symbol property keys from external modules without imports because accessibility checks were missing*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **typescript-bot** added labels `For Milestone Bug`, `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63110#issuecomment-3862839314) **DanielRosenwasser** said "@copilot+claude-opus-4.5 keep at it"

### [Issue microsoft/TypeScript#63111](https://github.com/microsoft/TypeScript/issues/63111) (Closed)

**Release announcement post for 4\.5 is broken**

*The TypeScript 4.5 announcement post’s layout on devblogs.microsoft.com is broken due to a missing closing div tag causing formatting errors.*

 * created by **mkantor**
 * [later](https://github.com/microsoft/TypeScript/issues/63111#issuecomment-3864434748) **mkantor** noted that the release-notes page didn’t appear broken and asked if the issue should be moved to the microsoft/TypeScript-Website repository

### [Issue microsoft/TypeScript#63112](https://github.com/microsoft/TypeScript/issues/63112) (Open)

**Infer works differently for interface and type alias**

*TypeScript infer in conditional types correctly matches index signatures on type aliases but fails for interfaces.*

 * created by **UnVuTWFu**
 * [later](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864623797) **mkantor** explained that the issue was a direct consequence of implicit index signatures not existing on interfaces (per issue #15300) and suggested adding an explicit index signature to fix the code
 * [later](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864688383) **UnVuTWFu** described wanting to pass a generic type and extract specific types via conditional types, noted interface returned never while type alias worked

