# Report for 2025-12-11 (Thursday, December 11th, 2025)

19 different users commented on 45 different issues.

## Recommended Actions

 * Response Recommended
    * @peterlustig78 reported unexpected type assignment error when using MixedRecord in [microsoft/TypeScript#17867](https://github.com/microsoft/TypeScript/issues/17867#issuecomment-3643166793)
    * @nonergodic provided a proposed solution with explanation and tests in [microsoft/TypeScript#37792](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-3646709265)
    * @snowc0de provided repro steps as requested in [microsoft/TypeScript#62572](https://github.com/microsoft/TypeScript/issues/62572#issuecomment-3646862355)
    * @bbrk24 asked whether custom objects implementing [Symbol.matchAll] would be supported by the fix in [microsoft/TypeScript#62873](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643607978)
    * @bbrk24 provided a screenshot showing the error in [microsoft/TypeScript#62873](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643800655)
    * @robpalme reported that error squiggles appeared on the identifier instead of the keyword and may mislead users in [microsoft/TypeScript#62876](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3643164578)
    * @valler asked how removing `composite` affects the build in [microsoft/TypeScript#62880](https://github.com/microsoft/TypeScript/issues/62880#issuecomment-3643147213)

## Activity Summary

### [Issue microsoft/TypeScript#17867](https://github.com/microsoft/TypeScript/issues/17867) (Open, `Suggestion`, `Awaiting More Feedback`)

**Need way to express hybrid types that are indexable for a subset of properties **

*Enable TypeScript interfaces to combine explicitly typed properties with a catch-all index signature for all other keys.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/17867#issuecomment-3552651144) **groszdaniel** suggested disallowing assignment when a property isn’t a subtype of the index signature type
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/17867#issuecomment-3553719986) **jcalz** explained that index signatures are a stable TypeScript feature and unlikely to change, described an alternate model with rest index signatures and exact types as infeasible, and suggested refocusing on the feature request instead of implementation details
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/17867#issuecomment-3554546802) **groszdaniel** stated index signatures are a stable feature, doubted the TS team would change their meaning, and noted uncertainty about backward compatibility or unsoundness if assignment rules were defined properly
 * [today](https://github.com/microsoft/TypeScript/issues/17867#issuecomment-3643166793) **peterlustig78** described a code example where reading from a MixedRecord type worked but writing an object to it failed unexpectedly

### [Issue microsoft/TypeScript#29841](https://github.com/microsoft/TypeScript/issues/29841) (Open, `Needs Investigation`, `Fix Available`, `Rescheduled`, **DanielRosenwasser**)

**Improve typings of Array\.map when called on tuples**

*Enhance Array.map’s TypeScript typings to return a tuple type when mapping over a tuple instead of a generic array.*

 * **RyanCavanaugh** added to milestone `TypeScript 5.7.0`
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-2980318799) **marcospgp** said "seeing this issue is still open, is there any chance we can still get proper tuple typing in built in functions like .map()?"
 * [11 weeks ago](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-3327091081) **Anoesj** requested automatic tuple .map() typing support and suggested a tsconfig option
 * [today](https://github.com/microsoft/TypeScript/issues/29841#issuecomment-3642875750) **petdomaa100** reported encountering the issue frequently and suggested using a dedicated mapTuple method or utility function as a workaround

### [Issue microsoft/TypeScript#37792](https://github.com/microsoft/TypeScript/issues/37792) (Closed, `Suggestion`, `Declined`)

**Support for Read\-only Typed Arrays**

*Provide a ReadonlyTypedArray<T> type to statically enforce immutability on TypedArray instances similar to ReadonlyArray<T>.*

 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-2928232832) **repulsio** said "Ran into this issue and was surprised this is not built-in"
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-3120737043) **yuhr** said "For those who want just an immutable byte array and don't need it to be an instance of TypedArray, Blob might be useful."
 * [10 weeks ago](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-3344764992) **pNm193** suggested a ReadonlyTypedArray type for immutable typed arrays, described use cases and examples, and detailed workarounds and a compliance checklist
 * [later](https://github.com/microsoft/TypeScript/issues/37792#issuecomment-3646709265) **nonergodic** provided a fully airtight solution implementation with TypeScript code, explanation link, and tests link

### [Issue microsoft/TypeScript#55843](https://github.com/microsoft/TypeScript/issues/55843) (Open, `Suggestion`, `Awaiting More Feedback`)

**String\#matchAll is too restrictive in its parameter type**

*TypeScript restricts string.matchAll to RegExp instances instead of allowing objects with a Symbol.matchAll method.*

 * (2.2 years ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/55843#issuecomment-2480532317) **lionel-rowe** remarked that the issue had existed for other Symbol methods but was now fixed and provided type definitions and an example illustrating lenient runtime types
 * (today) **jakebailey** closed the issue
 * (today) **jakebailey** reopened the issue

### [Issue microsoft/TypeScript#62208](https://github.com/microsoft/TypeScript/issues/62208) (Closed, `Suggestion`, `Breaking Change`, `Committed`)

**Deprecate, remove support for \`/// \<amd\-module name="\.\.\." /\>\` directives**

*Deprecate and remove support for /// <amd-module> directives following the removal of AMD modules in TypeScript 7.*

 * **DanielRosenwasser** added to milestone `TypeScript 6.0`
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/62208#issuecomment-3156085083) **sheetalkamat** said "Also amd-dependency directive"
 * [14 weeks ago](https://github.com/microsoft/TypeScript/issues/62208#issuecomment-3251089424) **DanielRosenwasser** said "Probably no implementation required here if we're just deprecating --module amd (see https://github.com/microsoft/TypeScript/issues/62199)."
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#62211](https://github.com/microsoft/TypeScript/issues/62211) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **RyanCavanaugh**, **Copilot**)

**Deprecate, remove support for using \`module\` in place of \`namespace\`**

*TypeScript 6.0 will deprecate and error on using the module keyword for namespaces, with errors enforced by default in 7.0.*

 * (7 weeks ago) **RyanCavanaugh** closed the issue
 * (today) **DanielRosenwasser** reopened the issue
 * **typescript-bot** added label `Fix Available`
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62390](https://github.com/microsoft/TypeScript/pull/62390) (Closed, **DanielRosenwasser**, **Copilot**)

**Implement TypeScript 6\.0 deprecation of \`module\` keyword for namespace declarations**

*Deprecate TypeScript’s module keyword for namespace declarations with a TS1547 error and a suppression option.*

 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62390#issuecomment-3254469869) **Copilot** updated 39 test files to use namespace instead of module and preserved tests specifically covering module keyword behavior
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62390#issuecomment-3254629852) **Copilot** updated 16 test files in tests/cases/compiler to replace module foo declarations with namespace foo, preserved ambient module declarations and excluded files testing module keyword behavior, and updated all baselines
 * [14 weeks ago](https://github.com/microsoft/TypeScript/pull/62390#issuecomment-3254953833) **Copilot** ran tests with npx hereby runtests-parallel and updated test files; reduced failures from over 100 to about 39; identified remaining failure causes; updated 25+ files to use namespace and adjusted baselines; and confirmed module deprecation feature works as expected
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62499](https://github.com/microsoft/TypeScript/issues/62499) (Open, `Infrastructure`, `Fix Available`, **jakebailey**)

**Consider adopting npm trusted publishing**

*Advocate adopting npm trusted publishing for cryptographic provenance and eliminating vulnerable legacy tokens to enhance supply chain security.*

 * (8 weeks ago) **RyanCavanaugh** set milestone to `TypeScript 6.0.0`, and assigned to **jakebailey**
 * **typescript-bot** added label `Fix Available`
 * (today) **DanielRosenwasser** set milestone to `Backlog`, and removed from milestone `TypeScript 6.0.0`

### [Issue microsoft/TypeScript#62572](https://github.com/microsoft/TypeScript/issues/62572) (Open, `Domain: Mapped Types`, `Experimentation Needed`, `Possible Improvement`)

**Destructuring all but one key dynamically via rest creates an unusable type by omitting all of its keys**

*Using object rest to exclude a dynamic key from Partial<T> omits all keys, yielding a never type and assignment error.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/62572#issuecomment-3386542176) **jcalz** explained two design limitations in TypeScript's type system around generics and union-typed keys, provided a non-generic code example, and suggested using a generic key parameter
 * **RyanCavanaugh** added label `Domain: Mapped Types`
 * [later](https://github.com/microsoft/TypeScript/issues/62572#issuecomment-3646862355) **snowc0de** provided a simple reproduction of the issue with a code snippet and playground link

### [PR microsoft/TypeScript#62684](https://github.com/microsoft/TypeScript/pull/62684) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**\[experiment\] Remove package deduplication**

*Experimentally remove package deduplication to assess the negative impact of not resolving typescript-go issue 1080.*

 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/62684#issuecomment-3458873303) **Benjamin-Dobell** noted GitHub's poor deduplication, pointed to an existing minimal reproduction link, and explained that Kysely's use of private fields and classes instead of interfaces causes the problem
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/62684#issuecomment-3458876394) **jakebailey** said "But aren't the errors it states about duplication objectively correct, and the code just happens to be lucky to not notice internally?"
 * [6 weeks ago](https://github.com/microsoft/TypeScript/pull/62684#issuecomment-3458931720) **Benjamin-Dobell** explained that the type-safety depends on build-time deduplication of the Kysely module and whether it’s used purely as a type or at runtime, noting unsoundness can occur if there’s no deduplication and runtime usage
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#62730](https://github.com/microsoft/TypeScript/pull/62730) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**DOM update 2025\-12\-10**

*Update the DOM to include the latest changes made on December 10, 2025.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639673318) **typescript-bot** ran user tests comparing main with the PR merge, noted one Git clone failure, and found everything else good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639719897) **typescript-bot** posted the requested perf run results for tsc with detailed comparison metrics
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3639794378) **typescript-bot** reported build results for top 400 repos and highlighted new TS2345 errors in microsoft/vscode comparing main and the pull request
 * [today](https://github.com/microsoft/TypeScript/pull/62730#issuecomment-3643825924) **jakebailey** said "Hm, I guess the generated Navigator is missing a few things"

### [Issue microsoft/TypeScript#62857](https://github.com/microsoft/TypeScript/issues/62857) (Closed, `Not a Defect`)

**JavaScript IntelliSense does not suggest methods added to built\-in prototypes**

*JavaScript IntelliSense in VS Code fails to suggest custom methods added to built-in prototypes like Promise.log.*

 * **mjbvz** unassigned **mjbvz**
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3634219335) **RyanCavanaugh** said "Global merges like this aren't supported; you'll need to use a .d.ts file for this"
 * [today](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3644523154) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62860](https://github.com/microsoft/TypeScript/issues/62860) (Closed, `Question`)

**TypeScript Auto\-Import Fails for Workspace Package in ESM Monorepo with Project References and Specific Dependencies**

*TypeScript's auto-import suggestions fail for local workspace packages in an ESM monorepo when project dependencies are specified.*

 * **mjbvz** unassigned **mjbvz**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62860#issuecomment-3633568553) **RyanCavanaugh** said "See https://github.com/Microsoft/TypeScript/wiki/FAQ#auto-import-heuristics-and-preferences"
 * **RyanCavanaugh** added label `Question`
 * [today](https://github.com/microsoft/TypeScript/issues/62860#issuecomment-3644523273) **typescript-bot** said "This issue has been marked as "Question" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#62872](https://github.com/microsoft/TypeScript/issues/62872) (Closed, `Not a Defect`)

**Resolving type incorrectly when loop is involved**

*TypeScript incorrectly infers 'any' for a loop variable when narrowing a union type across iterations.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62872#issuecomment-3634229217) **MathMan05** said "also to note, the useless if statement if removed makes things work again"
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62872#issuecomment-3634282073) **RyanCavanaugh** explained that the if statement is relevant because exit points could change what values reach `last` and linked to the circularity errors FAQ
 * [today](https://github.com/microsoft/TypeScript/issues/62872#issuecomment-3644523078) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#62873](https://github.com/microsoft/TypeScript/pull/62873) (Closed, `For Uncommitted Bug`)

**ES2020: fix String\.prototype\.matchAll type and description**

*Correct the TypeScript type definitions and documentation for ES2020’s String.prototype.matchAll method.*

 * [2 days ago](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3634399398) **typescript-bot** said "The TypeScript team hasn't accepted the linked issue #55843. If you can get it accepted, this PR will have a better chance of being reviewed."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3639384957) **DanielRosenwasser** said "v6 will be in TS, v7 will be the Go-based implementation."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3639401039) **ljharb** said "phew, thanks :-)"
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643174996) **ljharb** said "Will this show up in the nightly v6 build the same day it's merged?"
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643178806) **jakebailey** requested the typescript-bot to run tests for safety
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643179026) **typescript-bot** reported CI build statuses for four commands with links to started builds and results
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643256205) **typescript-bot** notified that the DT test results are ready and unchanged
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643282493) **typescript-bot** reported tsc user test results comparing main and the PR merge, noted a Git clone failure likely due to infra, and confirmed that everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643367543) **typescript-bot** provided the performance run results requested by @jakebailey, including errors, symbols, types, memory usage, and parse time metrics
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643488294) **typescript-bot** reported that tsc comparisons between main and the pull request merge on the top 400 repos succeeded without issues
 * (today) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643607978) **bbrk24** said "I'm not sure this actually resolves the linked issue -- the linked issue talks about passing custom objects that implement the [Symbol.matchAll] method, not just RegExp instances and strings."
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643767448) **ljharb** said "ah, that's true - it's more like the proper resolution to the incorrectly-closed #47310."
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643788658) **jakebailey** highlighted that the context was critical and that he would not have approved and merged the PR had he known, and noted that their lib types can be stricter than the spec, suggesting the function could accept number types
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643791502) **RyanCavanaugh** criticized the merge and noted that matchAll throws a runtime error when passed a string containing '(' because it's being regexified
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643800655) **bbrk24** provided evidence that testing produced an error via screenshot
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643805196) **ljharb** said "Then that's a major implementation bug - the spec does not say to do that. https://tc39.es/ecma262/#sec-string.prototype.matchall"
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643807947) **ljharb** said "I will file implementation bugs for every affected engine, but matchAll absolutely should not coerce to a regexp."
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643811921) **RyanCavanaugh** said "@ljharb What is step 5 doing if not creating a regexp?"
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643815541) **ljharb** said "shit, you're right. clearly my memory is incorrect, and i'm astonished it went in this way. Please do revert this PR, then, and I apologize for the confusion."
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3644164874) **Renegade334** pointed out that matchAll would align with match’s existing signature including coercion behavior and questioned their consistency
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3644170531) **jakebailey** said "Yeah, if we have a string somewhere else, that is probably a mistake"
 * [today](https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3644173626) **ljharb** reasoned that consistency with match motivated the design choice and suggested allowing strings for both or neither

### [PR microsoft/TypeScript#62876](https://github.com/microsoft/TypeScript/pull/62876) (Closed, `Author: Team`, `For Milestone Bug`, **RyanCavanaugh**)

**Deprecate \`module\` syntax**

*Deprecate and error on all ‘module’ and ‘declare module’ syntax forms in TypeScript*

 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3640806861) **typescript-bot** reported build jobs starting and provided status links
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3640821944) **typescript-bot** provided an installable tgz and testing instructions along with playground and npm module links
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3641045349) **robpalme** thanked the author for the pack and reported that provoking the intended checker error crashed the compiler, including a StackBlitz link and the error message
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3642832135) **RyanCavanaugh** joked that provoking the checker error crash was one way to get people to change their code
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3642874586) **RyanCavanaugh** invoked the TypeScript bot with 'test top800' and 'pack this' commands
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3642874877) **typescript-bot** posted build status updates for test top800 and pack this commands with links to results
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3642891289) **typescript-bot** provided instructions for installing the TypeScript 6.0.0-insiders build via a tgz link and shared playground and npm module links
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3643164578) **robpalme** commended the new pack for working without crashes and correctly erroring on the declare form, and noted that error squiggles appeared on the identifier rather than the keyword, which was misleading
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3643459174) **typescript-bot** provided build results for top 800 repos comparing main and refs/pull/62876/merge and asked for review
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3643824066) **jakebailey** said "@typescript-bot test top800"
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3643824331) **typescript-bot** initiated test job run and posted build status and result links
 * [today](https://github.com/microsoft/TypeScript/pull/62876#issuecomment-3644259333) **typescript-bot** reported that everything looked good after running tsc on the top 800 repositories comparing main and the pull request merge
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62880](https://github.com/microsoft/TypeScript/issues/62880) (Open, `Needs Investigation`, **andrewbranch**)

**subpath imports should play well with project references**

*TypeScript project references misinterpret Node.js subpath imports like '#bob/module' as internal files, causing TS6307 build errors.*

 * created by **valler**
 * [today](https://github.com/microsoft/TypeScript/issues/62880#issuecomment-3643147213) **valler** noted that removing `composite` in tsconfig.other.json removed the error but was unsure about build implications given docs recommendation

### [Issue microsoft/TypeScript#62881](https://github.com/microsoft/TypeScript/issues/62881) (Closed, `7.0 LS Migration`)

**unactionable warning: All type parameters are unused\. \(6205\)**

*Declaration merging to extend ColumnMeta with unused type parameter TData triggers warning 6205 and results in conflicting declarations.*

 * created by **jendrikw**
 * **RyanCavanaugh** added label `7.0 LS Migration`
 * [today](https://github.com/microsoft/TypeScript/issues/62881#issuecomment-3644104695) **RyanCavanaugh** said "This sort of check won't be in 7.0, so this is effectively fixed in that release"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62882](https://github.com/microsoft/TypeScript/issues/62882) (Open, `Suggestion`, `Experience Enhancement`)

**Autocompletion does NOT remove \`type\` from \`import type\` when needed**

*VS Code autocompletion no longer removes the type keyword from import type statements when switching to value imports.*

 * created by **Friend-LGA**
 * [today](https://github.com/microsoft/TypeScript/issues/62882#issuecomment-3642787238) **vs-code-engineering[bot]** thanked the user for creating the issue and suggested upgrading to the latest VS Code version to see if the issue persists
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62883](https://github.com/microsoft/TypeScript/issues/62883) (Closed, `Duplicate`)

**Redesign \`\(const\) enum\` and \`namespace\` emit for better treeshaking**

*Propose redesigning TypeScript's enum and namespace code generation using pure IIFEs like esbuild for improved treeshaking.*

 * created by **Septh**
 * [today](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3644205817) **MartinJohns** said "Duplicate of #27604."
 * [today](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3644308777) **Septh** expressed surprise and thanked the finder, hoping to bring the seven-year-old duplicate issue back to maintainers' attention
 * [later](https://github.com/microsoft/TypeScript/issues/62883#issuecomment-3646947172) **MartinJohns** said "Related: https://github.com/microsoft/typescript/wiki/faq#time-marches-on"

### [Issue microsoft/TypeScript#62884](https://github.com/microsoft/TypeScript/issues/62884) (Closed, `Question`)

**ts\.parseJsonConfigFileContent double\-adds relative path, resulting in broken "include" pattern\.**

*ts.parseJsonConfigFileContent incorrectly prefixes include paths with the base directory twice, causing no files to be matched.*

 * created by **maxpatiiuk**

### [PR microsoft/TypeScript#62885](https://github.com/microsoft/TypeScript/pull/62885) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Revert "ES2020: fix String\.prototype\.matchAll type and description"**

*Revert ES2020 String.prototype.matchAll type and description changes because they incorrectly addressed a working-as-intended issue instead of the original bug.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/62885#issuecomment-3643818687) **jakebailey** said "for posterity for other readers, see thread at https://github.com/microsoft/TypeScript/pull/62873#issuecomment-3643800655"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#62886](https://github.com/microsoft/TypeScript/issues/62886) (Closed, `Duplicate`)

**composite typescript project types should not leak into excluded files**

*Composite TypeScript projects' types settings in referenced tsconfigs are leaking into excluded files.*

 * created by **valler**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#62887](https://github.com/microsoft/TypeScript/issues/62887) (Open, `Needs Investigation`, **sheetalkamat**)

**TS Server Crash Loop: Copilot Chat virtual files \('vscode\-chat\-code\-block'\) trigger infinite Directory Watcher recursion on InferredProject**

*Copilot Chat’s virtual “vscode-chat-code-block” files cause the TypeScript server to enter infinite directory watcher recursion, spike CPU, and crash repeatedly.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644228310) **cleversonferreira** provided steps to unlock VS Code as a workaround until the bug was fixed
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644228323) **iErKy** said "Same problem here, @cleversonferreira fix seems to work (Thanks), hopefully this issue gets fixed because it's hard to work like this."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644228336) **Bialson** said "This issue is very annoying, I can also confirm that issue persists in my workflow. It should be fixed as soon as possible cause editor is unusable due to this problem."
 * (today) **rzhao271** added label `Bug`, and assigned to **mjbvz**
 * (today) **mjbvz** removed label `Bug`, and unassigned **mjbvz**, **justschen**
 * [today](https://github.com/microsoft/TypeScript/issues/62887#issuecomment-3644229903) **mjbvz** said "@sheetalkamat Can you please take a look at the virtual file watching to make sure it's handling the chat code block documents correctly "

### [PR microsoft/TypeScript#62889](https://github.com/microsoft/TypeScript/pull/62889) (Closed, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add note re: PRs to CONTRIBUTING\.md**

*Add a note to CONTRIBUTING.md outlining pull request guidelines per the 6.0/7.0 plan.*

 * created by **RyanCavanaugh**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **RyanCavanaugh**

### [PR microsoft/TypeScript#62890](https://github.com/microsoft/TypeScript/pull/62890) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix accidental module replacements in tests**

*Remove unintended redundant module replacements in tests introduced during cherry-picking to the tsgo-port branch.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#62891](https://github.com/microsoft/TypeScript/pull/62891) (Closed, `For Backlog Bug`)

**Fix typo: MERCHANTABLITY → MERCHANTABILITY**

*Corrects the typo 'MERCHANTABLITY' to 'MERCHANTABILITY' in copyright notices and related test files.*

 * created by **tt-a1i**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62891#issuecomment-3645848623) **typescript-bot** advised to document breaking changes on the wiki and notify DanielRosenwasser and RyanCavanaugh
 * [later](https://github.com/microsoft/TypeScript/pull/62891#issuecomment-3645918958) **tt-a1i** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#62892](https://github.com/microsoft/TypeScript/pull/62892) (Open, `For Backlog Bug`)

**Allow enum keys accessed with bracket notation as computed properties**

*Enable TypeScript to recognize enum keys accessed via bracket notation as valid computed property names in type literals.*

 * created by **tt-a1i**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/62892#issuecomment-3645920520) **tt-a1i** said "@microsoft-github-policy-service agree"

