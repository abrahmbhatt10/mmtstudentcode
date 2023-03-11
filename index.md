# Audio Samples for Multitrack Music Transformer

## Content

- [Best samples](#best-samples)
  - [Best unconditioned generation samples](#best-unconditional)
  - [Best instrument-informed generation samples](#best-instrument-informed)
  - [Best 4-beat continuation samples](#best-4-beat-continuation)
- [Examples of unconditional generation](#unconditional)
- [Examples of instrument-informed generation](#instrument-informed)
- [Examples of 4-beat continuation](#continuation-4-beat)
- [Examples of 16-beat continuation](#continuation-16-beat)

---

## Summary of the compared models

- __MMT__: Our proposed Multitrack Music Transformer model
- __MMM__: A decoder-only transformer using the MultiTrack representation proposed by Ens and Pasquier (2020)[^ens2020]
- __REMI+__: A decoder-only transformer using the REMI+ representation proposed by von Rütte et al. (2022)[^vonrutte2022]

| Model | Instrument control | Compound tokens | Average sample length<br>(second) | Inference speed<br>(notes per second) |
|-|:-:|:-:|:-:|:-:|
| MMT (ours) | __✓__ | __✓__ | __100.42__ | __11.79__ |
| MMM | ✕ | ✕ | 38.69 | 5.66 |
| REMI+ | ✕ | ✕ | 28.69 | 3.58 |
{:style="width: 75%; margin-left: auto; margin-right: auto;"}

[^ens2020]: Jeff Ens and Philippe Pasquier, “MMM: Exploring conditional multi-track music generation with the transformer,” arXiv preprint arXiv:2008.06048, 2020.
[^vonrutte2022]: Dimitri von Rütte, Luca Biggio, Yannic Kilcher, and Thomas Hofmann, “FIGARO: Generating symbolic music with fine-grained artistic control,” arXiv preprint arXiv:2201.10936, 2022.

---

## Best samples {#best-samples}

Here are some of the best samples we found.

{% include video_player.html id="7g0F0lMs18Y" %}

### Best unconditioned generation samples {#best-unconditional}

> __Settings__: Only a `start-of-song' event is provided to the model. The model generates the instrument list and subsequently the note sequence.

|-|-|-|-|
| {% include audio_player.html filename="audio/sod/best/3_unconditioned.mp3" style="width:240px;" %} | {% include audio_player.html filename="audio/sod/best/12_unconditioned.mp3" style="width:240px;" %} | {% include audio_player.html filename="audio/sod/best/16_unconditioned.mp3" style="width:240px;" %} | {% include audio_player.html filename="audio/sod/best/23_unconditioned.mp3" style="width:240px;" %} |
| {% include audio_player.html filename="audio/sod/best/31_unconditioned.mp3" style="width:240px;" %} | {% include audio_player.html filename="audio/sod/best/39_unconditioned.mp3" style="width:240px;" %} | {% include audio_player.html filename="audio/sod/best/43_unconditioned.mp3" style="width:240px;" %} | {% include audio_player.html filename="audio/sod/best/45_unconditioned.mp3" style="width:240px;" %} |

### Best instrument-informed generation samples {#best-instrument-informed}

> __Settings__: The model is given a 'start-of-song' event followed by a sequence of instrument codes and a 'start-of-notes' event to start with. The model then generates the note sequence.

|-|-|-|-|
| __Ensemble__: piano, church-organ, voices | {% include audio_player.html filename="audio/sod/best/7_instrument-informed.mp3" %} |
| __Ensemble__: contrabass, harp, english-horn, flute | {% include audio_player.html filename="audio/sod/best/40_instrument-informed.mp3" %} |
| __Ensemble__: trumpet, trombone | {% include audio_player.html filename="audio/sod/best/33_instrument-informed.mp3" %} |
| __Ensemble__: church-organ, viola, contrabass, strings, voices, horn, oboe | {% include audio_player.html filename="audio/sod/best/10_instrument-informed.mp3" %} |
{:style="width: 80%; margin-left: auto; margin-right: auto;"}

### Best 4-beat continuation samples {#best-4-beat-continuation}

> __Settings__: All instrument and note events in the first 4 beats are provided to the model. The model then generates subsequent note events that continue the input music.

|-|-|-|
| {% include audio_player.html filename="audio/sod/best/9_4-beat-continuation.mp3" %} | {% include audio_player.html filename="audio/sod/best/19_4-beat-continuation.mp3" %} | {% include audio_player.html filename="audio/sod/best/23_4-beat-continuation.mp3" %}
| {% include audio_player.html filename="audio/sod/best/26_4-beat-continuation.mp3" %} | {% include audio_player.html filename="audio/sod/best/34_4-beat-continuation.mp3" %} | {% include audio_player.html filename="audio/sod/best/35_4-beat-continuation.mp3" %} |

---

## Examples of unconditioned generation (unselected) {#unconditional}

> __Settings__: Only a `start-of-song' event is provided to the model. The model generates the instrument list and subsequently the note sequence.

| | Sample 1 | Sample 2 | Sample 3 |
|:-:|:-:|:-:|:-:|
| MMT (ours) | {% include audio_player.html filename="audio/sod/ape/0_unconditioned.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/ape/1_unconditioned.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/ape/2_unconditioned.mp3" style="width:250px;" %} |
| MMM        | {% include audio_player.html filename="audio/sod/mmm/0_unconditioned.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/mmm/1_unconditioned.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/mmm/2_unconditioned.mp3" style="width:250px;" %} |
| REMI+      | {% include audio_player.html filename="audio/sod/remi/0_unconditioned.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/remi/1_unconditioned.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/remi/3_unconditioned.mp3" style="width:250px;" %} |

---

## Examples of instrument-informed generation (unselected) {#instrument-informed}

> __Settings__: The model is given a 'start-of-song' event followed by a sequence of instrument codes and a 'start-of-notes' event to start with. The model then generates the note sequence.

| | Sample  1 | Sample 2 | Sample 3 |
|:-:|:-:|:-:|:-:|
| MMT (ours) | {% include audio_player.html filename="audio/sod/ape/0_instrument-informed.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/ape/1_instrument-informed.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/ape/2_instrument-informed.mp3" style="width:250px;" %} |

---

## Examples of 4-beat continuation (unselected) {#continuation-4-beat}

> __Settings__: All instrument and note events in the first 4 beats are provided to the model. The model then generates subsequent note events that continue the input music.


| | Sample 1 | Sample 2 | Sample 3 |
|:-:|:-:|:-:|:-:|
| MMT (ours) | {% include audio_player.html filename="audio/sod/ape/0_4-beat-continuation.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/ape/1_4-beat-continuation.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/ape/2_4-beat-continuation.mp3" style="width:250px;" %} |
| Ground truth | {% include audio_player.html filename="audio/sod/truth/0_truth.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/truth/1_truth.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/truth/3_truth.mp3" style="width:250px;" %} |

---

## Examples of 16-beat continuation (unselected) {#continuation-16-beat}

> __Settings__: All instrument and note events in the first 16 beats are provided to the model. The model then generates subsequent note events that continue the input music.


| | Sample 1 | Sample 2 | Sample 3 |
|:-:|:-:|:-:|:-:|
| MMT (ours) | {% include audio_player.html filename="audio/sod/ape/0_16-beat-continuation.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/ape/1_16-beat-continuation.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/ape/2_16-beat-continuation.mp3" style="width:250px;" %} |
| Ground truth | {% include audio_player.html filename="audio/sod/truth/0_truth.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/truth/1_truth.mp3" style="width:250px;" %} | {% include audio_player.html filename="audio/sod/truth/2_truth.mp3" style="width:250px;" %} |

---
