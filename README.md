## Instructions for the command–line interface

### Training 
The `calamari-cross-fold-train` command will train an ensemble of 5 models based on a cross–fold of the provided training data. Here, training duration is adapted by the `--early_stopping_nbest=5` parameter.

	usage: calamari-cross-fold-train --network=cnn=80:3x3,pool=2x2,cnn=100:3x3,pool=2x2,lstm=200,dropout=0.5,lstm=200,dropout=0.5 --files path_to_training_data/TRAIN_DATA/*.png --best_models_dir some_output_dir --early_stopping_nbest=5 
### Voting
Confidence voting to different predictions of the 5 best models.
  
 	 usage: calamari-predict --checkpoint path_to_model_0.ckpt ... path_to_model_4.ckpt --files path_to_test_data/TEST_DATA/*.bin.png --output_dir some_output_dir
### Evaluation
Evalute the predicted sentences produced by the `calamari-predict` script againt the provided ground truth.

	 usage: calamari-eval --gt path_to_test_data/TEST_DATA/*.gt.txt --pred path_to_predictions/*.pred.txt

### Version 
Calamari 2.1.2 (2022/01/18)
https://github.com/Calamari-OCR/calamari

### Dataset 
This dataset contains text line images (bin.png) and their corresponding ground truth (gt.txt) -- further divided into training and test sets. <br/> 
	
	test dataset: 1671 lines
	training dataset: 6742 lines 

 
