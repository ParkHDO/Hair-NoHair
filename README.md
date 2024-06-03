# Hair-NoHair
## 탈모 데이터셋을 활용한 Native APP이다.
 프로그램은 탈모 데이터셋을 활용해 탈모인지 아닌지를 판명해주는 프로그램이다.

* 이 코드는 PyQt5와 YOLOv5 모델을 사용하여 웹캠에서 실시간 객체 탐지와 이미지를 불러와서 객체 탐지를 수행하는 GUI 애플리케이션을 구현한 것입니다.
* 필요한 라이브러리와 모듈을 임포트합니다. window_yolo_ui는 PyQt5 디자이너로 생성된 UI 레이아웃 파일을 포함합니다.
* 탐지된 객체의 클래스를 저장하는 리스트입니다. 여기서는 두 가지 클래스(hair와 no-hair)가 있습니다.
* QMainWindow를 상속받은 MainWindow 클래스를 정의합니다. 초기화 메서드에서는 UI 설정과 창 제목을 설정합니다.
* GPU가 있으면 GPU를 사용하고, 없으면 CPU를 사용하도록 설정합니다. YOLOv5 모델을 로드하고, 로드에 실패하면 프로그램을 종료합니다.
* 0.5초마다 프레임을 읽어오는 타이머를 설정하고 시작합니다. 웹캠을 열고, 웹캠을 열지 못하면 프로그램을 종료합니다.
* 버튼 클릭 이벤트를 load_image 함수에 연결합니다. loaded_image 변수는 불러온 이미지를 저장하고, file_dialog_open 변수는 파일 다이얼로그의 상태를 추적합니다.
* OpenCV 이미지를 PyQt에서 사용할 수 있는 QImage로 변환합니다.
* 웹캠에서 프레임을 읽어와 YOLO 모델로 객체 탐지를 수행합니다. 탐지된 객체는 detections에 저장되고, 신뢰도가 높은 상위 2개의 객체 정보를 UI에 표시합니다.
* 파일 다이얼로그를 열어 이미지를 선택하고, 선택한 이미지를 loaded_image 변수에 저장합니다.
* PyQt5 애플리케이션을 실행합니다. MainWindow 객체를 생성하고 보여줍니다.
