# Report for 2026-05-21 (Thursday, May 21st, 2026)

11 different users commented on 22 different issues.

## Recommended Actions

 * Response Recommended
    * @jet2jet reported a crash in getResolvedSignature due to resolveNodeHandle mismatch in [microsoft/TypeScript-go#3938](https://github.com/microsoft/TypeScript-go/issues/3938#issuecomment-4518938609)

## Activity Summary

### [Issue microsoft/TypeScript-go#3655](https://github.com/microsoft/TypeScript-go/issues/3655) (Closed, `Needs Investigation`, **iisaduan**)

**Behavior difference: Pattern matching against \`extends { \[P in K\]?: unknown }\` emit slightly different error in tsgo**

*tsgo inconsistently expands mapped type constraint { [P in K]?: unknown } in generics, causing different errors than tsc*

 * (2 weeks ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.0 RC`, and assigned to **iisaduan**
 * [today](https://github.com/microsoft/TypeScript-go/issues/3655#issuecomment-4511888096) **iisaduan** agreed with Anders and explained that using `[P in "a"]` can be harder to comprehend when the iterated type is complex, leading to verbose expansions that are hard to interpret at a glance
 * (today) **iisaduan** closed the issue

### [Issue microsoft/TypeScript-go#3724](https://github.com/microsoft/TypeScript-go/issues/3724) (Closed, `wontfix`, **ahejlsberg**)

**Behavior difference: tsgo fails to typecheck self\-referential identity in a classic linked list**

*tsgo reports an implicit any error for a self-referential node property in a JavaScript linked list that TypeScript 6 accepts.*

 * **ahejlsberg** added label `wontfix`
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3724#issuecomment-4394184138) **hkleungai** described how adding a callback-based update method allowed tsgo to infer types correctly and contrasted this behavior with a similar issue regarding self-references in the same scope
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/issues/3724#issuecomment-4394209685) **hkleungai** mentioned that while type annotations are necessary, they’d prefer to rely on tsgo’s type inference to minimize annotations
 * [today](https://github.com/microsoft/TypeScript-go/issues/3724#issuecomment-4510832188) **ahejlsberg** described TS6 rules for determining the declared type of a `this.xxx` assignment declared property, including constructor control flow analysis, JSDoc annotations, union of assigned types, handling of self-referential assignments, and noted the change from TS7
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript-go#3747](https://github.com/microsoft/TypeScript-go/issues/3747) (Closed)

**Regression in 20260506\.1: generic substitution lost through method\-returned mapped type**

*tsgo CLI in version 7.0.0-dev.20260506.1 incorrectly loses generic substitutions for method-returned mapped types, defaulting to constraint defaults.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4455298605) **RyanCavanaugh** asked to disable skipLibCheck to confirm and explained a declaration emit bug with a minimal repro and conditions
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4455324118) **RyanCavanaugh** verified that the issue was fixed in 7.0.0-dev.20260514.1 and requested confirmation from Apollon77
 * (1 week ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/3747#issuecomment-4518177360) **Apollon77** said "Yes I verified it fixing my issue. Thanks a lot!"

### [Issue microsoft/TypeScript-go#3787](https://github.com/microsoft/TypeScript-go/issues/3787) (Closed, `Needs More Info`)

**tsgo and tsc diverge on incomplete composite\-ref declaration cache: TS2305 vs filterable TS6305**

*tsgo reports TS2305 errors instead of TS6305 missing-declaration errors when the composite declaration cache is incomplete.*

 * created by **XavierGeerinck**
 * **RyanCavanaugh** added label `Needs More Info`
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/3787#issuecomment-4454473597) **RyanCavanaugh** requested a concrete repro and explained that TS6305 is advisory for misconfigurations and not for build scheduling; recommended build tools analyze the project graph themselves
 * [today](https://github.com/microsoft/TypeScript-go/issues/3787#issuecomment-4511071037) **RyanCavanaugh** said "Closing; please open a fresh issue if there's a repro available. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript-go#3806](https://github.com/microsoft/TypeScript-go/issues/3806) (Closed, `Needs More Info`)

**Intermittent \`TS2307\` on directory imports — \`tsc\` passes, \`tsgo\` intermittently fails on the same tree**

*tsgo intermittently throws TS2307 for parent-directory imports using package.json main with bundler resolution, while tsc passes reliably.*

 * created by **Akshay090**
 * **RyanCavanaugh** added label `Needs More Info`
 * [6 days ago](https://github.com/microsoft/TypeScript-go/issues/3806#issuecomment-4464392347) **RyanCavanaugh** said "If you can confirm repro on latest we can try another round of synthesizing a repro, or if you can come up with a concrete repro that'd be great."
 * [today](https://github.com/microsoft/TypeScript-go/issues/3806#issuecomment-4511072704) **RyanCavanaugh** said "Closing; please open a fresh issue if there's a repro available. Thanks!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#3882](https://github.com/microsoft/TypeScript-go/pull/3882) (Closed)

**feat: unused identifier**

*The implementation of the unused identifier codefix (and other individual codefixes) has not been ported.*

 * created by **a-tarasyuk**
 * (today) **a-tarasyuk** closed the issue

### [Issue microsoft/TypeScript-go#3938](https://github.com/microsoft/TypeScript-go/issues/3938) (Open, `Needs Investigation`, **andrewbranch**)

**Result of getTypeOfLocation for \`PropertyAccessExpression\` and \`ElementAccessExpression\` may be different between 6 and 7**

*Parenthesized and nested property accesses yield incorrect object types in tsgo v7’s getTypeAtLocation compared to TypeScript 6.*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3938#issuecomment-4518938609) **jet2jet** described a bug where resolveNodeHandle in session.go returned an unexpected node instance and caused getResolvedSignature to crash for CallExpressions with PropertyAccessExpressions, and provided a stack trace

### [PR microsoft/TypeScript-go#3949](https://github.com/microsoft/TypeScript-go/pull/3949) (Closed)

**feat: completion snippets**

*Implement code completion snippets to enable quick insertion of commonly used code patterns*

 * created by **a-tarasyuk**
 * (today) **a-tarasyuk** closed the issue

### [Issue microsoft/TypeScript-go#4005](https://github.com/microsoft/TypeScript-go/issues/4005) (Open, `Domain: Editor`, `Needs More Info`)

**Native Preview returns no code actions for any TS diagnostic**

*TypeScript native preview on Remote-SSH shows diagnostics but no code actions for TS errors when using tsgo.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4005#issuecomment-4502555182) **RyanCavanaugh** noted that TS7 lacked the full suite of code actions and requested feedback to prioritize which ones to re-implement
 * **RyanCavanaugh** added label `Needs More Info`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/4005#issuecomment-4502684407) **a-tarasyuk** said "It could be useful, for instance, if VS Code tracked which quick fixes are used most often (if any 😄 )."
 * [today](https://github.com/microsoft/TypeScript-go/issues/4005#issuecomment-4511225902) **umbriquse** mentioned using the auto-import feature frequently and referenced a similar issue (#3318), noting that another user reported right-click auto-import worked for him
 * [today](https://github.com/microsoft/TypeScript-go/issues/4005#issuecomment-4513748304) **DanielRosenwasser** described that auto-import worked via auto-completion and code actions and invited filing separate issues for regressions

### [PR microsoft/TypeScript-go#4006](https://github.com/microsoft/TypeScript-go/pull/4006) (Closed)

**Bump fast\-uri to 3\.1\.2**

*Upgrade fast-uri to 3.1.2 to address high-severity CVE-2026-6321 and CVE-2026-6322*

 * created by **lucygramley**
 * (today) **lucygramley** closed the issue

### [Issue microsoft/TypeScript-go#4011](https://github.com/microsoft/TypeScript-go/issues/4011) (Open, `bug`, **weswigham**)

**Property names from JSDoc types not escaped in declaration files**

*Declaration files generated by tsgo fail to quote hyphenated JSDoc property names, leading to syntax errors.*

 * (yesterday) **RyanCavanaugh** set milestone to `TypeScript 7.0 RC`, and assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** assigned to **weswigham**, and unassigned **RyanCavanaugh**, **Copilot**

### [Issue microsoft/TypeScript-go#4014](https://github.com/microsoft/TypeScript-go/issues/4014) (Open, `Domain: Declaration Emit`, `Domain: Build Mode`, `Needs More Info`, `Needs Investigation`)

**\`DeepCloneNode\` allocation runaway \(44 GB / 308 s\) for recursive tagged\-tuple type alias**

*tsgo’s DeepCloneNode allocation spikes (44 GB over 308 s) when type-checking a recursive variadic tuple alias with a .tsbuildinfo file.*

 * created by **ebramanti**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4014#issuecomment-4510993141) **weswigham** speculated that a bug in type stringification affected incremental builds, suggested a change from issue #4024, and asked if it helped
 * (today) **weswigham** added labels `Domain: Declaration Emit`, `Domain: Build Mode`, `Needs More Info`, `Needs Investigation`

### [Issue microsoft/TypeScript-go#4016](https://github.com/microsoft/TypeScript-go/issues/4016) (Closed)

**@fileoverview breaks @jsx comments**

*tsgo does not honor @jsx annotations in @fileoverview comments, using the default JSX factory instead of the specified one.*

 * created by **blickly**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4020](https://github.com/microsoft/TypeScript-go/pull/4020) (Closed)

**fix\(4016\): skip unknown pragmas**

*Modify the parser to skip unrecognized pragmas instead of producing errors.*

 * created by **a-tarasyuk**
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript-go#4021](https://github.com/microsoft/TypeScript-go/pull/4021) (Closed)

**Rewrite invalid identifiers originating in JSDoc**

*Add sanitization helpers to the declaration transformer to rewrite invalid JSDoc identifiers and property names into valid TypeScript keys.*

 * created by **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4021#issuecomment-4510349097) **weswigham** suggested handling non-identifier @param and @typedef names upfront in the reparser by coercing or escaping them and quoting @property names
 * [today](https://github.com/microsoft/TypeScript-go/pull/4021#issuecomment-4510375899) **weswigham** said "Also: linked issue seems wrong?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4021#issuecomment-4510403236) **RyanCavanaugh** said "Should have been #4011, thanks for the hallucination Copilot"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4021#issuecomment-4510414945) **RyanCavanaugh** questioned whether coercing non-identifier names into identifiers was safe, noting they could still be referenced via x["some-name"] depending on the declaration type
 * [today](https://github.com/microsoft/TypeScript-go/pull/4021#issuecomment-4510473232) **weswigham** explained that @param tags can’t be referred to so renaming them is safe, noted that only @typedefs would be functional, showed an example with a kebab-case typedef, and suggested that the typedef case should be treated as an error
 * [today](https://github.com/microsoft/TypeScript-go/pull/4021#issuecomment-4510502920) **weswigham** suggested refusing to bind non-identifier typedefs/callbacks, renaming non-identifier @param declarations, and quoting non-identifier @property members during reparsing
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4022](https://github.com/microsoft/TypeScript-go/pull/4022) (Closed)

**Fix external helper crash after module\-status updates \(TDD rewrite\)**

*Disallow file reuse when external or CommonJS module indicators change to prevent nil-pointer crashes of external helpers.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4023](https://github.com/microsoft/TypeScript-go/pull/4023) (Open)

**TDD Rewrite Subagent**

*Implement a subagent mode to automatically re-execute pull requests with questionable test reliability.*

 * created by **RyanCavanaugh**

### [PR microsoft/TypeScript-go#4024](https://github.com/microsoft/TypeScript-go/pull/4024) (Open)

**Allow nil\-ing out arenas to break the GC link between nodes and the arena they came from**

*Allow arenas to be nilled out to sever GC links between nodes and their originating arenas, reducing diagnostic memory retention.*

 * created by **weswigham**

### [PR microsoft/TypeScript-go#4025](https://github.com/microsoft/TypeScript-go/pull/4025) (Closed, **RyanCavanaugh**, **Copilot**)

**Normalize \`\.github/agents/pr\-cleanup\.md\` to LF\-only line endings**

*Convert .github/agents/pr-cleanup.md to LF-only line endings for consistent formatting and reduced diff noise.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript-go#4026](https://github.com/microsoft/TypeScript-go/pull/4026) (Open)

**Rebuilt CLI watcher around new \`fswatch\` package**

*CLI watch functionality was rebuilt using the fswatch package, cutting idle CPU usage from ~5% to under 1%.*

 * created by **johnfav03**

### [PR microsoft/TypeScript-go#4027](https://github.com/microsoft/TypeScript-go/pull/4027) (Open, `dependencies`, `javascript`)

**Bump @nevware21/ts\-utils from 0\.13\.0 to 0\.14\.0**

*Upgrade the @nevware21/ts-utils dependency from 0.13.0 to 0.14.0, adding various new array, string, and type inspection helper functions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`

