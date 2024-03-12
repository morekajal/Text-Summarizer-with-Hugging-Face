# Text-Summarizer-with-Hugging-Face
Text Summarizer with Hugging Face Transformers library, Finetuning, Inferencing and Evaluation of model with Pretrained Model

- Used the Hugging Face 'samsum' dataset with AutoTokenizer, AutoModelForSeq2SeqLM, Hugging face Pipeline for summarization, and "google/pegasus-cnn_dailymail" model
- Encoded the data (with datasets map method) to input and target encodings with input_ids, attention_mask and converted target input_ids to labels
- Finetune the pretrained  "google/pegasus-cnn_dailymail" model on samsum['test'] dataset, as train dataset is quite huge and need more computation power
- Tackle with the OutOfMemory error by experimenting with TrainingArguments
- Use Trainer along with model, training_args, tokenizer, and data_collator
- tried with different epochs to reduce the training_loss
- Evaluated the mode with the rough_metrics and understand the purpose
- Save the pretrained model and tokenizer and again load them for inferencing
  
