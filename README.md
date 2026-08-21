# TRACE: Trust-aware Reliability and Conflict Estimation for Adaptive Multimodal Interfaces
<img width="1536" height="1024" alt="Fig 1" src="https://github.com/user-attachments/assets/78c56ce1-2960-4073-a7f7-aec5996bce0c" />

<img width="1402" height="1122" alt="Fig 6" src="https://github.com/user-attachments/assets/d3e9cc20-3640-4fba-82ae-fa23c6364f58" />


## Main Contributions
Our main contributions can be summarized as follows:
• we propose a reliability-conditioned conflict attribution mech-
anism based on leave-one-out consensus;
• Consensus reliability estimation that prevents inconsistent
modalities from forming an unjustifiably authoritative ma-
jority;
• Counterfactual Conflict Training for explicit contradiction
supervision; and
• An actionable Commit–Clarify–Defer mechanism connect-
ing multimodal reasoning with intelligent user-interface be-
havior.


## Usage

### Prerequisites
- Python 3.9.13
- PyTorch 1.13.0
- CUDA 11.7


### Datasets
Data files (containing processed MOSI, MOSEI datasets) can be downloaded from [here](https://drive.google.com/drive/folders/1BBadVSptOe4h8TWchkhWZRLJw8YG_aEi?usp=sharing). 
You can first build and then put the downloaded datasets into `./dataset` directory and revise the path in `./config/config.json`. For example, if the processed the MOSI dataset is located in `./dataset/MOSI/aligned_50.pkl`. Please make sure "dataset_root_dir": "./dataset" and "featurePath": "MOSI/aligned_50.pkl".
Please note that the meta information and the raw data are not available due to the privacy of YouTube content creators. For more details, please follow the [official website](https://github.com/ecfm/CMU-MultimodalSDK) of these datasets.

### Run the Codes
- Training

You can first set the training dataset name in `./train.py` as "mosei" or "mosi", and then run:
```
python3 train.py
```
By default, the trained model will be saved in `./pt` directory. You can change this in `train.py`.

- Testing

You can first set the testing dataset name in `./test.py` as "mosei" or "mosi", and then test the trained model:
```
python3 test.py
```
We also provide pre-trained models for testing. ([Google drive](https://drive.google.com/drive/folders/1GgCfC1ITAnRRw6RScGc7c2YUg5Ccbdba?usp=sharing))


