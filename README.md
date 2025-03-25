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
- Bilateral Filter, Median Blur, Adaptive Threshold, Morphological Transformations


## 문제점
같은 jpg 확장자 파일임에도 로딩되지않는 이미지들이 다수 존재했다
