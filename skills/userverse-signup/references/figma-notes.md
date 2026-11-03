# Figma 제작 메모 (Figma MCP `use_figma`)

## 순서
1. `whoami` → 팀 선택 → `create_new_file` 또는 기존 파일 → `create_session`
2. `listAvailableFontsAsync()`로 폰트 확인. 원하는 한글 픽셀 폰트가 없으면 비슷한 폰트로 대신하고, **텍스트 스타일(UV/Title, UV/Body …)** 로 묶어 나중에 스타일 폰트만 바꾸면 전체가 바뀌게 한다.
3. 새 페이지 → 변수 컬렉션(컬러 + 간격) → 텍스트 스타일
4. 컴포넌트(변형 세트)
   - Input: State=Default/Focus/OK/Error, TEXT `Value`·`Counter`, BOOLEAN `Show counter`·`Show dice`·`Show eye`
   - Button: Type=Primary/Ghost/Disabled, TEXT `Label`
   - Badge: Type=OK/ERR · Quest Chip: State=Default/OK/Bad · Checkbox: State=Off/On
5. 화면(375×812): 로그인, 회원가입, 이메일 형식 오류, 가입된 이메일, 재가입 환영, 닉네임 추천, 입력 조건 오류, 모두 통과, 완료
6. 각 화면 Content 높이 합이 프레임을 넘지 않는지 수치로 확인 → 넘치면 설명 한 줄로, 간격 한 단계 줄이기
7. 전체 스크린샷 1회 + 오류 화면 확대 1회로 확인

## 함정
- `setBoundVariableForPaint`로 바인딩한 paint에 opacity를 줘도 빠질 수 있다 → 틴트(14%, 50%, 60%)는 바인딩 없는 SOLID + opacity
- 인스턴스 이름은 변형 이름이 아니다 → `instance.mainComponent.name`으로 판별
- `resetOverrides()`는 컴포넌트 속성도 초기화
- 이모지·없는 글리프는 깨진다 → SVG 아이콘
- 픽셀 아이콘은 `shape-rendering="crispEdges"` SVG를 `createNodeFromSvg`로
- 절대 위치 장식은 오토레이아웃 자식으로 넣고 `layoutPositioning='ABSOLUTE'`
- `html_to_figma` 제출 URL은 세션 프록시에서 막힐 수 있다 → `use_figma`로 직접 빌드
- 라이브러리 Publish는 API로 불가 → Assets → Libraries → Publish 안내
