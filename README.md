# react-study

React.useState(initial value || null) // [undefind, fn] undefind : data fn : fn is change the data
-> array looking at data
useState(initial value) : It is possible initial value setting

undefind is the initial value and the second argument is a function that changes the value

modifier() -> this function is changes the value

modifier function으로 state를 바꿀 때 rendering이 새로운 data를 가지고 일어남

setCounter((current) => current + 1) is safer than setCounter(counter + 1)
modifier(function) more than safe

JSX는 HTML과 매우 유사
예를 들어, label 태그

```html
<label for="minutes">Minutes</label>
<input id="minutes" placeholder="Minutes" type="number" />
<label for="hours">Hours</label>
<input id="hours" placeholder="Hours" type="number" />
```

for은 자바스크립트 용어 => htmlFor 로 사용 (JSX)
class도 자바스크립트 용어 => className 로 사용 (JSX)

react 세계에선 input은 uncontroller 임
