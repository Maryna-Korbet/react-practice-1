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
  <a href="#closed-book">Task#1</a> &#xa0; | &#xa0;
  <a href="#orange-book">Task#2</a> &#xa0; | &#xa0;
  <a href="#green-book">Task#3</a> &#xa0; | &#xa0;
  <a href="#blue-book">Task#4</a> &#xa0; | &#xa0;
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

## :green_book: Task#3

# Список Forbes

Необхідно створити компонент `<ForbesList>`, за допомогою якого ми могли б
відображати інформацію про актуальну інформацію портала **Forbes**. Інформація
про актуальний рейтинг [forbes.json](./src/data/forbes.json).

[![Прев'ю компонента ForbesList](https://i.gyazo.com/d860b2fbd570a9eb800917b116fa0423.png)](https://gyazo.com/d860b2fbd570a9eb800917b116fa0423)

## Опис компонента `<ForbesList>`

Компонент повинен приймати один проп `list` - масив об'єктів друзів.

Компонент повинен створювати наступну структуру.

```jsx
<LeaderBoard>
  <BoardHeader>
    <BoardTitle>
      <TitleTop>Forbes</TitleTop>
      <TitleBottom>Leader board</TitleBottom>
    </BoardTitle>
  </BoardHeader>

  <LeaderBoardProfiles>
    {/* Довільна кіл-сть FriendListItem */}
  </LeaderBoardProfiles>
</LeaderBoard>
```

## Опис компонента `<ForbesListItem>`

Компонент повинен приймати кілька пропcів:

- `avatar` - аватар мільйонера
- `name` - ім'я мільйонера
- `capital` - статки мільйонера
- `isIncrease` - буль, що сигналізує про стан мільйонера: збільшився або ні.

Залежно від пропа `isIncrease`, повинна змінюватися іконка: при збільшення
статку - `<FcBullish/>` або при зменшенні - `<FcBearish/>`

Компонент повинен бути наступної структури.

```jsx
<ForbesItem>
  <Avatar
    src="https://randomuser.me/api/portraits/men/32.jpg"
    alt="Mark Zuckerberg"
  />
  <Name>Mark Zuckerberg</Name>
  <Capital>
    35.7 <BiDollarCircle color={theme.colors.accent} size={22} />
    {/* Тут має бути необхідна іконка зміни статку */}
  </Capital>
</ForbesItem>
```

## Приклад використання

```js
import forbes from 'data/forbes.json';

<FriendList list={forbes} />,
```

## :blue_book: Task#4

# Історія транзакцій

Необхідно створити компонент історії транзакцій в особистому кабінеті
крипто-гаманця.

[![Прев'ю компонента CryptoHistory](https://i.gyazo.com/c40db818fdf62f749f97ab24f1946928.png)](https://gyazo.com/c40db818fdf62f749f97ab24f1946928)

Дані для списку доступні у форматі JSON у файлі
[transactions.json](./src/data/transactions.json). Це масив об'єктів, кожен
об'єкт описує одну транзакцію з наступними властивостями:

- `id` — унікальний ідентифікатор транзакції
- `price` — залишок на рахунку
- `amount` - сума транзакції
- `date` - дата транзакції

## Опис компонента `<CryptoHistory>`

Необхідно створити компонент `<CryptoHistory>`, який приймає один проп `items` -
масив об'єктів транзакцій з `transactions.json`. Компонент створює розмітку
таблиці. Кожна транзакція - це рядок таблиці. У прикладі наведена структура двох
транзакцій.

```jsx
<BaseTable>
  <THead>
    <tr>
      <Th>№</Th>
      <Th>PRICE</Th>
      <Th>AMOUNT</Th>
      <Th>DATE</Th>
    </tr>
  </THead>

  <tbody>
    <Tr>
      <Td>1</Td>
      <Td>3190</Td>
      <Td>0.24843</Td>
      <Td>02/01/2022, 1:14 PM</Td>
    </Tr>
    <Tr>
      <Td>2</Td>
      <Td>3195</Td>
      <Td>0.088</Td>
      <Td>05/09/2022, 2:24 PM</Td>
    </Tr>
  </tbody>
</BaseTable>
```

> Для форматування дати використовуйте метод
> [format](https://date-fns.org/v2.28.0/docs/format) бібліотеки **date-fns**

## Приклад використання

```js
import transactions from 'data/transactions.json';

<TransactionHistory items={transactions} />;
```

## :rocket: Technologies

The following tools were used in this project:

- [React](https://pt-br.reactjs.org/)
