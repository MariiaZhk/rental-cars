# Car Rental / Застосунок для компанії з оренди автомобілів

## Опис

Цей застосунок складається з трьох основних сторінок:

### домашня сторінка:

містить загальний огляд послуг компанії та посилання на каталог автомобілів;

### каталог автомобілів:

- це cторінка з пропозиціями оренди різних автомобілів, які можна фільтрувати за критеріями. При завантаженні сторінки з бекенду приходять перші 12 оголошень про оренду авто, при натисканні на кнопку Load more - наступні 12. При натисканні на кнопку у вигляді "серця", яка міститься на кожній картці-оголошенні, відповідна картка додається до списку улюблених, а колір кнопки змінюється на блакитний.Повторне натискання на кнопку у вигляді "серця" видаляє оголошення зі списку улюблених, а колір кнопки змінюється на початковий.

- Реалізовано фільтр у вигляді селекту із dropdown, що містить марки автомобілів, наявні у базі даних. Пошук авто за маркою відбувається при натисканні кнопки "Search".

- Натисканням на кнопку "Learn more" відкривається модальне вікно з детальною інформацією про авто та умови його оренди.
  Модальне вікно можна закрити натисканням на кнопку у вигляді "хрестика", кліком на backdrop або натисканням клавішу Esc.
  Кнопка "Rental car" надає можливість користувачу зв'язатися з компанією за номером телефону.

### улюблені авто:

це сторінка з автомобілями, які користувач відніс до списку улюблених. Якщо користувач ще не обрав улюбдених авто, то відображається порожня сторінка з пропозицією зробити це.При оновленні сторінки зберігається результат дій користувача (вибрані авто залишаються в списку улюблених) за допомогою local storage.

##### Кожна сторінка містить хедер із навігацією та футер із контактною інформацією.

> > > > > > > > > > > > > > > > > > > > >

## Тестове завдання

Створити застосунок для компанії, що надає послуги надання в Україні автомобілів в оренду.

1. Застосунок складається з 3х сторінок:
   домашня сторінка з загальним описом послуг, що надає компанія.Стилізація та оформлення на ваш розсуд.
2. Cторінка, що містить каталог автівок різної комплектації, які користувач може фільтрувати за маркою, ціною за годину оренди авто та кількістю кілометрів, яку подолав автомобіль під час його експлуатації (пробіг).
3. Cторінка з оголошеннями, які були додані користувачем в улюблені Зовнішній вигляд програми повинен складатися з навігації(оформлення на ваш розсуд) та області перегляду.

## Технічне завдання

1. Відповідно до макету реалізувати картку оголошення про здачу авто в оренду.
2. На першій сторінці каталогу має рендеритися 12 оголошень, а їх решта - по кліку на кнопку Load more.
3. У разі кліку по кнопці у вигляді “серця” на картці оголошення воно має додаватися до списку улюблених, а колір кнопки змінюватися.
4. При оновленні сторінки має фіксуватись кінцевий результат дій користувача. Тобто, якщо додати оголошення в улюблені та оновити сторінку - то кнопка все одно залишається в стані “улюбленого оголошення” із відповідним кольором.
   У разі повторного кліку по кнопці у вигляді “серця” оголошення повинно бути видалене зі списку улюблених, а колір кнопки змінитись до початкового стану.
5. У разі кліку по кнопці Learn more має відкриватись модальне вікно з детальною інформацією про авто та умови його оренди.
6. Модальне вікно повинно закриватись по кліку на кнопку у вигляді “хрестика”, по кліку на backdrop або натисканню на клавішу Esc.
7. В коді пробіг авто має бути прописаний одним значенням (наприклад, 4500). В UI - виведено через кому (4,500).
8. Кнопку Rental car слід реалізувати як посилання, що надаватиме можливість користувачу зʼєднатись з компанією за номером телефону +380730000000.
9. Додай фільтрацію: dropdown із марками автомобіля makes.json - показати оголошення з автівками відповідної марки.
10. Створи маршрутизацію, використовуючи React Router. У застосунку повинні бути такі маршрути: “/” - домашня сторінка з загальним описом послуг, що надає компанія “/catalog” - сторінка, що містить каталог автівок різної комплектації “/favorites” - сторінка з оголошеннями, які були додані користувачем в улюблені. Якщо користувач зайшов за маршрутом, якого не існує, його необхідно перенаправляти на домашню сторінку.

11. Для роботи зі списком оголошень створи свій персональний бекенд для розробки за допомогою UI-сервісу https://mockapi.io/. Створи ресурс adverts. Використай конструктор ресурсу та опиши об'єкт оголошення, як описано нижче.

Advert

1. Створіть `advert` в **Mockapi** з наступними полями: `id`, `year`, `make`,
   `model`, `type`, `img`, `description`, `fuelConsumption`, `engineSize`,
   `accessories`, `functionalities`, `rentalPrice`, `rentalCompany`, `address`,
   `rentalConditions`, `mileage`.
2. В базі має бути від 32 оголошень з різними значеннями. Реалізована пагінація, де одна сторінка пагінації повинна вміщати 12 оголошень.Пагінація має бути реалізована на стороні Mockapi.

## Критерії виконання

- Верстка фіксована в рх, семантична та валідна.
- Обов’язкове використання Redux
- Для запитів використовується бібліотека Axios
- Пагінація реалізована на бекенді
- Немає помилок в консолі браузера.
- Інтерактивність працює відповідно до технічного завдання.
- Код відформатовано та не містить невикористовуваного коду
- В репозиторії має бути описаний **README.md**
- Проєкт задеплоїний на **github pages** або **netlify.com**
