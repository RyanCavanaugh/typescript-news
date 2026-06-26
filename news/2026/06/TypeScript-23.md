# Report for 2026-06-23 (Tuesday, June 23rd, 2026)

9 different users commented on 51 different issues.

## Recommended Actions

 * Response Recommended
    * @0xThiebaut reported that the problem occurs on WebStorm and linked to an existing issue in [microsoft/TypeScript#54087](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-4789272856)
    * @IIIMADDINIII asked about allowing decorators to influence return type inference in [microsoft/TypeScript#54652](https://github.com/microsoft/TypeScript/issues/54652#issuecomment-4789974934)

## Activity Summary

### [Issue microsoft/TypeScript#54087](https://github.com/microsoft/TypeScript/issues/54087) (Open, `Needs Investigation`, **sheetalkamat**)

**TypeScript file watcher holds onto folders and causes EPERM**

*TypeScript file watcher in VSCode intermittently locks folders on Windows, causing EPERM errors when renaming files until restart.*

 * [1.1 years ago](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-2812087903) **ahr-cw-de** said "Are there any updates as this is a really annoying problem?!"
 * [37 weeks ago](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-3377200662) **Gwynerva** listed four workarounds for the Windows issue, noting that some disable IntelliSense or autoimports and suggesting renaming folders externally or using Linux
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-4676219466) **muhammad-paksi** asked whether the issue would be resolved and provided a workaround snippet
 * [later](https://github.com/microsoft/TypeScript/issues/54087#issuecomment-4789272856) **0xThiebaut** mentioned that the problem also occurred on WebStorm and was traced to the linked issue

### [Issue microsoft/TypeScript#54652](https://github.com/microsoft/TypeScript/issues/54652) (Open, `Needs Investigation`, **rbuckton**)

**Decorated function parameter types are not inferred**

*Decorated class method parameters lose type inference under decorator syntax unlike direct decorator invocation*

 * (3 years ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **rbuckton**
 * [2 years ago](https://github.com/microsoft/TypeScript/issues/54652#issuecomment-2155755211) **fyc09** said "Is there any progress? @rbuckton "
 * [later](https://github.com/microsoft/TypeScript/issues/54652#issuecomment-4789974934) **IIIMADDINIII** expressed interest in return type inference, referenced a TypeScript Playground example, and suggested allowing decorators to influence type inference

### [Issue microsoft/TypeScript#63427](https://github.com/microsoft/TypeScript/issues/63427) (Open, `Bug`, `Help Wanted`, `Domain: lib.d.ts`)

**Add type definition for Math\.sumPrecise \(ES2025 / TC39 proposal\)**

*Add missing TypeScript declaration for the ES2026 Math.sumPrecise method to prevent compile errors.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4306994771) **RyanCavanaugh** said "@snakefood3232 actually what I need is a risotto recipe added to README.md, can you put up a PR right away?"
 * [8 weeks ago](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4310859954) **827652549** offered to fix the issue, corrected the ES version and placement in the issue description, opened PR #63429 with necessary changes, and asked about adding a Backlog milestone and for guidance on PR conventions
 * **RyanCavanaugh** added to milestone `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63427#issuecomment-4781901022) **RyanCavanaugh** said "Anyone planning to open the sixth PR to implement this should say why they're doing so, otherwise I'm going to assume they're an undisclosed bot and ban them."

### [PR microsoft/TypeScript#63483](https://github.com/microsoft/TypeScript/pull/63483) (Closed, `For Backlog Bug`)

**docs: add JSDoc comments to ReadonlySet interface**

*Add JSDoc comments to the ReadonlySet interface to improve its documentation.*

 * created by **niledas**
 * **typescript-bot** added label `For Backlog Bug`
 * [5 weeks ago](https://github.com/microsoft/TypeScript/pull/63483#issuecomment-4485867222) **niledas** said "Hi @RyanCavanaugh, please help review this small PR. Let me know if you have any suggestions."
 * (today) **RyanCavanaugh** closed the issue
 * (today) **RyanCavanaugh** reopened the issue

### [Issue microsoft/TypeScript#63546](https://github.com/microsoft/TypeScript/issues/63546) (Open, `Bug`, `Domain: Declaration Emit`)

**Duplicate function declarations in generated \`\.d\.ts\` for non\-module JS files with \`allowJs\` \+ \`declaration\`**

*Non-module JavaScript files compiled with allowJs and declaration produce duplicate global function declarations across their emitted .d.ts files.*

 * **RyanCavanaugh** added label `Fixed`
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63546#issuecomment-4686993381) **LangLangBart** asked whether tsgo should exit with a non-zero status after observing that the latest 7.0.0-dev.20260604.1 version silently aborts declaration emit and exits with code 0, unlike earlier versions that reported 'Duplicate function implementation' errors and exited with code 1
 * **RyanCavanaugh** removed label `Fixed`
 * **RyanCavanaugh** added label `Bug`
 * [later](https://github.com/microsoft/TypeScript/issues/63546#issuecomment-4791015251) **RyanCavanaugh** said "Tagging bug for the exit code thing"
 * **RyanCavanaugh** added to milestone `Backlog`

### [Issue microsoft/TypeScript#63553](https://github.com/microsoft/TypeScript/issues/63553) (Closed)

**different behaviour between function and arrow function while define never return type**

*TypeScript infers named functions that throw errors as void but equivalent arrow functions as never, and the author requests clarification.*

 * created by **CaptainJon**
 * [today](https://github.com/microsoft/TypeScript/issues/63553#issuecomment-4781539738) **RyanCavanaugh** explained that class methods that only throw infer void while function expressions infer never and function declarations must choose between the two inferences
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63554](https://github.com/microsoft/TypeScript/pull/63554) (Closed, `For Backlog Bug`)

**lib: add Math\.sumPrecise type definition \(ES2026 / esnext\)**

*Register and reference a new esnext.math library to include the Stage 4 ES2026 Math.sumPrecise type definition.*

 * created by **VanshBD**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63554#issuecomment-4707513903) **VanshBD** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript/pull/63554#issuecomment-4781905746) **RyanCavanaugh** asked what differences existed from the existing PR and requested responses in Latin
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63555](https://github.com/microsoft/TypeScript/issues/63555) (Open, `Domain: Performance`, `Possible Improvement`)

**Quadratic check time for diamond\-shaped interface inheritance graphs**

*TypeScript exhibits quadratic check time when traversing base types in diamond-shaped interface inheritance graphs.*

 * created by **canonic-epicure**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63555#issuecomment-4710611453) **MartinJohns** said "@m-mahdi-abbaszade You should read this and stop with your pointless spam: https://github.com/microsoft/TypeScript/blob/main/CONTRIBUTING.md#automated-comments"
 * [today](https://github.com/microsoft/TypeScript/issues/63555#issuecomment-4781486642) **RyanCavanaugh** assessed that the fix didn’t meet the 6.0 patch bar and suggested evaluating a PR in the Go repo while noting it would slightly slow the common case and isn’t recommended
 * (today) **RyanCavanaugh** added labels `Domain: Performance`, `Possible Improvement`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63555#issuecomment-4781962281) **canonic-epicure** said "Its a valid program after all => should compile."
 * [today](https://github.com/microsoft/TypeScript/issues/63555#issuecomment-4785188567) **RyanCavanaugh** said "A Turing-complete system that can produce correct outputs in finite and bounded time is going to be extremely useful 😉"
 * [today](https://github.com/microsoft/TypeScript/issues/63555#issuecomment-4785835932) **canonic-epicure** said "I agree, definitely, its very important to apply a proper fix."

### [Issue microsoft/TypeScript#63556](https://github.com/microsoft/TypeScript/issues/63556) (Open, `Domain: lib.d.ts`, `Possible Improvement`)

**Overload missing from createElementNS**

*createElementNS lacks an overload for the XHTML namespace, causing it to return generic HTMLElement instead of specific HTML element types*

 * created by **mozesstumpf**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63556#issuecomment-4713780576) **jcalz** said "Pls edit to say "overload" and not "override" (those are different things)"
 * (today) **RyanCavanaugh** added labels `Domain: lib.d.ts`, `Possible Improvement`, and set milestone to `Backlog`

### [Issue microsoft/TypeScript#63559](https://github.com/microsoft/TypeScript/issues/63559) (Open, `Bug`, `Fix Available`, `Domain: classes`)

**Incorrect type resolution with nested constructors**

*TypeScript incorrectly reports the outer constructor’s type for nested constructor extensions, causing B.kind to be 'A' instead of 'B'.*

 * created by **Mudloop**
 * (today) **RyanCavanaugh** added label `Bug`, and set milestone to `Dormant`
 * **typescript-automation[bot]** added label `Fix Available`
 * **RyanCavanaugh** added label `Domain: classes`

### [Issue microsoft/TypeScript#63560](https://github.com/microsoft/TypeScript/issues/63560) (Open, `Domain: Performance`, `Possible Improvement`)

**Quadratic duplicate declaration accumulation in intersection constructor properties can crash with RangeError**

*Quadratic accumulation of duplicate declarations in intersection constructor types causes RangeError crashes under diamond inheritance*

 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63560#issuecomment-4715904418) **canonic-epicure** said "That would be a huge context switch, staying with TS version for now."
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63560#issuecomment-4716141044) **MartinJohns** said "Kinda pointless then, since that version is not continued. 🤷‍♂️ "
 * [today](https://github.com/microsoft/TypeScript/issues/63560#issuecomment-4777370635) **canonic-epicure** said "I guess I can submit a reproduction-only issue to tsgo version, w/o a fix."
 * [today](https://github.com/microsoft/TypeScript/issues/63560#issuecomment-4781492702) **RyanCavanaugh** said "Same answer as in #63555"
 * (today) **RyanCavanaugh** added labels `Domain: Performance`, `Possible Improvement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63562](https://github.com/microsoft/TypeScript/pull/63562) (Closed, `For Backlog Bug`)

**Show nested JSDoc descriptions for destructured params in signature help**

*Signature help now includes nested JSDoc @param descriptions for destructured parameters by retrieving each property's documentation from the parent object type.*

 * created by **DukeDeSouth**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63562#issuecomment-4720146518) **DukeDeSouth** described fixes to property name literal checks, rest binding skipping, and added fourslash tests for quoted and numeric properties
 * [today](https://github.com/microsoft/TypeScript/pull/63562#issuecomment-4781290063) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the PR to the typescript-go repo referencing CONTRIBUTING.md and issue #62963
 * (today) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63563](https://github.com/microsoft/TypeScript/pull/63563) (Closed, `For Backlog Bug`)

**Narrow destructured discriminated unions when the discriminant has a default**

*Providing a default value for a discriminant in a destructured union prevents sibling bindings from narrowing.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/63563#issuecomment-4725904471) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (1 week ago) **typescript-automation[bot]** added label `For Backlog Bug`, and removed label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63563#issuecomment-4781311586) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the PR to the typescript-go repo referencing CONTRIBUTING.md and issue #62963
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63565](https://github.com/microsoft/TypeScript/issues/63565) (Open, `Bug`, `Domain: check: Control Flow`)

**\`export\` modifier on \`enum\` disables \`This condition will always return \* ts2845\`**

*Adding the export modifier to an enum prevents TypeScript from reporting a ts2845 error on an always-true condition.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4751644133) **mkantor** explained that enums can be declaration-merged and that external modules might define the same enum, causing pessimistic analysis
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4751672793) **mkantor** clarified that they misread the condition and that the second part only checks the truthiness of AdapterOutputType.PAGES
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4768133967) **eps1lon** said "The program would know all the values after declaration merging. How would more values in AdapterOutputType change AdapterOutputType.PAGES === 1?"
 * **RyanCavanaugh** added label `Bug`
 * [today](https://github.com/microsoft/TypeScript/issues/63565#issuecomment-4781453442) **RyanCavanaugh** said "Repros in 7.0 as well."
 * (today) **RyanCavanaugh** added label `Domain: check: Control Flow`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63567](https://github.com/microsoft/TypeScript/pull/63567) (Closed, `For Backlog Bug`)

**fix\(checker\): avoid stack overflow for self\-referential computed enum member names**

*Fix stack overflow crashes by treating self-referential computed enum member names as non-bindable during name resolution.*

 * created by **yen0304**
 * **typescript-automation[bot]** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63567#issuecomment-4781304230) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the contributor to the typescript-go repo, referring to CONTRIBUTING.md and pinned issue #62963; requested future responses in Latin
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63568](https://github.com/microsoft/TypeScript/issues/63568) (Open, `Needs Investigation`, **ahejlsberg**)

**Regression: 7\.0\.1\-RC Unable to Satisfy Recursive Mapped Type Constraint**

*TypeScript 7.0.1-RC fails to satisfy recursive mapped type constraints that worked in earlier releases.*

 * created by **sinclairzx81**
 * [today](https://github.com/microsoft/TypeScript/issues/63568#issuecomment-4781844137) **RyanCavanaugh** provided an isolated TypeScript snippet demonstrating ZodType, OptionalInternals, ZodObject, Properties, FromObject, and FromSchema definitions
 * [today](https://github.com/microsoft/TypeScript/issues/63568#issuecomment-4783629409) **RyanCavanaugh** presented a simplified TypeScript type example illustrating Wrapped, FromObject, and FromSchema types
 * (later) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**

### [Issue microsoft/TypeScript#63569](https://github.com/microsoft/TypeScript/issues/63569) (Closed, `Suggestion`, `Out of Scope`)

**Switch Expression**

*Add C#-style switch expression syntax to TypeScript for concise inline value mappings*

 * created by **Lenmint**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63569#issuecomment-4757274226) **MartinJohns** pointed out that the proposal was out of scope for TypeScript and the viability checklist item was checked mistakenly
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Out of Scope`
 * [today](https://github.com/microsoft/TypeScript/issues/63569#issuecomment-4781436373) **RyanCavanaugh** said "☝️"
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63573](https://github.com/microsoft/TypeScript/issues/63573) (Open, `Suggestion`, `Experience Enhancement`)

**Hover documentation for parameters documented with jsdoc renders improperly**

*VSCode hover feature misrenders JSDoc @param descriptions when using hyphens or wrapped lines.*

 * created by **SirzBenjie**
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Experience Enhancement`, and set milestone to `Backlog`

### [PR microsoft/TypeScript#63577](https://github.com/microsoft/TypeScript/pull/63577) (Closed, `For Uncommitted Bug`)

**chore: fix 'seperately'/'seperator' spelling in src/compiler/utilities\.ts**

*Correct typos in comments within src/compiler/utilities.ts by replacing 'seperately' with 'separately' and 'seperator' with 'separator'.*

 * created by **Dodothereal**
 * [today](https://github.com/microsoft/TypeScript/pull/63577#issuecomment-4781572896) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63577#issuecomment-4781572898) **typescript-automation[bot]** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * **typescript-automation[bot]** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63577#issuecomment-4781717544) **RyanCavanaugh** informed that the TypeScript repo was closed for development and directed the PR to the typescript-go repo referencing CONTRIBUTING.md and issue #62963
 * (today) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63578](https://github.com/microsoft/TypeScript/issues/63578) (Open, `Not a Defect`)

**Unexpectedly narrow implicit generator type**

*TypeScript’s implicit type inference for generator functions produces an unexpectedly narrow union type across multiple versions.*

 * created by **badeball**
 * [later](https://github.com/microsoft/TypeScript/issues/63578#issuecomment-4791228589) **RyanCavanaugh** provided a minimal TypeScript example demonstrating that FeatureChild is assignable to RuleChild, causing FeatureChild | RuleChild to simplify to RuleChild and affecting the inferred yield type
 * **RyanCavanaugh** added label `Not a Defect`

### [Issue microsoft/TypeScript#63579](https://github.com/microsoft/TypeScript/issues/63579) (Open, `Needs Investigation`, **johnfav03**)

**tsc \-\-build false negative through export star facade project**

*Incremental tsc --build with composite projects using export * facades fails to detect downstream type changes, resulting in stale declarations.*

 * created by **jasonkuhrt**

### [Issue microsoft/TypeScript#63580](https://github.com/microsoft/TypeScript/issues/63580) (Closed, `Bug`, `Domain: Parser`)

**Parser hangs on comment ending with \`\-\*/\`**

*TypeScript's createSourceFile function hangs indefinitely when parsing a comment that begins with /** and ends with -*/.*

 * created by **core-dumpling**
 * [later](https://github.com/microsoft/TypeScript/issues/63580#issuecomment-4790844410) **RyanCavanaugh** said "Doesn't repro in tsgo but a total LS hang is quite bad; we might want to take this for a 6.0 patch"
 * **RyanCavanaugh** added label `Bug`

### [PR microsoft/TypeScript#63581](https://github.com/microsoft/TypeScript/pull/63581) (Closed, `For Uncommitted Bug`)

**Fix infinite loop**

*Correct loop termination logic to fix an infinite loop in the application.*

 * created by **core-dumpling**
 * **typescript-automation[bot]** added label `For Uncommitted Bug`

