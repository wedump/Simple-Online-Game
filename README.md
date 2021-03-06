# Simple-Online-Game TO DO LIST

### Server Mock 객체 개발
- 우선 Player 1 기준으로, 기존 스스로 액션하던 방식에서 서버에 업데이트하고 데이터를 받아 액션을 취하는 방식으로 변경
- Player 1, 2가 공통적으로 페인터를 교체하고 액터를 할당받는 함수 별도 개발
- **완료**

### Mock Server를 통해 Player 2가 임의로 행동해야 함
- Palyer 2가 좌우로 움직이도록 임시 지정
- **완료**

### 초기 진입화면 개발 (아이디 입력, 방 개설, 방 선택)
- 초기 진입화면 없이, GAME URL로 바로 접근하며, ROOM ID는 고정, UID는 서버에서 생성하여 관리
- 인원 초과 시 접근 못하도록 막고, 메시지 알림
- **완료**

### Server API 개발 (data, register, update, exit)
- 나가기 버튼용 API exit 추가 개발
- **완료**

### 서버와 클라이언트 간 연동
- 이동 연동 완료
- XMLHttpRequest 객체가 싱글톤 이어서 크롬에서 서버의 update API 호출 시 요청을 취소하는 버그 -> 해결
- 스프라이트 인덱스, 기존 방에 진입해 있던 상대방 플레이어 현재위치 싱크해야 함 -> 해결
- 위치 싱크가 불일치하는 버그 -> 해결
- 간혹 키업 시에 상대방 화면에서 플레이어가 멈추지 않는 버그 -> 해결
- 버그 해결 후 이동이 부자연 스러운 면이 있음 -> 해결
- WebSocket을 적용하여 느림과 부자연 스러운 움직임 해결
- **완료**

### 4방향 공격 스프라이트 이미지 개발 및 적용
- Player 2 의 색상은 Canvas 이미지 픽셀 데이터 조작으로 처리
- **완료**

### 스테이지 외곽과 캐릭터 간 충돌처리
- 직사각형 바운싱 영역으로 처리
- **완료**

### 캐릭터 간 충돌처리
- 직사각형 바운싱 영역으로 처리
- **완료**

### 공격 충돌처리
- 공격용 바운싱 영역으로 별도 처리
- 캐릭터에 공격상태와 에너지 데이터 값 추가
- 서버에서 에너지 관리
- 공격당한 표시의 경우 painter에서 alpha값을 줄여 처리
- **완료**

### WebSocket Server 직접 개발
- **완료**
