# <img src="https://raw.githubusercontent.com/idiap/coqui-ai-TTS/main/images/coqui-log-green-TTS.png" height="56"/>


**🐸 Coqui TTS is a library for advanced Text-to-Speech generation.**

🚀 Pretrained models in +1100 languages.

🛠️ Tools for training new models and fine-tuning existing models in any language.

📚 Utilities for dataset analysis and curation.

[![Discord](https://img.shields.io/discord/1037326658807533628?color=%239B59B6&label=chat%20on%20discord)](https://discord.gg/5eXr5seRrv)
[![PyPI - Python Version](https://img.shields.io/pypi/pyversions/coqui-tts)](https://pypi.org/project/coqui-tts/)
[![License](<https://img.shields.io/badge/License-MPL%202.0-brightgreen.svg>)](https://opensource.org/licenses/MPL-2.0)
[![PyPI version](https://badge.fury.io/py/coqui-tts.svg)](https://pypi.org/project/coqui-tts/)
[![Downloads](https://pepy.tech/badge/coqui-tts)](https://pepy.tech/project/coqui-tts)
[![DOI](https://zenodo.org/badge/265612440.svg)](https://zenodo.org/badge/latestdoi/265612440)
[![GithubActions](https://github.com/idiap/coqui-ai-TTS/actions/workflows/tests.yml/badge.svg)](https://github.com/idiap/coqui-ai-TTS/actions/workflows/tests.yml)
[![GithubActions](https://github.com/idiap/coqui-ai-TTS/actions/workflows/docker.yaml/badge.svg)](https://github.com/idiap/coqui-ai-TTS/actions/workflows/docker.yaml)
[![GithubActions](https://github.com/idiap/coqui-ai-TTS/actions/workflows/style_check.yml/badge.svg)](https://github.com/idiap/coqui-ai-TTS/actions/workflows/style_check.yml)
[![Docs](<https://readthedocs.org/projects/coqui-tts/badge/?version=latest&style=plastic>)](https://coqui-tts.readthedocs.io/en/latest/)

</div>

## 📣 Notice
### This is a fork of the [new Coqui TTS](https://github.com/idiap/coqui-ai-TTS) which is a fork of the [old Coqui TTS that is now unmaintained repository](https://github.com/coqui-ai/TTS) that shutdown.
- **New PyPI package: [coqui-tts](https://pypi.org/project/coqui-tts)**
- Make sure you aren't using the Python package [TTS](https://pypi.org/project/TTS/). You should be using [Coqui-TTS](https://pypi.org/project/coqui-tts/).

From here on, I will **not** reference the old Coqui TTS (unless explicitly stated), so if I mention the "previous Coqui TTS" or the "old Coqui TTS", I am referring to [idiap/coqui-ai-TTS](https://github.com/idiap/coqui-ai-TTS).


My goal with this fork is to document my attempts to clone a voice using [Coqui-TTS](https://github.com/idiap/coqui-ai-TTS) to be used on [Home Assistant](https://www.home-assistant.io/). I am running the cloned voice on my local desktop. My Home Assistant is running on a [Raspberry Pi 5](https://www.pishop.us/product/raspberry-pi-5-8gb/) with 8 GB of RAM. As of right now, they both run on the same network, but, in the future, I will attempt to have these operations be performed over the internet.

As a result, I have emphasized human-like speech synthesis, so any results or features that did not aid in this endeavor may have been removed from the old version of Coqui-TTS. I also did not use Docker, so a lot of that was removed. If you are interested in running Docker, feel free to refer to the previous Coqui-TTS repo.

My **local desktop** is running on the following components:
* **OS:** Ubuntu 24.04
* **GPU:** Sapphire AMD Radeon RX 7900 XT - 20 GB GDR6, AMD RDNA 3
* **CPU:** Intel i7 14th generation - 14700K with 20 cores (8 P-Cores + 12 E-Cores)
* **CPU Cooler:** Corsair iCUE Link Titan 360 RX RGB Liquid CPU Cooler - 360 mm AIO
* **PSU:** Corsair HX1000i Fully Modular Ultra-Low Noise
* **Storage:** WD_BLACK 4 TB SN850X NVMe M.2 SSD with Heatsink
* **Memory:** Corsair Vengeance RGB DDR5 RAM 96 GB (2x48GB) 5600 MHz CL40 XMP
* **Motherboard:** ASUS TUF Gaming Z790-PLus Wi-Fi LGA 1700 ATX


## 💬 Where to ask questions (idiap/coqui-ai-TTS)
If it's about my modifications of Coqui-TTS, you can message me directly on GitHub. If it's not about my modifications, please refer to [idiap's version of coqui-ai-TTS](https://github.com/idiap/coqui-ai-TTS).


## 🔗 Links and Resources
| Type                            | Links                               |
| ------------------------------- | --------------------------------------- |
| 💼 **Documentation**              | [ReadTheDocs](https://coqui-tts.readthedocs.io/en/latest/)
| 💾 **Installation**               | [TTS/README.md](https://github.com/idiap/coqui-ai-TTS/tree/dev#installation)|
| 👩‍💻 **Contributing**               | [CONTRIBUTING.md](https://github.com/idiap/coqui-ai-TTS/blob/main/CONTRIBUTING.md)|
| 🚀 **Released Models**            | [Standard models](https://github.com/idiap/coqui-ai-TTS/blob/dev/TTS/.models.json) and [Fairseq models in ~1100 languages](https://github.com/idiap/coqui-ai-TTS#example-text-to-speech-using-fairseq-models-in-1100-languages-)|

For my specific changes, you can read about them in their corresponding *.md files on this fork.

## Features
- High-performance text-to-speech and voice conversion models, see list below.
- Fast and efficient model training with detailed training logs on the terminal and Tensorboard.
- Support for multi-speaker and multilingual TTS.
- Released and ready-to-use models.
- Tools to curate TTS datasets under ```dataset_analysis/```.
- Command line and Python APIs to use and test your models.
- Modular (but not too much) code base enabling easy implementation of new ideas.

## Model Implementations
### Spectrogram models
- [Tacotron](https://arxiv.org/abs/1703.10135), [Tacotron2](https://arxiv.org/abs/1712.05884)
- [Glow-TTS](https://arxiv.org/abs/2005.11129), [SC-GlowTTS](https://arxiv.org/abs/2104.05557)
- [Speedy-Speech](https://arxiv.org/abs/2008.03802)
- [Align-TTS](https://arxiv.org/abs/2003.01950)
- [FastPitch](https://arxiv.org/pdf/2006.06873.pdf)
- [FastSpeech](https://arxiv.org/abs/1905.09263), [FastSpeech2](https://arxiv.org/abs/2006.04558)
- [Capacitron](https://arxiv.org/abs/1906.03402)
- [OverFlow](https://arxiv.org/abs/2211.06892)
- [Neural HMM TTS](https://arxiv.org/abs/2108.13320)
- [Delightful TTS](https://arxiv.org/abs/2110.12612)

### End-to-End Models
- [XTTS](https://arxiv.org/abs/2406.04904)
- [VITS](https://arxiv.org/pdf/2106.06103)
- 🐸[YourTTS](https://arxiv.org/abs/2112.02418)
- 🐢[Tortoise](https://github.com/neonbjb/tortoise-tts)
- 🐶[Bark](https://github.com/suno-ai/bark)

### Vocoders
- [MelGAN](https://arxiv.org/abs/1910.06711)
- [MultiBandMelGAN](https://arxiv.org/abs/2005.05106)
- [ParallelWaveGAN](https://arxiv.org/abs/1910.11480)
- [GAN-TTS discriminators](https://arxiv.org/abs/1909.11646)
- [WaveRNN](https://github.com/fatchord/WaveRNN/)
- [WaveGrad](https://arxiv.org/abs/2009.00713)
- [HiFiGAN](https://arxiv.org/abs/2010.05646)
- [UnivNet](https://arxiv.org/abs/2106.07889)

### Voice Conversion
- [FreeVC](https://arxiv.org/abs/2210.15418)
- [kNN-VC](https://doi.org/10.21437/Interspeech.2023-419)
- [OpenVoice](https://arxiv.org/abs/2312.01479)

### Others
- Attention methods: [Guided Attention](https://arxiv.org/abs/1710.08969),
  [Forward Backward Decoding](https://arxiv.org/abs/1907.09006),
  [Graves Attention](https://arxiv.org/abs/1910.10288),
  [Double Decoder Consistency](https://erogol.com/solving-attention-problems-of-tts-models-with-double-decoder-consistency/),
  [Dynamic Convolutional Attention](https://arxiv.org/pdf/1910.10288.pdf),
  [Alignment Network](https://arxiv.org/abs/2108.10447)
- Speaker encoders: [GE2E](https://arxiv.org/abs/1710.10467),
  [Angular Loss](https://arxiv.org/pdf/2003.11982.pdf)

You can also help us implement more models.

<!-- start installation -->
## Installation

🐸TTS is tested on Ubuntu 24.04 with **python >= 3.10, < 3.13**, but should also
work on Mac and Windows.

If you plan to code or train models, clone 🐸TTS and install it locally.

```bash
git clone https://github.com/idiap/coqui-ai-TTS
```
```bash
cd coqui-ai-TTS
```
```bash
pip install -e .
```

When I was starting up the repo, I received errors with the previous steps alone, so if you have issues as well, or if you are only interested in [synthesizing speech](https://coqui-tts.readthedocs.io/en/latest/inference.html) with the pretrained 🐸TTS models, installing from PyPI is the easiest option.

```bash
pip install coqui-tts
```

### Optional dependencies

The following extras allow the installation of optional dependencies:

| Name | Description |
|------|-------------|
| `all` | All optional dependencies |
| `notebooks` | Dependencies only used in notebooks |
| `server` | Dependencies to run the TTS server |
| `bn` | Bangla G2P |
| `ja` | Japanese G2P |
| `ko` | Korean G2P |
| `zh` | Chinese G2P |
| `languages` | All language-specific dependencies |

You can install extras with one of the following commands:

```bash
pip install coqui-tts[server,ja]
```
or
```bash
pip install -e .[server,ja]
```

### Platforms

If you are on Ubuntu (Debian), you can also run the following commands for installation.

```bash
make system-deps
```
```bash
make install
```

<!-- end installation -->

## A Note on GPU Usage
The original Coqui-TTS includes GPU capabilities for Nvidia, but, as you can see above, I am running an AMD GPU. As of right now, I haven't figured out how to have the software use my AMD GPU, but the software does recognize my AMD GPU, so that's a start. I will work on the implementation of the AMD GPU once everything else is up and running since the CPU support is sufficient for now.

GPU Usage is noted in the following files (maybe more):
* Markdown files:
  - `/root/README.md`
    - Mentions GPU usage in the context of running TTS models, e.g., using `"cuda"` as the device in Python API examples and references to GPU in hardware requirements.
  - `/root/recipes/bel-alex73/README.md`
    - Describes running training with GPU, e.g., using `CUDA_VISIBLE_DEVICES` and multi-GPU training.
  - `/root/docs/source/training/training_a_model.md`
    - Explains how to check available GPUs (`nvidia-smi`) and how to run multi-GPU training with `CUDA_VISIBLE_DEVICES`.
  - `/root/docs/source/docker_images.md`
    - Shows how to run Docker containers with GPU support using `--gpus all` and mentions checking CUDA version with `nvidia-smi`.

* Python scripts:
  - `/root/TTS/bin/collect_env_info.py`
    - Collects and prints CUDA (GPU) info, including device names and availability.
  - `/root/TTS/tts/layers/xtts/gpt.py`
    - Has parameters for number of GPUs and DeepSpeed inference.
  - `/root/TTS/utils/distribute.py`
    - Contains functions for initializing distributed training across multiple GPUs using PyTorch.
  - `/root/TTS/tts/models/vits.py`
    - Handles distributed sampling and batch samplers for multi-GPU training.
  - `/root/TTS/bin/compute_statistics.py` 
    - Uses `torch.cuda.is_available()` to determine device for processing.
  - `/root/TTS/demos/xtts_ft_demo/xtts_demo.py`
    - Calls `clear_gpu_cache()` to manage GPU memory during dataset preprocessing.
  - `/root/notebooks (e.g., ExtractTTSpectrogram.ipynb, notebooks/TestAttention.ipynb)`
    - Use `torch.cuda.is_available()` and set `CUDA_VISIBLE_DEVICES` for GPU selection.

This is a good starting point to guide someone that is wanting to add AMD GPU support.

## Synthesizing speech by 🐸TTS
<!-- start inference -->
### 🐍 Python API

#### Multi-speaker and multi-lingual model

```python
import torch
from TTS.api import TTS

# Get device
device = "cuda" if torch.cuda.is_available() else "cpu"

# List available 🐸TTS models
print(TTS().list_models())

# Initialize TTS
tts = TTS("tts_models/multilingual/multi-dataset/xtts_v2").to(device)

# List speakers
print(tts.speakers)

# Run TTS
# ❗ XTTS supports both, but many models allow only one of the `speaker` and
# `speaker_wav` arguments

# TTS with list of amplitude values as output, clone the voice from `speaker_wav`
wav = tts.tts(
  text="Hello world!",
  speaker_wav="my/cloning/audio.wav",
  language="en"
)

# TTS to a file, use a preset speaker
tts.tts_to_file(
  text="Hello world!",
  speaker="Craig Gutsy",
  language="en",
  file_path="output.wav"
)
```

From version 0.27.0 you can [cache cloned
voices](https://coqui-tts.readthedocs.io/en/latest/cloning.html) with a custom
`speaker` ID, so you only need to pass audio files in `speaker_wav` once.

#### Single speaker model

```python
# Initialize TTS with the target model name
tts = TTS("tts_models/de/thorsten/tacotron2-DDC").to(device)

# Run TTS
tts.tts_to_file(text="Ich bin eine Testnachricht.", file_path=OUTPUT_PATH)
```

#### Voice conversion (VC)

Converting the voice in `source_wav` to the voice of `target_wav`:

```python
tts = TTS("voice_conversion_models/multilingual/vctk/freevc24").to("cuda")
tts.voice_conversion_to_file(
  source_wav="my/source.wav",
  target_wav="my/target.wav",
  file_path="output.wav"
)
```

Other available voice conversion models:
- `voice_conversion_models/multilingual/multi-dataset/knnvc`
- `voice_conversion_models/multilingual/multi-dataset/openvoice_v1`
- `voice_conversion_models/multilingual/multi-dataset/openvoice_v2`

For more details, see this
[dedicated page](https://coqui-tts.readthedocs.io/en/latest/vc.html).

#### Voice cloning by combining single speaker TTS model with the default VC model

This way, you can clone voices by using any model in 🐸TTS. The FreeVC model is
used for voice conversion after synthesizing speech.

```python

tts = TTS("tts_models/de/thorsten/tacotron2-DDC")
tts.tts_with_vc_to_file(
    "Wie sage ich auf Italienisch, dass ich dich liebe?",
    speaker_wav="target/speaker.wav",
    file_path="output.wav"
)
```

#### TTS using Fairseq models in ~1100 languages 🤯
For Fairseq models, use the following name format: `tts_models/<lang-iso_code>/fairseq/vits`.
You can find the language ISO codes [here](https://dl.fbaipublicfiles.com/mms/tts/all-tts-languages.html)
and learn about the Fairseq models [here](https://github.com/facebookresearch/fairseq/tree/main/examples/mms).

```python
# TTS with fairseq models
api = TTS("tts_models/deu/fairseq/vits")
api.tts_to_file(
    "Wie sage ich auf Italienisch, dass ich dich liebe?",
    file_path="output.wav"
)
```

### Command-line interface `tts`

<!-- begin-tts-readme -->

Synthesize speech on the command line.

You can either use your trained model or choose a model from the provided list.

- List provided models:

  ```sh
  tts --list_models
  ```

- Get model information. Use the names obtained from `--list_models`.
  ```sh
  tts --model_info_by_name "<model_type>/<language>/<dataset>/<model_name>"
  ```
  For example:
  ```sh
  tts --model_info_by_name tts_models/tr/common-voice/glow-tts
  ```
  ```sh
  tts --model_info_by_name vocoder_models/en/ljspeech/hifigan_v2
  ```

#### Single speaker models

- Run TTS with the default model (`tts_models/en/ljspeech/tacotron2-DDC`):

  ```sh
  tts --text "Text for TTS" --out_path output/path/speech.wav
  ```

- Run TTS and pipe out the generated TTS wav file data:

  ```sh
  tts --text "Text for TTS" --pipe_out --out_path output/path/speech.wav | aplay
  ```

- Run a TTS model with its default vocoder model:

  ```sh
  tts --text "Text for TTS" \
      --model_name "<model_type>/<language>/<dataset>/<model_name>" \
      --out_path output/path/speech.wav
  ```

  For example:

  ```sh
  tts --text "Text for TTS" \
      --model_name "tts_models/en/ljspeech/glow-tts" \
      --out_path output/path/speech.wav
  ```

- Run with specific TTS and vocoder models from the list. Note that not every vocoder is compatible with every TTS model.

  ```sh
  tts --text "Text for TTS" \
      --model_name "<model_type>/<language>/<dataset>/<model_name>" \
      --vocoder_name "<model_type>/<language>/<dataset>/<model_name>" \
      --out_path output/path/speech.wav
  ```

  For example:

  ```sh
  tts --text "Text for TTS" \
      --model_name "tts_models/en/ljspeech/glow-tts" \
      --vocoder_name "vocoder_models/en/ljspeech/univnet" \
      --out_path output/path/speech.wav
  ```

- Run your own TTS model (using Griffin-Lim Vocoder):

  ```sh
  tts --text "Text for TTS" \
      --model_path path/to/model.pth \
      --config_path path/to/config.json \
      --out_path output/path/speech.wav
  ```

- Run your own TTS and Vocoder models:

  ```sh
  tts --text "Text for TTS" \
      --model_path path/to/model.pth \
      --config_path path/to/config.json \
      --out_path output/path/speech.wav \
      --vocoder_path path/to/vocoder.pth \
      --vocoder_config_path path/to/vocoder_config.json
  ```

#### Multi-speaker models

- List the available speakers and choose a `<speaker_id>` among them:

  ```sh
  tts --model_name "<language>/<dataset>/<model_name>"  --list_speaker_idxs
  ```

- Run the multi-speaker TTS model with the target speaker ID:

  ```sh
  tts --text "Text for TTS." --out_path output/path/speech.wav \
      --model_name "<language>/<dataset>/<model_name>"  --speaker_idx <speaker_id>
  ```

- Run your own multi-speaker TTS model:

  ```sh
  tts --text "Text for TTS" --out_path output/path/speech.wav \
      --model_path path/to/model.pth --config_path path/to/config.json \
      --speakers_file_path path/to/speaker.json --speaker_idx <speaker_id>
  ```

#### Voice conversion models

```sh
tts --out_path output/path/speech.wav --model_name "<language>/<dataset>/<model_name>" \
    --source_wav <path/to/speaker/wav> --target_wav <path/to/reference/wav>
```

<!-- end-tts-readme -->
