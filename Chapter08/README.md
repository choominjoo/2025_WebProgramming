# 📘 명품 웹 프로그래밍 8장 요약  
**HTML DOM(Document Object Model)**

---

## 🎯 학습 목표  
- HTML DOM의 필요성과 구조 이해  
- DOM 트리와 HTML 태그의 관계 파악  
- DOM 객체의 구성 요소(프로퍼티, 메서드, 컬렉션 등) 이해  
- DOM을 이용해 HTML 콘텐츠와 스타일 제어  
- `document` 객체의 역할과 활용법 습득  
- `createElement()`, `appendChild()` 등을 이용한 DOM 동적 조작  

---

## 🧱 HTML DOM의 개념  
- **DOM(Document Object Model)**:  
  브라우저가 HTML 문서를 해석해 **태그마다 객체를 생성**한 구조.  
- **목적**  
  - HTML 태그의 **출력 모양**과 **콘텐츠**를 제어  
  - CSS 스타일 시트를 동적으로 변경  
  - 텍스트, 이미지 등의 내용을 수정  

---

## 🌳 DOM 트리 구조  
- HTML 문서의 포함 관계에 따라 **트리(tree)** 형태로 구성됨  
- 각 HTML 태그마다 **DOM 객체(Node)** 하나씩 생성  
- **루트 객체**는 `document`  
- DOM 변경 시 브라우저는 즉시 해당 HTML 출력 갱신  

---

## 📄 예시 구조
```html
<html>
  <head><title>HTML DOM 트리</title></head>
  <body>
    <p>이것은 <span>문장입니다.</span></p>
    <form>
      <input type="text">
      <input type="button" value="테스트">
    </form>
  </body>
</html>
```
→ DOM 트리 관계
`document` → `html` → (`head`, `body`) → (`p`, `form`) → (`span`, `input`, `input`)

---

## 🧩 DOM 객체의 구성 요소
| 구성 요소 | 설명 |
|-----------|------|
| property | 태그 속성(attribute)을 반영 |
| method | DOM 조작용 함수 |
| collection | 자식 노드들의 집합 (배열 형태) |
| event listener | 이벤트 발생 시 실행되는 함수 |
| CSS3 style | 태그의 스타일 정보를 제어 |

```java script
let p = document.getElementById("firstP");
p.style.color = "red";       // 글자 색 변경
p.innerHTML = "새 텍스트";  // 콘텐츠 변경

```
---

## 🔍 DOM 탐색 관계
