# Report for 2026-01-23 (Friday, January 23rd, 2026)

15 different users commented on 17 different issues.

## Recommended Actions

 * Response Recommended
    * @ffmiruz asked if the repository had long lines and suggested a performance optimization in [microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3794583430)
    * @bastiankistner offered to provide logs/traces in [microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3794827972)
    * @austinfennacy provided performance observations and a reproduction clip in [microsoft/TypeScript-go#2561](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791740211)
    * @ilbrando asked if the listed version matches the one they have installed and are experiencing the issue on in [microsoft/TypeScript-go#2573](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3794486254)

## Activity Summary

### [Issue microsoft/TypeScript-go#1673](https://github.com/microsoft/TypeScript-go/issues/1673) (Open, `Crash`, **Copilot**)

**Panic on textDocument/definition**

*A panic occurs during textDocument/definition handling when the requested line number exceeds the document’s line map.*

 * [12 weeks ago](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3447744485) **jakebailey** reported a panic in the definition handler due to a bad line number
 * **jakebailey** assigned to **Copilot**
 * [1 week ago](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3738641522) **mustafa519** mentioned also getting similar errors and provided a stack trace
 * [today](https://github.com/microsoft/TypeScript-go/issues/1673#issuecomment-3792918644) **DanielRosenwasser** said "@mustafa519 I think that is a distinct crash - I filed that here a few weeks ago and it should be fixed now: https://github.com/microsoft/typescript-go/issues/2492"

### [Issue microsoft/TypeScript-go#2054](https://github.com/microsoft/TypeScript-go/issues/2054) (Closed, `Domain: Build Mode`, `Needs More Info`, **sheetalkamat**)

**Semantics of \-\-stopBuildOnErrors has changed, now stops build on first error, instead of first project**

*tsgo’s --stopBuildOnErrors now halts the build and suppresses errors after the first failure rather than only skipping subsequent projects.*

 * [8 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2054#issuecomment-3576069209) **Raynos** noted that noEmitOnError was set to true in the tsconfig
 * [6 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2054#issuecomment-3629345499) **sheetalkamat** requested a minimal repro and noted surprising ordering of semantic and declaration emit errors
 * **sheetalkamat** added label `Needs More Info`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2054#issuecomment-3792092118) **sheetalkamat** said "Closing this for lack of repro steps. When we have details we can reopen again"
 * (today) **sheetalkamat** closed the issue

### [Issue microsoft/TypeScript-go#2402](https://github.com/microsoft/TypeScript-go/issues/2402) (Open, `Crash`)

**tsgo takes forever to compile, 325seconds vs typescript 42seconds**

*tsgo watch compilation takes 325s versus TypeScript’s 42s, and the reporter requests help diagnosing and resolving the slowdown.*

 * [5 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3673779704) **jogibear9988** asked how to track down which files cause the issue and whether they could share via a private repo; noted that reverting to yesterday’s version did not resolve it
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3703426438) **jogibear9988** reported that the newest version still errored, observed that disabling sourcemaps reduced ts-go build time to 13s versus 32s for normal TypeScript, and noted a ~5s startup delay before the build message
 * [3 days ago](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3771891076) **jogibear9988** said "Any ideas how we could proceed with this?"
 * [later](https://github.com/microsoft/TypeScript-go/issues/2402#issuecomment-3794583430) **ffmiruz** pointed out that scanning from the start for each position causes O(n²) behavior on long lines, asked if the repository had long lines, and suggested using the TypeScript O(1) approach

### [PR microsoft/TypeScript-go#2434](https://github.com/microsoft/TypeScript-go/pull/2434) (Open)

**Experiment: Quantified Types**

*Seeking a TypeScript function signature to consume an array of heterogeneous Layer objects without collapsing distinct generics.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705823991) **Andarist** suggested using reverse mapped types from two TypeScript PRs and provided a playground example
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3705842553) **devanshj** said "Yeah I think in theory you could pull it off with reverse mapped types and with some enhancements in the checker but then quantified types are nicer to read/understand... so I'm a bit biased haha"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3787582505) **Diggsey** expressed desire for quantified types and argued that reverse mapped types leak complexity compared to quantified types, noting that function types already support quantification
 * [today](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3793031614) **clinuxrulz** proposed an effect pipe example and stated it could only be implemented via existential types
 * [later](https://github.com/microsoft/TypeScript-go/pull/2434#issuecomment-3794171335) **devanshj** suggested implementing `pipe` without existential types using finite overloads and provided example links

### [PR microsoft/TypeScript-go#2498](https://github.com/microsoft/TypeScript-go/pull/2498) (Open)

**Declaration \(d\.ts\) output diff breakdown as seen in \`effect\`**

*Comparison of tsc and tsgo declaration file outputs highlighting syntax and type alias differences in the Effect v4 codebase.*

 * [1 week ago](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3744922224) **jakebailey** said "You should test with #2459, this is still a WIP area"
 * [2 days ago](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3781320725) **jakebailey** said "I am a little confused as to how these are high-priority issues; are these not all identical semantically?"
 * [yesterday](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3783734964) **fubhy** clarified that most signature changes were semantically identical except one altering the return type and noted other adjustments were QoL/readability improvements
 * [today](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3791516119) **jakebailey** asked why getConfig function declaration included undefined return in the emitted output
 * [today](https://github.com/microsoft/TypeScript-go/pull/2498#issuecomment-3791520658) **jakebailey** confirmed that #2459 will preserve types as-written to support the "before" suggestion

### [Issue microsoft/TypeScript-go#2540](https://github.com/microsoft/TypeScript-go/issues/2540) (Closed)

**Should handle \`FORCE\_COLOR\` environment variable**

*Support the FORCE_COLOR environment variable to override TTY detection and enable colored output for exec calls*

 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765354673) **jakebailey** questioned why this was needed now given the old codebase didn't do it
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765403442) **so1ve** described the difference between vue-tsc and vue-tsgo and requested colored and formatted tsgo help text appended to the CLI's help text like tsx
 * [5 days ago](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3765440078) **jakebailey** noted that picocolors, chalk, and Node support this, but TypeScript has never supported it, so it was surprising to require it now
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3793853624) **silverwind** recommended supports-color and go-supportscolor packages for bullet-proof color support
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3794000512) **jakebailey** said "We won't need that; it's just an environment variable check."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3794012015) **silverwind** stated that an env var check was sufficient for FORCE_COLOR support and that using FORCE_COLOR simplified color handling by delegating to the user
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3794020457) **jakebailey** said "I don't think we need anything more fancy (see how picocolors does it). We wouldn't take on a dep for this anyhow, since we need to be able to test it, via our own host abstraction."
 * [today](https://github.com/microsoft/TypeScript-go/issues/2540#issuecomment-3794030946) **silverwind** said "Yeah FORCE_COLOR support would be sufficient to get color output in cases where stdout is not a TTY, like on CI environments."

### [Issue microsoft/TypeScript-go#2555](https://github.com/microsoft/TypeScript-go/issues/2555) (Open, `Domain: Editor`)

**Installing Native Preview broke TS Imports**

*Installing VS Code’s Native Preview TypeScript extension on macOS breaks TypeScript auto-import suggestions despite reverting settings and reinstalling the editor.*

 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3778473834) **rubnogueira** suggested including the "node" types in tsconfig.json and referenced a TypeScript issue for defaults
 * [2 days ago](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3779894761) **tikki100** reported that the suggestion did not resolve the issue and provided detailed reproduction steps
 * [today](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3789626673) **rubnogueira** explained that with TypeScript 6.0 the tsconfig.json “types” array defaults to empty and requires explicitly listing relevant React types
 * [today](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3790969410) **jakebailey** clarified that the change hasn't been made yet and that the issue is unrelated
 * [later](https://github.com/microsoft/TypeScript-go/issues/2555#issuecomment-3794827972) **bastiankistner** described lacking import autocompletions, noted go-to-definition works, recalled it worked previously, and offered to post logs/traces

### [Issue microsoft/TypeScript-go#2561](https://github.com/microsoft/TypeScript-go/issues/2561) (Open, `Crash`)

**v0\.20260119\.1 crashes ts server for large project, v0\.20260116\.1 works**

*TypeScript Native Preview v0.20260119.1 crashes the TS server on large, high-memory projects, whereas v0.20260116.1 works.*

 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3787010907) **DanielRosenwasser** suggested that a regression might stem from PR 2499, that PR 2568 could have fixed it, and asked to try version 0.20260122.4
 * [today](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3789506705) **Titozzz** said "Just FYI we also noticed that since 3-4 days, and team members have either rolled back to a previous version or disabled tsgo. Someone noticed RAM usage up to 40 Go from the server!"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3790085897) **kratos-respawned** reported that the language server memory usage reached 92GB
 * [today](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791552923) **Titozzz** said "Seems like 0.20260122.4  is better, will report if issue rises again"
 * [today](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791740211) **austinfennacy** described memory usage issues across versions, noted a crash on version 0.20260119, observed fluctuating memory on 0.20260122.4, and indicated intent to keep auto-update enabled while leaving the issue open
 * [today](https://github.com/microsoft/TypeScript-go/issues/2561#issuecomment-3791903072) **DanielRosenwasser** announced that the issue was solved by PR #2553, noted version 0.20260122.4 as a last-known-good release, and recommended against pinning to a specific extension version

### [Issue microsoft/TypeScript-go#2573](https://github.com/microsoft/TypeScript-go/issues/2573) (Open, `Domain: Editor`, `Needs More Info`, **andrewbranch**)

**Seems like language server can't keep up with changes made in editor**

*The language server can't keep pace with editor changes, reporting outdated errors until it's restarted.*

 * created by **ilbrando**
 * **ilbrando** added label `Domain: Editor`
 * [today](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3790702573) **rubnogueira** noted that the issue was already solved in a previous issue but not in the latest release
 * [today](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3790986872) **jakebailey** said "That should be in 0.20260122.4."
 * [later](https://github.com/microsoft/TypeScript-go/issues/2573#issuecomment-3794486254) **ilbrando** said "Just saw that is the version I have installed and are experiencing the issue on?"

### [PR microsoft/TypeScript-go#2575](https://github.com/microsoft/TypeScript-go/pull/2575) (Closed)

**Don't build all platforms in parallel for release in CI**

*Modify CI release pipeline to build each platform sequentially with cache clearing to avoid space limitations.*

 * created by **jakebailey**
 * (today) **jakebailey** closed the issue

### [Issue microsoft/TypeScript-go#2576](https://github.com/microsoft/TypeScript-go/issues/2576) (Open)

**Autocompletions and quick fix suggestions try to import from "@types" packages**

*tsgo quick fixes and autocompletions wrongly import from @types packages instead of real modules*

 * created by **kyle-sawatsky**

### [PR microsoft/TypeScript-go#2577](https://github.com/microsoft/TypeScript-go/pull/2577) (Open)

**Add \-\-release flag to emulate real released binaries, rename release to nodebug**

*Add a --release flag to generate stripped release binaries and rename the release build tag to nodebug.*

 * created by **jakebailey**
 * [today](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3793259156) **rubiesonthesky** said "nodebug seems logical flag, but without context, it’s easy to read it as “node bug” 🐛 probably no harm, just funny coincidence. "
 * [today](https://github.com/microsoft/TypeScript-go/pull/2577#issuecomment-3793261911) **jakebailey** said they thought the name was funny, couldn't think of a better name, suggested leaving it as release and questioned flipping code in release mode

### [Issue microsoft/TypeScript-go#2578](https://github.com/microsoft/TypeScript-go/issues/2578) (Closed, `Crash`)

**panic: runtime error: invalid memory address or nil pointer dereference**

*A nil pointer dereference panic occurs in the MetadataTransformer.injectClassTypeMetadata function when processing class declarations.*

 * created by **Zzzen**
 * **Zzzen** added label `Crash`

### [PR microsoft/TypeScript-go#2579](https://github.com/microsoft/TypeScript-go/pull/2579) (Closed)

**Fix nil modifier list metadata loc**

*Correct the location metadata for nil modifier lists to ensure accurate modifier handling.*

 * created by **Zzzen**
 * [later](https://github.com/microsoft/TypeScript-go/pull/2579#issuecomment-3794372121) **DanielRosenwasser** said "I guess I don't understand how there are no other tests that run into this."

### [Issue microsoft/TypeScript-go#2580](https://github.com/microsoft/TypeScript-go/issues/2580) (Closed, `Crash`, **DanielRosenwasser**, **Copilot**)

**textDocument/completion runtime error: invalid memory address or nil pointer dereference**

*textDocument/completion handler in the TypeScript-Go language server panics with a nil pointer dereference when computing import statement completions.*

 * created by **sanny-io**
 * **sanny-io** added label `Crash`

