# ps-keystones

This repo contains keystone files taken from PS4 and PS5 games.

### What is a keystone?

A keystone file is 96 bytes long, and is generated using publicly known keys along with a passcode chosen under development of the game.
The passcode itself is not directly stored in the file (a hash of it is stored), nor is it feasible to obtain it from the keystone.
More details can be found on the [psdevwiki](https://www.psdevwiki.com/ps4/Keystone).

Usually a game will have different keystone files per title.
For example, if a game has an EU and US release, it is likely that those releases each will have a different keystone.
A simple way to obtain a keystone is to decrypt a save from the game, its relative path is `sce_sys/keystone`.

### Why are keystones useful?

If you have a save from the same game with a different title ID which you want to load,
it is likely that just patching the title ID will not be enough. If the keystone is different it will fail.
Having easy access to the keystones can save the headache when re-regioning a save.

If two games share the same passcode, their keystone will be the same.

### Structure of the repo

Each console has its own folder with subfolders `Set_XX` for digits `XX` each containing a maximum of 2 750 keystones named after the title id (with a `.keystone` extension).

### Keystone sources
* [Batang](https://github.com/B-a-t-a-n-g)
* [Bawsdeep](https://gitlab.com/BawsDeep)
* [bucanero](https://github.com/bucanero): [apollo-patches](https://github.com/bucanero/apollo-patches/tree/main/PS4)
* [garlicsaves](https://garlicsaves.com/tools/sample-saves)
* [ps4keystones](https://github.com/ps4keystones): [ps4keystones.github.io](https://github.com/ps4keystones/ps4keystones.github.io/tree/master/keystones)

If the source depends on arbitrary user input, the most common keystone collected for each title ID should be selected.

