# Eraser Ray Racers

A co-op space race for one to six pilots. You fly a little green alien saucer up through space. Its Eraser Ray cannon, slung under the hull, rubs out anything it touches: space debris, raider ships and the odd rainbow farting monkey. Work together to get as far as you can. The pilot who flies farthest wins.

**Play:** https://jasonninja15.github.io/eraser-ray-racers/

## What's out there

- **Space debris.** Rocks, scrap metal and dead satellites fall from the top of the screen. Erase them or dodge them. Flying into them hurts. Debris falls faster the farther you go, up to almost twice its starting speed at 6,000 m.
- **Raider ships.** Darts, gunboats and big dreadnoughts fly in from above, park overhead and shoot at the nearest pilot until they're erased. Their health scales with the number of pilots in the room, so a full room of six faces raiders six times as tough.
- **Mini ships (after 1,000 m).** Tiny, fast raiders that swarm in groups of two or three. They drop nothing, except that while a Mothership is on screen they drop a repair kit 25% of the time.
- **Space cat (after 1,300 m).** A cat in a little saucer drifts across the screen. Every volley of its Multi Cannon fires a fast blue laser at every pilot and every raider on screen. The lasers pierce, going straight through everything in their path.
- **Raider Mothership (after 2,000 m).** A boss. It flies in from the top, parks there and doesn't move. It charges its own ray cannon, which can aim in any direction, including above itself. A flickering red aim line follows you while it charges, then freezes into a solid flashing line for the last half second before it fires, so you have a moment to get out of the way. The ray then sweeps slowly after the nearest pilot. It also launches mini ships from its hangar bays. While it's on screen, debris and other raiders show up far less often. Its health bar sits under the distance readout. After one is erased, the next arrives 1,500 to 2,200 m later.
- **Rainbow farting monkeys.** Every so often a monkey in a space helmet zooms from one side of the screen to the other, bobbing up and down on a rainbow trail. Touching one takes half your hull.

The race speeds up the farther you go, and more raiders show up at once.

## Pickups

An enemy drops at most one item.

- **Repair kit:** fixes 25 hull.
- **Double Cannon:** a second Eraser Ray cannon for the next 400 m.
- **Mega Ray:** a wider beam that does double damage, for the next 400 m.
- **Ray Pierce:** your ray goes through one more thing, for the rest of the race. Pierce stacks.

Darts, gunboats and dreadnoughts drop a Double Cannon or Mega Ray 2% of the time at the start. That chance goes up by 2% every 500 m, to a maximum of 10%. A Mothership drops Ray Pierce 30% of the time, a Double Cannon or Mega Ray 30% of the time, and otherwise a repair kit. Mini ships drop only repair kits, and only while a Mothership is up.

The title screen lists only the enemies and pickups you have run into so far. It remembers them in your browser.

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
