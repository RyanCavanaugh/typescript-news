# Report for 2026-01-22 (Thursday, January 22nd, 2026)

18 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @KnorpelSenf asked whether regressions from 4.7 to 4.8 and imported TS codebase bugs would be addressed after the 7.0 release in [microsoft/TypeScript#62963](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3787149661)
    * @jsejcksn asked for a more idiomatic alternative to custom guard functions or invoking Symbol.hasInstance in [microsoft/TypeScript#63032](https://github.com/microsoft/TypeScript/issues/63032#issuecomment-3786580368)
    * @ericnorris asked if the fourslash test issue should be filed in the typescript-go repository in [microsoft/TypeScript#63033](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3787420587)
    * @dev-gabriel-henrique asked whether the issue should be considered a React or TypeScript issue in [microsoft/TypeScript#63042](https://github.com/microsoft/TypeScript/issues/63042#issuecomment-3790329669)
    * @dev-gabriel-henrique asked if there was a way to avoid a false positive without explicitly declaring (prevState): State => State in [microsoft/TypeScript#63042](https://github.com/microsoft/TypeScript/issues/63042#issuecomment-3790442598)

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [today](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3785027582) **adrian-gierakowski** praised the "I Mean It" Operator
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3789098645) **isc30** suggested an alternative implementation for the Exact util type

### [Issue microsoft/TypeScript#17002](https://github.com/microsoft/TypeScript/issues/17002) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`, `Fix Available`)

**Array\.isArray type narrows to any\[\] for ReadonlyArray\<T\>**

*Array.isArray fails to correctly narrow a union including ReadonlyArray<T>, resulting in an any[] type instead of ReadonlyArray<T>.*

 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-2782169204) **A-EbrahimRSA** thanked the commenter, noted they'd seen the workaround, and expressed preference for using the built-in .isArray method
 * [41 weeks ago](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-2787918238) **oconnorjoseph** said "Our team just ran into this issue with the readonly keyword as well. We would very much appreciate for this to work natively."
 * [today](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3784982171) **spalt08** offered another workaround using Array.isArray to define a readonly array type guard
 * [today](https://github.com/microsoft/TypeScript/issues/17002#issuecomment-3786996167) **cahnory** provided an alternative workaround using a type assertion for Array.isArray

### [Issue microsoft/TypeScript#40562](https://github.com/microsoft/TypeScript/issues/40562) (Open, `Suggestion`, `Awaiting More Feedback`)

**Non‑\`void\` returning assertion functions**

*Enable TypeScript to define assertion functions with non-void generic return types, as needed for Jest matchers and similar APIs.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/40562#issuecomment-2098979427) **irwincollin** expressed desire for a feature to enable compile-time safe mutable patterns, illustrated with a state machine example
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/40562#issuecomment-2155567926) **ITenthusiasm** agreed that a 'mutates' keyword to indicate in-place array mutation would be useful, described performance drawbacks of Array.map creating new arrays, and proposed example syntax
 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/40562#issuecomment-2155579956) **ITenthusiasm** noted that this issue could relate to #17181 and suggested that a library identifying mutating functions could meet some of its requirements
 * [today](https://github.com/microsoft/TypeScript/issues/40562#issuecomment-3786993840) **mkantor** said "This is also related to #22865."

### [Issue microsoft/TypeScript#50762](https://github.com/microsoft/TypeScript/issues/50762) (Closed, `Bug`, `Won't Fix`, `Breaking Change`, `Domain: Node ESM`, **andrewbranch**)

**package\.json \`exports\` resolution uses fallback conditions, unlike Node**

*In `--moduleResolution nodenext`, TypeScript’s exports resolution incorrectly falls back to other conditions after matching an import target, diverging from Node.js behavior.*

 * **typescript-bot** added label `Fix Available`
 * **andrewbranch** assigned to **andrewbranch**
 * **RyanCavanaugh** added label `Domain: Node ESM`
 * (today) **andrewbranch** added label `Won't Fix`, removed labels `Committed`, `Fix Available`, and removed from milestone `TypeScript 6.0.0`
 * [today](https://github.com/microsoft/TypeScript/issues/50762#issuecomment-3786028671) **andrewbranch** said "After a lot of trying, https://github.com/microsoft/TypeScript/pull/62483 was all we could do on this without breaking things more than it was worth it."
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#62241](https://github.com/microsoft/TypeScript/issues/62241) (Closed, `Bug`, `Domain: ES Modules`, `Fix Available`, **andrewbranch**, **Copilot**)

**Referenced project options not consulted to determine \.d\.ts format for synthetic default export eligibility**

*TypeScript allows default imports from modules without default exports under bundler resolution when synthetic default imports are disabled.*

 * **andrewbranch** added to milestone `TypeScript 6.0.0`
 * **typescript-bot** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: ES Modules`
 * (today) **andrewbranch** removed label `Fix Available`, and assigned to **Copilot**
 * **typescript-bot** added label `Fix Available`

### [Issue microsoft/TypeScript#62963](https://github.com/microsoft/TypeScript/issues/62963) (Open, `Meta-Issue`)

**Transition to 6\.0 Maintenance Mode**

*TypeScript 6.0 is entering maintenance mode with only critical fixes, deprecations, and compatibility changes accepted to accelerate the transition to the Go-based 7.0 release.*

 * **RyanCavanaugh** added label `Meta-Issue`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3723323514) **puppy0cam** said "If we amended our PRs to take out code changes but keep the test(s) created, would such a PR be accepted?"
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3724470262) **RyanCavanaugh** replied that test-only PRs would be accepted after 7.0 but currently no due to large ongoing PRs causing merge conflicts
 * [today](https://github.com/microsoft/TypeScript/issues/62963#issuecomment-3787149661) **KnorpelSenf** asked whether regressions from 4.7 to 4.8 and imported bugs would be fixed after the 7.0 release

### [Issue microsoft/TypeScript#63002](https://github.com/microsoft/TypeScript/issues/63002) (Closed, `Suggestion`, `Too Complex`)

**create primitive to prevent one folder from importing from another**

*Add a tsconfig.json setting to prevent imports between designated folders.*

 * (2 days ago) **RyanCavanaugh** added labels `Suggestion`, `Too Complex`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63002#issuecomment-3774164380) **RyanCavanaugh** argued that the lint rule's documentation was too long and its benefit unclear given most projects already use a linter
 * [today](https://github.com/microsoft/TypeScript/issues/63002#issuecomment-3787705333) **typescript-bot** said "This issue has been marked as "Too Complex" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63007](https://github.com/microsoft/TypeScript/issues/63007) (Closed, `Duplicate`)

**"Conditionally optional" type works for concrete parameter but not generic**

*Conditional optional types work for concrete types but not when used with generics in TypeScript.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63007#issuecomment-3764420109) **MartinJohns** explained that resolution of conditional types involving unbound generic types is deferred and marked the issue as a duplicate of #52144
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63007#issuecomment-3774685749) **RyanCavanaugh** said "🤖 This is an automated response. I looked for things that might help (duplicates, FAQ entries, etc) but didn't find anything. A human will take a look!"
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63007#issuecomment-3787705125) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63026](https://github.com/microsoft/TypeScript/pull/63026) (Open, `For Milestone Bug`, **gabritto**)

**Fixed a crash caused by circularly\-reentrant \`getEffectsSignature\`**

*Restores control flow container flags to function-like type-level nodes to prevent circular recursion in getEffectsSignature.*

 * created by **Andarist**
 * (yesterday) **typescript-bot** added label `For Milestone Bug`, and assigned to **gabritto**
 * [later](https://github.com/microsoft/TypeScript/pull/63026#issuecomment-3790911144) **ahejlsberg** expressed unease about introducing a stopgap recursion limiter and suggested restoring original ContainerFlags.IsControlFlowContainer values to match previous behavior

### [Issue microsoft/TypeScript#63029](https://github.com/microsoft/TypeScript/issues/63029) (Closed, `Working as Intended`)

**Top\-level variable type narrowing not matched within a function**

*TypeScript fails to retain top-level ENV_VAR’s narrowed string type inside the getEnvVars() function.*

 * **RyanCavanaugh** added label `Working as Intended`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63029#issuecomment-3781506915) **themaxgross** suggested testing code demonstrating confusing TypeScript behavior with variable declarations and the temporal dead zone, and asked if that might be the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63029#issuecomment-3781860250) **RyanCavanaugh** said "Right, you can observe ENV_VAR having the value undefined from getEnvVars (through some hypothetical indirect call), but OTHER_VAR is either a TDZ violation or a string, never undefined."
 * [today](https://github.com/microsoft/TypeScript/issues/63029#issuecomment-3785267207) **themaxgross** said they would investigate further and reopen the issue with more examples if needed, then closed the issue for now
 * (today) **themaxgross** closed the issue

### [PR microsoft/TypeScript#63030](https://github.com/microsoft/TypeScript/pull/63030) (Open, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Deprecate alwaysStrict: false in TypeScript 6\.0**

*TypeScript 6.0 deprecates alwaysStrict=false, emitting warnings and requiring ignoreDeprecations to silence them ahead of its removal in 7.0.*

 * **Copilot** assigned to **RyanCavanaugh**
 * (yesterday) **typescript-bot** added labels `For Milestone Bug`, `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787462714) **jakebailey** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787463153) **typescript-bot** reported build job statuses and results with links
 * [today](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787535109) **typescript-bot** notified that DT test results were ready and unchanged and provided a log link
 * [today](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787552435) **typescript-bot** reported test results comparing main and PR merge, noted infrastructure failures but otherwise found no issues
 * [today](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787619893) **typescript-bot** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/63030#issuecomment-3787685188) **typescript-bot** provided results of running tsc on the top 400 repos comparing main and the pull request merge and reported that everything looked good

### [PR microsoft/TypeScript#63031](https://github.com/microsoft/TypeScript/pull/63031) (Closed, `For Milestone Bug`, **RyanCavanaugh**, **Copilot**)

**Change default of \`types\` to \`\[\]\` in tsconfig\.json**

*Default tsconfig.json types array is now empty, with '*' wildcard support to maintain legacy inclusion and boost performance.*

 * (yesterday) **typescript-bot** added labels `For Milestone Bug`, `For Milestone Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3781900715) **jakebailey** said "Annoyingly the use of ` means it's not easy for a potential twoslash comment to target it, since  is for variants, but, I don't even think twoslash supports types` anyway"
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3785910022) **Copilot** reported fixing five tests by adding explicit types arrays and ensuring only expected errors appear in baselines
 * [today](https://github.com/microsoft/TypeScript/pull/63031#issuecomment-3787228978) **Copilot** addressed code review feedback and fixed 13 tests by adding explicit types arrays and resolving unintended errors

### [Issue microsoft/TypeScript#63032](https://github.com/microsoft/TypeScript/issues/63032) (Closed, `Working as Intended`)

**Narrowing readonly class instance using \`instanceof\` results in mutability**

*Narrowing a Readonly class instance with instanceof incorrectly drops its readonly properties and permits assignments.*

 * created by **jsejcksn**
 * [today](https://github.com/microsoft/TypeScript/issues/63032#issuecomment-3783332231) **MartinJohns** clarified that the code behaved as intended and explained that Readonly<T> only marks properties as readonly via the interface and doesn’t enforce immutability
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63032#issuecomment-3785561318) **RyanCavanaugh** said "The definition of a Foo is that it has a mutable value property, and instanceof Foo intentionally narrows readonlyFoo to Foo."
 * [today](https://github.com/microsoft/TypeScript/issues/63032#issuecomment-3786580368) **jsejcksn** apologized for the confusion and asked for a more idiomatic alternative to custom guard functions or direct Symbol.hasInstance invocation to preserve readonly attributes during instanceof checks
 * [today](https://github.com/microsoft/TypeScript/issues/63032#issuecomment-3786827714) **RyanCavanaugh** said "isReadonlyInstance is pretty much exactly what I'd do. I don't think there's a better altenrative"
 * [today](https://github.com/microsoft/TypeScript/issues/63032#issuecomment-3786903834) **jsejcksn** said "Thanks for the feedback @MartinJohns @RyanCavanaugh. I'm going to go ahead and close this for now."
 * (today) **jsejcksn** closed the issue

### [Issue microsoft/TypeScript#63033](https://github.com/microsoft/TypeScript/issues/63033) (Open)

**Autocomplete incorrectly suggests transitive files from monorepo package**

*Autocomplete incorrectly suggests unexported internal files from a monorepo package despite its exports configuration.*

 * created by **ericnorris**
 * [today](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3785554713) **RyanCavanaugh** said "Does this repro in TS 7? Auto-import has been basically rewritten from scratch in that codebase"
 * [today](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3786436239) **ericnorris** thanked RyanCavanaugh and reported seeing almost correct autocomplete behavior but new methods weren't suggested until after compilation, and said he would double-check his test setup
 * [today](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3786538498) **RyanCavanaugh** said "Sure. FWIW we will not be fixing TS 6 LS bugs, so only testing on 7 is relevant in terms of actionable work items"
 * [today](https://github.com/microsoft/TypeScript/issues/63033#issuecomment-3787420587) **ericnorris** verified that the bug was not present in TS 7, replicated the behaviour with a fourslash test, suggested adding a test to prevent regression, and asked if a separate issue should be filed in the typescript-go repository

### [PR microsoft/TypeScript#63038](https://github.com/microsoft/TypeScript/pull/63038) (Closed, `For Milestone Bug`, **andrewbranch**, **Copilot**)

**Fix: Consult referenced project options for synthetic default export eligibility**

*Consult referenced projects’ module options for synthetic default export eligibility using correct ES module range and redirect lookups.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **andrewbranch**
 * **typescript-bot** added label `For Milestone Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786568321) **Copilot** investigated the early-return logic at lines 3786-3796, found that getImpliedNodeFormatForEmit didn't return useful values for module: esnext with moduleResolution: bundler, and stated that using getEmitModuleKind in the declaration file section ensures correct handling of all module kinds, including nodenext
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786660816) **andrewbranch** suggested replacing getImpliedNodeFormatForEmit with getEmitModuleFormatOfFile and wiring it up in CheckerHost to avoid added code
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786684234) **Copilot** replaced function call with getEmitModuleFormatOfFile, added check for project reference declaration files, and removed manual redirect checking code
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786731112) **andrewbranch** said "@copilot I meant on line 3787"
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786751704) **Copilot** retained original behavior of getImpliedNodeFormatForEmit on line 3787 and added a conditional check to use getEmitModuleFormatOfFile for project reference declaration files when the implied format was undefined
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786758373) **andrewbranch** said "@copilot what happens when you replace line 3787 and delete the rest of your added code? If that's wrong explain to me what's going wrong and why"
 * [today](https://github.com/microsoft/TypeScript/pull/63038#issuecomment-3786773629) **Copilot** explained that replacing line 3787 and deleting the added code caused the "ambiguous-package" test to fail due to getCompilerOptionsForFile returning the consuming project's options for node_modules packages, leading getEmitModuleFormatOfFile to return ESNext and incorrectly trigger targetMode >= ES2015, and proposed using getRedirectFromSourceFile to distinguish project references from node_modules

### [Issue microsoft/TypeScript#63039](https://github.com/microsoft/TypeScript/issues/63039) (Open)

**Regression of \`this is\` type predicate for intersection of unions from 4\.7 to 4\.8**

*TypeScript 4.8 regression prevents this is type predicates from correctly narrowing intersection of union types that worked in 4.7*

 * created by **KnorpelSenf**

### [Issue microsoft/TypeScript#63040](https://github.com/microsoft/TypeScript/issues/63040) (Open)

**RangeError: Maximum call stack size exceeded in getTypeFromTypeNode when resolving recursive tuple rest with intersection**

*TypeScript crashes with a stack overflow error when resolving a recursive tuple rest type intersected with another type.*

 * created by **na7ure-a**
 * [today](https://github.com/microsoft/TypeScript/issues/63040#issuecomment-3788854014) **Andarist** said "It seems to date back to the OG: https://github.com/microsoft/TypeScript/pull/40002"

### [Issue microsoft/TypeScript#63041](https://github.com/microsoft/TypeScript/issues/63041) (Closed, `Duplicate`)

**False negative when updating React state with functional setState and object spread \(prevState\)**

*React's functional setState with object spread allows invalid properties without TypeScript type errors.*

 * created by **gabriel-h-nx**
 * **gabriel-h-nx** added label `Duplicate`
 * [later](https://github.com/microsoft/TypeScript/issues/63041#issuecomment-3789958633) **mkantor** suggested that the issue is a duplicate of #12936 unless proposing an extension to excess property check semantics
 * [later](https://github.com/microsoft/TypeScript/issues/63041#issuecomment-3789963042) **MartinJohns** explained that the issue stemmed from a missing return type annotation on the setFilters callback causing an inferred return type and compatibility check, and clarified that the duplicate label was applied automatically due to using the wrong issue template
 * [later](https://github.com/microsoft/TypeScript/issues/63041#issuecomment-3789984779) **mkantor** clarified that this isn’t the same as issue #39998 because explicitly written properties don’t error and provided a minimal reproducible example
 * [later](https://github.com/microsoft/TypeScript/issues/63041#issuecomment-3790046722) **gabriel-h-nx** apologized for incorrectly marking the issue as a duplicate
 * [later](https://github.com/microsoft/TypeScript/issues/63041#issuecomment-3790058041) **gabriel-h-nx** stated they would open another issue and expressed thanks
 * (later) **gabriel-h-nx** closed the issue

### [Issue microsoft/TypeScript#63042](https://github.com/microsoft/TypeScript/issues/63042) (Closed)

**False positive when updating React state with functional setState and object spread \(prevState\)**

*When using functional setState with object spread, TypeScript incorrectly allows unknown state properties without error.*

 * created by **dev-gabriel-henrique**
 * [later](https://github.com/microsoft/TypeScript/issues/63042#issuecomment-3790254933) **MartinJohns** said "Duplicate of #47758 / #241."
 * [later](https://github.com/microsoft/TypeScript/issues/63042#issuecomment-3790329669) **dev-gabriel-henrique** noted that the error occurred when React’s setState relied on previous state and questioned whether it belonged to React or TypeScript
 * [later](https://github.com/microsoft/TypeScript/issues/63042#issuecomment-3790382498) **MartinJohns** mentioned that the issue was a duplicate of #47758, explained that TypeScript infers the return type of the anonymous function rather than using State, and suggested adding an explicit type annotation as a workaround
 * [later](https://github.com/microsoft/TypeScript/issues/63042#issuecomment-3790442598) **dev-gabriel-henrique** asked if there was a way to avoid a false positive without explicitly declaring a function type, and said it was acceptable if not
 * (later) **dev-gabriel-henrique** closed the issue

