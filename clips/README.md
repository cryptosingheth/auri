# Clips — how the site uses them

All source clips live in `../../Auri Clips/` (12 Veo generations). The site references
the copies in this folder by role. Swap any file (same name) and the site picks it up.

## Hero montage (crossfading playlist, ~4.6s per clip)
| File | Current clip | Story beat |
|---|---|---|
| `hero.mp4` | Gold card tap at café terminal | spend |
| `montage-2.mp4` | Man at sunlit table with card | buy/own |
| `life-1.mp4` | Woman at café counter, latte | daily life |
| `montage-3.mp4` | Woman saving on phone, morning light | save |
| `life-3.mp4` | Couple on sofa, golden gift moment | gift |
| `montage-4.mp4` | Elegant older woman, gold phone | trust |

Playlist order is set in `index.html` (`PLAYLIST` array). 4–6 clips is the sweet spot.

## Section clips
| File | Where |
|---|---|
| `dev.mp4` | "Gold that takes instructions" — background of the terminal panel |
| `life-2.mp4` | (spare — vertical remittance split-screen, currently unused) |

## Posters
`poster-*.webp` are first-frame stills used before videos load (and in the artifact
preview, which can't carry video).

## Making better clips
See **PROMPT-PACK.md** in this folder — paste-ready Google Flow / Veo 3 prompts where
gold visibly IS the money (the founder's brief), plus negative prompts, a montage plan,
and ffmpeg trim/grade/compress commands. Note: current clips carry a small Veo sparkle
watermark bottom-right; final marketing footage should be regenerated or cropped.
