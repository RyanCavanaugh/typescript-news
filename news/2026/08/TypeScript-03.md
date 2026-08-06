# Report for 2026-08-03 (Monday, August 3rd, 2026)

6 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @miami-man asked whether this issue had been resolved in [microsoft/TypeScript#50466](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-5172407186)
    * @OldStarchy asked why identical functions are treated differently by the engine in [microsoft/TypeScript#63715](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5176324777)

## Activity Summary

### [Issue microsoft/TypeScript#50466](https://github.com/microsoft/TypeScript/issues/50466) (Open, `Needs Investigation`, **weswigham**)

**NodeNext resolution failed to resolve dual\-package correctly**

*NodeNext resolution incorrectly resolves a dual-package by selecting the CommonJS export instead of the type definitions, causing a TS2349 error.*

 * [3.7 years ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-1313095401) **aleclarson** suggested that TypeScript should warn when a `types` condition existed alongside both MJS and CJS entry points because it wasn't a valid solution
 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-1346916117) **justinhelmer** described adding dual package exports solution for TypeScript including package.json and tsconfig configurations and the requirement of separate *.d.cts files for CJS consumers
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-1880582216) **kerambit** mentioned encountering the same problem, referenced a linked solution, and noted that consumer code must use CJS although docs recommend nodenext
 * [today](https://github.com/microsoft/TypeScript/issues/50466#issuecomment-5172407186) **miami-man** said "Has this been resolved yet? I've been using a command line tool to automate this process for a few years now, so have lost track of status. "

### [Issue microsoft/TypeScript#63710](https://github.com/microsoft/TypeScript/issues/63710) (Open, `Domain: lib.d.ts`, `Possible Improvement`)

**\`ReadonlyMap\` lacks documentation for \`forEach\`, \`get\`, \`has\` and \`size\`**

*Document ReadonlyMap’s forEach, get, has, and size members in lib.es2015.collection.d.ts to match Map<K,V>.*

 * created by **KimMaru10**
 * (today) **RyanCavanaugh** added labels `Possible Improvement`, `Domain: lib.d.ts`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63711](https://github.com/microsoft/TypeScript/pull/63711) (Open, `For Backlog Bug`)

**docs: add JSDoc comments to ReadonlyMap interface**

*Add JSDoc comments for ReadonlyMap methods forEach, get, has, and size in lib.es2015.collection.d.ts for consistency with Map*

 * created by **KimMaru10**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63713](https://github.com/microsoft/TypeScript/pull/63713) (Closed, `For Backlog Bug`)

**Fix parameter property modifier followed by newline \(fixes \#28396\)**

*Allow constructor parameter property modifiers followed by a newline before the parameter name to be correctly recognized.*

 * (today) **typescript-automation[bot]** added labels `For Backlog Bug`, `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63713#issuecomment-5168441321) **Abhirup0** agreed to the Contributor License Agreement using the microsoft-github-policy-service
 * [later](https://github.com/microsoft/TypeScript/pull/63713#issuecomment-5176479082) **MartinJohns** said "@Abhirup0 You should read this: https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md#notes-on-contributing"
 * [later](https://github.com/microsoft/TypeScript/pull/63713#issuecomment-5176562134) **Abhirup0** thanked @MartinJohns and updated the PR description to include the AI assistance disclosure
 * [later](https://github.com/microsoft/TypeScript/pull/63713#issuecomment-5177565337) **MartinJohns** clarified that all code changes should be submitted to the microsoft/typescript-go repository and noted this repository no longer accepts non-critical changes
 * [later](https://github.com/microsoft/TypeScript/pull/63713#issuecomment-5178141961) **Abhirup0** acknowledged the explanation and said they would close the PR and port the fix to typescript-go
 * (later) **Abhirup0** closed the issue

### [Issue microsoft/TypeScript#63714](https://github.com/microsoft/TypeScript/issues/63714) (Open, `Design Limitation`, **RyanCavanaugh**, **Copilot**)

**Typescript still checks return type in a lamba that calls a function returning 'never'**

*TypeScript lambda with declared number return type errors for missing return when calling a never-returning method.*

 * created by **kwasimensah**
 * [today](https://github.com/microsoft/TypeScript/issues/63714#issuecomment-5173766276) **MartinJohns** explained that the behavior matched the specification from issue #32695, detailing the conditions for assertion or never-returning calls
 * [later](https://github.com/microsoft/TypeScript/issues/63714#issuecomment-5179477257) **jcalz** explained how to ensure control flow analysis by explicitly typing the impl variable and provided a code example

### [Issue microsoft/TypeScript#63715](https://github.com/microsoft/TypeScript/issues/63715) (Open, `Duplicate`)

**Implicitly typed type guard does not guard**

*TypeScript does not narrow union types when a never-returning guard function is implicitly typed as () => void, unlike when explicitly typed as () => never.*

 * created by **OldStarchy**
 * [today](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5175347329) **MartinJohns** explained that the behavior matched the specification from issue #32695, detailing the conditions for assertion or never-returning calls
 * [later](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5176324777) **OldStarchy** suggested that the issue may differ because bail always throws rather than being an asserts type guard and proposed raising a feature/change request since identical functions are treated differently by the engine
 * [later](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5176403750) **MartinJohns** clarified that bail always throws, explained the limitation is intentional for performance reasons, and noted the examples did not meet the explicit type naming requirement
 * [later](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5176541355) **OldStarchy** noted the complexity of type inference, suggested supporting never-returning methods for simpler use cases, and provided a code example with a workaround
 * [later](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5177240623) **MartinJohns** reiterated that they didn’t know the details and pointed to related issues, noted the team’s awareness of the restriction and suggested that Ryan address it when labeling or closing the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63715#issuecomment-5179494056) **jcalz** said "As a feature request, this would duplicate #45385 (which is a good read for people who run into this situation)."

