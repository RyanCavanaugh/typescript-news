# Report for 2026-07-02 (Thursday, July 2nd, 2026)

10 different users commented on 10 different issues.

## Recommended Actions

 * Moderation
    * @dominexmacedon-docs posted irrelevant spam content in [microsoft/TypeScript#63605](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4870009171)
    * @dominexmacedon-docs posted rude content in [microsoft/TypeScript#63607](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4873016141)
    * @dominexmacedon-docs posted rude content in [microsoft/TypeScript#63607](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4873037523)
 * Response Recommended
    * @mootari provided important information that .mts is also reserved by macOS in [microsoft/TypeScript#25945](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-4876969542)
    * @qgustavor asked what solution OS vendors should adopt for .ts file associations in [microsoft/TypeScript#25945](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-4877651277)
    * @ChetanyaRathi asked if a PR would be accepted and if the scope was correct in [microsoft/TypeScript#63573](https://github.com/microsoft/TypeScript/issues/63573#issuecomment-4871764159)

## Activity Summary

### [Issue microsoft/TypeScript#12936](https://github.com/microsoft/TypeScript/issues/12936) (Open, `Suggestion`, `Awaiting More Feedback`)

**Exact Types**

*Introduce an Exact<T> type (e.g. |T|) to enforce exact object types and disallow extra properties.*

 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [22 weeks ago](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-3807161298) **trusktr** emphasized that the feature was needed to prevent program errors and to provide proper types for iterating over Object.keys and Object.entries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries
 * [later](https://github.com/microsoft/TypeScript/issues/12936#issuecomment-4876450802) **Tuttotorna** proposed treating Exact<T> as a boundary operator and outlined enforcement rules to preserve structural typing outside boundaries

### [Issue microsoft/TypeScript#14150](https://github.com/microsoft/TypeScript/issues/14150) (Open, `Suggestion`, `Awaiting More Feedback`)

**Unsafe type\-incompatible assignments should not be allowed**

*Assigning a StringOnly object to a StringOrNull type erroneously compiles, allowing null assignments and risking runtime errors.*

 * [7 years ago](https://github.com/microsoft/TypeScript/issues/14150#issuecomment-508950229) **k4b7** proposed a --strictAssignment flag for strict variance in TypeScript, described its behavior for arrays and objects, discussed the need to update programs and library definitions, and suggested using pragmas to selectively enable the flag in source and .d.ts files
 * [6.9 years ago](https://github.com/microsoft/TypeScript/issues/14150#issuecomment-514331712) **AnyhowStep** shared a link to a prototype typescript-eslint rule that makes mutable properties invariant and described its testing status and usage
 * [5.3 years ago](https://github.com/microsoft/TypeScript/issues/14150#issuecomment-787418483) **castarco** asked about the status of the discussion on introducing a 'mutable' keyword, proposed example usages, and inquired why a 2016 proposal was closed
 * [later](https://github.com/microsoft/TypeScript/issues/14150#issuecomment-4876676597) **Tuttotorna** explained that the issue is a mutable alias boundary problem rather than a normal assignability problem and proposed specific read and write checks to enforce write-safe aliasing

### [Issue microsoft/TypeScript#25945](https://github.com/microsoft/TypeScript/issues/25945) (Closed, `External`)

**macOS considers typescript files to be MPEG\-2 Transport Stream \- QuickLook and Spotlight do not work**

*macOS incorrectly identifies TypeScript (.ts) files as MPEG-2 transport streams, breaking QuickLook and Spotlight functionality.*

 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3649797068) **qgustavor** described that the .ts extension issue arose from a lack of file extension standardization across operating systems, noted that renaming the extension was impractical, and proposed future OS heuristics to distinguish file types
 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3916884301) **qgustavor** suggested replacing .ts with .cts and .mts and then noted forgetting to edit after encountering an issue
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-4757554749) **neoneye** said "Just wasted 1 hour on trying to resolve this issue with Claude, making all kinds of changes to my mac, clearing caches. No luck getting quicklook working for ts files."
 * [later](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-4876969542) **mootari** noted that .mts suffers the same problem as .ts because macOS reserves it as an AVCHD transport stream
 * [later](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-4877651277) **qgustavor** described the difficulty of distinguishing .ts Transport Stream and TypeScript files on OSes and asked what solution OS vendors should adopt

### [Issue microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508) (Open, `Discussion`)

**6\.0 Migration Guide**

*Placeholder issue for drafting and publishing the migration guide for version 6.0.*

 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4331983425) **linnbenton** highlighted inconsistent baseUrl deprecation warnings in TS 6+ monorepo setups and asked whether this is intended as an early signal for TS 7 or if the migration strategy for monorepos is still evolving
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4743768229) **sahin52** pointed out that the default value of "strict" became true and linked the related pull request and issue
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4744398238) **sahin52** said "Also various other changes can be found in the milestone: https://github.com/microsoft/TypeScript/milestone/218?closed=1"
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871328823) **ljharb** said "I still want node10 semantics (i don't care what the defaults are). How can I keep them in TS 7+?"
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871339943) **jakebailey** said "You cannot, except to switch to bundler."
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871404071) **ljharb** asked what the difference between bundler and node10 was and why node10 support was removed, noting that people supporting old nodes would lose type support
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871588327) **andrewbranch** explained the distinctions between node10, bundler, and node16 module resolution algorithms and justified dropping node10 from TypeScript’s maintained algorithms
 * [today](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4871607338) **ljharb** argued that in latest node all code was CJS or ESM because they're indistinguishable; noted that testing multiple TypeScript versions was prohibitively hard due to TS 6 incompatibility; decided to use bundler; mentioned that resolve@next already models all node resolution permutations and has near-zero maintenance cost

### [Issue microsoft/TypeScript#63573](https://github.com/microsoft/TypeScript/issues/63573) (Open, `Suggestion`, `Experience Enhancement`)

**Hover documentation for parameters documented with jsdoc renders improperly**

*VSCode hover feature misrenders JSDoc @param descriptions when using hyphens or wrapped lines.*

 * (1 week ago) **RyanCavanaugh** added labels `Suggestion`, `Experience Enhancement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63573#issuecomment-4871764159) **ChetanyaRathi** offered to implement PR to strip leading hyphens and normalize multi-line descriptions in hover rendering and asked if the scope was correct and if the PR would be accepted

### [PR microsoft/TypeScript#63604](https://github.com/microsoft/TypeScript/pull/63604) (Closed, `For Backlog Bug`)

**fix\(completions\): exclude \`default\` keyword from expression\-body arrow function completions**

*Exclude the default keyword from expression-bodied arrow function completions by modifying completion context detection and filters.*

 * created by **tsushanth**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63604#issuecomment-4869923852) **MartinJohns** said "@tsushanth You should read this: https://github.com/microsoft/TypeScript/issues/62963"

### [Issue microsoft/TypeScript#63605](https://github.com/microsoft/TypeScript/issues/63605) (Closed)

**Is developing interpreter on top of Node\.js good?**

*Developing an interpreter on Node.js enables rapid prototyping and cross-platform deployment but sacrifices performance and memory efficiency versus native implementations.*

 * created by **dominexmacedon-docs**
 * [today](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4869806368) **MartinJohns** said "AI spam."
 * [today](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4869918188) **dominexmacedon-docs** denied being AI spam and suggested learning the Node.js-based language for its critical features
 * [today](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4869947662) **MartinJohns** called the issue spam, said it was AI generated and unrelated to the repository
 * [today](https://github.com/microsoft/TypeScript/issues/63605#issuecomment-4870009171) **dominexmacedon-docs** acknowledged the content was AI-generated spam, explained they used Copilot to generate markdown, and clarified that the language is real and built on Node.js

### [Issue microsoft/TypeScript#63606](https://github.com/microsoft/TypeScript/issues/63606) (Open, `Bug`, `Domain: lib.d.ts`)

**Intl\.PluralRules constructor should not be callable without new**

*The TypeScript lib.es2020.intl.d.ts incorrectly allows calling Intl.PluralRules without new, contrary to the ECMA-402 specification.*

 * created by **ptomato**

### [Issue microsoft/TypeScript#63607](https://github.com/microsoft/TypeScript/issues/63607) (Closed)

**Why can't we build a VM on the top of Node\.js? Is it because of not being Native?**

*Building a VM on Node.js supports basic features but fails to handle advanced capabilities like object iteration and control flow, so most implementations use C.*

 * created by **dominexmacedon-docs**
 * [today](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4872986822) **MartinJohns** said "This issue tracker is meant for bug reports and feature requests regarding TypeScript. It's not suited for your ChatGPT questions."
 * [today](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4873016141) **dominexmacedon-docs** replied defensively accusing the commenter of jealousy
 * [today](https://github.com/microsoft/TypeScript/issues/63607#issuecomment-4873037523) **dominexmacedon-docs** insulted the maintainer and asserted their right to post ChatGPT questions

