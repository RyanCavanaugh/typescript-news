# Report for 2026-08-28 (Friday, August 28th, 2026)

24 different users commented on 240 different issues.

## Activity Summary

### [Issue microsoft/TypeScript#11466](https://github.com/microsoft/TypeScript/issues/11466) (Closed, `Bug`, `Won't Fix`, `Domain: Decorators`)

**Improve decorator callstack information to reflect location of decorator**

*TypeScript decorator call stacks reference generated __decorate helper code instead of the decorator's original source line, hindering accurate navigation.*

 * **mhegazy** added label `Bug`
 * (6.1 years ago) **RyanCavanaugh** added label `Domain: Decorators`, and unassigned **rbuckton**
 * **RyanCavanaugh** added label `Won't Fix`
 * [today](https://github.com/microsoft/TypeScript/issues/11466#issuecomment-5457564737) **RyanCavanaugh** said "Doesn't seem like anyone else has ever noticed this."
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#13165](https://github.com/microsoft/TypeScript/issues/13165) (Closed, `Bug`, `Domain: API`, `Needs Human Review`)

**Compiler API: no Symbol for Node**

*TypeScript’s compiler API getSymbolAtLocation sometimes returns undefined for identifier nodes in abstract class method declarations and external object property accesses.*

 * [4.9 years ago](https://github.com/microsoft/TypeScript/issues/13165#issuecomment-927749755) **DanielSWolf** described attempting to retrieve the symbol for a variable declaration using getSymbolAtLocation on various AST nodes and seeing undefined results, and asked if an option was missing
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/13165#issuecomment-1503864494) **mhw0** mentioned that getSymbolAtLocation required passing the declaration’s name property (an Identifier or QualifiedName) rather than the declaration node itself
 * **RyanCavanaugh** added label `Domain: API`
 * [today](https://github.com/microsoft/TypeScript/issues/13165#issuecomment-5458035195) **RyanCavanaugh** noted that the pre-TypeScript-7 Compiler API was superseded by TypeScript 7 and closed the request
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14374](https://github.com/microsoft/TypeScript/issues/14374) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`, `VS Code Tracked`, `Needs Human Review`)

**Dom d\.ts does not define event\.target\.parentNode**

*VSCode autocomplete fails to list parentNode on event.target because the DOM type definitions omit that property.*

 * (7.5 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/14374#issuecomment-1968562317) **Vallek** said "Still not fixed?"
 * [today](https://github.com/microsoft/TypeScript/issues/14374#issuecomment-5458859058) **RyanCavanaugh** explained that event.target is EventTarget|null rather than Node and demonstrated narrowing it with instanceof Node before accessing parentNode
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#14575](https://github.com/microsoft/TypeScript/issues/14575) (Closed, `Bug`, `Help Wanted`, `Domain: API`, `Domain: JSDoc`, `Needs Human Review`)

**JSDoc comment nodes are not traversed and their parents are sent even if they should not**

*JSDoc comment nodes incorrectly retain parent pointers when parent tracking is disabled and aren’t traversed by forEachChild.*

 * (7.5 years ago) **RyanCavanaugh** added label `Domain: JSDoc`, set milestone to `Backlog`, and removed from milestone `Community`
 * [today](https://github.com/microsoft/TypeScript/issues/14575#issuecomment-5458869598) **RyanCavanaugh** explained that the behavior was in the pre-TypeScript-7 JavaScript Compiler API, which had been superseded by the TypeScript 7 API and was no longer being developed, and that changes to createSourceFile, JSDoc parent pointers, or forEachChild traversal could not be accepted
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#15514](https://github.com/microsoft/TypeScript/issues/15514) (Closed, `Bug`, `Domain: Something Else`, `Needs Human Review`)

**Cannot have array binding patterns without iterable extensions**

*Array destructuring in declarations triggers a missing iterator error instead of a destructuring error, while object destructuring yields no error.*

 * **mhegazy** added to milestone `Future`
 * **sandersn** unassigned **sandersn**
 * **RyanCavanaugh** added label `Domain: Something Else`
 * [today](https://github.com/microsoft/TypeScript/issues/15514#issuecomment-5458899027) **RyanCavanaugh** demonstrated that the declaration with destructuring parameters produced no diagnostics in TypeScript 2.2.1 and the current nightly
 * **RyanCavanaugh** added label `Needs Human Review`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#32367](https://github.com/microsoft/TypeScript/issues/32367) (Open, `Bug`, `Domain: JavaScript`, **sandersn**)

**JS typedef merged with default export class behaves strangely**

*A JSDoc typedef named 'default' merged with a default-export class triggers inconsistent type resolution and errors on value usage.*

 * [3 days ago](https://github.com/microsoft/TypeScript/issues/32367#issuecomment-5417803594) **weswigham** noted that the current nightly compiles files without diagnostics despite duplicate type-level default exports and suggested it should report a Duplicate identifier error
 * [yesterday](https://github.com/microsoft/TypeScript/issues/32367#issuecomment-5445732587) **RyanCavanaugh** said "Isn't the bare typedef default just declaring a local non-exported thing named default ? Would be illegal in TS but this isn't TS"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/32367#issuecomment-5445829779) **weswigham** said "typedefs are always exported."
 * (today) **RyanCavanaugh** removed label `Needs Human Review`, and assigned to **sandersn**

### [Issue microsoft/TypeScript#40023](https://github.com/microsoft/TypeScript/issues/40023) (Closed, `Infrastructure`, **jakebailey**, **RyanCavanaugh**)

**Clean up old branches in the repo?**

*Request to delete or archive five-year-old unmerged branches to clean up the repository.*

 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/40023#issuecomment-1987335818) **rubiesonthesky** said "It seems that @jakebailey has not had boring meetings either! :D "
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/40023#issuecomment-1987515163) **jakebailey** said "I deleted a bunch, but yes, I didn't actually pull the trigger to delete all of the other old branches."
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/40023#issuecomment-5416694729) **jakebailey** said "I'll finally be doing this cleanup soon. Backup of the branches to delete are here: https://gist.github.com/jakebailey/25e324d1357d9e65078e47ea347d8e69"
 * [today](https://github.com/microsoft/TypeScript/issues/40023#issuecomment-5457273212) **jakebailey** said "Deleted a few hundred branches 😄 "
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#4539](https://github.com/microsoft/TypeScript/issues/4539) (Closed, `Bug`, `Fixed`, `Help Wanted`, `Domain: JSX/TSX`, `Needs Human Review`)

**Poor error recovery in jsx elements**

*TypeScript’s JSX parser emits multiple confusing errors and fails to recover properly from malformed element attributes.*

 * (7.5 years ago) **RyanCavanaugh** added label `Domain: JSX/TSX`, set milestone to `Backlog`, and removed from milestone `Community`
 * [today](https://github.com/microsoft/TypeScript/issues/4539#issuecomment-5455630775) **RyanCavanaugh** noted that the issue was fixed in the current nightly, illustrated the reported errors with tsc --jsx preserve, and clarified that JSX expression-valued attributes require braces
 * (today) **RyanCavanaugh** added labels `Needs Human Review`, `Fixed`
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#4586](https://github.com/microsoft/TypeScript/issues/4586) (Closed, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Object\.constructor isn't implemented specifically enough**

*TypeScript types .constructor as generic Function, blocking extending real constructors and requiring more precise lib.d.ts constructor types.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/4586#issuecomment-1300944752) **KamilSzot** shared a workaround for typing the constructor property via an interface, demonstrated examples, outlined limitations with inheritance, and suggested a possible solution
 * **RyanCavanaugh** added label `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/4586#issuecomment-5455680526) **RyanCavanaugh** explained that assigning typeof Bar to an instance’s .constructor is unsafe due to lack of static-side class assignability enforcement and .constructor’s mutability
 * (today) **RyanCavanaugh** closed the issue

