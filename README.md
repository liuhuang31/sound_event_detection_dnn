The original code is here https://github.com/qiuqiangkong/DCASE2016_Task3
Because the original code has some problem, which i changed a little.
This is sourcecode of DCASE Challenge 2016 Task 3 (Audio event detection in real life).
Details of this challenge can be seen here. http://www.cs.tut.fi/sgn/arg/dcase2016/task-sound-event-detection-in-real-life-audio

#### Pre-requiste:
* pip install sed_eval		Evaluation toolbox
* pip install librosa		Feature extraction toolbox
* pip install hat 		Deep learning toolbox, https://qiuqiangkong.github.io/Hat 

#### Usage:
------ Preparation ------
* modify the paths of dataset in config.py

------ Train & detect on development datset ------
* run prepare_dev_data.py 	Calculate features for development data
* run main_dev_dnn.py 		Train model on development clips data
* run detect.py 		Detect events on development long audio data
* (optional) run show_results_on_all_folds.py		you must run all 4 folds before you use this function

------ Detect on Privative Evaluation Data ------ 
* run prepare_eva_data.py	Calculate features for evaluation data
* run main_eva_dnn.py		Train model on all development set
* run main_eva_detect.py	Detect and write out events of evaluation data 
