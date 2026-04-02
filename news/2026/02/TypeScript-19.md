# Report for 2026-02-19 (Thursday, February 19th, 2026)

8 different users commented on 16 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#63157](https://github.com/microsoft/TypeScript/issues/63157) (Closed)

**Extension required when moduleResolution=bundler and imports/exports used**

*TypeScript with bundler module resolution fails to resolve package imports via imports/exports mappings without .js extensions.*

 * created by **polson136**
 * [today](https://github.com/microsoft/TypeScript/issues/63157#issuecomment-3928556520) **polson136** said "I accidentally used the wrong issue template. Closing this issue and creating another issue here: https://github.com/microsoft/TypeScript/issues/63162"
 * (today) **polson136** closed the issue

### [Issue microsoft/TypeScript#63160](https://github.com/microsoft/TypeScript/issues/63160) (Open, `Duplicate`)

**Inferring from setter returns getter value**

*TypeScript's conditional type inference picks the getter's return type instead of the setter's parameter type.*

 * created by **LukeAbby**
 * [today](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3926391137) **MartinJohns** said "Duplicate of #62943."
 * [today](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3928849152) **LukeAbby** clarified that issue #62943 had been closed as a duplicate of #60162, #43729, and #60954, none involving infer, and noted that #60162 suggested adding a new intrinsic for dynamic props
 * [today](https://github.com/microsoft/TypeScript/issues/63160#issuecomment-3928911901) **MartinJohns** clarified that the first issue involved infer and was marked as a duplicate by a team member

### [Issue microsoft/TypeScript#63162](https://github.com/microsoft/TypeScript/issues/63162) (Closed, `Duplicate`)

**Module resolution: Extension required when moduleResolution=bundler and imports/exports used**

*TypeScript's bundler moduleResolution requires explicit .js extensions for imports and exports, causing build-time failures despite working in Vite.*

 * created by **polson136**

### [PR microsoft/TypeScript#63163](https://github.com/microsoft/TypeScript/pull/63163) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Port anyFunctionType subtype fix and JSX children NonInferrableType propagation from typescript\-go**

*Port fixes from typescript-go to make anyFunctionType a proper function subtype and correctly propagate NonInferrableType for JSX children.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930743569) **DanielRosenwasser** said "@typescript-bot test this"
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930743738) **typescript-bot** posted CI job status update with links to build start and result pages
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930788438) **typescript-bot** alerted that the DT test run failed and asked to check the logs
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930826766) **jakebailey** said "@typescript-bot run dt"
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930827028) **typescript-bot** started CI jobs and posted a status table
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930830569) **typescript-bot** ran user tests comparing main and the PR merge, noted one unrelated "Git clone failed" infrastructure failure and reported that everything else looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930882621) **typescript-bot** informed that the DT test run failed and linked to the log
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930957509) **typescript-bot** provided the requested performance run results
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930984285) **typescript-bot** provided benchmark results for the top 400 repos and reported that everything looked good

### [Issue microsoft/TypeScript#63164](https://github.com/microsoft/TypeScript/issues/63164) (Closed)

**Crash Fix for Issue \#63094**

*Fixes a crash caused by a debug failure when resolving overloaded decorators with the --experimentalDecorators flag.*

 * created by **umarfarooq478**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63165](https://github.com/microsoft/TypeScript/issues/63165) (Closed)

**Crash Fix for Issue \#63090**

*Resolve a RangeError caused by maximum call stack size exceeded during serialization of recursive distributive mapped types.*

 * created by **umarfarooq478**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63166](https://github.com/microsoft/TypeScript/issues/63166) (Closed)

**Crash Fix for Issue \#63050**

*Referencing a variable with a union of string literal types from an ambient declaration produces duplicate error messages and crashes the compiler.*

 * created by **umarfarooq478**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63167](https://github.com/microsoft/TypeScript/issues/63167) (Closed)

**Fix for Regression in Issue \#63019**

*A regression in TypeScript 4.2 makes generic functions returning unioned tuples unassignable to identical types.*

 * created by **umarfarooq478**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63168](https://github.com/microsoft/TypeScript/issues/63168) (Closed)

**Fix for Issue \#63094**

*Resolving overloaded decorators with the --experimentalDecorators flag causes a Debug Failure crash.*

 * created by **umarfarooq478**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63169](https://github.com/microsoft/TypeScript/issues/63169) (Closed)

**Fix for Issue \#63090**

*The compiler crashes with a stack overflow when serializing recursive distributive mapped types.*

 * created by **umarfarooq478**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63170](https://github.com/microsoft/TypeScript/issues/63170) (Closed)

**Fix for Issue \#63050**

*Prevent double error reporting when accessing variables with union string literal types in ambient declarations.*

 * created by **umarfarooq478**
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63171](https://github.com/microsoft/TypeScript/issues/63171) (Closed)

**Fix for Issue \#63019**

*TypeScript 4.2 introduced a regression preventing generic functions returning tuple unions from being assigned to identical types.*

 * created by **umarfarooq478**
 * (later) **jakebailey** closed the issue

