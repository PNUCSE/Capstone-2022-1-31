# Capstone-2022-1-31
## Wi-SUN Mesh 네트워크를 이용한 주차공간찾기 시스템 구축

### 프로젝트 목적
 이 프로젝트를 통해 현재 도시에서 발생하는 교통 문제중 하나인 주차 문제를 해결하고자 한다. 현재 주차장의 주차현황을 실시간으로 보여주어 주차장 이용과 탐색에 소모되는 시간을 줄이고 불법주차 문제 해결에 도움을 줄 수 있도록 한다.

### 팀원 및 역할
김정수 : 드라이버 구현<br/>
최재원 : 앱 개발<br/>
서경우 : 서버 및 DB 구축<br/>


### 구성도
![구성도](https://user-images.githubusercontent.com/88094303/195519466-63485603-a387-4c5a-863f-544bcef53ae8.png)
 각 주차공간마다 3가지센서를 통해 주차현황을 파악하고, 각 자리에 있는 Wi-SUN 모듈이 정보를 수집하여 주차장마다 있는 Gateway 모듈로 전달한 뒤 서버를 통해 DB에 저장하여 전체 주차장 데이터를 관리한다.
 
### 사용법
 1, 아두이노 : 아두이노 코드에 나온 핀번호에 맞게 회로 구성을 하면 센서 데이터를 받아올 수 있음. 조도센서의 저항은 10K옴 사용.<br/>
 2, 모듈 드라이버 : 모듈에 들어가는 펌웨어 코드를 보안상 업로드 하지 못하여 따로 구현한 드라이버만 업로드 함.<br/>
 3, UDP서버 : nodejs로 구현하였고, 터미널 창에 node udp_server를 치면 미리 설정한 포트로 온 데이터를 읽는다.<br/>
 4, DB : wampserver라는 프로그램으로 DB를 생성하고 UDP서버와 앱과 연동됨.<br/>
 5, App : 아래 이미지 속 기능 외에 즐겨찾기, 검색기록 확인 등 여러 기능이 있음.<br/>
 ![AppUI](https://user-images.githubusercontent.com/88094303/195768493-96ddf814-ad19-4f03-b85a-711aadff4cf7.png)
 
 ### 프로젝트 설명 영상 링크
 [![프로젝트 소개](https://img.youtube.com/vi/FgYEQUiT0v8/0.jpg)](https://www.youtube.com/watch?v=FgYEQUiT0v8)
