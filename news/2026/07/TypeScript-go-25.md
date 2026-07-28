# Report for 2026-07-25 (Saturday, July 25th, 2026)

10 different users commented on 10 different issues.

## Recommended Actions

 * Moderation
    * @rb1974805-web threatened violence in [microsoft/TypeScript-go#2628](https://github.com/microsoft/TypeScript-go/pull/2628#issuecomment-5082409336)
 * Response Recommended
    * @helenkwok provided repro steps and nightly test harness for BOM-handling inconsistency in [microsoft/TypeScript-go#4521](https://github.com/microsoft/TypeScript-go/issues/4521#issuecomment-5081827093)
    * @typescript-automation[bot] provided perf run results as requested in [microsoft/TypeScript-go#4744](https://github.com/microsoft/TypeScript-go/pull/4744#issuecomment-5081278216)

## Activity Summary

### [PR microsoft/TypeScript-go#2628](https://github.com/microsoft/TypeScript-go/pull/2628) (Closed)

**Fix dedupe/redirect nondeterminism**

*Ensure deterministic deduplication and redirection ordering by updating comparison logic and removing misleading stable sorts.*

 * created by **jakebailey**
 * (24 weeks ago) **jakebailey** closed the issue
 * [today](https://github.com/microsoft/TypeScript-go/pull/2628#issuecomment-5082409336) **rb1974805-web** said "I will distory you that's it"

### [Issue microsoft/TypeScript-go#4521](https://github.com/microsoft/TypeScript-go/issues/4521) (Open, `Domain: API and Extensibility`, **andrewbranch**)

**SourceFile text does not include BOM**

*SourceFile.getText and getFullText omit the UTF-8 BOM while node start and end positions include it, causing misaligned text slices.*

 * **DanielRosenwasser** added label `Domain: API and Extensibility`
 * (2 weeks ago) **RyanCavanaugh** set milestone to `Post-7.0`, and assigned to **andrewbranch**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4521#issuecomment-5081827093) **helenkwok** reproduced a BOM-handling inconsistency in the native preview's SourceFile APIs and provided a nightly test harness

### [Issue microsoft/TypeScript-go#4740](https://github.com/microsoft/TypeScript-go/issues/4740) (Closed, `Domain: Type Checking`, `Type Ordering`)

**Divergence from tsc: assignment accepted by 5\.9/6\.0 is rejected by \`tsgo\` \(recursive DeepPartial \+ contravariant \`this\` \+ UnionToIntersection cycle, reduced from chart\.js\)**

*tsgo rejects an assignment involving a recursive DeepPartial type with contravariant this and a union-to-intersection cycle that is accepted by tsc 5.9/6.0*

 * created by **johanrd**
 * [later](https://github.com/microsoft/TypeScript-go/issues/4740#issuecomment-5083895252) **ahejlsberg** said "This is a type ordering issue. The same diagnostic is reported with by TypeScript 6.0 when compiling with --stableTypeOrdering."
 * (later) **ahejlsberg** added labels `Domain: Type Checking`, `Type Ordering`
 * [later](https://github.com/microsoft/TypeScript-go/issues/4740#issuecomment-5084036360) **johanrd** confirmed that TypeScript 6.0.3 with --stableTypeOrdering still reports the TS2322 error, closed the issue, and suggested keeping a single instantiation per pipeline
 * (later) **johanrd** closed the issue

### [Issue microsoft/TypeScript-go#4742](https://github.com/microsoft/TypeScript-go/issues/4742) (Closed)

**Stack overflow while contextually typing yield in a computed property name**

*Native TypeScript compiler stack overflows when contextually typing a yield expression in a computed property name.*

 * created by **HuzaifaAbdulRehman**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4742#issuecomment-5080621843) **HuzaifaAbdulRehman** said "Closing as a duplicate of #4743; the two reports were filed concurrently. Continuing discussion in #4743."
 * (today) **HuzaifaAbdulRehman** closed the issue

### [Issue microsoft/TypeScript-go#4743](https://github.com/microsoft/TypeScript-go/issues/4743) (Closed, **DanielRosenwasser**)

**Panic: Stack overflow during contextual typing of yield in a computed property name**

*Native TypeScript compiler stack overflows during contextual typing of a computed property name containing a yield expression in a generator method.*

 * created by **HuzaifaAbdulRehman**

### [PR microsoft/TypeScript-go#4744](https://github.com/microsoft/TypeScript-go/pull/4744) (Closed)

**Reorganize AST to prevent duplicate fields**

*Restructure AST definitions to eliminate duplicate struct fields such as UnionTypeNode and reduce memory usage.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/4744#issuecomment-5081194414) **jakebailey** said "@typescript-bot perf test this faster"
 * [today](https://github.com/microsoft/TypeScript-go/pull/4744#issuecomment-5081194612) **typescript-automation[bot]** reported the start of CI jobs and provided links to status and results
 * [today](https://github.com/microsoft/TypeScript-go/pull/4744#issuecomment-5081278216) **typescript-automation[bot]** provided the perf run results for the requested benchmarks

### [Issue microsoft/TypeScript-go#4745](https://github.com/microsoft/TypeScript-go/issues/4745) (Closed)

**Native API syntactic diagnostics omit start and length**

*Native API syntactic diagnostics incorrectly omit start and length offsets, preventing error location reporting.*

 * created by **helenkwok**
 * [today](https://github.com/microsoft/TypeScript-go/issues/4745#issuecomment-5081879077) **mrazauskas** noted that the Diagnostic interface changed and recommended using pos and end
 * [today](https://github.com/microsoft/TypeScript-go/issues/4745#issuecomment-5082238688) **helenkwok** thanked for the clarification, corrected the downstream harness's diagnostic mappings, and closed the issue as not a bug
 * (today) **helenkwok** closed the issue
 * (today) **helenkwok** closed the issue

### [PR microsoft/TypeScript-go#4746](https://github.com/microsoft/TypeScript-go/pull/4746) (Closed)

**fix: emit missing TS7059 errors**

*Add missing logic ported from TypeScript to emit TS7059 diagnostic errors in oxc.*

 * created by **camc314**
 * [later](https://github.com/microsoft/TypeScript-go/pull/4746#issuecomment-5083806727) **camc314** said "@codex review"

### [Issue microsoft/TypeScript-go#4748](https://github.com/microsoft/TypeScript-go/issues/4748) (Open)

**Panic: nil pointer in NodeList\.HasTrailingComma during incremental rebuild \(build\-mode declaration printer\) — 7\.0\.2 and current nightly**

*A nil pointer dereference in NodeList.HasTrailingComma triggers a panic during incremental build-mode declaration printing in TypeScript.*

 * created by **nikeedw**

