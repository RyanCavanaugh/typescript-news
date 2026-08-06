# Report for 2026-07-30 (Thursday, July 30th, 2026)

11 different users commented on 29 different issues.

## Recommended Actions

 * Response Recommended
    * @Arlen22 provided a workaround and suggested areas for investigation in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-5142841539)
    * @danyreyna reported similar Docker build failure with fanotify_mark error in [microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5137934722)
    * @ayishaatwork asked if there are any related discussions or implementation details to review first in [microsoft/TypeScript#63677](https://github.com/microsoft/TypeScript/issues/63677#issuecomment-5133861386)

## Activity Summary

### [Issue microsoft/TypeScript#49229](https://github.com/microsoft/TypeScript/issues/49229) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support to method decorator that change the method signature**

*Enable TypeScript method decorators to modify method signatures and update the compiler’s type inference accordingly*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/49229#issuecomment-2461809830) **sybereal** explained that Zod parsing can change input types and described using a decorator to abstract schema validation and avoid manual parsing
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/49229#issuecomment-2600601913) **Jamesernator** suggested allowing decorators to change class type and reported a type error
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/49229#issuecomment-2816161609) **Arlen22** provided another example illustrating usefulness and noted surprise that support was missing
 * [today](https://github.com/microsoft/TypeScript/issues/49229#issuecomment-5138510770) **ayden94** provided implementation evidence and proposed a semantic model for type-changing standard method decorators in a TypeScript-Go/Corsa prototype

### [Issue microsoft/TypeScript#54256](https://github.com/microsoft/TypeScript/issues/54256) (Closed, `Suggestion`, `Domain: Performance`, `Experimentation Needed`, `Rescheduled`, **rbuckton**, **jakebailey**)

**Experiment with Parallelized Parsing**

*Investigate parallelizing TypeScript file parsing across worker processes to reduce load times and evaluate overhead and usability tradeoffs.*

 * (2 years ago) **RyanCavanaugh** set milestone to `TypeScript 5.7.0`, and removed from milestone `TypeScript 5.5.0`
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/54256#issuecomment-2608859169) **mistic** said "Is there any news on this effort? Is it still planned? Performance on big projects would definitely benefit from this (specially type checking on CI)"
 * [today](https://github.com/microsoft/TypeScript/issues/54256#issuecomment-5137807510) **ahejlsberg** said "Fixed in TS7!"
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#62050](https://github.com/microsoft/TypeScript/issues/62050) (Closed, `Working as Intended`, `Domain: Performance`)

**Control Flow Analysis Performance Regression**

*TypeScript v5.5.4’s control flow analysis changes from PR #58013 cause a 4x slowdown in type-checking large JavaScript files*

 * (1 year ago) **RyanCavanaugh** added label `Possible Improvement`, and set milestone to `Backlog`
 * **DanielRosenwasser** added label `Domain: Performance`
 * [today](https://github.com/microsoft/TypeScript/issues/62050#issuecomment-5137662191) **ahejlsberg** explained that the slowdown wasn’t a regression but resulted from the optimized control flow analysis now processing the entire large function, whereas previously analysis had been disabled for very large functions
 * (today) **ahejlsberg** added label `Working as Intended`, and removed labels `Help Wanted`, `Possible Improvement`
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4230165560) **Arlen22** reported that adding watchOptions to tsconfig.json and VSCode settings didn't fix the issue, and that enabling project diagnostics broke intellisense
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-4230346939) **Arlen22** said "The experimental tsgo vscode plugin does not have any of these problems."
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-5121159127) **eeysudo** described a terminal-only TSServer hang fix for remote SSH/WSL2 with steps for WSL2 daemon reset, SSH verification, log capture, hang pattern identification, and kernel tweak
 * [later](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-5142841539) **Arlen22** indicated that VS Code was not frozen and inotify was already maxed out, recommended hiding the outdated answer, and described a workaround by removing google apis while suggesting further investigation

### [Issue microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch does not work in docker**

*tsc --watch fails to detect file changes in Docker bind-mounted workspaces on macOS after upgrading to version 7.0.2.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4996181046) **johnfav03** asked if the issue also involved docker or was a separate issue with running watchers in parallel
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4996371305) **Alex-Bond** reported that the issue occurred on a native system where circular symlinks in node_modules overwhelmed the watcher, causing it to start listening but never receive updates
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4999890598) **jakebailey** advised the user to file a separate issue for the MacOS problem and clarified that TS7 has no toggle to revert to NodeJS behavior
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5137934722) **danyreyna** reported a similar issue when building with Docker using node:22.22.3-slim, where subsequent tsc --watch builds stalled due to a fanotify_mark operation not supported error

### [Issue microsoft/TypeScript#63677](https://github.com/microsoft/TypeScript/issues/63677) (Open, `Bug`, `Domain: check: Variance Relationships`)

**type parameter variance in generic call signature is incorrectly bivariant**

*TypeScript incorrectly allows bivariant assignments for invariant generic call signatures, resulting in unsound type checking.*

 * created by **ahmedajiz629**
 * (3 days ago) **RyanCavanaugh** added label `Bug`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63677#issuecomment-5133861386) **ayishaatwork** offered to work on the issue, reproduce the behavior, trace the compiler's assignability handling for generic function signatures, identify the unsound variance check, and share findings before opening a PR

### [Issue microsoft/TypeScript#63691](https://github.com/microsoft/TypeScript/issues/63691) (Open, `Suggestion`, `Awaiting More Feedback`)

**JSDoc tag for getting around "Object literals are open\-ended"**

*Propose adding a JSDoc tag (e.g., @closed) to enforce exact object literal types in checked JavaScript files.*

 * created by **TheNamlessGuy**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63693](https://github.com/microsoft/TypeScript/issues/63693) (Open, `Needs Investigation`, **joj**)

**Typescript 6\.0\.3升级到7\.0后报错**

*Upgrading TypeScript from 6.0.3 to 7.0 in VS2026 breaks compilation due to the removed 'target=ES5' option.*

 * created by **zlm166**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **joj**
 * [later](https://github.com/microsoft/TypeScript/issues/63693#issuecomment-5141412480) **zlm166** mentioned that others had encountered the same issue and linked a StackOverflow question

### [Issue microsoft/TypeScript#63694](https://github.com/microsoft/TypeScript/issues/63694) (Open, `Needs Investigation`, `Fix Available`, **ahejlsberg**)

**Assignability between distributive conditional types and their branch type is reversed in contravariant positions**

*TypeScript distributive conditional types incorrectly reverse assignability in contravariant positions.*

 * created by **ahmedajiz629**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, set milestone to `Backlog`, and assigned to **ahejlsberg**
 * **typescript-automation[bot]** added label `Fix Available`

### [Issue microsoft/TypeScript#63695](https://github.com/microsoft/TypeScript/issues/63695) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add support for \`@file\` jsdoc tag to describe a module**

*Support the JSDoc @file tag for module documentation in TypeScript and display descriptions in hover and autocomplete.*

 * created by **remcohaszing**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63696](https://github.com/microsoft/TypeScript/issues/63696) (Open, `Bug`, `Help Wanted`)

**False positive on destructured \`require\` is \`verbatimModuleSyntax\` and \`module\` is \`preserve\`**

*TypeScript incorrectly rejects destructured CommonJS require calls when verbatimModuleSyntax is enabled and module is preserve.*

 * created by **remcohaszing**
 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63696#issuecomment-5134707373) **Samyra312007** said "Thanks for sharing."

### [Issue microsoft/TypeScript#63697](https://github.com/microsoft/TypeScript/issues/63697) (Closed, `Design Limitation`)

**Return type inference limitation**

*TypeScript fails to infer the context property b in a generic callback passed to route.*

 * created by **aquapi**
 * [today](https://github.com/microsoft/TypeScript/issues/63697#issuecomment-5135643442) **RyanCavanaugh** explained that inference couldn't alternate between an outer call's contextual type and an inner call's context-sensitive expression, since resolving both would require a unification-based algorithm that is unlikely for performance and practical reasons
 * **RyanCavanaugh** added label `Design Limitation`

### [Issue microsoft/TypeScript#63698](https://github.com/microsoft/TypeScript/issues/63698) (Closed)

**The generated tuple order is incorrect after upgrading to TypeScript 7**

*UnionToTuple now generates incorrectly ordered tuples of TAPI keys under TypeScript 7, triggering type errors.*

 * created by **waivital**
 * [today](https://github.com/microsoft/TypeScript/issues/63698#issuecomment-5139492768) **MartinJohns** clarified that tuple order had never been supported and that UnionToIntersection was not a supported type
 * [later](https://github.com/microsoft/TypeScript/issues/63698#issuecomment-5144699122) **RyanCavanaugh** said "See also https://github.com/microsoft/TypeScript/issues/13298#issuecomment-468375328"
 * (later) **RyanCavanaugh** closed the issue

