# Headroom Piano

Yamaha C3 Grand Piano.
Made by [Bengt Nilsson] originally for Kontakt NKI format:

- Two mic positions
- 5 velocity layers
- 300 samples
- Wav size 875 MB, converted to flac 156 MB

Mapped by kinwie using sfz format v2 with ARIA extensions,
with the author's permission as long keeping the original instrument name.

Audio demo : https://sfzinstruments.github.io/pianos/headroom_piano


## Compatibility Notes

This SFZ Instrument is reconstructed with the heavily use of SFZ specification level 2.0 + ARIA Extensions. With this is mind, this instrument will only played properly in Plogue sforzando and similar sfz samplers that used ARIA Engine. Trying to play this instrument in other than ARIA-based sfz samplers may cause issues and problems if it doesn't support the opcodes superset used in this sfz instrument. If ARIA-based sfz sampler is not your choice, we advised you to choose a sfz sampler that has similar level of opcodes support for this instrument can be played and sounded as it should.


## Control Details

Sforzando's generic controls values :
- 0% -to- 100%
- Center value is 50% (set-to-default by Ctrl-click)

Two microphones layers : Close Mic and Decca Tree.
Each has dedicated volume, pan and width controls.

- Volume center is 50%. Turn it up to 100% add up to +6 dB
- Pan center is 50%. Lower value go Left and higher value go Right
- Width normal is 50%. Higher value go wider. 0% is mono

3-band EQ (peak) for each mic.
C is for Close mic.
D is for Decca Tree mic.

- FreqLow range : 20Hz to 400Hz (initial at 20Hz)
- FreqMid range : 200Hz to 4kHz (initial at 1.5kHz)
- FreqHi range : 2kHz to 20kHz (initial at 12kHz)
- Gain range : -/+ 12 dB (initial at 0 dB)
- Bandwidth range : 0 to 4 octaves (initial at 3 oct)

High Damper mode, added for high notes damper on/off option which is not available in the original Kontakt version.
It uses CC67, so you can use sforzando's Left Pedal to switch between the 2 modes : Undampened and Dampened.
- 0% : Undampened (as initial sfz load)
- 1% or greater : Dampened (by pressing the Left Pedal)

Release range, up to 2 secs, initial at 0.8s.

Veltrack is volume to velocity tracking. Lowering the value will cause the lower velocity notes louder.


## Improvements and Features

- This piano has the note-selfmasking sfz native feature and polyphony optimized. This means, when playing a lot of notes (e.g. repetitive, trills or sustain pedal down), the voices count will be handled effectively and lower, which also means less jumping in CPU usage and results in more natural piano sound behavior.

- Turning off either mic volume, Close Vol or Decca Vol at 0% will also disabling that mic layer and reduce polyphony by half.


## Usage Tips

- Setting Veltrack value to achieve a pleasant dynamic range that suit you also depend on your playing style and your keyboard/MIDI controller touch response. Try increase and decrease this "Veltrack" parameter as you play and feel the suitable one for you. To change the default value permanently, find this line in the sfz file : `set_hdcc$VELTRACK=1` and change the value to the one that you wanted, range from 0 to 1.

- MIDI CC numbers are assigned at the top of the sfz file with the #define macro. They can be quick and easily changed to your personal favor or to match your MIDI controller device setup. After loading the instrument in sforzando, click the "Open In Text Editor" blue button at the INFO page, the sfz file will open by your default text editor. You will see a list of parameter's defined numbers. Change the number to your preference and then save it (e.g. Ctrl+S in WinOS), the CC numbers are updated to new ones. This is a handy feature in sfz and is a bit similar to MIDI Learn function.

- The velocity ranges can be directly adjusted also using "Open In Text Editor" button to match your taste or keyboard response. 5 velocity layers : `#define $LOVELx` /  `#define $HIVELx`.

- Velocity layers' volume (in dB) can be re-adjusted at these lines : `#define $VOL_VELx`

- Intimate Piano is the child preset that use only the lowest velocity layer without EQ feature.

- No effect version added for both sfz presets, without width and equalizers, which have advantage of low CPU usage.

- If you are an advanced user and well understand this SFZ format, you can also modify anything in this sfz instrument to your personal taste, make new presets and settings that suit to your private need. SFZ is an easy-to-learn format and very editable. However, if you use this sfz as your basis to create a new one and want to distribute it, we just ask to explicitly put a note that it's derived from this sfz instrument in this github repository.


## Update Log

- Jan 2, 2022 : Rename control, Damper to Hi-Damp for less confusion.

- Nov 28, 2020 : Remove unnecessary master width for reducing CPU load and sticked an unused CC to maintain CC order.

- Sep 16, 2020 : Polyphony optimization by reducing high dampened notes release time from 20 to 10 seconds.

- Aug 17, 2020 : Add No Effect version


## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
<img alt="Creative Commons License" style="border-width:0"
src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />
This work is licensed under a <a rel="license"
href="http://creativecommons.org/licenses/by/4.0/">
Creative Commons Attribution 4.0 International License</a>.

[Bengt Nilsson]: http://www.bengtnilsson.com/samplelibraries.html
