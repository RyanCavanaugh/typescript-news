# Report for 2026-08-29 (Saturday, August 29th, 2026)

11 different users commented on 19 different issues.

## Recommended Actions

 * Response Recommended
    * @irfanstract asked if the linked PR would get revived in [microsoft/TypeScript#14466](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-5467139913)
    * @resucutie asked about progress towards resolving the issue in [microsoft/TypeScript#58657](https://github.com/microsoft/TypeScript/issues/58657#issuecomment-5465152429)
    * @kritharth2005 asked if the issue was still available to be taken up in [microsoft/TypeScript#63958](https://github.com/microsoft/TypeScript/issues/63958#issuecomment-5464152428)
    * @kritharth2005 provided detailed root cause analysis and repro environment update in [microsoft/TypeScript#63958](https://github.com/microsoft/TypeScript/issues/63958#issuecomment-5466830071)
    * @CamJN reported that the watcher count exceeds macOS process limits in [microsoft/TypeScript#64062](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5464328507)

## Activity Summary

### [Issue microsoft/TypeScript#14466](https://github.com/microsoft/TypeScript/issues/14466) (Open, `Suggestion`, `In Discussion`)

**Existential type?**

*Add existential type parameters in TypeScript definitions to avoid propagating generics for Binding and Scheduler constructors.*

 * [1 year ago](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-3194192650) **barasztamas** presented a common TypeScript use case example and expressed reluctance to use advanced TS solutions
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-3194224590) **MoritzR** suggested using a simpler function type returning Promise<void> and explained how to handle intermediate null values
 * [31 weeks ago](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-3768593626) **devanshj** offered a PR for experimenting with existential types, showed screenshots of its behavior on two comments, and welcomed feedback
 * [today](https://github.com/microsoft/TypeScript/issues/14466#issuecomment-5467139913) **irfanstract** said "any chance the linked PR would get revived?"

### [Issue microsoft/TypeScript#29188](https://github.com/microsoft/TypeScript/issues/29188) (Closed, `Design Limitation`)

**Conditional type does not narrow union type**

*TypeScript’s conditional type fails to narrow an Array<any> | Specification union in a recursive Mapping type, causing a type error.*

 * (2 days ago) **RyanCavanaugh** added label `Design Limitation`, and removed label `Needs Human Review`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/29188#issuecomment-5445952540) **weswigham** said "Also, just... ref https://github.com/microsoft/TypeScript/pull/63926. "
 * [today](https://github.com/microsoft/TypeScript/issues/29188#issuecomment-5465984036) **typescript-automation[bot]** said "This issue has been marked as "Design Limitation" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#58657](https://github.com/microsoft/TypeScript/issues/58657) (Open, `Suggestion`, `Awaiting More Feedback`)

**Improve support for internal packages by resolving path aliases**

*Add tsconfig.json to package exports to ensure TypeScript correctly resolves internal package path aliases.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/58657#issuecomment-2399150593) **damianobarbati** asked if there was a way to avoid tsconfig paths and use only native Node module resolution for module alias imports, noting that subpath imports worked but alias imports failed with TS2307
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/58657#issuecomment-2399780048) **zirkelc** clarified that the issue stemmed from TypeScript’s path resolution with import type and provided a related issue link
 * [43 weeks ago](https://github.com/microsoft/TypeScript/issues/58657#issuecomment-3459551699) **8ctavio** expressed interest in a way for monorepo packages to share module-resolution-related configurations, proposed an allowlist-based tsconfig.json solution for referring to package-specific settings, and mentioned opening a feature request for output-to-input directory mapping
 * [today](https://github.com/microsoft/TypeScript/issues/58657#issuecomment-5465152429) **resucutie** said "hello! any progress towards this issue? i'd like to get it resolved!"

### [Issue microsoft/TypeScript#63681](https://github.com/microsoft/TypeScript/issues/63681) (Open, `Suggestion`, `Awaiting More Feedback`)

**Proposal: \`unstable\` and \`volatile\` control\-flow analysis modifiers**

*Add erasable ‘unstable’ and ‘volatile’ declaration modifiers to disable TypeScript’s optimistic control-flow narrowing for specific variables and properties.*

 * (1 month ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63681#issuecomment-5104806304) **jcalz** said "cross-linking to #49669"
 * [today](https://github.com/microsoft/TypeScript/issues/63681#issuecomment-5467024419) **irfanstract** proposed that absence of `readonly` imply new semantics and suggested permitting `const` modifiers in interfaces to denote held-constant properties

### [Issue microsoft/TypeScript#63718](https://github.com/microsoft/TypeScript/issues/63718) (Open, `Bug`, `Help Wanted`, `Domain: Parser`)

**TS1518 depends on operand order in negated v\-mode class unions**

*TS1518 detection for negated v-mode RegExp character class unions is order-dependent, failing to flag invalid patterns when the string-pattern operand is second.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3 weeks ago](https://github.com/microsoft/TypeScript/issues/63718#issuecomment-5200200361) **goutamadwant** opened pull request #63723 with a fix and regression baselines, explained it evaluates every ClassUnion operand for MayContainStrings and reports TS1518 regardless of operand order, and asked for feedback
 * **RyanCavanaugh** added label `Domain: Parser`
 * [later](https://github.com/microsoft/TypeScript/issues/63718#issuecomment-5469316661) **a-tarasyuk** believed the issue was resolved by commit a19f54943b7

### [Issue microsoft/TypeScript#63781](https://github.com/microsoft/TypeScript/issues/63781) (Closed, `Working as Intended`, **ahejlsberg**)

**Error on function type that comes from a function declaration that is declared after usage site**

*tsgo reports an error on arr.map when using typeof on a function declared later in a union, unlike TypeScript 5.8.*

 * **RyanCavanaugh** assigned to **ahejlsberg**
 * **ahejlsberg** added label `Working as Intended`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63781#issuecomment-5444964687) **ahejlsberg** said "This is indeed a type ordering issue and TS 6 reports the same error with -stabletypeordering. That said, without -stabletypeordering TS6 throws an assertion, which is interesting."
 * [today](https://github.com/microsoft/TypeScript/issues/63781#issuecomment-5465983603) **typescript-automation[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#63958](https://github.com/microsoft/TypeScript/issues/63958) (Open, `Bug`)

**Declaration emit: JSDoc @typedef/@callback comments are separated from their synthesized type when preceded by another declaration**

*Declaration emit for JS files misplaces JSDoc @typedef/@callback comments, detaching them from their synthesized types when preceded by another declaration.*

 * created by **Abdullah-Builds**
 * (3 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63958#issuecomment-5464152428) **kritharth2005** asked if the issue was still available and offered to investigate declaration emit and JSDoc handling before sharing a proposed approach
 * [today](https://github.com/microsoft/TypeScript/issues/63958#issuecomment-5464172994) **kritharth2005** said "Okay "
 * [today](https://github.com/microsoft/TypeScript/issues/63958#issuecomment-5464688551) **Abdullah-Builds** released the issue for someone else to pick up
 * [today](https://github.com/microsoft/TypeScript/issues/63958#issuecomment-5466830071) **kritharth2005** described root cause of misplaced JSDoc comment in synthesized type aliases, explained missing preserveJsDoc in transformTypeAliasDeclaration and printer comment-scanning behavior, and noted updated repro environment on main

### [Issue microsoft/TypeScript#64049](https://github.com/microsoft/TypeScript/issues/64049) (Closed, `Won't Fix`)

**Erasing a \`const enum\` can emit an illegal \`"use strict"\` directive**

*Erasing a const enum places a string literal first in a default-parameter function, creating an illegal 'use strict' directive.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64049#issuecomment-5441731799) **RyanCavanaugh** ran #64041 to check for misplaced `use strict` directives, found none, and emphasized that disabling `use strict` is not acceptable
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64049#issuecomment-5441981277) **magic-akari** suggested that the scan may have missed some cases and provided links to specific test files for review
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64049#issuecomment-5442218368) **magic-akari** said "If TypeScript does not plan to address this, I think we can treat it as unspecified or implementation-dependent behavior, with no canonical interpretation, and close the issue on that basis."
 * [today](https://github.com/microsoft/TypeScript/issues/64049#issuecomment-5465983837) **typescript-automation[bot]** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-automation[bot]** closed the issue

### [Issue microsoft/TypeScript#64050](https://github.com/microsoft/TypeScript/issues/64050) (Open, `Needs Investigation`, **andrewbranch**)

**Content mapper duplicated inlay hints**

*Splitting a statement into multiple spans in the content mapper causes duplicate inlay hints due to separate hint generation for each span.*

 * (2 days ago) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `TypeScript 7.1`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript/issues/64050#issuecomment-5466688573) **jasonlyu123** explained that request spans mapped to multiple virtual spans, causing intersection checks to apply to generated inlay hint code unexpectedly and noting a client-side middleware workaround and potential impact on the duplicate entry solution

### [Issue microsoft/TypeScript#64062](https://github.com/microsoft/TypeScript/issues/64062) (Closed, `External`)

**LSP causes client to watch thousands of files**

*TypeScript LSP server's file watcher registers a project-wide glob, watching thousands of files and exhausting file descriptors.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5456560062) **CamJN** said "Perhaps, but the server shouldn't ask to watch files that are absolutely never going to be useful. Like why watch the contents of .git? "
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5456990232) **RyanCavanaugh** said "There's a trade-off here: if your root dir has many files/directories, asking for separate watches on each of those is less efficient than the "everything" watch that happens to include .git."
 * [today](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5461132184) **guillaumebrunerie** asked whether eglot uses one watch per file or per subdirectory and noted Linux supports only per-subdirectory watches
 * [today](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5464328507) **CamJN** concluded that there was one watcher per subdirectory resulting in 12,872 watchers exceeding macOS process limits
 * [today](https://github.com/microsoft/TypeScript/issues/64062#issuecomment-5464372309) **CamJN** said "By comparison, if it only watched the directories (and their subdirectories) named in the tsconfig's include section, the number of watchers would be 11."

### [PR microsoft/TypeScript#64093](https://github.com/microsoft/TypeScript/pull/64093) (Open, `For Milestone Bug`)

**feat: add Promise\.allKeyed and Promise\.allSettledKeyed to esnext**

*Add Promise.allKeyed and Promise.allSettledKeyed methods to the ESNext Promise API.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript#64094](https://github.com/microsoft/TypeScript/issues/64094) (Open)

**typescript\-language\-server does not work with @typescript/typescript6**

*typescript-language-server is incompatible with @typescript/typescript6 due to a missing tsserver.js wrapper in its lib directory.*

 * created by **guillaumebrunerie**

### [PR microsoft/TypeScript#64095](https://github.com/microsoft/TypeScript/pull/64095) (Open, `For Milestone Bug`)

**feat: add iterator methods to esnext**

*Add iterator methods to ESNext type definitions to support iteration protocols.*

 * created by **a-tarasyuk**

### [PR microsoft/TypeScript#64096](https://github.com/microsoft/TypeScript/pull/64096) (Open, `For Milestone Bug`, **DanielRosenwasser**)

**feat: add es2026 as a valid target and lib**

*Add ES2026 as a recognized compilation target and library option in TypeScript.*

 * created by **a-tarasyuk**

### [Issue microsoft/TypeScript#64097](https://github.com/microsoft/TypeScript/issues/64097) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**On TypeScript 7, Call hierarchy shows a full absolute path instead of file name \+ relative path**

*TypeScript 7 native-preview’s call hierarchy feature incorrectly displays full absolute file paths instead of file names with relative paths.*

 * created by **brian-xu-vlt**

### [Issue microsoft/TypeScript#64098](https://github.com/microsoft/TypeScript/issues/64098) (Open)

**tsconfig \`include\` silently drops \`Foo\.tsx\` when \`foo\.ts\` exists, on a case\-insensitive filesystem**

*TypeScript’s tsconfig include option silently ignores .tsx files on case-insensitive filesystems when a same-named .ts file exists, preventing diagnostics.*

 * created by **jomonkj**

