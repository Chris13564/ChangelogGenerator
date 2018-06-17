# ChangelogGenerator

Uses [CurseAPI-Minecraft](https://github.com/TheRandomLabs/CurseAPI-Minecraft) to generate changelogs.

It takes two files as input - `old.json` and `new.json`. `old.json` is the `manifest.json` of the
old modpack version, and `new.json` is the `manifest.json` of the new modpack version.

ChangelogGenerator generates two files - `changelog.txt` and `shortchangelog.txt`.
`shortchangelog.txt` only contains URLs to changelogs, while `changelog.txt` incorporates
full changelogs.

If you want to use different files as input, you can do something like this:
	java -jar ChangelogGenerator.jar oldmanifest.json manifest.json

Obviously it isn't perfect, but I tried to add as much mod compatibility as possible
(CoFH's mods, mezz's mods, etc.).

Because there's no official API for retrieving changelogs, there will be crashes when things change.
I usually fix these problems quickly.

At the moment, CurseMeta support is disabled since it's been down for a while.

I still haven't implemented proper command-line argument parsing.

To use this with Gradle:

	compile "com.github.TheRandomLabs:ChangelogGenerator:master-SNAPSHOT"

Example changelogs can be found at changelog.txt and shortchangelog.txt in this repository.

Planned features:
* Better mezz support
* IC2 support
* Proper command-line arguments
