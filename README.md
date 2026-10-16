# Eraser Ray Racers

A co-op space race for one to six pilots. You fly a little green alien saucer up through space. Its Eraser Ray cannon, slung under the hull, rubs out anything it touches: space debris, raider ships and the odd rainbow farting monkey. Work together to get as far as you can. The pilot who flies farthest wins.

**Play:** https://jasonninja15.github.io/eraser-ray-racers/

## What's out there

- **Space debris.** Rocks, scrap metal and dead satellites fall from the top of the screen. Erase them or dodge them. Flying into them hurts.
- **Raider ships.** Darts, gunboats and big dreadnoughts fly in from above, park overhead and shoot at the nearest pilot until they're erased. Their health scales with the number of pilots in the room, so a full room of six faces raiders six times as tough.
- **Rainbow farting monkeys.** Every so often a monkey in a space helmet zooms from one side of the screen to the other, bobbing up and down on a rainbow trail. Don't touch the monkeys.
- **Repair kits.** Erased raiders (and sometimes satellites and big rocks) drop green repair kits. Each one fixes 25 hull.

The race speeds up the farther you go, and more raiders show up at once.

## Controls

| Key | Action |
| --- | --- |
| W A S D / arrow keys | Fly |
| Mouse | Aim the Eraser Ray |
| Click / Space | Hold to fire. Let go before it overheats. |
| Esc | Pause (solo) or menu (multiplayer) |
| M | Sound on or off |

On a touchscreen, your left thumb flies and your right thumb aims and fires.

## Playing together

1. One player presses **Play together** and then **Create room**.
2. Share the five-character room code.
3. Everyone else presses **Play together**, types the code, and presses **Join**.
4. The host presses **Launch**. Players who join later drop straight into the race.

When a pilot is erased, they watch the others until everyone is out. Then the results screen ranks everyone by distance, and the host can start another race.

No account is needed. Players connect browser to browser over WebRTC, using the free public [PeerJS](https://peerjs.com) server to find each other. The host's page runs the debris, raiders and monkeys, so if the host leaves, the room closes. Some strict school or office networks block these connections.

## Install or download

- **Install app:** open the link above in Chrome and press **Install app** on the title screen, or use the install icon in the address bar. It works offline once it has been opened online.
- **Download file:** press **Download file** on the title screen to save `eraser-ray-racers.html`. Open it in any browser to play. Solo play works offline; multiplayer needs an internet connection.

## Files

- `index.html` is the whole game: one file, with every sprite drawn in canvas code.
- `eraser-ray-racers.html` is a copy of `index.html` for the download button. After editing `index.html`, copy it over again.
- `sw.js` is the offline service worker. Bump `CACHE` when the list of core files changes.
