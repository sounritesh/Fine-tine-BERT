#### Command for training with lang1
```
python run.py --model_name_or_path bert-base-multilingual-cased --dataset_name universal_dependencies --task_name pos --dataset_config_name de_hdt --output_dir /tmp/test-ner  --do_train  --do_eval --max_train_sample 800 --max_eval_samples 100 --max_predict_samples 100 --do_predict --text_column_name tokens --label_column_name upos
```

#### Command for training with lang 2
```
python run.py --model_name_or_path bert-base-multilingual-cased --dataset_name universal_dependencies --task_name pos --dataset_config_name de_hdt --output_dir /tmp/test-ner  --do_train  --do_eval --max_train_sample 800 --max_eval_samples 100 --max_predict_samples 100 --do_predict --text_column_name tokens --label_column_name upos --resume_from_checkpoint /tmp/test-ner
```

#### Command for testing with lang 3
```
python run.py --model_name_or_path bert-base-multilingual-cased --dataset_name universal_dependencies --task_name pos --dataset_config_name de_hdt --max_predict_samples 100 --do_predict --text_column_name tokens --label_column_name upos --resume_from_checkpoint /tmp/test-ner
```