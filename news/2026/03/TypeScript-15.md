# Report for 2026-03-15 (Sunday, March 15th, 2026)

7 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @microsoft-github-policy-service asked the user to agree to the Contributor License Agreement in [microsoft/TypeScript#63254](https://github.com/microsoft/TypeScript/pull/63254#issuecomment-4066279281)

## Activity Summary

### [Issue microsoft/TypeScript#35886](https://github.com/microsoft/TypeScript/issues/35886) (Closed, `Bug`, `Help Wanted`, `Domain: JS Emit`)

**import is cut after "transpileModule" compilation when object spread is used \(TypeScript 3\.7\)**

*TypeScript 3.7's transpileModule incorrectly removes imports from the output when object spread syntax is used.*

 * (4.1 years ago) **RyanCavanaugh** added label `Domain: JS Emit`, set milestone to `Backlog`, and removed from milestone `TypeScript 4.6.1`
 * [later](https://github.com/microsoft/TypeScript/issues/35886#issuecomment-4067934272) **sorochanalex** said "Was fixed in 4.3 with https://github.com/microsoft/TypeScript/pull/42904"
 * (later) **sorochanalex** closed the issue

### [Issue microsoft/TypeScript#42564](https://github.com/microsoft/TypeScript/issues/42564) (Closed, `Suggestion`, `In Discussion`)

**Constrained usage of type guard functions in conditions**

*TypeScript fails to narrow types when a type guard function is compared to false instead of using !.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/42564#issuecomment-4057975445) **kkmuffme** said "Isn't this a duplicate of https://github.com/microsoft/TypeScript/issues/44366 (which has been fixed in the meantime)"
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/42564#issuecomment-4058340405) **RyanCavanaugh** said "Indeed!"
 * (2 days ago) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/42564#issuecomment-4066965505) **paigefletcher1282-code** confirmed that it was

### [Issue microsoft/TypeScript#60561](https://github.com/microsoft/TypeScript/issues/60561) (Closed, `Working as Intended`)

**Module resolution: NodeNext breaks typechecking**

*Using nodenext moduleResolution and --transform-types in TypeScript breaks type checking despite correct module resolution.*

 * (2 days ago) **andrewbranch** added label `Working as Intended`, and removed label `Needs Investigation`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/60561#issuecomment-4056735977) **andrewbranch** explained that the ioredis typings bug arose from the double assignment in index.js and a mismatched TypeScript declaration, causing the analysis tool to misinterpret the default export and suggest incorrect import usage
 * [today](https://github.com/microsoft/TypeScript/issues/60561#issuecomment-4064517198) **typescript-bot** said "This issue has been marked as "Working as Intended" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#61325](https://github.com/microsoft/TypeScript/issues/61325) (Open, `Suggestion`, `Awaiting More Feedback`)

**Support for Import Maps**

*Add an importMap compilerOptions option to support WICG import maps for alias resolution and scopes across Node and Deno.*

 * created by **harrysolovay**
 * (1 year ago) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`
 * [later](https://github.com/microsoft/TypeScript/issues/61325#issuecomment-4066296558) **patroza** explained that two different mappings were needed when running a project from source versus compiled and suggested adding a TypeScript source entry if TypeScript adopted package.json

### [Issue microsoft/TypeScript#62200](https://github.com/microsoft/TypeScript/issues/62200) (Closed, `Suggestion`, `Breaking Change`, `Committed`, `Fix Available`, **andrewbranch**)

**Deprecate, remove \`\-\-moduleResolution node10\`**

*Remove the outdated --moduleResolution node/node10 flag in TypeScript 7.0, advising nodenext for Node.js and esnext with bundler for web.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4054811294) **monsanto** reported encountering TS2351 errors with default class exports in NodeNext, hypothesized a TypeScript bug, offered to share a repro, and requested a fix before removing moduleResolution: node
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4056497943) **RyanCavanaugh** said "@monsanto a repro would be extremely helpful, thanks"
 * [yesterday](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4060436192) **monsanto** provided a link to a related TypeScript issue as a repro
 * [later](https://github.com/microsoft/TypeScript/issues/62200#issuecomment-4066958003) **paigefletcher1282-code** urged to create a repro because it would be helpful

### [Issue microsoft/TypeScript#63195](https://github.com/microsoft/TypeScript/issues/63195) (Open, `Needs More Info`)

**Debug Failure: "No error for last overload signature" crash when CustomTypeOptions\.resources uses typeof on a large \(~10k line\) JSON file**

*TypeScript crashes with 'No error for last overload signature' when using typeof on a large JSON for i18next CustomTypeOptions.resources.*

 * (2 days ago) **RyanCavanaugh** added label `Needs More Info`, and removed label `Needs More Info`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4058537717) **RyanCavanaugh** said "Still can't repro this. Can you set up a cloneable repo?"
 * [later](https://github.com/microsoft/TypeScript/issues/63195#issuecomment-4066964354) **paigefletcher1282-code** confirmed experiencing the issue and asked for it to be fixed

### [Issue microsoft/TypeScript#63243](https://github.com/microsoft/TypeScript/issues/63243) (Closed, `Duplicate`)

**PromiseRejectedResut reason should be \`unknown\`**

*Require the PromiseRejectedResult.reason type in the es2020 promise library to be unknown instead of any*

 * created by **karlismelderis-mckinsey**
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63243#issuecomment-4045154423) **MartinJohns** said "Essentials a duplicate of #45602."
 * **RyanCavanaugh** added label `Duplicate`
 * [today](https://github.com/microsoft/TypeScript/issues/63243#issuecomment-4064517064) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63254](https://github.com/microsoft/TypeScript/pull/63254) (Open)

**fix\(compiler\): small improvement to error message handling**

*Fix minor misspellings in internal compiler checker comments to improve readability without changing behavior.*

 * created by **Vikash9546**
 * [later](https://github.com/microsoft/TypeScript/pull/63254#issuecomment-4066279281) **microsoft-github-policy-service[bot]** prompted the user to agree to the Contributor License Agreement by replying with the specified command
 * [later](https://github.com/microsoft/TypeScript/pull/63254#issuecomment-4067370704) **MartinJohns** quoted the pull request template advising against submitting typo-only PRs

### [PR microsoft/TypeScript#63255](https://github.com/microsoft/TypeScript/pull/63255) (Open)

**fix\(compiler\): small improvement to error message handling**

*Update two comments in parser.ts to correct grammar in parseErrorForMissingSemicolonAfter documentation*

 * created by **Vikash9546**
 * [later](https://github.com/microsoft/TypeScript/pull/63255#issuecomment-4067366563) **MartinJohns** quoted the pull request template advising against submitting typo-only PRs

