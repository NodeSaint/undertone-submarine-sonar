# UNDERTOW

A submarine sonar game played in total darkness. You're blind, you're outnumbered, and every time you ping to see, the enemy sees you too.

**[Play it now](https://nodesaint.github.io/undertone-submarine-sonar/)**

![Terminal green on black](https://img.shields.io/badge/aesthetic-CRT%20terminal-00ff41)

---

## The Premise

World War III has gone underwater. The Department of War has assigned you to the **USS IRON PHANTOM** — a stealth submarine deployed behind enemy lines. Your only instrument is sonar. Your only objective is survival.

The screen is black. You move through the dark. Hit spacebar to send a sonar ping — ASCII ripples expand outward, briefly revealing cave walls, enemy submarines, and repair kits before everything fades back to nothing. The catch: enemies hear your ping too. Now they know where you are.

## How To Play

| Action | Keyboard | Mobile |
|--------|----------|--------|
| Move | `W` `A` `S` `D` | D-pad |
| Sonar Ping | `Space` | PING button |
| Aim Torpedo | `Q` / `E` | AIM button |
| Fire Torpedo | `F` | FIRE button |

### Things to know

- **Pings are limited.** You get 5, they recharge over time. Use them wisely.
- **Each ping gives you away.** Enemies will turn aggressive and hunt your last known position.
- **Torpedoes have soft homing.** Aim in roughly the right direction and they'll curve toward nearby targets. You get 5, they reload every 3 seconds.
- **Repair kits** are scattered on the map. They show up as cyan `+` symbols when revealed by sonar. Walk over them to patch your hull (+30 HP).
- **Enemies ping too.** At least every 10 seconds, sometimes sooner. Listen and watch for red ripples — that's them giving away their position.
- **Hull carries between waves.** Don't take unnecessary hits. There are no freebies.

### Waves

11 waves. Each one adds another enemy submarine.

| Wave | Enemies | Codename |
|------|---------|----------|
| 1 | 2 | Silent Approach |
| 2 | 3 | First Contact |
| 3 | 4 | Deep Stalkers |
| 4 | 5 | Wolfpack Rising |
| 5 | 6 | Blind Hunt |
| 6 | 7 | Pressure Point |
| 7 | 8 | Kill Box |
| 8 | 9 | Iron Coffin |
| 9 | 10 | The Abyss |
| 10 | 11 | Dead Reckoning |
| 11 | 12 | Total War |

Kill every enemy in a wave. 10 seconds later, the next wave spawns. Survive all 11 and you've ruled the sea.

## What It Feels Like

You're staring at a black screen. You know there are enemies out there but you don't know where. You're low on hull, you've got one ping left, and you haven't seen anything in 15 seconds. Do you ping and risk getting hunted? Or do you keep drifting blind and hope you don't walk into something?

That's the whole game.

## Tech

Single `index.html`. No dependencies, no build step, no framework. Canvas rendering, Web Audio API for all sound (sonar pings, torpedoes, explosions, ambient ocean hum). Procedural cave generation via cellular automata. Works on desktop and mobile, portrait and landscape.

## Run Locally

Open `index.html` in a browser. That's it.

Or:

```
python3 -m http.server 8080
```

Then go to `http://localhost:8080`.
