# Scholar Slash

Scholar Slash is a browser fighting game in which a student clears waves of animated coursework, collects temporary study powers, and faces a final finance boss.

## Submission links

- **Public game:** https://james-regi.github.io/Scholar-V2/
- **Repository/source:** https://github.com/James-Regi/Scholar-V2
- **AI/build log:** [BUILD_LOG.md](BUILD_LOG.md)
- **Unfamiliar-user test:** [USER_TEST.md](USER_TEST.md)

Both public URLs were checked without GitHub authentication on September 1, 2026 and returned HTTP 200.

## Controls

- `A` / `D`: move
- `Space`: attack
- `K`: use a collected special ability
- `C`: use the jetpack and laser during the final boss battle

## Concise demonstration

1. Open the public game in a signed-out/private browser window.
2. Select **Enter The Fight**.
3. Demonstrate movement and a normal Space attack.
4. Defeat a textbook, collect its dropped study power, and use `K`.
5. Explain that three increasingly difficult rounds lead to the final boss, where `C` controls the jetpack laser.
6. Show this repository and briefly point to the build and user-test records.

## Reflection

The main design goal was to turn academic pressure into a compact arcade metaphor with controls that are understandable immediately. Iterative testing exposed problems that visual inspection alone missed: a syntax error prevented entry, misplaced function scope crashed attacks, cached assets hid fixes, negative health values drew bars backward, and Round 3 spawned too quickly. The strongest lesson was to test the deployed URL with real keyboard input and fresh browser state, not only the local source.

## Source files

- `index.html`: interface and game structure
- `style.css`: visual design and responsive layout
- `game.js`: game loop, combat, waves, powers, and rendering
