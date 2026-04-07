# Report for 2026-04-03 (Friday, April 3rd, 2026)

12 different users commented on 10 different issues.

## Recommended Actions

 * Response Recommended
    * @denis-migdal provided workarounds and examples in [microsoft/TypeScript#41232](https://github.com/microsoft/TypeScript/issues/41232#issuecomment-4186696712)
    * @Andrej730 asked about typical workaround for using a TypeScript bin file with pnpm link and publishConfig.bin in [microsoft/TypeScript#45319](https://github.com/microsoft/TypeScript/issues/45319#issuecomment-4187066007)
    * @ArfanFahad asked for help resolving a persistent warning and compilation failure in [microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4187144985)
    * @Arlen22 reported continued intellisense break when opening JS/TS files outside the project in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4187180248)
    * @eduardocque asked whether the second generic could be inferred from the first in the useStoreByPath function in [microsoft/TypeScript#63348](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184066053)
    * @eduardocque asked if a change request or suggestion would break TypeScript generics in [microsoft/TypeScript#63348](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184124618)

## Activity Summary

### [Issue microsoft/TypeScript#37487](https://github.com/microsoft/TypeScript/issues/37487) (Open, `Suggestion`, `Awaiting More Feedback`)

**\[feature\] class properties that are "readonly in public, writable in private" or other permutations**

*Propose a new TypeScript class property modifier to declare properties as publicly readonly but privately writable.*

 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/37487#issuecomment-1322320187) **dhoulb** explained two options for implementing overload-like signatures and implementations for class properties with associated style and compatibility rules
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/37487#issuecomment-1344190203) **LongTengDao** suggested using the 'declare' keyword to ensure safe property declarations and prevent a runtime disappearance bug caused by the old type eraser util
 * [2.9 years ago](https://github.com/microsoft/TypeScript/issues/37487#issuecomment-1501232253) **TheCymaera** suggested using modifier overloading to allow different access modifiers on class members and collapse them based on access context
 * [today](https://github.com/microsoft/TypeScript/issues/37487#issuecomment-4185455564) **khokm** described using tsdoc @readonly comments as a temporary workaround for properties that should be mutable inside but readonly outside

### [Issue microsoft/TypeScript#41232](https://github.com/microsoft/TypeScript/issues/41232) (Open, `Bug`, `Help Wanted`, `Domain: check: Control Flow`)

**\`asserts\` keyword does not enhance hoisted function type, works on functions assigned to a variable**

*The 'asserts' type predicate fails to refine hoisted function types but works on functions assigned to variables.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5.4 years ago](https://github.com/microsoft/TypeScript/issues/41232#issuecomment-724847848) **denismaxim0v** said "I think I could look into it"
 * **RyanCavanaugh** added label `Domain: Control Flow`
 * [later](https://github.com/microsoft/TypeScript/issues/41232#issuecomment-4186696712) **denis-migdal** provided information about using anonymous functions and classes to leverage name inference and noted the limitation of using implements

### [Issue microsoft/TypeScript#45319](https://github.com/microsoft/TypeScript/issues/45319) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add some way to specify a different output shebang**

*Allow specifying a different shebang in TypeScript source to apply to the compiled JavaScript output.*

 * **RyanCavanaugh** added label `Suggestion`
 * [4 years ago](https://github.com/microsoft/TypeScript/issues/45319#issuecomment-1081457164) **StringManolo** suggested using a `// @ts-shebang` directive as shorthand for the full shebang and offered a script to replace it in source files
 * [3.1 years ago](https://github.com/microsoft/TypeScript/issues/45319#issuecomment-1413040169) **Lioness100** said "I think this would be very useful :)"
 * [later](https://github.com/microsoft/TypeScript/issues/45319#issuecomment-4187066007) **Andrej730** asked what the typical workaround was for using a TypeScript bin entry locally via pnpm link and a JavaScript dist file for end users

### [Issue microsoft/TypeScript#62207](https://github.com/microsoft/TypeScript/issues/62207) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**, **Copilot**)

**Deprecate, remove support for \`baseUrl\`**

*TypeScript 6.0 will deprecate baseUrl support and require explicit prefixes in paths mappings.*

 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-3398112747) **andrewbranch** said "extends does not merge paths values. They are always fully overridden."
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-3398660496) **oliviertassinari** stated that extends merged paths correctly and identified the issue as paths resolution
 * [24 weeks ago](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-3398783245) **andrewbranch** explained that relative paths in tsconfig ‘paths’ are always resolved to the defining file, described past unintended behavior when a base config defined ‘paths’ and extending configs defined ‘baseUrl’, and noted that the ts5to6 migration tool can handle this automatically
 * [later](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4187144985) **ArfanFahad** reported having a persistent warning and a watcher compilation failure after applying IntelliSense fix
 * [later](https://github.com/microsoft/TypeScript/issues/62207#issuecomment-4187271405) **jakebailey** said "There's no problem. This is very intentional. Remove that option."

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * **RyanCavanaugh** added label `Domain: LS: TSServer`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3961671540) **Arlen22** said "Ok, this doesn't happen in every project, so it might be more on the typescript side of things. "
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3985103294) **Arlen22** described being unable to rename generic type parameters in one part of the project and expressed confusion about an underlying dependency or type issue
 * [later](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4187180248) **Arlen22** described that intellisense broke whenever opening JavaScript or TypeScript files outside the project and mentioned a workaround using a separate workspace

### [PR microsoft/TypeScript#63344](https://github.com/microsoft/TypeScript/pull/63344) (Closed)

**Document charCodeAt edge case behavior in first line**

*Update charCodeAt JSDoc to mention NaN return edge case in the main description line.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180926787) **jakebailey** said "Just do npm test, it'll do everything for you in the right order."
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4180995565) **bwalter007** reported that running npm test still yielded an ENOENT error before tests ran and asked if something was missing in the local setup
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4181033803) **RyanCavanaugh** said "I don't know what's going on; never heard of this happening before. Even after running git clean -xdf, npm ci + npm test is sufficient on my machine."
 * [later](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4186769595) **bwalter007** identified that a colon in the directory path caused the issue, renamed the directory, updated the baseline, and pushed the changes
 * [later](https://github.com/microsoft/TypeScript/pull/63344#issuecomment-4186769782) **bwalter007** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63347](https://github.com/microsoft/TypeScript/issues/63347) (Closed, `Not a Defect`)

**Minor performance issue when using HTMLElementTagNameMap**

*TypeScript 6.0’s overload resolution for HTMLElementTagNameMap has regressed, causing slower type-checking and minor performance issues on Linux*

 * created by **jasonlyu123**
 * [today](https://github.com/microsoft/TypeScript/issues/63347#issuecomment-4184232102) **RyanCavanaugh** identified the originating commit as a DOM update and explained that the performance cost increase was due to larger map entries and properties per element rather than a checker defect
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63347#issuecomment-4186205019) **jasonlyu123** analyzed commit-induced performance regression, noted difference in isInstantiation comparison and symbol id assignment, identified stricter baseline timing in TS6, and concluded it was a preexisting performance issue triggered by DOM updates

### [Issue microsoft/TypeScript#63348](https://github.com/microsoft/TypeScript/issues/63348) (Closed, `Working as Intended`)

**Inference is not working properly**

*TypeScript fails to infer the path generic type in useStoreByPath from its string argument.*

 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184005631) **eduardocque** asked if there was a way to avoid duplicating the generic value in the function signature and if they needed to rethink their solution or propose an alternative
 * [today](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184054209) **RyanCavanaugh** mentioned suggestion was tracked at issue #26242 and asked where style was coming from
 * [today](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184066053) **eduardocque** asked whether TypeScript could infer the second generic for the useStoreByPath function from the first generic and function parameters
 * [today](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184115596) **RyanCavanaugh** provided a standard workaround using a curried function with TypeScript generics
 * [today](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184124618) **eduardocque** asked if a change request or suggestion could be made without breaking TypeScript generics
 * [today](https://github.com/microsoft/TypeScript/issues/63348#issuecomment-4184174580) **MartinJohns** noted that the relevant issue #26242 had already been linked

### [Issue microsoft/TypeScript#63349](https://github.com/microsoft/TypeScript/issues/63349) (Closed)

**Merging type only \`namespace\` and \`const\` in module declaration**

*Request for a TypeScript module declaration that merges a default-exported value and augmentable type-only namespace without breaking LSP*

 * created by **Aylur**

