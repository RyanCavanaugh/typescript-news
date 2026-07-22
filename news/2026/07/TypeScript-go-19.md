# Report for 2026-07-19 (Sunday, July 19th, 2026)

10 different users commented on 18 different issues.

## Recommended Actions

 * Response Recommended
    * @zuyetawarmatik provided repro steps and link as requested in [microsoft/TypeScript-go#4580](https://github.com/microsoft/TypeScript-go/issues/4580#issuecomment-5019588142)

## Activity Summary

### [PR microsoft/TypeScript-go#4556](https://github.com/microsoft/TypeScript-go/pull/4556) (Closed, **andrewbranch**, **Copilot**)

**Add getConstraint\(\) and getDefault\(\) getters to TypeParameter**

*Add asynchronous getConstraint() and getDefault() methods to the TypeParameter API for direct retrieval of type parameter constraints and defaults*

 * created by **Copilot**
 * (1 week ago) **Copilot** assigned to **Copilot**, **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4556#issuecomment-5024026965) **Copilot** reworked both endpoints to follow the getTrueType/getFalseType pattern, removed fetchCheckerType helper, updated server-side functions, and adjusted fetchType return behavior

### [Issue microsoft/TypeScript-go#4580](https://github.com/microsoft/TypeScript-go/issues/4580) (Closed, `Domain: Editor`)

**TS7 plugin is not working with Yarn 4 nodeLinker = pnp**

*TS7’s VSCode plugin and compiler fail to work with Yarn 4 PnP due to missing tsserver and inaccessible cached archives.*

 * **zuyetawarmatik** added label `Domain: Editor`
 * **RyanCavanaugh** added to milestone `Need More Info`
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/4580#issuecomment-5007287838) **RyanCavanaugh** said ""uses Yarn 4" is not enough info to go on - we really need a concrete repro to investigate."
 * [later](https://github.com/microsoft/TypeScript-go/issues/4580#issuecomment-5019588142) **zuyetawarmatik** provided a reproduction repository link and steps causing a typecheck failure

### [PR microsoft/TypeScript-go#4615](https://github.com/microsoft/TypeScript-go/pull/4615) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 3 updates**

*Upgrade the root GitHub CodeQL Actions by bumping init to v4.37.0 and updating autobuild and analyze.*

 * (6 days ago) **dependabot[bot]** added labels `github_actions`, `dependencies`, `github_actions`
 * [later](https://github.com/microsoft/TypeScript-go/pull/4615#issuecomment-5021294781) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (later) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript-go#4646](https://github.com/microsoft/TypeScript-go/pull/4646) (Open, `Voight-Kampff Anomaly`)

**Fix hover documentation for intersected properties**

*Enhance TypeScript hover tooltips for intersection properties by aggregating JSDoc from all declarations.*

 * created by **cuishuang**
 * [4 days ago](https://github.com/microsoft/TypeScript-go/pull/4646#issuecomment-4979689386) **Andarist** said "this issue is already being fixed by my older PR: https://github.com/microsoft/typescript-go/pull/3663"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

### [Issue microsoft/TypeScript-go#4675](https://github.com/microsoft/TypeScript-go/issues/4675) (Open, `Domain: Editor`)

**Cursor jumps to the line above after accepting an inline completion that adds an auto\-import**

*Accepting a quick suggestion inline completion that triggers an auto-import causes the cursor to jump one line above instead of remaining on the current line.*

 * created by **svipas**
 * **svipas** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#4676](https://github.com/microsoft/TypeScript-go/pull/4676) (Open)

**Fix parsing of \`as\`/\`satisfies\` between \`\*\*\` operators**

*Account for right-associative exponentiation when rejecting unsafe as/satisfies expressions and add regression coverage.*

 * created by **magic-akari**

### [Issue microsoft/TypeScript-go#4677](https://github.com/microsoft/TypeScript-go/issues/4677) (Open, `Domain: Editor`)

**JSDoc \(TSDoc ???\) is not shown for object literal properties on hover**

*In TypeScript 7, VS Code stops displaying JSDoc comments on hover for const object literal properties, losing per-property documentation.*

 * created by **nazmul-nhb**
 * **nazmul-nhb** added label `Domain: Editor`

### [Issue microsoft/TypeScript-go#4678](https://github.com/microsoft/TypeScript-go/issues/4678) (Open, `Working As Intended`, **RyanCavanaugh**, **Copilot**)

**skipLibCheck doesn't suppress TS2320 "cannot simultaneously extend" for module augmentation of a \`\.d\.ts\` interface \(repro has no any\)**

*skipLibCheck:true does not suppress TS2320 cannot simultaneously extend errors during module augmentation of a .d.ts interface.*

 * created by **valentinmelusson**

### [PR microsoft/TypeScript-go#4679](https://github.com/microsoft/TypeScript-go/pull/4679) (Open, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 4 updates**

*Upgrade actions/setup-node to v7.0.0 and bump CodeQL init, autobuild, and analyze actions in root directory.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [Issue microsoft/TypeScript-go#4680](https://github.com/microsoft/TypeScript-go/issues/4680) (Open, `Needs More Info`)

**TS7030 "not all code paths return a value" false positive when a never\-returning exhaustiveness helper is called \(not returned\) in a switch default**

*tsgo wrongly reports not all code paths return for a switch default that calls a never-returning exhaustiveness helper*

 * created by **valentinmelusson**

### [Issue microsoft/TypeScript-go#4681](https://github.com/microsoft/TypeScript-go/issues/4681) (Open, `duplicate`)

**skipLibCheck doesn't suppress TS18042/TS2693 when a \.d\.ts's own export = points to a type instead of a value**

*skipLibCheck does not prevent tsgo from reporting TS18042 and TS2693 errors when a .d.ts file’s export= incorrectly refers to a type instead of a value.*

 * created by **valentinmelusson**

### [PR microsoft/TypeScript-go#4682](https://github.com/microsoft/TypeScript-go/pull/4682) (Open)

**\[api\] Always update inferred project if one is open**

*Automatically refresh an open inferred project when its contents change without requiring new file openings.*

 * created by **piotrtomiak**

### [Issue microsoft/TypeScript-go#4683](https://github.com/microsoft/TypeScript-go/issues/4683) (Closed, `duplicate`, **ahejlsberg**)

**Generic type parameter inferred differently across two call\-site positions with opposite variance \(narrow type vs union\)**

*TypeScript infers D from the columns as MetricWithCardinality rather than the union type when passing data to Table.*

 * created by **valentinmelusson**

### [Issue microsoft/TypeScript-go#4684](https://github.com/microsoft/TypeScript-go/issues/4684) (Closed, `Domain: Editor`)

**VS Code extension does not provide completions for directive comments**

*VS Code extension does not support completions for TypeScript directive comments such as @ts-expect-error.*

 * created by **mrazauskas**
 * **mrazauskas** added label `Domain: Editor`

### [PR microsoft/TypeScript-go#4685](https://github.com/microsoft/TypeScript-go/pull/4685) (Open)

**fix\(4677\): preserve JSDoc for mapped type properties in hover**

*Ensure JSDoc comments for mapped type properties are retained and displayed in hover tooltips.*

 * created by **a-tarasyuk**

