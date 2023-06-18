## sphereface2_speaker_verification

official implementation of sphereface2 for speaker verification in [Exploring Binary Classification Loss for Speaker Verification](https://ieeexplore.ieee.org/abstract/document/10094954), this code is based on [wespeaker](https://github.com/wenet-e2e/wespeaker)

### advantages:
1. better performance, especially on hard trials
2. robust to noisy labels
3. natural parallelization for the classifier layer

## Results

| Model | Params | LM | AS-Norm | vox1-O-clean | vox1-E-clean | vox1-H-clean |
|:------|:------:|:--:|:-------:|:------------:|:------------:|:------------:|
| AAM + ResNet34-TSTP-emb256 | 6.63M | × | × | 0.867 | 1.049 | 1.959 |
|                      |       | × | √ | 0.787 | 0.964 | 1.726 |
|                      |       | √ | × | 0.797 | 0.937 | 1.695 |
|                      |       | √ | √ | 0.723 | 0.867 | 1.532 |
| Sphereface2 + ResNet34-TSTP-emb256 | 6.63M | × | × | 0.904 | 0.973 | 1.737 |
|                      |       | × | √ | 0.835 | 0.931 | 1.652 |
|                      |       | √ | × | 0.835 | 0.875 | 1.533 |
|                      |       | √ | √ | 0.776 | 0.846 | 1.460 |



## Citations
If you find its useful, please cite it as
```bibtex
@inproceedings{han2023exploring,
  title={Exploring Binary Classification Loss for Speaker Verification},
  author={Han, Bing and Chen, Zhengyang and Qian, Yanmin},
  booktitle={ICASSP 2023-2023 IEEE International Conference on Acoustics, Speech and Signal Processing (ICASSP)},
  pages={1--5},
  year={2023},
  organization={IEEE}
}

@InProceedings{wen2021sphereface2,
  title = {SphereFace2: Binary Classification is All You Need for Deep Face Recognition},
  author = {Wen, Yandong and Liu, Weiyang and Weller, Adrian and Raj, Bhiksha and Singh, Rita},
  booktitle = {ICLR},
  year = {2022}
}
```
