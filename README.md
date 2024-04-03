# DeepUTF
DeepUTF: Locating Transcription Factor Binding Sites and Predicting Motifs via Interpretable Dual-Channel Encoder-Decoder Structure
# Datasets:
The complete sequence of chromosome 17 on human genome version hg38 was obtained from UCSC (https://hgdownload.soe.ucsc.edu/downloads.html#human). A total of 53 ChIP-seq datasets were collected from the ENCODE project (https://www.encodeproject.org/). These 53 ChIP-seq datasets originated from GM12878 (21), K562 (20), and HeLa_S3 (12) cell lines. Details of the datasets is available in Supplementary Table S1.
# Dependencies：
PyTorch 1.10.0;
Python 3.8;
Cuda 11.3;
# Model implementation：
data preprocessing: python data_process.py -d … -n … -s …;  train the model: python signal_operate.py -d … -n … -g … -s … -b … -e … -c …;  predict TFBSs: python test.py -d … -n … -g … -c …;  predict motif: python motifs_predict.py -d … -n … -g … -t … -c … -o …;

-d: Datasets path (eg.your_path/DeepUTF/HeLa_S3/CTCF);  -n: Dataset name (eg.CTCF);  -g: GPU device (default is 0);  -s: Random seed (default is 666);  -b: Batch size (default is 500);  -e: Epoch (default is 50);  -t: Threshold value (default is 0.3);  -c: Store model (your_path/DeepUTF/models/HeLa_S3/CTCF);  -o: Store motif (your_path/DeepUTF/motifs/HeLa_S3/CTCF).
