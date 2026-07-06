# Report for 2026-07-03 (Friday, July 3rd, 2026)

4 different users commented on 5 different issues.

## Recommended Actions

 * Response Recommended
    * @typescript-automation[bot] reported a server panic for signatureHelp request in [microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803367)
    * @typescript-automation[bot] reported a panic during signatureHelp handling in [microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803391)
    * @typescript-automation[bot] reported a server connection closed prematurely error in [microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803417)
    * @typescript-automation[bot] reported a server connection closed prematurely error in [microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803446)
    * @typescript-automation[bot] reported server connection closed prematurely in [microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803466)
    * @typescript-automation[bot] reported a server connection error for nuxt/nuxt in [microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803487)
    * @typescript-automation[bot] provided error report and logs for CI failure in [microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803515)
    * @typescript-automation[bot] reported a panic during textDocument/rangeFormatting in [microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803554)

## Activity Summary

### [Issue microsoft/TypeScript-go#4528](https://github.com/microsoft/TypeScript-go/issues/4528) (Open, `Domain: Type Checking`, `Type Ordering`)

**tsgo appears to loop until OOM on three/tsl Fn callback that TypeScript accepts**

*tsgo enters an infinite type-checking loop and exhausts memory when processing a three/tsl Fn callback that tsc accepts*

 * created by **hsheth2**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4528#issuecomment-4878905010) **ahejlsberg** described that TS6 with `-stableTypeOrdering` also ran out of memory while computing variance information for the `Node<TNodeType>` type, identifying a type ordering issue
 * (today) **ahejlsberg** added labels `Domain: Type Checking`, `Type Ordering`
 * [today](https://github.com/microsoft/TypeScript-go/issues/4528#issuecomment-4879046574) **ahejlsberg** suggested refactoring Node<TNodeType> into a NodeExtras mapping with specific extensions per type

### [PR microsoft/TypeScript-go#4529](https://github.com/microsoft/TypeScript-go/pull/4529) (Open)

**Fix wildcard directories being dropped for "\./"\-prefixed includes with dot\-directory excludes**

*Wildcard directories defined by './'-prefixed include patterns are incorrectly dropped when dot-directory excludes are present, preventing new file detection.*

 * created by **jansedlon**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4529#issuecomment-4874013472) **jansedlon** said "@microsoft-github-policy-service agree"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4529#issuecomment-4877759536) **jakebailey** said "Can you point to the Strada code, if this is just a porting bug?"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4529#issuecomment-4880819285) **jansedlon** pointed to the normalizePath implementation and explained how simpleNormalizePath strips './' segments to prevent the bug

### [Issue microsoft/TypeScript-go#4532](https://github.com/microsoft/TypeScript-go/issues/4532) (Open)

**\[ServerErrors\]\[TypeScript\] main vs **

*The main branch's pipeline analyzing 300 popular TypeScript repositories detected 11 interesting changes and encountered errors, timeouts, and cloning failures.*

 * created by **typescript-automation[bot]**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803367) **typescript-automation[bot]** reported a panic while handling textDocument/signatureHelp due to invalid memory address or nil pointer dereference
 * [today](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803391) **typescript-automation[bot]** logged a panic error when handling a textDocument/signatureHelp request due to a failed assertion 'Not a subspan'
 * [today](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803417) **typescript-automation[bot]** reported a server connection closed prematurely error with undefined reason for slopus/happy and included raw error artifacts, request logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803446) **typescript-automation[bot]** reported a server connection closure error undefined during analysis of drizzle-team/drizzle-orm and provided error details, last requests, and reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803466) **typescript-automation[bot]** reported that the server connection closed prematurely with an undefined error during automated formatting
 * [today](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803487) **typescript-automation[bot]** reported that the server connection closed prematurely with undefined error and provided affected repo, logs, and repro steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803515) **typescript-automation[bot]** reported server connection closed prematurely with undefined error for mermaid-js/mermaid and provided log and replay command details
 * [today](https://github.com/microsoft/TypeScript-go/issues/4532#issuecomment-4879803554) **typescript-automation[bot]** reported a panic during textDocument/rangeFormatting due to a debug failure

### [PR microsoft/TypeScript-go#4533](https://github.com/microsoft/TypeScript-go/pull/4533) (Open)

**\[api\] Add \`\.getNonPrimitiveType\(\)\` getter**

*Introduce a .getNonPrimitiveType() getter in the API to access non-primitive types.*

 * created by **mrazauskas**

