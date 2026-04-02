# Report for 2025-12-31 (Wednesday, December 31st, 2025)

1 different users commented on 2 different issues.

## Recommended Actions

 * Response Recommended
    * @jogibear9988 reported that the error still occurs and provided performance metrics in [microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3703426438)

## Activity Summary

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Open, `Crash`)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3671189110) **jakebailey** said "I do not think any of the new hangs are related to this issue, please look at other issues or file your own"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3671370893) **jakebailey** said "#2411 for the 18.1 hang"
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3673779704) **jogibear9988** asked how to track down which files cause the issue and whether they could share via a private repo; noted that reverting to yesterday’s version did not resolve it
 * [later](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3703426438) **jogibear9988** reported that the newest version still errored, observed that disabling sourcemaps reduced ts-go build time to 13s versus 32s for normal TypeScript, and noted a ~5s startup delay before the build message

