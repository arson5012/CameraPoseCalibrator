# Camera Pose Calibrator

* #### 💡 개요
  * 카메라가 회전되거나 기울어진 상태에서 설치되었는지 확인하고, 이를 보정할 수 있도록 돕는 프로그램  
    사용자는 카메라의 상태(물리적인 설치 상태)에 대해 빠르게 피드백을 받아볼 수 있으며, 현재 카메라의 설치 상태를 검증 가능
    
  * 이미지 사이즈, FOV(Field of View), WD(Working Distance) 을(를) 알고있을 때  
    카메라 행렬(Camera Matrix)을 계산하여 카메라의 자세(Roll, Pan, tilt)를 계산하여 표시   
   
* #### 🌍 환경 & 호환성  
  * OS:	MS Windows 10 ~
  * Language : C++ 11 ~
  * Opencv version : 4.8.0 ~
---

* #### 주요 기능 및 특징
  * Camera Matrix 계산   
    카메라의 사양 중 이미지 크기, FOV, WD 등의 데이터를 입력하여 카메라 행렬을 계산하며  
    이 행렬은 카메라의 좌표계를 설정하고, 이후 자세 추정에 필요한 기초 데이터를 제공    

  * Camera Pose Estimation  
    앞서 계산한 Camera Matrix를 활용해 3D 공간에서 카메라의 위치와 방향을 추정하며    
    이를 통해 카메라가 올바른 각도로 설치되었는지 확인 및 자세 보정에 필요한 정보를 제공    

  * Calibration Guide Box  
    카메라의 FOV와 WD를 기반으로 가이드 상자를 표시하여 설치 위치와 각도를 빠르게 조정할 수 있도록 도와주며  
    이를 통해 초기 설정 시간 절약 및 카메라 설치 상태를 1차로 확인 가능  

* #### 설치 및 실행 방법
  * <a href="https://github.com/arson5012/CameraPoseCalibrator/releases/download/Release_v1.0a/CPC_Installer.exe" target="_blank">
    <img class="img-concert" src="https://github.com/user-attachments/assets/ff1571e5-c315-434e-8b1e-5c65818e2025"/> </a> 파일을 실행하여 [CPC] 폴더 내의 Camera Pose Cailbrator.exe를 더블클릭하여 실행  
  </br>  
  
  > ![image](https://github.com/user-attachments/assets/84f74990-7da0-4faf-9459-2fc405a1a92f)
  <details><summary>">" 버튼을 눌러서 카메라 정보가 일치하는지 확인한다.</summary>카메라 정보가 일치하지 않는다면 NEW 버튼을 눌러 새로 만들거나</br>SEL 버튼을 눌러 기존의 파일을 불러와 적용하거나</br>EDIT 버튼을 눌러 현재 적용된 파일의 정보를 수정 후 적용할 수 있다.</br></details>  
  
  * LOAD 또는 LIVE 버튼을 눌러 체커보드를 불러오고  
    체커보드 속성을 각각의 EditCtrl에 입력한 후 Processing 버튼을 눌러 결과를 얻는다.

* #### 그 밖의 기능  
1. LIVE, VIDEO 영상에서 이미지를 GRAB 할 수 있는 기능
2. 체커보드 속성과 카메라의 구성 정보에 따라 체커보드를 생성/저장 할 수 있는 기능
3. GML Calibration Tool 과 동일한 형식으로 카메라 캘리브레이션 정보를 내보내는 기능
