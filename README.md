# Command-Line Interface

## Training 
	 calamari-cross-fold-train --network=cnn=80:3x3,pool=2x2,cnn=100:3x3,pool=2x2,lstm=200,dropout=0.5,lstm=200,dropout=0.5 --files "/Users/mollyskelbye/Desktop/OCR/OCR_SB/TRAIN_6742/*.png" --best_models_dir "/Users/mollyskelbye/Desktop/OCR" --early_stopping_nbest=5

## Testing
 
 	 calamari-predict --checkpoint "/Users/mollyskelbye/Desktop/OCR/*.ckpt.json” --files "/Users/mollyskelbye/Documents/GitHub/EXJOBB/TEST_20%/*.bin.png" --output_dir "/Users/mollyskelbye/Documents/GitHub/EXJOBB/TEST_20%”
 
## Evaluation of results

	 calamari-eval --gt ’’/Users/mollyskelbye/Desktop/OCR/OCR_SB/TEST_1671/*.gt.txt" --pred ”/Users/mollyskelbye/Desktop/OCR/*.pred.txt”’

 
