.PHONY: all

ifndef INPUT_FILE
INPUT_FILE = ../data/dev.json
endif

ifndef OUTPUT_DIR
OUTPUT_DIR = predictions/
endif

all: bert roberta gpt2 xlnet sentiment
bert: bert-base-cased bert-large-cased
roberta: roberta-base roberta-large 
xlnet: xlnet-base-cased xlnet-large-cased
gpt2: gpt2-small gpt2-medium gpt2-large

bert-base-cased:
	python3 eval_discriminative_models.py --pretrained-class bert-base-cased --tokenizer BertTokenizer --intrasentence-model BertLM --intersentence-model BertNextSentence --input-file $(INPUT_FILE) --output-dir $(OUTPUT_DIR) $(FLAGS) 

