
# Hex2WavJS

Javascript library for interacting with [TinyAudioBoot](https://github.com/ATtinyTeenageRiot/TinyAudioBoot/) and [8BitMixtapeNEO](https://github.com/8BitMixtape/8Bit-Mixtape-NEO)
# Usage


## Program Chip

```
var hex2wav = new Hex2wav();
var decoded_hex_array = hex2wav.decodeHexFile(hex_string);
var signal = hex2wav.generateProgrammingSignal(decoded_hex_array);
hex2wav.playSignal(hex2wav.audioCtx, signal);
```

## Send control signal

```
var hex2wav = new Hex2wav();
var sig = hex2wav.generateControlSignal(arr);
hex2wav.playSignal(hex2wav.audioCtx, sig);
```

## Set EEPROM

```
var arr = [85]; // max length 64
var hex2wav = new Hex2wav();
var sig = hex2wav.generateEEPROMSignal(arr);
hex2wav.playSignal(hex2wav.audioCtx, sig);
```

# Credit

* [Budi Prakosa](http://manticore.id) - Port of Chris code to JS
* [ChrisMicro](https://github.com/ChrisMicro) - Original Hex2Wav Java code
* [Frederik Olofsson](http://www.fredrikolofsson.com) - Hex file decoder code