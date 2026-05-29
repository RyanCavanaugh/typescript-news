# Report for 2026-05-27 (Wednesday, May 27th, 2026)

8 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @vrjordant asked if something needs to be done before merging in [microsoft/TypeScript#63064](https://github.com/microsoft/TypeScript/pull/63064#issuecomment-4557603112)

## Activity Summary

### [PR microsoft/TypeScript#63064](https://github.com/microsoft/TypeScript/pull/63064) (Open, `For Backlog Bug`)

**fix\(lib\): reorder Array\#reduce/reduceRight overloads in lib\.d\.ts**

*Reorder Array#reduce and reduceRight overloads in lib.d.ts to prioritize the generic initialValue overload and fix type inference*

 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/63064#issuecomment-4121939849) **RyanCavanaugh** said "@typescript-bot test it"
 * [9 weeks ago](https://github.com/microsoft/TypeScript/pull/63064#issuecomment-4121940094) **typescript-bot** said "Hey @RyanCavanaugh, this PR is in an unmergable state, so is missing a merge commit to run against; please resolve conflicts and try again."
 * **RyanCavanaugh** added to milestone `Post-7.0 lib candidates`
 * [today](https://github.com/microsoft/TypeScript/pull/63064#issuecomment-4557603112) **vrjordant** said "Is there something that needs to be done before this can be merged?"

### [PR microsoft/TypeScript#63508](https://github.com/microsoft/TypeScript/pull/63508) (Open, `For Backlog Bug`)

**Add missing JSDoc to ReadonlySet and ReadonlyMap members**

*Add JSDoc comments to ReadonlySet and ReadonlyMap methods to match their mutable counterparts.*

 * [today](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4556218663) **TxsharDev** said "@microsoft-github-policy-service agree"
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4559385934) **MartinJohns** said "Why another one? There's already #63483 and #63488. Seems to be done by AI."
 * [today](https://github.com/microsoft/TypeScript/pull/63508#issuecomment-4559644821) **TxsharDev** thanked MartinJohns, noted that #63488 was closed and #63483 only covered ReadonlySet, added JSDoc to ReadonlyMap methods to fill the same documentation gap, offered to remove the ReadonlySet portion if maintainers preferred, and clarified that the JSDoc was hand-written rather than AI-generated

### [PR microsoft/TypeScript#63509](https://github.com/microsoft/TypeScript/pull/63509) (Closed, `For Uncommitted Bug`)

**Add missing JSDoc parameter and return type tags to esnext lib files**

*Add missing JSDoc parameter and return tags to various esnext library declaration files.*

 * created by **Se3do**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63509#issuecomment-4559874594) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63509#issuecomment-4559874600) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **Se3do** closed the issue

### [Issue microsoft/TypeScript#63510](https://github.com/microsoft/TypeScript/issues/63510) (Closed, `AI Spam`)

**TypeScript compiler incorrectly reports duplicate identifiers for types and variables**

*TypeScript incorrectly flags user-defined types and variables as duplicate identifiers when they collide with built-in names.*

 * created by **sulthonzh**
 * [today](https://github.com/microsoft/TypeScript/issues/63510#issuecomment-4560487720) **MartinJohns** explained that there was no built-in Event type and suggested using `noLib` to exclude standard declaration files
 * [later](https://github.com/microsoft/TypeScript/issues/63510#issuecomment-4565283139) **mkantor** explained that the errors occurred because the code was in global scope and suggested adding imports, exports, or forcing moduleDetection to avoid them

### [Issue microsoft/TypeScript#63511](https://github.com/microsoft/TypeScript/issues/63511) (Closed)

**Contextual narrowing fails inside thunked argument when T is inferred from a separate argument**

*TypeScript fails to contextually narrow array literals in thunked callbacks when inferring generic T from another parameter.*

 * created by **johanrd**
 * [later](https://github.com/microsoft/TypeScript/issues/63511#issuecomment-4561792114) **MartinJohns** said "Duplicate of #241."
 * [later](https://github.com/microsoft/TypeScript/issues/63511#issuecomment-4562647363) **johanrd** said "@MartinJohns thanks"
 * (later) **johanrd** closed the issue

### [Issue microsoft/TypeScript#63512](https://github.com/microsoft/TypeScript/issues/63512) (Open)

**Missing JSDoc annotations in esnext lib declaration files**

*ESNext lib declaration files are missing JSDoc @param and @returns annotations, undermining IntelliSense documentation consistency.*

 * created by **Se3do**

### [PR microsoft/TypeScript#63513](https://github.com/microsoft/TypeScript/pull/63513) (Open, `For Uncommitted Bug`)

**Add missing JSDoc param and returns tags to lib\.d\.ts esnext files**

*Add missing JSDoc @param and @returns annotations to esnext lib.d.ts APIs including Error.isError, Date.toTemporalInstant, Atomics.pause, Map/WeakMap getOrInsert, Array.fromAsync, and Uint8Array.fromHex.*

 * created by **Se3do**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63513#issuecomment-4562709948) **Se3do** said "@microsoft-github-policy-service agree"

