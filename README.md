# OCR_YOLO_Parsing_Dacon 🏆 private 점수 1등, 최우수상 수상

## 재정QA: YOLO 기반 PDF 레이아웃 인식 + 좌표 텍스트 추출 + LLM 재해석
## 핵심아이디어: 재정 PDF 레이아웃을 YOLO로 탐지 → 좌표 단위 텍스트 추출 → 표/테이블은 LLM으로 구조적 재해석(🧠)

## 배경

- 중앙정부 재정 데이터는 방대하며 PDF 중심의 비정형 레이아웃(표, 도표, 각주, 머리말/꼬리말 등)로 제공됩니다.
- 단순 텍스트 추출만으로는 문맥/구조가 망가져 QA에 오류가 발생합니다.
- 본 리포지토리는 PDF 레이아웃을 보존하면서 정확한 질의응답을 수행하기 위한 문서이해 파이프라인을 제공합니다.

## 문제 정의 (Problem → Solution)
- ❗️ 필요: 레이아웃 인식(🔎), 좌표 기반 추출(📐)
  - ✅ 해결: YOLO로 title/table/figure/header/footer 블록 검출
- ❗️ 필요: 머지 셀·다단 등 복잡 표 재해석(📊)
  - ✅ 해결: LLM으로 구조화/정규화/요약(🧠)

## 📓 작동 원리 & 코드: notebooks/*.ipynb 참고

<img width="480" height="700" alt="page_3" src="https://github.com/user-attachments/assets/23420425-c5ec-4136-b557-a894a60ac5ba" />
<img width="480" height="700" alt="page_3" src="https://github.com/user-attachments/assets/02b60482-1cfd-4a91-9736-e1467942c6e2" />



## 감사의 말 (Acknowledgements)

- 대회 주최/주관 및 데이터 제공처에 감사드립니다.
- 본 연구/구현은 공개 문서와 대회 제공 자료만을 활용했습니다.


## Citation

```bibtex
@misc{zhao2024doclayoutyoloenhancingdocumentlayout,
      title={DocLayout-YOLO: Enhancing Document Layout Analysis through Diverse Synthetic Data and Global-to-Local Adaptive Perception}, 
      author={Zhiyuan Zhao and Hengrui Kang and Bin Wang and Conghui He},
      year={2024},
      eprint={2410.12628},
      archivePrefix={arXiv},
      primaryClass={cs.CV},
      url={https://arxiv.org/abs/2410.12628}, 
}

@article{wang2024mineru,
  title={MinerU: An Open-Source Solution for Precise Document Content Extraction},
  author={Wang, Bin and Xu, Chao and Zhao, Xiaomeng and Ouyang, Linke and Wu, Fan and Zhao, Zhiyuan and Xu, Rui and Liu, Kaiwen and Qu, Yuan and Shang, Fukai and others},
  journal={arXiv preprint arXiv:2409.18839},
  year={2024}
}

```
