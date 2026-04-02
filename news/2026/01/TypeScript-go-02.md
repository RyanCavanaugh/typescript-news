# Report for 2026-01-02 (Friday, January 2nd, 2026)

6 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @fabian-hiller provided context and a hypothesis about the slowdown cause in [microsoft/TypeScript-go#2384](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3706542883)

## Activity Summary

### [Issue microsoft/TypeScript-go#2384](https://github.com/microsoft/TypeScript-go/issues/2384) (Open)

**slow Code Completion with use valibot schema define**

*TypeScript code completion becomes significantly slow when using Valibot to define large schemas.*

 * created by **wszgrcy**
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3672562862) **ahejlsberg** explained that parse trees and binding information are cached but types are recomputed on every change, described the high cost of inferring types for a 4000-line expression, provided performance metrics comparing old and new compilers, and concluded that reducing compute is the only way to improve speed
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3672670301) **wszgrcy** thanked the maintainer, provided a link to the type file, and asked for modification suggestions to reduce type computation costs
 * [today](https://github.com/microsoft/TypeScript-go/issues/2384#issuecomment-3706542883) **fabian-hiller** suggested that the pipe function's 20 overload signatures may be causing the slowdown due to missing generic-related optimizations and provided a simplified example signature

### [PR microsoft/TypeScript-go#2390](https://github.com/microsoft/TypeScript-go/pull/2390) (Open)

**New auto\-import infrastructure**

*Redesigns TypeScript's auto-import collection infrastructure to support snapshot-based LSP, parallelized data collection, and improved caching.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3677629801) **alexandr2110pro** suggested checking a linked repo that reproduces autocompletion and autoimport issues in an Nx monorepo
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3685967528) **jansedlon** said "This looks solid. I'm wondering why is the difference in subsequent completion so small between TS and Go implementation. Do you think the gap widens with project size?"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3686389797) **rubnogueira** reported that upgrading to the latest master broke auto-imports and related features in their pnpm mono/polyrepo, requiring a revert, and said they looked forward to testing the fixes when time permitted
 * [today](https://github.com/microsoft/TypeScript-go/pull/2390#issuecomment-3705657539) **andrewbranch** expressed uncertainty about why the performance difference was small, noted how fast TS-based completions were, mentioned opportunities to optimize Go completions, and removed all profile hot spots for the auto-import path

### [Issue microsoft/TypeScript-go#2430](https://github.com/microsoft/TypeScript-go/issues/2430) (Closed, `Domain: Editor`)

**C\# language server stopped working after switching to \.ts file with tsgo enabled**

*Enabling tsgo in a VS Code ASP.NET MVC project breaks C# language server’s go-to-definition and reference features.*

 * created by **bjoerni79**
 * **bjoerni79** added label `Domain: Editor`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/2430#issuecomment-3697359931) **DanielRosenwasser** said "Can you elaborate a bit more on what isn't working? Are you using this from a Razor template or something?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2430#issuecomment-3706927676) **bjoerni79** apologized for the delay and stated intent to retest with the new version later

### [PR microsoft/TypeScript-go#2434](https://github.com/microsoft/TypeScript-go/pull/2434) (Open)

**Experiment: Quantified Types**

*Looking for a TypeScript typing approach to consume a heterogeneous array of Layer objects without collapsing types into a union.*

 * created by **devanshj**
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3700061096) **gabritto** said "This seems like a duplicate of https://github.com/microsoft/TypeScript/issues/14466."
 * [3 days ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3700068875) **devanshj** acknowledged forgetting to link the existing issue and noted that the PR implements a quantified type
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705759875) **Andarist** suggested using reverse mapped types to implement the consumeLayers example and recommended choosing a different motivating example while acknowledging the idea's interest
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705776547) **devanshj** noted that reverse mapped types simplified the example, provided a motivating code snippet, and said they would further refine the PR
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705823991) **Andarist** suggested using reverse mapped types from two TypeScript PRs and provided a playground example
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705842553) **devanshj** said "Yeah I think in theory you could pull it off with reverse mapped types and with some enhancements in the checker but then quantified types are nicer to read/understand... so I'm a bit biased haha"

### [Issue microsoft/TypeScript-go#2437](https://github.com/microsoft/TypeScript-go/issues/2437) (Open, `Domain: Editor`)

**TSGo prioritizes \`tsconfig\.json\` over \`jsconfig\.json\` in the same directory, even for file types the former excludes**

*When both config files reside in the same directory, TSGo always prioritizes tsconfig.json over jsconfig.json, disabling JavaScript type checking.*

 * created by **Bertie690**
 * **Bertie690** added label `Domain: Editor`

