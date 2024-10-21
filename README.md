# Full-Transformer-Encoder-Decoder-for-Speech-Recognition

For running the model, just run through the cells in the notebook. 

the experiments: I tuned the number of attention heads from 1-4, layers from 1-2, and dropout rate from 0.1 to 0.3. 

architectures you tried: the provided speech transformer architecture.

the number of epochs you trained for: for part 1, i stopped at epoch 52. For part2, i stopped at epoch 12. 

hyperparameters you used (and specify which combination resulted in the best score):
]
config
{'train_dataset': 'train-clean-100',
 'cepstral_norm': True,
 'input_dim': 27,
 'batch_size': 64,
 'enc_dropout': 0.23,
 'enc_num_layers': 1,
 'enc_num_heads': 1,
 'dec_dropout': 0.23,
 'dec_num_layers': 2,
 'dec_num_heads': 2,
 'd_model': 512,
 'd_ff': 2048,
 'learning_rate': '1E-4',
 'optimizer': 'AdamW',
 'momentum': 0.0,
 'nesterov': True,
 'scheduler': 'CosineAnnealing',
 'factor': 0.9,
 'patience': 3,
 'epochs': 100,
 'Name': 'Zhenjian Wang'}

I have tried to set dropout rate to 0.1, and adding layers and heads, but got worse result, with distance higher than 100. I also tried to increase the attention head in the second part of the HW, but it did not increase the performance of the model. 

data loading scheme: download the data from kaggle, then use the speechdataset class to read in the data. 	
