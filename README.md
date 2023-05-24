# Setting up for inference:

## Step1: Download this modified repo (NOT THE ORIGINAL)
This repo has a lot of changes that enable smooth inference to heatmaps.

## Step2: Set up conda env
Follow the instructions in the original repo readme for setting up the environment. **Important**: after the environment is set up by their instructions, run:

> pip install -r requirements.txt

This should be it for the environment. If you encounter that something is missing, just pip install it. This seemed to work for me. If you have troubles, e.g. w/ ME, try Adam (teammate not optimizer) or Google.

## Step3: Download and store data and model
First download the processed ScanNet200 data from X. Store the scannet200 folder in ../data/processed/. **Important**: Make a copy of this folder in the same directory, and call it scannet. This is currently nessasary as the repo sometimes interchanges these. I may fix this later if I have time. Then download the scannet200 **test** checkpoint (can be found in the main readme), and store it under /checkpoints/scannet200/. Make sure to not change any filenames!

## Step4: Run the inference script
Running the *inference.sh* script will use the downloaded checkpoint to do inference on the processed data, namely all data in the train folder:
