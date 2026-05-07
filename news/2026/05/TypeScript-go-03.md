# Report for 2026-05-03 (Sunday, May 3rd, 2026)

7 different users commented on 12 different issues.

## Recommended Actions

 * Response Recommended
    * @CarlosZiegler reported also seeing the issue in the cursor in [microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4369143872)

## Activity Summary

### [PR microsoft/TypeScript-go#2478](https://github.com/microsoft/TypeScript-go/pull/2478) (Open)

**Exit LSP process if parent process stops existing**

*Implement periodic parent process ID checks in the LSP server to terminate the server when the parent process exits.*

 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4269974535) **jakebailey** said "Going to draft this for the time being again, sorry; I want to double check that these comments are actually correct and would rather not cram it in."
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4270307434) **andrewbranch** said "I'm not against this if we think we still need it, but it feels like a bug (like #2499 was) if we can't exit just by reading from a STDIN that's no longer connected to anything"
 * [2 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4270354928) **jakebailey** explained that a client could set up a FIFO as the file descriptor for a child process which might never close
 * [later](https://github.com/microsoft/TypeScript-go/pull/2478#issuecomment-4372407010) **andrewbranch** said "I ended last week with 7 orphaned tsgo processes, so I guess we do still need this."

### [Issue microsoft/TypeScript-go#3621](https://github.com/microsoft/TypeScript-go/issues/3621) (Open, `Crash`, `Needs More Info`)

**Panic Alert Notification when Cursor edits some file and opening that file causes panic\.**

*Opening or editing a file causes a panic in the semanticTokens request because a token improperly spans multiple lines.*

 * **RealHaris** added label `Crash`
 * [4 days ago](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4342371254) **Swiftwork** said "Observing same issue for the last 1-2 weeks"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4361443953) **Raynos** said "Observing same issue in cursor too."
 * [later](https://github.com/microsoft/TypeScript-go/issues/3621#issuecomment-4369143872) **CarlosZiegler** said "Observing same issue in cursor too. "

### [Issue microsoft/TypeScript-go#3691](https://github.com/microsoft/TypeScript-go/issues/3691) (Closed, `bug`, `Domain: Type Checking`, **ahejlsberg**)

**Behavior difference: Assigning \`Object\.values\(obj\)\` to \`obj\[field\]\` gives error on tsgo but not on tsc**

*Assigning Object.values(obj) to a property triggers a self-referential initialization type error in tsgo but not in tsc*

 * created by **hkleungai**
 * (later) **ahejlsberg** added labels `bug`, `Domain: Type Checking`, set milestone to `TypeScript 7.0 RC`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3691#issuecomment-4372295101) **ahejlsberg** explained that failing to recognize an expando object literal had led to inferring an index type and causing circularity

### [Issue microsoft/TypeScript-go#3693](https://github.com/microsoft/TypeScript-go/issues/3693) (Closed, `wontfix`)

**Behavior difference: Exporting object literal from js file emits object literal type in tsgo, as opposed to \`namespace\` in tsc\.**

*tsgo exports JavaScript object literals as literal types instead of namespaces like tsc, and this behavior difference (along with optional omission of @satisfies JSDoc comments) should be documented in CHANGES.md.*

 * created by **hkleungai**
 * [later](https://github.com/microsoft/TypeScript-go/issues/3693#issuecomment-4372517238) **ahejlsberg** explained that the new declaration file emitter differs from Strada and stays closer to the original code and pointed to the CHANGES.md section

### [Issue microsoft/TypeScript-go#3694](https://github.com/microsoft/TypeScript-go/issues/3694) (Closed, `wontfix`, **DanielRosenwasser**, **iisaduan**, **Copilot**)

**Behavior difference: jsdoc \`@param\` referencing object attribute value throws TS2749 in tsc but throws TS2503 in tsgo**

*When using jsdoc @param to reference an object property, tsgo throws TS2503 instead of TS2749 like tsc*

 * created by **hkleungai**

### [PR microsoft/TypeScript-go#3695](https://github.com/microsoft/TypeScript-go/pull/3695) (Closed)

**Fix inference from never into union targets**

*Adjust type inference to correctly exclude never types from union targets, aligning behavior with Strada code.*

 * created by **Andarist**

### [PR microsoft/TypeScript-go#3696](https://github.com/microsoft/TypeScript-go/pull/3696) (Open, `dependencies`, `devcontainers_package_manager`)

**Bump ghcr\.io/devcontainers/features/node from 1\.7\.1 to 2\.0\.0**

*Bump devcontainers feature node from version 1.7.1 to version 2.0.0 via Dependabot.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `devcontainers_package_manager`, `dependencies`, `devcontainers_package_manager`

### [PR microsoft/TypeScript-go#3697](https://github.com/microsoft/TypeScript-go/pull/3697) (Open, `dependencies`, `github_actions`)

**Bump github/codeql\-action from 4\.35\.2 to 4\.35\.3 in the github\-actions group across 1 directory**

*Bump github/codeql-action from v4.35.2 to v4.35.3, adding private registry support, deprecation warnings, and bug fixes.*

 * created by **dependabot[bot]**
 * (later) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`

### [PR microsoft/TypeScript-go#3698](https://github.com/microsoft/TypeScript-go/pull/3698) (Open)

**Add minimal tsc output format**

*Implement a new --outputFormat minimal option in tsgo to emit compact, one-line diagnostics for easier parsing and reduced token usage.*

 * created by **JoviDeCroock**

### [PR microsoft/TypeScript-go#3699](https://github.com/microsoft/TypeScript-go/pull/3699) (Closed)

**Fix circularity in expando object property assignment**

*Break the circular reference causing infinite recursion during expando object property assignments.*

 * created by **ahejlsberg**

