# Report for 2026-06-20 (Saturday, June 20th, 2026)

7 different users commented on 8 different issues.

## Recommended Actions

 * Response Recommended
    * @maoger provided test results and requested review in [microsoft/TypeScript-go#4382](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4758968472)
    * @njfamirm noted that the issue occurred in ESLint in [microsoft/TypeScript-go#4387](https://github.com/microsoft/TypeScript-go/issues/4387#issuecomment-4761900002)

## Activity Summary

### [PR microsoft/TypeScript-go#4226](https://github.com/microsoft/TypeScript-go/pull/4226) (Closed, `No linked issue`)

**Convert \`valueSymbolLinks\` and \`symbolNodeLinks\` to id\-paged arrays**

*Replace valueSymbolLinks and symbolNodeLinks map stores with ID-paged arrays to reduce hash lookup costs and improve typechecking performance*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4695712559) **typescript-automation[bot]** posted automated CI build initiation status
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4695836495) **typescript-automation[bot]** said "@jakebailey, the perf run you requested failed. You can check the log here."
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4695919710) **typescript-automation[bot]** provided the perf run results for the requested comparison
 * [later](https://github.com/microsoft/TypeScript-go/pull/4226#issuecomment-4761758294) **mds-ant** said "Closing this PR in favor of https://github.com/microsoft/typescript-go/pull/4329."
 * (later) **mds-ant** closed the issue

### [PR microsoft/TypeScript-go#4234](https://github.com/microsoft/TypeScript-go/pull/4234) (Closed, `No linked issue`)

**Skip mark/rewind in \`tryParseTypeArgumentsInExpression\` when token isn't \`\<\`**

*Optimize tryParseTypeArgumentsInExpression by skipping parser mark/rewind overhead when the token isn't '<', improving performance.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4652925956) **jakebailey** said "@typescript-bot perf test this faster"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4652926633) **typescript-automation[bot]** noted CI jobs started and linked to results
 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4653159218) **typescript-automation[bot]** provided the requested performance run results
 * [later](https://github.com/microsoft/TypeScript-go/pull/4234#issuecomment-4761761427) **mds-ant** said "@jakebailey @DanielRosenwasser Are there any changes you'd like me to make here? If not, are we good to merge this PR?"

### [PR microsoft/TypeScript-go#4382](https://github.com/microsoft/TypeScript-go/pull/4382) (Open)

**fix\(relater\): add property comparison cache fast path to avoid false TS2321**

*Add a relation-cache fast path in property-type comparisons to avoid false TS2321 errors for large object literals*

 * created by **maoger**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4757235439) **maoger** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4758527237) **jakebailey** stated that they were not going to be raising any limits
 * [today](https://github.com/microsoft/TypeScript-go/pull/4382#issuecomment-4758968472) **maoger** removed the stack depth limit change, relied on a relation-cache fast path to avoid redundant stack pushes, confirmed tests passed and baseline unaffected, and marked the PR ready for review

### [PR microsoft/TypeScript-go#4384](https://github.com/microsoft/TypeScript-go/pull/4384) (Closed)

**Fix panic on non\-string include/exclude/files in extended configs**

*Prevent tsgo from panicking when extended config include, exclude, or files fields contain non-string values.*

 * created by **oMatheusmol**

### [Issue microsoft/TypeScript-go#4385](https://github.com/microsoft/TypeScript-go/issues/4385) (Closed, `Crash`)

**ja**

*The issue titled “ja” contains no stack trace details or reproduction steps.*

 * created by **Bt4vtfjsj4-pitido**
 * **Bt4vtfjsj4-pitido** added label `Crash`
 * (today) **ahejlsberg** closed the issue

### [PR microsoft/TypeScript-go#4386](https://github.com/microsoft/TypeScript-go/pull/4386) (Closed)

**Fix RemoteNodeList crash on Array species methods \(map/filter/slice\)**

*Array species methods crash on RemoteNodeList due to missing Symbol.species override causing incorrect constructor invocation.*

 * created by **hl662**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4386#issuecomment-4761254520) **JoostK** said "https://github.com/microsoft/typescript-go/pull/4346"
 * (later) **hl662** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/pull/4386#issuecomment-4762104356) **hl662** thanked and acknowledged jumping the gun

### [Issue microsoft/TypeScript-go#4387](https://github.com/microsoft/TypeScript-go/issues/4387) (Closed)

**Javascript memory heap**

*Running the Go-based tsgo type checker via npm scripts results in a Node "JavaScript heap out of memory" error.*

 * created by **njfamirm**
 * (later) **njfamirm** closed the issue
 * [later](https://github.com/microsoft/TypeScript-go/issues/4387#issuecomment-4761900002) **njfamirm** said "excuse me! this occurred in eslint"

