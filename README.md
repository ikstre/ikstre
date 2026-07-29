<div align="center">

# 이태호 · Lee Tae Ho

**"개선했다"는 말은 측정한 뒤에만 씁니다**

비정형 데이터를 정제·구조화하고, NLP·RAG·LLM 파이프라인을 AI 서비스로 구현하는 AI/Data 엔지니어

[![Email](https://img.shields.io/badge/iks6164%40naver.com-03C75A?logo=naver&logoColor=white)](mailto:iks6164@naver.com)
[![Paper](https://img.shields.io/badge/KCI_등재_논문-1저자-2563EB?logo=googlescholar&logoColor=white)](https://drive.google.com/file/d/11pMIT3o6J5oz8fJPHC49oCOtQfx1yvjJ/view?usp=drive_link)

</div>

---

## 🔭 대표 프로젝트 — [CPX 가상 환자 증례 생성](https://github.com/ikstre/Kosin)

> **"실습용 가상 환자 증례를, 검증된 의학 지식에 근거해 생성할 수 있을까?"**

의학교육 CPX(임상수행능력평가) 실습을 위한 **RAG·자기증류 기반 가상 환자 증례 생성 시스템**입니다.
OCR 정제부터 증례 구조화, 생성 엔진, API 설계까지 AI 서비스 전 구간을 담당했습니다.

- **OCR 정제 → 증례 블록 분할 → JSON 변환** 파이프라인 구축, FastAPI 증례 생성·조회 API 설계
- 로컬 LLM과 외부 API를 **선택 연동**하는 구조로 구현 — 폐쇄망·비용 제약 환경 모두 대응
- 구조화 질병 지식 **97건**, 자기증류 합성 증례 **1,293건** 구축
- **모델 선정도 감으로 하지 않았습니다** — 한국어 LLM 4계열 12종을 AutoRAG 자동 평가라인으로 비교해 `exaone3.5:7.8b` 채택
- 발현 증상 기준 **68개 분야** RAG 자동 평가로 검색 설정 최적화

`Python` · `FastAPI` · `ChromaDB` · `BGE-m3-ko` · `QLoRA` · `Ollama/LM Studio`

> 🚧 **후속 연구 논문 작성 중** — 시스템 설계와 평가 결과를 IMRaD 형식 논문으로 정리해 학술지 투고를 준비하고 있습니다.

## 👥 팀 프로젝트

| 프로젝트 | 역할 | 한 일 · 결과 |
|---|---|---|
| **[BidMate](https://github.com/ikstre/BidMate)**<br>기업·공공 RFP 분석 RAG | PM<br>RAG/LLM | PDF/HWP·CSV 98건을 corpus·QA **431쌍**으로 변환, retrieval·post-retrieval·generator **132개 조합** 자동 평가 파이프라인 구축 → `chunk 800 + HybridRRF` 채택으로 hit@5 **0.875** / nDCG@5 **0.844**. 프롬프트 임베딩 캐시로 p95 **6.99s → 2~3초대** |
| **[알약 객체 탐지](https://github.com/ikstre/AI_Model_for_Detecting_Oral_Medication_Tablets)**<br>YOLO 경구약제 이미지 탐지 | PM<br>ML 엔지니어 | AI Hub 라벨 **약 260만 개**를 GCI 기준 통합, 희소 클래스 **+16,012장** 보강 → 12,219건 / 56종. 클래스 가중치 Optuna 탐색으로 mAP@75:95 **0.942 → 0.988**, 앙상블 추가로 **0.994** |

## 📄 참여 논문

**학술지**

| 논문 | 게재 | 핵심 결과 |
|---|---|---|
| [LSTM과 BERT를 활용한 수식 임베딩 및 수학 문제 유형 분류](https://drive.google.com/file/d/11pMIT3o6J5oz8fJPHC49oCOtQfx1yvjJ/view?usp=drive_link) | 멀티미디어학회논문지 28.9 (2025)<br>**KCI 등재 · 1저자** | LaTeX 수식을 증강 bigram 시퀀스로, 주변 문맥을 KoBERT로 인코딩·결합해 6개 유형 분류 — 정확도 **91.96%**, F1 **0.92** (수식 222,919개) |
| [Knowledge-Based Post-Processing of On-Line Hangeul Short-Hand Writing Recognition](https://www.jmis.org/archive/view_article?pid=jmis-10-2-163) | JMIS 10.2 (2023)<br>**1저자** | 혼동 사전·형태소 사전 기반 동적 계획법 격자 탐색으로 실시간 필기 인식 오류 보정 — 구문 인식률 **55.43% → 86.63%** (오류 70% 감소) |

**학술대회**

| 논문 | 게재 | 핵심 결과 |
|---|---|---|
| [LSTM과 BERT를 활용한 LaTeX 수식 임베딩 앙상블 모델](https://drive.google.com/file/d/1QNQKKNoQUqvv7zcUryyFbXclqHL9sQ8j/view?usp=sharing) · [포스터](https://docs.google.com/presentation/d/10Jw0_3Eh4Gk09xI3GJXkv5--fMycdREI/edit?usp=drive_link) | 한국정보과학회 (2024.6)<br>**1저자** | TeX 수식 n-gram + KoBERT 컨텍스트 윈도우 앙상블 — 최고 정확도 **73%** (KoBERT 단독 55%) |
| [신경망을 이용한 온라인 한글 필기 글자 분할](https://drive.google.com/file/d/1w4mejbXWP-PaUse1oq6h3GJ5C-EeKWY4/view?usp=drive_link) · [포스터](https://drive.google.com/file/d/1-A4TAI-Lyp5NGffK1PkMSYlBsfCv7hcj/view?usp=drive_link) | 한국멀티미디어학회 춘계 (2023) | 연속 필기의 글자 경계를 MLP·RNN 두 방식으로 분할·비교 — 적중률 **94.29%** |
| [Food2Vec 모델을 활용한 재료의 유사성 및 음식 추천](https://drive.google.com/file/d/1bN9X_smEuxEhKZR-ne3d-gjOs97OwuCE/view?usp=drive_link) | 한국멀티미디어학회 춘계 (2023) | Word2Vec 기반 Food2Vec으로 식품 벡터 구성, 재료 유사도 기반 추천 (음식 38,192종) |

## 🛠 기술 스택

| 영역 | 스택 |
|---|---|
| **AI/ML** | ![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white) ![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white) ![Ultralytics YOLO](https://img.shields.io/badge/Ultralytics_YOLO-111F68) ![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white) ![Optuna](https://img.shields.io/badge/Optuna-1B4F72) |
| **NLP/LLM/RAG** | ![Transformers](https://img.shields.io/badge/Transformers-FFD21E?logo=huggingface&logoColor=black) ![ChromaDB](https://img.shields.io/badge/ChromaDB-FC521F) ![AutoRAG](https://img.shields.io/badge/AutoRAG-2E86C1) ![BGE-m3-ko](https://img.shields.io/badge/BGE--m3--ko-4B8BBE) ![LoRA/QLoRA](https://img.shields.io/badge/LoRA%2FQLoRA-6A1B9A) ![OpenAI API](https://img.shields.io/badge/OpenAI_API-412991?logo=openai&logoColor=white) ![Ollama](https://img.shields.io/badge/Ollama-000000?logo=ollama&logoColor=white) |
| **Backend/Deploy** | ![FastAPI](https://img.shields.io/badge/FastAPI-009688?logo=fastapi&logoColor=white) ![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?logo=streamlit&logoColor=white) ![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white) |
| **Infra/협업** | ![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black) ![GCP](https://img.shields.io/badge/GCP-4285F4?logo=googlecloud&logoColor=white) ![Conda](https://img.shields.io/badge/Conda-44A833?logo=anaconda&logoColor=white) ![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white) ![Notion](https://img.shields.io/badge/Notion-000000?logo=notion&logoColor=white) |

## 🎓 학력 · 교육

- **부경대학교 인공지능융합학과 석사** (2023.03 – 2025.02) — 인공지능 연구실 · 지도교수 신봉기<br>졸업논문: *LSTM과 BERT를 활용한 수학 문제 유형 분류*
- **부경대학교 컴퓨터공학부 소프트웨어·인공지능 전공 학사** (2017.03 – 2023.02)
- **코드잇 스프린트 AI 엔지니어 부트캠프 수료** (2025.11 – 2026.06) — 팀 프로젝트 3건 팀장 수행

---

<div align="center">

이 페이지의 모든 수치는 논문 게재본 · 평가 로그 · 실험 기록에서 실측한 값입니다.

📫 [iks6164@naver.com](mailto:iks6164@naver.com)

</div>
