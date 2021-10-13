#### Command for training with lang1
```
python run.py --model_name_or_path bert-base-multilingual-cased --dataset_name universal_dependencies --task_name pos --dataset_config_name de_hdt --output_dir /tmp/test-ner  --do_train  --do_eval --max_train_sample 800 --max_eval_samples 100 --text_column_name tokens --label_column_name upos --num_train_epochs 20.0 --overwrite_output_dir --max_seq_len 128 --pad_to_max_len
```

#### Command for training with lang 2
```
python run.py --model_name_or_path bert-base-multilingual-cased --dataset_name universal_dependencies --task_name pos --dataset_config_name id_gsd --output_dir /tmp/test-ner  --do_train  --do_eval --max_train_sample 800 --max_eval_samples 100 --text_column_name tokens --label_column_name upos --num_train_epochs 20.0 --resume_from_checkpoint /tmp/test-ner --overwrite_output_dir --max_seq_len 128 --pad_to_max_len
```

#### Command for testing with lang 3
```
python run.py --model_name_or_path bert-base-multilingual-cased --dataset_name universal_dependencies --task_name pos --dataset_config_name ur_udtb --max_predict_samples 100 --do_predict --text_column_name tokens --label_column_name upos --resume_from_checkpoint /tmp/test-ner --max_seq_len 128 --pad_to_max_len --output_dir /tmp/test-ner/test-ch --overwrite_output_dir
```