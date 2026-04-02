# Report for 2026-03-13 (Friday, March 13th, 2026)

8 different users commented on 32 different issues.

## Recommended Actions

 * Response Recommended
    * @kkmuffme suggested that this issue was a duplicate of issue #44366 in [microsoft/TypeScript#42564](https://github.com/microsoft/TypeScript/issues/42564#issuecomment-4057975445)
    * @monsanto provided repro steps as requested in [microsoft/TypeScript#62200](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4060436192)

## Activity Summary

### [Issue microsoft/TypeScript#42564](https://github.com/microsoft/TypeScript/issues/42564) (Closed, `Suggestion`, `In Discussion`)

**Constrained usage of type guard functions in conditions**

*TypeScript fails to narrow types when a type guard function is compared to false instead of using !.*

 * created by **lukejagodzinski**
 * (5.1 years ago) **RyanCavanaugh** added labels `In Discussion`, `Suggestion`
 * [today](https://github.com/microsoft/TypeScript/issues/42564#issuecomment-4057975445) **kkmuffme** said "Isn't this a duplicate of https://github.com/microsoft/TypeScript/issues/44366 (which has been fixed in the meantime)"
 * [today](https://github.com/microsoft/TypeScript/issues/42564#issuecomment-4058340405) **RyanCavanaugh** said "Indeed!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#60561](https://github.com/microsoft/TypeScript/issues/60561) (Closed, `Working as Intended`)

**Module resolution: NodeNext breaks typechecking**

*Using nodenext moduleResolution and --transform-types in TypeScript breaks type checking despite correct module resolution.*

 * [45 weeks ago](https://github.com/microsoft/TypeScript/issues/60561#issuecomment-2847690585) **RyanCavanaugh** said "Yeah, that does look wrong. It looks like the re-exported default chain isn't being correctly preserved as callable/constructable"
 * [42 weeks ago](https://github.com/microsoft/TypeScript/issues/60561#issuecomment-2903953632) **damianobarbati** inquired if the issue should be posted in the ioredis repository or in the tsc package
 * **andrewbranch** added to milestone `TypeScript 5.9.0`
 * (today) **andrewbranch** added label `Working as Intended`, removed label `Needs Investigation`, and unassigned **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/60561#issuecomment-4056735977) **andrewbranch** explained that the ioredis typings bug arose from the double assignment in index.js and a mismatched TypeScript declaration, causing the analysis tool to misinterpret the default export and suggest incorrect import usage

### [Issue microsoft/TypeScript#62200](https://github.com/microsoft/TypeScript/issues/62200) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**)

**Deprecate, remove \`\-\-moduleResolution node10\`**

*Remove the outdated --moduleResolution node/node10 flag in TypeScript 7.0, advising nodenext for Node.js and esnext with bundler for web.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-3536829117) **Adesoji1** said "so what's the solution?"
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-3543611338) **RyanCavanaugh** said "Depends on the problem, we usually say"
 * [today](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4054811294) **monsanto** reported encountering TS2351 errors with default class exports in NodeNext, hypothesized a TypeScript bug, offered to share a repro, and requested a fix before removing moduleResolution: node
 * [today](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4056497943) **RyanCavanaugh** said "@monsanto a repro would be extremely helpful, thanks"
 * [later](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4060436192) **monsanto** provided a link to a related TypeScript issue as a repro

### [Issue microsoft/TypeScript#63189](https://github.com/microsoft/TypeScript/issues/63189) (Open, `Bug`, `Domain: Decorators`)

**Incorrect reference \`this\` in static context with \`experimentalDecorators\` enabled**

*With experimentalDecorators enabled TypeScript incorrectly emits static `this` references as undefined rather than the class.*

 * created by **yavanosta**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63189#issuecomment-3961176209) **RyanCavanaugh** provided an auto-generated list of similar issues to assist the user
 * [today](https://github.com/microsoft/TypeScript/issues/63189#issuecomment-4058106478) **RyanCavanaugh** said "Looks like a duplicate of #56503"
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63189#issuecomment-4058121992) **yavanosta** clarified that the issue was not a duplicate of #56503, noting one concern involved static members and the other involved decorators
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: Decorators`, removed label `Duplicate`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195) (Open, `Needs More Info`)

**Debug Failure: "No error for last overload signature" crash when CustomTypeOptions\.resources uses typeof on a large \(~10k line\) JSON file**

*TypeScript crashes with 'No error for last overload signature' when using typeof on a large JSON for i18next CustomTypeOptions.resources.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-3996641257) **shahanahmed86** said "@RyanCavanaugh don't close issue, It will take me some time but I will share the concrete repro, honestly, super busy since the day I post this issue."
 * [today](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4054861901) **shahanahmed86** apologized for not providing a minimal repro, identified that the crash occurs when TypeScript hits the 5-million type-instantiation limit processing i18next’s types over a large translation JSON, and provided reproduction details and code snippets
 * (today) **RyanCavanaugh** added label `Needs More Info`, and removed label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4058537717) **RyanCavanaugh** said "Still can't repro this. Can you set up a cloneable repo?"

### [Issue microsoft/TypeScript#63199](https://github.com/microsoft/TypeScript/issues/63199) (Open, `Bug`, `Domain: Crashes`)

**Crash: TypeError: Cannot read properties of undefined \(reading 'aliasSymbol'\) remains when using variadic tuple with \(infer C\)\[\] and constrained infer**

*TypeScript compiler throws a TypeError reading 'aliasSymbol' when inferring variadic tuple types with a constrained infer array.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977102585) **Andarist** said "Im pretty sure https://github.com/microsoft/TypeScript/pull/63014 fixes this and this issue is a duplicate of https://github.com/microsoft/TypeScript/issues/63005"
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977198462) **na7ure-a** thanked the maintainer, tested the fix locally, confirmed the crash in #63005 was resolved but that the issue’s code snippet still crashed, and asked to test with the exact code from the issue
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977724475) **Andarist** apologized for misunderstanding and pushed a fix for the missing cases to the PR
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-4058143075) **RyanCavanaugh** expressed reluctance to include the PR in TS 6 without evidence from real codebases and noted that @na7ure-a's fuzzing isn't indicative of priority
 * **RyanCavanaugh** added label `Domain: Crashes`

### [Issue microsoft/TypeScript#63207](https://github.com/microsoft/TypeScript/issues/63207) (Open, `Bug`, `Domain: check: Type Circularity`)

**tsserver hangs indefinitely when inferring return type of class method that passes this to a function with deeply nested conditional return type**

*tsserver hangs when inferring a class method’s return type using remeda.pick without an explicit annotation due to circular type inference*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63207#issuecomment-3994012407) **RyanCavanaugh** explained that the hang was caused by an undetected type-checking cycle, linked to a relevant FAQ, and suggested annotating return types or using type assertions to unblock work
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63207#issuecomment-4040931836) **RyanCavanaugh** noted that tsgo finished in finite time, suggested tsc would finish in another 30 seconds, and listed TypeScript compilation errors and metrics
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63207#issuecomment-4040938729) **RyanCavanaugh** said "The emitted a.d.ts is 48 megabytes 🫨"
 * (today) **RyanCavanaugh** added labels `Bug`, `Domain: check: Type Circularity`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63216](https://github.com/microsoft/TypeScript/issues/63216) (Closed, `Duplicate`)

**\`keyof\` behaves differently with index signatures created using \`Record\`**

*The keyof operator returns string|number for an explicit {[x: string]: unknown} index signature but only string for Record<string, unknown> despite both supporting numeric indexing.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4017187645) **jcalz** said "Duplicate #31013"
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4025537931) **RyanCavanaugh** provided an automatically generated analysis and list of similar issues
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63216#issuecomment-4059102044) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63223](https://github.com/microsoft/TypeScript/issues/63223) (Open, `Bug`, `Domain: flag: isolatedDeclarations`)

**Toggling \`isolatedModules\` in \`tsconfig\.json\` while running the compiler in \`watch\` mode, doesn't re\-emit \`const enums\`, unlike toggling \`preserveConstEnums\`, which does**

*Unlike preserveConstEnums toggles, changing isolatedModules in watch mode does not re-emit const enums until a full rebuild.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63223#issuecomment-4025538117) **RyanCavanaugh** provided an automated list of similar issues
 * (2 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * **RyanCavanaugh** added label `Domain: flag: isolatedDeclarations`

### [Issue microsoft/TypeScript#63230](https://github.com/microsoft/TypeScript/issues/63230) (Open, `Bug`, `Domain: Crashes`)

**Compiler crash: Debug Failure in visitEachChildOfIndexSignatureDeclaration**

*TypeScript compiler crashes with a Debug Failure in visitEachChildOfIndexSignatureDeclaration when addInitializer uses an invalid index signature annotation*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63230#issuecomment-4040769522) **Andarist** explained that Corsa did not crash because it did not assert on missing .type and allowed nil to propagate while Strada expected .type
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63230#issuecomment-4040793418) **juanjh1** provided a minimal repro snippet with TypeScript code and a screenshot
 * **RyanCavanaugh** added label `Domain: Crashes`

### [Issue microsoft/TypeScript#63234](https://github.com/microsoft/TypeScript/issues/63234) (Closed, `Working as Intended`)

**TypeScript Rename Refactoring Fails to Preserve Object Shorthand Keys in VS Code**

*Renaming a TypeScript variable in an object shorthand with aliases off renames both key and value instead of expanding shorthand.*

 * created by **Hasan-Mir**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63234#issuecomment-4058120121) **RyanCavanaugh** clarified that the typescript.preferences.useAliasesForRenames setting disables shorthand expansion
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63235](https://github.com/microsoft/TypeScript/issues/63235) (Closed, `7.0 LS Migration`)

**Monorepo package exports suggested as relative imports when using re\-exported identifiers**

*VS Code suggests relative file imports for re-exported identifiers instead of using the package’s export path in a monorepo*

 * created by **aryzing**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63235#issuecomment-4058087831) **RyanCavanaugh** said "For LS bugs, please a) provide a cloneable repo (there are many ways to set up a monorepo, we cannot guess) and b) confirm in typescript-go and post in that repo. Thanks!"
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63240](https://github.com/microsoft/TypeScript/issues/63240) (Open, `Bug`, `Domain: flag: exactOptionalPropertyTypes`)

**Error from \`exactOptionalPropertyTypes\` not reported when using object spread with a ternary and optional property acces**

*TypeScript's exactOptionalPropertyTypes fails to report an error when combining object spread, a ternary expression, and optional property access.*

 * created by **aswinsvijay**
 * **RyanCavanaugh** added label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/63240#issuecomment-4057633138) **RyanCavanaugh** said "Confirmed repro in tsgo"
 * (today) **RyanCavanaugh** added label `Domain: flag: exactOptionalPropertyTypes`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63243](https://github.com/microsoft/TypeScript/issues/63243) (Closed, `Duplicate`)

**PromiseRejectedResut reason should be \`unknown\`**

*Require the PromiseRejectedResult.reason type in the es2020 promise library to be unknown instead of any*

 * created by **karlismelderis-mckinsey**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63243#issuecomment-4045154423) **MartinJohns** said "Essentials a duplicate of #45602."
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#63244](https://github.com/microsoft/TypeScript/issues/63244) (Open, `Needs Proposal`)

**bug\(lib\): Explicitly stating wrong return type of \`Promise\.then\` without arguments results in no error**

*Current TypeScript versions fail to report a type mismatch when Promise<string> is assigned from Promise.resolve(1).then() with no arguments.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4047353571) **iluha168** suggested splitting the PromiseLike.then and Promise.then definitions into two overloads to avoid the NoInfer breaking change and maintain return type hints
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4050549212) **Andarist** mentioned another instance of .then's typing affecting a scenario negatively and linked to a related TypeScript issue
 * [today](https://github.com/microsoft/TypeScript/issues/63244#issuecomment-4055854137) **paigefletcher1282-code** reported that the issue hadn't yet been reproduced and linked to issue #62071
 * **RyanCavanaugh** added label `Needs Proposal`

### [Issue microsoft/TypeScript#63245](https://github.com/microsoft/TypeScript/issues/63245) (Open, `Discussion`)

**Bloomberg feedback for 6\.0**

*Bloomberg reports moderate impact from TypeScript 6.0 RC, citing deprecated node module resolution, type checking regressions, JS emit changes, and removed hasDefaultLib API.*

 * created by **dragomirtitian**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63245#issuecomment-4045864995) **MartinJohns** expressed amazement that all projects used the node moduleResolution despite fewer than 1% of packages being affected
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63245#issuecomment-4046613300) **dragomirtitian** clarified that 100% of projects used node resolution but fewer than 1% experienced issues when moved to bundler
 * **RyanCavanaugh** added label `Discussion`

### [PR microsoft/TypeScript#63246](https://github.com/microsoft/TypeScript/pull/63246) (Closed, **DanielRosenwasser**)

**🤖 Pick PR \#63239 \(Fix missing lib files in reused pro\.\.\.\) into release\-6\.0**

*Cherry-pick PR #63239 into the release-6.0 branch to restore missing library files.*

 * created by **typescript-bot**
 * **typescript-bot** assigned to **DanielRosenwasser**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63247](https://github.com/microsoft/TypeScript/issues/63247) (Closed, `Duplicate`)

**Tor**

*TypeScript intentionally ignores type narrowings inside callbacks and does not reset them after function calls.*

 * created by **angelgsbrielruano**
 * **angelgsbrielruano** added label `Duplicate`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63249](https://github.com/microsoft/TypeScript/pull/63249) (Open)

**fix: add affectsEmit/affectsBuildInfo/affectsSemanticDiagnostics to isolatedModules option**

*Add affectsEmit, affectsBuildInfo, and affectsSemanticDiagnostics to the isolatedModules option to ensure watch mode re-emits const enum files.*

 * created by **GokhanKabar**

### [Issue microsoft/TypeScript#63250](https://github.com/microsoft/TypeScript/issues/63250) (Closed, `Not a Defect`)

**\# Bug Report: \`Omit\`\-based assertion narrowing fails to override method return types on classes with private members**

*Assertion narrowing using Omit on a class with private members fails to update its method's return type.*

 * created by **deyaaeldeen**
 * [today](https://github.com/microsoft/TypeScript/issues/63250#issuecomment-4058761505) **RyanCavanaugh** explained that assertion narrowings can't widen types so Client remains intersected, affecting overload resolution, and outlined why altering the process would break other behaviors
 * **RyanCavanaugh** added label `Not a Defect`

### [Issue microsoft/TypeScript#63251](https://github.com/microsoft/TypeScript/issues/63251) (Open, `Suggestion`, `Needs Proposal`)

**Mechanism to specify input source location to find \`package\.json\` instead of output source location when determining module format**

*Provide a mechanism to use source directory instead of output directory when locating package.json for NodeNext module resolution*

 * created by **monsanto**

### [PR microsoft/TypeScript#63252](https://github.com/microsoft/TypeScript/pull/63252) (Open)

**Fix exactOptionalPropertyTypes not enforced through spread\-with\-terna…**

*Enforce exactOptionalPropertyTypes on spread-with-ternary expressions by normalizing missingType to undefined before addOptionality*

 * created by **GokhanKabar**

