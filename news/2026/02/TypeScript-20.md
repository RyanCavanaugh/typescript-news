# Report for 2026-02-20 (Friday, February 20th, 2026)

8 different users commented on 10 different issues.

## Activity Summary

### [PR microsoft/TypeScript#63163](https://github.com/microsoft/TypeScript/pull/63163) (Open, `For Uncommitted Bug`, **DanielRosenwasser**, **Copilot**)

**Port anyFunctionType subtype fix and JSX children NonInferrableType propagation from typescript\-go**

*Port fixes from typescript-go to make anyFunctionType a proper function subtype and correctly propagate NonInferrableType for JSX children.*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930882621) **typescript-bot** informed that the DT test run failed and linked to the log
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930957509) **typescript-bot** provided the requested performance run results
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3930984285) **typescript-bot** provided benchmark results for the top 400 repos and reported that everything looked good
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3936094451) **jakebailey** said "DT is still broken due to the wordpress package 404, but the PR itself seems correct?"
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3936352629) **ahejlsberg** said "PR looks good to me, but was waiting to see DT results."
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3936667089) **jakebailey** fixed DT and requested the typescript-bot to run dt
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3936667361) **typescript-bot** reported dt jobs start and completion status with result links
 * [today](https://github.com/microsoft/TypeScript/pull/63163#issuecomment-3936759174) **typescript-bot** notified that DT test results were ready and unchanged

### [PR microsoft/TypeScript#63172](https://github.com/microsoft/TypeScript/pull/63172) (Open, `Author: Team`, `For Uncommitted Bug`, **jakebailey**)

**Deprecate assert in import\(\)**

*Deprecate use of assert within dynamic import() calls due to its runtime interpretation, which was overlooked in #63077.*

 * created by **jakebailey**
 * (today) **typescript-bot** added labels `Author: Team`, `For Uncommitted Bug`, `For Uncommitted Bug`, and assigned to **jakebailey**
 * [today](https://github.com/microsoft/TypeScript/pull/63172#issuecomment-3937632278) **DanielRosenwasser** said "We don't have a test with { assert: { type: json } }???"
 * [today](https://github.com/microsoft/TypeScript/pull/63172#issuecomment-3937830272) **DanielRosenwasser** said "I assume we have tests for runtime import() calls as well."

### [Issue microsoft/TypeScript#63173](https://github.com/microsoft/TypeScript/issues/63173) (Open, `Bug`, `Help Wanted`, `Domain: Crashes`)

**Crash: Maximum call stack size exceeded when declare const enum has a computed property named \[object\] followed by an object member**

*The compiler overflows the call stack when a const enum has a computed [object] member followed by an object member.*

 * created by **na7ure-a**
 * [later](https://github.com/microsoft/TypeScript/issues/63173#issuecomment-3938428643) **knowltonn287-source** posted a code snippet illustrating a const enum with conflicting member names

### [PR microsoft/TypeScript#63174](https://github.com/microsoft/TypeScript/pull/63174) (Open, `For Uncommitted Bug`)

**Fix \#37782: add quick fix for private methods**

*Add a TypeScript quick fix that automatically generates private methods in classes to improve productivity.*

 * created by **loganionian**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63174#issuecomment-3938166271) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."

### [PR microsoft/TypeScript#63175](https://github.com/microsoft/TypeScript/pull/63175) (Closed, `For Uncommitted Bug`)

**Fix \#29707: Adjust ClassConstructor type for better type safety**

*Change ClassConstructor type in mixin function from any[] to unknown[] for increased type safety and clarity.*

 * created by **loganionian**
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63175#issuecomment-3938183819) **typescript-bot** said "This PR doesn't have any linked issues. Please open an issue that references this PR. From there we can discuss and prioritise."
 * [today](https://github.com/microsoft/TypeScript/pull/63175#issuecomment-3938385453) **jakebailey** said "This is just the example code from the issue copied into an unreferenced file"
 * (today) **jakebailey** closed the issue

### [PR microsoft/TypeScript#63176](https://github.com/microsoft/TypeScript/pull/63176) (Closed, `For Backlog Bug`)

**fix\(checker\): mark getter/setter as deprecated when any declaration has @deprecated**

*Restore marking of getter/setter pairs as deprecated when either accessor includes a @deprecated tag.*

 * created by **TheAbMehta**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63176#issuecomment-3938363379) **TheAbMehta** said "@microsoft-github-policy-service agree"

