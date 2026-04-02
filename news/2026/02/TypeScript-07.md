# Report for 2026-02-07 (Saturday, February 7th, 2026)

10 different users commented on 8 different issues.

## Activity Summary

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3863766950) **justingrant** thanked maintainers for landing Temporal types, noted original type contributions, apologized for late review, reported a small type mistake, asked why @bakkot’s suggestion for property bag constraints didn’t work, and asked for recommendations on polyfill compatibility
 * [yesterday](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3863884548) **DanielRosenwasser** thanked justingrant and others for reviewing Temporal, discussed whether polyfill declaration files should be integrated into lib.d.ts, reflected on differing declaration patterns and his oversight in not seeking feedback, and mentioned plans to ship the 6.0 beta soon and address differences thereafter
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3864504776) **Renegade334** asked why bakkot's suggestion didn't work and explained that using type aliases in lib.d.ts hinders forward extensibility, then discussed potential workarounds
 * [today](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3865491719) **justingrant** expressed support for TS integrating Temporal and suggested contributing polyfill declaration types to lib.d.ts for compatibility, citing existing Temporal TS types and recommending tagging proposal champions

### [PR microsoft/TypeScript#63084](https://github.com/microsoft/TypeScript/pull/63084) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Add \-\-stableTypeOrdering for TS7 ordering compat**

*Add a hidden --stableTypeOrdering flag that enables TS7’s deterministic type, symbol, and node ordering algorithm for tsgo-port compatibility.*

 * [3 days ago](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3849927246) **typescript-bot** provided an installable tgz link and instructions for testing by referencing it in package.json and running npm install
 * (yesterday) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3864394113) **robpalme** said "Is it reasonable pre-migration approach to try to first make existing codebases work with and without this flag?"
 * [today](https://github.com/microsoft/TypeScript/pull/63084#issuecomment-3864762468) **jakebailey** said "Yes, though this flag causes a pretty significant slowdown. The blog post will explain better."

### [Issue microsoft/TypeScript#63105](https://github.com/microsoft/TypeScript/issues/63105) (Closed)

**Exposing local types in an ambient module's declare module fails**

*Re-exporting a local interface in a declare module leads to imported properties being typed as any instead of string.*

 * created by **hgl**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63105#issuecomment-3851373515) **SyedAdeel00** explained that ambient .d.ts files without top-level imports or exports are treated as global ambient modules causing imported types to become any and that adding export {} converts it into a proper module preserving type information; noted the same pattern in DefinitelyTyped
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63105#issuecomment-3851392739) **hgl** explained that the export {} workaround failed due to a Typescript 'foo was also declared here' error
 * [later](https://github.com/microsoft/TypeScript/issues/63105#issuecomment-3867087257) **hgl** said "This is expected behavior."
 * (later) **hgl** closed the issue

### [Issue microsoft/TypeScript#63112](https://github.com/microsoft/TypeScript/issues/63112) (Open)

**Infer works differently for interface and type alias**

*TypeScript infer in conditional types correctly matches index signatures on type aliases but fails for interfaces.*

 * created by **UnVuTWFu**
 * [today](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864623797) **mkantor** explained that the issue was a direct consequence of implicit index signatures not existing on interfaces (per issue #15300) and suggested adding an explicit index signature to fix the code
 * [today](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864688383) **UnVuTWFu** described wanting to pass a generic type and extract specific types via conditional types, noted interface returned never while type alias worked
 * [today](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864767667) **mkantor** asked if the provided code snippet matched the requirements
 * [today](https://github.com/microsoft/TypeScript/issues/63112#issuecomment-3864946734) **MartinJohns** stated that it compiled just fine

### [PR microsoft/TypeScript#63113](https://github.com/microsoft/TypeScript/pull/63113) (Closed, `For Backlog Bug`)

**Fix \#13948: preserve narrow types for computed property keys with union literal types**

*Computed property keys with union literal types now distribute over each member, preserving narrow types instead of widening to string.*

 * created by **DukeDeSouth**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63113#issuecomment-3866215466) **DukeDeSouth** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63113#issuecomment-3867024821) **mkantor** questioned why the change was desirable given it would typecheck code that causes a runtime error and suggested the type should be a union

### [Issue microsoft/TypeScript#63114](https://github.com/microsoft/TypeScript/issues/63114) (Open)

**No autocomplete suggestions for object property values within type arguments**

*TypeScript 5.9.3 fails to show autocomplete suggestions for string literal object property values used as generic type arguments.*

 * created by **jedwards1211**
 * [today](https://github.com/microsoft/TypeScript/issues/63114#issuecomment-3865154812) **mkantor** noted that the issue was fixed in v6.0.0-dev.20260204 by PR #62170

### [Issue microsoft/TypeScript#63115](https://github.com/microsoft/TypeScript/issues/63115) (Open)

**Support loading remote types**

*Enable TypeScript to load remote type definitions in config files via URLs, removing the need for type-only dependencies.*

 * created by **danciudev**

### [PR microsoft/TypeScript#63116](https://github.com/microsoft/TypeScript/pull/63116) (Open, `For Uncommitted Bug`)

**Free \`preProgram\` early in the test harness**

*Freeing preProgram memory early in the test harness to prevent out-of-memory errors when running the full program.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63116#issuecomment-3867403340) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

