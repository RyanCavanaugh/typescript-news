# Report for 2025-12-03 (Wednesday, December 3rd, 2025)

26 different users commented on 34 different issues.

## Recommended Actions

 * Response Recommended
    * @alvaro-cuesta asked if they were missing something because `typeof this` wasn’t working in [microsoft/TypeScript#3841](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3611367593)
    * @lokalise-mark provided a reproduction repo for the memory usage issue when test files are processed in [microsoft/TypeScript#57710](https://github.com/microsoft/TypeScript/issues/57710#issuecomment-3609929985)
    * @moznion asked whether the core issue lies in type inference or elsewhere in [microsoft/TypeScript#62790](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3610467030)
    * @moznion reported that the issue still occurs on the latest main branch in [microsoft/TypeScript#62790](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3611415516)
    * @jedwards1211 suggested limiting suggestions based on package size rather than entry point count in [microsoft/TypeScript#62829](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3608828162)
    * @jedwards1211 asked if including multiple file formats trips tsserver up in [microsoft/TypeScript#62829](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3610454675)
    * @wnadurski asked to keep this issue open for clearer reference until the bug is fixed in [microsoft/TypeScript#62831](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3612714470)

## Activity Summary

### [Issue microsoft/TypeScript#35180](https://github.com/microsoft/TypeScript/issues/35180) (Closed, `Bug`, `Help Wanted`, `Effort: Moderate`, `Domain: LS: Completion Lists`, `7.0 LS Migration`)

**Suggestions for property names don't show available keys**

*Autocompletion for object literal properties in union types only suggests common keys instead of keys from the selected variant*

 * (yesterday) **RyanCavanaugh** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/35180#issuecomment-3604507736) **RyanCavanaugh** said "Closing language service bugs related to the 6.0 implementation. For more information, see #62827"
 * [today](https://github.com/microsoft/TypeScript/issues/35180#issuecomment-3608955060) **mjbvz** said "Confirming that this seems fixed in both 6.0 and TS-go"

### [Issue microsoft/TypeScript#3841](https://github.com/microsoft/TypeScript/issues/3841) (Open, `Suggestion`, `In Discussion`)

**T\.constructor should be of type T**

*Suggest typing instance.constructor as the class type rather than Function to enable direct static property access without casting.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-2381594311) **jwbth** described how to avoid access-blocking to the prototype by declaring the constructor property in classes when useDefineForClassFields is enabled, noted that this applies when target is es2020 or higher, and pointed to relevant TypeScript documentation
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-2415542548) **thodnev** requested adding the issue to TS milestones, highlighted a divergent change code smell risk and endorsed @jwbth's one-line solution
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3263206692) **FrameMuse** described applying `declare ["constructor"]: typeof this` in a superclass to enable correct subclass inheritance, and noted that it failed for the Object interface because Object isn’t treated as a superclass by default
 * [later](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3611367593) **alvaro-cuesta** asked if they were missing something when `typeof this` didn’t work, noting that explicitly specifying each constructor worked
 * [later](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3612212409) **snarbles2** clarified that `this` and `typeof this` yield the same instance type and that `typeof this` does not refer to the constructor
 * [later](https://github.com/microsoft/TypeScript/issues/3841#issuecomment-3612606091) **FrameMuse** apologized for confusion and clarified that typeof this does not refer to the constructor inside the class body but does in static methods

### [Issue microsoft/TypeScript#41461](https://github.com/microsoft/TypeScript/issues/41461) (Closed, `Suggestion`, `Experience Enhancement`)

**Generic constrained to function: parameter is incorrectly inferred as \`any\`**

*The generic useCallback signature constrained to a function type incorrectly infers its callback parameter as any instead of its explicit type.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5 years ago](https://github.com/microsoft/TypeScript/issues/41461#issuecomment-724369077) **RyanCavanaugh** explained that the contextual type was `undefined | (x: string) => void` instead of just `(x: string) => void`, which broke the matching logic for inferring `T` from the return type
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/41461#issuecomment-1427792006) **Andarist** said "It's likely related to this: https://github.com/microsoft/TypeScript/issues/50719#issuecomment-1247417611"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#46802](https://github.com/microsoft/TypeScript/issues/46802) (Open, `Suggestion`, `Awaiting More Feedback`)

**\[Feature Request\] fieldof similar to keyof but include private and protected field**

*Introduce a TypeScript utility type 'fieldof' that enumerates private and protected class fields for mapped types.*

 * [4 years ago](https://github.com/microsoft/TypeScript/issues/46802#issuecomment-971389451) **jonlepage** demonstrated a workaround using an abstract class with a useWritable() method and expressed interest in extracting all fields without type assertions
 * [34 weeks ago](https://github.com/microsoft/TypeScript/issues/46802#issuecomment-2776826218) **katz12** described a use case with branded classes containing private fields, explained a type mapping issue using Resolve with keyof, and reported resolving it by removing the Resolve type
 * [26 weeks ago](https://github.com/microsoft/TypeScript/issues/46802#issuecomment-2941949534) **jimtendo** described a testing use-case for spyOn-like features by introducing a MakePublic utility type and providing example code
 * [today](https://github.com/microsoft/TypeScript/issues/46802#issuecomment-3607730661) **benwiley4000** described a TypeScript use case of updating private numeric members via a generic class method and provided a code example

### [Issue microsoft/TypeScript#50719](https://github.com/microsoft/TypeScript/issues/50719) (Closed, `Bug`, `Help Wanted`, `Domain: check: Type Inference`)

**Function parameter does not get inferred through target typing by a union through a layer of indirection**

*TypeScript fails to infer the parameter type of a callback function when that callback is wrapped in a union type and passed through an indirect generic.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/50719#issuecomment-1419026245) **Andarist** attempted to filter the contextual type by applicable constraints and create an intersection, and observed correct but slow results
 * (1.7 years ago) **RyanCavanaugh** added label `Domain: Type Inference`, and set milestone to `Backlog`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#56182](https://github.com/microsoft/TypeScript/pull/56182) (Closed, `For Uncommitted Bug`, **rbuckton**)

**Include source node inferences in string literal completions deeper in arguments**

*Expand string literal completions to include source node inferences for nested function arguments.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/pull/56182#issuecomment-2081536908) **Andarist** said "@andrewbranch @sandersn is there anything blocking this from being merged? :)"
 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/56182#issuecomment-2318988662) **Andarist** addressed code organization by moving logic closer to services and acknowledged the previous structure was suboptimal
 * [40 weeks ago](https://github.com/microsoft/TypeScript/pull/56182#issuecomment-2676740209) **Andarist** said "@jakebailey with 2 approvals, could this land now? :)"
 * [today](https://github.com/microsoft/TypeScript/pull/56182#issuecomment-3609378029) **jakebailey** said "@Andarist Can you merge main so CI is fresh?"
 * [later](https://github.com/microsoft/TypeScript/pull/56182#issuecomment-3611816868) **Andarist** said "@jakebailey done"

### [Issue microsoft/TypeScript#57710](https://github.com/microsoft/TypeScript/issues/57710) (Open, `Needs More Info`)

**Regression performance compiling types in version 5\.4\.2**

*TypeScript 5.4.2 exhibits a major type-checking performance regression compared to version 5.3.3 on a large codebase.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/57710#issuecomment-2040059013) **Katli95** asked how to bisect the problem on GitHub Actions and inquired about the best methods to detect it, such as local testing or monitoring memory spikes
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/57710#issuecomment-2040095179) **jakebailey** said "--extendedDiagnostics should show memory usage, or you could artificially lower the max memory with Node's max-old-space-size. That or provide a repro."
 * [39 weeks ago](https://github.com/microsoft/TypeScript/issues/57710#issuecomment-2693945734) **MisanthropicBit** provided diagnostic traces showing OOM error in Docker CI caused by large union types in @octokit/types and suggested temporary workarounds
 * [today](https://github.com/microsoft/TypeScript/issues/57710#issuecomment-3609929985) **lokalise-mark** reported a ~10% memory increase when upgrading past TypeScript 5.3.3 affecting test files and provided a reproduction repository

### [Issue microsoft/TypeScript#57905](https://github.com/microsoft/TypeScript/issues/57905) (Closed, `Bug`, `Help Wanted`, `Domain: check: Variance Relationships`)

**Sync/Async mix return types with Generics not allowed**

*TypeScript incorrectly disallows a synchronous generic subclass override of a method with return type T | Promise<T>.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/57905#issuecomment-2015988241) **RyanCavanaugh** described a type inference failure when unifying subclass and superclass signatures resulting in a union including Promise that fails to extend the constraint and suggested trying each union member separately to improve inference
 * **RyanCavanaugh** added label `Domain: Variance Relationships`
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#58910](https://github.com/microsoft/TypeScript/pull/58910) (Closed, `For Backlog Bug`, **weswigham**)

**Filter return type inferences by constraint applicability**

*Modify TypeScript’s inference algorithm to filter inferred return types based on applicable generic constraints.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-2227055468) **ehoogeveen-medweb** noted that the !inferredType case now always uses instantiatedConstraint and asked if that was intended
 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-2227113165) **Andarist** said "No, that wasn't intentional. Thanks for pointing that out - I corrected the PR but I doubt it will make a difference for any of the extended tests."
 * [1.2 years ago](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-2337751874) **Andarist** said "@gabritto @weswigham friendly 🏓 :)"
 * [today](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-3607603302) **jakebailey** requested the TypeScript bot to test and pack
 * [today](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-3607603683) **typescript-bot** reported CI build jobs starting and completion statuses
 * [today](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-3607625896) **typescript-bot** provided an installable tgz link and testing instructions for the TypeScript 6.0.0-insiders build
 * [today](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-3607666436) **jakebailey** said "Just to note it, this code now matches the fix that Anders applied separately in the Go codebase, so this should be good as-is now, yay."
 * [today](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-3607723240) **typescript-bot** reported that DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-3607749818) **typescript-bot** reported the user test run results comparing main and the PR merge, noting one Git clone failure and that everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-3607851763) **typescript-bot** posted performance run results detailing errors, symbols, types, memory usage, and parse time comparisons between baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/58910#issuecomment-3608015519) **typescript-bot** reported tsc comparison between main and PR branch and highlighted an unused '@ts-expect-error' directive in refined-github
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#61999](https://github.com/microsoft/TypeScript/pull/61999) (Open, `For Backlog Bug`)

**Don't defer index types for non\-generic substitution types**

*Stop deferring index type resolution for non-generic substitution types in the TypeScript compiler.*

 * created by **Andarist**
 * (21 weeks ago) **typescript-bot** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/61999#issuecomment-3610086295) **jakebailey** requested the TypeScript bot to test and pack
 * [today](https://github.com/microsoft/TypeScript/pull/61999#issuecomment-3610086531) **typescript-bot** posted automated status updates for build jobs
 * [today](https://github.com/microsoft/TypeScript/pull/61999#issuecomment-3610095197) **typescript-bot** provided installation instructions and links for testing the TypeScript 6.0.0 insiders build
 * [today](https://github.com/microsoft/TypeScript/pull/61999#issuecomment-3610149860) **typescript-bot** notified that the DT test results were ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/61999#issuecomment-3610176907) **typescript-bot** reported user test results showed no issues aside from unrelated infrastructure failures
 * [today](https://github.com/microsoft/TypeScript/pull/61999#issuecomment-3610365393) **typescript-bot** provided the requested performance run comparison report
 * [today](https://github.com/microsoft/TypeScript/pull/61999#issuecomment-3610445480) **typescript-bot** reported running tsc on the top 400 repos comparing main and the PR merge and found everything looked good

### [Issue microsoft/TypeScript#62030](https://github.com/microsoft/TypeScript/issues/62030) (Closed, `Needs More Info`)

**VS Code removes trailing comma in export statement**

*VS Code with Format on Save enabled removes the trailing comma in ES module export statements in .mjs files.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3053561406) **RyanCavanaugh** said "I can't repro this. Have you tested with extension bisect?"
 * **RyanCavanaugh** added label `Needs More Info`
 * (yesterday) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62030#issuecomment-3608365001) **craxal** confirmed reproduction of the issue, ran a bisect that did not identify an extension cause, and attached a screenshot

### [PR microsoft/TypeScript#62184](https://github.com/microsoft/TypeScript/pull/62184) (Open, `For Backlog Bug`)

**Fixed more ghost errors after LSP requests caching wrong contextual and parameter types**

*Ignore cached types and signatures on specific syntax nodes to prevent erroneous ghost errors after LSP requests*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/pull/62184#issuecomment-3193765315) **typescript-bot** reported build start and results
 * [15 weeks ago](https://github.com/microsoft/TypeScript/pull/62184#issuecomment-3193767506) **typescript-bot** provided an installable tgz and instructions for testing via package.json, plus links to a playground and npm module
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62184#issuecomment-3609353025) **jakebailey** expressed uncertainty about porting the save and restore mechanism due to SymbolLinks being split into multiple maps in the new codebase

### [Issue microsoft/TypeScript#62196](https://github.com/microsoft/TypeScript/issues/62196) (Open, `Suggestion`, `Breaking Change`, `Committed`, **iisaduan**)

**Deprecate \`\-\-target es5\`, make lowest target \`es2015\`**

*Deprecate --target es5 in TypeScript 6.0, raise the minimum target to ES2015, and update library inclusion and downlevel iteration handling.*

 * [today](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3606991662) **guilhermesimoes** provided examples of ES5-only devices and explained concern about dropping `--target es5`
 * [today](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3607212640) **jakebailey** said "Why can't you run your output through babel to lower to ES5?"
 * [today](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3607357654) **snarbles2** suggested using an older version of TypeScript and noted ES5 support might not be maintained
 * [today](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3608162705) **RyanCavanaugh** said "The statement being responded to there was "we'll have to forego all the goodies and improvements of TypeScript 7.0", which implies an inability to use an alternative downleveler."
 * [today](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3608321650) **snarbles2** clarified that the sentiment was about TypeScript 7's suitability rather than ignorance of Babel, and acknowledged Babel exists and ES5 support has some non-zero value
 * [today](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3608339216) **RyanCavanaugh** said "Probably! But if there's an actual technical blocker that we hadn't thought of, we would want to know about it."
 * [today](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3608761605) **guilhermesimoes** argued that avoiding alternative downlevelers was a preference rather than inability, explained the need to explore esbuild and swc given the deprecation of ES5 transpilation, cautioned against assuming all environments are evergreen, and supported the point with data on legacy browser usage

### [Issue microsoft/TypeScript#62737](https://github.com/microsoft/TypeScript/issues/62737) (Open, `Suggestion`, `Help Wanted`, `Experimentation Needed`)

**Show incompatible union members in discriminated union discriminator errors**

*Enhance TypeScript's discriminated union error messages to identify which union members in the discriminator cause assignment failures.*

 * (3 weeks ago) **RyanCavanaugh** added label `Help Wanted`, and set milestone to `Backlog`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62737#issuecomment-3597562402) **alpha2420** said "Hi @jankeape, I’d like to start working on this issue. Please let me know if there are any guidelines or initial steps I should follow."
 * [later](https://github.com/microsoft/TypeScript/issues/62737#issuecomment-3611083699) **janpaepke** suggested following the contributing guidelines, referenced a prior discussion and playground link, and offered to provide further context or testing

### [PR microsoft/TypeScript#62790](https://github.com/microsoft/TypeScript/pull/62790) (Open, `For Backlog Bug`)

**Fix compiler crash on generics overload resolution failure**

*Generate appropriate diagnostics instead of invoking Debug.fail to avoid compiler crashes when generic overload resolution fails.*

 * **typescript-bot** added label `For Backlog Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3561575931) **moznion** said "@microsoft-github-policy-service agree"
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3599611006) **jakebailey** said "I think this is just papering over a bug somewhere else. IIRC the intent of these debug fails are to assert that the previous steps added an error."
 * [today](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3610467030) **moznion** thanked jakebailey, asked whether the core issue was in type inference or elsewhere, and noted that the crash during type checking blocked upgrading from v5.6.3, suggesting it first appeared in v5.7
 * [today](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3610487746) **jakebailey** said "If it's a regression, I would consider bisecting with https://www.npmjs.com/package/every-ts"
 * [later](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3611415516) **moznion** said "I don't think this is a regression. It appears that the problem still occurs on the latest main branch."
 * [later](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3612713782) **jakebailey** said "But you said it wasn't broken in 5.5, so there is a commit in between where this broke."
 * [later](https://github.com/microsoft/TypeScript/pull/62790#issuecomment-3612719094) **jakebailey** said "But, https://github.com/microsoft/TypeScript/issues/61524#issuecomment-2780342066 seems to imply there's already a PR for this?"

### [Issue microsoft/TypeScript#62814](https://github.com/microsoft/TypeScript/issues/62814) (Closed, `Working as Intended`)

**Inference mismatch in strict and non\-strict mode**

*TypeScript strict mode erroneously changes boolean literal inference, causing compilation errors absent in non-strict mode.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3589290382) **MartinJohns** referenced the TypeScript handbook sections on strict null checks and truthiness narrowing
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3598074176) **RyanCavanaugh** provided an automatically generated list of similar issues with relevance percentages
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/62814#issuecomment-3609567108) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62816](https://github.com/microsoft/TypeScript/issues/62816) (Closed, `Question`)

**\`tsc\` transpile js to js converts Set iteration loops to invalid numeric key indexing**

*Transpiling JavaScript with tsc’s allowJs option converts Set for-of loops into invalid .length-based index loops.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3596641898) **nmain** suggested using the downlevelIteration option and explained that ES6 features like Set and iterators can't be polyfilled properly
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3598074292) **RyanCavanaugh** provided automated analysis linking to similar issues
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3609567360) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62819](https://github.com/microsoft/TypeScript/issues/62819) (Closed, `Duplicate`)

**invalid behavior of \`satisfies\`**

*TypeScript’s satisfies operator fails to flag extra spread properties from a const union object while direct object literals error*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62819#issuecomment-3596691093) **MartinJohns** said "Duplicate of #39998."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62819#issuecomment-3598074343) **RyanCavanaugh** provided an automated analysis of how 'satisfies' handles excess properties with object literals and spread expressions and linked to relevant FAQs
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62819#issuecomment-3609566790) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62820](https://github.com/microsoft/TypeScript/issues/62820) (Closed, `Suggestion`, `Out of Scope`)

**@Concurrent decorator**

*Add a @Concurrent decorator to iterate loops concurrently with optional batching and Promise.all or Promise.allSettled logic.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3597843019) **MartinJohns** said "This is explicitly out of scope for TypeScript."
 * (2 days ago) **RyanCavanaugh** added labels `Suggestion`, `Out of Scope`
 * [today](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3609567547) **typescript-bot** said "This issue has been marked as "Out of Scope" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62824](https://github.com/microsoft/TypeScript/issues/62824) (Open, `Bug`, `Help Wanted`, `Domain: check: Type Inference`)

**\`silentNeverType\` leak through return type inference**

*Return type inference in nested reverse-mapped types leaks the silent never type.*

 * created by **Andarist**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`
 * [today](https://github.com/microsoft/TypeScript/issues/62824#issuecomment-3608123470) **RyanCavanaugh** said "Is there a simpler test a mere mortal like me can understand?"
 * [today](https://github.com/microsoft/TypeScript/issues/62824#issuecomment-3608448101) **Andarist** provided a shorter repro and a minimal example illustrating how `silentNeverType` escapes through mapped types
 * **RyanCavanaugh** added to milestone `Backlog`

### [PR microsoft/TypeScript#62825](https://github.com/microsoft/TypeScript/pull/62825) (Open, `For Backlog Bug`)

**Fixed \`silentNeverType\` leak by propagating it through \`getIndexType\`**

*Propagate silentNeverType through getIndexType to prevent unintended type leakage.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#62827](https://github.com/microsoft/TypeScript/issues/62827) (Open, `Discussion`)

**Closing TS 6\.0 LS issues**

*All TypeScript 6.0 language service issues are being closed due to a full LSP-based rewrite targeting the native 7.0 codebase.*

 * [today](https://github.com/microsoft/TypeScript/issues/62827#issuecomment-3606935848) **mkantor** clarified that issues are only closed, not erased, and joked about closing issues with exes
 * [today](https://github.com/microsoft/TypeScript/issues/62827#issuecomment-3607017419) **rubiesonthesky** noted that closed issues labeled for the Language Server were mostly minor, and suggested prioritizing pressing issues and the Go port due to limited resources and many open issues
 * [today](https://github.com/microsoft/TypeScript/issues/62827#issuecomment-3607091540) **mkantor** suggested updating the issue templates to call out that new issues of this nature should not be filed in this repository
 * [today](https://github.com/microsoft/TypeScript/issues/62827#issuecomment-3608056507) **RyanCavanaugh** clarified that manually converting 500 issues into unit tests would be inefficient and that team resources are better spent elsewhere

### [Issue microsoft/TypeScript#62829](https://github.com/microsoft/TypeScript/issues/62829) (Open, `Needs Investigation`, **andrewbranch**)

**How to trace/debug auto import suggestions?**

*Enable tsserver debug logging to diagnose why auto-import suggestions are missing for an ESM package*

 * created by **jedwards1211**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3605000333) **RyanCavanaugh** pointed out limited logging in AutoImportProviderProject and asked if the 'Include package json auto imports' option was enabled
 * **RyanCavanaugh** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3608828162) **jedwards1211** thanked for the tip, described having more than 10 entry points for utilities, reported that enabling 'Include package json auto imports' had no effect, noted the same issue with es-toolkit, referenced MUI's guidance to avoid barrel imports, and suggested limiting suggestions based on package size rather than entry point count
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3608950076) **RyanCavanaugh** offered that they were rewriting auto-imports in TS7 with smarter bail-out heuristics and asked the user to publish their package or include it in tsgo for investigation
 * [today](https://github.com/microsoft/TypeScript/issues/62829#issuecomment-3610454675) **jedwards1211** shared a link to their npm package, described including CJS, ESM, source, declaration maps, and original source files, questioned if that trips tsserver, and mentioned needing to try tsgo

### [Issue microsoft/TypeScript#62830](https://github.com/microsoft/TypeScript/issues/62830) (Closed)

**Typings of Object\.groupBy are incorrect**

*The TypeScript definitions for Object.groupBy incorrectly type the returned object’s keys as numbers instead of strings*

 * [today](https://github.com/microsoft/TypeScript/issues/62830#issuecomment-3607463322) **a-student** thanked jcalz and mkantor for their comments and explanations and noted difficulty finding exact types while investigating the original problem
 * (today) **a-student** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62830#issuecomment-3607531472) **jcalz** suggested searching for `Object.keys` to find exact types
 * [today](https://github.com/microsoft/TypeScript/issues/62830#issuecomment-3607658990) **a-student** said "Initially i thought the problem was in the Object.groupBy typing. ("

### [Issue microsoft/TypeScript#62831](https://github.com/microsoft/TypeScript/issues/62831) (Closed, `Duplicate`)

**Overriding fields of a generic object using spread operator results in incorrect types**

*Using spread to override generic object properties yields incorrect intersection types instead of properly omitting and replacing original fields.*

 * [today](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3607272708) **jcalz** identified that the issue is a duplicate of #50185, #42690, and #10727 and explained the context for tracking the request
 * [today](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3607333043) **wnadurski** added context about real-world type safety risk, referenced issue #10727, and suggested fixing via the Omit type
 * [today](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3607527647) **jcalz** demonstrated how to implement object spread using Omit and a custom helper, providing example TypeScript code and a playground link
 * **RyanCavanaugh** added label `Duplicate`
 * [later](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3612714470) **wnadurski** asked to keep the issue open for clearer reference and communication of the bug until it’s fixed
 * [later](https://github.com/microsoft/TypeScript/issues/62831#issuecomment-3612864462) **jcalz** said "#42690 is open 🤷‍♂️"

### [PR microsoft/TypeScript#62832](https://github.com/microsoft/TypeScript/pull/62832) (Closed, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20251203202848732 to main**

*Pull request merging localized LCLS changes from lego/hb_5378966c-b857-470a-8675-daebef4a6da1_20251203202848732 into main.*

 * created by **csigs**
 * **typescript-bot** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#62833](https://github.com/microsoft/TypeScript/pull/62833) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Update security\.md**

*Update security.md to match Microsoft’s standard SECURITY.md template as requested by the security team.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62834](https://github.com/microsoft/TypeScript/pull/62834) (Closed, `For Uncommitted Bug`)

**Rename mock and require file references**

*Automatically update jest.mock, vitest.mock, require, and import file references when files are renamed*

 * created by **hjonasson**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3609308691) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3609308696) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3609308990) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [today](https://github.com/microsoft/TypeScript/pull/62834#issuecomment-3609364793) **hjonasson** quoted the Contributor License Agreement instructions and full agreement text

### [Issue microsoft/TypeScript#62835](https://github.com/microsoft/TypeScript/issues/62835) (Open, `Suggestion`, `Awaiting More Feedback`)

**Update test framework mock paths during file rename operations**

*Automatically update string literal paths in jest.mock and vitest.mock during TypeScript file rename or move to avoid broken tests.*

 * created by **hjonasson**
 * [today](https://github.com/microsoft/TypeScript/issues/62835#issuecomment-3610365760) **MartinJohns** questioned how the compiler would distinguish paths from strings and noted it would require a change like #42054 or specific test frameworks
 * [later](https://github.com/microsoft/TypeScript/issues/62835#issuecomment-3612334286) **jcalz** asked if 'hardcore' was a typo for 'hardcode'

### [PR microsoft/TypeScript#62836](https://github.com/microsoft/TypeScript/pull/62836) (Open, `For Backlog Bug`)

**Fix spread operator failing to distribute over union when type is inlined**

*Inline union types in true branches of conditional types were incorrectly narrowed, causing spread operator cross-product to miss union combinations.*

 * created by **thromel**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62836#issuecomment-3611315539) **thromel** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#62837](https://github.com/microsoft/TypeScript/pull/62837) (Open, `For Backlog Bug`)

**Improve error messages for discriminated union incompatible members**

*Enhance discriminated union assignment errors to report specific incompatible source types and include the discriminator property name.*

 * created by **alpha2420**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62837#issuecomment-3612436416) **microsoft-github-policy-service[bot]** requested that the contributor agree to the Contributor License Agreement and reply with the specified template

### [Issue microsoft/TypeScript#62838](https://github.com/microsoft/TypeScript/issues/62838) (Closed, `Duplicate`)

**\`JSON\.stringify\(undefined\)\` incorrectly types the return value as \`string\`**

*JSON.stringify(undefined) is typed as returning string in TypeScript instead of undefined.*

 * created by **afgomez**
 * [later](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3612849310) **MartinJohns** said "Duplicate of #18879."
 * [later](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3612897786) **afgomez** said "Oh! sorry for the noise. I only searched for JSON.stringify() in the open issues and I didn't find anything 😅."
 * [later](https://github.com/microsoft/TypeScript/issues/62838#issuecomment-3612938075) **MartinJohns** said "Searching with parentheses won't yield any result either way. Best results are with an added search modifier: JSON.stringify in:title"

### [PR microsoft/TypeScript#62839](https://github.com/microsoft/TypeScript/pull/62839) (Closed, `For Backlog Bug`)

**Fix reverse mapped contextual this inference leak**

*Skip reverse-mapped apparent types when computing contextual “this” to fix inference leaks and add a regression test for reverseMappedTypeParameterLeak.*

 * created by **learn-dumboo24**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62839#issuecomment-3612953132) **learn-dumboo24** said "@microsoft-github-policy-service agree"

