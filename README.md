# Zap UI

Zap UI это легкая в использовании UI библиотека, разработанная для совместной работы с React. Проект ориентирован на обеспечение удобства разработки пользовательских интерфейсов с использованием популярного фреймворка React и интеграции стилей с помощью Tailwind CSS..

## Содержание

- [Установка](#использование)
- [Требования](#требования)
- [Установка компонентов](#установка-компонентов)
  - [Элементы](#элементы)
    - [elements-biglink](#elements-biglink)
    - [elements-button](#elements-button)
    - [elements-input](#elements-input)
  - [Главные экраны](#главные-экраны)
    - [hello-simple-center](#hello-simple-center)
    - [hello-simple-gallery](#hello-simple-gallery)
    - [hello-simple-center-diagonal](#hello-simple-center-diagonal)
  - [Блоки информации](#блоки-информации)
    - [info-block-earth](#info-block-earth)
    - [info-block-mars](#info-block-mars)
    - [info-block-mercury](#info-block-mercury)
    - [info-block-upiter](#info-block-upiter)
    - [info-block-venus](#info-block-venus)
  - [CTA блоки](#call-to-action-блоки)
    - [cta-earth](#cta-earth)
  - [Блоки подписки](#блоки-подписки-на-новости)
    - [newsletter-sections](#newsletter-sections)
  - [Блоки отзывов](#блоки-отзывов)
    - [testimonials-kuiper-belt](#testimonials-kuiper-belt)
  - [Фото блоки](#фото-блоки) -[photo-content](#photo-content)
- [Команда проекта](#команда-проекта)

## Использование:

Установите npm-пакет с помощью команды:

```sh
$ npm i -D @roodiroot/zap-ui
```

Далее необходимо инициализировать свой проект:

```sh
$ npx @roodiroot/zap-ui init
```

Это создаст фаил конфигурации в корне проекта, в нем укажите актуальный путь для установки компонентов:

```js
{
    "contentPath": "src/components/ui"
}
```

## Разработка

### Требования

Для установки и запуска проекта, необходим [React](https://react.dev/), а так же установленная библиотека [TailwindCss](https://tailwindcss.com/).

### Установка компонентов

Для установки элементов, выполняйте команды:

```sh
$ npx @roodiroot/zap-ui add <Название элемента>
```

## Названия компонентов

### Элементы

#### elements-biglink

```sh
$ npx @roodiroot/zap-ui add elements-biglink
```

```tsx
<div className='hidden sm:mb-8 sm:flex sm:justify-center'>
  <BigLink
    onClick={() => console.log("hello world")}
    text={"Узнать больше про телескоп Habble"}
  />
</div>
```

#### elements-button

```sh
$ npx @roodiroot/zap-ui add elements-button
```

```tsx
<Button onClick={() => console.log("hello world")} variant='link' arrow>
  Hello
</Button>
```

#### elements-input

```sh
$ npx @roodiroot/zap-ui add elements-input
```

```tsx
<InputCastom placeholder='Введите ваш номер телефона' required />
```

### Главные экраны

#### hello-simple-center

```sh
$ npx @roodiroot/zap-ui add hello-simple-center
```

```tsx
<div className=''>
  <SimpleCenter
    h1='Бесплатный онлайн перевод с английского'
    description='Получите перевод миллионов слов и выражений в направлении русский-английский и реальные примеры употребления благодаря нашей технологии.'
    blur_elements
    biglink='Узнать больше про телескоп Habble'
    biglink_action={() => console.log("biglink")}
    button_link_text='Смотреть далее'
    button_link_action={() => console.log("button_link_action")}
    button_one_text='Консультация'
    button_one_action={() => console.log("button_one_action")}
  />
</div>
```

#### hello-simple-gallery

```sh
$ npx @roodiroot/zap-ui add hello-simple-gallery
```

```tsx
<SimpleGallery
  h1='EDM фестиваль &laquo;Энергия&nbsp;Будущего&raquo;'
  description='Здесь музыкальные ноты переплетаются в гармонии, сценические представления становятся настоящими шедеврами, а мастер-классы от мировых мастеров искусства разглашают тайны творческого мастерства. Присоединяйтесь к этому уникальному событию, где культуры соединяются в танце, звуке и красках, создавая неповторимую симфонию Всемирного Слияния!'
  img_list={[img1, img2, img3, img4, img5, img6, img7]}
  biglink='Узнать больше про телескоп Habble'
  biglink_action={() => console.log("biglink")}
  button_link_text='Смотреть далее'
  button_link_action={() => console.log("button_link_action")}
  button_one_text='Консультация'
  button_one_action={() => console.log("button_one_action")}
  pattern={pattern}
/>
```

#### hello-simple-center-diagonal

```sh
$ npx @roodiroot/zap-ui add hello-simple-center-diagonal
```

```tsx
<div>
  <SimpleCenterVariantDiagonal
    h1='Бесплатный онлайн перевод с английского'
    description='Получите перевод миллионов слов и выражений в направлении русский-английский и реальные примеры употребления благодаря нашей технологии.'
    img={img}
    biglink='Узнать больше про телескоп Habble'
    biglink_action={() => console.log("biglink")}
    button_link_text='Смотреть далее'
    button_link_action={() => console.log("button_link_action")}
    button_one_text='Консультация'
    button_one_action={() => console.log("button_one_action")}
  />
</div>
```

### Блоки информации

#### info-block-earth

```sh
$ npx @roodiroot/zap-ui add info-block-earth
```

```tsx
<InfoSectionFive
  title='Опыт фестиваля также привносит непередаваемое чувство общности — будьте частью единого течения людей'
  description='Наши музыкальные фестивали обещают каждому участнику несравненные впечатления, превращая визит в незабываемое приключение. Вас окутает магия музыки, когда вы окунетесь в вихрь разнообразных жанров — от мистических мелодий, создающих волнующую атмосферу, до динамичных ритмов, которые поднимут вас вверх.'
  img={img7}
  pattern={pattern}
/>
```

#### info-block-mars

```sh
$ npx @roodiroot/zap-ui add info-block-mars
```

```tsx
<InfoSectionFour
  title='Впечатления'
  description='Сцены, наполненные талантливыми артистами со всего мира, подарят вам уникальные сценические перформансы, которые оставят невероятные впечатления и станут источником вдохновения.'
  supdescription='Будте частью единого течения, объединенных любовью к музыке. Энергия толпы, единение в танце создают уникальную атмосферу, которую нельзя описать, но которую можно почувствовать в каждой ноте.'
  img_list={[img5, img2, img3, img4]}
/>
```

#### info-block-mercury

```sh
$ npx @roodiroot/zap-ui add info-block-mercury
```

```tsx
<InfoSectionOne
  title='Эксплозия танцевальных ритмов'
  description='Готовьтесь к танцевальной эксплозии, которая оставит след в вашем сердце на всегда! Погрузитесь в атмосферу энергии и вибраций!'
  button_link_text='Смотреть далее'
  button_link_action={() => console.log("button_link_action")}
  img={img1}
  adv_list={[
    {
      title: "Ощути Энергию Танцпола!",
      description:
        "Впечатляющие световые инсталляции: 300 000 люмен освещения. Ждут каждого кто попадет на фест.",
      first: "Эксклюзивные DJ-сеты",
      second: "4 звездных хедлайнера",
    },
    {
      title: "Билет в Мир Звуковых Вибраций!",
      description:
        "Беспрецедентная атмосфера фестиваля под открытым небом, 20 000 метров квадратных открытой площади.",
      first: "VIP-зона: 360-градусов",
      second: "Нон-стоп танцы",
    },
    {
      title: "Заклинание Электронного Рая!",
      description:
        "Уникальные музыкальные коллаборации во всей красе. Более 15 дуэтов на каждой сцене.",
      first: "Chill-out зона",
      second: "3 секретных гостя",
    },
  ]}
/>
```

#### info-block-upiter

```sh
$ npx @roodiroot/zap-ui add info-block-upiter
```

```tsx
<InfoSectionTree
  title='Три сцены поражающие воображение'
  subtitle='Локации'
  description='От энергичных ритмов на сцене до мистических мелодий и беззаветного веселья, каждая сцена — это отдельная история, созданная для Вас.'
  img={img3}
  adv_list={[
    {
      Icon,
      name: 'Сцена "ЭнергоБит"',
      description:
        "Под мощными звуками. Тут каждый бит – это заряд энергии, каждая нота – вихрь эмоций. Готовы ли вы к музыкальному эксплозиву?",
    },
    {
      Icon,
      name: '"Созвучия Небес"',
      description:
        "Тут встречаются мелодии, которые поднимут вас выше облаков. Погружайтесь в треки, созданные для кайфа и гармонии на фоне ночного неба.",
    },
    {
      Icon,
      name: '"Солнечный Гараж"',
      description:
        "Здесь хаус-ритмы сливаются с Вами, создавая атмосферу беззаветной радости и позитивных вибраций. Забудьте о заботах живите здесь и сейчас.",
    },
  ]}
/>
```

#### info-block-venus

```sh
$ npx @roodiroot/zap-ui add info-block-venus
```

```tsx
<InfoSectionTwo
  subtitle='&laquo;Энергии&nbsp;Будущего&raquo;'
  title='Для чего Вам быть c&nbsp;нами?'
  description='Встретьте с нами расслабление и умиротворение, где живая музыка и звуки природы сочетаются, чтобы создать волнующую симфонию душевного спокойствия.'
  adv_list={[
    {
      name: "Эмоции",
      description:
        "Фестиваль - отличный способ оторваться от рутины, погрузиться в энергию музыки и позволить себе окунуться в атмосферу веселья и радости.",
      Icon: Icon,
    },
    {
      name: "Коммуникации",
      description:
        "Возможность познакомиться с новыми людьми, поделиться своими впечатлениями и создать свою неповторимую историю фестиваля в компании единомышленников.",
      Icon: Icon,
    },
    {
      name: "Инсталляции",
      description:
        "Мы предлагаем уникальные и вдохновляющие искусственные инсталляции и интерактивные зоны, где каждый гость может стать частью творческого процесса.",
      Icon: Icon,
    },
    {
      name: "Кулинария",
      description:
        "Гостям доступны различные кулинарные площадки с разнообразными блюдами из мировой кухни, чтобы полностью погрузиться во вкусовые сенсации вместе с музыкой.",
      Icon: Icon,
    },
  ]}
/>
```

### Call to action блоки

#### cta-earth

```sh
$ npx @roodiroot/zap-ui add cta-earth
```

```tsx
<СTASectionImg
  head='Теперь вперед? Навстречу мечте и музыке.'
  description='Массовое празднество, показ достижений музыкального, театрального, эстрадного.'
  img={img}
  button_link_text='Смотреть далее'
  button_link_action={() => console.log("button_link_action")}
  button_one_text='Консультация'
  button_one_action={() => console.log("button_one_action")}
  pattern={pattern}
/>
```

### Блоки подписки на новости

#### newsletter-sections

```sh
$ npx @roodiroot/zap-ui add newsletter-sections
```

```tsx
<NewsletterSectionCenter
  header='Хотите персональную консультацию?'
  description='Введите ваш номер телефона, чтобы получить подробную информацию и персональные рекомендации от нашей команды.'
  pattern={pattern}
/>
```

### Блоки отзывов

#### testimonials-kuiper-belt

```sh
$ npx @roodiroot/zap-ui add testimonials-kuiper-belt
```

```tsx
<TestemonialsKuiperBeltBlock
  title='Отзывы'
  description='Почитайте что о нас пишут учасники прошлой &laquo;Энергии&nbsp;Будущего&raquo;'
  testimonials_list={[
    {
      text: "“Фестиваль был просто невероятен! Отличная организация, потрясающие артисты и энергия, которая заставляла танцевать до утра. Обязательно приду в следующем году!”",
      name: "Екатерина",
      date: "28 лет",
      img: face,
    },
    {
      text: "“Не могу перестать вспоминать тот момент, когда звуки музыки слились с лучами заката. Фестиваль создал магию, которую трудно передать словами. Это был не просто фестиваль, а настоящее волшебство.”",
      name: "Алексей",
      date: "34 года",
      img: face,
    },
    {
      text: "“Отличное сочетание стилей на разных сценах! Могла наслаждаться треками любимых артистов и открыть для себя новые таланты. Ожидаю следующий год с нетерпением!”",
      name: "Марина",
      date: "22 года",
      img: face,
    },
    {
      text: "“Впечатляющее световое шоу и звуковые эффекты на сцене 'Энергетический Эксплозив'. Это было как погружение в атмосферу будущего. Фестиваль на высшем уровне!”",
      name: "Денис",
      date: "31 год",
      img: face,
    },
    {
      text: "“Сцена 'Солнечные Лучи Гаража' просто волшебна! Танцевала, как будто никто не смотрит. Очень рада, что нашла это уютное место с хаусовыми вибрациями.”",
      name: "Анна",
      date: "25 лет",
      img: face,
    },
    {
      text: "“Отличное место для знакомства с новыми жанрами. 'Созвучия Небес' предоставили мне музыку, которую я раньше не слышал. Полный восторг от открытий!”",
      name: "Игорь",
      date: "29 лет",
      img: face,
    },
    {
      text: "“Идеальный фестиваль для тех, кто любит нестандартные музыкальные эксперименты. Организаторы умеют создавать уникальную атмосферу.”",
      name: "Наталья",
      date: "26 лет",
      img: face,
    },
    {
      text: "“Был на многих фестивалях, но этот выделяется атмосферой взаимопонимания и взаимодействия. Все – от посетителей до артистов – создают единое целое.”",
      name: "Артем",
      date: "32 года",
      img: face,
    },
    {
      text: "“Необычные декорации и арт-инсталляции добавили фестивалю уникальности. Чувствовала себя, как в мире искусства, где каждый уголок пронизан музыкой.”",
      name: "Ольга",
      date: "27 лет",
      img: face,
    },
  ]}
/>
```

### Фото блоки

#### photo-content

```sh
$ npx @roodiroot/zap-ui add photo-content
```

```tsx
<BigPhotoBlock img={img1} />
```

## Команда проекта

Оставьте пользователям контакты и инструкции, как связаться с командой разработки.

- [Максим Борисов](https://t.me/@mvoodi) — Front-End Engineer

## Источники

Впереди только светлое будущее.
