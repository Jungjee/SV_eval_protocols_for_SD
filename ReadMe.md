## Overview
This repository shares the evaluation protocols for speaker verification described in [[1]](https://ieeexplore.ieee.org/document/10096449).
The purpose is to select speaker embedding extractors that suit speaker diarisation using equal error rates without having the need to examine diarisation performances for each speaker embedding extractor.
The protocols consist of short segments (i.e., utterances) cropped from existing speaker diarisation datasets.

## Protocol details
We provide five evaluation protocols on two speaker diarisation datasets [2, 3]. Refer to [[1]](https://ieeexplore.ieee.org/document/10096449) for full details.
1. `clean_eval_protocol.txt`: both enrollment utterances are **single-speaker** utterances.
2. `overlap_1_49_eval_protocol.txt`: the enrollment utterance is **single-speaker**, but the the test utterance has a second speaker simultaneously speaking with a **1-49% ratio of overlap** in terms of duration.
3. `overlap_50_100_eval_protocol.txt`: the enrollment utterance is **single-speaker**, but the the test utterance has a second speaker simultaneously speaking with a **50-100% ratio of overlap** in terms of duration.
4. `speaker_change_eval_protocol.txt`: the enrollment utterance is **single-speaker**, but the the test utterance has a second speaker where the primary speaker does not speak while the second speaker utters.
5. (recommended) `combined_protocol.txt`: all four previous evaluation protocols are combined. 

### Data structure
We provide evaluation protocols on two datasets: DIHARD3 [2] and VoxConverse [3].
Below tree describes the folder/file structure under [evaluation_protocols](evaluation_protocols).
```
.
├── DIHARD3
│   ├── clean_eval_protocol.txt
│   ├── combined_protocol.txt
│   ├── overlap_1_49_eval_protocol.txt
│   ├── overlap_50_100_eval_protocol.txt
│   └── speaker_change_eval_protocol.txt
└── VoxConverse
    ├── clean_eval_protocol.txt
    ├── combined_protocol.txt
    ├── overlap_1_49_eval_protocol.txt
    ├── overlap_50_100_eval_protocol.txt
    └── speaker_change_eval_protocol.txt
```

## References
[1]
```
@inproceedings{jung2023in,
  title={In search of strong embedding extractors for speaker diarisation},
  author={Jung, Jee-weon and Heo, Hee-Soo and Lee, Bong-Jin and Huh, Jaesung and Brown, Andrew and Kwon, Youngki and Watanabe, Shinji and Chung, Joon Son,
  booktitle={Proc. ICASSP},
  year={2023}
}
```
[2]
```
@inproceedings{ryant2020third,
  title={The third DIHARD diarization challenge},
  author={Ryant, Neville and Singh, Prachi and Krishnamohan, Venkat and Varma, Rajat and Church, Kenneth and Cieri, Christopher and Du, Jun and Ganapathy, Sriram and Liberman, Mark},
  booktitle={Proc. Interspeech},
  year={2021}
}```
[3]
```
@inproceedings{chung2020spot,
  title={Spot the conversation: speaker diarisation in the wild},
  author={Chung, Joon Son and Huh, Jaesung and Nagrani, Arsha and Afouras, Triantafyllos and Zisserman, Andrew},
  booktitle={Proc. Interspeech},
  year={2020}
}```

If you make use of the evaluation protocols in this repository, consider referencing [1].
