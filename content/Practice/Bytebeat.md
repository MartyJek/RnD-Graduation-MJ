**Links**: [[Discovering novel computer music techniques by exploring the space of short computer programs]]

---

> Bytebeat is music generated from short programs. Specifically, these programs generate PCM audio as a function of time.

> a bytebeat program is a piece of code, which when put in a loop that increments a value `t`, generates a piece of music.

The visual equivalent of Bytebeat is sometimes called [[Bit art]].

---

## How is audio represented on computers?

As a list of numbers, just like everything else. The most common way of representing a waveform on a computer is called Linear Pulse Code Modulation, where the list of numbers are called samples and they represent discrete amplitude levels. The samples are spaced evenly in time.

The most common audio sampling encoding is signed integer 16-bit 44.1kHz, meaning that each sample lasts 1/44100 seconds (about 22 microseconds), and is an integer between -32768 and 32767. Larger bitdepths are typically represented with samples as floats between -1 and 1, allowing the signal to be described independently of the quantization step. The size of the quantization step is `0.5**(n-1)` where n is the bitdepth (0.000030517578125 for 16-bit).

The typical encoding used in bytebeat is unsigned integer 8-bit 8kHz, i.e. each sample is a value between 0 and 255, and is played for 1/8000th of a second (125 microseconds). This encoding is used because it is the default encoding used by aout on Linux, as it was the standard encoding when PCM sound cards first came to market.

---

**Source**: https://stellartux.github.io/websynth/guide.html#what
