# Report for 2025-11-27 (Thursday, November 27th, 2025)

7 different users commented on 7 different issues.

## Recommended Actions

 * Response Recommended
    * @trueadm provided repro steps as requested in [microsoft/TypeScript-go#1952](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3589398392)
    * @liuxingbaoyu provided repro steps as requested in [microsoft/TypeScript-go#2060](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3586819628)

## Activity Summary

### [Issue microsoft/TypeScript-go#1952](https://github.com/microsoft/TypeScript-go/issues/1952) (Open, `Crash`, `Needs More Info`, **DanielRosenwasser**, **weswigham**)

**Declaration emit crash**

*The declaration emitter panics with ‘Unknown parent for parameter: KindArrowFunction’ during compilation.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3487624973) **DanielRosenwasser** said "I'll try to get a minimal repro, but I need to make a custom build to echo the file name and run single-threaded. It's going to be a slog."
 * **DanielRosenwasser** assigned to **DanielRosenwasser**
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3494573284) **mmichels-brex** said "Having the same error here in the latest tsgo build"
 * [later](https://github.com/microsoft/TypeScript-go/issues/1952#issuecomment-3589398392) **trueadm** provided a minimal reproduction and noted it worked fine with tsc

### [Issue microsoft/TypeScript-go#2060](https://github.com/microsoft/TypeScript-go/issues/2060) (Open, `Needs More Info`)

**Typescript\-go does not infer large generics due to maximum length compiler will serialize**

*typescript-go cannot infer large nested generics for SStruct because the inferred type exceeds the compiler’s maximum serialized length, requiring manual annotations.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3547542225) **Raynos** described finding that SocketIssueList contained deeply nested references and a union of over 120 types, causing the type inference limit
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3547546359) **Raynos** noted that TypeScript 5.x was more tolerant of large unions and abandoned creating a reproduction due to complexity
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3547570066) **Raynos** suggested adding the count of types to the error message next to the maximum length
 * [today](https://github.com/microsoft/TypeScript-go/issues/2060#issuecomment-3586819628) **liuxingbaoyu** mentioned that Babel encountered the issue in recent versions and provided reproduction steps and a PR link

### [Issue microsoft/TypeScript-go#2162](https://github.com/microsoft/TypeScript-go/issues/2162) (Open, `Domain: Type Checking`, **ahejlsberg**)

**Type inference lost for callback parameter**

*Using ts-go configuration causes TypeScript to lose type inference for the organization plugin's sendInvitationEmail callback parameter.*

 * created by **Azzerty23**

### [Issue microsoft/TypeScript-go#2163](https://github.com/microsoft/TypeScript-go/issues/2163) (Closed, `Crash`)

**JetBrains Webstorm in Turborepo Crash**

*JetBrains WebStorm crashes in a Turborepo project due to a TypeScript Go bundler error resolving symlinks.*

 * created by **vrn-hkz**
 * **vrn-hkz** added label `Crash`
 * [later](https://github.com/microsoft/TypeScript-go/issues/2163#issuecomment-3588294918) **vrn-hkz** suggested manually adding the TypeScript path under Languages and Frameworks > TypeScript
 * (later) **vrn-hkz** closed the issue

### [Issue microsoft/TypeScript-go#2164](https://github.com/microsoft/TypeScript-go/issues/2164) (Closed)

**Pure annotation is dropped on property values**

*In the latest tsgo version, PURE annotations on property value calls (e.g., string()) within object literals are unexpectedly dropped, unlike in version 5.9.3.*

 * created by **mary-ext**

### [PR microsoft/TypeScript-go#2165](https://github.com/microsoft/TypeScript-go/pull/2165) (Closed)

**Merge main**

*Integrate the latest commits from the main branch into the current working branch to stay up-to-date.*

 * created by **bartlomieju**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2165#issuecomment-3589149177) **jakebailey** said "I don't think you meant to send this to this repo"
 * [later](https://github.com/microsoft/TypeScript-go/pull/2165#issuecomment-3589254637) **bartlomieju** said "Ooops, sorry, wrong repo indeed!"
 * (later) **bartlomieju** closed the issue

