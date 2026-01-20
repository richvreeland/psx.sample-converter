# 🕹️ psx sample converter

An audio converter that emulates the Sound Processing Unit of the original Sony Playstation.  
SPU implementation based on [PlayStation: The SPU](https://jsgroth.dev/blog/posts/ps1-spu-part-1/) articles by jsgroth, and the [psx-spx](https://psx-spx.consoledev.net/soundprocessingunitspu/) documentation.

## Signal Chain

### Pre Low-Pass
Shape the input spectrum before encoding — define what frequencies enter the chain

### Sample Rate
Decimate to simulate memory-constrained samples. Lower rates = more Gaussian smoothing on playback

### ADPCM Codec
Authentic PS1 SPU compression — 16-bit → 4-bit using shift + filter prediction (always enabled)

### Bit Depth
Additional quantization after ADPCM decode (16-bit = no extra reduction)

### Pitch + Gaussian
Combined pitch = (sample rate ÷ 44100) × pitch ratio, with SPU pitch counter and 512-entry Gaussian weight table
