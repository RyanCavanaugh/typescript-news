# Report for 2026-07-24 (Friday, July 24th, 2026)

4 different users commented on 6 different issues.

## Recommended Actions

 * Response Recommended
    * @brettz9 asked for feedback on removing jsdoc/require-yields rule and adding yields type enforcement in [microsoft/TypeScript#23857](https://github.com/microsoft/TypeScript/issues/23857#issuecomment-5073385863)
    * @LangLangBart provided benchmark results confirming the fix in [microsoft/TypeScript#63653](https://github.com/microsoft/TypeScript/issues/63653#issuecomment-5072023287)

## Activity Summary

### [Issue microsoft/TypeScript#23857](https://github.com/microsoft/TypeScript/issues/23857) (Open, `Suggestion`, `Awaiting More Feedback`, `Domain: JSDoc`)

**JSDoc support for @yields**

*Add JSDoc @yields tag support for TypeScript and ESLint valid-jsdoc rule to document generator yields*

 * **weswigham** added label `Awaiting More Feedback`
 * [3.6 years ago](https://github.com/microsoft/TypeScript/issues/23857#issuecomment-1327679723) **clshortfuse** noted that the original eslint rule is deprecated and explained how to use @yield and @return in JSDoc, shared a code example, mentioned disabling jsdoc/valid-types, linked a VSCode tooltip bug, and suggested using Generator<T> instead of Iterator<T>.
 * [2.8 years ago](https://github.com/microsoft/TypeScript/issues/23857#issuecomment-1731217475) **AnrDaemon** confirmed that using Generator<T> instead of Iterator<T> worked and provided a code example
 * [today](https://github.com/microsoft/TypeScript/issues/23857#issuecomment-5073385863) **brettz9** suggested removing the jsdoc/require-yields rule from the TypeScript config and adding a yields type enforcement rule, and asked for feedback on issue #1733

### [Issue microsoft/TypeScript#62974](https://github.com/microsoft/TypeScript/issues/62974) (Closed, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: TypeError: Cannot read properties of undefined \(reading 'flags'\) in isFreshLiteralType during recursive tuple expansion with unresolved identifiers**

*TypeScript compiler crashes with a TypeError reading 'flags' in isFreshLiteralType during recursive tuple expansion with unresolved identifiers*

 * (27 weeks ago) **RyanCavanaugh** added labels `Help Wanted`, `Domain: Crashes`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/62974#issuecomment-5075606305) **ahejlsberg** said "Fixed by https://github.com/microsoft/typescript-go/pull/4735."
 * (today) **ahejlsberg** closed the issue

### [Issue microsoft/TypeScript#63653](https://github.com/microsoft/TypeScript/issues/63653) (Closed, `Bug`, **ahejlsberg**)

**Template literal union type\-checking is exponentially slower when type is explicitly annotated vs inferred**

*TypeScript’s type-checker experiences exponential slowdown when checking large template literal union types on explicitly annotated variables compared to inferred ones.*

 * (2 days ago) **ahejlsberg** added label `Bug`, and removed label `Needs Investigation`
 * (yesterday) **ahejlsberg** closed the issue
 * [today](https://github.com/microsoft/TypeScript/issues/63653#issuecomment-5072023287) **LangLangBart** tested the nightly build and confirmed a 15× performance improvement and that the issue was fixed

### [PR microsoft/TypeScript#63670](https://github.com/microsoft/TypeScript/pull/63670) (Closed, `For Milestone Bug`)

**fix: Incorrect type resolution with nested constructors**

*Fix TypeScript's class extension logic to use constructor signatures instead of instance types for nested constructors.*

 * **typescript-automation[bot]** added label `For Milestone Bug`
 * [2 days ago](https://github.com/microsoft/TypeScript/pull/63670#issuecomment-5050210572) **thiagobarbosa** said "@microsoft-github-policy-service agree"
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63670#issuecomment-5057699534) **MartinJohns** pointed out a missed important note in the contributing guidelines
 * (today) **thiagobarbosa** closed the issue

### [Issue microsoft/TypeScript#63679](https://github.com/microsoft/TypeScript/issues/63679) (Open, `Bug`, `Help Wanted`)

**Should not allow \`import\.defer?\.\('x'\)\`**

*Prevent optional chaining calls on import.defer so import.defer?.('x') is correctly rejected.*

 * created by **fisker**

