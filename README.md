# 소프트웨어 개발 포트폴리오

웹 인터랙션, AI 백엔드, 임베디드 제어를 개발합니다. 프로젝트별로 핵심 설계와 구현 범위를 정리했습니다.

## 대표 프로젝트

### ARISE · 학교 소방안전 훈련

학생이 소화기 탐색·진압·대피를 연습하는 웹 프로토타입입니다. 27개 화면을 데이터로 관리하고, 미션 상태에 따라 다음 조작을 허용하는 방식으로 훈련 흐름을 구현했습니다. 브라우저에서 세 미션의 시작부터 완료까지 확인했습니다.

**JavaScript · Pointer Events · GitHub Pages** · [웹 데모](https://leejunseokhuswcon.github.io/ARISE/) · [구현과 검증 기록](https://github.com/leejunseokhuswcon/ARISE)

[![ARISE 시작 화면과 소화기 탐색·진압·대피 미션](https://raw.githubusercontent.com/leejunseokhuswcon/ARISE/main/docs/images/arise-overview.jpg)](https://github.com/leejunseokhuswcon/ARISE)

### Hyper-AutoPark-Rover · 자동 주차 로버 팀 프로젝트

ArUco 마커 검출 모듈과 웹캠 테스트 앱을 구현하고, 비콘 탐색부터 전면 주차까지 상태 흐름을 통합했습니다. 각 변경의 구현 내용, 테스트 결과, 실물 검증 범위는 병합된 PR에서 확인할 수 있습니다.

**Python · OpenCV · Arduino UNO Q** · [ArUco 검출 PR](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/13) · [상태 흐름 통합 PR](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/27)

### StayPet · AI 반려동물 라이프 시뮬레이션

반려동물 사진으로 캐릭터를 생성하는 백엔드 PoC입니다. FastAPI와 워커가 요청 접수와 생성 처리를 나누고, 모의 생성기와 실제 생성기가 같은 API 계약을 사용합니다. 업로드와 생성 작업을 확인하는 테스트가 저장소에 있습니다.

**Python · FastAPI · PostgreSQL** · [프로토타입과 API 문서](https://github.com/leejunseokhuswcon/staypet) · [테스트 코드](https://github.com/leejunseokhuswcon/staypet/tree/main/backend/tests)

### Q-Rover Study · 거리 센서와 카메라를 결합한 로버

Arduino UNO Q 실습에서 카메라 객체 인식은 MPU에, 거리 판정과 모터 정지는 MCU에 두었습니다. 두 입력 중 하나가 장애물을 감지하면 제동하며, 각 입력을 독립적으로 확인하는 시연 조건을 문서화했습니다.

**Arduino UNO Q · C++ · Python** · [제어 구조와 실습 가이드](https://github.com/leejunseokhuswcon/q-rover-study)
