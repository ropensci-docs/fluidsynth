# Fluidsynth settings

Get available settings and their types. See [fluidsynth
docs](https://www.fluidsynth.org/api/fluidsettings.html) for more
information on the available options.

## Usage

``` r
fluidsynth_setting_list()

fluidsynth_setting_options(setting)

fluidsynth_setting_default(setting)

libfluidsynth_version()
```

## Arguments

- setting:

  string with one of the options listed in `fluidsynth_setting_list()`,
  see examples.

## Value

a list with available options

## References

[FluidSynth Settings
Reference](https://www.fluidsynth.org/api/fluidsettings.html)

## See also

Other fluidsynth:
[`midi_play()`](https://docs.ropensci.org/fluidsynth/reference/fluidsynth.md),
[`soundfonts`](https://docs.ropensci.org/fluidsynth/reference/soundfonts.md)

## Examples

``` r
# List available settings:
fluidsynth_setting_list()
#>                                 name    type
#> 1                  audio.alsa.device  string
#> 2                       audio.driver  string
#> 3                  audio.file.endian  string
#> 4                  audio.file.format  string
#> 5                    audio.file.name  string
#> 6                    audio.file.type  string
#> 7             audio.jack.autoconnect integer
#> 8                      audio.jack.id  string
#> 9                   audio.jack.multi integer
#> 10                 audio.jack.server  string
#> 11                  audio.oss.device  string
#> 12                 audio.period-size integer
#> 13                     audio.periods integer
#> 14     audio.pipewire.media-category  string
#> 15         audio.pipewire.media-role  string
#> 16         audio.pipewire.media-type  string
#> 17   audio.pulseaudio.adjust-latency integer
#> 18           audio.pulseaudio.device  string
#> 19       audio.pulseaudio.media-role  string
#> 20           audio.pulseaudio.server  string
#> 21               audio.realtime-prio integer
#> 22               audio.sample-format  string
#> 23                 audio.sdl2.device  string
#> 24                  midi.alsa.device  string
#> 25              midi.alsa_seq.device  string
#> 26                  midi.alsa_seq.id  string
#> 27                  midi.autoconnect integer
#> 28                       midi.driver  string
#> 29                      midi.jack.id  string
#> 30                  midi.jack.server  string
#> 31                   midi.oss.device  string
#> 32                     midi.portname  string
#> 33                midi.realtime-prio integer
#> 34                player.reset-synth integer
#> 35              player.timing-source  string
#> 36                        shell.port integer
#> 37                      shell.prompt  string
#> 38              synth.audio-channels integer
#> 39                synth.audio-groups integer
#> 40               synth.chorus.active integer
#> 41                synth.chorus.depth  double
#> 42                synth.chorus.level  double
#> 43                   synth.chorus.nr integer
#> 44                synth.chorus.speed  double
#> 45                   synth.cpu-cores integer
#> 46           synth.default-soundfont  string
#> 47                   synth.device-id integer
#> 48      synth.dynamic-sample-loading integer
#> 49            synth.effects-channels integer
#> 50              synth.effects-groups integer
#> 51                        synth.gain  double
#> 52               synth.ladspa.active integer
#> 53                 synth.lock-memory integer
#> 54            synth.midi-bank-select  string
#> 55               synth.midi-channels integer
#> 56             synth.min-note-length integer
#> 57                synth.overflow.age  double
#> 58          synth.overflow.important  double
#> 59 synth.overflow.important-channels  string
#> 60         synth.overflow.percussion  double
#> 61           synth.overflow.released  double
#> 62          synth.overflow.sustained  double
#> 63             synth.overflow.volume  double
#> 64                   synth.polyphony integer
#> 65               synth.reverb.active integer
#> 66                 synth.reverb.damp  double
#> 67                synth.reverb.level  double
#> 68            synth.reverb.room-size  double
#> 69                synth.reverb.width  double
#> 70                 synth.sample-rate  double
#> 71              synth.threadsafe-api integer
#> 72                     synth.verbose integer
fluidsynth_setting_options('audio.driver')
#> [1] "alsa"       "file"       "jack"       "oss"        "pipewire"  
#> [6] "pulseaudio" "sdl2"      
fluidsynth_setting_default('synth.sample-rate')
#> [1] 44100
```
