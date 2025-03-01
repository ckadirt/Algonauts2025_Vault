## General
- Features were extracted using kaggle notebook described here [[03 Experiments/Features/Whisper V3/Summary|Summary]]
- The model is from huggingface, this id: `google/paligemma2-3b-mix-224`
- The layers extracted were `layers_to_extract = ["language_model.model.norm", "language_model.model.layers.16.post_feedforward_layernorm"]`
- For each interval of 1.49 seconds we take the first frame and the transcription and pass it to the model.
- Applied a padding and truncation to max 270 tokens.
- 256 of those tokens are from the image and 14 tokens from the transcript o
