이미지를 마치 만화처럼 보이도록 변환해주는 Python 프로그램

## 주요 기능
- 이미지의 노이즈를 제거하여 부드럽게 처리 <br>
- 그레이스케일 및 블러 처리로 에지를 강조 <br>
- Adaptive Thresholding을 사용한 선명한 윤곽선 검출<br>
- 컬러 이미지와 에지를 결합해 만화 효과 구현<br>
- 결과 이미지를 시각적으로 확인 및 저장 가능<br>

## 사용 기술
- OpenCV (cv2)<br>
- NumPy (np)<br>
- bitwise_and, cvtColor, Bilateral Filter, Median Blur, Adaptive Threshold, Morphological Transformations

## 결과

### good
![image](https://github.com/user-attachments/assets/7f457189-6e11-4db6-a63f-9ad671491f64)
### bad
![image](https://github.com/user-attachments/assets/f501ee01-9346-4bfd-92de-574f70d6c879)


## 한계점
조명 의존성
Adaptive Threshold는 밝기 차이에 민감하여, 그림자나 빛의 변화가 많은 이미지에서는 윤곽선이 과하게 검출되거나 손실됨.

색상 분리 한계
Bilateral Filter는 색상 영역을 부드럽게 만들지만, 색상 차이가 적은 영역은 만화 느낌이 덜하게 표현됨.

복잡한 배경에 취약
윤곽선이 많아질수록 원래 물체가 왜곡되며, 결과적으로 어지럽고 불분명한 만화 이미지가 생성됨.

모든 이미지에 통일된 파라미터 적용
blockSize, C 값은 이미지의 특성에 따라 조절이 필요한데, 고정된 값만 사용하면 일부 이미지에는 적합하지 않음.

실시간 적용 불리
Bilateral filter와 adaptive threshold는 연산량이 많아 대용량 이미지 또는 영상에는 처리 속도가 느림.
