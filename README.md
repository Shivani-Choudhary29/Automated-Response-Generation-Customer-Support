# Automated-Response-Generation-Customer-Support
Automated Response Generation for Customer Support using fine tuned LLama2 model

Step 1: Install All the Required Packages

Step 2: Import All the Required Libraries

Step 3: Explored and preprocess the dataset (Use Llama2 specification for Prompt)

Step 4: Fine Tune:
1. Load a llama-2-7b-chat-hf model (chat model)
2. Train it on the dataset ("Kaludi/Customer-Support-Responses"), which will produce our fine-tuned model Llama-2-7b-chat-finetune

Step 5: Load everything and start the fine-tuning process
  1. First of all, we want to load the dataset we defined. Here, our dataset is already preprocessed but, usually, this is where you would reformat the prompt, filter out bad text, combine      multiple datasets, etc.
  2. Then, we’re configuring bitsandbytes for 4-bit quantization.
  3. Next, we're loading the Llama 2 model in 4-bit precision on a GPU with the corresponding tokenizer.
  4. Finally, we're loading configurations for QLoRA, regular training parameters, and passing everything to the SFTTrainer. The training has started.

Step 6: Save the model and Use the text generation pipeline to ask questions.


Note: You can change the learning hyperparamter as per your system speed, If you have sufficient GPU access, you can train the model better.

