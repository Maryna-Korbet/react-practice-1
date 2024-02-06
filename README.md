<div align="center" id="top"> 
  <img src="./src/icons/learning.png" alt="React Practice 1" width="100"/>

&#xa0;

<a href="https://maryna-korbet.github.io/react-practice-1">Demo</a>

</div>

<h1 align="center">React Practice 1</h1>

<p align="center">
  <img alt="Github top language" src="https://img.shields.io/github/languages/top/Maryna-Korbet/react-practice-1?color=FF8C00">

  <img alt="Github language count" src="https://img.shields.io/github/languages/count/Maryna-Korbet/react-practice-1?color=FF8C00">

  <img alt="Repository size" src="https://img.shields.io/github/repo-size/Maryna-Korbet/react-practice-1?color=FF8C00">
</p>

<p align="center">
  <a href="#dart-about">About</a> &#xa0; | &#xa0; 
  <a href="#closed_book">Task#1</a> &#xa0; | &#xa0;
  <a href="#orange_book">Task#2</a> &#xa0; | &#xa0;
  <a href="#green_book">Task#3</a> &#xa0; | &#xa0;
  <a href="#blue_book">Task#4</a> &#xa0; | &#xa0;
  <a href="#rocket-technologies">Technologies</a> &#xa0; 
</p>

<br>

## :dart: About

Task performance practice

## :closed_book: Task#1

# Картка блогу

Необхідно створити компонент `<BlogCard/>`, за допомогою якого ми могли б
відображати інформацію про користувача соціальної мережі. Дані про користувача
лежать у файлі [article.json](./src/data/article.json).

[![Прев'ю компонента BlogCard](https://i.gyazo.com/5ce54e49016220bcde9209b893eb5e62.jpg)](https://gyazo.com/5ce54e49016220bcde9209b893eb5e62)

## Опис компонента `<BlogCard/>`

Компонент повинен приймати кілька пропсів з інформацією про користувача:

- `poster` — постер картки
- `tag` — категорія статті
- `title` — заголовок статті
- `description` — опис
- `name` — ім'я користувача
- `avatar` — аватар користувача
- `postedAt` — час створення (рекомендовано в форматі від дати до сьогодні)

Компонент повинен створювати наступну структуру.

```jsx
<Card>
  <CardHeader>
    <CardPoster
      src="https://source.unsplash.com/600x400/?computer"
      alt="card__image"
    />
  </CardHeader>
  <CardBody>
    <Tag>Technology</Tag>
    <CardTitle>What's new in 2022 Tech</CardTitle>
    <CardText>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Sequi perferendis
      molestiae non nemo doloribus. Doloremque, nihil! At ea atque quidem!
    </CardText>
  </CardBody>
  <CardFooter>
    <UserBox>
      <Avatar src="https://i.pravatar.cc/40?img=1" alt="Jane Doe" />
      <UserInfo>
        <UserName>Jane Doe</UserName>
        <Date>2h ago</Date>
      </UserInfo>
    </UserBox>
  </CardFooter>
</Card>
```

> Для форматування дати використовуйте метод
> [formatDistanceToNow](https://date-fns.org/v2.28.0/docs/formatDistanceToNow)
> бібліотеки **date-fns**

## Приклад використання

```js
import article from 'data/article.json';

<BlogCard
  poster={article.poster}
  tag={article.tag}
  title={article.title}
  description={article.description}
  userName={article.name}
  avatar={article.avatar}
  postedAt={article.postedAt}
/>;
```

## :orange_book: Task#2

# Секція статистики

Створити компонент `<Statistics>`, який би показував статистику з переданих
пропсів - основну статистику інтернет-магазину стосовно зареєстрованих
користувачів, відгуків тощо . Дані про статистику лежать у файлі
[data.json](./src/data/data.json).

[![Прев'ю компонента Statistics](https://i.gyazo.com/a75d617620bdb0805e19d5a394699dea.png)](https://gyazo.com/a75d617620bdb0805e19d5a394699dea)

## Опис компонента

Компонент повинен приймати два пропи `title` і `stats`, в яких вказується
заголовок та об'єкт статистики.

- `title` - не обов'язковий, і якщо він не переданий, не повинна рендеритись
  розмітка заголовка `<h3>`.
- `stats` - масив об'єктів, що містять інформацію про елемент статистики. Може
  мати довільну кількість елементів.

Компонент повинен створювати наступну структуру.

```jsx
<StatisticTitle>Main Statistics</StatisticTitle>

<StatisticsList>
  <StatisticBox>
    {/* Тут має бути іконка */}
    <StatisticCounter>2147</StatisticCounter>
    <StatisticText>Happy Customers</StatisticText>
  </StatisticBox>

  <StatisticBox>
    {/* Тут має бути іконка */}
    <StatisticCounter>3275</StatisticCounter>
    <StatisticText>Registered Members</StatisticText>
  </StatisticBox>

  <StatisticBox>
    {/* Тут має бути іконка */}
    <StatisticCounter>289</StatisticCounter>
    <StatisticText>Available Products</StatisticText>
  </StatisticBox>

  <StatisticBox>
    {/* Тут має бути іконка */}
    <StatisticCounter>1563</StatisticCounter>
    <StatisticText>Saved Trees</StatisticText>
  </StatisticBox>
</StatisticsList>
```

> Завдання з іконкою робити за бажанням. Треба продумати логіку, як динамічно
> відмалювати з бібліотеки
> [**react-icons**](https://github.com/react-icons/react-icons) та змінити
> дефолтний розмір

## Приклад використання

```js
import data from '/путь/к/data.json';

<Statistics title="Main Statistics" stats={data} />;
<Statistics stats={data} />;
```

## :green_book: Task#2

## :blue_book: Task#2

## :rocket: Technologies

The following tools were used in this project:

- [React](https://pt-br.reactjs.org/)
