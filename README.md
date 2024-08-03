## Generating Dubbed and narrated videos based on speakers’ gender identification using deep learning techniques

## Introduction
The purpose of the project is to create high-quality, highly accurate Vietnamese dubbed or dubbed videos with high subtitles and gender classification models while meeting diverse user needs.

#### Source of data sets
- AudioMNIST: Becker, S., Vielhaben, J., Ackermann, M., M ̈uller, K.-R., Lapuschkin, S., Samek, W.: Audiomnist:  xploring explainable artificial intelligence for audio analysis on a simple benchmark. Journal of the Franklin Institute
361(1), 418–428 (2024)
- TIMIT: Garofolo, J., Lamel, L., Fisher, W., Fiscus, J., Pallett, D., Dahlgren, N., Zue, V.: Timit acoustic-phonetic continuous speech corpus. Linguistic
Data Consortium (1992)
- RAVDESS: Livingstone, S.R., Russo, F.A.: The ryerson audio-visual database of emo-tional speech and song (ravdess): A dynamic, multimodal set of facial and vocal expressions in north american english. PLOS ONE 13(5), 0196391 (2018)
- CTU & COMMON: Nguyen, H.T., Thanh, T.N.L., Ngoc, T.L., Le, A.D., Tran, D.T.: Eval-uation on noise reduction in subtitle generator for videos. In: Innova-tive Mobile and Internet Services in Ubiquitous Computing, pp. 140–150. Springer (2022)

## Installation
Python version 3.6 and install the dependencies:

    pip install -r requirements.txt

## Usage
Using Speech-to-Text with Openai Whisper

    python3 openai-whisper.py https://www.youtube.com/watch?v=zkczDkbaE68 --l_in en -r 10 -v 40 --ad_subtitle_en=True --retain_sound=True -noise=True --gender auto 

Using Speech-to-Text with Google Cloud

    python3 google-cloud.py https://www.youtube.com/watch?v=zkczDkbaE68 --l_in en -r 10 -v 40 --ad_subtitle_en=True --retain_sound=True -noise=True --gender auto

The explanation of the parameters is explained as follow:

    

    source_path: Path to the video or audio file to subtitle (required).
    
    -r, --rate: Rate for speech (default: 10). Example usage: -r 15

    -v, --volume: Volume for speech (default: 50). Example usage: -v 70

    -ms, --ms_start: Start time in milliseconds for overlaying the audio on the video (default: 0). Example usage: -ms 500

    --ad_subtitle_en: Create subtitle videos with original language: --ad_subtitle_en true

    --retain_sound: Retain the original sound (default: True). Example usage: --retain_sound false
    
    -s, --l_in: Input file language (default: "en"). Example usage: -s fr

    -d, --l_out: Output file language (default: "vi"). Example usage: -d es

    -noise, --algorithm_noise: Choose noise reduction algorithm (default: False). Example usage: -noise true

    --gender: Gender recognition for Text To Speech model (choices: "auto", "female", "male"; default: "auto"). Example usage: --gender female

## Demo

Please click into below image!

[![Thesis defense](https://img.youtube.com/vi/MAtX8bfNNy4/0.jpg)](https://www.youtube.com/watch?v=MAtX8bfNNy4)
