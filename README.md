# Frontend-Interview-Questions
Список вопросов для собеседования фронтенд разработчика

- [Общие](#general)  
- [Технические](#technical)  
	- [HTML](#html)
	- [CSS](#css)
	- [JavaScript](#javascript)
	- [React](#react)
	
<a name="general"/>

## Общие 
- Опыт работы и над какими проектами работал?
- Какие были использованы технологии?
- Чем занимался на этих проектах, за что отвечал - разработкой с нуля, введением новых фич, поддержкой и т.п
- Stack, на чем готов писать сейчас

<a name="technical"/>

## Технические

<a name="html"/>

#### _HTML_

- В чем разница между <script>, <script async> и <script defer>

<a name="css"/>

#### _CSS_

- Расскажи про специфику CSS селекторов
	- Какой стиль перепишет предыдущий?
- Опиши проп `position` и его возможные значения
- Препроцессоры

<a name="javascript"/>

#### _JavaScript_

- Какие типы данных есть в JS? 
	- В чем разница между `null` и `undefined`?
- Что такое всплытие (bubbling)?
	- Что такое делегирование событий?
- Что такое hoisting?
	- В чем разница между `var` и `let` / `const`?
	- Почему не стоит использовать `var`?
- Что такое замыкание?
- Как работает объект `this`?
	- Глобальный контекст
	- Как можно передать контекст функции при ее вызове? 
- В чем разница между `==` и `===`?
- Что такое strict mode?
	- Для чего нужен?
	- Какие ограничения вводит?
	- Что вызовет ошибку только в strict mode, несколько примеров?
- В чем разница между стрелочной и стандартной функциями?
- Что такое прототип объекта?
	- Какой прототип у `Object`?
	- В чем разница между `in` и `hasOwnProperty()`?
	- Какие есть типы пропсов? В чем их разница?
	- Как создать новый объект с определенным прототипом? 
	- Как задать новый проп объекту?
- Что такое Event Loop в браузере?
	- Макро и микро таски, рендеры
	- Какой приоритет и порядок выполнения?
	- Как создать макро и микро таски?
	- Что выведет данный код?
	
		```javascript
		console.log(1);

		setTimeout(() => console.log(2));

		Promise.resolve().then(() => console.log(3));

		Promise.resolve().then(() => setTimeout(() => console.log(4)));

		Promise.resolve().then(() => console.log(5));

		setTimeout(() => console.log(6));

		console.log(7);
		```
- Как можно оптимизировать трудоемкий процесс, чтобы избежать фризов?
	- Web workers
	- Macro Tasks
- Что такое Object Constructor Function?
	- Что выведет данный код?

		```js
		function Person(name, age) {
			return {
				name, age
			}
		}

		const john = new Person('John', 30);

		console.log(john instanceof Person);
		```
- ES6+
	- Классы
	- Промисы
	- Spread операторы
	- Деструктуризация массивов и объектов
	- Async / await
	- JS модули, export / import
	- Set, Map, WeakSet, WeakMap
		- В чем отличие WeakSet и WeakMap? 
	- Optional chaining (.?)
	- Оператор нулевого слияния (??)
		- Разница между `||` и `??`
		```js
		function printName(name) {
			console.log(name || 'defaultName');
		}
		
		printName('John');
		printName('');
		printName();
		```
- Как использовать приложение в режиме оффлайн?
	- Service Workers
- CORS?

##### Coding

```js
const players = [1, 2, 3, 4, 5];

// Объявить две переменные в одну строчку так, чтобы они имели следующие значения:
// winner: number = 1
// otherPlayers: number[] = [2, 3, 4, 5]
```

```javascript
// Напиши цикл, который перебирает числа до 100, возвращая 
// "fizz" на числа кратные 3, 
// "buzz" на числа кратные 5 
// "fizzbuzz" на числа кратные и 3, и 5
```
	
```js
import React, { useState } from 'react';	

function ItemList() {
  const [items, setItems] = useState(['item1', 'item2', 'item3', 'item4']);
  const [searchTerm, setSearchTerm] = useState('');

  const handleSearch = event => {
    setSearchTerm(event.target.value);
  };

  return (
    <div>
      <input type="text" onChange={handleSearch} value={searchTerm} />
      <ul>
        {items.map(item => (
          <li key={item}>{item}</li>
        ))}
      </ul>
    </div>
  );
}

// 1. Изменить компонент так, чтобы выводился список элементов подходящих под поисковой запрос
// 2. Добавить debounce на инпут
```



<a name="react"/>

#### _React_

⚠️ useEffect запускается два раза (придумать вопрос)

- Для чего был создан React?
	- Какую проблему решает?
- Назовите жизненные циклы React компонента
	- Как их можно реализовать с помощью хуков?
	- Где выполнять асинхронные запросы
- Что такое Virtual DOM?
	- Как происходит процесс сверки (Reconciliation)?
	- Сложность алгоритма сверки?
- Какой компонент нельзя реализовать через функциональный компонент?
- JSX
- Что такое React Hook?
	- Назови хуки, которые использовал
	- В чем разница между `useEffect()` и `useLayoutEffect()`?
	- В чем разница между `useState()` и `useRef()`?
	- Писал ли свои кастомные хуки?
- Какие библиотеки часто используешь вместе с React?
- Контролируемый и неконтролируемый компонент
- Какие есть подходы для оптимизации компонента?
	- useMemo, useCallback
- HOC
- CSS Method
- Для чего нужен State Management?
	- Что такое Flux архитектура?
	- Что такое Redux? В чем отличие от Flux?
	- Когда стоит использовать Redux, а когда React Context?
- TypeScript
- UI Library
- Testing
- SSR

#### _Next.js_

Coming soon...

#### _Инструменты_

- Webpack
- Babel

#### _Безопасность_

Coming soon...

#### Прочее

- Различия между `cookies`, `localStorage` и `sessionStorage`

#### Todo List:
- Добавить вопрос про использование ref в Context
- Добавить вопрос про кэш и пагинацию в rtk query
- Добавить вопросы про архитектуру


- [Coding Interview & Technical Assessment Platform - CoderPad](https://coderpad.io/)
