---
dg-publish: true
---

## Feature extraction general
- Dataset with stimuli and parcels is here: https://www.kaggle.com/datasets/ckadirt/algonauts2025nsl on kaggle.
- This notebook perform feature extraction on kaggle using that detaset:[https://www.kaggle.com/code/ckadirt/features-extraction-algonauts2025](https://www.kaggle.com/code/ckadirt/features-extraction-algonauts2025 "https://www.kaggle.com/code/ckadirt/features-extraction-algonauts2025")
- You just need to modify the `extract_fn` function, which receives the video, audio, and transcript intervals (you can define the duration) and should return a dictionary with `layer_name` and corresponding `torch.Tensor`. It also uses Connor's feature extractor and writes .h5 files.

## Feature extraction Whisper V3 Large
- The features were extracted from the encoder of the model, which on HF implementation receives a fixed sequence len input so processor had to apply padding, ending with a dimension of batch_size, 1500, 1280, the sequence dimension has been averaged so each interval is 1, 1, 1280
- Four layers were extracted: 
- `layers_to_extract = ["layer_norm", 'layers.31.fc2', 'layers.25.fc2', 'layers.12.fc2']`
- The time interval was the same as the TR 1.49seconds.

## Results
This is the result using RR with just the Whisper features, a concatenation of all the layers extracted.
![[download (7).png]]
This is the result using RR with the original audio features from the developer kit: mfcc
![[download (8).png]]

This is the result using the features for audio+text (concatenated) from the developer kit: bert + mfcc:
![[download (9).png]]