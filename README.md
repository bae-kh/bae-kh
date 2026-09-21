<div align="center">

# Kanghyun Bae

### AI Engineer · Computer Vision · LLM/AX · AI Backend

**Building reliable AI systems from models to applications.**

Computer Vision 연구 경험에서 출발해 LLM/AX와 AI Backend로 확장했습니다.<br>
모델 성능뿐 아니라 **평가 조건, 실패 처리, 추론 파이프라인, 서비스 연동**까지 함께 설계합니다.

</div>

## Featured Projects

### 1. [XROSS Edge AI](https://github.com/SEJONG-XROSS/xross-ai)

`Edge AI` · `Computer Vision` · `Team Project`

- **Problem** — 영상만으로는 가림과 배경 움직임에 취약하고, 무게센서만으로는 Pick/Put의 행동 의미를 구분하기 어려운 무인매장 시나리오를 다뤘습니다.
- **Built** — 팀에서 Edge AI와 sensor-event 연동을 중심으로 참여해 YOLOv8·ByteTrack 고객 context, TSM/ResNet50 행동 인식, MQTT trigger, vision-weight cross-validation, backend payload와 SQLite DLQ/retry를 연결했습니다.
- **Evidence / Limit** — RTX 4070 Ti에서 TSM model-only latency **11.82ms → 2.44ms**, PyTorch–TensorRT FP16 class prediction **156/156 일치**를 확인했습니다. 저장 clip 기준이며 live RTSP E2E나 새로운 환경의 일반화 결과는 아닙니다. [검증 보고서](https://github.com/SEJONG-XROSS/xross-ai/blob/main/optimization/results/model-optimization-report.md)

### 2. [LLM Financial Reporting](https://github.com/bae-kh/llm-financial-reporting-pipeline)

`LLM / AX` · `Workflow Automation` · `Evaluation`

- **Problem** — 정확해야 하는 금융 계산과 확률적인 LLM 해석을 분리하고, 외부 데이터·모델 실패가 정상 결과처럼 보이지 않도록 설계했습니다.
- **Built** — Python 지표 계산, 뉴스 snapshot·필터링, Structured Outputs 이후의 evidence·의미 검증, 재작성·fallback·run tracking을 구성했습니다. 검증된 workflow 위에는 주문·추천 기능이 없는 제한된 3-tool Agent를 연결했습니다.
- **Evidence / Limit** — 회귀 테스트 **170개**가 통과하며, 공개 TSLA 실행에서 미근거 주가 전망을 거부하고 1회 재작성했습니다. Live 결과는 1회 실행과 headline metadata 기반 분석입니다. [실행 샘플](https://github.com/bae-kh/llm-financial-reporting-pipeline/blob/main/reports/samples/TSLA_2024-12_live_llm_sample.md)

### 3. [AI Text Moderation Backend](https://github.com/bae-kh/text-moderation-api)

`AI Backend` · `Model Serving` · `Operations`

- **Problem** — 한국어 유해 표현 모델의 category·confidence를 API 응답에 그치지 않고 실제 검토 정책과 운영 흐름으로 연결했습니다.
- **Built** — FastAPI model lifecycle과 threadpool 추론, `allow / review / block` 정책, PostgreSQL review queue, Alembic, Admin API, structured logging, Docker Compose와 CI를 구성했습니다.
- **Evidence / Limit** — 자동화 테스트 **28개**, Docker health smoke test와 Locust 부하 테스트를 구성했습니다. Threshold는 60건 pilot의 56개 조합을 비교한 baseline이며 production 최적값이 아닙니다. [Calibration 근거](https://github.com/bae-kh/text-moderation-api/blob/main/calibration_results/calibration_report.md)

### 4. [Soccer Shot Analyzer](https://github.com/bae-kh/soccer-shot-analyzer)

`Computer Vision` · `FastAPI / SSE` · `React`

- **Problem** — 단일 카메라 축구 영상의 CV 분석을 사용자가 업로드하고 진행률과 결과를 확인할 수 있는 서비스 흐름으로 연결했습니다.
- **Built** — YOLOv8 공 검출, CSRT tracking fallback, YOLOv8-seg 골대 분할, SciPy trajectory fitting을 FastAPI background execution, SSE streaming, React UI와 연결했습니다.
- **Evidence / Limit** — 공개 demo에서 upload → progress → result 흐름을 확인했습니다. 속도와 궤적은 제한된 sample 영상의 추정값이며 radar·IMU·multi-view Ground Truth로 검증한 정확도가 아닙니다.

## Background

- 세종대학교 컴퓨터공학 전공
- Computer Vision 연구실 학부연구생
- **Evidence over Claims** — 결과와 함께 평가 조건, 실패 상태, 재현 범위를 기록합니다.

## Tech Stack

**Languages**

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![SQL](https://img.shields.io/badge/SQL-336791?style=flat-square&logo=postgresql&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)

**AI / Computer Vision**

![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=pytorch&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![Hugging Face](https://img.shields.io/badge/Transformers-FFD21E?style=flat-square&logo=huggingface&logoColor=black)
![TensorRT](https://img.shields.io/badge/TensorRT-76B900?style=flat-square&logo=nvidia&logoColor=white)

**Backend / Data / Tools**

![FastAPI](https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=flat-square&logo=githubactions&logoColor=white)
