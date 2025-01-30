---
dg-publish: true
---
Cesar here.

## Objectives
- Trying to see how far can we get with each modilaty. AKA decode parcels just using the video, audio, transcrips.
- Trying to see how far can we get with full features (skipping PCA).

---
## Setup 

I lost the code on SAI cluster, lol. But I've coded over the developer kit notebook.
### For ablation
* Used the same configs/pca features that are on the drive folder provided for the algonauts.
* Retrained the models with the same config: Sklearn, everything the same, just the inputs is different.
* Time window were the same 5
### For full features
- I had to extract the features for the full dataset since it were not provided for the organizers, arount 12 Gbs. here on [hf](https://huggingface.co/datasets/medarc/AlgonautsDS-features/tree/main/developer_kit) 
- For the mcff audio extraction I've used a 128 embedding dimension.
- I had to change the RR alpha parameter bcz it was overfitting when using that huge amount of features, I've used season 6 as validation set and the best alpha was around 40000.
- Time window were the same 5
 
---
## Resuts

Video is the most informative features as expected, is this due to encoder?
![[modality ablation.png]]


There is not a huge drop on performance when using PCA
![[Result full features.png]]


---
## Info about the PCA

| Modality | Model              | Feature Size | Feature Size After PCA |
| -------- | ------------------ | ------------ | ---------------------- |
| Visual   | 3D ResNet Slow R50 | 8192         | 250                    |
| Audio    | MFCCs              | 20           | 20                     |
| Text     | BERT-base-uncased  | (10, 768)    | 50                     |
