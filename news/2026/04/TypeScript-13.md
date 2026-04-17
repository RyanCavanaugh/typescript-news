# Report for 2026-04-13 (Monday, April 13th, 2026)

15 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @Janther reported that TypeScript hover shows 'string' instead of an empty string literal in [microsoft/TypeScript#45329](https://github.com/microsoft/TypeScript/issues/45329#issuecomment-4245129346)
    * @paztis reported a TypeScript configuration error TS5110 in [microsoft/TypeScript#63381](https://github.com/microsoft/TypeScript/issues/63381#issuecomment-4242101376)
    * @guillaumebrunerie asked if this approach suits the use case in [microsoft/TypeScript#63397](https://github.com/microsoft/TypeScript/issues/63397#issuecomment-4238179681)
    * @conartist6 reported that the TS parser accepted unconventional code as valid in [microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238372874)
    * @conartist6 provided repro steps and version information in [microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238804046)
    * @nmain reported syntax errors in the example playground in [microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238908847)
    * @conartist6 asked if omitting extra symbols is a semantics issue rather than syntax in [microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238997510)
    * @snarbles2 asked what was expected to happen in [microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4243716992)

## Activity Summary

### [Issue microsoft/TypeScript#17253](https://github.com/microsoft/TypeScript/issues/17253) (Open, `Domain: check: Control Flow`, `Possible Improvement`)

**Properties of instances of anonymous classes have type \<any\> after an instanceof guard\.**

*TypeScript fails to enforce generic property types on instances of anonymous classes after an instanceof check.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/17253#issuecomment-2501750703) **joeedh** suggested updating getTypeOfPrototypeProperty to use type.default fallback for type parameters
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/17253#issuecomment-2646346484) **maximan3000** provided a temporary solution by duplicating a non-generic class with inheritance to fix TypeScript inference, including code and a sandbox link
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * (later) **ahejlsberg** added label `Possible Improvement`, and removed label `Bug`
 * [later](https://github.com/microsoft/TypeScript/issues/17253#issuecomment-4244726458) **ahejlsberg** changed the label from "bug" to "possible improvement" and suggested substituting `unknown` instead of `any` for type parameters with `instanceof`, noting it’s safer for covariant but still unsound for contravariant positions

### [Issue microsoft/TypeScript#45329](https://github.com/microsoft/TypeScript/issues/45329) (Open, `Suggestion`, `Awaiting More Feedback`)

**String union types narrowed to falsy should narrow string to ""**

*TypeScript fails to narrow string union types to empty string on falsy checks, resulting in false|string instead.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/45329#issuecomment-1059797670) **JoshuaKGoldberg** apologized for missing the mention and described using empty string instead of null or undefined in response type unions with an example
 * [36 weeks ago](https://github.com/microsoft/TypeScript/issues/45329#issuecomment-3133678262) **chrisvfritz** highlighted the incomplete implementation of empty string type narrowing in TypeScript and advocated for improved narrowing to avoid hacks
 * [later](https://github.com/microsoft/TypeScript/issues/45329#issuecomment-4245129346) **Janther** mentioned encountering the same issue, shared a code example returning a Doc or string, and noted that TypeScript hover shows "string" instead of the empty string literal

### [PR microsoft/TypeScript#63364](https://github.com/microsoft/TypeScript/pull/63364) (Closed)

**Fix: parameter typo in es5 definitions \#63352**

*Corrects a misleading parameter name in src/lib/es5.d.ts to improve TypeScript definition accuracy.*

 * created by **rishabh1230**
 * (today) **rishabh1230** closed the issue

### [Issue microsoft/TypeScript#63381](https://github.com/microsoft/TypeScript/issues/63381) (Open, `Needs More Info`)

**ESM strict imports mode option to moduleResolution bundler**

*Add a tsconfig option to enforce including file extensions on ESM imports when using bundler moduleResolution*

 * created by **paztis**
 * [today](https://github.com/microsoft/TypeScript/issues/63381#issuecomment-4241363827) **jakebailey** said "If you want to require that, why not use nodenext? The difference between the two modes is effectively just that rule..."
 * [later](https://github.com/microsoft/TypeScript/issues/63381#issuecomment-4242101376) **paztis** described their current TypeScript configuration and reported an incompatibility error TS5110 between moduleResolution and module options
 * **RyanCavanaugh** added label `Needs More Info`

### [Issue microsoft/TypeScript#63383](https://github.com/microsoft/TypeScript/issues/63383) (Closed, `Working as Intended`, **mjbvz**)

**Typescript 'rootDir' error**

*VSCode 1.114+ incorrectly reports TypeScript rootDir errors in a multi-package monorepo configuration despite successful CLI compilation*

 * created by **m-hall**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63383#issuecomment-4231365032) **mkantor** advised explicitly setting rootDir when upgrading to TypeScript 6.0 and suggested using ts5to6 to automate the change
 * **jakebailey** added label `Working as Intended`
 * [later](https://github.com/microsoft/TypeScript/issues/63383#issuecomment-4244528039) **m-hall** said "Ok, looks like updating the tsconfig does solve the issue. Thanks!"
 * (later) **m-hall** closed the issue

### [Issue microsoft/TypeScript#63384](https://github.com/microsoft/TypeScript/issues/63384) (Closed, `Won't Fix`, `7.0 LS Migration`)

**JS and TS Tasking long time to start which make the save of tsx files slower\.**

*Delays in the JavaScript and TypeScript formatter startup are slowing or blocking TSX file saves.*

 * created by **flexdevguy**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * **RyanCavanaugh** added label `Won't Fix`
 * [later](https://github.com/microsoft/TypeScript/issues/63384#issuecomment-4245038508) **RyanCavanaugh** said "See #62827"
 * (later) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** added label `7.0 LS Migration`

### [Issue microsoft/TypeScript#63391](https://github.com/microsoft/TypeScript/issues/63391) (Open, `Bug`, `Domain: JS Emit`, `Fix Available`)

**The module namespace object returned by \_\_importStar is not the same when import the same module multiple times**

*TypeScript’s compiled CommonJS __importStar helper creates separate namespace objects for repeated imports of the same module.*

 * created by **yanjiew1**
 * **RyanCavanaugh** added label `Bug`
 * [later](https://github.com/microsoft/TypeScript/issues/63391#issuecomment-4245031560) **RyanCavanaugh** noted that there was no reasonable space for runtime helpers to stash a global lookup table and questioned why the user was using commonjs instead of a modern target
 * **RyanCavanaugh** added to milestone `Dormant`

### [Issue microsoft/TypeScript#63392](https://github.com/microsoft/TypeScript/issues/63392) (Open, `Docs`, **RyanCavanaugh**)

**Review/update https://typescriptlang\.org/tsconfig for TS 6\.0**

*The TypeScript tsconfig documentation is outdated for version 6.0, showing incorrect defaults and options for target, types, paths, rootDir, and module.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4231401777) **mkantor** suggested relocating the issue to the TypeScript-Website repository while noting template and visibility concerns, and offered to refile it if desired
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4231403772) **mkantor** offered to draft a pull request but deferred to a maintainer and asked if a first pass would be helpful
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4231410817) **mkantor** said "If anyone spots additional items requiring attention, please post them as comments and I'll add them to my list."
 * **RyanCavanaugh** added label `Docs`
 * [later](https://github.com/microsoft/TypeScript/issues/63392#issuecomment-4244991841) **RyanCavanaugh** said "I started this at https://github.com/RyanCavanaugh/schemastore/pull/1 but haven't had time to get it over the finish line. Feel free to doublecheck this; it's not fully vetted yet."
 * **RyanCavanaugh** assigned to **RyanCavanaugh**

### [Issue microsoft/TypeScript#63397](https://github.com/microsoft/TypeScript/issues/63397) (Open, `Suggestion`, `Needs Proposal`)

**skipLibChecks specificity**

*Enable skipLibCheck to accept glob patterns for selectively skipping type checking on specified declaration files.*

 * created by **dragomirtitian**
 * [today](https://github.com/microsoft/TypeScript/issues/63397#issuecomment-4237637681) **dragomirtitian** said "This  is similar to https://github.com/microsoft/TypeScript/issues/30511 but that issue is specifically for just node_modules"
 * [today](https://github.com/microsoft/TypeScript/issues/63397#issuecomment-4238179681) **guillaumebrunerie** suggested using regular .ts files with declare global blocks instead of handwritten .d.ts files to ensure proper type checking even with skipLibCheck

### [Issue microsoft/TypeScript#63398](https://github.com/microsoft/TypeScript/issues/63398) (Closed, `Unactionable`)

**Two ExpressionStatements allowed on one line with no semicolon\!**

*TypeScript incorrectly accepts two expression statements on a single line without a semicolon instead of throwing a parse error.*

 * created by **conartist6**
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238372874) **conartist6** noted that the TypeScript parser accepted unconventional code as valid
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238469131) **nmain** said "This doesn't reproduce obviously in 6.0.2.  Please fill out the entire template including a minimal, version numbers, etc."
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238804046) **conartist6** provided a TypeScript Playground link and noted it reproduced on version 6.0.2
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238908847) **nmain** reported that the example produced 10 syntax errors in the playground
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4238997510) **conartist6** said "That example scrambles my brain. If it's just a matter of ignoring some spurious errors, surely that means that in this language omitting those extra symbols is a matter of semantics not syntax...?"
 * [today](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4239696983) **mkantor** said ""Unexpected keyword or identifier" sounds like a syntax error to me. What do you mean by "ignoring some spurious errors"?"
 * [later](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4243716992) **snarbles2** said "What are you expecting to happen that is not happening?"
 * [later](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4244051165) **conartist6** expressed surprise that the runtime assigns concrete meaning to undefined behavior and characterized the parse error as a lint-like warning while noting that multi-statement lines are fundamental to TypeScript
 * [later](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4244074729) **conartist6** observed that the project parser isn't considered the definitive Typescript parser and that the Prettier parser defines valid Typescript syntax
 * [later](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4244223556) **nmain** marked the issue as a duplicate of issue #44232
 * **RyanCavanaugh** added label `Unactionable`
 * [later](https://github.com/microsoft/TypeScript/issues/63398#issuecomment-4244940165) **RyanCavanaugh** clarified that the issue was a misunderstanding and that TypeScript cannot permit invalid syntax
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63399](https://github.com/microsoft/TypeScript/issues/63399) (Closed, `Duplicate`)

**Make object type indexable**

*Enable expressions like obj !== null && typeof obj === 'object' to narrow unknown to an indexable Record<string, unknown>.*

 * created by **dupasj**
 * [today](https://github.com/microsoft/TypeScript/issues/63399#issuecomment-4240396586) **MartinJohns** said "Essentially you want #38801."
 * **RyanCavanaugh** added label `Duplicate`
 * [later](https://github.com/microsoft/TypeScript/issues/63399#issuecomment-4244967183) **RyanCavanaugh** said "This is obviously fine on the read side but it's pretty dangerous if you have a write inside the if, since Record is basically any in terms of obj.prop = value"

### [Issue microsoft/TypeScript#63400](https://github.com/microsoft/TypeScript/issues/63400) (Closed)

**Inquiry Regarding Web API Type Support Based on Browser Compatibility Standards**

*Asking which browser compatibility guidelines or authoritative sources TypeScript uses to decide Web API type definitions inclusion.*

 * created by **MomoseMitsuki**
 * [today](https://github.com/microsoft/TypeScript/issues/63400#issuecomment-4241143081) **MartinJohns** referred to the Microsoft TypeScript DOM lib generator for DOM-related types and noted that general JavaScript types are included when they're at least stage 3 and not experimental
 * [later](https://github.com/microsoft/TypeScript/issues/63400#issuecomment-4244796576) **guest271314** said "I don't think anything is stopping you from creating your own types."
 * (later) **MomoseMitsuki** closed the issue

