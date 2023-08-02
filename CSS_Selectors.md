# Types of Selectors

## 1. Universal Selector (\*)

- HTML 문서의 모든 요소를 선택한다. (html, head 포함)

```css
* {
  color: white;
}
```

## 2. Type Selector

- 지정한 모든 tag를 선택한다.

```css
h1 {
  font-size: 20px;
}
```

## 3. Class Selector (\.)

- HTML attribute에서 지정한 모든 class를 선택한다.

```css
.class {
  background-color: red;
}
```

## 4. ID Selector (\#)

- HTML attribute에서 지정한 하나의 ID를 선택한다.

```css
#id {
  color: red;
}
```

## 5. Attribute Selectors

### 5-1. selector[attr]

- 지정한 모든 attribute를 선택한다.

```css
img[alt] {
  color: blue;
}
```

### 5-2. selector[attr="value"]

- 지정한 attribute와 value를 가진 모든 요소를 선택한다.

```css
a[target="_blank"] {
  font-size: 20px;
}
```

### 5-3. selector[attr *= "value"]

- 지정한 attribute의 value를 가진 모든 요소를 선택한다.

```html
<!DOCTYPE html>
<html>
  <head>
    <style>
      a[href="test"] {
        color: red;
      }
    </style>
  </head>
  <body>
    <a href="test-case-1"></a>
    <a href="test-case-2"></a>
    <a href="test-case-3"></a>
    <a href="test"></a>
    <!-- 모든 a tag의 글자색이 빨간색으로 바뀐다. -->
  </body>
</html>
```

### 5-4. selector[attr ^= "value"]

- 지정한 value로 시작하는 모든 요소를 선택한다.

```css
a[href="http"] {
  font-size: 20px;
}
```

### 5-5. selector[attr $= "value"]

- 지정한 value로 끝나는 모든 요소를 선택한다.

```css
a[href=".com"] {
  font-size: 20px;
}
```

### 5-6. selector[attr ~= "value"]

- 지정한 value를 (공백으로 분리된) 단어로 포함하는 모든 요소를 선택한다.

```html
<!DOCTYPE html>
<html?>
  <head>
    <style>
      div[class="test"] {
        color: red;
      }
    </style>
  </head>
  <body>
    <div class="test-case-1"></div>
    <div class="test-case-2"></div>
    <div class="test case3"></div>
    <div class="test case4"></div>
    <!-- 3, 4번째 div tag만 글자색이 빨간색으로 바뀐다. -->
  </body>
</html>
```

### 5-7. selector[attr |= "value"]

- 지정한 value와 같거나 value 뒤에 hyphen(-)으로 시작하는 요소를 모두 선택한다.

```html
<!DOCTYPE html>
<html?>
  <head>
    <style>
      div[class="test"] {
        color: red;
      }
    </style>
  </head>
  <body>
    <div class="test-case-1"></div>
    <div class="test-case-2"></div>
    <div class="test case3"></div>
    <div class="test case4"></div>
    <!-- 모든 div tag의 글자색이 빨간색으로 바뀐다. -->
  </body>
</html>
```

## 6. Combinator Selectors

### 6-1. Descendant Combinator (selector selector)

- 지정한 선택자의 모든 하위 element(후손 element)를 선택한다.

```css
p div {
  color: red;
}
```

### 6-2. Child Combinator (selector X > selector Y)

- 선택자 X의 모든 children elements 중에 선택자 Y와 일치하는 모든 요소를 선택한다.

```css
p > div {
  color: red;
}
```

### 6-3. Adjacent Sibling Combinator (selector X + selector Y)

- 선택자 X의 형제 요소 중에 바로 뒤에 위치하는 선택자 Y 요소를 하나만 선택한다.

```css
p + div {
  color: red;
}
```

### 6-4. General Sibling Combinator (selector X ~ selector Y)

- 선택자 X의 형제 요소 중, 뒤에 위치하는 모든 선택자 Y 요소를 선택한다.

```css
p ~ div {
  color: red;
}
```

## 7. Pseudo Class Selectors (\:)

- https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-classes 참고

## 8. Pseudo Element Selectors (\::)

- https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements 참고
