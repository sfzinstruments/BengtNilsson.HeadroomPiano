# Headroom Piano

Yamaha C3 Grand Piano.
Made by [Bengt Nilsson] originally for Kontakt NKI format:

- Two mic positions
- 5 velocity layers
- 300 samples
- Wav size 875 MB, converted to flac 156 MB

Mapped by kinwie using sfz format v2 with ARIA extensions,
with the author's permission as long keeping the original instrument name.

## Details

Sforzando's generic controls values :
- 0% -to- 100%
- Center value is 50% (set-to-default by Ctrl-click)

Two microphones layers : Close Mic and Decca Tree.
Each has dedicated volume, pan and width controls.

- Volume at 0% will also turn off the mic layer and saving polyphony
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

Damper mode, added for high notes damper on/off option which is not available in the original Kontakt version.
It uses CC67, so you can use sforzando's Left Pedal to switch between the 2 modes : Undampened and Dampened.
- 0% : Undampened (as initial sfz load)
- 1% or greater : Dampened (by pressing the Left Pedal)

Release range, up to 2 secs, initial at 0.8s.

Veltrack is volume to velocity tracking.
Lowering the value will cause the lower velocity notes louder.
You can adjust this for different dynamics, keyboard's pressure or playing style if needed.

Tips:
You can peek the used MIDI CC number by clicking the 'blue box' (Open in Text Editor) in sforzando's Info page because I didn't label the numbers to the Controls page.

Intimate Piano is the child preset that use only the lowest velocity layer without EQ feature

## License

<a rel="license" href="http://creativecommons.org/licenses/by/4.0/">
<img alt="Creative Commons License" style="border-width:0"
src="https://i.creativecommons.org/l/by/4.0/88x31.png" /></a><br />
This work is licensed under a <a rel="license"
href="http://creativecommons.org/licenses/by/4.0/">
Creative Commons Attribution 4.0 International License</a>.

[Bengt Nilsson]: http://www.bengtnilsson.com/samplelibraries.html
