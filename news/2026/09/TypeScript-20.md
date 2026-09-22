# Report for 2026-09-20 (Sunday, September 20th, 2026)

18 different users commented on 35 different issues.

## Recommended Actions

 * Response Recommended
    * @yunxu1019 reported that the issue cannot be reproduced in the latest VSCode and suggested adding a recursion counter in [microsoft/TypeScript#59047](https://github.com/microsoft/TypeScript/issues/59047#issuecomment-5762226464)
    * @RobertSandiford provided repro steps as requested in [microsoft/TypeScript#63358](https://github.com/microsoft/TypeScript/issues/63358#issuecomment-5752327256)
    * @RobertSandiford provided a link to a fix commit in [microsoft/TypeScript#63358](https://github.com/microsoft/TypeScript/issues/63358#issuecomment-5752930050)
    * @GeorgeGkas asked about the recommended strategy for build-time transforms with IDE type checking without compiler patching in [microsoft/TypeScript#63771](https://github.com/microsoft/TypeScript/issues/63771#issuecomment-5762826006)
    * @Abdellox asked for steps to reproduce, expected vs actual behavior, and environment details in [microsoft/TypeScript#64368](https://github.com/microsoft/TypeScript/issues/64368#issuecomment-5759018848)
    * @typescript-automation[bot] reported an access denied error for the 'run dt' pipeline in [microsoft/TypeScript#64372](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5763107668)

## Activity Summary

### [Issue microsoft/TypeScript#50209](https://github.com/microsoft/TypeScript/issues/50209) (Closed, `Bug`, `Help Wanted`, `Domain: Comment Emit`)

**Repeated single line comment after variable declaration in if/for block when targeting ES5**

*TypeScript 4.7.4 misplaces single-line comments and splits variable declarations in ES5 if/for blocks.*

 * [3.8 years ago](https://github.com/microsoft/TypeScript/issues/50209#issuecomment-1320732490) **toyobayashi** explained that they wrap preprocessor directives in comments before transpiling with tsc and then remove the comment markers afterward via a Node.js script to preserve directives in the output JavaScript files
 * (48 weeks ago) **RyanCavanaugh** added labels `Domain: Comment Emit`, `Needs Human Review`
 * **RyanCavanaugh** removed label `Needs Human Review`
 * [later](https://github.com/microsoft/TypeScript/issues/50209#issuecomment-5762634479) **RyanCavanaugh** said "ES5 output is no longer supported, so this is moot"
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#51376](https://github.com/microsoft/TypeScript/issues/51376) (Open, `Bug`, `Needs More Info`, `Help Wanted`, `Domain: Related Error Spans`, `Needs Human Review`)

**Spread operator with wrong optional property raises error on incorrect source line**

*TypeScript misreports error location when spreading an object with an optional property into a stricter type*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/51376#issuecomment-5737556389) **RyanCavanaugh** requested tsconfig.json settings, editor/extension version, and exact source to reproduce the error
 * (2 days ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/51376#issuecomment-5755811601) **laverdet** questioned if maintainers were using the same playground link and confirmed the repro on TS v6 and v7; provided code showing a confusing TS2322 error for attribute: "" under strict mode

### [Issue microsoft/TypeScript#59047](https://github.com/microsoft/TypeScript/issues/59047) (Open, `Bug`, `Needs More Info`, `Domain: Crashes`, `Needs Human Review`, **iisaduan**)

**TS Server fatal error:  Maximum call stack size exceeded**

*TS Server crashes with maximum call stack size exceeded error when opening a file containing syntax errors in VS Code*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/59047#issuecomment-5738321489) **RyanCavanaugh** requested that the user attach efront.js and verbose tsserver logs to reproduce the crash
 * (2 days ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/59047#issuecomment-5762226464) **yunxu1019** said "你在这几个溢出的函数外添加个临时的递归计数器，超过一定的域值输出当前节点就可以了吧。我在最近的版本的vscode上已经无法复现了，打开以后语法引擎只是不停地转圈，不会再崩溃了。"

### [Issue microsoft/TypeScript#63358](https://github.com/microsoft/TypeScript/issues/63358) (Open, `Bug`, `Needs More Info`, `Domain: JSX/TSX`, `Needs Human Review`)

**TSX error location error with location and JSX comment**

*A preceding JSX comment causes TypeScript to report a non-ReactNode type error on the comment instead of the expression.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63358#issuecomment-5739207853) **RyanCavanaugh** noted that the diagnostic could not be reproduced with TypeScript 5.0.4 and requested a self-contained project or exact React declaration version and JSX compiler settings to reproduce the TS2322 range issue
 * (2 days ago) **RyanCavanaugh** added labels `Needs Human Review`, `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript/issues/63358#issuecomment-5752327256) **RobertSandiford** provided reproduction steps and project configuration demonstrating a TS2322 error assigning 'Location' to 'ReactNode'
 * [today](https://github.com/microsoft/TypeScript/issues/63358#issuecomment-5752930050) **RobertSandiford** said "Fix here: https://github.com/RobertSandiford/TypeScript/commit/5fd2177180294078dab2b36ee0463e3acf07158c"

### [Issue microsoft/TypeScript#63771](https://github.com/microsoft/TypeScript/issues/63771) (Open, `Suggestion`, `Awaiting More Feedback`)

**Transformer Plugin or Compiler API**

*Requesting TypeScript team feedback on reintroducing a transformer plugin API versus continuing with the compiler API amid JS-Go integration challenges.*

 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63771#issuecomment-5360797703) **RyanCavanaugh** suggested gathering fresh takes on the new API and content mappers and requested specific scenarios not addressed
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63771#issuecomment-5360861448) **lppedd** noted that their requirement for a port of typescript-transform-paths was still valid and asked whether the current proposal covered those transformation APIs
 * [1 month ago](https://github.com/microsoft/TypeScript/issues/63771#issuecomment-5362968812) **RyanCavanaugh** stated that emit-side transforms were currently unsupported and expected to remain out of scope because many extensible type-erasing emitters exist
 * [later](https://github.com/microsoft/TypeScript/issues/63771#issuecomment-5762826006) **GeorgeGkas** asked what the recommended idiomatic approach was for custom file loading and build-time transformations with IDE support given that native emit-side transforms are unlikely to land soon

### [PR microsoft/TypeScript#64268](https://github.com/microsoft/TypeScript/pull/64268) (Open, `For Milestone Bug`, **RyanCavanaugh**)

**lib: ZonedDateTime\.toLocaleString must not accept a timeZone option**

*Restrict ZonedDateTime.toLocaleString’s options type to exclude timeZone by introducing a specialized interface extending Intl.DateTimeFormatOptions.*

 * (2 days ago) **typescript-automation[bot]** added label `For Milestone Bug`, removed label `For Backlog Bug`, and assigned to **RyanCavanaugh**
 * [today](https://github.com/microsoft/TypeScript/pull/64268#issuecomment-5755669697) **lukiod** adopted a fixture for the variable form, pointed out that Omit only applied to object literals and replaced it with timeZone?: never for stricter checking, updated temporal.ts to exercise the variable form, and reaccepted the four temporal baselines

### [Issue microsoft/TypeScript#64322](https://github.com/microsoft/TypeScript/issues/64322) (Closed, **jakebailey**, **Copilot**)

**\[Bug\] PrivateIdentifier nodes are omitted from 2020 semantic classifications**

*ECMAScript private fields and methods are omitted from TypeScript 2020 semantic classifications, preventing proper property and method highlighting.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/64322#issuecomment-5738467283) **VALLIS-NERIA** confirmed that the issue still existed in the latest main branch and noted that the semantic provider only works for identifiers but not private identifiers, linking to relevant code
 * (yesterday) **jakebailey** assigned to **Copilot**, **jakebailey**
 * (later) **jakebailey** closed the issue

### [PR microsoft/TypeScript#64329](https://github.com/microsoft/TypeScript/pull/64329) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Narrow HTMLElement autocapitalize to supported keywords**

*Narrow HTMLElement.autocapitalize property type to the six valid keywords and reject misspellings*

 * (2 days ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/64329#issuecomment-5738114447) **jakebailey** said "This is a generated file "
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64332](https://github.com/microsoft/TypeScript/pull/64332) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Update lib\.dom\.d\.ts: MutationObserverInit\.attributeFilter can accept an iterator**

*Extend MutationObserverInit.attributeFilter in lib.dom.d.ts to accept any Iterable<string> instead of only string arrays.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64333](https://github.com/microsoft/TypeScript/pull/64333) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Add camera control properties \(pan, tilt, zoom\) to DOM media track types**

*Adds camera control properties pan, tilt, zoom, torch, and whiteBalanceMode to DOM media track type definitions in lib.dom.d.ts.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64334](https://github.com/microsoft/TypeScript/pull/64334) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Restore navigator\.connection DOM typings**

*Restore navigator.connection DOM typings by re-adding NavigatorNetworkInformation, NetworkInformation, and ConnectionType declarations*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64335](https://github.com/microsoft/TypeScript/pull/64335) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Model required currency/unit options for Intl\.NumberFormat currency/unit styles**

*Enforce mandatory currency and unit fields for currency or unit styles in Intl.NumberFormatOptions definitions to match runtime behavior.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64336](https://github.com/microsoft/TypeScript/pull/64336) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Allow iterable File constructor fileBits**

*Allow any iterable of BlobPart for the File constructor in DOM and WebWorker libs and add corresponding tests*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64338](https://github.com/microsoft/TypeScript/pull/64338) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Narrow return type of Performance/PerformanceObserverEntryList\.getEntriesByType by entry type literal**

*Add literal-string overloads to getEntriesByType in lib.dom.d.ts and lib.webworker.d.ts so it returns specific PerformanceEntry subclass arrays for each entry type.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64339](https://github.com/microsoft/TypeScript/pull/64339) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Make WritableStreamDefaultWriter\.write contravariant in its chunk type**

*Update WritableStreamDefaultWriter.write signature to enforce contravariance in chunk types, preventing unsound writable stream assignments.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64340](https://github.com/microsoft/TypeScript/pull/64340) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Allow kebab\-case indexing on CSSStyleDeclaration**

*Allow accessing CSSStyleDeclaration properties using kebab-case keys by adding a string index signature*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64341](https://github.com/microsoft/TypeScript/pull/64341) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix MIDIMessageEvent\.data incorrectly typed as nullable**

*Update MIDIMessageEvent.data in TypeScript DOM declarations to be non-null Uint8Array, eliminating redundant null checks.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64342](https://github.com/microsoft/TypeScript/pull/64342) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Declare Document\.scrollingElement as HTMLElement \| null**

*Change Document.scrollingElement’s type to HTMLElement | null in lib.dom.d.ts with tests and baseline updates.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64343](https://github.com/microsoft/TypeScript/pull/64343) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Add IntegerTypedArray type and use it for crypto\.getRandomValues**

*Introduce an IntegerTypedArray type and update crypto.getRandomValues to accept only integer typed arrays.*

 * **Copilot** assigned to **RyanCavanaugh**
 * (2 days ago) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64344](https://github.com/microsoft/TypeScript/pull/64344) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Model Intl\.Collator\#compare as a readonly bound function property**

*Make Intl.Collator.compare a readonly bound function property in lib.es5.d.ts to align with the spec and prevent assignment and unbound-method issues.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64345](https://github.com/microsoft/TypeScript/pull/64345) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Fix HTMLElement error event typings**

*Adjust DOM typings to ensure HTMLElement error event handlers receive a UIEvent and preserve Window.onerror behavior.*

 * (2 days ago) **typescript-automation[bot]** added labels `For Milestone Bug`, `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64346](https://github.com/microsoft/TypeScript/pull/64346) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**, **Copilot**)

**Reject timeZone in ZonedDateTime\.toLocaleString options**

*Remove the timeZone option from Temporal.ZonedDateTime.toLocaleString and error on its usage because the method always uses the receiver’s time zone.*

 * (2 days ago) **typescript-automation[bot]** added label `For Uncommitted Bug`, and removed label `For Milestone Bug`
 * [yesterday](https://github.com/microsoft/TypeScript/pull/64346#issuecomment-5745662690) **Sector6759** suggested defining the interface with timeZone?: never to prevent accidentally passing the timeZone option in non-literal options objects
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#64349](https://github.com/microsoft/TypeScript/pull/64349) (Closed, `For Uncommitted Bug`, **jakebailey**, **Copilot**)

**Classify private identifiers in semantic tokens**

*Include PrivateIdentifier nodes in semantic token classification to highlight private fields and methods with appropriate token types and declaration modifiers.*

 * (yesterday) **Copilot** assigned to **Copilot**, **jakebailey**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * (later) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#64354](https://github.com/microsoft/TypeScript/issues/64354) (Closed)

**Burp Professional 2026**

*Propose implementing Burp Suite Professional 2026 support using the aanyapatels/Burpsuite-Professional repository.*

 * created by **aanyapatels**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/64354#issuecomment-5744806500) **MartinJohns** said "I will never understand how people think this is acceptable behavior."
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#64364](https://github.com/microsoft/TypeScript/issues/64364) (Closed)

**Suggestion: \`brand type\` for finite literal brands with companion \`\.is\` / \`\.from\`**

*Propose brand type syntax to define finite literal unions with nominal branding and autogenerated .is/.from runtime guards.*

 * created by **mishelashala**
 * [today](https://github.com/microsoft/TypeScript/issues/64364#issuecomment-5753207502) **MartinJohns** said "This is out of scope for TypeScript. The issue template for feature requests (that you didn't use) has a viability checklist, which this suggestion does not align with."
 * (today) **mishelashala** closed the issue

### [PR microsoft/TypeScript#64365](https://github.com/microsoft/TypeScript/pull/64365) (Closed, `For Uncommitted Bug`)

**fix\(vscode\-typescript\): activate for content\-mapped\-only workspaces**

*Permit VS Code TypeScript extension to activate for content-mapped-only workspaces by adding workspace activation events and syncing open files.*

 * created by **snhsish**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64365#issuecomment-5752493767) **snhsish** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64366](https://github.com/microsoft/TypeScript/pull/64366) (Open, `For Uncommitted Bug`)

**Watch project directories that are close to the filesystem root**

*tsc --watch doesn’t detect changes in projects near the filesystem root because it ignores directories with under five path components.*

 * created by **Generalsimus**
 * (today) **typescript-automation[bot]** added labels `For Uncommitted Bug`, `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5753121877) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5753293920) **Generalsimus** quoted the policy service directive for Microsoft
 * [later](https://github.com/microsoft/TypeScript/pull/64366#issuecomment-5759505773) **Generalsimus** said "@microsoft-github-policy-service agree"

### [PR microsoft/TypeScript#64367](https://github.com/microsoft/TypeScript/pull/64367) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 4 updates**

*Bump codecov/codecov-action to v7.1.1 and github/codeql-action init, analyze, and upload-sarif to v4.38.1 in the repository root*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64368](https://github.com/microsoft/TypeScript/issues/64368) (Open)

**Content mapper: allowing document highlight result from other language\-servers**

*Propose returning null instead of empty arrays for content-mapper document highlight results to enable fallback from other language servers.*

 * created by **jasonlyu123**
 * [later](https://github.com/microsoft/TypeScript/issues/64368#issuecomment-5759018848) **Abdellox** offered to help investigate and asked for steps to reproduce, expected vs actual behavior, and environment details

### [PR microsoft/TypeScript#64369](https://github.com/microsoft/TypeScript/pull/64369) (Open, `For Uncommitted Bug`)

**LEGO: Pull request from lego/hb\_5378966c\-b857\-470a\-8675\-daebef4a6da1\_20260921092356953 to main**

*Merge updated localized LCL strings from lego/hb_5378966c-b857-470a-8675-daebef4a6da1 branch into main.*

 * created by **csigs**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#64370](https://github.com/microsoft/TypeScript/issues/64370) (Open, `Won't Fix`)

**Native compiler \(tsgo\) aborts with "fatal error: stack overflow" on deeply nested expressions**

*tsgo compiler crashes with a fatal stack overflow when parsing extremely deeply nested parentheses, brackets, or type arguments due to unbounded parser recursion.*

 * created by **kajaaz**

### [PR microsoft/TypeScript#64371](https://github.com/microsoft/TypeScript/pull/64371) (Closed, `For Uncommitted Bug`)

**parser: bound recursion depth to avoid stack overflow on deeply nested input**

*Bound parser recursion with a 40000-depth limit and new TS1700 diagnostic to prevent stack overflows on deeply nested input.*

 * created by **kajaaz**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/64371#issuecomment-5762820056) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [later](https://github.com/microsoft/TypeScript/pull/64371#issuecomment-5763313376) **kajaaz** said "@microsoft-github-policy-service agree company="Ledger""

### [PR microsoft/TypeScript#64372](https://github.com/microsoft/TypeScript/pull/64372) (Open, `Author: Team`, `For Milestone Bug`, **ahejlsberg**)

**Restore idempotency to \`resolveObjectTypeMembers\`**

*Restore resolveObjectTypeMembers idempotency by preventing base type arguments from accessing partially resolved class or interface members*

 * created by **ahejlsberg**
 * (later) **typescript-automation[bot]** added labels `Author: Team`, `For Milestone Bug`, `For Milestone Bug`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5763106068) **ahejlsberg** said "@typescript-bot test it"
 * [later](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5763107668) **typescript-automation[bot]** reported CI build statuses for multiple commands and noted an access denied error for the 'run dt' pipeline
 * [later](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5763296299) **jakebailey** said "I fixed the DT error (forgot to grant a perm), but note that DT doesn't check 7.0 or 7.1 quite yet."
 * [later](https://github.com/microsoft/TypeScript/pull/64372#issuecomment-5763474607) **typescript-automation[bot]** provided the requested performance run results with a comparison report

