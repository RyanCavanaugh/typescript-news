# Report for 2025-12-07 (Sunday, December 7th, 2025)

16 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @Pentadome asked why paths can't be excluded from type checking in [microsoft/TypeScript#40426](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3626316257)
    * @XantreDev asked for clarification about simple cases and why RegExp literals are excluded from AST-level inference in [microsoft/TypeScript#58944](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3622389790)
    * @DavidVanPluto provided real-world usage data on ES5-only environments requiring support in [microsoft/TypeScript#62196](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3627498607)
    * @bradthomasbrown asked why generics default to conflicting types instead of a standard default or requiring explicit specification in [microsoft/TypeScript#62240](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3624527695)
    * @bradthomasbrown suggested adding a remark to make the error more intuitive in [microsoft/TypeScript#62240](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3627644579)
    * @Scalahansolo asked whether this should also work with moduleResolution set to bundler in [microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627521315)

## Activity Summary

### [Issue microsoft/TypeScript#40426](https://github.com/microsoft/TypeScript/issues/40426) (Open, `Suggestion`, `Awaiting More Feedback`)

**Disable type checking for node\_modules entirely**

*Allow disabling TypeScript type checking for node_modules to avoid build errors caused by external libraries’ faulty type definitions.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3257038644) **iva2k** suggested adding an option to silence node_modules type check messages while still importing types
 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3257296565) **onyedikachi23** praised the proposed option to silence node_module type check messages while preserving type propagation
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3590991290) **sparr** encountered error checking in excluded node_modules and requested how to disable it
 * [later](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3626316257) **Pentadome** said "I needed to import a .ts file from a node module and now i get typescript errors from that file. Why can't we set paths where we don't want type checking?"

### [Issue microsoft/TypeScript#58944](https://github.com/microsoft/TypeScript/issues/58944) (Open, `Discussion`)

**Isolated Declarations in TS 5\.5: State of the feature**

*A status update on TypeScript 5.5’s experimental --isolatedDeclarations flag, outlining its current stability, effects, and usage guidance.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3192229040) **dynst** questioned whether isolatedDeclarations erroneously errors on types or interfaces defined in the same file and asked if this was a bug
 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3192348561) **kirkwaiblinger** explained that using a numeric literal works whereas Infinity relies on a global, and provided a playground link
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3197456987) **dynst** suggested adding documentation for the feature and noted issues with number and RegExp literal type inference
 * [today](https://github.com/microsoft/TypeScript/issues/58944#issuecomment-3622389790) **XantreDev** asked what constituted the simple case for isolatedDeclarations and why RegExp literals were excluded from AST-level inference

### [Issue microsoft/TypeScript#62196](https://github.com/microsoft/TypeScript/issues/62196) (Open, `Suggestion`, `Breaking Change`, `Committed`, **iisaduan**)

**Deprecate \`\-\-target es5\`, make lowest target \`es2015\`**

*Deprecate --target es5 in TypeScript 6.0, raise the minimum target to ES2015, and update library inclusion and downlevel iteration handling.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3608321650) **snarbles2** clarified that the sentiment was about TypeScript 7's suitability rather than ignorance of Babel, and acknowledged Babel exists and ES5 support has some non-zero value
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3608339216) **RyanCavanaugh** said "Probably! But if there's an actual technical blocker that we hadn't thought of, we would want to know about it."
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3608761605) **guilhermesimoes** argued that avoiding alternative downlevelers was a preference rather than inability, explained the need to explore esbuild and swc given the deprecation of ES5 transpilation, cautioned against assuming all environments are evergreen, and supported the point with data on legacy browser usage
 * [later](https://github.com/microsoft/TypeScript/issues/62196#issuecomment-3627498607) **DavidVanPluto** provided examples of devices that require ES5 environments and argued that removing `--target es5` would force them to stay on TypeScript 6.0

### [Issue microsoft/TypeScript#62240](https://github.com/microsoft/TypeScript/issues/62240) (Open, `Docs`)

**Revert ts5\.9 changes for Uint8Array**

*Revert TypeScript 5.9’s generic Uint8Array type changes because they break compatibility with older TS versions.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3382157244) **RyanCavanaugh** said "@guest271314 I think you've weighed in on this enough now, thanks for the feedback"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3462101660) **webmaster128** proposed providing a way to narrow Uint8Array<ArrayBufferLike> to Uint8Array<ArrayBuffer> and asked if such a feature already exists
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3473468306) **paulmillr** asked why Uint8Array wasn't defaulted to Uint8Array<ArrayBuffer> to prevent related issues
 * [today](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3624527695) **bradthomasbrown** expressed confusion about TypeScript's default generic types conflicting and suggested alternative default strategies
 * [later](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3627188690) **snarbles2** argued that TypeScript should keep the default generic argument for Uint8Array as ArrayBufferLike, recommended against option A, noted limited appetite for further breaking changes, suggested making the constructor less precise to improve inference, and explained why defaulting to ArrayBuffer would hinder function parameter acceptance
 * [later](https://github.com/microsoft/TypeScript/issues/62240#issuecomment-3627644579) **bradthomasbrown** suggested adding a remark to clarify default type parameter differences in TypedArrays to make the error more intuitive

### [Issue microsoft/TypeScript#62796](https://github.com/microsoft/TypeScript/issues/62796) (Open, `Suggestion`, `Awaiting More Feedback`)

**\`noUncheckedIndexedAccess\` should forbid unsound \`Record\<string, string\>\` → \`Record\<"k", string\>\` coercion**

*TypeScript should forbid unsound coercion from Record<string,string> to Record<'k',string> when noUncheckedIndexedAccess is enabled.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62796#issuecomment-3572627590) **jendrikw** said "I only use record types with the value type including undefined: Record. Record works way better (read: stricter) that way."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62796#issuecomment-3572750326) **andersk** noted that noUncheckedIndexedAccess documentation omitted arrays, provided an out-of-bounds array access test case link, and agreed that enabling the flag helps find unsound indexed code
 * [later](https://github.com/microsoft/TypeScript/issues/62796#issuecomment-3627476213) **jcalz** noted that the issue duplicated #29698 and asked whether fixing #29698 would resolve the problem without touching noUncheckedIndexedAccess

### [Issue microsoft/TypeScript#62820](https://github.com/microsoft/TypeScript/issues/62820) (Closed, `Suggestion`, `Out of Scope`)

**@Concurrent decorator**

*Add a @Concurrent decorator to iterate loops concurrently with optional batching and Promise.all or Promise.allSettled logic.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3609567547) **typescript-bot** said "This issue has been marked as "Out of Scope" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (4 days ago) **typescript-bot** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3621065252) **Mindaugas3** said "is it maybe possible to do with existing typescript decorators?"
 * [today](https://github.com/microsoft/TypeScript/issues/62820#issuecomment-3624160373) **MartinJohns** said "No. JavaScript decorators can't be applied to for-loops."

### [PR microsoft/TypeScript#62844](https://github.com/microsoft/TypeScript/pull/62844) (Closed, `For Milestone Bug`)

**Allow subpath imports that start with \`\#/\`**

*Allow subpath imports starting with '#/' in package.json imports to mirror matching exports entries.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3621281581) **Scalahansolo** said "Does this implementation handle multiple file extensions? I.e. if a project contains both .ts and .tsx files?"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3621362730) **jakebailey** assumed it would require a new module resolution mode
 * [later](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627409807) **andrewbranch** said "Yeah, technically this shouldn’t go in node16. @magic-akari can you gate this on moduleResolution === ModuleResolutionKind.NodeNext?"
 * [later](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627521315) **Scalahansolo** said "Shouldn't this also work with moduleResolution being bundler?"
 * [later](https://github.com/microsoft/TypeScript/pull/62844#issuecomment-3627553198) **magic-akari** acknowledged feedback, said they’d gate the feature on NodeNext and Bundler modes, and asked if a new module resolution mode is needed or if gating behind NodeNext is sufficient

### [Issue microsoft/TypeScript#62849](https://github.com/microsoft/TypeScript/issues/62849) (Closed, `Not a Defect`)

**The existence of /// reference directives in dependencies breaks explicit typeRoots ordering**

*Dependencies using triple-slash reference directives load their type definitions before custom typeRoots, ignoring explicit typeRoots ordering.*

 * created by **a-non-a-mouse**

### [Issue microsoft/TypeScript#62850](https://github.com/microsoft/TypeScript/issues/62850) (Closed, `Not a Defect`)

**Typescript fail to pick up error with Nullish Coalescing Operator**

*TypeScript incorrectly allows using 'something.tagsArray ?? {}' to assign an optional Tag array to a boolean map without error.*

 * created by **brenhub24**
 * [today](https://github.com/microsoft/TypeScript/issues/62850#issuecomment-3623876771) **jcalz** explained that TypeScript infers the union of an array literal and an empty object as {} and thus allows assignment to a weak object type due to missing property normalization not applying to arrays

### [PR microsoft/TypeScript#62851](https://github.com/microsoft/TypeScript/pull/62851) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group with 3 updates**

*Upgrade actions/checkout to v6.0.1 and update actions/setup-node and github/codeql-action to their latest versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#62852](https://github.com/microsoft/TypeScript/issues/62852) (Closed)

**Module resolution: TypeScript not finding related modules in \.d\.ts and the same ones in consumer \.ts**

*Module specifiers in a custom .d.ts file fail to resolve during a TypeScript compiler API build using NodeNext resolution despite the same modules resolving at runtime.*

 * created by **hydroperx**
 * (later) **hydroperx** closed the issue

### [Issue microsoft/TypeScript#62853](https://github.com/microsoft/TypeScript/issues/62853) (Closed, `Duplicate`)

**Inconsistent behaviour of Record or Enum and mapped type**

*TypeScript’s Record type does not error on missing enum or const-object keys while equivalent mapped types correctly report errors.*

 * created by **ipva3**
 * [later](https://github.com/microsoft/TypeScript/issues/62853#issuecomment-3626744322) **MartinJohns** said "Duplicate of #62796."
 * [later](https://github.com/microsoft/TypeScript/issues/62853#issuecomment-3627388958) **jcalz** identified the duplication of issue #29698 concerning contravariance of Record<K, V>, provided a minimal example, and noted that issue #62796 was misfocused on noUncheckedIndexedAccess

### [Issue microsoft/TypeScript#62857](https://github.com/microsoft/TypeScript/issues/62857) (Closed, `Not a Defect`)

**JavaScript IntelliSense does not suggest methods added to built\-in prototypes**

*JavaScript IntelliSense in VS Code fails to suggest custom methods added to built-in prototypes like Promise.log.*

 * created by **sangafabrice**
 * **vs-code-engineering[bot]** assigned to **mjbvz**

