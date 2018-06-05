# NoiseReduction
ノイズ軽減

## Algorithm
スペクトルサブトラクション (Spectral Subtraction) によるノイズ軽減.   
[librosa](https://librosa.github.io/librosa/)のSTFT(Short-Time Fourier Transfor)を利用している.   
ノイズを含む音声から, ノイズ部分の時間を切り取り, STFTの平均をとる.   
そして, すべてのSTFTから平均ノイズSTFTを減算し, ノイズ軽減音声を生成する.


## 事前準備
1. python3をインストール.
2. pip3で下記をインストール   
```pip3 install argparse```   
```pip3 install numpy```   
```pip3 install librosa```   

## 使い方
```python3 NoiseReduction.py -i [元の音声ファイル名] -o[ノイズ軽減の音声ファイル名] -s [サンプルノイズの開始時 (sec)] -f [再プルノイズの終了時 (sec)]```