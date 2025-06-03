# Multimodal-Argumentative-Fallacy-Classification-in-Political-Debates-Codes



This repository contains the codebase for our task on the **MMUSED-Fallacy** dataset. We explore multiple input modalities—**Text**, **Audio**, and **Multimodal (Text + Audio)**—to classify argumentative fallacies.

## Structure
The repository is organized into three main directories, each representing a different modality:


## Models Used

- **Text-Only**: [`RoBERTa`](https://huggingface.co/roberta-base) with tokenized concatenated sentences for context.
- **Audio-Only**: `BiLSTM` trained on `MFCC` features extracted from raw audio.
- **Text-Audio**: A late fusion approach combining `RoBERTa` (for text) and [`Wav2Vec2`](https://huggingface.co/facebook/wav2vec2-base-960h) (for audio), followed by a `Logistic Regression` classifier.

## Reproducibility

To ensure reproducibility:

- Set random seeds for all modules.
- Provide preprocessed data scripts.
- Checkpoints and metrics are saved under the `results/` directory.

## Citation

If you use this repository or build upon our experiments, please use MAMKit toolkit, which provides the backbone for our data loading and preprocessing:

```bibtex
@inproceedings{mancini-etal-2024-mamkit,
    title = "{MAMK}it: A Comprehensive Multimodal Argument Mining Toolkit",
    author = "Mancini, Eleonora  and
      Ruggeri, Federico  and
      Colamonaco, Stefano  and
      Zecca, Andrea  and
      Marro, Samuele  and
      Torroni, Paolo",
    editor = "Ajjour, Yamen  and
      Bar-Haim, Roy  and
      El Baff, Roxanne  and
      Liu, Zhexiong  and
      Skitalinskaya, Gabriella",
    booktitle = "Proceedings of the 11th Workshop on Argument Mining (ArgMining 2024)",
    month = aug,
    year = "2024",
    address = "Bangkok, Thailand",
    publisher = "Association for Computational Linguistics",
    url = "https://aclanthology.org/2024.argmining-1.7",
    doi = "10.18653/v1/2024.argmining-1.7",
    pages = "69--82",
}
```



---

