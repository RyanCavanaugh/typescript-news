# Report for 2025-11-28 (Friday, November 28th, 2025)

7 different users commented on 11 different issues.

## Recommended Actions

 * Response Recommended
    * @sparr asked for a way to disable error checking of .ts sources in node_modules in [microsoft/TypeScript#40426](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3590991290)
    * @Squidgical asked for default-export support for type aliases in verbatimModuleSyntax in [microsoft/TypeScript#41409](https://github.com/microsoft/TypeScript/issues/41409#issuecomment-3591638904)
    * @diegoimbert requested support for typed SQL queries in Windmill in [microsoft/TypeScript#49552](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-3590394392)
    * @Squidgical provided repro steps for a TypeScript bug in [microsoft/TypeScript#51434](https://github.com/microsoft/TypeScript/issues/51434#issuecomment-3591758569)
    * @TyIsI asked whether this behavior should be documented in [microsoft/TypeScript#62815](https://github.com/microsoft/TypeScript/issues/62815#issuecomment-3590639917)
    * @sparr asked why it's targeting ES5 despite setting compilerOptions.target to ES6 or ES2018 in [microsoft/TypeScript#62816](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591044742)
    * @sparr asked for clarification about why producing invalid code is considered "working as intended" in [microsoft/TypeScript#62816](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591683354)

## Activity Summary

### [Issue microsoft/TypeScript#34969](https://github.com/microsoft/TypeScript/issues/34969) (Closed, `Suggestion`, `Awaiting More Feedback`)

**need "libRoots" in tsconfig\.json for private node\-runtime type definition**

*Add a libRoots compiler option to tsconfig.json to support custom private Node runtime type definitions.*

 * **RyanCavanaugh** added label `Suggestion`
 * [6 years ago](https://github.com/microsoft/TypeScript/issues/34969#issuecomment-551997239) **RyanCavanaugh** said "There are about a dozen other ways to get files into your program, so some discussion of why those don't work well for you would be interesting to hear"
 * [6 years ago](https://github.com/microsoft/TypeScript/issues/34969#issuecomment-560312627) **baslr** said "@eczn does typeRoots not work?"
 * (today) **eczn** closed the issue

### [Issue microsoft/TypeScript#40426](https://github.com/microsoft/TypeScript/issues/40426) (Open, `Suggestion`, `Awaiting More Feedback`)

**Disable type checking for node\_modules entirely**

*Allow disabling TypeScript type checking for node_modules to avoid build errors caused by external libraries’ faulty type definitions.*

 * [13 weeks ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3236263649) **onyedikachi23** said "It's almost 5 yrs now. @RyanCavanaugh Please 🙏 add the feature."
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3257038644) **iva2k** suggested adding an option to silence node_modules type check messages while still importing types
 * [12 weeks ago](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3257296565) **onyedikachi23** praised the proposed option to silence node_module type check messages while preserving type propagation
 * [today](https://github.com/microsoft/TypeScript/issues/40426#issuecomment-3590991290) **sparr** encountered error checking in excluded node_modules and requested how to disable it

### [Issue microsoft/TypeScript#41409](https://github.com/microsoft/TypeScript/issues/41409) (Open, `Suggestion`, `Awaiting More Feedback`)

**export default type**

*Add support for `export default type` syntax to allow directly default-exporting type aliases in TypeScript.*

 * [2.2 years ago](https://github.com/microsoft/TypeScript/issues/41409#issuecomment-1712528877) **AndreiSoroka** reported a bug in import syntax after converting a default export to a named type export
 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/41409#issuecomment-2109560289) **movahhedi** said "For those who were looking for "Type annotations for export default", follow #13626."
 * [18 weeks ago](https://github.com/microsoft/TypeScript/issues/41409#issuecomment-3092628997) **Gouvernathor** explained that marking a type in an export declaration works but is indirect and that combining 'export type { IFraction as default }' with 'export default Implementation' errors, forcing clients to use a named import instead of a default import
 * [later](https://github.com/microsoft/TypeScript/issues/41409#issuecomment-3591638904) **Squidgical** expressed desire to default export type aliases in verbatimModuleSyntax due to current limitations causing workarounds

### [PR microsoft/TypeScript#49552](https://github.com/microsoft/TypeScript/pull/49552) (Open, `Experiment`, `Author: Team`, `For Uncommitted Bug`, **rbuckton**)

**More specific TemplateStringsArray type for tagged templates**

*Proposal to refine TemplateStringsArray types in TypeScript to enable literal-aware interpolation for tagged templates*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-2715244649) **ssalbdivad** said "@rbuckton So surely today is the day we have been waiting for to merge this performance-bottlenecked PR? 😅"
 * [35 weeks ago](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-2755704370) **porsager** said "Pleeeeease reconsider merging this! I mean... Doom was implemented in Typescript but we can't do this? 😥"
 * [15 weeks ago](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-3173673073) **sosoba** noted that Ts 5.9 still didn't provide types for TemplateStringsArray
 * [today](https://github.com/microsoft/TypeScript/pull/49552#issuecomment-3590394392) **diegoimbert** said "Would really love it, it would enable me to have typed sqlQUERIES in Windmill :)"

### [Issue microsoft/TypeScript#51434](https://github.com/microsoft/TypeScript/issues/51434) (Open, `Needs Investigation`)

**Random reports of error 7022 \(implicitly has type 'any' because self\-reference\)**

*TypeScript 4.7.4 regression causes error 7022 by implicitly inferring 'any' for self-referencing variables.*

 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/51434#issuecomment-1375166349) **Compositr** said "Yeah, I've noticed it sometimes breaks when typing a dot on larger projects for me too. I agree that this kind of nullifies the point of IntelliSense if it can't help you the instant you need it"
 * [2.4 years ago](https://github.com/microsoft/TypeScript/issues/51434#issuecomment-1604303875) **voliva** verified the issue was fixed in version 5.0.4 onward and asked whether to keep the issue open to add a regression test
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/51434#issuecomment-1885910576) **tobz1000** demonstrated that the error still occurred in TS 5.3.2 and noted that removing the explicit assignment prevented it
 * [later](https://github.com/microsoft/TypeScript/issues/51434#issuecomment-3591758569) **Squidgical** described a TypeScript type-checking issue involving mutually dependent record-returning functions and provided a code reproduction

### [PR microsoft/TypeScript#53017](https://github.com/microsoft/TypeScript/pull/53017) (Open, `For Backlog Bug`, **ahejlsberg**)

**Infer type parameters from indexes on those parameters**

*Infer generic type parameters in TypeScript based on index accesses of those parameters.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-2353627950) **typescript-bot** provided an installable tgz link and instructions to test the TypeScript 5.7.0-insiders build, including a playground link and npm module reference
 * [1.1 years ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-2353753077) **jakebailey** said "I can't say I'm an expert here but I can certainly try to review it if/when things are settled; I'm just always one to run extended tests and make playgrounds 😄 "
 * [50 weeks ago](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-2538911899) **jcalz** said "cross-linking #20126 here (it's mentioned above but hard to find)"
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591670468) **jakebailey** requested the TypeScript bot to test and pack
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591670501) **typescript-bot** reported jobs starting and provided status and results links
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591674246) **typescript-bot** provided an installable tgz and links for testing the build
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591684397) **typescript-bot** reported DT tests ran and found an unused '@ts-expect-error' directive error in rdfjs__data-model
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591696488) **typescript-bot** reported user test results comparing main and pull merge, noted an infrastructure git clone failure and new TS2345 type errors in webpack configs
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591710203) **typescript-bot** provided the requested performance run results comparing baseline to the PR
 * [later](https://github.com/microsoft/TypeScript/pull/53017#issuecomment-3591733538) **typescript-bot** provided comparative tsc results for top 400 repos, highlighted build failures in react-navigation/react-navigation, and requested a review

### [PR microsoft/TypeScript#54029](https://github.com/microsoft/TypeScript/pull/54029) (Open, `For Backlog Bug`, **ahejlsberg**)

**Improve inference for context sensitive functions within reverse mapped types**

*Enhance TypeScript’s inference algorithm to better handle context-sensitive functions within reverse mapped types.*

 * created by **Andarist**
 * **typescript-bot** added label `For Backlog Bug`
 * **sandersn** assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591670868) **jakebailey** requested the TypeScript bot to test and pack
 * [later](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591670904) **typescript-bot** posted CI job statuses and results with links
 * [later](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591677200) **typescript-bot** provided an installable tgz and testing instructions via package.json, along with links to a playground and npm module
 * [later](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591684547) **typescript-bot** informed that the DT test results were ready, reported that everything looked the same, and provided a link to the log
 * [later](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591701794) **typescript-bot** posted the results of the requested perf run for tsc showing comparison metrics
 * [later](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591725156) **typescript-bot** reported test results and noted a git clone failure, otherwise everything looked good
 * [later](https://github.com/microsoft/TypeScript/pull/54029#issuecomment-3591736549) **typescript-bot** ran tsc on the top 400 repositories comparing main and refs/pull/54029/merge and reported everything looked good

### [PR microsoft/TypeScript#56300](https://github.com/microsoft/TypeScript/pull/56300) (Open, `For Backlog Bug`, **weswigham**, **ahejlsberg**)

**Default reverse mapped type inference to its constraint**

*Default reverse mapped type inference to the constraint if no specific type is provided*

 * [2 years ago](https://github.com/microsoft/TypeScript/pull/56300#issuecomment-1792868141) **typescript-bot** reported that the DT test results were ready and unchanged
 * (2 years ago) **sandersn** assigned to **weswigham**, **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/56300#issuecomment-3591670649) **jakebailey** requested the TypeScript bot to test and pack
 * [later](https://github.com/microsoft/TypeScript/pull/56300#issuecomment-3591670694) **typescript-bot** reported CI job statuses for various commands with links to started builds and results
 * [later](https://github.com/microsoft/TypeScript/pull/56300#issuecomment-3591674443) **typescript-bot** provided an installable tgz with usage instructions and links to a playground and npm module
 * [later](https://github.com/microsoft/TypeScript/pull/56300#issuecomment-3591684614) **typescript-bot** reported that the DT test results were ready and unchanged
 * [later](https://github.com/microsoft/TypeScript/pull/56300#issuecomment-3591697072) **typescript-bot** reported that user tests encountered an infrastructure failure but otherwise passed
 * [later](https://github.com/microsoft/TypeScript/pull/56300#issuecomment-3591713758) **typescript-bot** posted the requested performance run results
 * [later](https://github.com/microsoft/TypeScript/pull/56300#issuecomment-3591735748) **typescript-bot** reported that running the top 400 repos with tsc on main and the PR merge looked good

### [Issue microsoft/TypeScript#62815](https://github.com/microsoft/TypeScript/issues/62815) (Closed, `Working as Intended`)

**Getting error 2576 when accessing static methods of a class as a passed parameter\.**

*Invoking a static class method on a parameter typed as the class instance leads to TypeScript error 2576.*

 * created by **TyIsI**
 * [today](https://github.com/microsoft/TypeScript/issues/62815#issuecomment-3590630122) **MartinJohns** explained how to access static members by using typeof Fafo1 instead of an instance of the class
 * [today](https://github.com/microsoft/TypeScript/issues/62815#issuecomment-3590639917) **TyIsI** acknowledged that using typeof solved the issue, speculated on prototype comparison behavior, and asked whether this should be documented due to confusing error

### [Issue microsoft/TypeScript#62816](https://github.com/microsoft/TypeScript/issues/62816) (Closed, `Question`)

**\`tsc\` transpile js to js converts Set iteration loops to invalid numeric key indexing**

*Transpiling JavaScript with tsc’s allowJs option converts Set for-of loops into invalid .length-based index loops.*

 * created by **sparr**
 * [today](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591029614) **MartinJohns** explained that targeting ES5 disables "for of" loops and Set support and concluded that the behavior was working as intended
 * [today](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591044742) **sparr** said "Why is it targeting ES5 when my compilerOptions.target is ES6 or ES2018 or otherwise?"
 * [today](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591045909) **MartinJohns** explained that specifying input files on the command line ignores tsconfig and that without a specified target the compiler defaults to ES5
 * [later](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591683354) **sparr** thanked the maintainers and expressed confusion about invalid code being "working as intended"
 * [later](https://github.com/microsoft/TypeScript/issues/62816#issuecomment-3591703024) **MartinJohns** explained that downleveling to ES5 intentionally produced the correct for-of loop code and that enabling type checks would warn about missing length properties

