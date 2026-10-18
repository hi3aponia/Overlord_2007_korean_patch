1. 개요
대상 게임: Overlord 1 (2007) PC (Steam / GOG / 패키지판 공통)
패치 버전: v1.0_F (최종 정식 배포본)
번역 범위: 스토리, 퀘스트, 인게임 UI/HUD, 튜토리얼, 시스템 설정기, 폰트 100% 한글화
2. 원본 대비 변경 및 패치된 파일 상세 내역
경로 및 파일명	원본 대비 변경 사항	세부 내용
Language\*.8ld
(총 41개 파일)	수정 (암호화 재패키징)	• Triumph 전용 M8LD 바이너리 컨테이너 복호화 후 대사 번역 및 재암호화
• 본편 33개 스토리 챕터 대사, 미니언(놀 등) 조언 대사 202종, 퀘스트 목표 158종 100% 번역
Language\Apps\
(Config.8ld, Launcher.8ld)	수정 (런처/설정 텍스트)	• 게임 실행 전 설정 도구 및 런처 인터페이스 텍스트 한글화
Language\ENGLISH\
(Overlord.TTF, Subtitle.ttf, Title.TTF)	교체 (한글 폰트 탑재)	• 유니코드 완성형 11,172자를 지원하는 고화질 한국어 TTF 폰트로 전면 교체 (인게임 HUD, 타이틀, 자막 폰트)
Language\Resources\
(system.xml, System_Quests.xml, TutorialMessages*.xml 등 5종)	수정 (시스템/조작 가이드)	• 키보드/마우스 및 XInput 게임패드 튜토리얼 팝업 가이드 전체 한글화
• 영지 및 던전명(25개 전역), 퀘스트 일지 시스템 텍스트 한글화
Resources\Interface.prp
(10,132 KB)	수정 (바이너리 컨테이너 패치)	• 메인 메뉴, 옵션 설정, 대장간, 인게임 HUD 텍스트 한글화
• [버그 픽스] '새 프로필 생성' 시 system_rpk@generic_M이 출력되던 GENERIC_MENU@OK 키 복구 완료
• 원본 파일 크기(10,374,897 Byte) 및 32비트 바이트 정렬 100% 유지
Resources\Interface Patch.prp
(733 KB)	수정	• 추가 인터페이스 UI 레이아웃 및 텍스트 패치
Resources\System.psp
(5,701 KB)	수정	• 인게임 시스템 스크립트 및 UI 상호작용 한글화 대응
Config.exe
(1,878 KB)	수정 (설정기 실행 파일)	• 원본 설정기에서 '창 모드(Windowed)' 선택 시 드롭다운이 깨지거나 비정상 작동하던 버그 수정 및 한국어 인터페이스 지원
Install_Patch.bat
installer.ps1	신규 추가 (원클릭 자동 설치기)	• Steam / GOG 설치 경로 자동 감지
• [신규] Windows GUI [찾아보기] 창 또는 직접 입력을 통한 사용자 지정 설치 폴더 선택 기능
• 패치 전 원본 자동 백업(Backup_Original_PrePatch/)
• 한글 윈도우 프로필 세이브 호환성 자동 검사 및 복구
• UTF-8 with BOM 적용으로 콘솔 글자 깨짐 방지
Restore_Original.bat
restore.ps1	신규 추가 (원클릭 복원 도구)	• 패치 이전의 깨끗한 원본 상태로 1클릭 복구 (폴더 지정 지원)
README.txt	신규 추가	• 설치 방법 및 게임 내 자막 켜기(Options -> Audio -> Subtitles On) 설정 가이드
3. 주요 한글화 및 기능 수정 요약 (GitHub Release Notes용 텍스트)
markdown
### 🎮 한글화 내용 요약
1. **스토리 및 퀘스트 대사 100% 완역**
   - 본편 전체 33개 챕터, 서브 퀘스트, NPC 대사 전면 한국어화
   - 미니언 조언가 놀(Gnarl)의 상황별 대사 202종 및 퀘스트 목표 158종 완역
2. **시스템 및 UI 100% 한글화**
   - 메인 메뉴, 옵션 설정, 대장간 제련소, 영지/던전명, 인게임 HUD
   - 키보드/마우스 및 게임패드(XBox 360/XInput) 조작 가이드 팝업 한글화
3. **고해상도 한글 전용 TTF 폰트 내장**
   - 11,172자 한글 유니코드를 온전히 지원하여 글자 깨짐 및 누락 없음
4. **버그 수정 및 안정성 향상**
   - [프로필 버그 픽스] '새 프로필 생성' 시 `system_rpk@generic_M`이 출력되던 식별자 오류 수정 (`[확인]` 버튼 복구)
   - [창 모드 픽스] `Config.exe`에서 창 모드 선택 시 글자가 깨지던 문제 수정
   - [세이브 호환성] 한글 윈도우 환경에서 프로필 생성 시 튕기던 비ASCII 세이브 경로 문제 자동 점검 및 해결
5. **편의 기능**
   - 원클릭 자동 설치 및 자동 원본 복구 지원
   - 자동 경로 감지 외 마우스로 원하는 폴더를 선택할 수 있는 폴더 찾아보기(GUI) 기능 탑재
