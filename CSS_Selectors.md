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

## 5. Attribute Selector

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
  <body></body>
</html>
```
