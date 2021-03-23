## So what I did here was look at how the Dragonfire client did things, and then re-organised it all into the latest dev release (5.50-dev) of Minetest with some minor improvements.

### Enabled Always
- No Fall Damage
- All Privileges (fly, noclip, fast mode)
- No Slip on slippery surfaces.
- Fast Digging (well as fast as possible)
- Extended tool range (can build from far away, etc)
- Cheat Detection is disabled by default, yes there is a client-side cheat detection flag. Lame I know, it's disabled to report no cheating.

### Modes
- Normal mode
- Fullbright (no shadows, no night time)
- Zeus Mode (x-ray vision for mining, makes stone 'transparent')
- Fast Action/Place (place blocks at record-breaking speed)

### How to setup

Download Minetest 5.50-Dev from https://github.com/minetest/minetest and copy the source files in this respoitory over the originals in the mintest repo, then compile it. You will now be running the "hax0red" version of Minetest.

Otherwise just search these files for the keyword `!!HAX` and you will find every modified line in each of the files, which you can use to easily re-produce these modifications manually in the new Mintest releases or versions.

It's that simple, all the modifications are pretty basic, if you take a look at them all using that search keyword im sure you can make your own improvements.

I have supplied a pre-compiled linux binary of Mintest 5.50-Dev _(hax0red)_ so if you cba to compile just replace your binary with [this one](https://github.com/DragonfireLinux/DragonfireLinux/raw/main/minetest).

### Notes

XRay works the same as in original Dragonfire however there is no longer a superfluous loop, but also now on mode change the update is instant as I force the client to re-render what is in your line of sight.

Modes are changed by pressing the key assigned to Mute, by default that key is `M`, yes that's right I have hijacked the mute hotkey for this implementation.

Generally, I consider this a better, simplified, implementation of the core functionality that the original Dragonfire client offered, with a much less hassle interface that is flicked through in a set of 4 modes using one key.

**The original Dragonfire client is available here:**
https://github.com/EliasFleckenstein03/dragonfireclient
_(but the author only supplies windows builds and it's based on 5.4 stable)_
