# Play or convert a midi file

Play a midi file to your audio device, render it to a file, or parse the
raw data. Additional settings can be specified, see
[fluidsynth_setting_list](https://docs.ropensci.org/fluidsynth/reference/fluidsynth_settings.md)
for available options.

## Usage

``` r
midi_play(
  midi = demo_midi(),
  soundfont = soundfont_path(),
  audio.driver = NULL,
  settings = list(),
  verbose = interactive()
)

midi_convert(
  midi = demo_midi(),
  soundfont = soundfont_path(),
  output = "output.mp3",
  settings = list(),
  verbose = interactive()
)

midi_read(midi = demo_midi(), verbose = FALSE)

demo_midi()
```

## Arguments

- midi:

  path to the midi file

- soundfont:

  path to the soundfont

- audio.driver:

  which audio driver to use, see [fluidsynth
  docs](https://www.fluidsynth.org/api/CreatingAudioDriver.html)

- settings:

  a named vector with additional settings from
  [`fluidsynth_setting_list()`](https://docs.ropensci.org/fluidsynth/reference/fluidsynth_settings.md)

- verbose:

  print some progress status to the terminal

- output:

  filename of the output. The out

## Value

midi_read returns data frame with midi events.

## Details

The `midi_convert` function internally uses fluidsynth to generate a raw
wav file, and then
[`av::av_audio_convert()`](https://docs.ropensci.org/av//reference/encoding.html)
to convert into the requested about format. See
[`av::av_muxers()`](https://docs.ropensci.org/av//reference/formats.html)
for supported output formats and their corresponding file extension.

You need a soundfont to synthesize midi, see the
[soundfonts](https://docs.ropensci.org/fluidsynth/reference/soundfonts.md)
page. On Linux you may also need to specify an `audio.driver` that works
for your hardware, although on recent distributions the defaults
generally work.

## See also

Other fluidsynth:
[`fluidsynth_settings`](https://docs.ropensci.org/fluidsynth/reference/fluidsynth_settings.md),
[`soundfonts`](https://docs.ropensci.org/fluidsynth/reference/soundfonts.md)

## Examples

``` r
df <- midi_read(demo_midi())
```
