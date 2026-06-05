# Report for 2026-06-03 (Wednesday, June 3rd, 2026)

8 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @glebbash proposed solutions for allowing optional chaining on unknown types and requested reconsideration in [microsoft/TypeScript#37700](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-4617038844)
    * @mariusGundersen provided additional runtime support information in [microsoft/TypeScript#42219](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-4619886824)

## Activity Summary

### [Issue microsoft/TypeScript#23405](https://github.com/microsoft/TypeScript/issues/23405) (Open, `Suggestion`, `Committed`, `Domain: JSDoc`, `Domain: JavaScript`)

**Support a @nonnull/@nonnullable JSDoc assertion comment**

*Enable @nonnull/@nonnullable JSDoc tags to assert non-null values as an alternative to the non-null assertion operator.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/23405#issuecomment-2864099138) **mhofman** said "Losing inference and having to be explicit about the type is IMO not sufficiently ergonomic."
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/23405#issuecomment-2864430422) **SethFalco** asked for elaboration on inference concerns and argued that his proposal preserved inference and preferred JSDoc ergonomics over TypeScript-specific syntax
 * [52 weeks ago](https://github.com/microsoft/TypeScript/issues/23405#issuecomment-2925585653) **aweebit** suggested abusing JSDoc's @type tag to introduce a non-nullable syntax
 * [today](https://github.com/microsoft/TypeScript/issues/23405#issuecomment-4616091456) **NemoStein** described a workaround for class property initialization issues in JSDoc and proposed using a '!string' syntax

### [Issue microsoft/TypeScript#37700](https://github.com/microsoft/TypeScript/issues/37700) (Closed, `Suggestion`, `Declined`)

**Optional chaining of unknown should be unknown**

*Allow optional chaining on values with unknown type, yielding unknown result instead of a type error.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3884461544) **grundb** acknowledged that the helper function was heavy-handed but handled the common case of chaining unknown values
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3884491782) **adrian-gierakowski** provided a TypeScript implementation of an optionalChain function with a recursive GetPath type and demonstrated its behavior through various usage examples
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-3884786810) **mfulton26** said "https://github.com/sindresorhus/dot-prop can be used to "get, set, or delete a property from a nested object using a dot path [or an array path]" that will return undefined for nonexistent paths."
 * [today](https://github.com/microsoft/TypeScript/issues/37700#issuecomment-4617038844) **glebbash** explained that current strictness forces unsafe type-casting and illustrated three JavaScript scenarios where optional chaining on unknown is painful, then proposed solutions like a 'dynamic' type or a compiler flag

### [Issue microsoft/TypeScript#42219](https://github.com/microsoft/TypeScript/issues/42219) (Open, `Suggestion`, `Awaiting More Feedback`)

**\[Feature\] Import non\-js content as const string**

*Enable importing non-JS file content as const string with compile-time TypeScript types via import.meta.content.*

 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-1400486580) **nsaunders** supported the idea and described a CSS workaround using a `*.css.ts` module with build tool extraction, syntax highlighting and Prettier limitations, and linked a demo project
 * [20 weeks ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-3732822567) **valler** said "This should be compatible with type stripping, so it should be a JS feature really. The request is not so much about typing, but to reduce the need for custom loaders and/or intermediary build steps."
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-4177548196) **linusg** mentioned that importing modules as plain text was being standardized in TC39 via import attributes and linked to the stage 3 proposal
 * [later](https://github.com/microsoft/TypeScript/issues/42219#issuecomment-4619886824) **mariusGundersen** noted that importing as text is now supported in Bun, Deno, and Firefox Nightly and linked a blog post

### [Issue microsoft/TypeScript#63192](https://github.com/microsoft/TypeScript/issues/63192) (Closed, `Bug`, `Domain: check: Type Circularity`)

**RangeError: Maximum call stack size exceeded when trying to infer type of a variable reassigned in a loop**

*TypeScript crashes with a maximum call stack size exceeded error when inferring types for a variable reassigned in a loop.*

 * (13 weeks ago) **RyanCavanaugh** added labels `Bug`, `Domain: check: Type Circularity`, and set milestone to `Backlog`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63430](https://github.com/microsoft/TypeScript/issues/63430) (Open, `Needs Investigation`, **andrewbranch**)

**Paths from tsconfig are not used if declaration is on a different partition**

*TypeScript ignores tsconfig path mappings for imports on a different drive when emitting declaration files, producing absolute paths.*

 * (2 weeks ago) **RyanCavanaugh** set milestone to `Backlog`, and assigned to **andrewbranch**
 * **typescript-bot** added label `Fix Available`
 * **andrewbranch** removed label `Fix Available`

### [PR microsoft/TypeScript#63516](https://github.com/microsoft/TypeScript/pull/63516) (Closed, `For Backlog Bug`, `Voight-Kampff Anomaly`)

**Update toFixed/toExponential/toPrecision digit range in docs to match the spec**

*Update Number.prototype.toFixed, toExponential, and toPrecision documentation to reflect the ES2018 spec’s increased digit limits of 0–100 and 1–100.*

 * created by **ibondarenko1**
 * **typescript-bot** added label `For Backlog Bug`
 * **RyanCavanaugh** added label `Voight-Kampff Anomaly`
 * (today) **RyanCavanaugh** closed the issue
 * (today) **RyanCavanaugh** reopened the issue

### [Issue microsoft/TypeScript#63527](https://github.com/microsoft/TypeScript/issues/63527) (Closed, `Needs Investigation`, **ahejlsberg**)

**\`erasableSyntaxOnly\` should error on unerasable \`as\`/\`satisfies\`**

*ErasableSyntaxOnly should report errors for as or satisfies expressions that cannot be safely removed.*

 * (yesterday) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4606483396) **RyanCavanaugh** summarized key takeaways about erasableSyntaxOnly, questioned shipped precedence rules, and proposed testing top1000 code to determine if a precedence error could be introduced in TS 7.0
 * [today](https://github.com/microsoft/TypeScript/issues/63527#issuecomment-4615276410) **ahejlsberg** explained that only operators with lower or equal precedence can follow `as` or `satisfies`, provided an example, and proposed a PR to stop parsing at unexpected higher-precedence operators

### [Issue microsoft/TypeScript#63531](https://github.com/microsoft/TypeScript/issues/63531) (Open, `Help Wanted`, `Docs`)

**Markdown heading level bug in Narrowing documentation**

*The 'Truthiness narrowing' heading in the TypeScript Narrowing documentation is formatted as H1 instead of H2, causing subsequent sections to be incorrectly nested under it in the table of contents.*

 * created by **mzleman**
 * [later](https://github.com/microsoft/TypeScript/issues/63531#issuecomment-4620530645) **MartinJohns** showed a screenshot of the bottom of the page

### [Issue microsoft/TypeScript#63532](https://github.com/microsoft/TypeScript/issues/63532) (Closed, `Suggestion`, `Out of Scope`)

**Runtime\-safe type casts and checks for TypeScript\.**

*Request native TypeScript runtime-safe type assertions and checks to replace error-prone 'as unknown as' casts.*

 * created by **matthiasrieger**
 * [later](https://github.com/microsoft/TypeScript/issues/63532#issuecomment-4621176028) **MartinJohns** said "Runtime type checking has been requested many times before, but is explicitly out of scope. Check the viability checklist again."
 * [later](https://github.com/microsoft/TypeScript/issues/63532#issuecomment-4621840415) **snarbles2** clarified that this isn't a runtime feature and suggested TypeBox or ArkType as libraries that might provide the functionality

