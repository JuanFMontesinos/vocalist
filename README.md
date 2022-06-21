# VocaLiST: An Audio-Visual Synchronisation Model for Lips and Voices
[[Project Page]](https://ipcv.github.io/VocaLiST/) [[Arxiv]](https://arxiv.org/abs/2204.02090) [[Weights]](https://drive.google.com/drive/folders/1-g4qHUNNcCZpmSqEflKMxPMvwnn9e88N?usp=sharing)

Official repository for the paper VocaLiST: An Audio-Visual Synchronisation Model for Lips and Voices. 

The paper has been accepted to Interspeech 2022.

### Datasets
There are 2 datasets involved in this work: i) The AV speech dataset of LRS2, 
and ii) the AV singing voice dataset of Acappella.
The LRS2 dataset can be requested for download [here](https://www.robots.ox.ac.uk/~vgg/data/lip_reading/lrs2.html).
The Acappella dataset can be downloaded by following the steps mentioned [here](https://ipcv.github.io/Acappella/acappella/).

### Preprocessing
All the models considered in this work operate on audios sampled at 16kHz 
and videos with 25fps. The preprocessing steps are the same as in 
https://github.com/Rudrabha/Wav2Lip/blob/master/preprocess.py. The objective 
of the preprocessing step is to obtain the cropped RGB face frames of size 3x96x96 
in the .jpg format and audios of 16kHz sampling rate for each of the video samples in respective datasets.

### Testing
To test the models, first download the pretrained model weights from [here](https://drive.google.com/drive/u/0/folders/1-g4qHUNNcCZpmSqEflKMxPMvwnn9e88N).
To test on LRS2, run the program test_lrs2.py. 
To test on Acappella dataset, run the program test_acappella.py.
If you wish to evaluate on Acappella dataset only for a particular context, 
run the program test_acappella_specific.py. Please remember to change the paths to the 
pretrained weights and the dataset related paths accordingly.

### Acknowledgements

The evaluation code is adapted from  Out of time: automated lip sync in the wild. 
The training  code and the experiment configuration setup is borrowed or adapted from that of A Lip Sync Expert Is All You Need for Speech to Lip Generation In the Wild.
The code for internal components of the transformer block is borrowed from
that of the work Multimodal Transformer for Unaligned Multimodal Language Sequences.

### License
This project makes use of source code of other existing works. 
Only the original source code from this repository is provided under CC-BY-NC license, 
while the parts of the repository based on the code reused/adapted from elsewhere 
are available under their respective license terms. 
The code for evaluation setup is adapted from the source code of the paper 
''Out of time: automated lip sync in the wild'' which is made available under https://github.com/joonson/syncnet_python/blob/master/LICENSE.md.
The code for the transformer encoder and its internal components are made available under https://github.com/yaohungt/Multimodal-Transformer/blob/master/LICENSE.
The code related to reading the experiment configuration (hparams) is adapted from the code of https://github.com/Rudrabha/Wav2Lip/
which is under non-commercial license terms. 
