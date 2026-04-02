# Report for 2025-11-29 (Saturday, November 29th, 2025)

4 different users commented on 4 different issues.

## Recommended Actions

 * Response Recommended
    * @PaulRBerg suggested adding support for targeted TS file checking in AI agents in [microsoft/TypeScript#27379](https://github.com/microsoft/TypeScript/issues/27379#issuecomment-3592411655)
    * @topce suggested closing the issue and provided a PR and workaround in [microsoft/TypeScript#598](https://github.com/microsoft/TypeScript/issues/598#issuecomment-3591943628)

## Activity Summary

### [Issue microsoft/TypeScript#27379](https://github.com/microsoft/TypeScript/issues/27379) (Open, `Suggestion`, `In Discussion`)

**Allow tsconfig\.json when input files are specified**

*Enable tsconfig.json when input files are specified with --project or -p, with CLI options overriding and include/exclude ignored.*

 * [44 weeks ago](https://github.com/microsoft/TypeScript/issues/27379#issuecomment-2613823947) **lolmaus** asked how VS Code handled running tsc on individual files
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/27379#issuecomment-3116544324) **toppsdown** expressed confusion about tsc ignoring tsconfig and reported errors when running tsc on a Next.js file
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/27379#issuecomment-3120790150) **richardkmichael** described a workaround for debugging a single file by replacing include with files in tsconfig
 * [later](https://github.com/microsoft/TypeScript/issues/27379#issuecomment-3592411655) **PaulRBerg** described AI coding agent use case and requested targeted TypeScript file linting to avoid token waste
 * [later](https://github.com/microsoft/TypeScript/issues/27379#issuecomment-3592437374) **alveifbklsiu259** recommended tscw-config for running tsc against specific files while respecting tsconfig.json

### [PR microsoft/TypeScript#53017](https://github.com/microsoft/TypeScript/pull/53017) (Open, `For Backlog Bug`, **ahejlsberg**)

**Infer type parameters from indexes on those parameters**

*Infer generic type parameters in TypeScript based on index accesses of those parameters.*

 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591696488) **typescript-bot** reported user test results comparing main and pull merge, noted an infrastructure git clone failure and new TS2345 type errors in webpack configs
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591710203) **typescript-bot** provided the requested performance run results comparing baseline to the PR
 * [today](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591733538) **typescript-bot** provided comparative tsc results for top 400 repos, highlighted build failures in react-navigation/react-navigation, and requested a review
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3592607394) **Andarist** provided repro examples with react-hook-form and TS playground links

### [Issue microsoft/TypeScript#598](https://github.com/microsoft/TypeScript/issues/598) (Open, `Suggestion`, `Help Wanted`)

**Don't allow falsely discarded parameters when determining overloaded signature compatibility**

*Ensure overload resolution respects parameter count by disallowing silently discarded parameters during signature compatibility checks.*

 * (6.7 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/598#issuecomment-1200139567) **shevchenkobn** proposed an algorithm for function type inheritance using an extends-based overload matching approach
 * [today](https://github.com/microsoft/TypeScript/issues/598#issuecomment-3591943628) **topce** argued that enabling the feature would catch the error, referenced a PR and a Windows ts-go fix, and suggested closing the issue as Knockout is no longer used and the behavior is by design

### [Issue microsoft/TypeScript#62802](https://github.com/microsoft/TypeScript/issues/62802) (Closed)

**Const type parameters may resolve into non\-const types when iterating over \`Record\<string, \(\) =\> void\>\` parameter**

*TypeScript const type parameters resolve into non-const types when iterating over Record<string, () => TReturnType>, breaking literal type inference.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62802#issuecomment-3580423210) **Andarist** provided a final solution link in TS playground
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62802#issuecomment-3582954819) **sanniassin** summarized type info loss when inferring types within conditional types for function parameters, illustrated the issue with code examples, and proposed workarounds to preserve parent type information
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62802#issuecomment-3585813663) **Andarist** explained that the issue was purely informational and described how TypeScript’s inference relies on pattern matching with type variables in conditional branches, clarified why return types aren’t part of that inference and suggested limited documentation usefulness
 * (today) **sanniassin** closed the issue

