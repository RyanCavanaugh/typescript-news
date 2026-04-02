# Report for 2026-02-27 (Friday, February 27th, 2026)

11 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @james-pre provided reproduction steps and environment details in [microsoft/TypeScript#63197](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3975896004)
    * @na7ure-a asked to test the fix with the exact code from the issue in [microsoft/TypeScript#63199](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977198462)
    * @guillaumebrunerie asked whether libraries depending on global state might break during Vite development and whether this is a Vite bug or a misunderstanding in [microsoft/TypeScript#63203](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3977064991)

## Activity Summary

### [Issue microsoft/TypeScript#44589](https://github.com/microsoft/TypeScript/issues/44589) (Open, `Suggestion`, `Awaiting More Feedback`)

**Ability to extend compilerOptions's paths config**

*Support merging compilerOptions.paths in extended tsconfigs so project-specific mappings don’t overwrite base paths.*

 * [2 years ago](https://github.com/microsoft/TypeScript/issues/44589#issuecomment-1934510915) **dben89x** criticized the previous resolution as arrogant and dismissive and argued for customizable baseUrl path handling in composite configs to avoid repetition
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/44589#issuecomment-1938317780) **dannyfranca** said "Folks, there has been an ongoing proposal since November 2023. Let's contribute to the discussion to help get it going: https://github.com/microsoft/TypeScript/issues/56436"
 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/44589#issuecomment-3192573848) **Loque18** said "+1 here feature needed ! "
 * [today](https://github.com/microsoft/TypeScript/issues/44589#issuecomment-3975020711) **x-keyscore** said "+1 here feature needed !"

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3904267874) **fabon-f** mentioned making a commit with suggested changes and asked whether they should submit an issue before the PR
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3904278277) **jakebailey** said "Feel free to just send it, just mention #60164 to make the bot not yell at you"
 * [3 days ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3952328155) **Renegade334** said "Have opened #63190 for a small interoperability improvement."
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3975924546) **DanielRosenwasser** described merging #63190, questioned including plural forms in DateUnit and TimeUnit due to compatibility concerns, and opened issue #63201
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3975960874) **ptomato** explained the rationale for accepting both singular and plural units in duration-related APIs

### [PR microsoft/TypeScript#63183](https://github.com/microsoft/TypeScript/pull/63183) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**DOM update**

*Optimize the DOM update process to ensure efficient and accurate rendering of dynamic content changes.*

 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63183#issuecomment-3942054688) **typescript-bot** announced that the DT test results were ready and that everything looked the same, providing a link to the log
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63183#issuecomment-3942063967) **typescript-bot** reported test results comparing main and refs/pull/63183/merge, noted a Git clone failure, and indicated everything else looked good
 * [5 days ago](https://github.com/microsoft/TypeScript/pull/63183#issuecomment-3942149269) **typescript-bot** reported that compiling the top 400 repos with tsc on main and the pull request merge yielded no issues
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63190](https://github.com/microsoft/TypeScript/pull/63190) (Closed, `For Uncommitted Bug`)

**discrete pluralizer for lib\.esnext\.temporal unit unions**

*Restrict DateUnit and TimeUnit unions to singular names and use a pluralizer helper for js-temporal compatibility.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3961416016) **jakebailey** said "In a way I wish it were just PluralizeUnits, but I'm not the greatest namer out there."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3961773716) **Renegade334** said "Comme ça ?"
 * (2 days ago) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3975598199) **DanielRosenwasser** asked what the long-term best practice is for handling singular vs plural unit references

### [Issue microsoft/TypeScript#63197](https://github.com/microsoft/TypeScript/issues/63197) (Open)

**Fatal OOM crash on recursive template literal type**

*A recursive template literal type definition causes a fatal out-of-memory crash in TypeScript versions 5.9.3 and 6.0.0-beta.*

 * created by **james-pre**
 * [today](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3975868967) **RyanCavanaugh** requested the actual minimal repro for the issue and noted that long compilation time isn't a security issue
 * [today](https://github.com/microsoft/TypeScript/issues/63197#issuecomment-3975896004) **james-pre** provided environment details, a CI reproduction link, an example type causing the crash, and the tsconfig configuration

### [Issue microsoft/TypeScript#63198](https://github.com/microsoft/TypeScript/issues/63198) (Closed, `Duplicate`)

**"Pure" Replacement for Enums \(Erasable Constants\)**

*Propose a fully erasable TypeScript enum syntax that compiles to a simple object literal without runtime code.*

 * [today](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973129333) **jcalz** expressed confusion about the proposal's specifics and sketched a potential syntax interpretation
 * [today](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973156762) **Boukeng-rochinel** proposed an enum emitting a plain JavaScript object to support type-stripping runtimes instead of IIFEs since const enums are removed entirely at compile time
 * [today](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973393272) **MartinJohns** noted that the proposal would conflict with the Viability Checklist and language Design Goals
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973939522) **RyanCavanaugh** said "This seems to lack an actual proposal. #60790 is the spirit of what's being implied here."

### [Issue microsoft/TypeScript#63199](https://github.com/microsoft/TypeScript/issues/63199) (Open)

**Crash: TypeError: Cannot read properties of undefined \(reading 'aliasSymbol'\) remains when using variadic tuple with \(infer C\)\[\] and constrained infer**

*TypeScript compiler throws a TypeError reading 'aliasSymbol' when inferring variadic tuple types with a constrained infer array.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3974139578) **RyanCavanaugh** said "Crashes in TS7 as well"
 * [later](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977102585) **Andarist** said "Im pretty sure https://github.com/microsoft/TypeScript/pull/63014 fixes this and this issue is a duplicate of https://github.com/microsoft/TypeScript/issues/63005"
 * [later](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977198462) **na7ure-a** thanked the maintainer, tested the fix locally, confirmed the crash in #63005 was resolved but that the issue’s code snippet still crashed, and asked to test with the exact code from the issue

### [PR microsoft/TypeScript#63200](https://github.com/microsoft/TypeScript/pull/63200) (Closed, `For Uncommitted Bug`)

**Adds the symbol name to the error message for TS2742**

*Include the missing symbol name in TS2742 error messages to offer clearer guidance on required imports.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63200#issuecomment-3973509034) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63200#issuecomment-3973509082) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **gabritto** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63200#issuecomment-3974692409) **RyanCavanaugh** said "fyi @weswigham "

### [PR microsoft/TypeScript#63201](https://github.com/microsoft/TypeScript/pull/63201) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Revert "discrete pluralizer for lib\.esnext\.temporal unit unions"**

*Revert the discrete pluralizer addition for lib.esnext.temporal unit unions in TypeScript*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#63202](https://github.com/microsoft/TypeScript/pull/63202) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump minimatch from 3\.1\.2 to 3\.1\.5**

*Upgrade the minimatch dependency from version 3.1.2 to 3.1.5 to include ReDoS warnings, performance improvements, and bug fixes.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63203](https://github.com/microsoft/TypeScript/issues/63203) (Open, `Suggestion`, `Awaiting More Feedback`)

**Narrow a ternary expression to unique symbol type**

*Enable TypeScript to infer a unique symbol type from a ternary expression whose runtime result is constant.*

 * created by **mitar**
 * [later](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3977064991) **guillaumebrunerie** asked whether libraries depending on global state might break during Vite development and whether this is a Vite bug or a misunderstanding
 * [later](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3977083251) **mitar** explained that Vite optimized imports during development by duplicating and bundling them together, causing symbol identity mismatches when the same module was imported via different absolute or relative paths

