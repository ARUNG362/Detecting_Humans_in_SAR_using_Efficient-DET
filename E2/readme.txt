STEP 1 : Install Python version 7 or later

STEP 2 : After installing python install the following libraries in python
	# pip install -r requirements.txt

	# base ----------------------------------------
	Cython
	matplotlib>=3.2.2
	numpy>=1.18.5
	opencv-python>=4.1.2
	Pillow
	PyYAML>=5.3.1
	scipy>=1.4.1
	tensorboard>=2.2
	torch>=1.7.0
	torchvision>=0.8.1
	tqdm>=4.41.0

	# logging -------------------------------------
	# wandb

	# plotting ------------------------------------
	seaborn>=0.11.0
	pandas

	# export --------------------------------------
	#coremltools==4.0
	#onnx>=1.8.0
	scikit-learn==0.19.2  # for coreml quantization

	# extras --------------------------------------
	#thop  # FLOPS computation
	#pycocotools>=2.0  # COCO mAP

	# ui------------------------------------------
	pyqt5 # ui

STEP 3 : Download anaconda 3 and configure it to your system
	https://repo.anaconda.com/archive/

STEP 4 : Copy the source code to a new folder(eg: Human-Rescue)

STEP 5 : Create a new folder inside the Human-Rescue folder and name it as weights

STEP 6 : Open Anaconda Prompt and change the directory to the weights folder(eg: cd C/Users/Desktop/Human-Rescue/weights)

STEP 7 : Then download the weights as follow:

	#!/bin/bash
	# Download latest models from https://github.com/ultralytics/yolov5/releases
	# Usage:
	#    $ bash weights/download_weights.sh

	python - <<EOF
	from utils.google_utils import attempt_download

	for x in ['s', 'm', 'l', 'x']:
	    attempt_download(f'yolov5{x}.pt')

	EOF

STEP 8 : Create another folder inside Human-Rescue and name it as data

STEP 9 : Inside data store the video that you want to detect and it should be in .mp4 format(eg: 1.mp4)

STEP 10 : Running the project:
		-> Open Anaconda prompt and change the directory to the Human-Rescue folder
			# cd C/Users/Desktop/Human-Rescue
		-> Then type the run command with the input you want detect
			# python detect_result.py --source data/1.mp4 --weights weights/drone_survivor.pt --classes 0 --project ui_test --img 3840
				NOTE : *data/1.mp4 refers to the input vide0
	



	