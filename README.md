# Зима в лесу (Winter in the Forest)

Track 7 of 7 on «Ностальгия» (_Nostalgiya_, “Nostalgia”), the album by Полуживые (_Poluzhivye_), on poems by Arseny Tarkovsky.

On the site: https://vovazakharov.com/music/winter-in-the-forest

## Files

- `winter-in-the-forest_mix.mp3` — the mix, unmastered, as a 320 kbps mp3; the lossless WAV the master was made from is [`nostalgia-07-winter-in-the-forest.wav`](https://github.com/vzakharov/vovazakharov.com/releases/download/music-sources/nostalgia-07-winter-in-the-forest.wav).
- `winter-in-the-forest.flac` — the master, 24-bit.
- `winter-in-the-forest.master.mp3` — its 320 kbps mp3 copy.
- `mastering/` — the script that made the master: `master.py`, the `spectrum.py` it imports, and their `requirements.txt`.

## How it was mastered

```sh
pip install -r mastering/requirements.txt
curl -LO https://github.com/vzakharov/vovazakharov.com/releases/download/music-sources/nostalgia-07-winter-in-the-forest.wav
python mastering/master.py nostalgia-07-winter-in-the-forest.wav ref.flac winter-in-the-forest.flac
```

with `ffmpeg` on `PATH` and the reference below saved as `ref.flac`. Half
strength (`master.py`'s default): Matchering matches the mix to the reference,
half of the EQ difference goes onto the mix, and a limiter keeps the decoded
file under -1 dBTP. `master.py`'s docstring has the whole chain.

## The reference

«Назови меня по имени» (_Nazovi menya po imeni_, “Call Me by Name”), Грёбаный бал, at [vovas-music/nazovi@e53ea7a](https://github.com/vovas-music/nazovi/blob/e53ea7a86eb4a83730778954fb68ef88145a96af/Gryobany%20bal%20-%20Nazovi%20menya%20po%20imeni.flac) — raw download:
https://raw.githubusercontent.com/vovas-music/nazovi/e53ea7a86eb4a83730778954fb68ef88145a96af/Gryobany%20bal%20-%20Nazovi%20menya%20po%20imeni.flac

It was picked blind: three catalogue masters each mastered the mix, and the
operator ranked them unlabelled, loudness-matched, before learning which was
which. It is linked rather than copied here, since it already lives in this
organization.
