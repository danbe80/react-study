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

inverted -> 클릭 시 disabled toggle
disabled란? input을 비활성화 시킬 수 있는 method

```js
const onInvert = () => {
  reset();
  setInverted((current) => !current);
};
```

<코드챌린지>

```js
function App() {
  const [index, setIndex] = React.useState("0");
  const onSelete = (event) => {
    setIndex(event.target.value);
  };
  return (
    <div>
      <h1>Super Converter</h1>
      <select value={index} onChange={onSelete}>
        <option value="0">Minutes & Hours</option>
        <option value="1">Km & Miles</option>
      </select>
      <hr />
      {index === "0" ? <MinutesToHours /> : null}
      {index === "1" ? <KmToMiles /> : null}
    </div>
  );
}
```

select tag를 이용해 onChange event로 event 발생 시 onSelete 실행
option에 value를 설정

```js
{
  index === "0" ? <MinutesToHours /> : null;
}
{
  index === "1" ? <KmToMiles /> : null;
}
```

JSX에 js를 사용하려면 {중괄호}를 사용

props란?
-> 부모 컴포넌트로부터 자식 컴포넌트에 데이터를 보낼 수 있게 해주는 방법
component에 보내지는 argument

HTML tag에 들어가는 ex) onClick 은 이벤트 리스너지만 JSX에 컴포넌트에 ex) onClick은 이벤트 리스너가 아니라 props의 이름이다.

propTypes => prop에 type을 정해놓고 data를 잘못 보내도 console에 오류로 보여지게끔 한다.
오류 확인이 propType의 사용 이유
