# Report for 2026-04-30 (Thursday, April 30th, 2026)

7 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @otech47 provided reproducibility details and context in [microsoft/TypeScript#61717](https://github.com/microsoft/TypeScript/issues/61717#issuecomment-4359135572)
    * @ritschwumm asked why each line was changed and whether line endings were switched in [microsoft/TypeScript#63453](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4359360882)
    * @carljohnsonnewhampshire-hue asked for advice on bypassing TypeScript's recursive type checking heuristics in [microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4355952195)
    * @carljohnsonnewhampshire-hue asked if there’s a way to write recursive record mapped types differently to enable proper type checking in [microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4357766912)

## Activity Summary

### [Issue microsoft/TypeScript#61717](https://github.com/microsoft/TypeScript/issues/61717) (Open, `Bug`, `Help Wanted`, `Domain: tsc -b`)

**\`tsc \-\-build \-\-watch\` produces stray \`\.js\`/\`\.js\.map\` files when adding a file to upstream project**

*tsc --build --watch in TS 5.6+ wrongly emits stray .js/.js.map files into upstream project src when switching branches.*

 * (49 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: tsc -b`, and set milestone to `Backlog`
 * [later](https://github.com/microsoft/TypeScript/issues/61717#issuecomment-4359135572) **otech47** shared detailed reproduction context for a bug emitting stray .d.ts files under tsc --watch in a Yarn workspaces monorepo, noting dependencies on large file checkouts and long watcher uptime

### [Issue microsoft/TypeScript#62660](https://github.com/microsoft/TypeScript/issues/62660) (Closed, `Needs More Info`)

**Repro of huge spike tsc memory usage from 5\.5\.4 \-\> 5\.6\.2**

*Compiling deeply nested generic wrap functions with TypeScript 5.6.2 doubles memory usage compared to 5.5.4*

 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/62660#issuecomment-3434501160) **AlexeiDarmin-SA** appreciated the bisect to the PR, noted that traversal in setTextRange could cause multiplicative work on large codebases, and asked about shortcutting it or adding an opt-in performance flag
 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/62660#issuecomment-3434511120) **RyanCavanaugh** suggested adding a type annotation to avoid printing enormous anonymous types and reduce memory usage; provided an example showing .d.ts size drop
 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/62660#issuecomment-3434562249) **AlexeiDarmin-SA** started annotating anonymous types in a large private repo and thanked RyanCavanaugh, stating they’d follow up in a few days
 * [today](https://github.com/microsoft/TypeScript/issues/62660#issuecomment-4355388632) **AlexeiDarmin-SA** analyzed declaration emit output, identified hotspots from long inferred type chains in reselect/redux selectors, added explicit type annotations and reduced deep createSelector composition, and resolved memory and emit performance issues enabling upgrade beyond 5.5.4 and migration to TS Go
 * (today) **AlexeiDarmin-SA** closed the issue

### [Issue microsoft/TypeScript#63451](https://github.com/microsoft/TypeScript/issues/63451) (Open, `Bug`, `Fix Available`, `Domain: classes`)

**\`new super\(\)\` in static method does not cause error**

*TypeScript 6.0 incorrectly allows new super() in static blocks and methods without error.*

 * created by **Withered-Flower-0422**
 * [today](https://github.com/microsoft/TypeScript/issues/63451#issuecomment-4354002466) **RyanCavanaugh** thanked the user, listed similar issues, and explained that 'new super()' is valid per the ECMAScript spec
 * [today](https://github.com/microsoft/TypeScript/issues/63451#issuecomment-4354227318) **Withered-Flower-0422** corrected that `new super()` is disallowed in JavaScript and throws errors
 * (today) **RyanCavanaugh** added label `Bug`, set milestones to `Backlog`, `Dormant`, and removed from milestone `Backlog`
 * **typescript-bot** added label `Fix Available`

### [Issue microsoft/TypeScript#63452](https://github.com/microsoft/TypeScript/issues/63452) (Open, `Needs Investigation`)

**TS IntelliSense is very slow or loads endlessly on simple ArkType wrapper**

*VSCode’s TypeScript IntelliSense hangs indefinitely and exhibits extremely slow error detection in a simple ArkType wrapper project*

 * created by **FunctionDJ**
 * **vs-code-engineering[bot]** assigned to **mjbvz**
 * [today](https://github.com/microsoft/TypeScript/issues/63452#issuecomment-4354002566) **RyanCavanaugh** provided an automatically generated list of similar issues with relevance percentages
 * [today](https://github.com/microsoft/TypeScript/issues/63452#issuecomment-4354134744) **RyanCavanaugh** noted that the video showed insertion at the log end, reported his own local responsiveness, suggested @ssalbdivad for clues, and concluded it likely didn't meet the 6.0 LS patch bar
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and unassigned **mjbvz**

### [PR microsoft/TypeScript#63453](https://github.com/microsoft/TypeScript/pull/63453) (Closed, `For Uncommitted Bug`)

**fix: detected calls to child\_process from a function\.\.\. in\.\.\.**

*Sanitized child_process usage in scripts/find-unused-diganostic-messages.mjs to prevent command injection*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4351194500) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4351194517) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4354624555) **jakebailey** noted that this was not a security problem, suggested the author hadn't tested locally, pointed out formatting issues, and asked if the author was a bot and how they determined the issue needed fixing
 * [later](https://github.com/microsoft/TypeScript/pull/63453#issuecomment-4359360882) **ritschwumm** asked why the change modified every line of the diagnostic script and whether the line endings were switched

### [Issue microsoft/TypeScript#63454](https://github.com/microsoft/TypeScript/issues/63454) (Closed, `Design Limitation`)

**\`1 \| 2 \| 3\` can be assigned to \`1 \| 2\` when using a recursive type**

*A recursive mapped type wrapper in TypeScript unsoundly allows assignment between unions 1|2|3 and 1|2.*

 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4353396688) **carljohnsonnewhampshire-hue** demonstrated that the BuildType example allowed num and str to be assigned to each other without type errors
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4353411975) **carljohnsonnewhampshire-hue** demonstrated that when object type nesting is one level shallower, both assignments fail as expected
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4354002694) **RyanCavanaugh** provided an automatically generated analysis with links to similar issues
 * **RyanCavanaugh** added label `Design Limitation`
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4354488447) **RyanCavanaugh** explained inability to know ahead of time that BuildType will terminate and requested a reliable heuristic to detect termination without false positives
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4355952195) **carljohnsonnewhampshire-hue** asked for suggestions on intentionally circumventing TypeScript's recursive type heuristics
 * [today](https://github.com/microsoft/TypeScript/issues/63454#issuecomment-4357766912) **carljohnsonnewhampshire-hue** asked if there was a way to write the recursive type definition differently to allow TypeScript to check assignments, perhaps via tail recursion

