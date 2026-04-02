# Report for 2026-01-05 (Monday, January 5th, 2026)

5 different users commented on 21 different issues.

## Recommended Actions

 * Response Recommended
    * @MarkMoretto asked if missing createElement suggestions in VSCode were related to his settings or if it needed its own issue in [microsoft/TypeScript#62857](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3712337535)
    * @MehmetHooke suggested lowering ignoreDeprecations version to 5.0 in [microsoft/TypeScript#62916](https://github.com/microsoft/TypeScript/issues/62916#issuecomment-3714239338)

## Activity Summary

### [Issue microsoft/TypeScript#62827](https://github.com/microsoft/TypeScript/issues/62827) (Open, `Discussion`)

**Closing TS 6\.0 LS issues**

*All TypeScript 6.0 language service issues are being closed due to a full LSP-based rewrite targeting the native 7.0 codebase.*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62827#issuecomment-3689236309) **magic-akari** asked whether issues with open PRs could be excluded from the bulk closure, citing issue #42468 and PR #62818 as an example
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62827#issuecomment-3693007960) **coderrshyam** mentioned Microsoft ownership of GitHub and suggested contacting the GitHub API team leader
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62827#issuecomment-3693140053) **Bashamega** said "Different teams @coderrshyam, different offices"
 * [today](https://github.com/microsoft/TypeScript/issues/62827#issuecomment-3711699202) **RyanCavanaugh** said "@magic-akari we are very unlikely to merge those PRs, since we're trying to minimize code churn in 6.0"

### [Issue microsoft/TypeScript#62857](https://github.com/microsoft/TypeScript/issues/62857) (Closed, `Not a Defect`)

**JavaScript IntelliSense does not suggest methods added to built\-in prototypes**

*JavaScript IntelliSense in VS Code fails to suggest custom methods added to built-in prototypes like Promise.log.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3634219335) **RyanCavanaugh** said "Global merges like this aren't supported; you'll need to use a .d.ts file for this"
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3644523154) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (3 weeks ago) **typescript-bot** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3712337535) **MarkMoretto** asked if missing createElement suggestions in VSCode were related to his settings or if it needed its own issue
 * [today](https://github.com/microsoft/TypeScript/issues/62857#issuecomment-3713529074) **sangafabrice** suggested opening a new issue, explained that VS Code intentionally suggests React-related functions without the package installed, and reported successful testing on Windows 10 with VS Code 1.107.1

### [Issue microsoft/TypeScript#62906](https://github.com/microsoft/TypeScript/issues/62906) (Open, `Suggestion`, `Awaiting More Feedback`)

**Spreading object with optional property causes incorrect type inference when \`exactOptionalPropertyTypes = false\`**

*Spreading optional properties incorrectly infers defined types ignoring undefined when exactOptionalPropertyTypes is false.*

 * created by **ptandler**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62906#issuecomment-3665067937) **jcalz** stated that the issue still looked like a duplicate
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62906#issuecomment-3681630116) **ptandler** summarized the semantics of optional properties with exactOptionalPropertyTypes disabled, explained JavaScript object spread runtime behavior, argued that TypeScript should infer number | undefined for spread properties, and clarified that the issue is due to a mismatch with ECMAScript semantics rather than the exactOptionalPropertyTypes setting
 * [today](https://github.com/microsoft/TypeScript/issues/62906#issuecomment-3711948041) **RyanCavanaugh** noted that implementing this would require making EOPT a tri-state (off, classic, on) but doubted the appetite for the off option
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#62908](https://github.com/microsoft/TypeScript/issues/62908) (Closed, `Duplicate`)

**Incorrect type narrowing with async/await**

*TypeScript incorrectly infers that a variable updated inside Promise.allSettled can only be undefined, preventing proper type narrowing.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62908#issuecomment-3669948614) **ritschwumm** described a twofold issue with TypeScript's type narrowing behavior and provided a workaround using an identity function or IIFE
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62908#issuecomment-3670042326) **MartinJohns** described a simpler option to prevent type narrowing upon assignment using type assertions, noted gotchas with string literal assignments and the satisfies operator, and discussed tsc’s type inference behavior and performance implications
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62908#issuecomment-3670820084) **jcalz** proposed a dedicated operator for non-narrowing assignments to avoid repetition
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#62913](https://github.com/microsoft/TypeScript/issues/62913) (Closed, `Not a Defect`)

**Incorrect rename refactoring in object destructuring**

*Renaming a destructured variable to its original name incorrectly preserves alias syntax instead of simplifying the destructuring.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62913#issuecomment-3674751833) **MartinJohns** said "That's expected to me. You're renaming the variable."
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62913#issuecomment-3674755809) **MartinJohns** explained that the behavior was controlled by the setting `javascript.preferences.renameShorthandProperties` / `typescript.preferences.renameShorthandProperties` and pointed to issue #29238
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62913#issuecomment-3709315358) **dbaeumer** explained that the case differed from the referenced issue, argued that an alias was unnecessary, and suggested using a destructuring alias instead
 * [today](https://github.com/microsoft/TypeScript/issues/62913#issuecomment-3712249347) **RyanCavanaugh** disagreed with the premise and argued that rename operations should consistently preserve runtime behavior unless there’s an error, as conditional behavior is confusing
 * **RyanCavanaugh** added label `Not a Defect`

### [Issue microsoft/TypeScript#62915](https://github.com/microsoft/TypeScript/issues/62915) (Open, `Help Wanted`, `Docs`)

**Document that compiler\.extends can be an array**

*Update tsconfig.json documentation to indicate that the compiler.extends option can accept an array of configurations.*

 * created by **aryzing**
 * (today) **RyanCavanaugh** added labels `Help Wanted`, `Docs`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#62916](https://github.com/microsoft/TypeScript/issues/62916) (Closed)

**\[help\] tsc "ignoreDeprecations": "6\.0"**

*Asking why the TypeScript compiler’s "ignoreDeprecations": "6.0" setting isn’t suppressing deprecation warnings.*

 * created by **cinast**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62916#issuecomment-3678549783) **cinast** added an 'or not' note and attached a screenshot
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62916#issuecomment-3678550098) **cinast** said "either         "ignoreDeprecations": 6,"
 * (today) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/62916#issuecomment-3714239338) **MehmetHooke** suggested lowering the ignoreDeprecations version to "5.0" and provided a sample compilerOptions JSON snippet

### [Issue microsoft/TypeScript#62917](https://github.com/microsoft/TypeScript/issues/62917) (Closed, `Duplicate`)

**Passing \`this\` from a constructor before all fields are set introduces \`undefined\`s in some cases**

*TypeScript does not warn when passing this from a constructor before field initialization, causing undefined property values.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62917#issuecomment-3679123715) **Taureon** identified the issue as related to issue #9998 and suggested it was a descending issue instead
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62917#issuecomment-3679315214) **jcalz** provided a reproducible example showing that 'this' isn't treated as partially initialized before property assignments, related it to other issues, and asked if this is a bug
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62917#issuecomment-3680264848) **mkantor** said "https://github.com/microsoft/TypeScript/issues/30462#issuecomment-723680510 is sort of related to this."
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#62930](https://github.com/microsoft/TypeScript/issues/62930) (Closed)

**\> Nic nie ciekawi mnie bardziej niż zimna myszka\.**

*User remarks that nothing interests them more than a cold mouse.*

 * created by **mekrix777mekort-ops**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/62930#issuecomment-3694069489) **mekrix777mekort-ops** posted a nonsensical comment
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62937](https://github.com/microsoft/TypeScript/issues/62937) (Closed, `Not a Defect`)

**Crash: RangeError: Invalid string length in addSpans when evaluating deeply recursive Template Literal Types with \-\-strict enabled**

*TypeScript compiler crashes with a RangeError on deeply recursive template literal type evaluation when strict mode is enabled*

 * created by **na7ure-a**
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62937#issuecomment-3707209815) **Andarist** explained that it ended up creating a humongous string equivalent to 'k'.repeat(536000000) + 'k'.repeat(1000000)
 * **RyanCavanaugh** added label `Not a Defect`
 * [today](https://github.com/microsoft/TypeScript/issues/62937#issuecomment-3712516046) **RyanCavanaugh** said "TypeScript is not intended to be resilient to explicit attempts to crash it"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62938](https://github.com/microsoft/TypeScript/issues/62938) (Closed)

**Spory wewnętrznej  interpersonalne Systemu**

*Internal interpersonal conflicts within the system are ongoing but failing to produce measurable progress.*

 * created by **mekrix777mekort-ops**
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62940](https://github.com/microsoft/TypeScript/issues/62940) (Closed)

**I acknowledge that issues using this template may be closed without further explanation at the maintainer's discretion\.**

*Acknowledgement that issues using this template can be closed at the maintainer’s discretion without explanation.*

 * created by **mekrix777mekort-ops**
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62940#issuecomment-3703794787) **MartinJohns** said "Wat?"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#62941](https://github.com/microsoft/TypeScript/issues/62941) (Open, `Bug`, `Help Wanted`, `Domain: check: Contextual Types`)

**Crash: RangeError: Maximum call stack size exceeded during contextual typing of object literal with yield in computed property name**

*TypeScript throws a stack overflow when contextual typing an object with a generator yielding in a computed property name.*

 * created by **na7ure-a**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#62943](https://github.com/microsoft/TypeScript/issues/62943) (Closed, `Duplicate`)

**infer property setter type**

*Define a type-safe TypeScript approach to extract the setter parameter type of an object's property.*

 * created by **waelbettayeb**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62943#issuecomment-3704965042) **MartinJohns** said "Duplicate of #60162 / #43729. There's also #60954. All not exactly (using infer), but IMO close enough and about the same issue."
 * **RyanCavanaugh** added label `Duplicate`

### [Issue microsoft/TypeScript#62944](https://github.com/microsoft/TypeScript/issues/62944) (Open, `Suggestion`, `Declined`)

**Allow inferred object literal optional properties**

*Introduce syntax for inferring optional object literal properties (e.g. prop2?) to allow marking certain properties optional during type inference.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706224710) **rtcpw** thanked the contributor for suggesting a helper function and said it was a nice workaround
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3706285199) **MartinJohns** explained that existing helper types could support optional properties and cautioned that the proposed syntax might mislead users
 * [today](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3710383243) **nmain** mentioned that zod already covered the use case and provided an example
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Declined`
 * [today](https://github.com/microsoft/TypeScript/issues/62944#issuecomment-3711959335) **RyanCavanaugh** agreed that zod handles the scenario well and preferred using the partial function as a sufficient workaround

### [Issue microsoft/TypeScript#62946](https://github.com/microsoft/TypeScript/issues/62946) (Closed)

**I acknowledge that issues using this template may be closed without further explanation at the maintainer's discretion\.**

*Acknowledgement that issues using this template can be closed at the maintainer’s discretion without explanation.*

 * created by **mekrix777mekort-ops**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/62946#issuecomment-3706781505) **jcalz** said "Sir, this is a Wendy's."
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62946#issuecomment-3706899605) **MartinJohns** said "No, this is Patrick!"
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#62950](https://github.com/microsoft/TypeScript/pull/62950) (Open, `For Backlog Bug`)

**Ignore computed name parents when looking up containing functions**

*Update lookup to skip computed name parent nodes when identifying a node’s containing function.*

 * created by **Andarist**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **typescript-bot** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#62953](https://github.com/microsoft/TypeScript/issues/62953) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: LS: Inlay Hints`)

**\[Feature Request\] \[Typescript Extension\] Less redundant inlay hints for arrow function vars/consts**

*Extend the TypeScript inlay hints setting to hide variable type hints for arrow functions that already display return types.*

 * created by **refrakto**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`, `Domain: LS: Inlay Hints`

### [Issue microsoft/TypeScript#62954](https://github.com/microsoft/TypeScript/issues/62954) (Open, `Suggestion`, `In Discussion`, `Experimentation Needed`)

**Explicit variance annotations for built\-in \.d\.ts files**

*Proposal to include explicit variance annotations in built-in .d.ts definitions to speed up TypeScript type checking.*

 * created by **akaltar**
 * [today](https://github.com/microsoft/TypeScript/issues/62954#issuecomment-3712221242) **DanielRosenwasser** said "I think if you send a PR we'd be open to discussing it a bit more. We are currently focused on tsgo and parity, but we could run perf tests on the PR to see the differences."
 * (today) **DanielRosenwasser** added labels `Suggestion`, `In Discussion`, `Experimentation Needed`

### [PR microsoft/TypeScript#62955](https://github.com/microsoft/TypeScript/pull/62955) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Simplify "Configure Build Tools" devcontainer step\.**

*Simplify the devcontainer configuration step that sets up build tools.*

 * created by **DanielRosenwasser**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [Issue microsoft/TypeScript#62956](https://github.com/microsoft/TypeScript/issues/62956) (Closed)

**Wrong warning about Duplicate identifier defined by js\-doc**

*VS Code incorrectly warns of a duplicate identifier for a JSDoc typedef when followed immediately by an IIFE in a JavaScript file.*

 * created by **saeed-serpooshan**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

