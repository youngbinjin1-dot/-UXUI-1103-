# 디자인 md 형식 (steam.md · userverse.md 공통)

## Frontmatter
```yaml
brand / brand_ko / slug / generated / source_type / confidence / is_official
region / industry[]
color_tone / primary_color_hex / primary_color_name / mood[]
font_category / font_primary / font_korean_supported
density / corner_style / flatness
visual_style[] / theme_modes[]
released_year / last_major_revision
signature_keyword: "한 줄 시그니처"
hero_html: |   # 이 스타일을 보여주는 작은 HTML 조각
sources[]
```

## 본문 ①~⑫
1. **브랜드 DNA** — 이름, 한 줄 정체성, 철학, 시그니처 요소 1개
2. **톤 & 무드** — 키워드 3개, 무드 설명, 비주얼 스타일, 밀도, 모서리, 평면성
3. **컬러 시스템** — CSS 변수(primary 단계, neutral 단계, semantic, surface, text, border)
4. **타이포그래피** — 폰트 페어링(출처·라이선스), 렌더링 주의, 위계(크기/행간)
5. **스페이싱** — base unit, 토큰, 모바일 레이아웃 규칙, 화면 골격
6. **모서리** — 규칙과 금지(예: 직각 + 끊김 없는 테두리)
7. **Depth** — 그림자/안쪽 음영/외곽선 토큰
8. **Iconography & Graphic** — 아이콘 그리드, 그래픽 모티프, 장식 사용 규칙
9. **컴포넌트 가이드** — 상태표 + CSS (Field, Quest Chip, Warning Bubble, Dice, Country Select, Button, Toggle, Gauge, Notice, Completion)
10. **Motion & Sound** — duration/ease 토큰, 이벤트별 사운드 표
11. **Anti-patterns** — 5~7개 금지 규칙
12. **시그니처 적용 예시** — 바로 붙여 넣어 볼 수 있는 HTML+CSS

## 레퍼런스 이미지에서 뽑는 순서
1. 배경색(가장 넓은 면) → `bg/base`, 한 단계 어둡게 `bg/page`
2. 강조색(그래픽 색) → `primary-500`, 밝게 300 / 어둡게 700 / 14% 틴트
3. 글자색 → 흰색 계열 3단계
4. 오류·성공 → 강조색과 색상(hue)이 충분히 떨어진 색 (핑크면 레드오렌지·민트)
5. 폰트 → 레퍼런스 타이틀 느낌(둥근 사각, 픽셀 등)과 한글 지원 여부
6. 모티프 → 반복되는 도형(픽셀 별, 궤도 링, 스트라이프 등)을 화면당 1~3개만
