# Jarvis Morning Briefing

자비스가 매일 아침 06:00 (KST)에 자동 발행하는 개인 모닝 브리핑.

## 🌐 Live URL
- **최신**: https://jarvis-briefing.pages.dev/
- **과거 호**: https://jarvis-briefing.pages.dev/archive/YYYY-MM-DD.html

## 📰 구성
- **Masthead**: Jarvis Morning Briefing · Issue No · Live from Seoul
- **Ticker**: Total Tasks / Yesterday Commits / Wiki Pages / Systems Status
- **Section A**: Today's Priorities — 단기 할 일
- **Insight of the Day**: 3개 인사이트 (Medium 다이제스트 카드 스타일)
- **Section B**: Editor's Picks — 어제 활동 기반 추천 3선
- **Section C**: Yesterday in Review — git 활동
- **Section D-E**: Outlook / Horizon — 중기·장기 할 일
- **Section F**: Systems Status — 네네 + Channel Master 헬스

## 🛠️ 자동화
PowerShell 스크립트가 매일 06:00 (Task Scheduler):
1. 데이터 수집 (할-일-모음, git log, nene-health, Channel Master)
2. 인사이트/추천 HTML 파일 읽기
3. HTML 생성
4. 텔레그램 첨부 + Cloudflare Pages 자동 배포
5. nene-health 다음 회차용 갱신

스크립트: `Jarvis-llm-wiki/.claude/scripts/morning-briefing-html.ps1`

## 🎨 디자인
- Editorial newspaper masthead + Medium digest 카드 하이브리드
- Mobile-first, 768px+ 가로 카드 레이아웃
- Playfair Display + Source Serif 4 + Noto Serif KR + IBM Plex Mono
- 종이색 #fafaf7 + Editorial Red #c41e3a 액센트
