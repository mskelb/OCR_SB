## About this repository 
📌 This repository provides scripts for training an ensemble of five character recognition models using a cross––folding technique. These experiments are based on the research outlined in the paper 'OCR Processing of Swedish Historical Newspapers Using Deep Hybrid CNN–LSTM Networks': [OCR Processing of Swedish Historical Newspapers Using Deep Hybrid CNN–LSTM Networks](https://acl-bg.org/proceedings/2021/RANLP%202021/pdf/2021.ranlp-1.23.pdf). 

📌 The experiments, conducted with the open––source OCR engine Calamari, showcased the superiority of mixed deep CNN––LSTM hybrid models over previous methods for character recognition of Swedish historical newspaper text dated between 1818 and 1848. The models achieved an average character accuracy rate (CAR) of 97.43%, setting a new state––of––the––art standard in the analysis of 19th––century Swedish newspaper text.

## Instructions for the command–line interface

### Training 
The `calamari-cross-fold-train` command will train an ensemble of 5 models based on a cross–fold of the provided training data. Training duration is adapted by the `--early_stopping_nbest=5` parameter.

	usage: calamari-cross-fold-train --network=cnn=80:3x3,pool=2x2,cnn=100:3x3,pool=2x2,lstm=200,dropout=0.5,lstm=200,dropout=0.5 --files path_to_training_data/*.png --best_models_dir some_output_dir --early_stopping_nbest=5 
### Voting
Confidence voting to different predictions of the five best models.
  
 	 usage: calamari-predict --checkpoint path_to_model_0.ckpt ... path_to_model_4.ckpt --files path_to_test_data/*.bin.png --output_dir some_output_dir
### Evaluation
Evaluate the predicted sentences produced by the `calamari-predict` script against the provided ground truth.

	 usage: calamari-eval --gt path_to_test_data/*.gt.txt --pred path_to_predictions/*.pred.txt

### Version 
Calamari 2.1.2 (2022/01/18)
https://github.com/Calamari-OCR/calamari

### Dataset 
The dataset contains text line images (bin.png) and their corresponding ground truth (gt.txt) from selected Swedish newspapers spanning between 1818 and 1848. The dataset has been further divided into training and test subsets. <br/> 
	
	test dataset: 1671 lines
	training dataset: 6742 lines 

 
