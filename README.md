# Stegofile-Concealer

Hide text or files inside PNG images or WAV audio using LSB steganography, with a Magic PIN and optional AES-256 encryption - instantly, privately, for free.

Everything runs locally in your browser via the Web Crypto API and Canvas/ArrayBuffer processing. No upload, no server, no tracking, no ads, no dependencies. Works fully offline once loaded.

## Usage

Download [`stegofile-concealer.html`](./stegofile-concealer.html) and open it in any modern browser. That's it - no install, no build step, no internet connection required.

## How it works

- **Magic PIN** - any string you choose (auto-uppercased), used as a marker so nobody can confirm hidden data exists without knowing it (plausible deniability)
- **Password (optional)** - adds AES-256-GCM encryption on top of the PIN
- **Carriers** - PNG images (lossless) or WAV audio (uncompressed PCM) - both required because lossy formats (JPEG, MP3) destroy the hidden bits
- **Capacity** - depends on carrier size; shown live in the UI before hiding

## Security model

```
PIN  = "Does anything exist here?" (plausible deniability)
PWD  = "What does it say?"         (AES-256-GCM encryption)
```

## Online version

A hosted, always up-to-date version of this tool is available at [ascend-digital.net/tools/stegofile](https://ascend-digital.net/tools/stegofile/), available in many other languages, alongside other privacy-first browser tools (image conversion, and more).

## License

GPL-3.0 - see [LICENSE](./LICENSE).
