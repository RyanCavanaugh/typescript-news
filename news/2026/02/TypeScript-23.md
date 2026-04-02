# Report for 2026-02-23 (Monday, February 23rd, 2026)

11 different users commented on 9 different issues.

## Recommended Actions

 * Response Recommended
    * @Bertie690 asked if the feature was still desired and if they could submit a PR in [microsoft/TypeScript#10886](https://github.com/microsoft/TypeScript/issues/10886#issuecomment-3949053605)
    * @kylefiegener-gardiant reported missing strikethrough styling for deprecated TSX props in [microsoft/TypeScript#60442](https://github.com/microsoft/TypeScript/issues/60442#issuecomment-3948350643)
    * @ackvf reported that TypeScript ignores unused variables prefixed with underscore despite tsconfig settings in [microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3947083281)
    * @ackvf provided additional information about IDE and eslint detection of unused variables in [microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3947153366)
    * @Arlen22 asked how to measure project size in [microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3946105193)

## Activity Summary

### [Issue microsoft/TypeScript#10886](https://github.com/microsoft/TypeScript/issues/10886) (Open, `Suggestion`, `Help Wanted`, `Domain: lib.d.ts`)

**Array inheritance in ES6 declaration file \(lib\.es6\.d\.ts\)**

*Update lib.es6.d.ts to support ES6 Array subclass methods returning the subclass type via this and static of/from.*

 * **mhegazy** added label `Domain: lib.d.ts`
 * (6.9 years ago) **RyanCavanaugh** set milestone to `Backlog`, and removed from milestone `Community`
 * [today](https://github.com/microsoft/TypeScript/issues/10886#issuecomment-3949053605) **Bertie690** asked if the feature was still desired and if they could submit a PR to implement the Array instance methods

### [Issue microsoft/TypeScript#60442](https://github.com/microsoft/TypeScript/issues/60442) (Open, `Suggestion`, `Experience Enhancement`)

**Show deprecation warnings on implementations of a deprecated property**

*Show deprecation warnings on object literal assignments and implementations of a deprecated interface property, not just property access.*

 * (1.2 years ago) **RyanCavanaugh** added label `Experience Enhancement`, and set milestone to `Backlog`
 * [1 year ago](https://github.com/microsoft/TypeScript/issues/60442#issuecomment-2589979946) **mathpaquette** said "@rbuckton  @DanielRosenwasser @andrewbranch could we please assign someone to review this improvement? thank you."
 * [today](https://github.com/microsoft/TypeScript/issues/60442#issuecomment-3948350643) **kylefiegener-gardiant** said "Also not seeing any strikethrough when using a deprecated component prop in a TSX file."

### [PR microsoft/TypeScript#62628](https://github.com/microsoft/TypeScript/pull/62628) (Closed, `For Uncommitted Bug`, **RyanCavanaugh**)

**Add lib\.esnext\.temporal**

*Adds ESNext Temporal library definitions to TypeScript with spec-compliant property constraints but without custom calendar support.*

 * [1 week ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3900131745) **jakebailey** said "Is someone putting together a set of improvements on these types, e.g. the ones discussed above? We can change these before the RC, so having people test things in nightly would be very helpful."
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3904267874) **fabon-f** mentioned making a commit with suggested changes and asked whether they should submit an issue before the PR
 * [1 week ago](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3904278277) **jakebailey** said "Feel free to just send it, just mention #60164 to make the bot not yell at you"
 * [later](https://github.com/microsoft/TypeScript/pull/62628#issuecomment-3952328155) **Renegade334** said "Have opened #63190 for a small interoperability improvement."

### [PR microsoft/TypeScript#63103](https://github.com/microsoft/TypeScript/pull/63103) (Closed, `For Uncommitted Bug`)

**just another test please dont fire me**

*User performs a security test and provides a HackerOne profile link.*

 * **typescript-bot** added label `For Uncommitted Bug`
 * [2 weeks ago](https://github.com/microsoft/TypeScript/pull/63103#issuecomment-3850476365) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * (2 weeks ago) **Jhounx** closed the issue
 * [today](https://github.com/microsoft/TypeScript/pull/63103#issuecomment-3946738372) **MartinJohns** said "Spammer."

### [Issue microsoft/TypeScript#63143](https://github.com/microsoft/TypeScript/issues/63143) (Open, `Suggestion`, `Awaiting More Feedback`)

**Add switch to disable \_var unused variable prevention**

*Add a tsconfig option to disable automatic ignoring of underscore-prefixed unused variables so the compiler still reports them to IDE.*

 * created by **ackvf**
 * [1 week ago](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3905192485) **guillaumebrunerie** suggested using an underscore suffix rather than a prefix to avoid variable shadowing, noted TypeScript's standalone usage invalidates IDE-only error filtering, and recommended configuring ESLint’s no-unused-variables rule
 * [today](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3945877868) **RyanCavanaugh** asked for clarification about the situation requiring writing an unused `_column` parameter
 * [today](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3947083281) **ackvf** clarified that TypeScript ignores variables prefixed with underscore regardless of tsconfig settings and requested opt-in configuration to report all unused variables
 * [today](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3947153366) **ackvf** noted that IDE and eslint only flagged ev as unused and provided screenshots showing that `_column` and `_ev` were also unused
 * (today) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [today](https://github.com/microsoft/TypeScript/issues/63143#issuecomment-3947344632) **guillaumebrunerie** suggested two possible solutions by renaming the variable or enabling the @typescript-eslint/no-unused-vars rule and provided a playground link and screenshot

### [Issue microsoft/TypeScript#63151](https://github.com/microsoft/TypeScript/issues/63151) (Open, `Bug`, `Help Wanted`, `Domain: LS: TSServer`)

**Intellisense keeps crashing**

*Intellisense in a remote SSH VS Code workspace stalls indefinitely with a perpetual loading spinner, disabling completions and navigation.*

 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922806396) **Arlen22** said "Reloading the window after closing all offending files seems to be fairly consistent. "
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922816633) **Arlen22** said "Adding the offending file (prisma.config.ts) to my project tsconfg.json file also seems to be fixing it. "
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3922834193) **Arlen22** provided additional log entries that might be relevant
 * [today](https://github.com/microsoft/TypeScript/issues/63151#issuecomment-3946105193) **Arlen22** noted that the issue occurred with any external file, provided environment details, and asked how to measure project size

### [PR microsoft/TypeScript#63188](https://github.com/microsoft/TypeScript/pull/63188) (Closed, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Eliminate interpolation from workflows**

*Remove interpolation from workflows to prevent analyzers from misinterpreting them as potential security risks.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript#63189](https://github.com/microsoft/TypeScript/issues/63189) (Open)

**Incorrect reference \`this\` in static context with \`experimentalDecorators\` enabled**

*With experimentalDecorators enabled TypeScript incorrectly emits static `this` references as undefined rather than the class.*

 * created by **yavanosta**

### [PR microsoft/TypeScript#63190](https://github.com/microsoft/TypeScript/pull/63190) (Closed, `For Uncommitted Bug`)

**discrete pluralizer for lib\.esnext\.temporal unit unions**

*Restrict DateUnit and TimeUnit unions to singular names and use a pluralizer helper for js-temporal compatibility.*

 * created by **Renegade334**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [later](https://github.com/microsoft/TypeScript/pull/63190#issuecomment-3952317584) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

