# 📘 명품 웹 프로그래밍 2장 요약  
**HTML5 기본 문서 구조 및 주요 태그**

---

## 🎯 학습 목표  
- HTML 페이지의 기본 구조와 필수 태그 이해  
- HTML5 문서를 작성할 수 있다  
- 이미지, 표, 하이퍼링크 삽입  
- 인라인 프레임(iframe) 사용  
- 오디오·비디오 삽입  

---

## 🧱 HTML5 기본 구조  

```html
<!DOCTYPE html>
<html>
<head>
  <meta charset="utf-8">
  <title>문서 제목</title>
</head>
<body>
  문서의 본문 내용
</body>
</html>
```

- `<!DOCTYPE html>` : HTML5 문서임을 선언  
- `<html>`, `<head>`, `<title>`, `<body>`는 필수  
- 주석문 : `<!-- 주석 내용 -->`  

---

## 🏷️ HTML 태그의 특징  
- **시작/종료 태그**: `<h1>제목</h1>`  
- **빈 요소 태그**: `<br>`, `<hr>`  
- **대소문자 구분 없음**  
- **속성(attribute)**  
  - 예: `<img src="heart.jpg" width="100" alt="이미지">`  

---

## 🧾 기본 텍스트 관련 태그  

| 기능 | 태그 예시 |
|------|------------|
| 제목(heading) | `<h1>` ~ `<h6>` |
| 단락 | `<p>` |
| 줄바꿈 | `<br>` |
| 수평선 | `<hr>` |
| 주석 | `<!-- 내용 -->` |
| 특수문자 | `&lt;`, `&copy;`, `&#169;`, `&nbsp;` 등 |
| 원본 형식 유지 | `<pre>` |
| 강조/꾸미기 | `<b>`, `<i>`, `<em>`, `<strong>`, `<mark>`, `<small>`, `<del>`, `<ins>` |

---

## 🧩 블록 태그 vs 인라인 태그  

| 구분 | 블록 태그 | 인라인 태그 |
|------|------------|--------------|
| 예시 | `<div>`, `<p>`, `<ul>` | `<span>`, `<a>`, `<img>` |
| 특징 | 새 줄에서 시작 | 같은 줄 내 삽입 가능 |
| 대표 사용 | `<div>` | `<span>` |

---

## ⚙️ 메타데이터 관련 태그  

| 태그 | 역할 |
|------|------|
| `<base>` | 기본 URL 지정 |
| `<link>` | 외부 CSS 연결 |
| `<meta>` | 인코딩, 키워드, 설명, 저자 등 지정 |

예시:  
```html
<head>
  <meta charset="utf-8">
  <meta name="author" content="황기태">
  <meta name="keywords" content="HTML, CSS, 웹 프로그래밍">
  <link rel="stylesheet" href="style.css">
</head>
```

---

## 🖼️ 이미지 삽입  
```html
<img src="media/Elvis1.jpg" width="150" height="200" alt="Elvis">
```
- **src**: 이미지 경로  
- **alt**: 대체 텍스트  
- **형식**: JPG, PNG, GIF, BMP 등  

---

## 🧮 리스트  

| 종류 | 태그 | 설명 |
|------|------|------|
| 순서 있는 리스트 | `<ol>` | 숫자, 알파벳 등 순서 표시 |
| 순서 없는 리스트 | `<ul>` | 점(•)으로 표시 |
| 정의 리스트 | `<dl>` | `<dt>` 용어 / `<dd>` 설명 |

중첩 가능  
```html
<ul>
  <li>음식
    <ul><li>스파게티</li></ul>
  </li>
</ul>
```

---

## 📊 표 (Table)  

```html
<table border="1">
  <caption>성적표</caption>
  <thead><tr><th>이름</th><th>HTML</th></tr></thead>
  <tbody><tr><td>홍길동</td><td>90</td></tr></tbody>
  <tfoot><tr><th>합계</th><th>90</th></tr></tfoot>
</table>
```

- `<caption>` : 표 제목  
- `<thead>`, `<tbody>`, `<tfoot>` : 표 구분  
- `<tr>` : 행, `<th>` : 제목 셀, `<td>` : 데이터 셀  

---

## 🔗 하이퍼링크  

```html
<a href="http://www.naver.com">네이버</a>
<a href="image.jpg" download>이미지 다운로드</a>
```

- **href** : 이동할 URL  
- **target 속성**
  - `_blank` : 새 창
  - `_self` : 현재 창
  - `_parent` : 부모 창
  - `_top` : 최상위 창  

- **앵커(Anchor)**  
  ```html
  <a href="#section1">이동</a>
  <h3 id="section1">목적지</h3>
  ```

---

## 🪟 인라인 프레임 (iframe)  

```html
<iframe src="iframe1.html" width="200" height="150">
브라우저가 iframe을 지원하지 않습니다.
</iframe>
```

- 웹 페이지 안에 다른 HTML 문서를 삽입  
- **srcdoc 속성**으로 직접 코드 삽입 가능  

```html
<iframe srcdoc="<p>Hello iframe!</p>"></iframe>
```

- **계층 구조**
  - 부모(parent), 자식(child), 최상위(top) 윈도우  
  - `<a target="frameName">` 으로 특정 프레임에 페이지 로드 가능  

---

## 🎵 오디오 / 🎬 비디오 삽입  

### 🎬 비디오  
```html
<video src="media/bear.mp4" width="320" height="240" controls></video>
```

### 🎵 오디오  
```html
<audio src="media/music.mp3" controls loop></audio>
```

- **controls**: 재생 버튼 표시  
- **autoplay**: 자동 재생 (보안상 대부분의 브라우저에서 제한)  
- **loop**: 반복 재생  

---

## 🧠 핵심 정리  

- HTML 문서는 `<html>`, `<head>`, `<body>` 구조  
- 텍스트, 이미지, 표, 리스트, 링크 등은 태그로 표현  
- `<iframe>`으로 페이지 내 다른 페이지 삽입 가능  
- `<audio>`, `<video>`로 멀티미디어 통합  

---

**Q1.** 블록 요소와 인라인 요소를 구분해서 사용하는 이유는 무엇일까?  

**Q2.** `<iframe>`을 과도하게 사용하면 웹 접근성에 어떤 영향을 줄까?  

**Q3.** HTML5에서 오디오·비디오를 플러그인 없이 재생할 수 있게 된 의미는 무엇일까?  
