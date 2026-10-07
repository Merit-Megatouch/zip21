# ZIP21 (zip21)

Status: runs on the reconstructed legacy engine (batch smoke test 2026-10-07: renders, takes touches). Hand play-test pending.

## Checklist
- [ ] Window size in game.conf matches the largest PNG (notes/scaffold.md)
- [ ] Every symbol in notes/unresolved.txt has a stand-in in src/host/loader_services.cpp
      (`make analyze GAME=zip21` until it reports 0)
- [ ] First run: `make run GAME=zip21 DEBUG=shots` — crash trace + screenshots in notes/shots
- [ ] Paths: `make run GAME=zip21 DEBUG=files`; engine trace: `mkdir -p data/var/merit/debug/files && touch data/var/merit/debug/files/resource_locator`
- [ ] Reference code: `make decompile GAME=zip21`
- [ ] Translations + help text appear (gamedata/translations/zip21.utf8)
- [ ] Sound and music play (`DEBUG=sound`)
- [ ] A full game plays through (`DEBUG=profile` to catch stalls and old-malloc bugs)

## Log
<!-- dated notes: what broke, what fixed it -->

- 2026-10-07 — runs on src/legacy (sprite engine, gendef records, Allegro subset); smoke-tested headless.
