# Managing soundfonts

FluidSynth requires a soundfont to synthesize a midi. On Linux
distributions some soundfonts are often preinstalled, though their
quality varies. If your midi sounds very poor, try using another
soundfont.

## Usage

``` r
soundfont_path(download = FALSE)

soundfont_download()
```

## Arguments

- download:

  automatically download soundfont if none exists.

## Value

the path to a local soundfont to synthesize a midi file.

## Details

[GeneralUser-GS](https://schristiancollins.com/generaluser) by S.
Christian Collins is a nice free soundfont. You can use
`soundfont_download()` to install a copy of this soundbank for use by
this package.

## See also

Other fluidsynth:
[`fluidsynth_settings`](https://docs.ropensci.org/fluidsynth/reference/fluidsynth_settings.md),
[`midi_play()`](https://docs.ropensci.org/fluidsynth/reference/fluidsynth.md)
