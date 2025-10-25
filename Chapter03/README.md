# 📘 명품 웹 프로그래밍 3장 요약  
**HTML5 문서 구조화 & 웹 폼**

---

## 🎯 학습 목표  
- HTML5 시맨틱(semantic) 태그의 개념 이해  
- 시맨틱 태그를 이용한 구조화된 웹 페이지 작성  
- 웹 폼(form)의 목적과 구성 요소 이해  
- 다양한 입력 방식과 HTML5 폼 요소 활용  

---

## 🧱 HTML5 문서 구조화의 필요성  
### 기존 HTML의 한계  
- `<div>`나 `<table>` 태그로만 구조 표현 → 의미 전달 어려움  
- 검색 엔진이 문서 구조를 인식하기 힘듦  

### 문서 구조화의 이유  
- 검색 엔진 최적화(SEO)  
- 사물인터넷 환경에서 기계가 정보를 이해할 수 있도록  
- 사용자와 장치가 “의미” 중심으로 접근 가능  

---

## 🧩 시맨틱 웹과 시맨틱 태그  
| 태그 | 설명 |
|------|------|
| `<header>` | 문서나 섹션의 머리말, 제목·소개 포함 |
| `<nav>` | 하이퍼링크 모음(목차, 메뉴 등) |
| `<section>` | 문서의 장(chapter)·절(section) |
| `<article>` | 독립적인 콘텐츠(게시글, 블로그 글 등) |
| `<aside>` | 본문 외의 참고 내용(노트, 팁, 광고 등) |
| `<footer>` | 문서나 섹션의 꼬리말(저자, 저작권 등) |

> **CSS3**로 모양과 색, 위치를 지정해야 하며 태그만으로 시각적 효과는 자동 생성되지 않는다.  

---

## 🧱 시맨틱 태그 적용 예시  
```html
<header>header</header>
<nav>nav</nav>
<section>section</section>
<aside>aside</aside>
<footer>footer</footer>
```

---

## 🧾 시맨틱 태그로 구조화한 문서 예시
**모차르트 소개 페이지**

- `<header>` : 제목, 요약, 이미지  
- `<nav>` : 목차  
- `<section>` : 본문  
- `<article>` : 세부 절(생애, 죽음, 음악 등)  
- `<aside>` : 관련 노트  
- `<footer>` : 저작 정보  

---

## 🧱 추가 시맨틱 태그  

| 태그 | 설명 |
|------|------|
| `<figure>` | 삽화, 코드, 이미지 등을 하나의 블록으로 표현 |
| `<figcaption>` | `<figure>`에 대한 설명 |
| `<details>` / `<summary>` | 접었다 펼 수 있는 정보 블록 |
| `<mark>` | 중요한 텍스트 강조 |
| `<time>` | 시간 데이터 |
| `<meter>` | 비율/수치 데이터 |
| `<progress>` | 작업 진행 상태 표시 |

---

## ❌ HTML5에서 제거된 태그  
> 구조화에 방해되는 태그들은 더 이상 사용하지 않음  

`<big>`, `<center>`, `<font>`, `<frame>`, `<strike>`, `<u>`, `<applet>` 등  

---

## 🧮 웹 폼 (Web Form)
### 개념  
- 사용자 입력을 웹 서버로 전달하기 위한 인터페이스  
- 로그인, 검색, 등록, 예약, 쇼핑 등에 사용  

### 기본 구조  
```html
<form name="fo" method="get" action="serverProgram">
  ...
</form>
```

| 속성 | 설명 |
|------|------|
| `name` | 폼 이름 지정 |
| `method` | 데이터 전송 방식(GET/POST) |
| `action` | 전송 대상 서버 프로그램의 URL |

---

## 🖋️ 텍스트 입력 요소  

| 태그 | 설명 |
|------|------|
| `<input type="text">` | 한 줄 입력 |
| `<input type="password">` | 비밀번호 입력 |
| `<textarea>` | 여러 줄 입력 |
| `<datalist>` | 입력 가능한 데이터 목록 제시 |

---

## 🔘 버튼 관련 요소  

| 태그 | 설명 |
|------|------|
| `<input type="button">` | 일반 버튼 |
| `<input type="submit">` | 서버 전송 버튼 |
| `<input type="reset">` | 입력 초기화 |
| `<input type="image">` | 이미지 버튼 |
| `<button>` | 다목적 버튼 (태그 내부에 텍스트/이미지 포함 가능) |

---

## ☑️ 선택형 입력 요소  

| 형태 | 태그 | 특징 |
|------|------|------|
| 체크박스 | `<input type="checkbox">` | 다중 선택 가능 |
| 라디오버튼 | `<input type="radio">` | 단일 선택 (name 동일 그룹) |
| 콤보박스 | `<select>` + `<option>` | 드롭다운 선택형 입력 |

---

## 🏷️ `<label>` 태그의 활용  
- 폼 요소의 캡션 역할  
- 클릭 범위를 넓혀 **접근성 향상**  

```html
<label>사용자 ID: <input type="text"></label>
<label for="pw">비밀번호:</label>
<input id="pw" type="password">
```

---

## 🎨 색상 입력  
```html
<input type="color" value="#00BFFF">
```
- 사용자가 직접 색상 선택 가능  
- JavaScript로 선택된 색을 문서 스타일에 반영 가능  

---

## ⏰ 시간 입력 관련 태그  
| 태그 | 설명 |
|------|------|
| `<input type="date">` | 날짜 입력 |
| `<input type="time">` | 시간 입력 |
| `<input type="month">` | 월 입력 |
| `<input type="week">` | 주 입력 |
| `<input type="datetime-local">` | 날짜+시간 입력 |

---

## 🔢 숫자 입력  
| 태그 | 설명 |
|------|------|
| `<input type="number">` | 스핀 버튼 제공 |
| `<input type="range">` | 슬라이드 바 제공 |

```html
<input type="number" min="0.0" max="10.0" step="0.5">
<input type="range" min="10" max="30" list="temperatures">
```

---

## 💡 힌트와 형식 지정  
| 기능 | 예시 |
|------|------|
| 힌트 표시 | `placeholder="id@host"` |
| 이메일 형식 | `<input type="email">` |
| URL 형식 | `<input type="url">` |
| 전화번호 형식 | `<input type="tel">` |
| 검색 입력 | `<input type="search">` |

---

## 📦 폼 그룹핑  
- `<fieldset>` : 관련 폼 요소들을 묶음  
- `<legend>` : 그룹의 제목  

```html
<fieldset>
  <legend>회원정보</legend>
  이메일: <input type="email">
</fieldset>
```

---

## 🧠 핵심 정리  
- 시맨틱 태그는 구조 + 의미를 함께 전달  
- `<header>`, `<section>`, `<article>`은 문서 구조를 명확히 함  
- `<form>`과 다양한 `<input>` 태그로 사용자 입력을 구현  
- HTML5는 **표준화된 입력 방식**과 **의미 중심 구조화**를 통해 접근성과 검색 효율을 높임  

---

**Q1.** 시맨틱 태그를 활용하면 SEO(검색엔진최적화)에 어떤 이점이 있을까?  

**Q2.** `<form>`의 `GET`과 `POST` 방식은 어떤 상황에서 각각 더 적합할까?  

**Q3.** `<label>` 태그를 사용하면 사용자 접근성과 UX가 어떻게 개선될까?  
