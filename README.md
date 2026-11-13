# Bomber Run

Created from [gameskeleton](https://github.com/comprofix/gameskeleton) v0.5.1.

A 1943bj-inspired arcade shooter with faithful combat, enemy movement, scoring, weapons, power-ups, and life-bar mechanics, expanded with original worlds, themes, and bosses.

## Download

Builds for Windows and Linux (64-bit) are on the
[Releases](https://github.com/comprofix/bomberrun/releases) page, with `SHA256SUMS.txt` to check
them against.

- **Windows:** unzip `bomberrun-vX.Y.Z-windows-amd64.zip` and run `bomberrun.exe`.
- **Linux:** extract `bomberrun-vX.Y.Z-linux-amd64.tar.gz` and run `./bomberrun`.
  It needs OpenGL, X11 and ALSA, which desktop systems already have.

## Requirements

- Go 1.27 or later
- **Linux only:** cgo plus the X11/GL/ALSA development packages:
  `libgl1-mesa-dev libxcursor-dev libxi-dev libxinerama-dev libxrandr-dev libxxf86vm-dev libasound2-dev pkg-config`

## Build and run

```sh
go run ./cmd/bomberrun                 # run the game
go run -tags debug ./cmd/bomberrun     # with the debug overlay
go generate ./assets               # rebuild sprite sheets
go vet ./...
go test ./...
go build -o bin/ ./cmd/bomberrun
```

## Personal documents

`DESIGN.md` and `PLAN.md` are personal working documents. `.gitignore` keeps
them out of git, so back them up somewhere else. `AGENTS.md` is tracked and contains the shared project guidance. `CLAUDE.md` is a compatibility hand-off for Claude Code. Keep personal instructions in the local, untracked configuration supported by your coding agent.

## License

MIT. See [LICENSE](LICENSE).
