---
dg-publish: true
---
**Algonauts 2019:**

![[2019 image.png]]

- **Overview:** The inaugural Algonauts Challenge in 2019 focused on predicting brain activity in response to static images of objects. Participants were tasked with developing computational models to predict neural responses recorded via fMRI and MEG.  [algonauts.csail.mit.edu](http://algonauts.csail.mit.edu/2019/challenge.html)    
- **Stimuli:** Participants were provided with a set of static images depicting various objects.
- **Target:** The goal was to predict brain activity from two sources: fMRI data from two brain regions and MEG data from two time windows. 
- **Winning Method:** 

**Algonauts 2021:**

![[2021 image.png]]
- **Overview:** The 2021 challenge aimed to predict brain responses to dynamic visual stimuli, specifically short video clips. Participants developed models to forecast neural activity as recorded by fMRI and MEG during the viewing of these clips.   [algonauts.csail.mit.edu](http://algonauts.csail.mit.edu/2021/challenge.html)
- **Stimuli:** Short video clips (3 to 10 seconds) depicting various dynamic scenes were used as stimuli.
- **Target:** The objective was to accurately predict brain responses to these video clips, selected voxels from whole brain. 
- **Winning Method:** The winning method by huze, proposed an effective ensemble approach combining multiple deep neural networks. He utilized different models for stimuli encoding, and based on those diverse features he trained diverse fmri decoding models to create a weight ensemble method, ensuring improved performance on the validation set. This ensemble strategy allowed for capturing diverse aspects of the data, leading to enhanced prediction accuracy.   [algonauts.csail.mit.edu](http://algonauts.csail.mit.edu/reports_2021/report_huze.pdf)

**Algonauts 2023:**
![[2023 image.png]]

- **Overview:** The 2023 challenge focused on predicting human brain responses to complex natural visual scenes. This edition utilized data from the Natural Scenes Dataset (NSD), the largest available dataset of its kind, to facilitate data-intensive modeling.    [algonauts.csail.mit.edu](https://algonautsproject.com/2023/challenge.html)
- **Stimuli:** Participants were provided with images of complex natural scenes from the NSD dataset.
- **Target:** The goal was to develop computational models that could predict brain responses recorded while participants viewed these natural scenes, fsaverage, vertice brain surfaces.   
- **Winning Method:** The winning method by huze was based on the memory approach, where he used the previous seen images and the current one to predict the current brain activity, and also some other behavioral data. The final score also uses feature ensemble.  [arxiv](https://arxiv.org/abs/2308.01175)