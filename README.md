## 페트병 분리배출을 위한 YOLOv7 기반 자동 분류 시스템(YOLOv7 Based Automatic Classification System for Separate Discharge of PET Bottles)

#### 2022-11-22 최초 Update

-------------------------------------
### ▶Introduction
> [1] 가장 최근에 발표된 YOLOv7 model을 이용해 페트병 검출 후 크롭 이미지로 저장(경계상자 기준)
> 
> [2] YOLOv7 model을 이용해 라벨 및 뚜껑 검출 후 해당 부분을 배경 색상 정보를 가져와 삭제함(k=2인 color clustering 성능 향상 목적)
> 
> [3] Color Clustering 기법을 이용해 음료와 페트병을 k=2, 즉 이진 분류함
> 
> [4] 페트병 1개를 기준으로 이미지 상단에 한글로 작성된 페트병 분류 피드백을 입력해 결과를 반환함
> * A. 빈 페트병 + 라벨 있음
> * B. 빈 페트병 + 라벨 없음  => 정상 분리배출 가능
> * C. 음료가 있는 페트병 + 라벨 있음
> * D. 음료가 있는 페트병 + 라벨 없음

-------------------------------------
### ▶ Experimental Environment
> [1] Python 3.8.13
> 
> [2] Pytorch 1.11.0
>
> [3] GPU NVIDIA GeForce RTX 3060

-------------------------------------
### ▶ Precautions
> YOLOv7 기반 환경이 설정되어 있어야합니다.
> 
> Yolov7을 용도에 맞게 수정했습니다.(Crop image 생성, Background color정보를 가져와 Detection 부분에 입힘)



### 
※ 전남대학교 Energy+AI 핵심인재양성 교육단에서 주최한 2022 동계 마이크로캡스톤디자인대회에 참여한 결과물입니다.
