# Fine-tuning-DeepSeek-R1-Distill-Qwen-1.5B-for-ReAct

The ReAct prompt is used to build agents which can use tools if needed. DeepSeek-R1-Distill-Qwen-1.5B runs on local with minimal resources but does not give good results on ReAct prompt. This repo contains code to fine-tune the DeepSeek-R1-Distill-Qwen-1.5B model with ReAct example so that the final trained model can be used for ReAct prompts giving better results and thus able to build agents locally.

`react_dataset.jsonl` - This is the dataset of 60 samples for ReAct. It is curated through output of bigger models as well as manual efforts (of course it can be improved further with different cases).

`ReAct_DeepSeek_Training.ipynb` - This notebook gives details on actual training procedure using Unsloth and saving LoRA weights of the trained model.

`ReAct_Model_Export.ipynb` - This notebook shows how the trained model can be pushed to huggingface hub, converted to GGUF format along with quantization and use that final model through ollama so it can be used locally to build agents.
