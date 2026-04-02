# Report for 2026-03-29 (Sunday, March 29th, 2026)

13 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @dskloetc reported that their issue matches another user's report and occurs without specifying node10 in [microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4152848989)
    * @cscnk52 provided recommended moduleResolution settings and documentation link in [microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4152939556)

## Activity Summary

### [Issue microsoft/TypeScript#40562](https://github.com/microsoft/TypeScript/issues/40562) (Open, `Suggestion`, `Awaiting More Feedback`)

**Non‑\`void\` returning assertion functions**

*Enable TypeScript to define assertion functions with non-void generic return types, as needed for Jest matchers and similar APIs.*

 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/40562#issuecomment-2155567926) **ITenthusiasm** agreed that a 'mutates' keyword to indicate in-place array mutation would be useful, described performance drawbacks of Array.map creating new arrays, and proposed example syntax
 * [1.8 years ago](https://github.com/microsoft/TypeScript/issues/40562#issuecomment-2155579956) **ITenthusiasm** noted that this issue could relate to #17181 and suggested that a library identifying mutating functions could meet some of its requirements
 * [9 weeks ago](https://github.com/microsoft/TypeScript/issues/40562#issuecomment-3786993840) **mkantor** said "This is also related to #22865."
 * [today](https://github.com/microsoft/TypeScript/issues/40562#issuecomment-4150900529) **artur-klesun-st** highlighted that the feature would enable mutable object argument types similar to Rust and gave a TypeScript example demonstrating its use

### [Issue microsoft/TypeScript#62508](https://github.com/microsoft/TypeScript/issues/62508) (Open, `Discussion`)

**6\.0 Migration Guide**

*Placeholder issue for drafting and publishing the migration guide for version 6.0.*

 * [19 weeks ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-3511889471) **sujansince2003** suggested changing module resolution to 'bundler' and warned about potential package errors
 * [5 days ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4122670559) **dan-mcdonald** reported confusion about a deprecated 'moduleResolution=node10' error while using 'bundler' in tsconfig
 * [4 days ago](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4127577695) **RyanCavanaugh** said "@dan-mcdonald please log a new issue with a complete repro. Thanks!"
 * [later](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4152848989) **dskloetc** described that their issue matched another user's, showing the deprecated 'moduleResolution=node10' error when upgrading TypeScript without requesting node10 and noting they couldn't provide a repro
 * [later](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4152939556) **cscnk52** provided guidance on using node16/nodenext/bundler for moduleResolution and linked to the TypeScript docs
 * [later](https://github.com/microsoft/TypeScript/issues/62508#issuecomment-4153001690) **dskloetc** thanked cscnk52 for the information and mentioned that the error message could have been more helpful

### [Issue microsoft/TypeScript#63225](https://github.com/microsoft/TypeScript/issues/63225) (Open, `Needs Investigation`)

**\`Omit\` causes function to lose contextual typing**

*Omitting keys from AssertableState<T> in TypeScript 6.0 causes function parameters to lose contextual typing and default to any.*

 * created by **dragomirtitian**
 * [2 weeks ago](https://github.com/microsoft/TypeScript/issues/63225#issuecomment-4029620365) **Andarist** said "Bisects to https://github.com/microsoft/TypeScript/pull/60528 . I'll investigate it"
 * **RyanCavanaugh** added label `Needs Investigation`
 * [later](https://github.com/microsoft/TypeScript/issues/63225#issuecomment-4154951497) **Andarist** noted that a PR revamping mapped type keys would solve the problem but development had to wait for the 7.1 dev line

### [Issue microsoft/TypeScript#63291](https://github.com/microsoft/TypeScript/issues/63291) (Open, `Needs Investigation`, **ahejlsberg**)

**Removing optional modifier in a mapped type behaves inconsistently b/w array vs object**

*Under exactOptionalPropertyTypes, mapped array types lose undefined unions when removing optional modifiers, unlike object types.*

 * created by **juhort**
 * (5 days ago) **RyanCavanaugh** added label `Needs Investigation`, and assigned to **ahejlsberg**
 * [later](https://github.com/microsoft/TypeScript/issues/63291#issuecomment-4152793334) **Andarist** shared a trivial fix patch for stripping optionality when mapping over tuples under EOPT with a link to the PR and a detailed Strada patch

### [Issue microsoft/TypeScript#63307](https://github.com/microsoft/TypeScript/issues/63307) (Closed, `Won't Fix`)

**packageId is not generated when name or version fields are missing**

*TypeScript’s moduleNameResolver should generate packageId for packages missing name or version fields instead of returning undefined.*

 * (2 days ago) **RyanCavanaugh** added label `Won't Fix`, and removed label `Needs More Info`
 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4144496145) **RyanCavanaugh** noted that changing this wouldn't qualify for a 6.0 patch and that the TS7+ API would likely change making the issue moot
 * [today](https://github.com/microsoft/TypeScript/issues/63307#issuecomment-4151608046) **typescript-bot** said "This issue has been marked as "Won't Fix" and has seen no recent activity. It has been automatically closed for house-keeping purposes."
 * (today) **typescript-bot** closed the issue

### [Issue microsoft/TypeScript#63309](https://github.com/microsoft/TypeScript/issues/63309) (Closed, `Bug`, **RyanCavanaugh**, **Copilot**)

**Regression in 6\.0: type inferred from const with broader type is too narrow**

*TypeScript 6.0 mistakenly narrows a class property initialized from a union-typed constant to a single literal value.*

 * [2 days ago](https://github.com/microsoft/TypeScript/issues/63309#issuecomment-4145893834) **RyanCavanaugh** said "Bisects to #62243, which is pretty surprising?"
 * (2 days ago) **RyanCavanaugh** assigned to **Copilot**, **RyanCavanaugh**
 * **RyanCavanaugh** added label `Bug`

### [PR microsoft/TypeScript#63310](https://github.com/microsoft/TypeScript/pull/63310) (Closed, **RyanCavanaugh**, **Copilot**)

**Mark class property initializers as outside of CFA containers**

*Restore PropertyDeclaration as a control flow container to isolate class property initializer type inference and prevent module-level narrowing leaks*

 * [yesterday](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148381148) **typescript-bot** reported results of user tests comparing main and the PR merge, noting one Git clone failure but otherwise everything looked good
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148456905) **typescript-bot** reported successful test results from running the top 400 repos with tsc comparing main and PR merge
 * [yesterday](https://github.com/microsoft/TypeScript/pull/63310#issuecomment-4148850455) **typescript-bot** posted performance run results as requested
 * **RyanCavanaugh** added to milestone `TypeScript 6.0.2`

### [Issue microsoft/TypeScript#63311](https://github.com/microsoft/TypeScript/issues/63311) (Closed, `Not a Defect`)

**\`typescript\.d\.ts\` uses ES2015\+ globals \(\`Map\`, \`ReadonlyMap\`\) without \`/// \<reference lib\>\` directive**

*typescript.d.ts uses ES2015 Map and ReadonlyMap without a /// <reference lib='es2015' /> directive, causing type errors outside ES2015 contexts.*

 * created by **baraknaveh**
 * [today](https://github.com/microsoft/TypeScript/issues/63311#issuecomment-4149633663) **jakebailey** argued that libraries typically omit references for builtins, explained directive preservation behavior, stated compiler errors clearly instruct fixes, and noted default target is ES2025
 * **RyanCavanaugh** added label `Not a Defect`
 * [later](https://github.com/microsoft/TypeScript/issues/63311#issuecomment-4154354423) **RyanCavanaugh** said "TypeScript itself doesn't run in environments that predate these values, so if anything this is helpful for indicating that your config is wrong in some way."
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63313](https://github.com/microsoft/TypeScript/issues/63313) (Closed, `Not a Defect`)

**Type of return value of \`yield\` cannot be inferred from explicitly declared \`TNext\`**

*Generator yield return type isn't inferred from the declared TNext, causing 'i' to be any instead of number.*

 * created by **zimtsui**
 * [later](https://github.com/microsoft/TypeScript/issues/63313#issuecomment-4154411899) **RyanCavanaugh** explained that the situation was a true circularity and not a bug
 * **RyanCavanaugh** added label `Not a Defect`

### [Issue microsoft/TypeScript#63315](https://github.com/microsoft/TypeScript/issues/63315) (Closed, `Duplicate`)

**Error type constructor**

*Provide a type error constructor in TypeScript to allow explicit type-level errors instead of fallback to never.*

 * created by **masaeedu**
 * [yesterday](https://github.com/microsoft/TypeScript/issues/63315#issuecomment-4148730562) **MartinJohns** said "Duplicate of #23689."
 * **RyanCavanaugh** added label `Duplicate`

### [PR microsoft/TypeScript#63317](https://github.com/microsoft/TypeScript/pull/63317) (Closed)

**docs: Add Chinese README**

*Add a Chinese version of the project’s README to the documentation directory.*

 * created by **CJstate**
 * [today](https://github.com/microsoft/TypeScript/pull/63317#issuecomment-4150260532) **MartinJohns** said "This doesn't seem to serve any purpose."
 * [later](https://github.com/microsoft/TypeScript/pull/63317#issuecomment-4154609455) **RyanCavanaugh** said "This seems substantially worse than just letting people use machine translation."
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63318](https://github.com/microsoft/TypeScript/issues/63318) (Closed, `Unactionable`)

**typesctip 6 and package\.json exports definitions**

*TypeScript 6’s stricter package.json exports cause module resolution errors for three/examples/jsm/GLTFLoader imports.*

 * created by **darkship**
 * [today](https://github.com/microsoft/TypeScript/issues/63318#issuecomment-4151164042) **matheusschreiber** suggested adding `.js` extension to the module import path
 * (later) **RyanCavanaugh** added labels `Needs Investigation`, `Unactionable`, removed label `Needs Investigation`, assigned to **andrewbranch**, and unassigned **andrewbranch**
 * [later](https://github.com/microsoft/TypeScript/issues/63318#issuecomment-4154591031) **RyanCavanaugh** said "This is not a 6.0 regression and is the behavior at least as far back as 5.5"
 * (later) **RyanCavanaugh** closed the issue
 * [later](https://github.com/microsoft/TypeScript/issues/63318#issuecomment-4154968264) **darkship** noticed that their project was using module "ESNext" under TS 5.9.3 which worked but failed after upgrading to 6.0.2 and thanked @matheusschreiber

### [PR microsoft/TypeScript#63319](https://github.com/microsoft/TypeScript/pull/63319) (Closed, `dependencies`, `github_actions`)

**Bump the github\-actions group with 2 updates**

*Upgrade the GitHub Actions workflows by updating codecov-action to v6.0.0 and bumping codeql-action.*

 * created by **dependabot[bot]**
 * (today) **dependabot[bot]** added labels `dependencies`, `github_actions`, `dependencies`, `github_actions`
 * (later) **RyanCavanaugh** closed the issue

### [Issue microsoft/TypeScript#63320](https://github.com/microsoft/TypeScript/issues/63320) (Open, `Suggestion`, `Awaiting More Feedback`)

**importModuleSpecifier "shortest" does not choose shortest result among multiple matching paths aliases**

*TypeScript’s auto-import ‘shortest’ setting ignores path length and picks the first matching alias instead of the shortest.*

 * created by **GertSallaerts**
 * [later](https://github.com/microsoft/TypeScript/issues/63320#issuecomment-4154429746) **RyanCavanaugh** stated that the issue was uncommon, the workaround was reasonable, and a fix was unwarranted due to performance concerns
 * (later) **RyanCavanaugh** added labels `Suggestion`, `Awaiting More Feedback`

### [Issue microsoft/TypeScript#63321](https://github.com/microsoft/TypeScript/issues/63321) (Closed)

**\[FAQ\] Resolve TODO: Write up common symptoms of \`declare class\` / \`interface\` confusion\.**

*Add FAQ entry outlining differences and common pitfalls when using TypeScript's declare class versus interface.*

 * created by **5cover**
 * [later](https://github.com/microsoft/TypeScript/issues/63321#issuecomment-4154286645) **mkantor** explained that pull requests can be submitted to the microsoft/TypeScript-wiki repository and provided an example link
 * [later](https://github.com/microsoft/TypeScript/issues/63321#issuecomment-4154311389) **RyanCavanaugh** said "Integrated, thanks!"
 * (later) **RyanCavanaugh** closed the issue

### [PR microsoft/TypeScript#63322](https://github.com/microsoft/TypeScript/pull/63322) (Closed)

**fix: prevent stack overflow in symbolToTypeNode with recursive return type references**

*Implement cycle detection in symbolToTypeNode using a visitedSymbols set to avoid stack overflow from recursive return types.*

 * created by **wdskuki**
 * [later](https://github.com/microsoft/TypeScript/pull/63322#issuecomment-4154199586) **wdskuki** said "@microsoft-github-policy-service agree"
 * [later](https://github.com/microsoft/TypeScript/pull/63322#issuecomment-4154528847) **RyanCavanaugh** said "See https://github.com/microsoft/TypeScript?tab=readme-ov-file#contribute - bugfixes should be in typescript-go repo"
 * (later) **RyanCavanaugh** closed the issue

