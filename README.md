# 밀집지역 위험 알림 AI 프로젝트

카메라에서 들어오는 영상에서 특정 면적안의 사람 인식 및 인원수 파악 
인원수와 면적을 이용하여 계산하여 밀집도 계산
밀집도 단계별 알림
알림 방법 : 화면 표시, 문자 전송
- 1단계(Normal) 
   - 일반 단계, 밀집도 0 ~ 3 / ㎡
- 2단계 (Caution) 
   - 일반 단계, 밀집도 3 ~ 5 / ㎡
- 3단계 (Warning)
   - 일반 단계, 밀집도 5 / ㎡ 이상
   
<img src='data/output.jpg'>


## Ultralytics YOLOv8 모델 

### 개요
YOLOv8 is the latest iteration in the YOLO series of real-time object detectors, offering cutting-edge performance in terms of accuracy and speed. Building upon the advancements of previous YOLO versions, YOLOv8 introduces new features and optimizations that make it an ideal choice for various object detection tasks in a wide range of applications.
<img src='https://github.com/ultralytics/docs/releases/download/0/yolov8-comparison-plots.avif'>

#### 주요 기능
Advanced Backbone and Neck Architectures: YOLOv8 employs state-of-the-art backbone and neck architectures, resulting in improved feature extraction and object detection performance.
앵커 프리 스플릿 Ultralytics 헤드: YOLOv8 앵커 프리 스플릿 Ultralytics 헤드를 채택하여 앵커 기반 접근 방식에 비해 더 나은 정확도와 효율적인 탐지 프로세스에 기여합니다.
최적화된 정확도-속도 트레이드오프: 정확도와 속도 간의 최적의 균형을 유지하는 데 중점을 둔 YOLOv8 은 다양한 애플리케이션 영역의 실시간 물체 감지 작업에 적합합니다.
다양한 사전 학습 모델: YOLOv8 에서는 다양한 작업 및 성능 요구 사항을 충족하는 다양한 사전 학습 모델을 제공하므로 특정 사용 사례에 적합한 모델을 쉽게 찾을 수 있습니다.

#### [COCO dataset 특징]
ImageNet dataset의 문제점을 해결하기 위해 2014년 제안되었습니다. COCO dataset은 다양한 특징은 다음과 같습니다.

 다양한 크기의 물체가 존재하며 높은 비율로 작은 물체들이 존재합니다. 
또한, 덜 iconic합니다. 즉, 이미지가 특정 카테고리에 명확하게 속해있지 않다는 의미입니다.
80개의 classes가 있습니다.
" person bicycle car motorcycle airoplane bus train truck boat traffic light fire hydrant stop sign parking meter bench bird cat dog horse sheep cow elephant bear zebra giraffe backpack umbrella handbag tie suitcase frisbee skis snowboard sports ball kite baseball bat baseball glove skateboard surfboard tennis racket bottle wine glass cup fork knife spoon bowl banana apple sandwich orange broccoli carrot hot dog pizza donut cake chair sofa potted plant bed dining table toilet tv laptop mouse remote keyboard cell phone microwave oven toaster sink refrigerator book clock vase scissors teddy bear hair drier toothbrush " 
