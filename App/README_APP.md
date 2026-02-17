# ReportMaker GUI 앱

노트북(rmv5.ipynb)을 기반으로 한 독립 실행형 프로그램입니다.

## 실행 방법

1. **의존성 설치**
   ```bash
   pip install -r requirements.txt
   ```

2. **API 키 설정**  
   프로젝트 폴더에 `.env` 파일을 만들고 다음 한 줄을 넣습니다.
   ```
   GEMINI_API_KEY=여기에_키_입력
   ```
   또는 시스템 환경 변수 `GEMINI_API_KEY`에 키를 설정해도 됩니다.

3. **GUI 실행**
   ```bash
   python report_maker_gui.py
   ```

4. **동작 순서**
   - 시작 시 입력 창: 보고서 제목, 목적, 서술방식(줄글형/Bullet 항목형), Gemini 모델(Flash/Pro), 요구사항
   - [다음: 목차 생성] → 목차 자동 생성
   - 생성된 목차 확인 후, 필요 시 "목차 수정 지시"에 수정 요청 입력 후 [반영]
   - [보고서 생성] → 본문 생성 후 DOCX 파일이 **내 PC → 다운로드** 폴더에 저장됨

---

## .exe로 만들기 (PyInstaller)

1. PyInstaller 설치
   ```bash
   pip install pyinstaller
   ```

2. 실행 파일 생성 (콘솔 창 없이 GUI만 띄우기)
   ```bash
   pyinstaller --onefile --windowed --name ReportMaker report_maker_gui.py
   ```
   - `dist/ReportMaker.exe` 가 생성됩니다.
   - `.env` 파일은 exe와 **같은 폴더**에 두거나, 환경 변수로 `GEMINI_API_KEY`를 설정해야 합니다.

3. (선택) 아이콘 지정
   ```bash
   pyinstaller --onefile --windowed --icon=report.ico --name ReportMaker report_maker_gui.py
   ```
