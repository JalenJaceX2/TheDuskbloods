# TheDuskbloods
The Duskbloods setup Guide

Download the latest playDB-CNT launcher

https://github.com/sikoGD/playDB-CNT/releases

Download the latest Lichii emulator

https://github.com/zortos293/Lichii/releases

You don't want to use this version of Lichii for other games (Only use it for Duskbloods)

Windows

    Download another copy of Lichii and extract it where you want
    Create a folder named `user` in the same folder that has your `lichii.exe`
        This will set Lichii to portable mode and keep it separate from any other copies of Lichii you may have
    Add your `prod.keys` and `title.keys` to Lichii
        They go in your new lichii folder `\user\keys\`
    Place `Play Duskbloods.exe` and the `_internal` folder in the same folder as your `lichii.exe`
    Launch `Play Duskbloods.exe`
    `Browse` to your game file
    `Patch Lichii`
    Click `Start game`
    Set Lichii to `Docked` mode


Alternative to `Patch Lichii` or if you're on Linux
```
You have to `Start game` from the Duskbloods launcher once to automatically create a certificate
Exit the game
Manually add these settings:
Settings - System - Network
Redirect host names to a server you run - `On`
Host names
    npln.srv.nintendo.net, npln.nintendo.net, n.n.srv.nintendo.net, p.srv.nintendo.net, fromsoftware-game.net
Server address
    127.0.0.1:18443
CA certificate
    `Browse...` to your ca.der
    Linux `~/.local/share/lichii/duskbloods_test/pki/ca.der`
    Windows - your new lichii folder `\user\duskbloods_test\pki\ca.der`
```


Current issues:
```
Having to `Patch` or manually set host name redirect
    Fixed in PR 1557 - Not sure when or if that will be added
Flickering (not always, but sometimes the fog/sky will have bad flickering)
    Fixed with PR 2306 - Will be included in the next update
`Use the game's own DLSS` does not work and will crash
    Fixed with PRs 1483, 1490, and 1527 - Not sure when or if those will be added
Hub area save bug (might only be present on the Linux PGO build)
    Set timezone to `UTC` to fix
```

Online or Update error workaround

I didn't need it, but a few people have

(Possible your game dump is older than mine)
```
your new lichii folder `\user\duskbloods_test\nand\system\save\bcat\0400D1D02399A000\Regulation\`
Copy `regulation_nt_1_0.bin`
Paste and rename it to `regulation_nt_0_900.bin`
```
