# Command–Line Interface

## Train
Training an ensemble of 5 models based on a cross-fold on the provided training data. 
	 calamari-cross-fold-train --network=cnn=80:3x3,pool=2x2,cnn=100:3x3,pool=2x2,lstm=200,dropout=0.5,lstm=200,dropout=0.5 --files "/PATH_TO_TRAINING_DATA/*.png" --best_models_dir "/SOME_OUTPUT_DIR" --early_stopping_nbest=5 

## Predict
 
 	 calamari-predict --checkpoint "/PATH_TO_TRAINED_MODELS/*.ckpt.json" --files "/PATH_TO_TEST_DATA/*.bin.png" --output_dir "/SOME_OUTPUT_DIR"
 
## Evaluate results

	 calamari-eval --gt ’’/Users/mollyskelbye/Desktop/OCR/OCR_SB/TEST_1671/*.gt.txt" --pred ”/Users/mollyskelbye/Desktop/OCR/*.pred.txt”’

 
