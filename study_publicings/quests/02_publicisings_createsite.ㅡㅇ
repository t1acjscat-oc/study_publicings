프롬포트

```
{
  "title": "스터디로그(StudyLog) - 공부 기록 & 프로젝트 관리 사이트",
  "role": "당신은 HTML/CSS/JavaScript만 사용해서 학습용 웹사이트를 만드는 프론트엔드 개발자입니다. 백엔드 서버는 없으며, CRUD 기능은 로컬 상태(예: JavaScript 배열)나 임시 스토리지(localStorage)를 사용해서 데모 형태로 구현합니다.",
  "goal": "대학생이나 취준생이 매일의 공부 내용을 기록하고, 주간 목표와 통계를 확인할 수 있는 '스터디로그' 웹사이트를 제작합니다. 상단 메뉴에는 하위 메뉴가 포함되어야 하며, 최소 한 개의 메뉴에는 CRUD(Create, Read, Update, Delete) 기능이 구현되어야 합니다. 또한 관리자 전용 화면을 포함해야 합니다.",
  "technical_requirements": {
    "stack": ["HTML5", "CSS3", "Vanilla JavaScript"],
    "files": ["index.html", "style.css", "app.js"],
    "constraints": [
      "반응형 레이아웃: 모바일, 태블릿, 데스크탑 기본 대응",
      "외부 프레임워크(React, Vue, Bootstrap 등) 사용 금지",
      "CRUD는 JavaScript로만 구현하고 서버 통신은 하지 않음",
      "주석을 충분히 작성해서 학습용 코드가 되도록 함"
    ]
  },
  "layout": {
    "header": {
      "logo_text": "StudyLog",
      "nav": [
        {
          "label": "홈",
          "id": "menu-home",
          "submenus": []
        },
        {
          "label": "공부 기록",
          "id": "menu-study",
          "submenus": [
            { "label": "오늘의 공부 (CRUD)", "id": "submenu-today" },
            { "label": "주간 목표", "id": "submenu-weekly" },
            { "label": "나의 통계", "id": "submenu-stats" }
          ]
        },
        {
          "label": "자료실",
          "id": "menu-library",
          "submenus": [
            { "label": "HTML/CSS 정리", "id": "submenu-htmlcss" },
            { "label": "AI & 자동화 노트", "id": "submenu-ai" }
          ]
        },
        {
          "label": "마이페이지",
          "id": "menu-mypage",
          "submenus": [
            { "label": "나의 프로필", "id": "submenu-profile" },
            { "label": "알림 설정", "id": "submenu-noti" }
          ]
        },
        {
          "label": "관리자",
          "id": "menu-admin",
          "submenus": [
            { "label": "관리자 로그인", "id": "submenu-admin-login" },
            { "label": "공부 기록 관리 (CRUD)", "id": "submenu-admin-study" },
            { "label": "공지사항 관리", "id": "submenu-admin-notice" }
          ]
        }
      ]
    },
    "footer": {
      "text": "© 2025 StudyLog. All rights reserved."
    }
  },
  "pages": [
    {
      "id": "home",
      "title": "홈",
      "components": [
        "간단한 인사 메시지와 사이트 소개 섹션",
        "오늘의 공부 기록 일부를 카드 형태로 3개 정도 보여주는 하이라이트 섹션",
        "이용 방법(1. 오늘 공부 기록하기, 2. 주간 목표 설정, 3. 통계 확인) 안내 섹션"
      ]
    },
    {
      "id": "today-study",
      "title": "오늘의 공부 (CRUD)",
      "description": "사용자가 오늘 공부한 내용을 CRUD로 관리하는 핵심 기능 페이지",
      "crud": {
        "entity_name": "공부 기록",
        "fields": [
          { "name": "date", "label": "날짜", "type": "date", "required": true },
          { "name": "title", "label": "공부 제목", "type": "text", "required": true },
          { "name": "category", "label": "카테고리", "type": "select", "options": ["HTML/CSS", "JavaScript", "AI/자동화", "기타"], "required": true },
          { "name": "time", "label": "공부 시간(분)", "type": "number", "required": true },
          { "name": "memo", "label": "메모", "type": "textarea", "required": false }
        ],
        "ui": {
          "create_form": "상단에 새 공부 기록을 추가하는 폼 배치",
          "list_view": "아래쪽에 테이블 혹은 카드 목록 형태로 기존 기록 나열",
          "actions": ["보기", "수정", "삭제"],
          "edit_mode": "수정 버튼 클릭 시 해당 레코드를 폼에 불러와 수정 후 저장",
          "delete_confirm": "삭제 버튼 클릭 시 confirm()으로 사용자에게 확인"
        },
        "data_storage": "JavaScript 배열과 localStorage를 사용해 페이지 새로고침 후에도 데이터가 유지되도록 구현"
      }
    },
    {
      "id": "weekly-goal",
      "title": "주간 목표",
      "components": [
        "이번 주 목표를 입력하는 간단한 폼",
        "목표 리스트를 카드 형태로 나열",
        "완료 여부를 표시하는 체크박스"
      ]
    },
    {
      "id": "stats",
      "title": "나의 통계",
      "components": [
        "공부 기록 데이터를 기반으로 주간/월간 총 공부 시간 합계를 보여주는 섹션",
        "카테고리별 비율을 막대 그래프 또는 가짜 그래프 레이아웃으로 표현(실제 그래프 라이브러리 없이 CSS로 구현)"
      ]
    },
    {
      "id": "library-htmlcss",
      "title": "HTML/CSS 정리",
      "components": [
        "HTML 기본 태그 요약 리스트",
        "CSS 선택자, 박스 모델 등의 개념을 카드 형태로 정리",
        "코드 예제를 표시하는 <pre><code> 블럭"
      ]
    },
    {
      "id": "library-ai",
      "title": "AI & 자동화 노트",
      "components": [
        "n8n, Gemini API, curl 예제 등 간단한 설명",
        "각 예제를 박스 카드 형태로 나열",
        "주의사항이나 팁을 강조 박스로 표시"
      ]
    },
    {
      "id": "mypage-profile",
      "title": "나의 프로필",
      "components": [
        "이름, 닉네임, 목표 직무 등을 입력하는 폼",
        "저장 버튼 클릭 시 localStorage에 저장",
        "저장된 정보를 다시 불러와 화면에 보여주기"
      ]
    },
    {
      "id": "mypage-noti",
      "title": "알림 설정",
      "components": [
        "오늘 공부 알림, 주간 목표 리마인드 등 체크박스 옵션",
        "알림 시뮬레이션용으로 '테스트 알림' 버튼을 만들어 alert() 실행"
      ]
    },
    {
      "id": "admin-login",
      "title": "관리자 로그인",
      "components": [
        "아이디와 비밀번호를 입력하는 로그인 폼",
        "하드코딩된 값(예: id: admin, pw: 1234)과 일치할 때만 관리자 페이지로 이동시키는 JavaScript 로직",
        "실제 보안 기능은 없고 학습용 데모임을 화면에 작은 글씨로 표시"
      ]
    },
    {
      "id": "admin-study",
      "title": "공부 기록 관리 (관리자용 CRUD)",
      "description": "일반 사용자 페이지에서 작성된 공부 기록을 관리자 관점에서 한 번에 관리",
      "components": [
        "공부 기록 전체 목록을 테이블로 표시",
        "각 행마다 '수정', '삭제' 버튼 제공",
        "관리자는 제목, 카테고리, 시간, 메모 등을 직접 수정할 수 있음",
        "특정 날짜나 카테고리로 필터링하는 셀렉트 박스 제공"
      ]
    },
    {
      "id": "admin-notice",
      "title": "공지사항 관리",
      "components": [
        "공지사항 제목과 내용을 입력하는 폼",
        "공지사항 목록을 위에서 아래로 나열",
        "홈 화면에 최신 공지 1~2개가 보이도록 연동(데이터 공유)"
      ]
    }
  ],
  "style_guide": {
    "color_palette": {
      "primary": "#4F46E5",
      "secondary": "#EC4899",
      "background": "#F9FAFB",
      "text_main": "#111827",
      "text_muted": "#6B7280"
    },
    "font": "기본 시스템 폰트(예: 'Noto Sans KR', sans-serif)",
    "components": [
      "카드형 박스 디자인",
      "둥근 모서리와 약한 그림자",
      "호버 시 버튼 색상 또는 그림자 변화"
    ]
  },
  "comment": "이 JSON에 맞춰 HTML/CSS/JS 코드를 생성하고, 각 페이지 섹션을 id로 구분하여 단일 페이지(SPA 형태) 또는 여러 HTML 파일로 구성해도 됩니다. 메뉴 클릭 시 해당 섹션으로 스크롤 이동하거나, JavaScript로 섹션을 토글하는 방식으로 구현해 주세요."
}
```

