# Задание: ресёрч для детского сайта «Игротека»

## Контекст

«Игротека» — домашний сайт-каталог игр для ребёнка (возраст примерно 5–8 лет, язык — русский). Он лежит на GitHub Pages: https://mrilili.github.io/Igroteka2/ (исходники: https://github.com/MrIlIlI/Igroteka2). Это одна страница `index.html` с массивом `GAMES` (125 карточек) плюс восемь собственных мини-игр в папке `games/`, которые написал ИИ (помечены как «Сделал робот»). У каждой карточки есть поля: `name`, `kind` (категория), `age`, `url`, `img`, `source`, `controls`, `players`, `desc`.

Категории сейчас: Прыжки, Приключения, Головоломки, Думаем, Ловкость, На двоих, Память, Счёт, Рисуем, Музыка, Спокойно.

Полный текущий список игр приложен ниже (раздел «Текущий каталог»). Не предлагай то, что уже есть.

Игр уже достаточно. Главная цель — качество и безопасность, а не количество.

## Что нужно сделать

### 1. Брейншторм: что добавить на сайт (не только игры)

Придумай и обоснуй идеи улучшения сайта. Нужны и игры, и не-игры: разделы, функции, форматы. Примеры направлений, но не ограничивайся ими:

- новые категории или подборки (например «Творим», «Наука», «Истории», «Для всей семьи», «Короткая игра на 5 минут»);
- интерактивные обучающие вещи: тренажёры чтения и счёта, клавиатурные тренажёры для детей, простые симуляторы (физика, космос, природа);
- детские сайты-инструменты: рисовалки, музыкальные игрушки, конструкторы, «песочницы»;
- режим «нашёл игру — открыл на весь экран» для всех карточек;
- функции самого сайта: избранное, «случайная игра», таймер игры, семейный режим «играем вдвоём», ограничение по возрасту.

Для каждой идеи: что это, зачем ребёнку, насколько сложно реализовать (легко / средне / сложно), ссылка на пример или источник.

### 2. Поиск недостающих картинок

У 17 карточек вместо настоящей обложки стоит нарисованная заглушка (в списке ниже помечены «КАРТИНКА-ЗАГЛУШКА»). Самое важное — **Учи.ру**. Для каждой такой игры найди:

- прямую ссылку на официальную обложку, логотип или скриншот (желательно квадрат или близко к квадрату, не меньше 400×400);
- можно ли её использовать на личном некоммерческом сайте (лицензия, пресс-кит, открытый источник);
- если официальной картинки нет, предложи, откуда взять скриншот самой игры.

Отдай это таблицей: название | ссылка на картинку | источник | можно ли использовать | примечание.

### 3. Качество и безопасность уже существующих игр и источников

Проверь сайты-источники из каталога (Яндекс Игры, Poki, Google Doodles, Y8, CoolMathGames, Играемся, FRVR, отдельные авторские сайты) и ответь по каждому:

- есть ли реклама, всплывающие окна, переходы на другие игры, чат, покупки, регистрация;
- открывается ли игра сразу на полный экран или ребёнок видит каталог с кучей других игр;
- не пропали ли игры, не сменились ли ссылки (особенно Google Doodles и Y8).

Приоритеты при отборе новых игр и источников, в порядке убывания:

1. **Можно положить прямо на сайт.** Открытый исходный код или бесплатный встраиваемый лаунчер (лицензии MIT, GPL, CC и подобные). Такие игры хотим скачать в папку `games/` и открывать без внешних сайтов. Для каждой: ссылка на репозиторий, лицензия, какие файлы нужны, работает ли без сервера (чистый HTML/JS).
2. **Открывается сразу на весь экран, без рекламы и каталога.** Отдельные авторские сайты, Google Doodles, Chrome Music Lab и подобное.
3. **Открытые каталоги допустимы**, но с оговоркой: честно опиши, что ребёнок увидит вокруг игры.

Перечень кандидатов на замену: если какая-то игра из каталога живёт на «шумном» сайте, а есть версия с открытым кодом или на чистом сайте, предложи замену с конкретной ссылкой.

### 4. Порядок на главной странице

Предложи новый порядок карточек с учётом правил:

- новые добавления стоят в самом верху;
- игры «Сделал робот» (восемь штук) уходят ниже, не на первый экран;
- Учи.ру нужно поднять заметно выше, чем сейчас (сейчас 56-я позиция).

Выдай готовый порядок как список названий сверху вниз, с короткой пометкой, почему именно так (например «свежее», «образовательное», «быстрый старт»).

## Формат результата

Результаты потом будут переданы другому ИИ-агенту, который вносит правки в код. Поэтому:

- всё в одном Markdown-файле;
- каждая рекомендуемая игра или ресурс — отдельной записью по шаблону ниже (это нужно, чтобы агент мог сразу сделать карточку);
- ссылки только прямые и проверенные, без сокращателей; если ссылка не проверена, напиши «(не проверено)»;
- не придумывай игры и лицензии: если не уверен, так и напиши.

Шаблон записи для игры или ресурса:

```
### Название (по-русски, как для ребёнка)
- url: прямая ссылка на игру
- категория: одна из существующих или предложение новой
- возраст: от N лет
- игроков: 1 / 2 / 1–4
- управление: мышь / стрелки / клавиатура / тач
- источник: название сайта или автора
- лицензия и возможность положить на сайт: да (ссылка на код, лицензия) / нет / неизвестно
- что видит ребёнок вокруг игры: полный экран / каталог / реклама / регистрация
- картинка: прямая ссылка на обложку или скриншот + можно ли использовать
- описание (1–2 предложения для ребёнка, по-русски)
- почему стоит добавить (1 предложение)
- приоритет: высокий / средний / низкий
```

Структура файла:

1. Краткое резюме (10–15 строк): главные выводы и топ-10 рекомендаций.
2. Идеи для сайта (брейншторм).
3. Новые игры и ресурсы (по шаблону), сначала те, что можно положить на сайт.
4. Недостающие картинки (таблица).
5. Аудит текущих источников и список проблемных ссылок.
6. Предлагаемый порядок карточек.
7. Что не удалось проверить и почему.

## Текущий каталог

Формат: название | категория | возраст | игроков | источник | ссылка | (пометка о заглушке)

- Песок и огонь | Спокойно | 5+ | 1 | Сделал робот | games/pesok.html
- Сонные призраки | Ловкость | 6+ | 1 | Сделал робот | games/sleepy.html
- До рассвета | Ловкость | 6+ | 1 | Сделал робот | games/svetlyachok.html
- Хор зверей | Музыка | 4+ | 1-2 | Сделал робот | games/hor.html
- Лабиринт дракона | Приключения | 5+ | 1 | Сделал робот | games/labirint.html
- Плыг-Па-Па! | Ловкость | 3+ | 1 | Сделал робот | games/plyg.html
- Найди пару | Память | 4+ | 1-2 | Сделал робот | games/pary.html
- Пиратский счёт | Счёт | 5+ | 1 | Сделал робот | games/schet.html
- Супер Марио | Прыжки | 6+ | 1 | Другой сайт | https://www.joshuakgoldberg.com/FullScreenMario/Source/
- Огонь и Вода | На двоих | 6+ | 1-2 | Яндекс Игры | https://yandex.ru/games/app/fireboy-and-watergirl-1-in-the-forest-temple-96860
- Сабвей Серф | Ловкость | 6+ | 1 | Poki | https://poki.com/ru/g/subway-surfers
- Ам Ням | Головоломки | 4+ | 1 | Яндекс Игры | https://yandex.ru/games/app/am-niam-pererezh-veriovku-289684
- Остров чемпионов | Приключения | 7+ | 1 | Google | https://www.google.com/logos/2020/kitsune/rc6/kitsune20.html?hl=ru
- Курочка через дорогу | Ловкость | 5+ | 1 | Poki | https://poki.com/ru/g/crossy-road
- Кот-волшебник | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2016/halloween16/halloween16.html?hl=ru | КАРТИНКА-ЗАГЛУШКА
- Магазин обезьянок | Спокойно | 5+ | 1 | Poki | https://poki.com/ru/g/monkey-mart
- Смешной футбол | На двоих | 4+ | 1-2 | Яндекс Игры | https://yandex.ru/games/app/futbol-sluchainyi-197306
- Плохое мороженое | На двоих | 6+ | 1-2 | Poki | https://poki.com/ru/g/bad-ice-cream
- Город на воде | Спокойно | 4+ | 1 | Другой сайт | https://oskarstalberg.com/Townscaper/
- Мотогонки X3M | Ловкость | 7+ | 1 | Poki | https://poki.com/ru/g/moto-x3m
- Улитка Боб 3 | Головоломки | 5+ | 1 | Яндекс Игры | https://yandex.ru/games/app/ulitka-bob-3-neobitaemyi-ostrov-442218
- Поющие блобы | Музыка | 4+ | 1 | Google | https://gacembed.withgoogle.com/blob-opera?lang=ru&locale=ru
- Ловкие воры 2 | На двоих | 7+ | 1-2 | Y8 | https://ru.y8.com/games/money_movers_2
- Мальчик-лук | Прыжки | 6+ | 1 | Яндекс Игры | https://yandex.ru/games/app/super-onion-boy-2-415849
- Битва призраков | Ловкость | 6+ | 1 | Google | https://www.google.com/logos/2021/halloween18_reboot/r1025/halloween18_reboot.html?hl=ru | КАРТИНКА-ЗАГЛУШКА
- Спрячь апельсин | Головоломки | 5+ | 1 | Яндекс Игры | https://yandex.ru/games/app/cover-orange-puteshestvie-286418
- Космонавт Астро | Прыжки | 6+ | 1 | Яндекс Игры | https://yandex.ru/games/app/189286
- Кот-пират | Прыжки | 6+ | 1 | Poki | https://poki.com/ru/g/nekopirate-quest-for-gold
- Красный шарик | Прыжки | 5+ | 1 | Яндекс Игры | https://yandex.ru/games/app/red-ball-4-263344
- Лисёнок Фокси | Прыжки | 6+ | 1-2 | Яндекс Игры | https://yandex.ru/games/app/foxy-land-2-197228
- Мир Алекса | Прыжки | 6+ | 1 | Яндекс Игры | https://yandex.ru/games/app/alex-world-197434
- Приключения Неженки | Прыжки | 7+ | 1 | Poki | https://poki.com/ru/g/fancy-pants
- Найди друзей | Приключения | 4+ | 1 | Другой сайт | https://amanita-design.net/thequestfortherest/
- Найди конфетку | Приключения | 7+ | 1 | Poki | https://poki.com/ru/g/find-the-candy
- Панголин | Приключения | 6+ | 1 | Google | https://www.google.com/logos/2017/vday17/vday17-27917071.html?hl=ru
- Щенок-беглец | Приключения | 5+ | 1 | FRVR | https://frvr.com/play/dogescape/
- Ам Ням 2 | Головоломки | 6+ | 1 | Яндекс Игры | https://yandex.ru/games/app/am-niam-pererezh-veriovku-2-511180
- Ам Ням: Магия | Головоломки | 5+ | 1 | Яндекс Игры | https://yandex.ru/games/app/am-niam-pererezh-veriovku-magiia-482665
- Ам Ням: Путешествие во времени | Головоломки | 4+ | 1 | Яндекс Игры | https://yandex.ru/games/app/am-niam-pererezh-verevku-puteshestvie-vo-vremeni-503258
- Братья-динозаврики | Головоломки | 6+ | 1 | Poki | https://poki.com/ru/g/dino-bros
- Вилли в сказке | Головоломки | 4+ | 1 | Яндекс Игры | https://yandex.ru/games/app/wheely-6-fairytale-425997
- Машинка Вилли | Головоломки | 4+ | 1 | Яндекс Игры | https://yandex.ru/games/app/wheely-3-96821
- Робот Робби | Головоломки | 6+ | 1 | Яндекс Игры | https://yandex.ru/games/app/robbie-96763
- Тетрис | Головоломки | 7+ | 1 | Tetris.com | https://play.tetris.com/
- Улитка Боб 5 | Головоломки | 6+ | 1 | Y8 | https://ru.y8.com/games/snail_bob_5
- Улитка Боб 7 | Головоломки | 6+ | 1 | Y8 | https://ru.y8.com/games/snail_bob_7_fantasy_story
- Улитка Боб: зима | Головоломки | 5+ | 1 | Яндекс Игры | https://yandex.ru/games/app/snail-bob-6-winter-story-96817
- Улитка Боб: остров | Головоломки | 5+ | 1 | Яндекс Игры | https://yandex.ru/games/app/snail-bob-8-island-story-96819
- Duolingo | Думаем | 6+ | 1 | Другой сайт | https://www.duolingo.com/
- Кролик и морковки | Думаем | 5+ | 1 | Google | https://www.google.com/logos/2017/logo17/logo17.html?hl=ru | КАРТИНКА-ЗАГЛУШКА
- Лабиринт-программа | Думаем | 6+ | 1 | Blockly Games | https://blockly.games/maze?lang=ru
- Майнкрафт: программируем | Думаем | 7+ | 1 | Code.org | https://studio.code.org/ru/courses/mc/units/1/lessons/1/levels/1
- Пицца | Думаем | 6+ | 1 | Google | https://www.google.com/logos/2021/pizza/rc5/pizza.html?hl=ru
- Путь мумии | Думаем | 7+ | 1 | Poki | https://poki.com/ru/g/mummys-path-deluxe
- Сапёр | Думаем | 7+ | 1 | Google | https://www.google.com/fbx?fbx=minesweeper&hl=ru | КАРТИНКА-ЗАГЛУШКА
- Учи.ру | Думаем | 6+ | 1 | Другой сайт | https://uchi.ru/ | КАРТИНКА-ЗАГЛУШКА
- Шахматы | Думаем | 6+ | 1 | Другой сайт | https://lichess.org/learn | КАРТИНКА-ЗАГЛУШКА
- Шахматы ChessKid | Думаем | 7+ | 1 | ChessKid | https://www.chesskid.com/ru/play/computer
- Шахматы для малышей | Думаем | 6+ | 1 | Poki | https://poki.com/ru/g/jr-chess
- Ам Ням: башня | Ловкость | 6+ | 1 | Яндекс Игры | https://yandex.ru/games/app/om-nom-tower-3d-204334
- Ам Ням: бег | Ловкость | 6+ | 1 | Яндекс Игры | https://yandex.ru/games/app/am-niam-gonka-153785
- Ам Ням: шарики | Ловкость | 5+ | 1 | Яндекс Игры | https://yandex.ru/games/app/am-niam-shariki-176736
- Баскетбол | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2012/basketball-2012-hp.html
- Бег из храма 2 | Ловкость | 7+ | 1 | Poki | https://poki.com/ru/g/temple-run-2
- Бег с барьерами | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2012/hurdles-2012-hp.html
- Безумная машинка | Ловкость | 6+ | 1 | Poki | https://poki.com/ru/g/drive-mad
- Бейсбол | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2019/july4th19/r6/july4th19.html?hl=ru
- Битва призраков 2 | Ловкость | 6+ | 1 | Google | https://www.google.com/logos/2021/halloween21/v81123/halloween21.html?hl=ru | КАРТИНКА-ЗАГЛУШКА
- Дракончик Блумги | Ловкость | 6+ | 1-2 | Poki | https://poki.com/ru/g/blumgi-dragon
- Змейка | Ловкость | 5+ | 1 | Google | https://www.google.com/fbx?fbx=snake_arcade | КАРТИНКА-ЗАГЛУШКА
- Кот-волшебник 2 | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2020/halloween20/rc1/halloween20.html?hl=ru | КАРТИНКА-ЗАГЛУШКА
- Мороженое и перцы | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2016/scoville/scoville16.html?hl=ru
- Пакман | Ловкость | 6+ | 1 | Google | https://www.google.com/logos/2010/pacman10-hp.html | КАРТИНКА-ЗАГЛУШКА
- Попкорн | Ловкость | 6+ | 1 | Google | https://www.google.com/logos/2024/popcorn/rc5/popcorn.html?hl=ru
- Садовые гномы | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2018/gnomes/gnomes18.html?hl=ru
- Сверчок и мяч | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2017/cricket17/cricket17.html?hl=ru
- Чай с шариками | Ловкость | 5+ | 1 | Google | https://www.google.com/logos/2023/boba/rc3/boba.html?hl=ru
- Человечек на крючках | Ловкость | 7+ | 1 | Poki | https://poki.com/ru/g/stickman-hook
- Boxing Random | На двоих | 5+ | 1-2 | Яндекс Игры | https://yandex.ru/games/app/boxing-random-197305
- Volley Random | На двоих | 4+ | 1-2 | Яндекс Игры | https://yandex.ru/games/app/volley-random-197307
- Близнецы-лучники | На двоих | 7+ | 1-2 | Poki | https://poki.com/ru/g/twin-shot
- Близнецы-лучники 2 | На двоих | 7+ | 1-2 | Poki | https://poki.com/ru/g/twin-shot-2-html5
- Два шара 3D: Темный | На двоих | 6+ | 1-2 | Яндекс Игры | https://yandex.ru/games/app/dva-shara-3d-temnyi-192107
- Динозаврики | На двоих | 5+ | 1-2 | Яндекс Игры | https://yandex.ru/games/app/dino-meat-hunt-dry-land-201408
- Дуэль на двоих | На двоих | 5+ | 2 | Яндекс Игры | https://yandex.ru/games/app/igry-na-dvoikh-duel-227711
- Игры на четверых | На двоих | 5+ | 2-4 | Яндекс Игры | https://yandex.ru/games/app/2-3-4-player-games-233488
- Крестики-нолики | На двоих | 4+ | 1-2 | Google | https://www.google.com/fbx?fbx=tic_tac_toe&hl=ru | КАРТИНКА-ЗАГЛУШКА
- Ловкие воры | На двоих | 7+ | 1-2 | Y8 | https://ru.y8.com/games/money_movers
- Ловкие воры 3 | На двоих | 7+ | 1-2 | Y8 | https://ru.y8.com/games/money_movers_3_guard_duty
- Мини-игры 3D | На двоих | 5+ | 2-4 | Яндекс Игры | https://yandex.ru/games/app/mini-igry-na-dvoikh-3-286057
- Мини-игры на двоих | На двоих | 5+ | 2 | Яндекс Игры | https://yandex.ru/games/app/mini-igry-na-dvoikh-2-202043
- Огонь и Вода 2 | На двоих | 7+ | 1-2 | Другой сайт | https://www.coolmathgames.com/0-fireboy-watergirl-2-light-temple
- Огонь и Вода 3 | На двоих | 7+ | 1-2 | Другой сайт | https://www.coolmathgames.com/0-fireboy-watergirl-3-ice-temple
- Огонь и Вода 4 | На двоих | 7+ | 1-2 | Другой сайт | https://www.coolmathgames.com/0-fireboy-watergirl-4-crystal-temple
- Огонь и Вода 5 | На двоих | 7+ | 1-2 | Другой сайт | https://www.coolmathgames.com/0-fireboy-watergirl-5-elements
- Огонь и Вода 6 | На двоих | 7+ | 1-2 | Другой сайт | https://www.coolmathgames.com/0-fireboy-watergirl-6-fairy-tales
- Плохое мороженое 3 | На двоих | 6+ | 1-2 | Poki | https://poki.com/ru/g/bad-ice-cream-3
- Ра3ума Игры 2-3-4 Игрока | На двоих | 5+ | 2-4 | Яндекс Игры | https://yandex.ru/games/app/ra3uma-igry-2-3-4-igroka-209957
- Смешной баскетбол | На двоих | 4+ | 1-2 | Яндекс Игры | https://yandex.ru/games/app/basket-random-197304
- Четыре в ряд | На двоих | 5+ | 1-2 | Poki | https://poki.com/ru/g/four-in-a-row
- Шашки | На двоих | 6+ | 1-2 | Poki | https://poki.com/ru/g/master-checkers
- Ам Ням: соедини пары | Память | 5+ | 1 | Яндекс Игры | https://yandex.ru/games/app/om-nom-connect-classic-176735
- Лотерея картинок | Память | 6+ | 1 | Google | https://www.google.com/logos/2019/loteria/r3/loteria19.html?hl=ru
- Найди голубей | Память | 6+ | 1 | Poki | https://poki.com/ru/g/hidden-pigeon
- Найди отличия | Память | 5+ | 1 | Poki | https://poki.com/ru/g/spot-the-differences
- Пары: подводный мир | Память | 4+ | 1 | Играемся | https://www.igraemsa.ru/igry-dlja-detej/igry-na-vnimanie-i-pamjat/najdi-paru-vodnyj-mir
- 2048 | Счёт | 8+ | 1 | Poki | https://poki.com/ru/g/2048
- Весёлый счёт | Счёт | 4+ | 1 | Играемся | https://www.igraemsa.ru/igry-dlja-detej/matematicheskie-igry/veselyj-schet
- Змеи и лесенки | Счёт | 5+ | 2-4 | Poki | https://poki.com/ru/g/snakes-and-ladders
- Line Rider | Рисуем | 6+ | 1 | Другой сайт | https://linerider.com/ | КАРТИНКА-ЗАГЛУШКА
- Silk | Рисуем | 4+ | 1 | Другой сайт | https://weavesilk.com/
- Волшебная раскраска | Рисуем | 4+ | 1 | Poki | https://poki.com/ru/g/magic-coloring-book
- Рисуй и слушай | Рисуем | 4+ | 1 | Google | https://musiclab.chromeexperiments.com/Kandinsky/
- Угадай рисунок | Рисуем | 6+ | 1 | Google | https://quickdraw.withgoogle.com/?locale=ru | КАРТИНКА-ЗАГЛУШКА
- Диджей | Музыка | 5+ | 1 | Google | https://www.google.com/logos/2017/hiphop/hiphop17.html?hl=ru | КАРТИНКА-ЗАГЛУШКА
- Звуки на кнопках | Музыка | 4+ | 1 | Другой сайт | https://patatap.com/
- Мелодия | Музыка | 4+ | 1 | Google | https://musiclab.chromeexperiments.com/Melody-Maker/ | КАРТИНКА-ЗАГЛУШКА
- Музыка фигур | Музыка | 5+ | 1 | Google | https://www.google.com/logos/2017/fischinger/fischinger17.html?hl=ru | КАРТИНКА-ЗАГЛУШКА
- Мяузика | Музыка | 4+ | 1 | Яндекс Игры | https://yandex.ru/games/app/miauzika-387266
- Ритм | Музыка | 4+ | 1 | Google | https://musiclab.chromeexperiments.com/Rhythm/
- Сочини песню | Музыка | 4+ | 1 | Google | https://musiclab.chromeexperiments.com/Song-Maker/
- Котик-пиццерия | Спокойно | 6+ | 1 | Poki | https://poki.com/ru/g/cat-pizza
- Песочные замки | Спокойно | 4+ | 1 | Другой сайт | https://vectorpark.com/sandcastles/
- Пчела и цветы | Спокойно | 4+ | 1 | Google | https://www.google.com/logos/2020/earthday20/r3/earthday20.html?hl=ru | КАРТИНКА-ЗАГЛУШКА
- Собери арбуз | Спокойно | 5+ | 1 | Poki | https://poki.com/ru/g/watermelon-drop
