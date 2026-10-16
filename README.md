# Voice packs

Speech model files the OpenSwarm desktop app downloads the first time a person turns on its natural
reply voice. Nothing here is code. Each release is one pack, named by the digests of its files, and
the app checks every file's size and sha256 against its own pin before using it, so a copy from here
and a copy from the original source are interchangeable.

## pocket-en-9b960942

Kyutai's Pocket TTS (English, without voice cloning) in the layout the
[ptts](https://github.com/gradium-ai/xn-ptts) runtime loads, with one voice.

| File | Bytes | sha256 |
| --- | ---: | --- |
| `config.json` | 988 | `c1178a4fb93365c9d5086d6a075540e88eaaf117277d7a82c7f2246af77f39c1` |
| `tokenizer.json` | 245,020 | `f498428e1eafee50492f7be13dc9bfafcfc12e508cd0eb1b01c92ecd5d8c6687` |
| `alba.safetensors` | 512,088 | `ad234695323e4030336b6afc8a050c97e3110603e11ecd8226d9562488300a50` |
| `model.q8.gguf` | 164,952,320 | `dda32506821b9895d67cf66232e97c4187f92ec82e51e7e537835bb681f964e8` |

The files are copied unchanged from revision `7cc3c90b88f3e6617ded1b9b74100d1cd0162d90` of
[davencyw/pocket-tts-ptts](https://huggingface.co/davencyw/pocket-tts-ptts), where
`alba.safetensors` sits at `embeddings/alba.safetensors`.

## Credits and licence

- **Model:** [Pocket TTS](https://huggingface.co/kyutai/pocket-tts) by [Kyutai](https://kyutai.org),
  CC BY 4.0 ([code](https://github.com/kyutai-labs/pocket-tts),
  [paper](https://arxiv.org/abs/2509.06926)).
- **Voice:** alba, voice-acted by Alba MacKenna, from
  [kyutai/tts-voices](https://huggingface.co/kyutai/tts-voices), CC BY 4.0.
- **Layout:** [davencyw/pocket-tts-ptts](https://huggingface.co/davencyw/pocket-tts-ptts), CC BY 4.0,
  which renamed the weights, added `config.json`, and added `model.q8.gguf` (the flow model's
  transformer linears quantized to q8_0 by ptts's `quantize` example).

All files are licensed under [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/); the full text
is in [LICENSE](LICENSE). This repository changes nothing in them.

Kyutai's terms of use apply: use must comply with all applicable laws and must not involve voice
impersonation or cloning without explicit and lawful consent, presenting generated speech as genuine
recordings of real people or events, or any other illegal, harmful, deceptive or unauthorized activity.
