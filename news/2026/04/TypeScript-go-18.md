# Report for 2026-04-18 (Saturday, April 18th, 2026)

4 different users commented on 3 different issues.

## Recommended Actions

 * Response Recommended
    * @pedro757 reported that the latest version used 50% more RAM and was still worse than version 20260408 in [microsoft/TypeScript-go#3423](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4274358674)

## Activity Summary

### [Issue microsoft/TypeScript-go#3423](https://github.com/microsoft/TypeScript-go/issues/3423) (Closed, `Crash`)

**Memory usage spiked in version 7\.0\.0\-dev\.20260416\.1**

*Memory usage increased from about 1.1GB to 6GB after upgrading to version 7.0.0-dev.20260416.1*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4261499932) **sbking** provided a heap profile with the setting disabled
 * (2 days ago) **jakebailey** closed the issue
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4262703657) **jakebailey** said "@sbking Can you try again with the version we just put out on the marketplace?"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4274358674) **pedro757** said "@jakebailey I think it improved a bit in the latest version, but still not as good as version 20260408, latest version uses 50% more RAM"
 * [today](https://github.com/microsoft/TypeScript-go/issues/3423#issuecomment-4274597818) **jakebailey** said "There's nothing else that should have affected that; if possible a repro would be good, or a bisect "

### [Issue microsoft/TypeScript-go#3426](https://github.com/microsoft/TypeScript-go/issues/3426) (Open, `possible improvement`, **ahejlsberg**)

**tsc produces error, tsgo doesn't with sufficiently nested type**

*TypeScript 6 reports a nested type incompatibility between input and output APIs that tsgo overlooks until a layer is removed.*

 * **ahejlsberg** added label `possible improvement`
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4271613649) **joshcartme** inquired whether differentiating between generic and concrete types in Copilot's PR was reasonable after building and testing it against his repro and noting tsgo reported the error
 * [today](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4273579488) **ahejlsberg** pointed out that the proposed fix was invalid because generative recursive type references such as Deep<Deep<T>> can lack generic types after instantiation but still require detection
 * [today](https://github.com/microsoft/TypeScript-go/issues/3426#issuecomment-4274224844) **joshcartme** acknowledged understanding after explanation

### [PR microsoft/TypeScript-go#3440](https://github.com/microsoft/TypeScript-go/pull/3440) (Open)

**\[internal/compiler/js\_exports\.go\] Export symbols for ts\-morph**

*Proposes exporting symbols for ts-morph in internal/compiler/js_exports.go to facilitate integration and notes wasm size reduction when switching to typescript-go.*

 * created by **SamuelMarks**

