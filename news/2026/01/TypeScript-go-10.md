# Report for 2026-01-10 (Saturday, January 10th, 2026)

1 different users commented on 2 different issues.

## Recommended Actions

 * Response Recommended
    * @HananoshikaYomaru provided config and output showing tsgo ignored tsconfig.json exclude in [microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3733530689)
    * @HananoshikaYomaru reported that tsgo isn't respecting include/exclude settings in [microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3733546667)

## Activity Summary

### [Issue microsoft/TypeScript-go#2418](https://github.com/microsoft/TypeScript-go/issues/2418) (Open)

**\[BUG\] tsgo list more files than tsc**

*tsgo’s --listFilesOnly output includes extra files compared to tsc, breaking basic tsgo --noEmit CI checks.*

 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3678181840) **jakebailey** said "Can you use --explainFiles to check?"
 * [3 weeks ago](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3678525881) **HananoshikaYomaru** attached two log files and thanked @jakebailey for reviewing them
 * [yesterday](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3730926809) **jakebailey** asked for an example of an unexpected file, tsconfig settings, project details, and to compare against TS 6.0
 * [today](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3733530689) **HananoshikaYomaru** described a React project’s tsconfig.json and reported that tsgo --noEmit ignored the exclude setting, listing migration files
 * [today](https://github.com/microsoft/TypeScript-go/issues/2418#issuecomment-3733546667) **HananoshikaYomaru** reported that updating include settings still linted src/migrations and suspected tsgo ignored include/exclude

