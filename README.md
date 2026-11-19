# Bomber Run

Created from [gameskeleton](https://github.com/comprofix/gameskeleton) v0.5.1.

An original, clean-slate arcade shooter. It is informed by independent research into classic arcade shooters and shaped by owner-approved design decisions; it is not a recreation of any existing game. Version 1 is planned as five World War II levels (Ocean, River / Jungle, Desert, City and Military Base). The design is still being consolidated and no gameplay has been implemented yet.

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

## Private working documents

`DESIGN.md`, `PLAN.md`, `AGENTS.md` and `CLAUDE.md` are private working
documents and are not part of this repository. In a working copy they are
untracked symbolic links to canonical files kept in a separate private notes
repository, and `.gitignore` keeps them out of Git. Keep personal agent
instructions in the local, untracked configuration supported by your coding
agent (for example `CLAUDE.local.md`).

## License

MIT. See [LICENSE](LICENSE).
