## General
- Features were extracted using kaggle notebook described here [[03 Experiments/Features/Whisper V3/Summary|Summary]]
- The model is from huggingface, this id: `google/paligemma2-3b-mix-224`
- The layers extracted were `layers_to_extract = ["language_model.model.norm", "language_model.model.layers.16.post_feedforward_layernorm"]`
- For each interval of 1.49 seconds we take the first frame and the transcription and pass it to the model.
- Applied a padding and truncation to max 276 tokens.
- 256 of those tokens are from the image and 20 tokens from the transcript of that interval. 
- Dimension of the features for each layer of each interval is: `1,276, 2304`
- Extracting those features for all the stimuli is heavy on disk space, for season 1 of friends is around 28Gb for one layer (56Gb for the two layers I did), and the max output of kaggle is just 20Gb, in the future I'm thinking about implementing a direct write on HF from kaggle to skip the output limit.
- For that reason I just decided to do a quick experiment on wolf and life stimuli, training on Wolf and evaluating on life with RR.

## Results
- Since features are heavy the experiment was done with a stimuli window of 2, but I'll write a more efficient way to do RR and scale it longer stimuli window.
- This is the result using 2 for stimuli window with all the features from the developer kit trained on wolf and validated on life.
- ![[wolftr_lifete_all_sw2_700k.png]]
- And this are the results with Paliggema
- 