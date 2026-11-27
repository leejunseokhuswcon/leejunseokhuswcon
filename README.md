# 소프트웨어 개발 포트폴리오

웹 인터랙션, AI 백엔드, 임베디드 제어를 개발합니다. 프로젝트별로 핵심 설계와 구현 범위를 정리했습니다.

## 대표 프로젝트

### Hyper-AutoPark-Rover · 자동 주차 로버 팀 프로젝트

**담당** · 카메라 인식, 전면 주차 제어, 자율 주차 상태 흐름 통합

- **마커 인식** · OpenCV로 ArUco 마커 검출 모듈을 구현하고, 웹캠 테스트 앱에서 마커 ID와 중심 오차를 확인했습니다. [PR #13](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/13) · [병합 코드 변경](https://github.com/yumina0616/Hyper-AutoPark-Rover/commit/07cb8080ca992f6f3a3bd070543ed8b9edcb0c26)
- **정지 판단** · 전면 주차의 정렬·접근·완료 상태를 분리했습니다. 새 카메라 프레임과 새 거리 측정값이 모두 들어올 때만 정지 조건을 갱신하며, 상태 전이 시나리오 8개를 단위 테스트로 확인했습니다. [PR #24](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/24) · [병합 코드 변경](https://github.com/yumina0616/Hyper-AutoPark-Rover/commit/ddc48cb0dd36536f07fa9aa7311d9d1aab52695a)
- **주차 흐름 통합** · 비콘 탐색부터 마커 정렬·전면 주차까지 연결하고 장애물·센서 오류·시간 초과 시 중단하도록 구현했습니다. PR에 자동 테스트 결과와 실물 주행의 미검증 범위를 기록했습니다. [PR #27](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/27) · [병합 코드 변경](https://github.com/yumina0616/Hyper-AutoPark-Rover/commit/352a3d2b0f8abc63aa5a30f04f00ed2e21212b23)

**Python · OpenCV · Arduino UNO Q**

### ARISE · 학교 소방안전 훈련

학생이 소화기 탐색·진압·대피를 연습하는 웹 프로토타입입니다. 27개 화면을 데이터로 관리하고, 미션 상태에 따라 다음 조작을 허용하는 방식으로 훈련 흐름을 구현했습니다. 브라우저에서 세 미션의 시작부터 완료까지 확인했습니다.

**JavaScript · Pointer Events · GitHub Pages** · [웹 데모](https://leejunseokhuswcon.github.io/ARISE/) · [구현과 검증 기록](https://github.com/leejunseokhuswcon/ARISE)

[![ARISE 시작 화면과 소화기 탐색·진압·대피 미션](https://raw.githubusercontent.com/leejunseokhuswcon/ARISE/main/docs/images/arise-overview.jpg)](https://github.com/leejunseokhuswcon/ARISE)

### StayPet · AI 반려동물 라이프 시뮬레이션

반려동물 사진으로 캐릭터를 생성하는 백엔드 PoC입니다. FastAPI와 워커가 요청 접수와 생성 처리를 나누고, 모의 생성기와 실제 생성기가 같은 API 계약을 사용합니다. 업로드와 생성 작업을 확인하는 테스트가 저장소에 있습니다.

**Python · FastAPI · PostgreSQL** · [프로토타입과 API 문서](https://github.com/leejunseokhuswcon/staypet) · [테스트 코드](https://github.com/leejunseokhuswcon/staypet/tree/main/backend/tests)

### Q-Rover Study · 거리 센서와 카메라를 결합한 로버

Arduino UNO Q 실습에서 카메라 객체 인식은 MPU에, 거리 판정과 모터 정지는 MCU에 두었습니다. 두 입력 중 하나가 장애물을 감지하면 제동하며, 각 입력을 독립적으로 확인하는 시연 조건을 문서화했습니다.

**Arduino UNO Q · C++ · Python** · [제어 구조와 실습 가이드](https://github.com/leejunseokhuswcon/q-rover-study)

## 공개 기여 기록

[작성한 공개 PR 전체](https://github.com/search?q=is%3Apr+is%3Apublic+author%3Aleejunseokhuswcon&type=pullrequests)와 저장소별 기본 브랜치의 작성자 필터를 연결했습니다.

| 저장소 | 코드 변경과 PR | 작성자별 커밋 기록 |
| --- | --- | --- |
| Hyper-AutoPark-Rover | [#13 마커 인식](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/13) · [#24 전면 주차 정지](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/24) · [#25 main 동기화](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/25) · [#27 주차 흐름 통합](https://github.com/yumina0616/Hyper-AutoPark-Rover/pull/27) | [커밋 보기](https://github.com/yumina0616/Hyper-AutoPark-Rover/commits/main/?author=leejunseokhuswcon) |
| ARISE | [웹 프로토타입](https://github.com/leejunseokhuswcon/ARISE/commit/3fe00d3e5c95693b752a3cce14f6e48581d9d69c) · [GitHub Pages 배포](https://github.com/leejunseokhuswcon/ARISE/commit/fb2b5cf5683106621c2470b102119cde46cedb68) | [커밋 보기](https://github.com/leejunseokhuswcon/ARISE/commits/main/?author=leejunseokhuswcon) |
| StayPet | [캐릭터 생성 API·워커·테스트 초기 구현](https://github.com/leejunseokhuswcon/staypet/commit/afe8c301098801135bfb37ad8961f9055a9fa7fc) | [커밋 보기](https://github.com/leejunseokhuswcon/staypet/commits/main/?author=leejunseokhuswcon) |
| Q-Rover Study | [1차시 모터 구동](https://github.com/leejunseokhuswcon/q-rover-study/commit/5cb1e6ef5c233eb1222e2d788fc6c596a20ccf38) · [2차시 센서·비전 통합](https://github.com/leejunseokhuswcon/q-rover-study/commit/d853a5b0e4fe947fc31317a96406584642c43647) | [커밋 보기](https://github.com/leejunseokhuswcon/q-rover-study/commits/main/?author=leejunseokhuswcon) |
| hello-world | [#1 README 실습](https://github.com/leejunseokhuswcon/hello-world/pull/1) | [커밋 보기](https://github.com/leejunseokhuswcon/hello-world/commits/main/?author=leejunseokhuswcon) |
