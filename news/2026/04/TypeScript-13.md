# Report for 2026-04-13 (Monday, April 13th, 2026)

15 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @valerciora asked for help resolving build errors with TypeScript configuration in [microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4243807156)
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

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4197912770) **SOMONSOUM** suggested removing the baseUrl setting and adding a paths configuration
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4205504780) **ArfanFahad** removed baseUrl and confirmed it worked after adding paths
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4220113144) **Jasper-Nelligan** reported that adding a catch-all paths entry caused VSCode to auto-suggest imports from node_modules and asked if anyone else was facing the issue
 * [later](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4243807156) **valerciora** asked for help resolving build failures and deprecation suppression errors when using TypeScript 5.9.3 with baseUrl and ignoreDeprecations settings

### [PR microsoft/TypeScript#63364](https://github.com/microsoft/TypeScript/pull/63364) (Closed)

**Fix: parameter typo in es5 definitions \#63352**

*Corrects a misleading parameter name in src/lib/es5.d.ts to improve TypeScript definition accuracy.*

 * created by **rishabh1230**
 * (today) **rishabh1230** closed the issue

### [Issue microsoft/TypeScript#63381](https://github.com/microsoft/TypeScript/issues/63381) (Open)

**ESM strict imports mode option to moduleResolution bundler**

*Add a tsconfig option to enforce including file extensions on ESM imports when using bundler moduleResolution*

 * created by **paztis**
 * [today](https://github.com/microsoft/TypeScript/issues/63381#issuecomment-4241363827) **jakebailey** said "If you want to require that, why not use nodenext? The difference between the two modes is effectively just that rule..."
 * [later](https://github.com/microsoft/TypeScript/issues/63381#issuecomment-4242101376) **paztis** described their current TypeScript configuration and reported an incompatibility error TS5110 between moduleResolution and module options

### [Issue microsoft/TypeScript#63383](https://github.com/microsoft/TypeScript/issues/63383) (Closed, `Working as Intended`, **mjbvz**)

**Typescript 'rootDir' error**

*VSCode 1.114+ incorrectly reports TypeScript rootDir errors in a multi-package monorepo configuration despite successful CLI compilation*

 * created by **m-hall**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63383#issuecomment-4231365032) **mkantor** advised explicitly setting rootDir when upgrading to TypeScript 6.0 and suggested using ts5to6 to automate the change
 * **jakebailey** added label `Working as Intended`
 * [later](https://github.com/microsoft/TypeScript/issues/63383#issuecomment-4244528039) **m-hall** said "Ok, looks like updating the tsconfig does solve the issue. Thanks!"
 * (later) **m-hall** closed the issue

### [Issue microsoft/TypeScript#63397](https://github.com/microsoft/TypeScript/issues/63397) (Open)

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

### [Issue microsoft/TypeScript#63399](https://github.com/microsoft/TypeScript/issues/63399) (Open)

**Make object type indexable**

*Enable expressions like obj !== null && typeof obj === 'object' to narrow unknown to an indexable Record<string, unknown>.*

 * created by **dupasj**
 * [today](https://github.com/microsoft/TypeScript/issues/63399#issuecomment-4240396586) **MartinJohns** said "Essentially you want #38801."

### [Issue microsoft/TypeScript#63400](https://github.com/microsoft/TypeScript/issues/63400) (Open)

**Inquiry Regarding Web API Type Support Based on Browser Compatibility Standards**

*Asking which browser compatibility guidelines or authoritative sources TypeScript uses to decide Web API type definitions inclusion.*

 * created by **MomoseMitsuki**
 * [today](https://github.com/microsoft/TypeScript/issues/63400#issuecomment-4241143081) **MartinJohns** referred to the Microsoft TypeScript DOM lib generator for DOM-related types and noted that general JavaScript types are included when they're at least stage 3 and not experimental
 * [later](https://github.com/microsoft/TypeScript/issues/63400#issuecomment-4244796576) **guest271314** said "I don't think anything is stopping you from creating your own types."

