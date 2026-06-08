# Report for 2026-06-04 (Thursday, June 4th, 2026)

9 different users commented on 23 different issues.

## Recommended Actions

 * Response Recommended
    * @lygstate asked if the bug could be fixed in [microsoft/TypeScript#35909](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-4626919034)
    * @Ijtihed provided CLA agreement in [microsoft/TypeScript#63535](https://github.com/microsoft/TypeScript/pull/63535#issuecomment-4629413532)
    * @dxbjavid offered to open a tracking issue for triage in [microsoft/TypeScript#63536](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4630294013)

## Activity Summary

### [Issue microsoft/TypeScript#35909](https://github.com/microsoft/TypeScript/issues/35909) (Open, `Suggestion`, `Awaiting More Feedback`)

**Can't evaluate equality of symbols made by Symbol\.for**

*TypeScript treats Symbol.for calls as distinct types, causing erroneous type errors on equality comparisons and assignments.*

 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-1012984992) **cowboyd** agreed with nicolo-ribaudo, suggested type syntax for Symbol and Symbol.for(), and asked why the thread had petered out and what could be done
 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-1159692746) **pjeby** described a use case for interop using Symbol.for() and explained TypeScript's limitation without global symbol syntax
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-2585209754) **yuhr** reposted an excerpt from issue #60944 explaining the use-case for non-unique symbol keys to support multiple library versions and the compile-time issues with string keys
 * [today](https://github.com/microsoft/TypeScript/issues/35909#issuecomment-4626919034) **lygstate** said "It's a bug, can it fixed? As Symbol.for("literal") basically act like "literal" with symbol attribute"

### [Issue microsoft/TypeScript#59653](https://github.com/microsoft/TypeScript/issues/59653) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Number\.prototype\.toFixed, Number\.prototype\.toExponential,Number\.prototype\.toPrecision comments error**

*The lib/es5.d.ts comments for Number.prototype.toFixed, toExponential, and toPrecision list incorrect parameter ranges.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/59653#issuecomment-2295503200) **purple-force** said "Since this definition is used by later version es spec and many developers don't know the history, maybe following the spec is  a better choice?"
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62707](https://github.com/microsoft/TypeScript/issues/62707) (Open, `Bug`, `Help Wanted`, `Domain: Parser`)

**TS1508: Unexpected '?'\. Did you mean to escape it with backslash? shouldn't report even with \`v\` flag**

*TypeScript wrongly reports TS1508 for unescaped '?' in regex character classes when using the v flag.*

 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/62707#issuecomment-3479986144) **Andarist** provided a patch diff to fix the incorrectly reported character and noted that the other issue required further investigation
 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/62707#issuecomment-3484170740) **graphemecluster** noted that three lines were unnecessary and provided a diff to remove them
 * **RyanCavanaugh** added label `Domain: Parser`
 * [later](https://github.com/microsoft/TypeScript/issues/62707#issuecomment-4629401261) **Ijtihed** said "I fixed lone & handling in /v character classes and added a  compiler regression test for it asw. "

### [Issue microsoft/TypeScript#63514](https://github.com/microsoft/TypeScript/issues/63514) (Closed, `Not a Defect`)

**Reassigning of inferred \`object\` with Indexed access value does not widen it's type**

*Reassigning an inferred object via indexed access in TypeScript fails to widen its type beyond object.*

 * [6 days ago](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4577403452) **nmain** explained that the `never` type contains no values, thus satisfies all predicates, and that asserting a value as `never` implies unreachable code
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4605191004) **RyanCavanaugh** explained that never must always be a valid keyof object using logical arguments
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/63514#issuecomment-4627426140) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63516](https://github.com/microsoft/TypeScript/pull/63516) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Update toFixed/toExponential/toPrecision digit range in docs to match the spec**

*Update Number.prototype.toFixed, toExponential, and toPrecision documentation to reflect the ES2018 spec’s increased digit limits of 0–100 and 1–100.*

 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * (yesterday) **RyanCavanaugh** closed the issue
 * (yesterday) **RyanCavanaugh** reopened the issue
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63523](https://github.com/microsoft/TypeScript/issues/63523) (Closed, `Working as Intended`)

**tsc may fail to report error when \`file\.js\` & \`file\.d\.ts\` coexist, even when \`@ts\-check\` is added on \`file\.js\`\.**

*After TypeScript 4.5 update, JavaScript files with @ts-check ignore errors if a corresponding .d.ts file is present.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4592123266) **hkleungai** noted skipLibCheck was enabled but the bug persisted, questioned that .d.ts files took priority over .js files, and suggested documentation clarification, highlighting a tsc ordering inconsistency
 * **RyanCavanaugh** added label `Working as Intended`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4605129005) **RyanCavanaugh** noted that automatically ingesting both would cause duplicate identifier errors and suggested it was a configuration error
 * [today](https://github.com/microsoft/TypeScript/issues/63523#issuecomment-4627426281) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63525](https://github.com/microsoft/TypeScript/pull/63525) (Closed, `For Uncommitted Bug`)

**Fix JSDoc grammar typo: 'returns a undefined' → 'returns undefined'**

*Grammar typo corrected in JSDoc for SymbolConstructor.keyFor by changing '@returns a undefined' to '@returns undefined'*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4599055199) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (2 days ago) **RyanCavanaugh** closed the issue
 * (2 days ago) **RyanCavanaugh** reopened the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63525#issuecomment-4625580688) **RyanCavanaugh** said "@driphtyio need CLA sign before we can merge this"

### [Issue microsoft/TypeScript#63527](https://github.com/microsoft/TypeScript/issues/63527) (Closed, `Needs Investigation`, **ahejlsberg**)

**\`erasableSyntaxOnly\` should error on unerasable \`as\`/\`satisfies\`**

*ErasableSyntaxOnly should report errors for as or satisfies expressions that cannot be safely removed.*

 * **RyanCavanaugh** added label `Needs Investigation`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4606483396) **RyanCavanaugh** summarized key takeaways about erasableSyntaxOnly, questioned shipped precedence rules, and proposed testing top1000 code to determine if a precedence error could be introduced in TS 7.0
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4615276410) **ahejlsberg** explained that only operators with lower or equal precedence can follow `as` or `satisfies`, provided an example, and proposed a PR to stop parsing at unexpected higher-precedence operators
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63531](https://github.com/microsoft/TypeScript/issues/63531) (Closed, `Help Wanted`, `Docs`)

**Markdown heading level bug in Narrowing documentation**

*The 'Truthiness narrowing' heading in the TypeScript Narrowing documentation is formatted as H1 instead of H2, causing subsequent sections to be incorrectly nested under it in the table of contents.*

 * created by **mzleman**
 * [today](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4620530645) **MartinJohns** showed a screenshot of the bottom of the page
 * (today) **RyanCavanaugh** added labels `Help Wanted`, `Docs`
 * [today](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4625038495) **RyanCavanaugh** said "Weird, the accessibility scan is supposed to yell at us when this happens"
 * [later](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4630156658) **MannXo** said "I'll take this if no one's working on it yet."
 * [later](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4630477675) **MartinJohns** said "@MannXo There are already open PR to address this issue. Generally, the TypeScript team does not assign issues to users. You're free to just work on issues labelled as "Help wanted" and issue PRs."

### [Issue microsoft/TypeScript#63532](https://github.com/microsoft/TypeScript/issues/63532) (Closed, `Suggestion`, `Out of Scope`)

**Runtime\-safe type casts and checks for TypeScript\.**

*Request native TypeScript runtime-safe type assertions and checks to replace error-prone 'as unknown as' casts.*

 * created by **matthiasrieger**
 * [today](https://github.com/microsoft/TypeScript/issues/63532#issuecomment-4621176028) **MartinJohns** said "Runtime type checking has been requested many times before, but is explicitly out of scope. Check the viability checklist again."
 * [today](https://github.com/microsoft/TypeScript/issues/63532#issuecomment-4621840415) **snarbles2** clarified that this isn't a runtime feature and suggested TypeBox or ArkType as libraries that might provide the functionality
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Out of Scope`
 * [today](https://github.com/microsoft/TypeScript/issues/63532#issuecomment-4625032016) **RyanCavanaugh** noted that the request was out of scope according to the checklist
 * (today) **RyanCavanaugh** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63532#issuecomment-4625496694) **matthiasrieger** encouraged the contributor to implement it without emitting different JS based on expression types
 * [today](https://github.com/microsoft/TypeScript/issues/63532#issuecomment-4625533232) **matthiasrieger** clarified that runtime is in the name, suggested using TypeBox or ArkType, and noted that without transpilation boilerplate is required

### [Issue microsoft/TypeScript#63533](https://github.com/microsoft/TypeScript/issues/63533) (Open, `Design Notes`)

**Design Meeting Notes, 2026\-06\-04**

*Ban unparenthesized type assertions and satisfies with binary operators under erasableSyntaxOnly to preserve source maps and prevent ambiguous precedence.*

 * created by **RyanCavanaugh**
 * **RyanCavanaugh** added label `Design Notes`

### [Issue microsoft/TypeScript#63534](https://github.com/microsoft/TypeScript/issues/63534) (Closed, `Duplicate`)

**TypeScript incorrectly reports literal comparison error inside class method after state mutation**

*TypeScript incorrectly infers this.n as 0 within the first conditional and flags a false-positive comparison to 1 after mutation.*

 * created by **mcube-12139**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63534#issuecomment-4626922086) **RyanCavanaugh** said "#9998"
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#63535](https://github.com/microsoft/TypeScript/pull/63535) (Closed, `For Backlog Bug`)

**Allow lone ampersands in Unicode sets regex classes**

*Enable lone ampersands in Unicode set regex character classes while retaining && as the intersection operator.*

 * created by **Ijtihed**
 * **typescript-bot** added label `For Backlog Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63535#issuecomment-4629413532) **Ijtihed** agreed to the Contributor License Agreement using the microsoft-github-policy-service command

### [PR microsoft/TypeScript#63536](https://github.com/microsoft/TypeScript/pull/63536) (Closed, `For Uncommitted Bug`, `Voight-Kampff Anomaly`)

**fix catastrophic backtracking in jquery typesMap rule**

*Replace the nested digit quantifier in the jQuery typesMap regex with a linear pattern to prevent catastrophic backtracking.*

 * created by **dxbjavid**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4630189689) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4630189730) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4630294013) **dxbjavid** explained the regex performance issue, provided benchmark timings, and offered to open a tracking issue
 * [later](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4630607045) **jakebailey** stated they didn't plan to fix this now and noted it wasn't an issue in the new language server
 * [later](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4631652211) **dxbjavid** acknowledged that the Go server uses RE2, agreed there was no backtracking issue, and consented to leave the JS language service as-is
 * [later](https://github.com/microsoft/TypeScript/pull/63536#issuecomment-4633060366) **jakebailey** said "It's not that, but that it doesn't uses regexes for this at all"
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`

