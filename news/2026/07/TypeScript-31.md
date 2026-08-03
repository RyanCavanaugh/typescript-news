# Report for 2026-07-31 (Friday, July 31st, 2026)

9 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @dasa asked if 2027 was a typo in [microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5146188990)

## Activity Summary

### [Issue microsoft/TypeScript#46135](https://github.com/microsoft/TypeScript/issues/46135) (Open, `Suggestion`, `Awaiting More Feedback`, **gabritto**)

**Ambient Module Declarations for Import Attributes \(formerly known as Import Assertions\)**

*Enable ambient module declarations based on import attributes to provide type definitions for CSS modules and asset URL imports.*

 * [30 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3692946297) **otomad** suggested supporting the inline grab module type and provided a TypeScript code example
 * [28 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3745345018) **justinfagnani** noted that major browsers, Node, Deno, Bun, Rollup, and Webpack support CSS and JSON modules with import attributes, and asked if that provides enough platform support for TypeScript support
 * [27 weeks ago](https://github.com/microsoft/TypeScript/issues/46135#issuecomment-3784607037) **jonathantneal** created a pull request for the issue
 * **gabritto** assigned to **gabritto**

### [Issue microsoft/TypeScript#54256](https://github.com/microsoft/TypeScript/issues/54256) (Closed, `Suggestion`, `Domain: Performance`, `Experimentation Needed`, `Rescheduled`, **rbuckton**, **jakebailey**)

**Experiment with Parallelized Parsing**

*Investigate parallelizing TypeScript file parsing across worker processes to reduce load times and evaluate overhead and usability tradeoffs.*

 * [1.5 years ago](https://github.com/microsoft/TypeScript/issues/54256#issuecomment-2608859169) **mistic** said "Is there any news on this effort? Is it still planned? Performance on big projects would definitely benefit from this (specially type checking on CI)"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/54256#issuecomment-5137807510) **ahejlsberg** said "Fixed in TS7!"
 * (yesterday) **ahejlsberg** closed the issue
 * (today) **DanielRosenwasser** set milestone to `TypeScript 7.0`, and removed from milestone `TypeScript 5.7.0`

### [Issue microsoft/TypeScript#63085](https://github.com/microsoft/TypeScript/issues/63085) (Closed, `Planning`)

**TypeScript 6\.0 Iteration Plan**

*The TypeScript 6.0 iteration plan details milestone dates and scheduled compiler additions, language improvements, breaking changes, and deprecations.*

 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4256022474) **typescript-bot** provided a CI jobs progress update with command, status, and results links
 * [15 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4256102755) **typescript-bot** said "Hey, @DanielRosenwasser! I've set the version of release-6.0 to 6.0.3 for you."
 * [6 weeks ago](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-4726011060) **Huaian666** said "about the typescript part — switched to this recently and the performance difference is night and day compared to what i was using"
 * [today](https://github.com/microsoft/TypeScript/issues/63085#issuecomment-5146150455) **DanielRosenwasser** said "The TypeScript 7.1 iteration plan has been posted over at https://github.com/microsoft/TypeScript/issues/63703!"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63646](https://github.com/microsoft/TypeScript/issues/63646) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-\-watch does not work in docker**

*tsc --watch fails to detect file changes in Docker bind-mounted workspaces on macOS after upgrading to version 7.0.2.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4996371305) **Alex-Bond** reported that the issue occurred on a native system where circular symlinks in node_modules overwhelmed the watcher, causing it to start listening but never receive updates
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-4999890598) **jakebailey** advised the user to file a separate issue for the MacOS problem and clarified that TS7 has no toggle to revert to NodeJS behavior
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5137934722) **danyreyna** reported a similar issue when building with Docker using node:22.22.3-slim, where subsequent tsc --watch builds stalled due to a fanotify_mark operation not supported error
 * [today](https://github.com/microsoft/TypeScript/issues/63646#issuecomment-5145530428) **johnfav03** thanked maintainers and explained that Docker's filesystem returns EOPNOTSUPP and that the watch will fall back from fanotify to inotify once the PR is merged

### [Issue microsoft/TypeScript#63699](https://github.com/microsoft/TypeScript/issues/63699) (Closed)

**Declaration emit drops expando properties when the synthesized namespace also contains \`export { … }\`**

*TypeScript 7.0+'s declaration emit drops inline function expando properties in .d.ts when the namespace includes explicit exports.*

 * created by **lassan**
 * [today](https://github.com/microsoft/TypeScript/issues/63699#issuecomment-5145865952) **lassan** said "Withdrawing this — filed prematurely on my side before we'd decided to report it upstream. Closing to keep it out of your triage queue. Apologies for the noise."
 * (today) **lassan** closed the issue

### [Issue microsoft/TypeScript#63700](https://github.com/microsoft/TypeScript/issues/63700) (Open, `Suggestion`, `Committed`, `Domain: lib.d.ts`, `Fix Available`)

**Support recent \`Iterator\`/\`Iterator\.prototype\` methods in \`esnext\` \(eventually \`es2027\`\)**

*Add TC39 stage 3 and stage 4 Iterator methods zip, zipKeyed, chunks, join, and includes to TypeScript 7.1 esnext.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Domain: lib.d.ts`, `Suggestion`, `Committed`, and set milestone to `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`

### [Issue microsoft/TypeScript#63701](https://github.com/microsoft/TypeScript/issues/63701) (Open, `Suggestion`, `Committed`, `Domain: lib.d.ts`)

**Support \`Promise\.allKeyed\`/\`Promise\.allSettledKeyed\` methods in \`esnext\` \(eventually \`es2027\`\)**

*Add support for Promise.allKeyed and Promise.allSettledKeyed in TypeScript 7.1’s esnext library to implement the stage 3 await dictionary proposal.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Suggestion`, `Committed`, `lib update`, and set milestone to `TypeScript 7.1`
 * **typescript-automation[bot]** added label `Fix Available`
 * (today) **DanielRosenwasser** added label `Domain: lib.d.ts`, and removed labels `Fix Available`, `lib update`

### [Issue microsoft/TypeScript#63702](https://github.com/microsoft/TypeScript/issues/63702) (Open, `Bug`, `Domain: lib.d.ts`)

**\`lib\.d\.ts\` Updates for TypeScript 7\.1**

*Update lib.d.ts for TypeScript 7.1 by integrating TSJS-lib-generator improvements and pending pull requests.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Bug`, `Domain: lib.d.ts`

### [Issue microsoft/TypeScript#63703](https://github.com/microsoft/TypeScript/issues/63703) (Open, `Planning`)

**TypeScript 7\.1 Iteration Plan**

*The TypeScript 7.1 iteration plan defines milestones and the planned language, editor, performance, and infrastructure improvements.*

 * created by **DanielRosenwasser**
 * **DanielRosenwasser** added label `Planning`
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5146188990) **dasa** said "2027, is that a typo?"
 * [today](https://github.com/microsoft/TypeScript/issues/63703#issuecomment-5146248499) **DanielRosenwasser** said "Sure is! 🫠🤦‍♂️"

### [Issue microsoft/TypeScript#63704](https://github.com/microsoft/TypeScript/issues/63704) (Open, `Suggestion`, `Committed`, `Domain: lib.d.ts`, `ES Next`)

**Add \`es2026\` as valid \`target\` and \`lib\`**

*Add ES2026 as a valid TypeScript target and library, incorporating new ECMAScript 2026 features and moving specified APIs to the es2026 lib.*

 * created by **DanielRosenwasser**
 * (today) **DanielRosenwasser** added labels `Suggestion`, `Committed`, `Domain: lib.d.ts`, `ES Next`

### [Issue microsoft/TypeScript#63705](https://github.com/microsoft/TypeScript/issues/63705) (Open, `Needs Investigation`, **weswigham**)

**TypeScript 7 declaration emit reuses an unrelated JSDoc import and generates an invalid type reference**

*TypeScript 7's declaration emit incorrectly reuses a private JSDoc import alias, producing invalid type references in declarations.*

 * created by **platypii**
 * (today) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **weswigham**

### [PR microsoft/TypeScript#63706](https://github.com/microsoft/TypeScript/pull/63706) (Closed, `For Uncommitted Bug`)

**ci: name version\-bump workflow steps for readability**

*Add descriptive names to the long version-bump and LKG steps in new-release-branch.yaml and set-version.yaml to improve readability in the GitHub Actions UI*

 * created by **MGPOCKY**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63706#issuecomment-5149980689) **MGPOCKY** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63706#issuecomment-5149981104) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63706#issuecomment-5149997554) **jakebailey** said "we do not need this"
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63707](https://github.com/microsoft/TypeScript/issues/63707) (Open)

**TypeScript Best Practices for Maintainable Production Code**

*Comprehensive TypeScript best practices for maintainable production code covering strict typing, code organization, error handling, performance, testing, and security.*

 * created by **nhokphal**

