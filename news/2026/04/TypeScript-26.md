# Report for 2026-04-26 (Sunday, April 26th, 2026)

9 different users commented on 13 different issues.

## Recommended Actions

 * Response Recommended
    * @mliebold-jax provided repro steps via a linked issue in [microsoft/TypeScript#60854](https://github.com/microsoft/TypeScript/issues/60854#issuecomment-4327986912)
    * @pratyush618 provided repro steps and a suggested fix location in [microsoft/TypeScript#63420](https://github.com/microsoft/TypeScript/issues/63420#issuecomment-4322765618)
    * @creazyfrog asked if the PR did not meet expectations in [microsoft/TypeScript#63438](https://github.com/microsoft/TypeScript/pull/63438#issuecomment-4322551280)

## Activity Summary

### [Issue microsoft/TypeScript#38638](https://github.com/microsoft/TypeScript/issues/38638) (Open, `Suggestion`, `Awaiting More Feedback`)

**Improve declare module wildcards so that they can match parts of a path more like a glob**

*Support glob-style wildcards in TypeScript’s declare module paths to allow flexible multi-part path matching.*

 * [3.5 years ago](https://github.com/microsoft/TypeScript/issues/38638#issuecomment-1255678162) **Nantris** said "It would be great if we could do like ours-somemodule-platform and target it with ours-*-platform"
 * [3.3 years ago](https://github.com/microsoft/TypeScript/issues/38638#issuecomment-1367368553) **Qtax** mentioned that image-minimizer-webpack-plugin also required this support and described using a hack for module declarations
 * [2.5 years ago](https://github.com/microsoft/TypeScript/issues/38638#issuecomment-1751910462) **sdegutis** said "I just ran into the issue that foo-bar.md doesn't match *.md but foobar.md does. There's no way to fix this as far as I can tell."
 * [later](https://github.com/microsoft/TypeScript/issues/38638#issuecomment-4326797595) **wuhkuh** reported having to sprinkle // @ts-expect-error comments when bundling audio assets via rolldown until the issue is resolved

### [Issue microsoft/TypeScript#60854](https://github.com/microsoft/TypeScript/issues/60854) (Closed, `Needs More Info`)

**TS server significantly slower to initialize when \`includePackageJsonAutoImports\` is \`auto\`**

*TypeScript server startup doubles in a monorepo after migrating to package.json exports because it scans far more auto-import files by default.*

 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/60854#issuecomment-2568266644) **RyanCavanaugh** said "That's interesting. We can take a look if there's a repro that demonstrates the difference."
 * [1.3 years ago](https://github.com/microsoft/TypeScript/issues/60854#issuecomment-2568272024) **OliverJAsh** said "I just tried to create a reduced test case but no luck so far. I'll give this some more thought but meanwhile let's close this."
 * (1.3 years ago) **OliverJAsh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/60854#issuecomment-4327986912) **mliebold-jax** said "I think I've found a similar issue to this here. I listed the steps within the linked issue to reproduce it."

### [PR microsoft/TypeScript#63417](https://github.com/microsoft/TypeScript/pull/63417) (Closed, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 4 updates**

*Upgrade four GitHub Actions dependencies (upload-artifact, cache, codeql-action, and github-script) to their latest versions in the root directory.*

 * (1 week ago) **dependabot[bot]** added labels `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63417#issuecomment-4323488434) **dependabot[bot]** said "Looks like these dependencies are updatable in another way, so this is no longer needed."
 * (today) **dependabot[bot]** closed the issue

### [Issue microsoft/TypeScript#63420](https://github.com/microsoft/TypeScript/issues/63420) (Open, `Bug`, `Domain: Intersection`)

**union of pattern template literals intersected with optional brand mutually assignable to one with incompatible brand**

*TypeScript incorrectly allows mutual assignment between unions of template literal types intersected with incompatible optional brand properties.*

 * (5 days ago) **RyanCavanaugh** added labels `Bug`, `Domain: Intersection`, and set milestone to `Backlog`
 * [today](https://github.com/microsoft/TypeScript/issues/63420#issuecomment-4322765618) **pratyush618** explained a reproducible bug in TypeScript where intersection sources against union-of-intersections targets incorrectly passed type checking and suggested a fix in checker.ts

### [Issue microsoft/TypeScript#63421](https://github.com/microsoft/TypeScript/issues/63421) (Closed, `Not a Defect`)

**"Using type predicates" documentation promotes lying to the type system**

*The TypeScript documentation's type predicate example encourages misuse of 'as' assertions, undermining type safety.*

 * [4 days ago](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4298029720) **RyanCavanaugh** argued that there’s usually no perfect way to write a type predicate function because built-in narrowing suffices and noted that using ‘in’ loses type safety on the key
 * [3 days ago](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4303181436) **ilyash-b** asked whether to comment on this in the handbook or close the issue, noting that 'in' is not a clear winner over 'as'
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4312902534) **jendrikw** said "Type guard are always circumventing the type system. I don't use them at all and just test for the properties that I actually need."
 * [today](https://github.com/microsoft/TypeScript/issues/63421#issuecomment-4323651670) **typescript-bot** said "This issue has been marked as "Not a Defect" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63426](https://github.com/microsoft/TypeScript/issues/63426) (Closed, `Duplicate`)

**Incorrect TS18047 Error \-\-\> "variable is possibly null"**

*TypeScript incorrectly flags the selection variable as possibly null even after an explicit null check in v6.0.3.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4312855925) **mkantor** explained that feature addition PRs were on hold until the 7.0 release and noted the 7.0 beta was recently released
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4313308617) **PoseidonEnergy** asked how to get feedback on their PR from the TypeScript team given their issue was marked duplicate
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4313573692) **MartinJohns** said "Just FYI, the new compiler is written in Go. The TypeScript code base won't be continued anymore."
 * [today](https://github.com/microsoft/TypeScript/issues/63426#issuecomment-4323651561) **typescript-bot** said "This issue has been marked as "Duplicate" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [PR microsoft/TypeScript#63438](https://github.com/microsoft/TypeScript/pull/63438) (Closed, `For Backlog Bug`)

**fix\(checker\): emit precise error when labeled continue/break targets a non\-enclosing label**

*Emit specific TS1115 and TS1116 errors for labeled continue or break statements targeting non-enclosing labels in the same function instead of TS1107.*

 * created by **creazyfrog**
 * **typescript-bot** added label `For Backlog Bug`
 * [today](https://github.com/microsoft/TypeScript/pull/63438#issuecomment-4322343495) **jakebailey** said "Can you please tell me what tool you used to send this PR, and how you chose this issue to fix?"
 * [today](https://github.com/microsoft/TypeScript/pull/63438#issuecomment-4322551280) **creazyfrog** explained that they used Claude code to generate the PR, described how they selected the issue, and asked if it did not meet expectations
 * [today](https://github.com/microsoft/TypeScript/pull/63438#issuecomment-4322761471) **jakebailey** said "Please read CONTRIBUTING.md"
 * (today) **creazyfrog** closed the issue

### [Issue microsoft/TypeScript#63442](https://github.com/microsoft/TypeScript/issues/63442) (Open)

**Formatting fails for entire file when a line contains only whitespace between two comments**

*A line containing only whitespace between two single-line comments prevents VS Code from formatting the entire TypeScript or JavaScript file.*

 * created by **glitcher255**

### [PR microsoft/TypeScript#63443](https://github.com/microsoft/TypeScript/pull/63443) (Open, `For Uncommitted Bug`, `dependencies`, `github_actions`)

**Bump the github\-actions group across 1 directory with 5 updates**

*Update five GitHub Actions packages in the root directory to newer versions.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * **typescript-bot** added label `For Uncommitted Bug`

### [PR microsoft/TypeScript#63444](https://github.com/microsoft/TypeScript/pull/63444) (Open, `For Uncommitted Bug`)

**fix: remove grammatically incorrect 'the' before x in Math\.sign JSDoc**

*Remove the grammatically incorrect 'the' before x in the Math.sign JSDoc description.*

 * created by **AmSach**
 * **typescript-bot** added label `For Uncommitted Bug`

### [Issue microsoft/TypeScript#63445](https://github.com/microsoft/TypeScript/issues/63445) (Open)

**TS server crashes with \`@mui/icons\-material\` v9 package**

*@mui/icons-material v9 causes the TypeScript server to crash repeatedly during tsconfig.app.json initialization in VS Code.*

 * created by **mliebold-jax**

