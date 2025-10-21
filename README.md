이 리포지토리는 ITWILL 기말 프로젝트 **AI Desk Guide**의 개인 정리 버전입니다.  
> 원본 팀 리포: [https://github.com/itwill-ai/AI-Desk-Guide](https://github.com/yujinc129-oss/5piece)


# 🦾 AI Desk Guide

**AI Desk Guide**는 사용자의 책상 이미지를 분석하여 인체공학적 피드백을 제공하는 AI 기반 데스크테리어 솔루션입니다.  
YOLOv8 객체 인식과 GPT 분석을 결합해 사용자의 자세와 환경을 과학적으로 진단하고, 맞춤형 개선 가이드를 제공합니다.

---

## 📘 프로젝트 개요

| 항목 | 내용 |
|------|------|
| 🎯 목표 | 사용자의 책상 환경을 AI로 분석하여 인체공학적 개선 가이드 제공 |
| 🧠 주요 기술 | YOLOv8 (Roboflow), Streamlit, GPT-4, Python |
| 📅 개발 기간 | 2025.09.18 ~ 2025.10.23 |
| 👥 팀 구성 | 심령하 (),  () 외 |

---

## 💡 주요 기능

1. **객체 인식 (YOLOv8)**
   - 책상 이미지에서 `monitor`, `keyboard`, `mouse`, `wrist rest`, `lamp` 등 탐지  
   - Roboflow API를 통해 실시간 추론

2. **인체공학 분석 (ErgonomicsAnalyzer)**
   - 사용자 키, 성별, 모니터 인치 등을 바탕으로 이상적 모니터 높이 계산  
   - 실제 높이와 비교하여 `Good`, `Moderate`, `Severe` 등 진단

3. **개인 맞춤 피드백 (GPT 기반)**
   - 탐지 결과를 문장 형태로 요약하여, 사용자에게 “가이드 문장”으로 제공  
   - 예: *“모니터가 이상 높이보다 6cm 낮습니다. 받침대를 추가해보세요.”*

4. **웹 인터페이스 (Streamlit)**
   - 이미지 업로드 → 분석 → 결과 리포트 확인까지 한 번에

---

## 🖼️ 예시 결과

| 업로드 이미지 | 분석 결과 |
|----------------|-------------|
| ![input](images/sample_desk.jpg) | ![output](images/sample_result.jpg) |

---

## ⚙️ 실행 방법

### 1️⃣ 환경 설정
```bash
git clone https://github.com/<your-username>/AI-Desk-Guide.git
cd AI-Desk-Guide
pip install -r requirements.txt
