# Files

Files over GitHub's 100 MiB limit are split into 99 MiB `.part` pieces.

## Rejoin

Linux / Git Bash:

```bash
cat xiaomi-work.rar.*.part > xiaomi-work.rar
cat xiaomi-presentation/both-themes-tour.mp4.*.part > xiaomi-presentation/both-themes-tour.mp4
```

Windows cmd:

```bat
copy /b xiaomi-work.rar.00.part+xiaomi-work.rar.01.part+xiaomi-work.rar.02.part+xiaomi-work.rar.03.part+xiaomi-work.rar.04.part xiaomi-work.rar
cd xiaomi-presentation && copy /b both-themes-tour.mp4.00.part+both-themes-tour.mp4.01.part both-themes-tour.mp4
```

## Verify

```bash
sha256sum -c SHA256SUMS.txt
```

| File | Size | Parts |
|---|---|---|
| xiaomi-work.rar | 433 MB | 5 |
| 1117.zip | 47 MB | — |
| cocos-lib.rar | 7.7 MB | — |
| xiaomi-presentation/both-themes-tour.mp4 | 170 MB | 2 |
| xiaomi-presentation/1-captain-cook-tour.mp4 | 86 MB | — |
| xiaomi-presentation/2-bb24-tour.mp4 | 79 MB | — |
| xiaomi-work1/ (6 files) | 79 MB | — |
