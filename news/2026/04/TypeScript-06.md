# Report for 2026-04-06 (Monday, April 6th, 2026)

19 different users commented on 48 different issues.

## Recommended Actions

 * Moderation
    * @FagnerMartinsBrack posted rude content in [microsoft/TypeScript#10011](https://github.com/microsoft/TypeScript/issues/10011#issuecomment-4195652127)
    * @coderlife-book posted rude content in [microsoft/TypeScript#63347](https://github.com/microsoft/TypeScript/issues/63347#issuecomment-4197232279)
 * Response Recommended
    * @vadimmos asked if there's any progress on the issue and if developers are still forced to rely on documentation without autocompletion and type checking in [microsoft/TypeScript#11781](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-4199635479)
    * @shmuel-taub asked why all Iterables are being limited to return readonly and suggested handling type and immutability issues with separate overrides in [microsoft/TypeScript#48228](https://github.com/microsoft/TypeScript/pull/48228#issuecomment-4195435172)
    * @SOMONSOUM provided code suggestion for tsconfig configuration in [microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4197912770)
    * @denis-migdal provided a minimal reproducible example and real code signature in [microsoft/TypeScript#63363](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4193519030)
    * @denis-migdal provided repro examples as information in [microsoft/TypeScript#63363](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4200106490)
    * @NullVoxPopuli reported not having the issue with neovim built-in LSP and tsserver in [microsoft/TypeScript#63367](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4195761326)
    * @guillaumebrunerie asked why a NuGet package was wanted for the old version v5.5.4 in [microsoft/TypeScript#63371](https://github.com/microsoft/TypeScript/issues/63371#issuecomment-4200091566)

## Activity Summary

### [Issue microsoft/TypeScript#10011](https://github.com/microsoft/TypeScript/issues/10011) (Open, `By Design`, `Suggestion`, `Needs Proposal`, `Help Wanted`, `Committed`, `Canonical`, `Effort: Difficult`, `Working as Intended`, `Awaiting More Feedback`)

**Love for TypeScript**

*The author expresses gratitude for Anders Hejlsberg’s contributions to TypeScript and VS Code and suggests adding a LOVE tag on GitHub.*

 * [7.3 years ago](https://github.com/microsoft/TypeScript/issues/10011#issuecomment-447594045) **typescript-bot** said "This issue has been marked 'Working as Intended' and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (7.3 years ago) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/10011#issuecomment-4194592524) **RyanCavanaugh** said "Bad bots, what are we doing here"
 * (today) **RyanCavanaugh** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/issues/10011#issuecomment-4195652127) **FagnerMartinsBrack** said "@RyanCavanaugh BOTs can't love, so they don't see a reason for one's existence =("

### [Issue microsoft/TypeScript#11781](https://github.com/microsoft/TypeScript/issues/11781) (Open, `Suggestion`, `Help Wanted`, `Domain: lib.d.ts`)

**Service Worker typings**

*Include built-in Service Worker type definitions in TypeScript’s default library, matching existing community @types packages.*

 * [34 weeks ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-3173204669) **strogonoff** asked clarifying questions about tsconfig.json usage and warned about unintended inheritance and worker type application
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-3243343623) **eighty4** solved the issue with project references for scoping libraries and noted their limitation in bundler-built webapps requiring noEmit: false
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-3377075608) **FusillyCode** explained that previous solutions broke Firefox compatibility and provided a workaround using skipLibCheck and custom ServiceWorkerGlobalScope casting
 * [later](https://github.com/microsoft/TypeScript/issues/11781#issuecomment-4199635479) **vadimmos** said "Is there any progress on this issue? Are developers still doomed to write ServiceWorker code with one eye on the documentation, without the ability to rely on autocompletion and type checking tools?"

### [Issue microsoft/TypeScript#20183](https://github.com/microsoft/TypeScript/issues/20183) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Domain: LS: Completion Lists`, `VS Code Tracked`)

**Sort jsdoc parameter suggestions by argument position **

*JSDoc parameter suggestions triggered after @param should be sorted by their position in the function signature.*

 * [2.3 years ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-1848271459) **ckcherry23** said "Hi @mjbvz, I'm a first-time contributor. Is this issue still relevant to take up?"
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-2600577963) **RafaelMeir4** asked if the issue was still a priority and requested guidance to the relevant implementation files
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/20183#issuecomment-4069910721) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#22467](https://github.com/microsoft/TypeScript/issues/22467) (Open, `Bug`, `Help Wanted`, `Domain: API`, `Good First Issue`)

**getDefinitionAtPosition doesn't distinguish different kinds in a merged declaration**

*getDefinitionAtPosition incorrectly reports all merged declarations as class rather than distinguishing module, class, and interface*

 * **RyanCavanaugh** added label `Domain: API`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-4069921460) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/22467#issuecomment-4076261227) **paigefletcher1282-code** confirmed that the issue was fixed
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#23185](https://github.com/microsoft/TypeScript/issues/23185) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Domain: Error Messages`)

**Cannot Load Custom Definition File in Repository**

*TypeScript cannot locate and use a custom .d.ts file for the ‘messageformat’ module despite various tsconfig settings.*

 * (7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * **sandersn** added label `GraceHopperOSD`
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#27910](https://github.com/microsoft/TypeScript/issues/27910) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Domain: Error Messages`, `Experience Enhancement`)

**TS2367: This condition will always return 'false' since the types 'Constructor\<T\>' and 'typeof Child' have no overlap\.**

*Comparing a generic constructor type Constructor<T> to the specific Child class always fails due to incompatible types, causing TS2367.*

 * [4.9 years ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-836730432) **vsDizzy** provided better illustrations with two images
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-4069922982) **ManishPrakkash** said "Checking in to see if this is still open for a PR? I’d like to help out with the requested changes"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/27910#issuecomment-4076259171) **paigefletcher1282-code** confirmed it worked for them now
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#30408](https://github.com/microsoft/TypeScript/issues/30408) (Open, `Suggestion`, `Help Wanted`, `Good First Issue`, `Effort: Moderate`, `Domain: Error Messages`, `Experience Enhancement`)

**Confusing error message for labels used before definition**

*A continue to a label defined after a for loop incorrectly triggers a confusing TS1007 error.*

 * **sandersn** added label `GraceHopperOSD`
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-3375208805) **tysoncung** suggested checking the error logs and asked for environment details to help investigate the issue
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/30408#issuecomment-3685142380) **mhughes2012** said "I can take this on, I have a fix for it. Please assign me."
 * (today) **RyanCavanaugh** removed labels `Domain: Related Error Spans`, `PursuitFellowship`

### [Issue microsoft/TypeScript#31885](https://github.com/microsoft/TypeScript/issues/31885) (Open, `Help Wanted`, `Docs`)

**wiki doc: @template reference re: jsdoc \(and old usejsdoc\.org reference\)**

*Clarify that @template is a custom TypeScript JSDoc tag and update the wiki's outdated usejsdoc.org reference to jsdoc.app.*

 * (6.7 years ago) **RyanCavanaugh** removed labels `Bug`, `Bug`
 * **sandersn** added label `GraceHopperOSD`
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#32253](https://github.com/microsoft/TypeScript/issues/32253) (Open, `Docs`)

**Object\.freeze after object creation doesn't error**

*TypeScript fails to report errors when assigning to properties of objects frozen at runtime using Object.freeze.*

 * **sandersn** added label `GraceHopperOSD`
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/32253#issuecomment-980067603) **jimmywarting** expressed a desire to refactor the JSXIdentifier class to freeze instances with Object.freeze
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/32253#issuecomment-2643171986) **IanBellomy** asked if calling Object.freeze should produce an error instead of changing the parameter type
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#32283](https://github.com/microsoft/TypeScript/issues/32283) (Open, `Needs Proposal`, `Help Wanted`, `Effort: Moderate`, `Domain: LS: Quick Info`, `Experience Enhancement`)

**Show type info of yield**

*Show the yield keyword’s argument and return types when the cursor is placed over it.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * **sandersn** added label `GraceHopperOSD`
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/32283#issuecomment-2014074216) **DanielRosenwasser** said "Similar to #11261 which is about quick info on return."
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#35455](https://github.com/microsoft/TypeScript/issues/35455) (Open, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: JSDoc`, **sandersn**)

**JSDocTag width is inconsistent**

*TypeScript’s getWidth returns only the tag name length for JSDocTag but the full comment length for JSDocParameterTag, causing inconsistent widths.*

 * (6.1 years ago) **sandersn** added label `GraceHopperOSD`, and assigned to **sandersn**
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#36185](https://github.com/microsoft/TypeScript/issues/36185) (Open, `Suggestion`, `Help Wanted`, `Community Tooling`, `Experience Enhancement`)

**Add diff chunk header lines to Git**

*Add regex rules to Git userdiff to recognize TypeScript function and class declarations in diff headers.*

 * [5.5 years ago](https://github.com/microsoft/TypeScript/issues/36185#issuecomment-702450062) **michaelblyons** said "You can clone https://github.com/git/git and submit a patch to their mailing list. You can even do use GitGitGadget to convert a PR to the right format."
 * [4.2 years ago](https://github.com/microsoft/TypeScript/issues/36185#issuecomment-1013748014) **michaelblyons** said "@yehee's PR seems to have stalled (https://github.com/git/git/pull/859). Does anyone else want to take it up?"
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/36185#issuecomment-2227479870) **matthewhughes934** mentioned that yehee's PR had stalled and opened a new PR, asking for feedback
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#37346](https://github.com/microsoft/TypeScript/issues/37346) (Open, `Bug`, `Help Wanted`, `Domain: JSDoc`, `checkJs`, **orta**)

**@description JSDoc tag interferes with callback parameter documentation**

*Including a JSDoc @description tag in a @callback comment erroneously removes its parameter typing, causing a call signature error.*

 * (5.5 years ago) **sandersn** added label `GraceHopperOSD`, and removed label `good first issue`
 * **RyanCavanaugh** added label `Domain: JSDoc`
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#37760](https://github.com/microsoft/TypeScript/issues/37760) (Open, `Bug`, `Help Wanted`, `Domain: Parser`)

**Parsing issue for call expression with type arguments following left\-shift**

*Using the left-shift operator before a generic call expression in TypeScript causes parsing ambiguity that breaks syntax highlighting.*

 * **RyanCavanaugh** added label `help wanted`
 * **sandersn** added label `GraceHopperOSD`
 * **RyanCavanaugh** added label `Domain: Parser`
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#37823](https://github.com/microsoft/TypeScript/issues/37823) (Open, `Bug`, `Help Wanted`, `Domain: classes`)

**Cannot assign to \.\.\. because it is a read\-only property when using type guard in ctor**

*TypeScript wrongly reports a readonly property assignment error inside constructors when 'this' is narrowed by a type guard.*

 * **sandersn** added label `GraceHopperOSD`
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/37823#issuecomment-2186580346) **mwaibel-go** demonstrated that using a type assertion on the object whose property is to be assigned triggers the same error in TS 5.5.2
 * **RyanCavanaugh** added label `Domain: classes`
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#39003](https://github.com/microsoft/TypeScript/issues/39003) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**HTMLFormControlsCollection namedItem should return only form input elements**

*TypeScript’s HTMLFormControlsCollection.namedItem method is incorrectly typed to return generic Element instead of specific form control types.*

 * [5.7 years ago](https://github.com/microsoft/TypeScript/issues/39003#issuecomment-650142886) **ilogico** suggested declaring types in an augmentable interface like HTMLElementTagNameMap due to potential custom form controls
 * **sandersn** added label `GraceHopperOSD`
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/39003#issuecomment-974480436) **toofarm** said "Bumping this issue. The HTMLFormElement definition is causing erroneous errors in my code when I try to access a form element's value prop"
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#39010](https://github.com/microsoft/TypeScript/issues/39010) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**MediaTrackConstraintsSet misses torch**

*TypeScript's MediaTrackConstraintsSet definition omits the torch constraint, preventing its use.*

 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [5.8 years ago](https://github.com/microsoft/TypeScript/issues/39010#issuecomment-644853039) **RyanCavanaugh** noted that there were many ways to silence errors without switching to JS
 * **sandersn** added label `GraceHopperOSD`
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#39864](https://github.com/microsoft/TypeScript/issues/39864) (Open, `Bug`, `Help Wanted`, `Domain: classes`)

**Support either type asserting \`self\` in classes, or properly ignoring workaround**

*Support type-asserting 'self' in class inheritance or properly ignore related workarounds to preserve correct super method typing*

 * **sandersn** added label `GraceHopperOSD`
 * [5 years ago](https://github.com/microsoft/TypeScript/issues/39864#issuecomment-792735815) **Zzzen** said "Would you elaborate on what skip-parenthesized-assertions is? Currently, this error is thrown by parser, should we move the logic to checker where the full ast is known? @RyanCavanaugh "
 * **RyanCavanaugh** added label `Domain: classes`
 * **RyanCavanaugh** removed label `PursuitFellowship`

### [Issue microsoft/TypeScript#42853](https://github.com/microsoft/TypeScript/issues/42853) (Open, `Needs Investigation`, **weswigham**)

**Preserve interfaces in generated declaration files for augmentation**

*Provide a compiler option to preserve original interfaces in generated declaration files to support augmentation.*

 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-968275925) **theKashey** said "Interesting solution, not sure I can afford it in monorepo. Currently the best workaround seems to be keeping some d.ts manually written 😔"
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-1328235219) **jaulz** said "Unfortunately, this is still an issue. It would be really nice instead of running a script after the build. "
 * [today](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-4193049923) **FranjoMindek** requested an option to enable automatic type merging for user and package types
 * [today](https://github.com/microsoft/TypeScript/issues/42853#issuecomment-4194057887) **zardoy** said "I think Most probably it will be fixed in go compiler rewrite"

### [PR microsoft/TypeScript#48228](https://github.com/microsoft/TypeScript/pull/48228) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**isArray\(\) preserve mutability and element type**

*Refine Array.isArray's type guard to preserve readonly/mutable status and element types for arrays, ArrayLike, and Iterable while maintaining any/unknown compatibility.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/48228#issuecomment-2249432973) **typescript-bot** provided the requested performance run results
 * [1.6 years ago](https://github.com/microsoft/TypeScript/pull/48228#issuecomment-2249520768) **typescript-bot** reported the tsc regression results for top 400 repos, highlighting build failures in apollographql/apollo-client and discordjs/discord.js
 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`
 * [today](https://github.com/microsoft/TypeScript/pull/48228#issuecomment-4195435172) **shmuel-taub** questioned why all Iterables were limited to return readonly and proposed separate overrides for isArray to address type and immutability issues

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-3398783245) **andrewbranch** explained that relative paths in tsconfig ‘paths’ are always resolved to the defining file, described past unintended behavior when a base config defined ‘paths’ and extending configs defined ‘baseUrl’, and noted that the ts5to6 migration tool can handle this automatically
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4187144985) **ArfanFahad** reported having a persistent warning and a watcher compilation failure after applying IntelliSense fix
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4187271405) **jakebailey** said "There's no problem. This is very intentional. Remove that option."
 * [later](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4197912770) **SOMONSOUM** suggested removing the baseUrl setting and adding a paths configuration

### [PR microsoft/TypeScript#63327](https://github.com/microsoft/TypeScript/pull/63327) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63310 \(Mark class property initializers as\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63310 marking class property initializers into the release-6.0 branch for review and merge*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63342](https://github.com/microsoft/TypeScript/issues/63342) (Open)

**type checking complexity with multiple template literals in unions**

*TypeScript’s type checking time scales exponentially with unions of template literal types in dynamic route definitions.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4180241279) **jakebailey** said "I'm pretty sure I tried this (no pun intended) in https://github.com/microsoft/TypeScript/pull/59759"
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4180398717) **eps1lon** asked what the conclusion was after discussions fizzled over memory concerns and offered to investigate the benchmarks further
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4180447400) **jakebailey** said "The conclusion was "we didn't come to a conclusion before this codebase became closed to new PRs": https://github.com/microsoft/TypeScript#contribute"
 * [later](https://github.com/microsoft/TypeScript/issues/63342#issuecomment-4197960180) **eps1lon** said "There's a Go port: https://github.com/microsoft/typescript-go/pull/3331"

### [PR microsoft/TypeScript#63344](https://github.com/microsoft/TypeScript/pull/63344) (Closed)

**Document charCodeAt edge case behavior in first line**

*Update charCodeAt JSDoc to mention NaN return edge case in the main description line.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4181033803) **RyanCavanaugh** said "I don't know what's going on; never heard of this happening before. Even after running git clean -xdf, npm ci + npm test is sufficient on my machine."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4186769595) **bwalter007** identified that a colon in the directory path caused the issue, renamed the directory, updated the baseline, and pushed the changes
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4186769782) **bwalter007** said "@microsoft-github-policy-service agree"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63346](https://github.com/microsoft/TypeScript/issues/63346) (Open)

**Experimental \(deprecated\) decorators are included by default**

*The ESNext library includes legacy experimental decorator types by default, causing conflicts with new decorator definitions.*

 * created by **OldStarchy**
 * [today](https://github.com/microsoft/TypeScript/issues/63346#issuecomment-4193336835) **RyanCavanaugh** thanked the user and provided a list of similar issues

### [Issue microsoft/TypeScript#63347](https://github.com/microsoft/TypeScript/issues/63347) (Closed, `Not a Defect`)

**Minor performance issue when using HTMLElementTagNameMap**

*TypeScript 6.0’s overload resolution for HTMLElementTagNameMap has regressed, causing slower type-checking and minor performance issues on Linux*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63347#issuecomment-4184232102) **RyanCavanaugh** identified the originating commit as a DOM update and explained that the performance cost increase was due to larger map entries and properties per element rather than a checker defect
 * **RyanCavanaugh** added label `Not a Defect`
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63347#issuecomment-4186205019) **jasonlyu123** analyzed commit-induced performance regression, noted difference in isInstantiation comparison and symbol id assignment, identified stricter baseline timing in TS6, and concluded it was a preexisting performance issue triggered by DOM updates
 * [today](https://github.com/microsoft/TypeScript/issues/63347#issuecomment-4195945122) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63347#issuecomment-4197232279) **coderlife-book** said "close damned bot"

### [Issue microsoft/TypeScript#63349](https://github.com/microsoft/TypeScript/issues/63349) (Closed)

**Merging type only \`namespace\` and \`const\` in module declaration**

*Request for a TypeScript module declaration that merges a default-exported value and augmentable type-only namespace without breaking LSP*

 * created by **Aylur**
 * [today](https://github.com/microsoft/TypeScript/issues/63349#issuecomment-4193336881) **RyanCavanaugh** thanked the user and provided an automated list of similar issues
 * [today](https://github.com/microsoft/TypeScript/issues/63349#issuecomment-4195181354) **Aylur** said "https://github.com/microsoft/typescript/issues/11034"
 * (today) **Aylur** closed the issue

### [Issue microsoft/TypeScript#63353](https://github.com/microsoft/TypeScript/issues/63353) (Open)

**Declaration emit references imported type without importing it when inheriting static methods via CommonJS \`require\`**

*Declaration emitter omits import for a referenced typedef and emits an unused require import when inheriting static methods via CommonJS.*

 * created by **avivkeller**
 * [today](https://github.com/microsoft/TypeScript/issues/63353#issuecomment-4193336982) **RyanCavanaugh** provided automated analysis with links to similar issues
 * [today](https://github.com/microsoft/TypeScript/issues/63353#issuecomment-4193365190) **avivkeller** clarified that the referenced issues correspond to regressions in different TypeScript versions and identified one as unrelated

### [Issue microsoft/TypeScript#63358](https://github.com/microsoft/TypeScript/issues/63358) (Open, `Bug`)

**TSX error location error with location and JSX comment**

*A preceding JSX comment causes TypeScript to report a non-ReactNode type error on the comment instead of the expression.*

 * created by **RobertSandiford**
 * [today](https://github.com/microsoft/TypeScript/issues/63358#issuecomment-4193337056) **RyanCavanaugh** said "🤖 This is an automated response. I looked for things that might help (duplicates, FAQ entries, etc) but didn't find anything. A human will take a look!"
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63358#issuecomment-4194330994) **RyanCavanaugh** said "Repro confirmed in TS7"

### [Issue microsoft/TypeScript#63361](https://github.com/microsoft/TypeScript/issues/63361) (Closed, `Question`)

**\`Flatten\<O\>\` does not merge union object fields — distributes instead**

*Flatten<O> merges root-level object unions correctly but fails to recursively flatten nested object union fields, leaving them distributed.*

 * created by **kevalcodezee**
 * [today](https://github.com/microsoft/TypeScript/issues/63361#issuecomment-4192309871) **jcalz** explained why the type failed due to union distribution, provided an alternative implementation, and directed to Stack Overflow or Discord for further discussion
 * **RyanCavanaugh** added label `Question`
 * (later) **kevalcodezee** closed the issue

### [Issue microsoft/TypeScript#63363](https://github.com/microsoft/TypeScript/issues/63363) (Open)

**Inside a generic function with a remapped type as parameter, elements are wrongfully inferred as {}\.**

*Indexed access of remapped generic type properties in a generic function leads to them being inferred as {} instead of their defined type.*

 * created by **denis-migdal**
 * [today](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4192072558) **denis-migdal** noted that the behavior was introduced after version 5.3.3 and previously produced a TypeScript index signature error
 * [today](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4193188506) **RyanCavanaugh** said "Why are you writing the function signature this way in the first place?"
 * [today](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4193519030) **denis-migdal** provided a minimal reproducible example and shared the real code signature with a playground link
 * [later](https://github.com/microsoft/TypeScript/issues/63363#issuecomment-4200106490) **denis-migdal** provided TypeScript examples comparing different mapped type key remappings and noted which caused fewer inference issues

### [PR microsoft/TypeScript#63365](https://github.com/microsoft/TypeScript/pull/63365) (Closed)

**fix: skip block\-scoped variable check for label identifiers**

*The compiler now skips block-scoped variable usage checks for labels to prevent false used-before-declaration errors.*

 * created by **Ankitajainkuniya**
 * [today](https://github.com/microsoft/TypeScript/pull/63365#issuecomment-4194514514) **RyanCavanaugh** said "@Ankitajainkuniya what agent did you use to write this?"
 * [today](https://github.com/microsoft/TypeScript/pull/63365#issuecomment-4194663106) **Ankitajainkuniya** explained using OpenAI as a coding assistant for parts of the implementation with their own review and modifications, affirmed that architecture decisions and product logic were theirs, and linked to their open-source projects repository
 * [today](https://github.com/microsoft/TypeScript/pull/63365#issuecomment-4194672014) **RyanCavanaugh** said "Please have your workflow ingest https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md before proceeding."
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63366](https://github.com/microsoft/TypeScript/pull/63366) (Closed)

**Require AI disclosure in PR descriptions**

*Implement a requirement for contributors to disclose AI-generated content in pull request descriptions.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63367](https://github.com/microsoft/TypeScript/issues/63367) (Open)

**Stuck in initialization loop on v1\.114 w/ TS 5, also on v1\.113 w/ TS 6**

*VSCode repeatedly loops initializing TypeScript configurations for each project in a large pnpm monorepo on v1.114 with TS 5 or v1.113 with TS 6*

 * created by **NullVoxPopuli**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63367#issuecomment-4195761326) **NullVoxPopuli** said "if it helps, I do not have this issue with neovim, the built in LSP, and tsserver"

### [PR microsoft/TypeScript#63368](https://github.com/microsoft/TypeScript/pull/63368) (Open)

**Harden ATA package name filtering**

*Restrict ATA package names to alphanumeric characters, underscores, periods, and hyphens to prevent shell-related validation issues.*

 * created by **jakebailey**

### [Issue microsoft/TypeScript#63369](https://github.com/microsoft/TypeScript/issues/63369) (Closed)

**InstanceType\<T\> \| undefined collapses to InstanceType\<T\> in return type of generic method with polymorphic this**

*TypeScript’s generic static method with polymorphic this collapses InstanceType<TThis> | undefined to just InstanceType<TThis>.*

 * created by **codextremist**
 * [today](https://github.com/microsoft/TypeScript/issues/63369#issuecomment-4196742923) **MartinJohns** noted missing playground link and said x resolved to Foo | undefined, suggesting strictNullChecks might be disabled
 * [later](https://github.com/microsoft/TypeScript/issues/63369#issuecomment-4200095009) **codextremist** said "Thanks @MartinJohns . You're right, strictNullChecks solve this!"
 * (later) **codextremist** closed the issue

### [Issue microsoft/TypeScript#63370](https://github.com/microsoft/TypeScript/issues/63370) (Open)

**Add a \`redeclare\` keyword to redeclare class attributes, behaving like \`override \!:\` while keeping type modifiers\.**

*Add a new `redeclare` keyword in TypeScript to override and declare class properties while preserving or adjusting existing type modifiers.*

 * created by **denis-migdal**

### [Issue microsoft/TypeScript#63371](https://github.com/microsoft/TypeScript/issues/63371) (Open)

**NuGet package not available for v5\.5\.4**

*Request for information on when the NuGet package for TypeScript v5.5.4 will be released.*

 * created by **swarajkd**
 * [later](https://github.com/microsoft/TypeScript/issues/63371#issuecomment-4200091566) **guillaumebrunerie** said "v5.5.4 is almost two years old, why do you want a NuGet package for it? "

