# Instructions for the command–line interface

## Training 
Training an ensemble of 5 models based on a cross-fold on the provided training data using the specific network architecture. Here, 5 models will be trained using 80% of the provided data for training and 20% for validation.

	 calamari-cross-fold-train --network=cnn=80:3x3,pool=2x2,cnn=100:3x3,pool=2x2,lstm=200,dropout=0.5,lstm=200,dropout=0.5 --files path_to_training_data/*.png --best_models_dir some_output_dir --early_stopping_nbest=5 

## Voting
  Confidence voting to different predictions of the 5 models.
  
 	 calamari-predict --checkpoint path_to_model_1.ckpt path_to_model_2.ckpt ... --files path_to_test_data/*.bin.png --output_dir some_output_dir
 
## Evaluate results

	 calamari-eval --gt path_to_test_data/*.gt.txt --pred path_to_predictions/*.pred.txt

 
