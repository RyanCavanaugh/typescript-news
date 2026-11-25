# Report for 2026-11-20 (Friday, November 20th, 2026)

19 different users commented on 47 different issues.

## Recommended Actions

 * Response Recommended
    * @heXaCo0l asked for an update on the plan in [microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-7047585063)
    * @ClementValot asked about the TypeScript team's current and future position on the issue in [microsoft/TypeScript#8306](https://github.com/microsoft/TypeScript/issues/8306#issuecomment-7064873524)

## Activity Summary

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*The TypeScript 7.1 iteration plan outlines release milestones and planned compiler, editor, library, API, and performance improvements.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6285163659) **erlichmen** asked when the TypeScript 7.1.0 beta would be published and whether users should build it from the `release-7.1` branch
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6297602298) **DanielRosenwasser** announced that the beta was published, the blog post was available, and the v7.1-beta tag had been created
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-6949297487) **sosoba** asked whether the 7.1 RC and stable release plan would be updated
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-7047585063) **heXaCo0l** said "@DanielRosenwasser any update on the plan ? "
 * [later](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-7061436783) **remcohaszing** mentioned that a release candidate was reportedly planned for December 1 and a stable release for the second week of December, while noting the information was unconfirmed

### [Issue microsoft/TypeScript#64668](https://github.com/microsoft/TypeScript/issues/64668) (Closed, `Bug`)

**panic: Unhandled case in Node\.MemberList**

*Nightly TypeScript crashes when evaluating an enum member referencing a class in a same-named namespace.*

 * **RyanCavanaugh** added to milestone `Backlog`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64668#issuecomment-6106820085) **andre-fajar-n** said "Could you share how to reproduce this bug? @YuanchengJiang "
 * [5 weeks ago](https://github.com/microsoft/TypeScript/issues/64668#issuecomment-6107485244) **YuanchengJiang** provided reproduction steps, commit references, build configuration, and operating system details
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64743](https://github.com/microsoft/TypeScript/pull/64743) (Closed, `For Backlog Bug`)

**Fix enum crash when namespace and enum share a name**

*Fix an enum evaluation crash when a merged namespace export is incorrectly treated as an enum member.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6143495673) **smg99** said "@microsoft-github-policy-service agree"
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6207033948) **smg99** clarified that they submitted the PR independently, offered to sign the Microsoft CLA personally, and noted that the AST MemberList review finding was addressed in commit d064a4c4
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/64743#issuecomment-6283523879) **smg99** stated that they had signed the CLA and asked @jakebailey to review
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65098](https://github.com/microsoft/TypeScript/issues/65098) (Open, `Suggestion`, `Possible Improvement`, **gabritto**)

**TS7\.1 importing \.json with type: something still parses the JSON file even though ambient module declaration is used**

*TypeScript 7.1 unnecessarily parses JSON imports even when matching ambient module declarations with import attributes provide their types.*

 * (3 days ago) **RyanCavanaugh** added label `Bug`, set milestone to `TypeScript 7.1.1 RC`, and assigned to **gabritto**
 * (today) **gabritto** added label `Suggestion`, removed label `Bug`, set milestone to `Backlog`, and removed from milestone `TypeScript 7.1.1 RC`
 * [today](https://github.com/microsoft/TypeScript/issues/65098#issuecomment-7048140558) **gabritto** explained that the behavior was intentional and predated #63931, citing ambient-module resolution, file-processing order, and import-attribute constraints
 * [today](https://github.com/microsoft/TypeScript/issues/65098#issuecomment-7048363637) **Knagis** questioned whether imports with a non-JSON type attribute should parse JSON files, noting that the JavaScript specification requires `{ type: "json" }` while bundlers may configure different behavior
 * [today](https://github.com/microsoft/TypeScript/issues/65098#issuecomment-7049233144) **gabritto** asked whether disabling `resolveJsonModule` while permitting `.json` imports with `with { "type": "json" }` would solve the issue, and requested the issue’s impact in the full codebase
 * **gabritto** added label `Possible Improvement`
 * [today](https://github.com/microsoft/TypeScript/issues/65098#issuecomment-7049517235) **Knagis** explained that strict JSON resolution requiring explicit import types would address significant game-project impact, while describing constraints around designer-exported JSON assets and existing URL-import workarounds

### [PR microsoft/TypeScript#65359](https://github.com/microsoft/TypeScript/pull/65359) (Closed, `For Backlog Bug`)

**Fix JSX intrinsic tag error reporting**

*Improve JSX intrinsic tag diagnostics by eliminating duplicates, pinpointing errors on tag names, and preserving closing-tag symbol resolution.*

 * (2 weeks ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * (today) **ayushtripathi-45** closed the issue

### [Issue microsoft/TypeScript#65516](https://github.com/microsoft/TypeScript/issues/65516) (Open, `Needs Investigation`, **andrewbranch**)

**Content mapper ignore directives need diagnostic\-code selectors**

*Add diagnostic-code selectors to content-mapper ignore directives so framework diagnostics can be suppressed without hiding unrelated errors.*

 * (3 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **andrewbranch**
 * **andrewbranch** added to milestone `TypeScript 7.1.1 RC`
 * [today](https://github.com/microsoft/TypeScript/issues/65516#issuecomment-7045966690) **andrewbranch** questioned whether code generation could include an index signature to address excess property checking and expressed concern that the proposed functionality could broadly disable TypeScript errors

### [Issue microsoft/TypeScript#65558](https://github.com/microsoft/TypeScript/issues/65558) (Closed, `Working as Intended`)

**TS7 JSDoc \`@overload\` is ignored on \`const\` arrow function \(works in 6\.0\.2, not in 7\.0\.2\)**

*TypeScript 7.0.2 regresses by ignoring JSDoc `@overload` annotations on `const` arrow functions, unlike function declarations and TypeScript 6.0.3.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65558#issuecomment-6977922609) **zhengdaodeguL** asked a maintainer to assign a milestone to the issue before submitting a pull request
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65558#issuecomment-6984746122) **RyanCavanaugh** said "https://github.com/microsoft/TypeScript/blob/e086ad3b8205668290a81baed890c536047003db/tsc/CHANGES.md?plain=1#L325"
 * **RyanCavanaugh** added label `Working as Intended`
 * [today](https://github.com/microsoft/TypeScript/issues/65558#issuecomment-7054839068) **github-actions[bot]** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **github-actions[bot]** closed the issue

### [Issue microsoft/TypeScript#65559](https://github.com/microsoft/TypeScript/issues/65559) (Closed, `Not a Defect`)

**Fix: small edits reshuffle the \`\-\-checkers\` partition**

*Small file edits unpredictably reshuffle checker assignments, causing check-time variance; quantizing file weights is proposed to stabilize partitioning.*

 * created by **ubugeeei**
 * **RyanCavanaugh** added label `Not a Defect`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/65559#issuecomment-6984291729) **RyanCavanaugh** clarified that the proposed fix still allowed a one-node change to move a file and alter subsequent assignments, so no invariant could be maintained
 * [today](https://github.com/microsoft/TypeScript/issues/65559#issuecomment-7054838296) **github-actions[bot]** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **github-actions[bot]** closed the issue

### [PR microsoft/TypeScript#65590](https://github.com/microsoft/TypeScript/pull/65590) (Closed, `Author: Team`, `For Uncommitted Bug`, **andrewbranch**)

**\[api\] AST predicate APIs**

*Add API predicate functions for identifying AST node categories and structures that cannot be auto-generated.*

 * (yesterday) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **andrewbranch**
 * (today) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#65597](https://github.com/microsoft/TypeScript/issues/65597) (Open, **RyanCavanaugh**, **Copilot**)

**Downlevel optional chaining loses \`this\` for parenthesized callees with \`\!\`, \`as\` or type arguments, and for parenthesized template tags**

*Downlevel optional chaining incorrectly loses the method receiver for parenthesized callees using non-null assertions, type assertions, type arguments, or template tags.*

 * created by **zloirock**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [Issue microsoft/TypeScript#65598](https://github.com/microsoft/TypeScript/issues/65598) (Closed, `Bug`)

**Calls through \`\#private\` members lose \`this\` below ES2022 when the callee is parenthesized or has \`\!\`, \`as\` or \`satisfies\`**

*Downlevel compilation loses the correct `this` receiver for calls through `#private` methods when callees are parenthesized or type-modified.*

 * created by **zloirock**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `TypeScript 7.1.1 RC`
 * (today) **weswigham** closed the issue

### [Issue microsoft/TypeScript#65600](https://github.com/microsoft/TypeScript/issues/65600) (Open, **RyanCavanaugh**, **Copilot**)

**7\.0 regression: expando property on a function declaration is dropped when a merged namespace exports a type with the same name \(TS2339\)**

*TypeScript 7.0 regresses by dropping function expando properties when merged namespaces export a type with the same name, causing TS2339 errors.*

 * created by **MartinFerret**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#65602](https://github.com/microsoft/TypeScript/pull/65602) (Closed, `For Milestone Bug`)

**fix\(65598\): preserve this binding in wrapped private member calls**

*Ensure wrapped calls to private members preserve the correct `this` binding.*

 * created by **a-tarasyuk**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (today) **typescript-automation[bot]** added label `For Milestone Bug`, and removed label `For Uncommitted Bug`
 * (today) **weswigham** closed the issue

### [PR microsoft/TypeScript#65603](https://github.com/microsoft/TypeScript/pull/65603) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Allow expando assignments to merge with same\-named type\-only namespace members**

*Allow expando assignments to merge with same-named type-only namespace members while preserving safe declaration emission and alias behavior.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/65603#issuecomment-7045684732) **RyanCavanaugh** said "@copilot mcfly please"
 * [today](https://github.com/microsoft/TypeScript/pull/65603#issuecomment-7045821495) **Copilot** restacked the changes through the binder fix, declaration emit fix, and baseline updates, noting that the final tree matched the pre-restack head

### [PR microsoft/TypeScript#65604](https://github.com/microsoft/TypeScript/pull/65604) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Use the built\-in Actions token for three workflows**

*Replace the bot with GitHub Actions’ built-in token across three workflows.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#65605](https://github.com/microsoft/TypeScript/issues/65605) (Open, `Bug`, **RyanCavanaugh**, **Copilot**)

**Declaration emit exports the renamed locals of reserved\-word expando members after the first one**

*TypeScript 7.x declaration emit incorrectly exports renamed locals for reserved-word expando members after the first, causing declarations to allow nonexistent runtime properties.*

 * created by **ktfth**
 * (today) **RyanCavanaugh** added label `Bug`, set milestone to `Backlog`, and assigned to **Copilot**, **RyanCavanaugh**

### [PR microsoft/TypeScript#65606](https://github.com/microsoft/TypeScript/pull/65606) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Keep renamed reserved\-word expando locals private in declaration emit**

*Fix declaration emit so renamed locals for reserved-word expando members remain private while only their aliases are exported.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`

### [Issue microsoft/TypeScript#65607](https://github.com/microsoft/TypeScript/issues/65607) (Open, `Needs Investigation`, `Domain: check: Order Dependence`, **jakebailey**)

**Moving an unrelated \`new Schema\<T\>\(…, options\)\` above a mongoose model turns \`typeof Model extends Model\<infer R\>\` into \`never\`**

*An unrelated Mongoose schema’s declaration order causes TypeScript to infer `never` when extracting a model’s raw type via a conditional type.*

 * created by **jltrv**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65608](https://github.com/microsoft/TypeScript/pull/65608) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix various LS text insertion / quoting bugs**

*Fixes multiple language server text insertion and quoting bugs, following the approach used in issue #64839.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65609](https://github.com/microsoft/TypeScript/pull/65609) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Fix flaky fanotify cross\-watcher test**

*Loosen the fanotify cross-watcher test to tolerate duplicate update events emitted by the operating system during non-atomic file writes.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#65610](https://github.com/microsoft/TypeScript/pull/65610) (Open, `Author: Team`, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Preserve \`this\` in downleveled optional chains wrapped in erased type syntax or used as template tags**

*Preserve method receivers when downleveling optional chains wrapped in erased type syntax or used as template tags.*

 * created by **RyanCavanaugh**
 * (today) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65611](https://github.com/microsoft/TypeScript/issues/65611) (Open)

**\[ServerErrors\]\[JavaScript\] main**

*Main reports JavaScript server errors from analyzing 300 popular TypeScript repositories, with 16 interesting changes, 26 timeouts, and 30 unknown failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051275230) **typescript-automation[bot]** reported a panic in the textDocument/diagnostic handler affecting Chart.js, with stack trace, artifacts, and replay commands provided
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051276177) **typescript-automation[bot]** reported a panic in `textDocument/typeDefinition` caused by an unexpected AST trivia kind, affecting `processing/p5.js`, and provided artifact and replay references
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051277029) **typescript-automation[bot]** reported a panic during textDocument/completion caused by an unexpected KindIdentifier in KindImportDeclaration trivia, affecting the decolua/9router repository
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051277868) **typescript-automation[bot]** reported a panic during textDocument/completion caused by an unexpected KindIdentifier in KindCallExpression trivia, affecting the zhaoolee/ChromeAppHeroes repository
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051278788) **typescript-automation[bot]** reported a panic in textDocument/references during cross-project handling, caused by an unexpected KindIdentifier trivia token under KindBinaryExpression
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051279624) **typescript-automation[bot]** reported a panic in textDocument/implementation during cross-project handling caused by an unexpected KindIdentifier in a KindBinaryExpression's trivia
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051280531) **typescript-automation[bot]** reported a textDocument/hover panic involving an unexpected AST trivia kind and provided affected-repository artifacts and replay commands
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051281451) **typescript-automation[bot]** reported a panic during `textDocument/hover` caused by an unexpected AST trivia relationship, affecting the amark/gun repository and providing diagnostic artifacts and replay commands
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051282352) **typescript-automation[bot]** reported a premature server connection closure in react/react and provided affected requests and reproduction steps
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051283317) **typescript-automation[bot]** reported that the new server closed prematurely with an undefined error for usebruno/bruno, while the old server completed successfully, and provided recent LSP requests and a reproduction command
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051284197) **typescript-automation[bot]** reported a premature server connection closure affecting tastejs/todomvc, included recent LSP requests, and provided repository reproduction steps and artifact links
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051285064) **typescript-automation[bot]** reported a panic in `textDocument/implementation` during cross-project handling, caused by an unexpected AST trivia kind
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051286013) **typescript-automation[bot]** reported a panic in the TypeScript language service while handling a cross-project textDocument/implementation request, involving unexpected AST trivia on a call expression
 * [today](https://github.com/microsoft/TypeScript/issues/65611#issuecomment-7051286913) **typescript-automation[bot]** reported a panic during cross-project handling in the TypeScript language service, involving an unexpected AST trivia kind and a references lookup stack trace

### [PR microsoft/TypeScript#65612](https://github.com/microsoft/TypeScript/pull/65612) (Closed, `Author: Team`, `For Uncommitted Bug`, **DanielRosenwasser**)

**Remove vestigial \`immediate\` keyword\.**

*Remove the unintended, vestigial `immediate` keyword from the codebase, as it was never part of the merged implementation.*

 * created by **DanielRosenwasser**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **DanielRosenwasser**
 * (today) **DanielRosenwasser** closed the issue

### [PR microsoft/TypeScript#65613](https://github.com/microsoft/TypeScript/pull/65613) (Closed, `Author: Team`, `For Milestone Bug`, **andrewbranch**)

**Content mapper diagnostic code selectors**

*Adds diagnostic code selectors to the content mapper, incorporating review feedback from the preceding pull request.*

 * created by **andrewbranch**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, and assigned to **andrewbranch**

### [Issue microsoft/TypeScript#65614](https://github.com/microsoft/TypeScript/issues/65614) (Open)

**\[ServerErrors\]\[TypeScript\] main**

*TypeScript’s main branch produced server errors while analyzing 300 popular GitHub repositories, with most runs timing out or failing.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054066190) **typescript-automation[bot]** reported a panic during textDocument/formatting caused by the assertion failure "Token end is child end"
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054067047) **typescript-automation[bot]** reported a panic in `textDocument/implementation` during cross-project handling, caused by an unexpected AST trivia kind
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054067964) **typescript-automation[bot]** reported a panic in textDocument/formatting caused by the failed assertion “Token end is child end” and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054068831) **typescript-automation[bot]** reported a nil pointer dereference panic in textDocument/codeAction, including a TypeScript checker stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054069822) **typescript-automation[bot]** reported a panic in the `textDocument/references` handler during cross-project processing involving an unexpected `KindIdentifier` trivia node
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054070685) **typescript-automation[bot]** reported an unhandled panic in textDocument/codeAction caused by an unsupported Node.Text KindObjectLiteralExpression case, affecting babel/babel
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054071569) **typescript-automation[bot]** reported a panic in textDocument/documentHighlight caused by an unexpected KindArrayLiteralExpression trivia state
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054072477) **typescript-automation[bot]** reported a panic in textDocument/documentHighlight caused by an unexpected KindCallExpression trivia state and provided the stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054073363) **typescript-automation[bot]** reported a panic while handling textDocument/hover caused by an unexpected KindCallExpression trivia state, affecting anomalyco/opencode and providing artifact and replay references
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054074315) **typescript-automation[bot]** reported a panic while handling a textDocument/hover request caused by an unexpected AST trivia kind, affecting the cheeriojs/cheerio repository and providing stack trace and replay artifact references
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054075210) **typescript-automation[bot]** reported a panic during `textDocument/hover` caused by unexpected AST trivia in the TypeScript language server and provided affected-repository artifacts and replay commands
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054075936) **typescript-automation[bot]** reported a panic in textDocument/implementation during cross-project handling, including the associated stack trace
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054076685) **typescript-automation[bot]** reported a panic in `textDocument/implementation` during cross-project handling caused by an unexpected AST trivia kind
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054077414) **typescript-automation[bot]** reported a panic during cross-project handling of textDocument/implementation involving an unexpected KindAwaitExpression trivia node
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054078080) **typescript-automation[bot]** reported a panic in textDocument/implementation during cross-project handling involving an unexpected AST node kind
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054078767) **typescript-automation[bot]** reported a panic while handling a cross-project `textDocument/references` request, caused by an unexpected AST trivia kind
 * [today](https://github.com/microsoft/TypeScript/issues/65614#issuecomment-7054079535) **typescript-automation[bot]** reported a panic in `textDocument/formatting` caused by a failed `Token end is child end` assertion

### [Issue microsoft/TypeScript#65615](https://github.com/microsoft/TypeScript/issues/65615) (Open)

**Declaration emit aliases an expando member to an out\-of\-scope or different identifier when the assigned value is an identifier**

*Declaration emit incorrectly aliases expando properties assigned from identifiers, producing out-of-scope or semantically wrong declarations instead of property types.*

 * created by **ktfth**

### [Issue microsoft/TypeScript#65616](https://github.com/microsoft/TypeScript/issues/65616) (Open, `Domain: check: Order Dependence`)

**\`\-\-incremental\`: unused import not reported after an edit when it appears only in an export's inferred type**

*Incremental TypeScript builds fail to report unused imports referenced only in an export’s inferred type after source edits.*

 * created by **bjornpagen**

### [PR microsoft/TypeScript#65617](https://github.com/microsoft/TypeScript/pull/65617) (Closed, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Produce union types when instantiating generic contextual types**

*Produce union types instead of selecting individual inference candidates when instantiating generic contextual types inferred from return types.*

 * created by **ahejlsberg**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, and assigned to **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055264204) **ahejlsberg** said "@typescript-bot test it"
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055265305) **typescript-automation[bot]** reported the status and results links for the initiated test, user test, DefinitelyTyped, and performance jobs
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055664586) **typescript-automation[bot]** reported new TS2353 errors in webpack user tests caused by the `intercept` property and requested investigation
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055670972) **typescript-automation[bot]** reported that the DT test results were ready and unchanged, and linked to the build log
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055783338) **typescript-automation[bot]** provided the requested performance run results comparing the baseline and PR
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055837443) **jakebailey** said "Looks like some new errors in those benchmarks."
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7055889110) **ahejlsberg** said "@jakebailey It needed a merge from main."
 * [today](https://github.com/microsoft/TypeScript/pull/65617#issuecomment-7056457477) **typescript-automation[bot]** reported that testing the top 400 repositories with `tsc` showed no differences between the baseline and PR and that everything looked good

### [PR microsoft/TypeScript#65618](https://github.com/microsoft/TypeScript/pull/65618) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Update deps**

*Update dependencies to accommodate new dprint formatting and resolve an audit finding.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**

### [PR microsoft/TypeScript#65619](https://github.com/microsoft/TypeScript/pull/65619) (Open, `Domain: Performance`, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Build set instead of binary searching for denormalized origins**

*Optimize denormalized union origin construction by using a type set for membership checks instead of repeated binary searches.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/65619#issuecomment-7057734601) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript/pull/65619#issuecomment-7057735682) **typescript-automation[bot]** reported that the performance test job started and linked to its build results
 * [today](https://github.com/microsoft/TypeScript/pull/65619#issuecomment-7058201437) **typescript-automation[bot]** reported the requested performance-run results, including compiler benchmark comparisons between the baseline and pull request

### [Issue microsoft/TypeScript#65620](https://github.com/microsoft/TypeScript/issues/65620) (Open)

**An assertion over a large union of string literals never finishes**

*TypeScript type checking hangs or scales quadratically when assertion narrowing intersects large unions of string literals with object types.*

 * created by **magurotuna**

### [PR microsoft/TypeScript#65621](https://github.com/microsoft/TypeScript/pull/65621) (Open, `Author: Team`, `For Backlog Bug`, **ahejlsberg**, **jakebailey**)

**Order types, symbols, and nodes by content instead of by ID**

*Order types, symbols, and nodes deterministically by content rather than creation IDs, interning identical types and eliminating ID-dependent output.*

 * created by **jakebailey**
 * (today) **typescript-automation[bot]** added labels `Author: Team`, `For Backlog Bug`, and assigned to **jakebailey**, **ahejlsberg**
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7058810918) **jakebailey** requested TypeScript bot runs for dt, user testing, top1000 testing, and performance testing
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7058811804) **typescript-automation[bot]** reported that automated jobs had started and listed their build and result statuses
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7059075808) **typescript-automation[bot]** reported that the DT test run failed and linked to the build log for details
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7059157452) **typescript-automation[bot]** reported new TS2589 errors in type-fest user tests when comparing the baseline and PR, and asked @jakebailey to investigate
 * [today](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7059223121) **typescript-automation[bot]** reported that the requested performance run results were available and included compiler baseline-versus-PR comparison metrics
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7060258049) **typescript-automation[bot]** reported results from comparing baseline and PR TypeScript compiler runs across the top 1,000 repositories, highlighting an unexpected change and ClickHouse/ClickStack build failures
 * [later](https://github.com/microsoft/TypeScript/pull/65621#issuecomment-7060258563) **typescript-automation[bot]** reported additional changes from the top 1,000 repositories suite, including build failures and TypeScript errors in vercel/ai examples

### [Issue microsoft/TypeScript#65623](https://github.com/microsoft/TypeScript/issues/65623) (Open)

**Panic during declaration emit with stripInternal on parenthesized or wrapped internal type**

*TypeScript crashes during declaration emit with `--stripInternal` when internal types are wrapped in parentheses or other type constructs.*

 * created by **ShakilUrRehman21**

### [PR microsoft/TypeScript#65624](https://github.com/microsoft/TypeScript/pull/65624) (Open, `For Uncommitted Bug`)

**Fix panic during declaration emit with stripInternal on parenthesized and wrapped types**

*Prevent declaration emit panics by propagating stripped internal types through parenthesized, operator, and array type wrappers.*

 * created by **ShakilUrRehman21**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#65625](https://github.com/microsoft/TypeScript/issues/65625) (Open)

**\[7\.1\] export ScriptTarget enum from typescript/sync and  typescript/async**

*Export the `ScriptTarget` enum from `typescript/sync` and `typescript/async` for consistent compiler options construction.*

 * created by **AviVahl**
 * [later](https://github.com/microsoft/TypeScript/issues/65625#issuecomment-7063494316) **AviVahl** said "FYI @andrewbranch, as you seem to be the one working on the API. 🙏 "

### [Issue microsoft/TypeScript#8306](https://github.com/microsoft/TypeScript/issues/8306) (Closed, `Won't Fix`, `Suggestion`)

**Support final classes \(non\-subclassable\)**

*Request support for a `final` class modifier that prevents subclassing and produces a compiler error when extension is attempted.*

 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/8306#issuecomment-3978027852) **Voltra** indicated willingness to investigate how `abstract` is implemented and potentially implement `final`
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/8306#issuecomment-3979439167) **Xample** said "@Voltra yes but your pr won’t be accepted and your work rolled back « Endgame ». You better convince ecma script to add final. "
 * [35 weeks ago](https://github.com/microsoft/TypeScript/issues/8306#issuecomment-4060516246) **TiMESPLiNTER** shared a decorator and ESLint plugin implementation for enforcing final classes and methods, along with usage examples and links to the related packages and repository
 * [later](https://github.com/microsoft/TypeScript/issues/8306#issuecomment-7064873524) **ClementValot** argued that recent JavaScript and TypeScript developments support broader adoption of class extendability contracts, and asked where the TypeScript team stood on the issue in 2027

