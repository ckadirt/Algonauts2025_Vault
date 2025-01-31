---
dg-home: false
dg-publish: true
type: meeting
---
Algonauts 2025 Website: [https://algonautsproject.com/](https://algonautsproject.com/) 

Challenge details: [https://www.codabench.org/competitions/4313/](https://www.codabench.org/competitions/4313/)

We have ~6 months to submit our best encoding model (July 6 2025)

Download data: [https://github.com/courtois-neuromod/algonauts_2025.competitors](https://github.com/courtois-neuromod/algonauts_2025.competitors)

Python dev kit: [https://colab.research.google.com/drive/1fop0zvaLBLBagvJRC-HDqGDSgQElNWZB?usp=sharing](https://colab.research.google.com/drive/1fop0zvaLBLBagvJRC-HDqGDSgQElNWZB?usp=sharing)

MedARC github repo: [https://github.com/PaulScotti/algonauts2025](https://github.com/PaulScotti/algonauts2025)

HF Repo: [https://huggingface.co/datasets/medarc/AlgonautsDS-features/](https://huggingface.co/datasets/medarc/AlgonautsDS-features/tree/main)

Working group in MedARC Discord: [https://discord.com/channels/1025299671226265621/1326979843203792957/1326979843203792957](https://discord.com/channels/1025299671226265621/1326979843203792957/1326979843203792957)

## Jan 18 2024

Attendees 

everyone within these brackets have been invited to the github
<>
Paul Scotti (Discord: paulscotti, GitHub: PaulScotti)
Alisa Milchevskaya (Discord: milchevskaya, GitHub: alismil)
Devashri ( Discord: Devashri, Github: Devadeut)
David Weisberg (Discord: Wise_Burger, Github: DavidWeisberg1)
Swarnim Maheshwari (Discord: MootVerick, Github: Snimm)
Yondon Fu (Discord: yondonfu, Github: yondonfu)
Sina Habibian (Discord: sinahab, Github: sinahab)
Jiaxin Cindy Tu (Discord: cindyhfls, Github/Huggingface: cindyhfls)
Rishab Iyer (Discord: bishop, GitHub: rishab-iyer1)
Ian Knight (Discord: knjght, Github: ijight)
Itamar Fruchter (Discord: pitz2217, GitHub: ItamarFruchter)
Connor Lane (Discord: connortslane, GitHub: clane9)
Xun Zhang (Discord: xunzhang4856, Github: tqxg2018)
Ishaan Koratkar (Discord: whybyfire, Github: koratkar)
Mihir Tripathy (discord: mihirtripathy, github: mihirneal)
Cesar Kadir (discord: ckadirt, github: ckadirt)
</>

Keith Matanachai (discord: keithm, GitHub: matan53153)

  

Ideas
- leveraging other datasets
	- forrest gump, sherlock holmes
- predicting voxel space and then projecting with parcellation
	- might work, might not. unclear whether predicting a higher-dim intermediate target would be useful
- Play around with different feature extractors other than the one provided in the tutorial
	- Visual Feature - slow_r50 model, Kinetics  [others: intensity, emotion]
	- Audio Feature - Mel-frequency cepstral coefficients (MFCCs) [others: emotion, tone]
		- These audio features are especially weak. And good points in the meeting about potential usefulness of audio.
	- Language Feature - bert-base-uncased
- Play around with the encoding parameters: modality, hrf_delay, stimulus_window, movies_train, movies_val
- Play around with the encoding model: ridge regression, elastic net 
- Use longer context (Cf Huze [MEM from 2023](https://arxiv.org/abs/2308.01175))
	- something something transformer

Resources:

Gallant lab tutorial: [https://github.com/gallantlab/voxelwise_tutorials?tab=readme-ov-file](https://github.com/gallantlab/voxelwise_tutorials?tab=readme-ov-file)

Himalaya: [https://gallantlab.org/himalaya/](https://gallantlab.org/himalaya/) [https://github.com/gallantlab/voxelwise_tutorials](https://github.com/gallantlab/voxelwise_tutorials)

Pytorch model hub: https://pytorch.org/hub/research-models

[Slides](https://www.canva.com/design/DAGcXZL5tVk/EHBP42X6TRen6ZYTbG2cZA/view?utm_content=DAGcXZL5tVk&utm_campaign=designshare&utm_medium=link2&utm_source=uniquelinks&utlId=hf5ae8e20c6) presented