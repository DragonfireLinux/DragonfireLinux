So what I did where was look at how the Dragonfire client did things, and then re-orangised it all into the latest dev release (5.50-dev) of Minetest with some improvements.

### Enabled Always:
- No Fall Damage
- All Privilages _(fly, noclip, fast mode)_
- No Slip on slippery surfaces.
- Fast Digging _(well as fast as possible)_
- Extended tool range _(can build from far away, etc)_
- Cheat Detection is disabled by default, yes there is a client side cheat detection flag. Lame I know, it's disabled to report no cheating.

### Modes:
- Normal mode
- Fullbright _(no shadows, no night time)_
- Zeus Mode _(xray vision for mining, makes stone 'transparent')_
- Fast Action/Place _(place blocks at record breaking speed)_
 
XRay works the same as in original Dragonfire however there is no longer a superfluous loop, but also now on mode change the update is instant as I force the client to re-render what is in your line of sight.

Modes are changed by pressing the key assigned to Mute, yes that's right I have hijacked the mute hotkey for this implementation.

Generally I consider this a better implementation of the core functionality that the original Dragonfire client offered, with a much less hassle interface which is flicked though in a set of 4 modes using one key.

The original Dragonfire client is available here:
https://github.com/EliasFleckenstein03/dragonfireclient
