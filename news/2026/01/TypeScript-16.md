# Report for 2026-01-16 (Friday, January 16th, 2026)

14 different users commented on 31 different issues.

## Recommended Actions

 * Response Recommended
    * @nh2 asked what closed the issue as completed in [microsoft/TypeScript#46420](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-3763469195)

## Activity Summary

### [Issue microsoft/TypeScript#46420](https://github.com/microsoft/TypeScript/issues/46420) (Closed, `Needs More Info`, `Needs Investigation`, `Domain: Performance`)

**Slow performance in incremental mode with no changes**

*TypeScript's incremental mode still re-parses every file on unchanged runs, causing slow type-check performance in large projects.*

 * [4.1 years ago](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-978209865) **samuliasmala** described experiencing the same issue with the incremental flag and provided reproduction steps and timing measurements
 * (1.4 years ago) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-3760229956) **nh2** said "@RyanCavanaugh Was this solved? What was the fix?"
 * [today](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-3761384747) **DanielRosenwasser** recommended trying early previews of TypeScript 7 and provided install instructions
 * [later](https://github.com/microsoft/TypeScript/issues/46420#issuecomment-3763469195) **nh2** said "Thanks, I'm aware of that; that's not what I asked though. I asked what closed this as completed, as I'm looking into bugs related to incremental mode (which I believe tsgo also does have)."

### [PR microsoft/TypeScript#48889](https://github.com/microsoft/TypeScript/pull/48889) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**\[Experiment\] Handle package\.json watch in tsc \-\-build**

*tsc --build --watch now monitors package.json files adjacent to tsconfig or referenced projects to ensure correct incremental builds.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/48889#issuecomment-1152985072) **craigphicks** asked whether changes to package.json would trigger rebuilds like source files, whether additional validations are needed beyond that, and requested clarification of the package.json behavior table under tsc -b -w
 * [3.5 years ago](https://github.com/microsoft/TypeScript/pull/48889#issuecomment-1152986422) **craigphicks** questioned the design of timestamp checking and watching under tsc -b for non-composite root projects and asked if the identified hole under specific conditions is correct and justified
 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/48889#issuecomment-2773187303) **sandersn** said "@sheetalkamat this PR has 3 years since the last comments. Is it worth reviving?"
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript#53086](https://github.com/microsoft/TypeScript/pull/53086) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**\[WIP\] Allow adding arbitrary extension files to program without d\.ts files being on the disk**

*Enable adding arbitrary extension files into TypeScript programs without on-disk declaration files using host APIs.*

 * (2.8 years ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`
 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/53086#issuecomment-2773744842) **sandersn** said "@sheetalkamat this experiment is 2 years old now. Is it worth keeping? Can I close it?"
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript#55835](https://github.com/microsoft/TypeScript/pull/55835) (Closed, **sheetalkamat**)

**\[wip\] Experiment with module resolution cache be the only one to store resolutions**

*Propose experimenting with using the module resolution cache as the exclusive store for resolution data.*

 * created by **sheetalkamat**
 * [2.3 years ago](https://github.com/microsoft/TypeScript/pull/55835#issuecomment-1732116938) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * (today) **sheetalkamat** closed the issue
 * **typescript-bot** assigned to **sheetalkamat**

### [PR microsoft/TypeScript#55968](https://github.com/microsoft/TypeScript/pull/55968) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**\[wip\] Shared resolutions in tsserver **

*Work in progress pull request reworks shared resolution logic in tsserver with ongoing testing.*

 * (1.5 years ago) **jakebailey** reopened the issue
 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/55968#issuecomment-2339557143) **yuhuung** said "Is this still planned to be merged? @sheetalkamat "
 * [1.3 years ago](https://github.com/microsoft/TypeScript/pull/55968#issuecomment-2341513127) **sheetalkamat** said "This is still work in progress and being worked on."
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript#56074](https://github.com/microsoft/TypeScript/pull/56074) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**\[wip\] Type acquisition and module resolution updates**

*Work-in-progress pull request updating type acquisition and module resolution awaiting test execution.*

 * (2.2 years ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`
 * [2.2 years ago](https://github.com/microsoft/TypeScript/pull/56074#issuecomment-1758654641) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript#56679](https://github.com/microsoft/TypeScript/pull/56679) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**Experiment using caches to answer readFile, fileExists**

*Experiment using caching mechanisms to optimize responses for readFile and fileExists operations.*

 * [2.1 years ago](https://github.com/microsoft/TypeScript/pull/56679#issuecomment-1841593286) **typescript-bot** started the regular perf test suite on the PR and provided monitoring and results links
 * [2.1 years ago](https://github.com/microsoft/TypeScript/pull/56679#issuecomment-1841618202) **typescript-bot** provided the requested performance run results with a detailed comparison report
 * [41 weeks ago](https://github.com/microsoft/TypeScript/pull/56679#issuecomment-2770686221) **sandersn** said "@sheetalkamat this experiment is over a year old. Is it OK to close it?"
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript#57942](https://github.com/microsoft/TypeScript/pull/57942) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**\[draft\] Change to run tsserver under incremental verification**

*Change tsserver to run under an incremental verification process.*

 * (1.8 years ago) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **sheetalkamat**
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript#61732](https://github.com/microsoft/TypeScript/pull/61732) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**\[WIP\] Resolution sharing**

*Add resolution sharing capability to support buddy builds creation under issue #55968.*

 * [34 weeks ago](https://github.com/microsoft/TypeScript/pull/61732#issuecomment-2892207259) **typescript-bot** updated build status for `pack this` command
 * [34 weeks ago](https://github.com/microsoft/TypeScript/pull/61732#issuecomment-2892207478) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [34 weeks ago](https://github.com/microsoft/TypeScript/pull/61732#issuecomment-2892214909) **typescript-bot** provided an installable tgz package link and testing instructions, along with playground and npm module links
 * (today) **sheetalkamat** closed the issue
 * (today) **sheetalkamat** reopened the issue
 * (today) **sheetalkamat** closed the issue

### [PR microsoft/TypeScript#62138](https://github.com/microsoft/TypeScript/pull/62138) (Open, `For Backlog Bug`)

**Add types for \`RegExp\.escape\`**

*Add missing TypeScript type definitions for the proposed RegExp.escape method in library files.*

 * [23 weeks ago](https://github.com/microsoft/TypeScript/pull/62138#issuecomment-3146650995) **i-ayushh18** announced completion of types for `RegExp.escape` in PR #62138 by the AI Assistant
 * [23 weeks ago](https://github.com/microsoft/TypeScript/pull/62138#issuecomment-3146687980) **i-ayushh18** announced completion of types for `RegExp.escape` in PR #62138 by the AI Assistant
 * [13 weeks ago](https://github.com/microsoft/TypeScript/pull/62138#issuecomment-3397206018) **jakebailey** said "This PR has a bunch of conflicts at this point; I'm pretty sure we could get this changed in if fixed"
 * [later](https://github.com/microsoft/TypeScript/pull/62138#issuecomment-3762937312) **fgiering** said "One day.... Maybe... "

### [PR microsoft/TypeScript#62460](https://github.com/microsoft/TypeScript/pull/62460) (Closed, `Author: Team`, `For Uncommitted Bug`, **sheetalkamat**)

**add some errors for diagnosing repos with issues**

*Add error logging for diagnosing repos with issues to gather more data for issue #62418.*

 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/62460#issuecomment-3310102252) **typescript-bot** reported user test results with one infrastructure failure and that everything else looked good
 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/62460#issuecomment-3310106634) **typescript-bot** reported that tSC runs on the top 400 repos comparing main and the pull request merge looked good
 * [17 weeks ago](https://github.com/microsoft/TypeScript/pull/62460#issuecomment-3310184705) **typescript-bot** reported that tSC runs on the top 400 repos comparing main and the pull request merge looked good
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript#62985](https://github.com/microsoft/TypeScript/issues/62985) (Closed, `Not a Defect`)

**Cannot extract base type from branded intersection**

*Request for a TypeScript mechanism to remove a branded intersection from a type and recover its base type.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3750926737) **RyanCavanaugh** explained that reverse inference from an intersection is not well-defined in a structural type system and provided an alternative implementation using Omit2 and StripThrows with code examples
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3750977452) **jcalz** noted similarity to issues #54213 and #57918 and suggested filing a feature request for branded-primitive support in Omit instead of treating it as a bug
 * [today](https://github.com/microsoft/TypeScript/issues/62985#issuecomment-3762468460) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62986](https://github.com/microsoft/TypeScript/issues/62986) (Closed, `Duplicate`)

**Only the last overload of a function is considered while inferring**

*Inference for overloaded functions only uses the last signature when inferring return or parameter types instead of uniting all overloads*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3750434692) **MartinJohns** explained that the issue was long-known, stemmed from overload resolution, required new syntax, and noted that a solution was unlikely soon
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3750878939) **jcalz** said "duplicate of #29732, #56430, #56829, and others."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/62986#issuecomment-3762468416) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62989](https://github.com/microsoft/TypeScript/pull/62989) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Prepare tests for \`\-\-noImplicitAny\`**

*A script prepends // @strict: false to tests whose error outputs changed when enabling default --noImplicitAny.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62989#issuecomment-3753134272) **DanielRosenwasser** said "This history is already a nightmare..."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62989#issuecomment-3756883789) **jakebailey** said "On one hand, I feel bad locking so many tests into a mode we basically don't want anyone using, but on the other, that is what they were testing before, so, there's not much difference...."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62989#issuecomment-3757078321) **DanielRosenwasser** described wanting to annotate error baselines to explain why they’re off and noted that forward migration might not happen
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#62991](https://github.com/microsoft/TypeScript/issues/62991) (Open, `Bug`, `Domain: Parser`)

**Not currectly parse superClass starts with \`{}\`**

*Expressions beginning with {} such as {}.Foo and {}! are not correctly parsed as class superclasses.*

 * created by **fisker**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62991#issuecomment-3758129886) **MartinJohns** said "Is this real and useful code or just code trying to break the compiler?"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62991#issuecomment-3758248210) **fisker** stated that the code was not real or useful and noted it was found in the Prettier test suite
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#62992](https://github.com/microsoft/TypeScript/issues/62992) (Open, `Suggestion`, `Awaiting More Feedback`)

**generics in constructor**

*Add support for generic type parameters on class constructors to enforce parameter type constraints.*

 * created by **y-nk**
 * [today](https://github.com/microsoft/TypeScript/issues/62992#issuecomment-3760042724) **jcalz** inquired about the type of instances of a class with a generic constructor parameter and questioned if the issue duplicated earlier tickets
 * [today](https://github.com/microsoft/TypeScript/issues/62992#issuecomment-3761040803) **RyanCavanaugh** acknowledged a use case for constructors with additional type parameters and noted its inconsistent support across OOP languages
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/62992#issuecomment-3761207773) **jcalz** clarified that the motivating use case involved writing a generic constructor parameter property and that the provided example resembled duplicate issue #40451 and wouldn’t work even if the proposed feature existed
 * [today](https://github.com/microsoft/TypeScript/issues/62992#issuecomment-3762190348) **RyanCavanaugh** admitted not paying close attention to the long type variable names in the example, noted that type parameters cannot perform a lexical escape even indirectly, and mentioned that issue #40451 is more complex because it tries to involve `this`

### [Issue microsoft/TypeScript#62993](https://github.com/microsoft/TypeScript/issues/62993) (Open, `Bug`, `Help Wanted`, `Fix Available`, `Domain: Crashes`, **RyanCavanaugh**, **Copilot**)

**Crash: RangeError: Maximum call stack size exceeded in addTypesToUnion when using incomplete keyof type annotation on object destructuring**

*Compiler crashes with a RangeError in addTypesToUnion when destructuring an object with an incomplete keyof annotation under strict mode*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/62993#issuecomment-3759331169) **Andarist** provided a shorter repro snippet
 * [today](https://github.com/microsoft/TypeScript/issues/62993#issuecomment-3761056551) **RyanCavanaugh** provided another code example that reproduced the issue in TS7
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Fix Available`, `Fix Available`

### [Issue microsoft/TypeScript#62994](https://github.com/microsoft/TypeScript/issues/62994) (Closed, `Duplicate`)

**Typescript Playground Set interval Bug**

*Repeatedly executing setInterval code in the TypeScript Playground fails to clear previous intervals unless the page is reloaded*

 * created by **IamStaple**
 * [today](https://github.com/microsoft/TypeScript/issues/62994#issuecomment-3760010266) **MartinJohns** suggested using the TypeScript-Website repo and explained that the playground is intended only for quick snippets rather than a fresh environment
 * [today](https://github.com/microsoft/TypeScript/issues/62994#issuecomment-3760349874) **MartinJohns** said "Duplicate of https://github.com/microsoft/TypeScript-Website/issues/2541."
 * **RyanCavanaugh** added label `Duplicate`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62995](https://github.com/microsoft/TypeScript/issues/62995) (Closed, `Fixed`)

**Bug with type argument inference if it has default value \`= undefined\` and actual value is object with non\-arrow function**

*TypeScript incorrectly infers generic type arguments defaulting to undefined when given an inline object with non-arrow functions.*

 * [today](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760618285) **MartinJohns** said "Likely a duplicate of #47599."
 * [today](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760689845) **termi** explained that their example uses three generic parameters to demonstrate the necessity of the D=undefined default and contrasted it with a simpler case where the default can be removed
 * [today](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760706496) **termi** clarified that the issue was related to #47599 but not a duplicate and noted that adding '=undefined' in a generic parameter caused a problem
 * [today](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3760910569) **Andarist** said "This is already fixed by https://github.com/microsoft/TypeScript/pull/62243 . You can try out nightly build."
 * **RyanCavanaugh** added label `Fixed`
 * [today](https://github.com/microsoft/TypeScript/issues/62995#issuecomment-3761049019) **RyanCavanaugh** said "Confirmed in nightly playground"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62996](https://github.com/microsoft/TypeScript/pull/62996) (Closed, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Fix crash on incomplete type operators \(keyof/readonly/unique\)**

*Add parser validation to report TS1110 and use an any placeholder to avoid stack overflows when type operators lack operands.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-bot** added labels `For Milestone Bug`, `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62996#issuecomment-3761269051) **RyanCavanaugh** demonstrated that using 'const x: keyof = { a: 1 }' does not crash
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62997](https://github.com/microsoft/TypeScript/pull/62997) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Prevent contextual typing recursion in destructuring initializers**

*Track active binding patterns during contextual typing of union-typed destructuring initializers to prevent infinite recursion and stack overflows.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/62997#issuecomment-3761722647) **Copilot** added both cases to the regression test file

### [PR microsoft/TypeScript#62998](https://github.com/microsoft/TypeScript/pull/62998) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**\[WIP\] Fix stack overflow in type checking code**

*Add a guard in type checking to prevent stack overflow from circular dependency when resolving object literal initializers*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62999](https://github.com/microsoft/TypeScript/pull/62999) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix stack overflow when checking circular binding element references**

*Use quick or cached types to avoid stack overflows when destructuring patterns reference their own bindings under strictNullChecks.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * **typescript-bot** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63000](https://github.com/microsoft/TypeScript/issues/63000) (Closed, `AI Spam`)

**Template Variable Extraction/Replacement Inconsistency**

*Template variable extraction trims whitespace-only names but replacement fails due to mismatched placeholders.*

 * created by **jammievae**
 * [today](https://github.com/microsoft/TypeScript/issues/63000#issuecomment-3761706702) **MartinJohns** said "AI slop."
 * [today](https://github.com/microsoft/TypeScript/issues/63000#issuecomment-3762070161) **RyanCavanaugh** said "I'm very surprised to learn we have Dart code in this repo."
 * (today) **RyanCavanaugh** closed the issue
 * **RyanCavanaugh** added label `AI Spam`

### [Issue microsoft/TypeScript#63001](https://github.com/microsoft/TypeScript/issues/63001) (Open, `Needs Investigation`, **DanielRosenwasser**)

**Global 'this' capture logic is slightly wrong in \`\-\-noImplicitThis\`**

*Arrow functions within functions typed with globalThis incorrectly trigger a --noImplicitThis global this capture error.*

 * created by **DanielRosenwasser**

### [Issue microsoft/TypeScript#63002](https://github.com/microsoft/TypeScript/issues/63002) (Open, `Suggestion`, `Too Complex`)

**create primitive to prevent one folder from importing from another**

*Add a tsconfig.json setting to prevent imports between designated folders.*

 * created by **ORESoftware**
 * [today](https://github.com/microsoft/TypeScript/issues/63002#issuecomment-3762617606) **MartinJohns** said "https://eslint.org/docs/latest/rules/no-restricted-imports"

### [Issue microsoft/TypeScript#63003](https://github.com/microsoft/TypeScript/issues/63003) (Closed, `Bug`, `Domain: lib.d.ts`)

**\[Typo\] Possible typo in JSDoc string for \`Math\.trunc\(…\)\` function \(lib\.es2015\.core\.d\.ts\)**

*The JSDoc comment for Math.trunc in lib.es2015.core.d.ts contains a typo with an extra 'the' before 'a numeric expression'.*

 * created by **MichaelZalla**

### [Issue microsoft/TypeScript#63004](https://github.com/microsoft/TypeScript/issues/63004) (Open, `Bug`)

**Explicit \`never\` return type in \`catch\` block & condition in \`finally\` marks the whole \`finally\` block as unreachable**

*TypeScript incorrectly flags a conditional finally block as unreachable when a catch handler calls a function declared to return never.*

 * created by **d-fischer**

### [Issue microsoft/TypeScript#63005](https://github.com/microsoft/TypeScript/issues/63005) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash： when inferring from a tuple with middle rest elements and trailing variadic elements**

*TS compiler crashes when inferring a tuple with both middle rest and trailing variadic elements.*

 * created by **na7ure-a**

