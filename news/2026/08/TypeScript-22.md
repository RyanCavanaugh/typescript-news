# Report for 2026-08-22 (Saturday, August 22nd, 2026)

12 different users commented on 32 different issues.

## Recommended Actions

 * Response Recommended
    * @bigboateng provided details about the fix in #63968 in [microsoft/TypeScript#63965](https://github.com/microsoft/TypeScript/issues/63965#issuecomment-5386604706)
    * @yunasora asked to be assigned to the issue in [microsoft/TypeScript#63966](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5385271015)

## Activity Summary

### [Issue microsoft/TypeScript#39648](https://github.com/microsoft/TypeScript/issues/39648) (Open, `Suggestion`, `In Discussion`)

**Spreading tuple into generic/type arguments**

*Allow tuple types to be spread into generic type parameters in TypeScript to reduce repetitive type arguments*

 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/39648#issuecomment-1590966308) **callumacrae** reported the same issue, shared current code, and requested a concise generic type for useMutation
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/39648#issuecomment-1915927431) **roryabraham** described having requested a syntactic sugar feature in type-fest to allow Merge to accept multiple types without nesting
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/39648#issuecomment-1915941787) **somebody1234** clarified that the kind is possible by accepting eight parameters with defaults and that the proposal only bundles parameters into an array
 * [later](https://github.com/microsoft/TypeScript/issues/39648#issuecomment-5385347405) **immjs** described using meta-programming to extract type parameters from an input constructor and apply them to the output constructor when extending a class within a function

### [Issue microsoft/TypeScript#61830](https://github.com/microsoft/TypeScript/issues/61830) (Closed, `Needs More Info`)

**VSCode's Intellisense breaks when using tsconfig's references**

*VSCode's auto-import fails to suggest symbols from tsconfig project references in monorepo setups without manual imports or package.json cleanup.*

 * **RyanCavanaugh** added label `Needs More Info`
 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/61830#issuecomment-2957927295) **Yokool** acknowledged missing the FAQ section, noted dependency list size affects the search algorithm, confirmed that enabling includePackageJsonAutoImports fixed the issue, and apologized for the oversight
 * (1.1 years ago) **Yokool** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/61830#issuecomment-5384582824) **chbybnwr** asked whether includePackageJsonAutoImports was set and expressed frustration that its default-off setting wasted time locating package exports in IntelliSense

### [Issue microsoft/TypeScript#63121](https://github.com/microsoft/TypeScript/issues/63121) (Open, `Suggestion`, `Awaiting More Feedback`)

**Display files with errors summary in \`\-\-watch\` mode**

*Enhance tsc --watch to display a summary of files with errors and their counts after each compilation*

 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/63121#issuecomment-3880022447) **RyanCavanaugh** provided an automated list of similar issues
 * (27 weeks ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63121#issuecomment-5382540259) **Gerrit0** reported that TS7 prints error summaries with `tsc -p` in single-project builds but not with `--build --watch` and requested always including the summary

### [Issue microsoft/TypeScript#63859](https://github.com/microsoft/TypeScript/issues/63859) (Closed, `Not a Defect`)

**Root file order causes tsgo to miss recursive conditional type assignability error**

*Reordering root files causes tsgo to miss recursive conditional type assignability errors.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63859#issuecomment-5351507581) **tomquist** reported that reversing the compilation root file order prevented the TS2322 error and that tsgo succeeded in both orders, confirming the root-order-dependent difference under stable type ordering
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63859#issuecomment-5351507595) **RyanCavanaugh** clarified that resilience to ordering changes is a TS7 feature, not a bug, and suggested using a simpler repro for order-dependent behavior mirroring TS6
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63859#issuecomment-5383597251) **typescript-automation[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63866](https://github.com/microsoft/TypeScript/issues/63866) (Closed, `Won't Fix`)

**Document that \`@typescript/typescript6\` ships the API under \`@typescript/old\` \(path\-based tooling\)**

*Document that the TypeScript 6 API from @typescript/typescript6 resides under @typescript/old and requires updating path-based tooling ignores accordingly.*

 * created by **Akshay090**
 * **RyanCavanaugh** added label `Won't Fix`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63866#issuecomment-5361288112) **RyanCavanaugh** argued that internal package layout shouldn't be documented and that tooling must adjust to changes
 * [today](https://github.com/microsoft/TypeScript/issues/63866#issuecomment-5383597546) **typescript-automation[bot]** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63881](https://github.com/microsoft/TypeScript/issues/63881) (Closed, `Working as Intended`, **ahejlsberg**)

**Assignment to an \`any\`\-parameterised generic rejected by tsgo, accepted by tsc 6\.0\.3**

*tsgo rejects assigning a typed ObjectSchema<FormData> to AnyObjectSchema while tsc 6.0.3 accepts it.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63881#issuecomment-5351510003) **ahejlsberg** explained that the behavior was due to the deeper analysis introduced by microsoft/typescript-go#3445, which revealed that Shape<any, any> was not assignable to Shape<FormData, AnyObject>.
 * (1 week ago) **ahejlsberg** added label `Working as Intended`, and removed label `Needs Investigation`
 * [today](https://github.com/microsoft/TypeScript/issues/63881#issuecomment-5383597393) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63960](https://github.com/microsoft/TypeScript/issues/63960) (Open, `Needs More Info`)

**TS 7\.0\.2 \(tsgo\): augmentation of a type\-only re\-exported interface resolves order\-dependently — same file set passes via explicit include list, fails via directory glob**

*TypeScript 7.0.2's directory-glob file input causes it to ignore augmentations on type-only re-exported interfaces, unlike explicit include lists.*

 * created by **DoodleBears**

### [PR microsoft/TypeScript#63961](https://github.com/microsoft/TypeScript/pull/63961) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use pinned gzip for localization generation**

*Generate localization files using a pinned klauspost/compress gzip implementation to ensure consistent outputs across Go toolchains.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [Issue microsoft/TypeScript#63962](https://github.com/microsoft/TypeScript/issues/63962) (Open, `Bug`)

**Crash: class\-level decorator on an anonymous class panics during ES decorator emit**

*Using a class decorator on an unnamed class triggers a TypeScript compiler panic during ES decorator emission*

 * created by **daniellockyer**

### [Issue microsoft/TypeScript#63963](https://github.com/microsoft/TypeScript/issues/63963) (Open, `Bug`)

**Crash: malformed object destructuring assignment panics in class fields transform**

*TypeScript compiler panics when processing a malformed object destructuring assignment in class fields transform*

 * created by **daniellockyer**

### [Issue microsoft/TypeScript#63964](https://github.com/microsoft/TypeScript/issues/63964) (Open, `Bug`)

**Crash: malformed \`super\` destructuring in a decorated class static block panics**

*The Go-based TypeScript compiler panics on malformed super destructuring in a decorated class static block*

 * created by **daniellockyer**

### [Issue microsoft/TypeScript#63965](https://github.com/microsoft/TypeScript/issues/63965) (Open, `Bug`)

**Crash: optional chain \+ tagged template panics the optional\-chain transform**

*Combining optional chaining with a tagged template literal (e?.``()) triggers a compiler panic due to unhandled KindTaggedTemplateExpression.*

 * created by **daniellockyer**
 * [later](https://github.com/microsoft/TypeScript/issues/63965#issuecomment-5386604706) **bigboateng** put up a fix in #63968, described the root cause in the optional-chain transform, and detailed how the fix handles tagged templates

### [Issue microsoft/TypeScript#63966](https://github.com/microsoft/TypeScript/issues/63966) (Open, `Possible Improvement`)

**Performance regression for declaration emit of an oversized inferred type**

*TypeScript 7’s declaration emit for nested inferred types now uses significantly more memory and time and still produces TS7056 errors*

 * created by **daniellockyer**
 * [later](https://github.com/microsoft/TypeScript/issues/63966#issuecomment-5385271015) **yunasora** requested assignment to investigate and fix the declaration emit performance regression with tests and benchmarks

### [PR microsoft/TypeScript#63967](https://github.com/microsoft/TypeScript/pull/63967) (Closed, `For Milestone Bug`)

**fix: panic on nil point on name check**

*Add a nil name check in checkNonIdentifierName to prevent nil pointer panics during name validation.*

 * created by **Dansyuqri**
 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63967#issuecomment-5385591182) **Dansyuqri** quoted the Contributor License Agreement and the instructions for agreeing via the microsoft-github-policy-service

### [PR microsoft/TypeScript#63968](https://github.com/microsoft/TypeScript/pull/63968) (Open, `For Uncommitted Bug`)

**Fix panic in the optional\-chain transform when a chain ends in a tagged template**

*Update the optional-chain transformer to correctly handle tagged template heads rather than panicking and include regression tests.*

 * created by **bigboateng**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63968#issuecomment-5386598913) **bigboateng** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#63969](https://github.com/microsoft/TypeScript/pull/63969) (Open, `For Uncommitted Bug`)

**Avoid cloning cached declaration types after truncation**

*Prevent cloning of cached declaration type nodes after truncation threshold is reached, drastically improving compile performance.*

 * created by **butros10games**
 * (later) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63969#issuecomment-5386818021) **butros10games** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63970](https://github.com/microsoft/TypeScript/issues/63970) (Open, `Suggestion`, `Awaiting More Feedback`)

**Inconsistent typing of endless generators between functions and lambdas**

*TypeScript infers void return for named infinite generators but never for generator lambdas, causing incompatible assignment errors.*

 * created by **jacekkopecky**

