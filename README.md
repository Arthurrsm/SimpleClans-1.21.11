# SimpleClans – Paper 1.21.11 Port

**This is an unofficial port** of the SimpleClans plugin, adapted for **Paper 1.21.11** servers and built with **Java 21**. It is not maintained by the original author and is not available on Spigot.

To download this version, use **only** the [Releases](../../releases) section of this repository. Do not use the download links from the original project: they point to older versions that do not work on Paper 1.21.11.

## What changed from the original

- Built against the Paper 1.21.11 API and Java 21 (the original targets Spigot 1.16.4 and Java 8).
- XSeries updated to 13.8.0. The old version prevented the plugin from enabling on Paper 1.20.5 and later.
- `plugin.yml` with `api-version: '1.21'`.
- Native WorldGuard 7 support restored (`WorldGuardProvider`).
- Deprecated calls replaced: main-hand item (`getItemInMainHand`) and player head owner (`setOwningPlayer`).
- Removed build plugins that only served the original author (javadoc, copying to a test server, git hash).

Supported integrations: Vault, PlaceholderAPI, LuckPerms, WorldGuard (6 and 7), GriefPrevention, Landlord, DiscordSRV, and BungeeCord.

## Download

Download `SimpleClans-1.21.11.jar` from the [Releases](../../releases) section and place it in your server's `plugins/` folder.

## Before installing

- Back up the `plugins/SimpleClans` folder (config and database).
- This version runs automatic database migrations (new columns). **You cannot go back to the old `.jar` using the same database.**

## Building from source

Requirements: JDK 21 and Maven (for example, [Temurin 21](https://adoptium.net/) for Java and [Maven](https://maven.apache.org/) for the build).

From the project folder, run:

```
mvn -B -Dmaven.test.skip=true clean package
```

The output file is `target/SimpleClans.jar`. The first build takes a few minutes while dependencies download.

## Credits

The original SimpleClans project and its authors. This port only adapts the code to the current Paper version.

## License

See the [LICENSE](LICENSE) file.
