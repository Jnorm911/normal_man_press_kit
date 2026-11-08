# Pawn'd Chess Launch Trailer and Controller GIF

Working plan for the post-launch promo video and the controller GIF. Facts checked against the live Steam page on Nov 8, 2026.

## Deliverables

| Asset | Length | Use |
| --- | --- | --- |
| Launch trailer | 60–75 s | Steam (first trailer slot), press page, YouTube |
| Social cut (optional) | 20–30 s | Reddit, X, Bluesky, Discord. Same shots, one per pillar |
| Controller GIF | ~9.5 s loop | Press page, Steam "About" section, outreach emails |

The controller GIF is done: `assets/pawnd_chess/pawnd_controller_play.gif` (720×514, 546 KB). A matching MP4 loop is in `assets/pawnd_chess/pawnd_controller_play.mp4` (134 KB). Use the MP4 wherever video is allowed (Reddit, X, Discord). It's sharper and smaller.

## How Steam uses the trailer

These are from the Steamworks trailer docs unless marked otherwise.

- **Specs:** 1920×1080, 30 or 60 fps, 5,000+ kbps, H.264 + AAC, 44.1 or 48 kHz audio, .mp4 or .mov. No official length limit.
- **The first trailer feeds the microtrailer.** Steam cuts six random 1-second clips from your first trailer to make the looping preview shown in search results and on capsules. You can't pick them. So every second must look like the game: no black frames, no long logo cards, no slow fades.
- **Viewers may watch with no sound.** Valve says the trailer should work without audio. Community guides say the first trailer autoplays muted. All the selling has to be in on-screen text.
- **The first trailer should be mostly gameplay** (Valve's recommendation), with the in-game HUD visible.
- **Length:** 60–90 seconds is community advice, not a Steam rule. Aim for about 70.
- **Player size:** the store player is small, roughly 600 px wide. Text and the controller overlay must read at that size.

The store page already has "Pawn'd Chess - Gameplay Trailer". When the new one is ready, set it as the first trailer in Edit Store Page so it drives the microtrailer.

## Problems with the current footage

I reviewed the six clips in `~/Movies` (2026-11-03, 15:33 to 15:47).

1. **The title screen clip is from the demo.** `15-43-56.mov` shows "Next Fest Demo v0.9.5 · Build 26279769" and a **Wishlist** button. A launch trailer can't show either. The controller overlay also covers the menu buttons. **Re-record it on the release build** with the overlay moved off the menu.
2. **The other clips were probably recorded on the demo too** (same day, a day before launch). Before you edit, check that the gameplay screens match the release build.
3. **There's no Steam Deck footage**, and Steam Deck is one of the five pillars. See the reshoot list.
4. **The macOS window bar is visible** ("Pawn'd Chess" title bar and a black border). Record fullscreen, or crop in the editor.
5. **The controller overlay is small** (about 15% of frame width). At Steam's player size it becomes a thumbnail. For the controller shots, zoom in so the overlay and board fill the frame (see the editing notes).
6. **`15-46-50.mov` has no controller overlay**, and there may be a mouse cursor in frame. That's fine for the accessibility section, but hide the cursor in reshoots.
7. **Recording bitrate is very low** (about 350 kbps video). Flat pixel art survives it, but fades and theme changes will smear. For reshoots, set OBS to CQP/CRF 16–18, or 12,000+ kbps.
8. **Missing shots:** difficulty/Elo picker, position editor, FEN import/copy, favorites, local hotseat.

## Reshoot list

All on the release build, fullscreen, controller overlay on, cursor hidden, 1080p60.

| # | Shot | Length to capture | Notes |
| --- | --- | --- | --- |
| R1 | Steam Deck in hands, playing (filmed with a phone) | 10–15 s | Most convincing proof of "Deck first". Landscape, steady, soft light, no glare on the screen. Show thumbs on the D-pad or stick and a move landing. If you can't film it, use the device mockup (see "Steam Deck imagery"). |
| R2 | Steam Deck screen recording | 15–20 s | Steam's built-in Game Recording on the Deck (Settings → Game Recording), then export the clip. The Deck is 1280×800 (16:10): crop it to 16:9 in the editor, or use it inside a framed shot. |
| R3 | Opponent and difficulty picker | 8–10 s | Scroll from 600 to 2600 Elo with the controller, then start a game. |
| R4 | Position editor | 8–10 s | Place a few pieces with the controller and set up a recognizable puzzle. |
| R5 | FEN import or copy | 5–6 s | Paste a FEN; the board snaps to the position. |
| R6 | Favorites | 4–5 s | Save the position, then reopen it from Favorites. |
| R7 | Local hotseat (optional) | 5–6 s | Two players, one device. |
| R8 | Title screen, release build | 6–8 s | No demo text, no Wishlist button. Used for the end card. |

## Steam Deck imagery

On screen, the game looks the same on Deck and PC, so the Deck has to be visible as hardware. Options, best first:

1. **Your own Deck, photographed or filmed running the game.** Free, authentic, no license questions.
2. **Mockup: a free photo of a Deck with a real Deck capture dropped onto the screen.** Done, in `assets/pawnd_chess/`:
   - `pawnd_steam_deck_mockup.jpg` (1920×1080): trailer frame. The empty bottom-left corner can hold a title.
   - `pawnd_steam_deck_mockup_logo.jpg`: the same frame with the Pawn'd Chess wordmark top right.
   - `pawnd_steam_deck_mockup_square.jpg` (2000×2000): social posts.

   Photo: [Steam Deck handheld gaming computer on black surface](https://www.pexels.com/photo/steam-deck-2-handheld-gaming-computer-on-black-surface-14005916/) by Alex Andrews on Pexels. The Pexels license allows commercial use and edits with no attribution required; a credit is still polite. Don't use it in a way that implies Valve endorses the game. The screen shows `steam-deck-gameplay.png`, the real 1280×800 Deck capture from the site, warped to the screen's angle with the photo's glass reflection kept on top. For a purple board to match the trailer, take a new Deck screenshot (Steam + R1) and rebuild it. Screen corners in the photo at 3000×3000: TL 1074,790 · TR 2182,1310 · BR 1852,1932 · BL 722,1395 (glass edge; the image is inset 5.5%).

   I couldn't find a free photo of a Deck held in hands; Adobe Stock has paid ones.
3. **Valve's official Steam Deck social templates** (PSD, 25 MB, from the Steamworks [templates page](https://partner.steamgames.com/doc/steamhardware/steamdeck/templates)): "Your Game is on Deck" banners with the Steam Deck logo, in light, dark and custom colors. They're banners, not device mockups. They need Photoshop or Photopea and the Motiva Sans font. Valve says to **hide the Verified layers** if the game isn't Verified, and Pawn'd's rating is still pending.

Where they go: the trailer (Deck section and end card), the press kit, social posts and the Steam "About" section. Keep mockups out of the Steam screenshot gallery; Valve wants those to be gameplay.

## Wording

Don't say "AI". Avoid the word "engine" too. Chess players hear "engine" as Stockfish-style analysis (evaluation bar, best-move lines), and the Steam page doesn't list that. Promising it invites reviews saying "no engine analysis".

What "plug and play engine" really means here: everything that usually takes a chess GUI plus downloads plus setup is already in the game. So sell **no setup**, not "engine".

| Pillar | Headline (on screen) | Supporting captions |
| --- | --- | --- |
| Controller first | **Chess, built for your controller.** | Every menu, every move, on the pad |
| Steam Deck first | **Pick up and play on Steam Deck.** | — |
| Human-like CPU | **Opponents that play like people.** | 600 to 2600 Elo · Powered by Maia |
| Chess tools | **Serious chess tools. Zero setup.** | Position editor · FEN import & copy · Undo, redo, favorites |
| Accessibility | **Make yourself comfortable.** | Bigger text · High-contrast & monochrome boards · Narration |
| End card | **Pawn'd Chess — Out now on Steam** | Windows · macOS · Linux · Steam Deck |

Alternatives for the tools line, if "Serious chess tools. Zero setup." doesn't land:
- "Study tools built in. Nothing to install."
- "Set up any position. Import any FEN."
- "Everything you'd download a chess app for, already here."

Claims to keep out of the video for now:
- **"Steam Deck Verified"**: the Deck rating is still pending. "Pick up and play on Steam Deck" says what you can show without claiming the badge.
- **"Playable without vision"**: Steam lists it, but it's still untested (Tier 4 from the press kit audit).
- **"Review Game" / analysis**: the button exists on the game-over screen, but the Steam page doesn't describe it. Leave it out until the copy is settled.
- **"Powered by Maia"** is fine. It's already on the Steam page, and chess players know Maia as the human-like model, which helps credibility. It doesn't use the word AI.

## Shot list (about 70 s)

Times in the source clips are approximate (±3 s); scrub to the exact frame. Clip names are the files in `~/Movies`.

| Time | Shot | Source | On-screen text |
| --- | --- | --- | --- |
| 0:00–0:04 | Controller presses → pawn to d4 (zoomed in on overlay + board) | `15-33-07` 4–8 s | **Chess, built for your controller.** |
| 0:04–0:09 | Deck in hands, a move lands | R1 | **Pick up and play on Steam Deck.** |
| 0:09–0:12 | Deck screen, quick move | R2 | — |
| 0:12–0:15 | Knight to f3, legal-move dots showing | `15-33-07` 10–14 s | — |
| 0:15–0:19 | "Maia is thinking…" then the reply lands | `15-35-13` 14–20 s | **Opponents that play like people.** |
| 0:19–0:23 | Elo picker scrolling 600 → 2600 | R3 | 600 to 2600 Elo |
| 0:23–0:27 | Check, king square flashes red | `15-35-13` 25–29 s | Powered by Maia |
| 0:27–0:31 | Position editor, pieces placed | R4 | **Serious chess tools. Zero setup.** |
| 0:31–0:34 | FEN pasted, board snaps | R5 | FEN import & copy |
| 0:34–0:38 | Undo, then load saved position | `15-35-13` 36–44 s + R6 | Undo, redo, favorites |
| 0:38–0:43 | Settings: UI scale to XL + Atkinson Hyperlegible font | `15-46-50` 20–28 s | **Make yourself comfortable.** |
| 0:43–0:48 | Big-text light theme board | `15-46-50` 28–34 s | Bigger text |
| 0:48–0:53 | Color alternatives → monochrome board with hatched highlights | `15-42-44` 13–22 s | High-contrast & monochrome boards |
| 0:53–0:57 | Narration settings | `15-42-44` 14–17 s or `15-46-50` 16–19 s | Narration |
| 0:57–1:02 | Hotseat (optional) or one more strong move | R7 / `15-37-24` 48–53 s | Local hotseat on one device |
| 1:02–1:08 | Title screen, release build | R8 | **Pawn'd Chess — Out now on Steam** · Windows · macOS · Linux · Steam Deck |

Shot length: 2–5 s each. Cut on a move landing or a menu selection. Never hold a static board longer than about 4 s.

The social cut (20–30 s) uses the first shot of each pillar plus the end card.

## Text style

- **Font:** Atkinson Hyperlegible (free from Google Fonts or the Braille Institute; install it and iMovie can use it). It's an option in the game and it backs up the accessibility message. Use Bold for headlines and Regular for captions.
- **Size:** headlines about 80–90 px tall at 1080p, captions about 54–60 px. Anything smaller won't read in Steam's player.
- **Word count:** at most 6 words per card. Keep each card on screen for at least 2 s; roughly 1 s plus 1 s for every 3 words.
- **Placement:** over the dark left panel or a top band. Never over the board or the controller overlay.
- **Color:** white text with a soft dark shadow. Use one accent color sampled from the board purple (macOS Digital Color Meter) for the end-card line or an underline. Same position and style for every card.
- **Motion:** quick fade or cut in, no spinning or typewriter effects. The footage is the show.
- **Music:** upbeat, royalty-free, cut on the beat. The video must still make sense muted.

## Editing in iMovie

iMovie is fine for this. If you want more control over titles and zooms later, DaVinci Resolve is free.

1. **File → New Movie**, then import the clips (drag from `~/Movies`). The first clip you add sets the frame rate; start with a 60 fps clip.
2. **Trim:** drag the clip edges in the timeline, or select a range in the browser and press E to add just that range.
3. **Zoom in on controller shots:** select the clip → Crop button above the viewer → **Crop to Fill**, then drag the frame around the controller overlay and board. The same tool removes the macOS title bar. Use Ken Burns only for a slow push-in.
4. **Titles:** Titles tab → pick a plain one ("Standard Lower Third" or "Centered") → drag it above the clip → set the font, size and color in the viewer. Make one, then copy and paste it so every card matches.
5. **Steam Deck clips (16:10):** crop to fill 16:9, or put them over a dark background with Picture in Picture.
6. **Music:** drag the track under the clips; iMovie can lower music under other audio automatically.
7. **Export:** File → Share → File → Resolution **1080p**, Quality **High**, Compress **Better Quality** → .mov or .mp4 (H.264). This lands well above Steam's 5,000 kbps minimum. Check the exported file plays muted and still makes sense.

## The controller GIF

Made from `15-33-07.mov`, 4.0 to 13.5 s: the cursor moves along the pawns, D-pad presses light up on the overlay, the d-pawn lifts with legal-move dots, 1.d4 d5, then the knight jumps to f3. Cropped to the overlay plus the board (macOS title bar removed), 15 fps, 192-color palette.

To rebuild it or make another from a different clip or time range (change `-ss` start and `-t` length):

```bash
ffmpeg -ss 4 -t 9.5 -i "$HOME/Movies/2026-11-03 15-33-07.mov" -vf "fps=15,crop=1470:1050:30:30,scale=720:-2:flags=lanczos,split[a][b];[a]palettegen=max_colors=192:stats_mode=full[p];[b][p]paletteuse=dither=none" -loop 0 pawnd-controller-play.gif
```

GIF limits:
- Steam allows animated GIFs in the "About this game" section and publishes no hard size cap. Keep each under about 3 MB so the page stays fast.
- One GIF per About section works well. The Steam page already has four headers ("Chess built for your controller", "Find your next challenge", "Make yourself comfortable", "Try another idea"), so each could get a GIF once the reshoots exist.
- Wherever video is allowed, the MP4 loop looks better than a GIF.
