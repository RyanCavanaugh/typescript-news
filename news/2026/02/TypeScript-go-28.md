# Report for 2026-02-28 (Saturday, February 28th, 2026)

3 different users commented on 3 different issues.

## Recommended Actions

 * Response Recommended
    * @wadjoh provided repro steps and test results as requested in [microsoft/TypeScript-go#2935](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3978651671)

## Activity Summary

### [Issue microsoft/TypeScript-go#2935](https://github.com/microsoft/TypeScript-go/issues/2935) (Closed, `Crash`, **ahejlsberg**, **jakebailey**, **Copilot**)

**Stack overflow in type instantiation with recursive function and generic type params**

*A recursive generic camelCase transformation using type-fest triggers a tsgo stack overflow from v4.38.0 onward, while tsc compiles it.*

 * created by **wadjoh**
 * **wadjoh** added label `Crash`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3976721921) **apendua** said "A fun fact, this crash does not seem to occur with the latest version of type-fest (i.e. ^5.0.0), but I was able to confirm that it breaks for ^4.0.0."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3978398912) **wadjoh** narrowed down the issue to type-fest 4.38.0 due to PR 1081, observed it stops crashing at version 5.0.0, and said they would update the issue description
 * [today](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3978488787) **jakebailey** said "Also try TS 6.0 with --stableTypeOrdering."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2935#issuecomment-3978651671) **wadjoh** provided a 3-line example with type-fest@4.38.0, updated the initial description, and confirmed that TS 6.0.0-beta with --stableTypeOrdering still compiled successfully
 * (today) **jakebailey** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2940](https://github.com/microsoft/TypeScript-go/pull/2940) (Closed, **jakebailey**, **Copilot**)

**Fix stack overflow in type relation checking with recursive generic types**

*TypeScript’s recursive generic type checking causes unbounded recursion and stack overflow, mitigated by a compiler-level depth counter.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **jakebailey**

### [PR microsoft/TypeScript-go#2941](https://github.com/microsoft/TypeScript-go/pull/2941) (Closed)

**Remove and simplify code related to allowSyntheticDefaultImports/esModuleInterop**

*Remove and simplify allowSyntheticDefaultImports and esModuleInterop code paths now always enabled and error when false.*

 * created by **jakebailey**

