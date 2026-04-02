# Report for 2026-02-28 (Saturday, February 28th, 2026)

6 different users commented on 8 different issues.

## Activity Summary

### [PR microsoft/TypeScript#63155](https://github.com/microsoft/TypeScript/pull/63155) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.3\.2 to 5\.3\.6**

*Update fast-xml-parser to v5.3.6 to enhance entity processing security and performance*

 * **dependabot[bot]** added label `javascript`
 * (1 week ago) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63155#issuecomment-3977930454) **dependabot[bot]** said "Superseded by #63204."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#63190](https://github.com/microsoft/TypeScript/pull/63190) (Closed, `For Uncommitted Bug`)

**discrete pluralizer for lib\.esnext\.temporal unit unions**

*Restrict DateUnit and TimeUnit unions to singular names and use a pluralizer helper for js-temporal compatibility.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3961773716) **Renegade334** said "Comme ça ?"
 * (3 days ago) **jakebailey** closed the issue
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3975598199) **DanielRosenwasser** asked what the long-term best practice is for handling singular vs plural unit references
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3979239031) **MartinJohns** deemed adding overly generic names like PluralizeUnit weird in the global namespace due to its limited use case
 * [today](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3979269904) **jakebailey** said "This is the Temporal namespace, no?"

### [Issue microsoft/TypeScript#63191](https://github.com/microsoft/TypeScript/issues/63191) (Closed, `Suggestion`, `Declined`)

**The "?" operator would be forbidden before the "\!" operator**

*Request to disallow combining optional chaining (?) with non-null assertion (!) in TypeScript to prevent unsafe undefined values.*

 * (3 days ago) **RyanCavanaugh** added labels `Suggestion`, `Declined`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3968828854) **jcalz** said "Also see #34875 and #35025 "
 * [today](https://github.com/microsoft/TypeScript/issues/63191#issuecomment-3978814967) **typescript-bot** said "This issue has been marked as "Declined" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63199](https://github.com/microsoft/TypeScript/issues/63199) (Open)

**Crash: TypeError: Cannot read properties of undefined \(reading 'aliasSymbol'\) remains when using variadic tuple with \(infer C\)\[\] and constrained infer**

*TypeScript compiler throws a TypeError reading 'aliasSymbol' when inferring variadic tuple types with a constrained infer array.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3974139578) **RyanCavanaugh** said "Crashes in TS7 as well"
 * [today](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977102585) **Andarist** said "Im pretty sure https://github.com/microsoft/TypeScript/pull/63014 fixes this and this issue is a duplicate of https://github.com/microsoft/TypeScript/issues/63005"
 * [today](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977198462) **na7ure-a** thanked the maintainer, tested the fix locally, confirmed the crash in #63005 was resolved but that the issue’s code snippet still crashed, and asked to test with the exact code from the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63199#issuecomment-3977724475) **Andarist** apologized for misunderstanding and pushed a fix for the missing cases to the PR

### [Issue microsoft/TypeScript#63203](https://github.com/microsoft/TypeScript/issues/63203) (Open, `Suggestion`, `Awaiting More Feedback`)

**Narrow a ternary expression to unique symbol type**

*Enable TypeScript to infer a unique symbol type from a ternary expression whose runtime result is constant.*

 * created by **mitar**
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3977064991) **guillaumebrunerie** asked whether libraries depending on global state might break during Vite development and whether this is a Vite bug or a misunderstanding
 * [today](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3977083251) **mitar** explained that Vite optimized imports during development by duplicating and bundling them together, causing symbol identity mismatches when the same module was imported via different absolute or relative paths
 * [later](https://github.com/microsoft/TypeScript/issues/63203#issuecomment-3979903350) **mkantor** suggested using Symbol.for("none") unconditionally and asked if memory cost was a concern, then proposed a workaround switching symbols based on NODE_ENV

### [PR microsoft/TypeScript#63204](https://github.com/microsoft/TypeScript/pull/63204) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.3\.2 to 5\.3\.8**

*Upgrade fast-xml-parser dependency from v5.3.2 to v5.3.8 incorporating improved entity security, performance, XML builder support, and CJS typing fixes.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * **typescript-bot** added label `For Uncommitted Bug`

