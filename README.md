# 🖋️ Fingerprint Recognition (HW5)

[![Python](https://img.shields.io/badge/python-3.8%2B-blue)](#requirements) [![PyPI](https://img.shields.io/badge/dependencies-green)](#requirements) [![License](https://img.shields.io/badge/license-Academic%20Use-yellow)](#license)

지문 이미지의 **전처리 → 특징점 추출 → 매칭** 전 과정을 구현합니다.  
EASY(Test2)에는 KD-Tree 기반 단순 거리 매칭을, HARD(Test1)에는 Siamese 네트워크 기반 임베딩 매칭을 적용했습니다.

---

## 🔍 Features

- **Preprocessing**  
  - Noise 제거, Otsu & Adaptive Threshold 이진화  
  - Convex Hull ROI 추출 및 세선화  
- **Minutiae Extraction**  
  - 3×3 윈도우 vs. 컨볼루션 기반 빠른 검출  
  - ROI/Border 마스크로 불필요 점 제거  
- **EASY Matching (Test2)**  
  - KD-Tree를 사용한 평균·최대·최소 거리 계산  
  - Precision/Recall/FAR/FRR/Accuracy 측정  
- **HARD Matching (Test1)**  
  - Minutiae 맵 → Siamese CNN 임베딩 (128-dim)  
  - 회전 증강(±30°), CosineEmbeddingLoss로 학습  
  - L2 거리 기반 최단거리 매칭  

---
