<div align="center">

# Video2Music: Suitable Music Generation from Videos using an Affective Multimodal Transformer model

To try out the demo, there are two options. There is one notebook that is intended to be used in colab (Video2Music_colab.ipynb) and one that you can run locally (Video2Music_local.ipynb).
I would recommend using the colab version, as it is easier to get it running. Besides, running the model requires a lot of computational resources which might cause your local device to crash. 
When using the colab version, there is nothing else you have to do, just upload it or use this [link](https://colab.research.google.com/drive/1Pq1FBO5uRvKY9nzMGzMhJq1ILPxIKvU-?usp=sharing) directly. 

When running it locally, there are a few things you have to do first. 

First you need to set up an environment that uses Python=3.8. If you have conda, just run
```bash
conda create -n video2music python=3.8
conda activate video2music
```

If you do not have conda for Linux run:

```bash
pyenv install 3.8.18
pyenv virtualenv 3.8.18 video2music
pyenv activate video2music
```

and for Windows (assuming you have Python=3.8 installed):
```shell
python3.8 -m venv video2music
video2music\Scripts\activate  
```

Now, having set up the environment, we need to install the dependencies, please follow the guide matching your operating system.

## Linux Guide
```bash
apt-get update
apt-get install ffmpeg
apt-get install fluidsynth
git clone git clone https://github.com/Ally511/Video2Music.git
cd Video2Music
pip install -r requirements.txt
```
## Windows Guide
First, you need to install ffmpeg. Try:
```shell
winget install ffmpeg
ffmpeg --version
```
If you have trouble with this, you can also download it [manually](https://ffmpeg.org/download.html), and add it to your system variables:
```
Environment Variables → System variables → Path → Edit
```
and add the bin directory. 
Next, install fluidsynth2.4.6, download the zip via this [link](https://github.com/FluidSynth/fluidsynth/releases) and add it to your system variables following the guide above.

Then run:
```shell
git clone https://github.com/Ally511/Video2Music.git
cd Video2Music
pip install -r requirements.txt
```

## Continuation for both Operating Systems

* Download the processed training data `AMT.zip` from [HERE](https://drive.google.com/file/d/1qpcBXF04pgdy9hqRexr0mTx7L9_CAFpt/view?usp=drive_link) and extract the zip file and put the extracted two files directly under this folder (`saved_models/AMT/`)

* Download the soundfont file `default_sound_font.sf2` from [HERE](https://drive.google.com/file/d/1B9qjgimW9h6Gg5k8PZNt_ArWwSMJ4WuJ/view?usp=drive_link) and put the file directly under this folder (`soundfonts/`)


## Getting Started

Now you can run the notebook! I hope everything runs smoothly. Have fun!

## Acknowledgements

The code in this repository is based on the original [Video2Music](https://github.com/AMAAI-Lab/Video2Music/tree/main).


