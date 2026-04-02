# Report for 2026-02-17 (Tuesday, February 17th, 2026)

16 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @tredondo asked about workarounds for avoiding JSDoc duplication for function overloads in [microsoft/TypeScript#407](https://github.com/microsoft/TypeScript/issues/407#issuecomment-3917888976)
    * @xixixao asked for a built-in helper for forcing tuple inference in [microsoft/TypeScript#44309](https://github.com/microsoft/TypeScript/issues/44309#issuecomment-3917247529)
    * @xixixao requested an idiomatic TypeScript tuple creation syntax in [microsoft/TypeScript#44309](https://github.com/microsoft/TypeScript/issues/44309#issuecomment-3919630118)
    * @Arlen22 provided logs and described reproduction steps in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041847)
    * @Arlen22 provided logs of preceding lines in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041859)
    * @Arlen22 provided a workaround in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041867)
    * @joshcartme asked for other workarounds in [microsoft/TypeScript#63152](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3917229422)

## Activity Summary

### [Issue microsoft/TypeScript#25945](https://github.com/microsoft/TypeScript/issues/25945) (Closed, `External`)

**macOS considers typescript files to be MPEG\-2 Transport Stream \- QuickLook and Spotlight do not work**

*macOS incorrectly identifies TypeScript (.ts) files as MPEG-2 transport streams, breaking QuickLook and Spotlight functionality.*

 * [16 weeks ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3457429664) **RyanCavanaugh** said "Is this the MacOS issue tracker? 😅"
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3463523226) **cryptolit0** mocked the project as being sponsored by Microsoft
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3649797068) **qgustavor** described that the .ts extension issue arose from a lack of file extension standardization across operating systems, noted that renaming the extension was impractical, and proposed future OS heuristics to distinguish file types
 * [today](https://github.com/microsoft/TypeScript/issues/25945#issuecomment-3916884301) **qgustavor** suggested adopting .cts and .mts over .ts to avoid conflicts and provided a migration guide

### [Issue microsoft/TypeScript#39998](https://github.com/microsoft/TypeScript/issues/39998) (Open, `Suggestion`, `Awaiting More Feedback`)

**Suggestion: perform excess property checks when spreading an inline object literal**

*Add excess property checks for inline object literals spread within other object literals to catch invalid properties.*

 * [1.7 years ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-2110801768) **vtgn** expressed disappointment about TypeScript's inability to catch validation errors early, noting they encountered the issue in a simple case
 * [25 weeks ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3223170523) **dpeter99** said "I have just run into this at work, while trying to figure out whay I wasn't getting "may only specify known properties" warnings."
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3730376223) **zacaj** critiqued the lack of validation for `satisfies` when spreads were used
 * [later](https://github.com/microsoft/TypeScript/issues/39998#issuecomment-3920632797) **OliverJAsh** mentioned that with exactOptionalPropertyTypes enabled, spread must be used for optional properties and provided examples

### [Issue microsoft/TypeScript#407](https://github.com/microsoft/TypeScript/issues/407) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: JSDoc`)

**JSDoc for methods with multiple signatures **

*Seeking strategies for writing concise JSDoc definitions that support IntelliSense for functions with multiple overloads.*

 * [3.9 years ago](https://github.com/microsoft/TypeScript/issues/407#issuecomment-1077950620) **P-Daddy** described a workaround for documenting overloaded functions using an interface with an any member and noted its limitations
 * [2.6 years ago](https://github.com/microsoft/TypeScript/issues/407#issuecomment-1616572744) **geoffreytools** described noticing that JSDoc tooltips are not shown for higher-order function return types and that existing workarounds obfuscate information, and requested a way to control tooltip display or manage JSDoc duplication
 * [1.2 years ago](https://github.com/microsoft/TypeScript/issues/407#issuecomment-2486684266) **SamB** noted that the title misled them into thinking it was a stale duplicate of the @overload JSDoc issue and pointed to issue #51005's clearer title
 * [today](https://github.com/microsoft/TypeScript/issues/407#issuecomment-3917888976) **tredondo** said "Apologies for pinging the issue, but another year has passed and I was wondering if there any workarounds for avoiding the duplication of JSDoc for function overloads."

### [Issue microsoft/TypeScript#44309](https://github.com/microsoft/TypeScript/issues/44309) (Open, `Suggestion`, `Awaiting More Feedback`)

**Infer a tuple type instead of array type when possible**

*Add a TypeScript compiler option to infer fixed-length tuple types instead of general arrays when possible.*

 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/44309#issuecomment-850532834) **echentw** reported a possible regression in tuple type inference when using map
 * [4.7 years ago](https://github.com/microsoft/TypeScript/issues/44309#issuecomment-850560921) **whzx5byb** linked related issues and a pull request
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/44309#issuecomment-2630230016) **Rudxain** provided additional use-cases demonstrating tuple type inference
 * [today](https://github.com/microsoft/TypeScript/issues/44309#issuecomment-3917247529) **xixixao** asked for a built-in helper to force tuple inference without readonly side effects
 * [today](https://github.com/microsoft/TypeScript/issues/44309#issuecomment-3917686627) **echentw** provided a workaround using a generic tuple function to infer tuple types
 * [later](https://github.com/microsoft/TypeScript/issues/44309#issuecomment-3919630118) **xixixao** said "@echentw Yeah, that's good, but I would really prefer to have an idiomatic TypeScript way of creating tuples, something that's so core to JS ( [a, b] )."

### [Issue microsoft/TypeScript#62008](https://github.com/microsoft/TypeScript/issues/62008) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support \`@import\` JSDoc tag for auto\-imports**

*Allow auto-import suggestions to generate JSDoc @import tag syntax instead of inline import(...) types for improved readability.*

 * **RyanCavanaugh** added label `Awaiting More Feedback`
 * [32 weeks ago](https://github.com/microsoft/TypeScript/issues/62008#issuecomment-3048488526) **rossrobino** said "This would be really nice!"
 * [32 weeks ago](https://github.com/microsoft/TypeScript/issues/62008#issuecomment-3050111484) **alexharri** expressed support for @import syntax, compared it to inline import style with examples, and suggested an auto-import feature defaulting to @import
 * [today](https://github.com/microsoft/TypeScript/issues/62008#issuecomment-3917172723) **apendua** said "I'd be happy to help with this one if it gets accepted."

### [PR microsoft/TypeScript#63137](https://github.com/microsoft/TypeScript/pull/63137) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update DOM types**

*Update DOM type definitions to accommodate planned changes for the upcoming 6.0 release.*

 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3900069759) **typescript-bot** reported tsc user test results comparing main and the pull request merge, noted one Git clone failure and otherwise everything looked good
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3900164989) **typescript-bot** provided the requested performance run results
 * [4 days ago](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3900223481) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the pull request merge resulted in no issues
 * [today](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3916572678) **jakebailey** requested typescript-bot to run various test commands
 * [today](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3916573035) **typescript-bot** posted CI build status updates for commands test top400, user test this, and run dt
 * [today](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3916664421) **typescript-bot** reported DT test results showing changed errors for the deno package
 * [today](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3916697709) **typescript-bot** reported tsc user test results comparing main and the pull request merge, noted one Git clone failure and otherwise everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63137#issuecomment-3916905055) **typescript-bot** reported that running tsc on the top 400 repos comparing main and the pull request merge resulted in no issues

### [PR microsoft/TypeScript#63139](https://github.com/microsoft/TypeScript/pull/63139) (Closed, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.3\.2 to 5\.3\.4**

*Update fast-xml-parser dependency from 5.3.2 to 5.3.4 to apply bug fixes and performance improvements.*

 * (3 days ago) **dependabot[bot]** added labels `dependencies`, `javascript`
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63139#issuecomment-3918526968) **dependabot[bot]** said "Superseded by #63155."
 * (today) **dependabot[bot]** closed the issue

### [PR microsoft/TypeScript#63142](https://github.com/microsoft/TypeScript/pull/63142) (Closed, `For Uncommitted Bug`)

**Fix \`from\` and \`with\` method types of \`Temporal\.PlainMonthDay\`**

*Adjust Temporal.PlainMonthDay.from and .with type signatures to accept era and eraYear parameters alongside year.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63142#issuecomment-3904350170) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63142#issuecomment-3904353035) **fabon-f** said "@microsoft-github-policy-service agree"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63149](https://github.com/microsoft/TypeScript/issues/63149) (Open)

**\[TS\]: Incorrect handling of \`JSDoc\` description of interface property**

*VS Code incorrectly strips parentheses-enclosed JSX tags from interface property JSDoc descriptions in hover tooltips.*

 * created by **psnet**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63150](https://github.com/microsoft/TypeScript/issues/63150) (Open, `Suggestion`, `Experience Enhancement`)

**\[JavaScript/TypeScript Language Hints\] Hide default \`Object\` properties/methods until manually typed just like in Rust\.**

*Enable hiding default JavaScript/TypeScript Object properties and methods from IntelliSense until manually typed, similar to Rust analyzer.*

 * created by **FrameMuse**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * [yesterday](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041807) **vs-code-engineering[bot]** suggested upgrading to the latest VS Code version and checking if the issue persisted
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041819) **Arlen22** reported that upgrading to the latest version did not fix the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041826) **mjbvz** instructed to collect the TS Server log in verbose mode, locate the semantic error log file, and share any errors or stack traces
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041847) **Arlen22** reported that the TS server repeatedly restarted after specific log entries despite restarting servers and testing multiple versions
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041859) **Arlen22** provided the preceding log lines and expressed uncertainty about their consistency
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3917041867) **Arlen22** described a workaround by keeping prisma.config.ts and other non-tsconfig files closed to prevent the issue while noting it was not a solution
 * **mjbvz** unassigned **mjbvz**

### [Issue microsoft/TypeScript#63152](https://github.com/microsoft/TypeScript/issues/63152) (Open)

**\.call selects the wrong overload, resulting in ts2554**

*Using .call on XMLHttpRequest.prototype.open incorrectly selects the longer overload and triggers a TS2554 error.*

 * created by **joshcartme**
 * [today](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3917210799) **MartinJohns** said "Duplicate of #38353."
 * [today](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3917229422) **joshcartme** thanked MartinJohns and asked for other workarounds due to lib.dom types preventing signature rewrite
 * [today](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3918753674) **MartinJohns** said "You can either use a type assertion, or you can bind the object like const bound = xhrOpen.bind(this); return bound(method, url); (I don't know if this has any performance implications.)"
 * [later](https://github.com/microsoft/TypeScript/issues/63152#issuecomment-3920845934) **nmain** suggested augmenting the Function type with fake variadic overloads and provided a Playground link and code snippet

### [Issue microsoft/TypeScript#63153](https://github.com/microsoft/TypeScript/issues/63153) (Closed, **DanielRosenwasser**, **Copilot**)

**Crash for declaration emit with nested binding pattern**

*The TypeScript compiler crashes when emitting declaration files for a constructor parameter with a nested binding pattern.*

 * created by **DanielRosenwasser**
 * [today](https://github.com/microsoft/TypeScript/issues/63153#issuecomment-3917463096) **DanielRosenwasser** said "Basically we just need to adjust walkBindingPattern to continue when it hits a binding pattern. Would be good to get some more tests with different types of binding patterns at different levels."
 * (today) **DanielRosenwasser** assigned to **Copilot**, **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#63154](https://github.com/microsoft/TypeScript/pull/63154) (Closed, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Fix crash in declaration emit with nested binding patterns**

*Declaration emit crashed on nested binding pattern parameter properties and now correctly skips nested patterns in walkBindingPattern with added tests.*

 * created by **Copilot**
 * (today) **Copilot** assigned to **Copilot**, **DanielRosenwasser**
 * **typescript-bot** added label `For Uncommitted Bug`
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#63155](https://github.com/microsoft/TypeScript/pull/63155) (Open, `For Uncommitted Bug`, `dependencies`, `javascript`)

**Bump fast\-xml\-parser from 5\.3\.2 to 5\.3\.6**

*Update fast-xml-parser to v5.3.6 to enhance entity processing security and performance*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `javascript`, `dependencies`, `javascript`
 * (today) **typescript-bot** added labels `For Uncommitted Bug`, `For Uncommitted Bug`

