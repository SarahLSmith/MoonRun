# MoonRun

A 2D side-scrolling sci-fi arcade game, made with pygame. You play an
astronaut on the moon, avoiding craters and meteorites with a jetpack and
collecting speed and jetpack boosts. The score rises with time survived,
and the game keeps a top-five leaderboard. A two-player mode is included.

Created in 2019 by Remigius Ezeabasili, Jonas Kohl, Sarah Smith and Mohammad
Yazdani as a university team project. Music by Eric Skiff.

## Gameplay

- **Single player:** arrow keys. Survive as long as possible. If you fall
  too far behind the moving world, or move too fast and drop off-screen,
  the game ends.
- **Two players:** the second player uses W, A and S, and the last player
  to survive wins. There's no score in this mode.

## Design notes

- The jump is a linear rise followed by a quadratic fall, to model a
  jetpack rather than a standard jump.
- Obstacles and items are kept in lists and updated each frame, which is
  the standard pygame game-loop pattern.
- The idea was inspired by the Chrome dinosaur game. No code was reused.
  All sprites are original. Sound effects come from the Bitkits VST library,
  except the jetpack sound, which was made from white noise.

## How to run

Requirements: Python 3 and pygame. The original instructions specify
pygame 1.9.6, and this hasn't been checked on newer versions.

```bash
pip install pygame==1.9.6
python moonrun.py
```

Run it from any folder. The script changes to its own folder to find the
assets. `font.ttf` is recommended, though not required.

## Files

```
moonrun.py       game code: classes, game logic and main loop
highscore.hs     saved leaderboard (pickle), created by the game
*.png, *.wav,    sprites, sounds, music and font
*.mp3, font.ttf
README.txt       original setup instructions
DESCRIPTION.txt  original game description and credits
```

## Known gaps

- `highscore.hs` is a pickle file, so it should be treated as trusted
  local data only.
- Pygame 1.9.6 is old. Newer versions haven't been tested.
