<div align="center">

# 이태호 · Taeho Lee

**비정형 데이터를 정제·구조화하고, NLP·RAG·LLM 파이프라인을 AI 서비스로 구현하는 AI/Data 엔지니어**

[![Email](https://img.shields.io/badge/Email-iks6164@naver.com-03C75A?style=flat-square&logo=naver&logoColor=white)](mailto:iks6164@naver.com)
[![GitHub](https://img.shields.io/badge/GitHub-ikstre-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/ikstre)
<!-- TODO: 포트폴리오/노션 링크 있으면 아래 주석 해제 -->
<!-- [![Portfolio](https://img.shields.io/badge/Portfolio-000000?style=flat-square&logo=notion&logoColor=white)](LINK_HERE) -->

</div>

---

## About

- 텍스트 데이터 전처리부터 NLP·RAG·LLM 파이프라인 구축, 지표 기반 평가와 서비스 구현까지 수행
- KCI 등재지 게재를 포함해 **논문 5편**에 참여 (1저자 3편)
- **AutoRAG 기반 RAG 최적화** — hit@5 0.875 / nDCG@5 0.844, 응답 지연 p95 6.99s → 2~3초대
- **대규모 라벨 통합·자동화 파이프라인** — 검출 성능 mAP@75:95 0.942 → 0.988, 앙상블 적용 시 0.994
- 데이터 처리 흐름을 안정적인 AI 서비스로 연결하는 엔지니어로 성장하고자 합니다

---

## Tech Stack

**ML / DL**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![YOLO](https://img.shields.io/badge/Ultralytics_YOLO-111F68?style=flat-square&logo=yolo&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Optuna](https://img.shields.io/badge/Optuna-1B4F72?style=flat-square)

**NLP / LLM / RAG**

![Transformers](https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![RAG](https://img.shields.io/badge/RAG-4B8BBE?style=flat-square)
![AutoRAG](https://img.shields.io/badge/AutoRAG-2E86C1?style=flat-square)
![ChromaDB](https://img.shields.io/badge/ChromaDB-FF6F61?style=flat-square)
![LangChain](https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI_API-412991?style=flat-square&logo=openai&logoColor=white)
![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white)

`LSTM` `BERT` `BGE-m3-ko` `LoRA / QLoRA` `모델 양자화` `Prompt Engineering`

**Service / Deploy**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)

**Infra / Collaboration**

![Linux](https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=linux&logoColor=black)
![GCP](https://img.shields.io/badge/GCP-4285F4?style=flat-square&logo=googlecloud&logoColor=white)
![Anaconda](https://img.shields.io/badge/Conda-44A833?style=flat-square&logo=anaconda&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![Notion](https://img.shields.io/badge/Notion-000000?style=flat-square&logo=notion&logoColor=white)

---

## Projects

### CPX 가상 환자 증례 생성 시스템
> RAG·자기증류 데이터 기반 의학교육용 가상 환자 증례 생성 시스템

**역할** AI 서비스 개발 — OCR 정제, 증례 구조화, RAG 생성 엔진, FastAPI API 설계
**기술** `Python` `FastAPI` `ChromaDB` `BGE-m3-ko` `QLoRA` `Ollama / LM Studio`

- OCR 정제 → 증례 블록 분할 → JSON 변환 파이프라인 구성, 증례 생성·조회 API와 로컬 LLM·외부 API 선택 연동 구조 구현
- 구조화 질병 지식 97건, 자기증류 합성 증례 1,293건 구축
- 한국어 LLM 4계열 12종을 AutoRAG 자동 평가라인으로 비교해 `exaone3.5:7.8b` 선정
- 발현 증상 기준 68개 분야 RAG 자동 평가로 검색 설정 최적화, 후속 연구 논문 작성 중

[![Repository](https://img.shields.io/badge/Repository-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/ikstre/Kosin)

---

### BidMate
> 기업·공공 RFP 문서 대상 RAG 시스템

**역할** PM, RAG/LLM — 로컬 모델 파이프라인 구축, AutoRAG 최적화, LoRA·QLoRA 실험
**기술** `Python` `Streamlit` `ChromaDB` `AutoRAG` `BGE-m3-ko` `LoRA / QLoRA`

- PDF/HWP·CSV 문서 98건을 corpus / QA 431쌍으로 변환해 ChromaDB 구축
- retrieval · post-retrieval · generator 총 132개 조합 자동 평가 파이프라인 구축
- 평가 결과 `chunk 800 + HybridRRF` 채택 — hit@5 0.875 / nDCG@5 0.844 / p95 6.99s
- 프롬프트 임베딩 캐시 도입으로 p95 6.99s → 2~3초대 단축, grounded·field coverage 지표로 품질 점검

[![Repository](https://img.shields.io/badge/Repository-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/ikstre/BidMate)

---

### AI 경구약제 알약 식별
> YOLO 기반 AI Hub 경구약제 이미지 객체 검출 모델

**역할** PM, ML 엔지니어 — Optuna 하이퍼파라미터 탐색 및 학습 파이프라인 구축, 성능 평가
**기술** `Python` `Ultralytics YOLO` `COCO` `OpenCV` `Optuna` `Pandas`

- AI Hub 제공 전체 데이터 약 260만 개 라벨을 GCI(Global Category Index) 기준으로 통합
- 희소 클래스 +16,012장 보강 및 이상 데이터 제거 → 최종 12,219건 / 56종 클래스
- 클래스 가중치 Optuna 탐색으로 mAP@75:95 **0.942 → 0.988** 개선, 여기에 모델 앙상블을 추가해 최고 **0.994** 달성

[![Repository](https://img.shields.io/badge/Repository-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/ikstre/AI_Model_for_Detecting_Oral_Medication_Tablets)

---

## Publications

### 학술지

**LSTM과 BERT를 활용한 수식 임베딩 및 수학 문제 유형 분류**
멀티미디어학회논문지 28.9 (2025): 1426–1434 · KCI 등재 · 1저자
LaTeX 수식을 증강 bigram 시퀀스로, 주변 문맥을 KoBERT로 인코딩·결합해 고교 수학 문제 6개 유형 분류 — 정확도 **91.96%**, F1 **0.92** (수식 222,919개)
[논문 보기](https://drive.google.com/file/d/11pMIT3o6J5oz8fJPHC49oCOtQfx1yvjJ/view?usp=drive_link)

**Knowledge-Based Post-Processing of On-Line Hangeul Short-Hand Writing Recognition**
The Journal of Multimedia Information System 10.2 (2023): 163–168 · 1저자
인식기 혼동 사전과 형태소 어휘 사전 기반 동적 계획법 격자 탐색으로 한글 필기 인식 오류를 실시간 보정 — 구문 인식률 **55.43% → 86.63%** (오류 70% 감소)
[논문 보기](https://www.jmis.org/archive/view_article?pid=jmis-10-2-163)

### 학술대회

**LSTM과 BERT를 활용한 LaTeX 수식 임베딩 앙상블 모델**
한국정보과학회 학술발표논문집 (2024.6): 984–986 · 1저자
TeX 수식을 n-gram화해 LSTM으로, 주변 컨텍스트 윈도우를 KoBERT로 분석·결합한 앙상블 모델 — 최고 정확도 **73%** (KoBERT 단독 55%, 수식 65,388개)
[논문 보기](https://drive.google.com/file/d/1QNQKKNoQUqvv7zcUryyFbXclqHL9sQ8j/view?usp=sharing) · [포스터](https://docs.google.com/presentation/d/10Jw0_3Eh4Gk09xI3GJXkv5--fMycdREI/edit?usp=drive_link)

**신경망을 이용한 온라인 한글 필기 글자 분할**
한국멀티미디어학회 춘계학술발표대회 논문집 26.1 (2023): PD.35–36 · 2저자
연속 한글 필기의 글자 경계를 다층 퍼셉트론과 순환 신경망 두 방식으로 분할·비교 — 적중률 **94.29%**
[논문 보기](https://drive.google.com/file/d/1w4mejbXWP-PaUse1oq6h3GJ5C-EeKWY4/view?usp=drive_link) · [포스터](https://drive.google.com/file/d/1-A4TAI-Lyp5NGffK1PkMSYlBsfCv7hcj/view?usp=drive_link)

**Food2Vec 모델을 활용한 재료의 유사성 및 음식 추천**
한국멀티미디어학회 춘계학술발표대회 논문집 26.1 (2023): PD.37–40 · 2저자
Word2Vec 기반 Food2Vec으로 식품 벡터를 구성해 재료 유사도 기반 음식 추천과 영양정보 제공 (음식 38,192종)
[논문 보기](https://drive.google.com/file/d/1bN9X_smEuxEhKZR-ne3d-gjOs97OwuCE/view?usp=drive_link)

---

## Education

**부경대학교 인공지능융합학과 석사** (2023.03 – 2025.02)
인공지능 연구실 (Artificial Intelligence Lab) · 지도교수 신봉기
졸업논문: LSTM과 BERT를 활용한 수학 문제 유형 분류

**부경대학교 컴퓨터공학부 소프트웨어·인공지능 전공 학사** (2017.03 – 2023.02)
주요과목: 딥러닝, 강화학습, 컴퓨터비전, 소프트웨어공학

**코드잇 스프린트 AI 엔지니어 부트캠프 수료** (2025.11 – 2026.06)
Python·데이터 분석·머신러닝·PyTorch 기반 모델 구현, 텍스트 임베딩·BERT/GPT·프롬프트 엔지니어링·PEFT·RAG, Docker·모델 변환/양자화·FastAPI 서빙 이수 · 팀 프로젝트 3건 팀장 수행

---

<div align="center">

<!-- TODO: 통계 카드가 필요하면 주석 해제 -->
<!--
![GitHub Stats](https://github-readme-stats.vercel.app/api?username=ikstre&show_icons=true&hide_border=true)
![Top Langs](https://github-readme-stats.vercel.app/api/top-langs/?username=ikstre&layout=compact&hide_border=true)
-->

</div>
