# Report for 2026-04-23 (Thursday, April 23rd, 2026)

15 different users commented on 14 different issues.

## Recommended Actions

 * Response Recommended
    * @brandonbothell asked if TypeScript plans to ever add PnP support in [microsoft/TypeScript#35206](https://github.com/microsoft/TypeScript/pull/35206#issuecomment-4309892721)
    * @lith-x provided a minimal reproduction snippet clarifying the issue in [microsoft/TypeScript#42384](https://github.com/microsoft/TypeScript/issues/42384#issuecomment-4309351634)
    * @Zain-ul-din reported that the loading got stuck forever even in a simple file in [microsoft/TypeScript#46726](https://github.com/microsoft/TypeScript/issues/46726#issuecomment-4312259830)
    * @PoseidonEnergy asked where to submit a feature PR given conflicting contribution guidelines in [microsoft/TypeScript#63426](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4309658685)
    * @PoseidonEnergy asked how to get feedback on their PR from the TypeScript team in [microsoft/TypeScript#63426](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4313308617)
    * @snakefood3232 offered to submit a PR to extend the Math interface in [microsoft/TypeScript#63427](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4306189949)
    * @snakefood3232 offered to submit a PR in two days in [microsoft/TypeScript#63427](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4306545660)
    * @827652549 asked whether to add the issue to the Backlog milestone and requested guidance on PR conventions in [microsoft/TypeScript#63427](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4310859954)

## Activity Summary

### [Issue microsoft/TypeScript#28289](https://github.com/microsoft/TypeScript/issues/28289) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add new moduleResolution option: \`yarn\-pnp\`**

*Add a new "yarn-pnp" moduleResolution option to the TypeScript compiler to support Yarn Plug’n’Play.*

 * [4.4 years ago](https://github.com/microsoft/TypeScript/issues/28289#issuecomment-966424931) **pauldraper** asked arcanis to merge pull request #8 to support scoped typings packages
 * [4.3 years ago](https://github.com/microsoft/TypeScript/issues/28289#issuecomment-989955577) **Luiz-Monad** countered with the example of F# type providers and argued that dynamic type emission could be integrated to improve compiler flexibility
 * [33 weeks ago](https://github.com/microsoft/TypeScript/issues/28289#issuecomment-3245018405) **p99will** provided a workaround using `yarn dlx @yarnpkg/sdks vscode` to integrate Yarn PnP with VSCode/TypeScript and enable node type declarations in tsconfig.json
 * [today](https://github.com/microsoft/TypeScript/issues/28289#issuecomment-4309791717) **brandonbothell** said "I guess typescript-go might support pnp eventually."

### [PR microsoft/TypeScript#35206](https://github.com/microsoft/TypeScript/pull/35206) (Closed, `Experiment`, `lib update`, `For Uncommitted Bug`)

**Native support for PnP**

*Add proof-of-concept native support for Yarn Plug’n’Play module resolution in TypeScript.*

 * [21 weeks ago](https://github.com/microsoft/TypeScript/pull/35206#issuecomment-3570057954) **arcanis** provided an update that a new PR implemented the full PnP specification in TypeScript-Go with technical blockers addressed, tests included, validation on Datadog completed, contributors thanked, and urged TS team collaboration
 * (1 month ago) **typescript-bot** closed the issue
 * [1 month ago](https://github.com/microsoft/TypeScript/pull/35206#issuecomment-4121422967) **typescript-bot** announced closure of all PRs that didn't meet post-6.0 criteria and directed contributors to file issues or submit to the appropriate repos for bugfixes, language service improvements, type system changes, or library updates
 * [today](https://github.com/microsoft/TypeScript/pull/35206#issuecomment-4309892721) **brandonbothell** said "So, does typescript not plan on ever adding pnp support?"

### [Issue microsoft/TypeScript#42384](https://github.com/microsoft/TypeScript/issues/42384) (Open, `Suggestion`, `In Discussion`)

**Type guard should infer the type of parent object when applied on a property**

*Allow narrowing of a union object's type when a property type guard succeeds.*

 * [1.6 years ago](https://github.com/microsoft/TypeScript/issues/42384#issuecomment-2327709232) **AlbertMarashi** provided a TypeScript type guard example to reduce type assertions
 * [1.4 years ago](https://github.com/microsoft/TypeScript/issues/42384#issuecomment-2477274707) **Rudxain** provided another repro link using Array#every as a workaround and noted its inefficiency and the need for re-assignment inside the branch for control flow analysis to narrow the destructuring pattern
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/42384#issuecomment-2561282538) **eliasm307** mentioned encountering a similar issue with TypeScript non-nullable object properties and provided a code example and Play link
 * [today](https://github.com/microsoft/TypeScript/issues/42384#issuecomment-4309351634) **lith-x** provided a code snippet illustrating expected and unexpected type narrowing behavior with nullable fields

### [Issue microsoft/TypeScript#46726](https://github.com/microsoft/TypeScript/issues/46726) (Closed, `Needs Investigation`, `Domain: Performance`, `7.0 LS Migration`)

**Slow IntelliSense with react\-hook\-form resolvers on commands \`completionInfo\`, \`completionEntryDetails\`, and, \`encodedSemanticClassifications\-full\`**

*Integrating react-hook-form Zod resolvers causes slow IntelliSense for completionInfo, completionEntryDetails, and encodedSemanticClassifications-full commands.*

 * (4.4 years ago) **andrewbranch** added labels `Needs Investigation`, `Domain: Performance`, and removed label `Needs More Info`
 * [later](https://github.com/microsoft/TypeScript/issues/46726#issuecomment-4312259830) **Zain-ul-din** reported that the loading got stuck forever even in a simple file and attached a screenshot
 * (later) **andrewbranch** added labels `Strada (TS 6.0-) Language Service`, `7.0 LS Migration`, and removed label `Strada (TS 6.0-) Language Service`
 * [later](https://github.com/microsoft/TypeScript/issues/46726#issuecomment-4314328340) **andrewbranch** said "Closing language service bugs related to the 6.0 implementation. For more information, see https://github.com/microsoft/TypeScript/issues/62827"
 * (later) **andrewbranch** closed the issue

### [Issue microsoft/TypeScript#63416](https://github.com/microsoft/TypeScript/issues/63416) (Closed, `Duplicate`)

**JSDoc parser treats \`@foo\` inside fenced code blocks as a tag, breaking hover previews**

*JSDoc parser does not respect fenced code blocks and incorrectly treats @tags inside them as JSDoc tags, breaking hover documentation previews.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63416#issuecomment-4276891516) **MartinJohns** said "Duplicate of #58992."
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63416#issuecomment-4282661729) **RyanCavanaugh** generated an automated analysis listing similar issues
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63416#issuecomment-4309798395) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63419](https://github.com/microsoft/TypeScript/issues/63419) (Closed, `Won't Fix`)

**Transformer that updates an ambient property declaration is emitted as non\-ambient**

*TypeScript transformers updating ambient property declarations in TS 4.3 lose the ambient flag and emit the property.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63419#issuecomment-4290418828) **RyanCavanaugh** provided an automated analysis listing similar issues and suggesting to close if duplicate
 * **RyanCavanaugh** added label `Won't Fix`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63419#issuecomment-4290565099) **RyanCavanaugh** said "This doesn't meet the 6.0 patch bar, and 7.0+ doesn't have a corresponding implementation for this code."
 * [today](https://github.com/microsoft/TypeScript/issues/63419#issuecomment-4309798697) **typescript-bot** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63421](https://github.com/microsoft/TypeScript/issues/63421) (Open, `Not a Defect`)

**"Using type predicates" documentation promotes lying to the type system**

*The TypeScript documentation's type predicate example encourages misuse of 'as' assertions, undermining type safety.*

 * **RyanCavanaugh** added label `Not a Defect`
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4298029720) **RyanCavanaugh** argued that there’s usually no perfect way to write a type predicate function because built-in narrowing suffices and noted that using ‘in’ loses type safety on the key
 * [today](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4303181436) **ilyash-b** asked whether to comment on this in the handbook or close the issue, noting that 'in' is not a clear winner over 'as'
 * [later](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4312902534) **jendrikw** said "Type guard are always circumventing the type system. I don't use them at all and just test for the properties that I actually need."

### [Issue microsoft/TypeScript#63426](https://github.com/microsoft/TypeScript/issues/63426) (Open, `Duplicate`)

**Incorrect TS18047 Error \-\-\> "variable is possibly null"**

*TypeScript incorrectly flags the selection variable as possibly null even after an explicit null check in v6.0.3.*

 * [today](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4305049124) **MartinJohns** said "Another duplicate of #9998."
 * [today](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4305685799) **nmain** said "There are also hundreds of posts in #9998 and duplicates explaining why it's not easy to fix and why it hasn't been fixed yet."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4309658685) **PoseidonEnergy** asked where to submit a feature PR given conflicting contributing guidelines between microsoft/TypeScript and microsoft/typescript-go
 * [later](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4312855925) **mkantor** explained that feature addition PRs were on hold until the 7.0 release and noted the 7.0 beta was recently released
 * [later](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4313308617) **PoseidonEnergy** asked how to get feedback on their PR from the TypeScript team given their issue was marked duplicate
 * [later](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4313573692) **MartinJohns** said "Just FYI, the new compiler is written in Go. The TypeScript code base won't be continued anymore."

### [Issue microsoft/TypeScript#63427](https://github.com/microsoft/TypeScript/issues/63427) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Add type definition for Math\.sumPrecise \(ES2025 / TC39 proposal\)**

*Add missing TypeScript declaration for the ES2026 Math.sumPrecise method to prevent compile errors.*

 * (today) **RyanCavanaugh** added labels `Bug`, `Help Wanted`, `Domain: lib.d.ts`
 * [today](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4306189949) **snakefood3232** suggested extending the Math interface in a new lib.es2025.d.ts file and offered to submit a PR within two days
 * [today](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4306545660) **snakefood3232** offered to create type augmentations for Math.sumPrecise and submit a PR in two days
 * [today](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4306994771) **RyanCavanaugh** said "@snakefood3232 actually what I need is a risotto recipe added to README.md, can you put up a PR right away?"
 * [today](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4310859954) **827652549** offered to fix the issue, corrected the ES version and placement in the issue description, opened PR #63429 with necessary changes, and asked about adding a Backlog milestone and for guidance on PR conventions

### [Issue microsoft/TypeScript#63428](https://github.com/microsoft/TypeScript/issues/63428) (Closed)

**Non\-literal enum initializer has surprising behavior**

*A computed non-literal enum initializer causes the enum to accept arbitrary numbers instead of only its defined values.*

 * created by **walkerburgin**
 * [today](https://github.com/microsoft/TypeScript/issues/63428#issuecomment-4308582992) **MartinJohns** explained that Number.POSITIVE_INFINITY is typed as number causing the union to be unbounded and that casting a literal to number has the same issue
 * (today) **walkerburgin** closed the issue

### [PR microsoft/TypeScript#63429](https://github.com/microsoft/TypeScript/pull/63429) (Open, `For Uncommitted Bug`)

**lib: add Math\.sumPrecise type definition \(ES2025\)**

*Add type definition for the Stage 4 TC39 Math.sumPrecise method to TypeScript’s esnext standard library definitions.*

 * created by **827652549**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63429#issuecomment-4310683342) **827652549** said "@microsoft-github-policy-service agree"

### [Issue microsoft/TypeScript#63430](https://github.com/microsoft/TypeScript/issues/63430) (Open)

**Paths from tsconfig are not used if declaration is on a different partition**

*TypeScript ignores tsconfig path aliases in declaration files when source and mapped files reside on different drive partitions.*

 * created by **dragomirtitian**

### [PR microsoft/TypeScript#63431](https://github.com/microsoft/TypeScript/pull/63431) (Closed, `For Uncommitted Bug`)

**Update README\.md**

*Update the project's README.md to include the important modifications highlighted by @ahejlsberg.*

 * created by **slimmii**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63431#issuecomment-4312729642) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (later) **jakebailey** closed the issue

