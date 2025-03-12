# KT_AIVLE_MINI_PROJECT_4

# 얼굴 인식 기반 출입 시스템

이 프로젝트는 얼굴 인식 기술을 활용하여 실시간 출입 시스템을 구현하는 것을 목표로 합니다. 이를 통해 기존 출입 카드 방식에서 발생하는 대기 시간을 줄이고, 효율적인 출입 절차를 제공합니다.


## 프로젝트 정보

- **주제**: 얼굴 인식
- **데이터**: 유명인 얼굴 데이터 및 개인 얼굴 데이터
- **데이터 출처**:  
  - [LFW Dataset (Kaggle)](https://www.kaggle.com/datasets/jessicali9530/lfw-dataset)  
  - [Face Recognition Dataset (Roboflow Universe)](https://universe.roboflow.com/new-workspace-kuixc/face-recognition-dataset/dataset/1)  
  - [Test Dataset (Roboflow Universe)](https://universe.roboflow.com/td-vgaen/test-uiodm/dataset/2)
- **데이터 구분**: 이미지 데이터 (Image)
- **중점 사항**:
  1. 데이터 전처리 및 Keras를 이용한 학습 및 추론
  2. 데이터 전처리 및 YOLO를 이용한 학습 및 추론

## 프로젝트 개요

### 배경 및 문제점
- **문제점**: 출퇴근 시간 및 점심 시간과 같이 사원의 출입이 많은 경우, 기존 카드 태그 방식으로 인해 긴 대기 시간이 발생.
- **해결책**: 고속도로 하이패스와 유사한 실시간 얼굴 인식 모델을 도입하여 대기 시간을 줄이고 출입 과정을 효율화.


## 프로젝트 진행 단계

### 1일차
#### STEP 1: 데이터셋 준비 및 전처리
- **데이터셋 준비**: 개인 얼굴 이미지 파일 수집 및 제공된 얼굴 이미지 파일 활용.
- **데이터 전처리**: Keras의 이미지 처리 함수 사용.

#### STEP 2: FaceNet 모델 생성
- **모델 구조 생성**: FaceNet 모델은 (160, 160) 크기의 이미지를 입력받아 128차원의 벡터를 출력.
- **구조 추가**: FaceNet 모델을 기반으로 추가 학습을 진행.

#### STEP 3: 모델 저장 및 추론
- **사전 학습 모델**: FaceNet 사용 또는 독창적인 모델 생성.
- **저장 및 로드**: .keras 파일로 저장 후, 로컬 py 파일에서 불러와 동작 확인.


### 2일차
#### STEP 1: YOLO 데이터셋 준비 및 전처리
- **데이터셋 준비**: 개인 이미지와 제공 이미지 파일 활용.
- **YOLO 데이터 구조**: UltraLytics YOLO-cls 모델에 맞게 데이터셋 구조 조정.

#### STEP 2: YOLO 모델 학습 및 저장
- **모델 선택**: UltraLytics YOLO-cls 사용.
- **학습 및 저장**: 학습 완료 후 .pt 파일로 저장 및 로컬 py 파일에서 확인.


### 3일차
#### STEP 1: 데이터 수집 및 Annotation
- **이미지 수집 및 라벨링**: Roboflow, CVAT 등 온라인 툴 또는 로컬 Ybat-master 사용.
- **Augmentation**: 이미지 다양화를 통해 데이터셋 확장.

### 4일차
#### STEP 2: YOLO 데이터 전처리 및 학습
- **YAML 파일 생성**: 데이터 구조를 YAML 파일에 저장.
- **YOLO 모델 학습**: UltraLytics YOLO로 학습 후 .pt 파일 저장 및 추론.


### 5일차
#### STEP 1 ~ 3: 모델 개선 및 성능 확인
- **모델 개선**: Keras 및 YOLO 모델 구조 변경, 하이퍼파라미터 튜닝.
- **실성능 확인**: 로컬 Cam에서 다양한 조건에서 성능 측정.
- **결과 정리**: PPT로 시각화 및 발표 준비.
<img width="766" alt="Image" src="https://github.com/user-attachments/assets/84041fb0-3037-4797-8327-8e1b3f85e6e9" />

## 참고 자료
- [FaceNet 논문](https://arxiv.org/abs/1503.03832)
- [UltraLytics YOLO Documentation](https://docs.ultralytics.com/)

