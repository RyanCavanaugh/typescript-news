# Report for 2026-02-26 (Thursday, February 26th, 2026)

13 different users commented on 16 different issues.

## Recommended Actions

 * Response Recommended
    * @54145a suggested using template literal types to infer tag names from CSS selectors for improved querySelector type safety in [microsoft/TypeScript#29037](https://github.com/microsoft/TypeScript/issues/29037#issuecomment-3973006589)
    * @54145a suggested TypeScript should emit an error when a subclass overrides only the setter of a parent getter/setter pair in [microsoft/TypeScript#47581](https://github.com/microsoft/TypeScript/issues/47581#issuecomment-3971117842)
    * @goodov provided information about attempted configurations in [microsoft/TypeScript#61021](https://github.com/microsoft/TypeScript/issues/61021#issuecomment-3968277986)
    * @Boukeng-rochinel proposed adding a feature for enums emitting plain JavaScript objects for type-stripping runtimes in [microsoft/TypeScript#63198](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973156762)

## Activity Summary

### [Issue microsoft/TypeScript#29037](https://github.com/microsoft/TypeScript/issues/29037) (Open, `Suggestion`, `In Discussion`, `Domain: lib.d.ts`)

**querySelector return type could be more specific for compound selectors**

*Enhance querySelector to return a specific element interface for compound selectors that include a type selector.*

 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/29037#issuecomment-715309310) **Raynos** asked whether someone could open a PR with this change from the playground
 * [5.2 years ago](https://github.com/microsoft/TypeScript/issues/29037#issuecomment-726688864) **g-plane** said "For anyone who want this feature now, I've released an npm package for you. Here is the repository: https://github.com/g-plane/typed-query-selector . Feel free to use and star it."
 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/29037#issuecomment-3135919989) **jendrikw** said "What would be the next steps to get this feature into the official dom types?"
 * [later](https://github.com/microsoft/TypeScript/issues/29037#issuecomment-3973006589) **54145a** suggested using template literal types to extract tag names from CSS selector strings for improved querySelector type safety

### [Issue microsoft/TypeScript#42357](https://github.com/microsoft/TypeScript/issues/42357) (Open, `Suggestion`, `Awaiting More Feedback`)

**Readonly everything by default**

*Propose a TypeScript compiler option to default all types to readonly and mark mutable properties using the mutable keyword.*

 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/42357#issuecomment-2495533305) **rhaksw** suggested using an ESLint plugin as a more practical alternative to changing TypeScript
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/42357#issuecomment-2555281974) **ardokirsipuu** suggested using an ESLint plugin instead of changing TypeScript and asked which specific rules (read-only vs no-mutation) were intended
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/42357#issuecomment-2555665593) **rhaksw** said "Yes, I meant the rule in your second link, functional/immutable-data. Thanks!"
 * [today](https://github.com/microsoft/TypeScript/issues/42357#issuecomment-3967570611) **andyearnshaw** reposted a comment from another issue and described frequent unnecessary useMemo patterns in React, recommended using a frozen default array constant and advocated for read-only types by default with a Writable utility

### [Issue microsoft/TypeScript#47581](https://github.com/microsoft/TypeScript/issues/47581) (Open, `Suggestion`, `Experience Enhancement`)

**A derived class is allowed be created without a parent's getter or setter\.**

*Subclasses can declare a setter for an inherited property without providing a corresponding getter, causing runtime errors.*

 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/47581#issuecomment-1165374361) **BlakeOne** agreed that Child should inherit Parent's getter and noted that this makes overriding the setter unnecessarily difficult
 * [3.2 years ago](https://github.com/microsoft/TypeScript/issues/47581#issuecomment-1330436120) **Jack-Works** reported that TypeScript did not error when a subclass defined only a setter and inherited a getter from the parent class
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/47581#issuecomment-2429307596) **viktorpts** joined discussion and argued that making an overridden getter private reduced accessibility and broke Liskov Substitution, and suggested that the child class should either retain access to the parent's getter or cause a compilation error when overriding only the setter
 * [today](https://github.com/microsoft/TypeScript/issues/47581#issuecomment-3971117842) **54145a** explained that overriding only the setter in a subclass discards the parent’s getter at runtime, breaking type safety and substitutability, and suggested TypeScript emit a compile-time error for this scenario

### [Issue microsoft/TypeScript#61021](https://github.com/microsoft/TypeScript/issues/61021) (Open, `Suggestion`, `In Discussion`)

**rewriteRelativeImportExtensions & enforce consistent extensions**

*Add a compiler option enforcing consistent .ts extensions for relative imports and disallowing .js paths when importing TypeScript files*

 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/61021#issuecomment-3266883073) **mbrevda** confirmed side-by-side compilation as the cause and asked if it’s possible to enforce strict Node module resolution without extension substitution
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/61021#issuecomment-3266984421) **darksabrefr** clarified that rewriteRelativeImportExtensions ensures code can run in place while allowImportingTsExtensions disables extension substitution
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/61021#issuecomment-3267031381) **mbrevda** reported extension substitution occurring despite allowImportingTsExtensions being true, preventing catching node module resolution errors until runtime
 * [today](https://github.com/microsoft/TypeScript/issues/61021#issuecomment-3968277986) **goodov** upvoted the issue, noted that Node broke due to missing .js files, and reported that trying various options didn’t help

### [Issue microsoft/TypeScript#63152](https://github.com/microsoft/TypeScript/issues/63152) (Closed, `Duplicate`)

**\.call selects the wrong overload, resulting in ts2554**

*Using .call on XMLHttpRequest.prototype.open incorrectly selects the longer overload and triggers a TS2554 error.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3922916941) **jcalz** suggested widening xhrOpen's type using an intermediate variable and provided example code
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3923237925) **joshcartme** thanked everyone and complimented @jcalz's solution, then suggested closing the issue
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3970220324) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63160](https://github.com/microsoft/TypeScript/issues/63160) (Closed, `Duplicate`)

**Inferring from setter returns getter value**

*TypeScript's conditional type inference picks the getter's return type instead of the setter's parameter type.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3928849152) **LukeAbby** clarified that issue #62943 had been closed as a duplicate of #60162, #43729, and #60954, none involving infer, and noted that #60162 suggested adding a new intrinsic for dynamic props
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3928911901) **MartinJohns** clarified that the first issue involved infer and was marked as a duplicate by a team member
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3970220256) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63191](https://github.com/microsoft/TypeScript/issues/63191) (Closed, `Suggestion`, `Declined`)

**The "?" operator would be forbidden before the "\!" operator**

*Request to disallow combining optional chaining (?) with non-null assertion (!) in TypeScript to prevent unsafe undefined values.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3960760106) **RyanCavanaugh** explained that disallowing non-null assertions when undefined/null wasn’t in the operand would render the operator pointless and illustrated using `a?.b!` to satisfy an incorrectly declared function signature
 * (yesterday) **RyanCavanaugh** added labels `Suggestion`, `Declined`
 * [today](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3968828854) **jcalz** said "Also see #34875 and #35025 "

### [Issue microsoft/TypeScript#63194](https://github.com/microsoft/TypeScript/issues/63194) (Open, `Suggestion`, `Awaiting More Feedback`)

**🚀 Proposal: Cross\-Context Function Annotation \(for APIs like \`page\.evaluate\` of playwright\)**

*Introduce an isolated function annotation for cross-context APIs like page.evaluate to prevent closure captures and invalid global access.*

 * created by **jogibear9988**
 * [today](https://github.com/microsoft/TypeScript/issues/63194#issuecomment-3966878590) **nmain** observed that Playwright's function stringification and custom evals in a separate environment are too specialized for TypeScript to model
 * [today](https://github.com/microsoft/TypeScript/issues/63194#issuecomment-3967379989) **jogibear9988** asked whether React's "use server"/"use client" directive was similar
 * [today](https://github.com/microsoft/TypeScript/issues/63194#issuecomment-3967751959) **RyanCavanaugh** suggested using a lint rule to forbid outer lexical scope access for predefined functions and noted that baking it into TS as a primitive would be difficult
 * (today) **RyanCavanaugh** added labels `Suggestion`, `For Milestone Bug`, `Awaiting More Feedback`, and removed label `For Milestone Bug`

### [Issue microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195) (Open, `Needs More Info`)

**Debug Failure: "No error for last overload signature" crash when CustomTypeOptions\.resources uses typeof on a large \(~10k line\) JSON file**

*TypeScript crashes with 'No error for last overload signature' when using typeof on a large JSON for i18next CustomTypeOptions.resources.*

 * created by **shahanahmed86**
 * [today](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-3967758768) **RyanCavanaugh** said "We need a concrete repro we can run ourselves"
 * **RyanCavanaugh** added label `Needs More Info`

### [PR microsoft/TypeScript#63196](https://github.com/microsoft/TypeScript/pull/63196) (Closed, `For Uncommitted Bug`)

**job/momentum**

*Pull request for job/momentum includes boilerplate template but lacks implementation details or issue reference.*

 * created by **alexandercarlis2-dotcom**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63196#issuecomment-3968127296) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63197](https://github.com/microsoft/TypeScript/issues/63197) (Open)

**Fatal OOM crash on recursive template literal type**

*A recursive template literal type definition causes a fatal out-of-memory crash in TypeScript versions 5.9.3 and 6.0.0-beta.*

 * created by **james-pre**

### [Issue microsoft/TypeScript#63198](https://github.com/microsoft/TypeScript/issues/63198) (Closed, `Duplicate`)

**"Pure" Replacement for Enums \(Erasable Constants\)**

*Propose a fully erasable TypeScript enum syntax that compiles to a simple object literal without runtime code.*

 * created by **Boukeng-rochinel**
 * [later](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3972916409) **MartinJohns** said "https://www.typescriptlang.org/docs/handbook/enums.html#const-enums"
 * [later](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973078434) **nmain** suggested simplifying search terms and pointed to issue #62883 for enum IIFE
 * [later](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973129333) **jcalz** expressed confusion about the proposal's specifics and sketched a potential syntax interpretation
 * [later](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973156762) **Boukeng-rochinel** proposed an enum emitting a plain JavaScript object to support type-stripping runtimes instead of IIFEs since const enums are removed entirely at compile time
 * [later](https://github.com/microsoft/TypeScript/issues/63198#issuecomment-3973393272) **MartinJohns** noted that the proposal would conflict with the Viability Checklist and language Design Goals

### [Issue microsoft/TypeScript#63199](https://github.com/microsoft/TypeScript/issues/63199) (Open)

**Crash: TypeError: Cannot read properties of undefined \(reading 'aliasSymbol'\) remains when using variadic tuple with \(infer C\)\[\] and constrained infer**

*TypeScript compiler throws a TypeError reading 'aliasSymbol' when inferring variadic tuple types with a constrained infer array.*

 * created by **na7ure-a**

### [PR microsoft/TypeScript#63200](https://github.com/microsoft/TypeScript/pull/63200) (Closed, `For Uncommitted Bug`)

**Adds the symbol name to the error message for TS2742**

*Include the missing symbol name in TS2742 error messages to offer clearer guidance on required imports.*

 * created by **arcanis**
 * (later) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63200#issuecomment-3973509034) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63200#issuecomment-3973509082) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

