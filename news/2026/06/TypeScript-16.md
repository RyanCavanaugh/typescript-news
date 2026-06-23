# Report for 2026-06-16 (Tuesday, June 16th, 2026)

11 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @nmain asked why the defaults are any on Generator<> and Iterable<> but unknown on IteratorObject<> in [microsoft/TypeScript#63561](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4729759859)
    * @rtritto asked if the issue would still be rejected in [microsoft/TypeScript#63564](https://github.com/microsoft/TypeScript/issues/63564#issuecomment-4730245004)

## Activity Summary

### [Issue microsoft/TypeScript#34955](https://github.com/microsoft/TypeScript/issues/34955) (Open, `Bug`, `Domain: check: Control Flow`)

**Why doesn't awaiting a Promise\<never\> change reachability?**

*TypeScript 3.7.2 does not mark code after awaiting a Promise<never> as unreachable despite its never return type.*

 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/34955#issuecomment-1753518865) **jespertheend** said "I'm implementing the garbage collection using WeakRefs as we speak :)"
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/34955#issuecomment-1753923564) **jespertheend** said "Actually, I just realised what I want to do isn't possible :/ So errors for unreachable code would actually be very convenient here."
 * [1.9 years ago](https://github.com/microsoft/TypeScript/issues/34955#issuecomment-2196027585) **toonvanvr** described encountering the same issue and sharing a workaround that uses `return await loggedCriticalError` to preserve the return type and immediate logging, accompanied by example code
 * [later](https://github.com/microsoft/TypeScript/issues/34955#issuecomment-4730425037) **nikeee** reported a new case involving definite return analysis and process.exit in Node.js, stating that the code should not error

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Open, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4256022056) **DanielRosenwasser** said "@typescript-bot bump release-6.0"
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4256022474) **typescript-bot** provided a CI jobs progress update with command, status, and results links
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4256102755) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.3 for you."
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4726011060) **Huaian666** said "about the typescript part — switched to this recently and the performance difference is night and day compared to what i was using"

### [Issue microsoft/TypeScript#63547](https://github.com/microsoft/TypeScript/issues/63547) (Closed, `Won't Fix`)

**packageId is not set when calling resolveModuleName on a directory with an index\.d\.ts file in a dependency**

*TypeScript resolveModuleName fails to set packageId when importing a directory’s index.d.ts without explicit index path*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63547#issuecomment-4699887821) **tahanawab4848** described the root cause of missing packageId when resolving directory indices vs explicit file paths and suggested adding packageId lookup in loadModuleFromDirectoryWorker in moduleNameResolver.ts, plus provided a workaround code snippet
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63547#issuecomment-4714142629) **typescript-automation[bot]** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (yesterday) **typescript-automation[bot]** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63547#issuecomment-4721398343) **RyanCavanaugh** warned that automated comments are disallowed per CONTRIBUTING.md and that future instances will result in an org block
 * [today](https://github.com/microsoft/TypeScript/issues/63547#issuecomment-4724301391) **tahanawab4848** apologized and clarified that the comment was not automated
 * [today](https://github.com/microsoft/TypeScript/issues/63547#issuecomment-4724403439) **RyanCavanaugh** said "@tahanawab4848 fair enough. How'd you even find this issue in the first place, let alone decide to do all that research for a bug that was marked as something we wouldn't ever fix?"

### [Issue microsoft/TypeScript#63557](https://github.com/microsoft/TypeScript/issues/63557) (Closed, `Suggestion`, `Declined`)

**Fix confusing keywords "as const" and introduce "valueof"**

*Add a valueof utility type and rename as const to accurately reflect its literal narrowing and readonly behavior.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63557#issuecomment-4712231908) **MartinJohns** said "Duplicate of #37642."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63557#issuecomment-4712663568) **jcalz** noted the issue contained two independent requests and recommended splitting them; indicated the ‘valueof’ request was a duplicate unlikely to be implemented; argued that changing ‘as const’ to ‘as readonly’ would be a breaking change for little benefit and suggested using a userland helper function
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63557#issuecomment-4713898113) **Mudloop** noted that while utility types can be written in userspace they are cumbersome to copy and reorganize, and agreed that aliasing 'as const' would confuse users
 * [today](https://github.com/microsoft/TypeScript/issues/63557#issuecomment-4721300128) **nmain** pointed out that the topic has been repeatedly discussed and referenced the FAQ entry in the issue template
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Declined`
 * [today](https://github.com/microsoft/TypeScript/issues/63557#issuecomment-4721358879) **RyanCavanaugh** said "Echoing https://github.com/microsoft/TypeScript/issues/63557#issuecomment-4712663568, neither of these are changes that are aligned with our general principles."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63561](https://github.com/microsoft/TypeScript/issues/63561) (Open)

**Generator functions may not return \`IteratorObject\`**

*Generator functions declared to return IteratorObject<T> without explicit return statements incorrectly trigger a missing return value error.*

 * created by **laverdet**
 * [today](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4719928165) **jcalz** explained implicit returns conform to unknown, noted TypeScript expects void for IteratorObject return types, and suggested defaulting the second type argument to void
 * [today](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4720879905) **nmain** said "This also "works" if you use Iterable as your return type because instead of TReturn = unknown, TNext = unknown, Iterable defaults to TReturn = any, TNext = any.  "
 * [today](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4720908626) **laverdet** said "Maybe TReturn should default to void instead of unknown."
 * [today](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4723589163) **Renegade334** observed that TypeScript already provides a dedicated return type for generator functions usable in return annotations
 * [later](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4729759859) **nmain** questioned whether the facilitation was deliberate and asked why defaults are any on Generator<> and Iterable<> but unknown on IteratorObject<>
 * [later](https://github.com/microsoft/TypeScript/issues/63561#issuecomment-4732242373) **laverdet** described using generator functions for simple iterables, downcasting to Iterator<T> due to Generator<T,R,N>’s complexity, noted lost functionality with built-in iterators, suggested creating a custom interface extending Generator, and proposed considering void as a default for TReturn on IteratorObject while acknowledging it may be too late

### [PR microsoft/TypeScript#63563](https://github.com/microsoft/TypeScript/pull/63563) (Closed, `For Backlog Bug`)

**Narrow destructured discriminated unions when the discriminant has a default**

*Providing a default value for a discriminant in a destructured union prevents sibling bindings from narrowing.*

 * created by **DukeDeSouth**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63563#issuecomment-4725904450) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63563#issuecomment-4725904471) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (today) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63564](https://github.com/microsoft/TypeScript/issues/63564) (Closed)

**Generic type to \`json\` method of \`fetch\`**

*Enable specifying the JSON return type by adding a generic type parameter to the fetch Response.json method.*

 * created by **rtritto**
 * [later](https://github.com/microsoft/TypeScript/issues/63564#issuecomment-4730143403) **MartinJohns** said "Duplicate of #44603 / #30220. This has been rejected several times already."
 * (later) **rtritto** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63564#issuecomment-4730245004) **rtritto** asked if the issue would still be rejected given that response.json uses JSON.parse and other issues refer to JSON.type
 * [later](https://github.com/microsoft/TypeScript/issues/63564#issuecomment-4730271134) **MartinJohns** stated that it would still be rejected, noted similar past issues, argued that it adds no safety and misleads users about type checking, and suggested using declaration merging as a workaround

