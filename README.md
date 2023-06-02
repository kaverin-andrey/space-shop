# Оглавление
1. [Как развернуть проект](#Как-развернуть-проект)
2. [Дополнительные команды](#Дополнительные-команды)
3. [Универсальные классы](#Универсальные-классы)
4. [Миксины](#Миксины)
5. [Переменные](#Переменные)
6. [Другое](#Другое)

## Как развернуть проект

1. В терминале:
```
npm i
```
2. После того как установятся все зависимости<br>
**Для того что бы развернуть проект для разработки(большинство тасков не будет выполняться)**
```
npm run dev
```
**Для того что бы собрать финальную версию проекта**
```
npm run buid
```
3. После того как сборщик закончит работу, готовый проект будет лежать в папке **dist**

## Дополнительные команды
1. Собрать zip архив(будет произведена финальная сборка проекта)
```
npm run zip
```
2. Если необходимо сделать пак иконок вручную
```
npm run svg
```

## Универсальные классы
1. Класс, ограничивающий максимальную ширину блока(1230px) с инлайн отступами 24px
```
<div class="container"></div>
```
2. Гриды(создает сетку в 12 колонок)
```
<div class="grid"></div>
```

## Миксины
1. Шрифт
```
@include font(Имя_шрифта, размер_шрифта, межстрочный_интервал, толщина, цвет);
```
	- межстрочный_интервал(необязательный, по умолчанию 1.2)
	- толщина(необязательный, по умолчанию 400)
	- цвет(необязательный, по умолчанию $ui-color-black = #000)
2. Ширина
```
@include maxWidth(Ширина, отступ_сверху, отступ_снизу);
```
	- Ширина(Необязательно, по умолчанию $ui-container-width = 1230px)
	- отступ_сверху(Необязательный, если не задать, то ничего не будет)
	- отступ_снизу(Необязательный, если не задать, то ничего не будет)

- Инлайн отступы автоматичски будут = 24px
3. Flex
```
@include flex(align-items, justify-content)
```
**Есть несколько настроек.**
- align-items:
	- fs -> align-items: flex-start;
	- ce -> align-items: center;
	- fe -> align-items: flex-end;
	- str -> align-items: stretch;
- justify-content:
	- fs -> justify-content: flex-start;
	- ce -> justify-content: center;
	- fe -> justify-content: flex-end;
	- sb -> justify-content: space-between;
	- se -> justify-content: space-evenly;
	- sa -> justify-content: space-around;
```
@include flex-wrap(wrap);
```
**Тут 2 варианта**
- 0 -> flex-wrap: nowrap;
- 1 -> flex-wrap: wrap;
```
@include flex-item(количество, отступ);
```
- количество - количество элементов, которые нужно разместить в 1 строке
- отступ - нужный отступ между элементами
4. Скроллбар
```
@include scrollbar(xy, height, width, widthscroll)
```
- xy - направление скролла(по оси X или Y)
- height - необязательный параметр(максимальная высота блока для скролла по оси Y)
- width - необязательный параметр(максимальная ширина блока для скролла по оси X)
- widthscroll - толщина скролла
5. Медиазапросы
```
@include media(width);
```
- width - тут несколько доступных параметров
	- 1
	```
	@media screen and (max-width:999px) {
	}
	```
	- 2
	```
	@media screen and (max-width:768px) {
	}
	```
	- 3
	```
	@media screen and (max-width:576px) {
	}
	```
	- произвольное_число
	```
	@media screen and (max-width:произвольное_числоpx) {
	}
	```
## Переменные
```
$ui-container-width: 1230px;
$ui-container-offset: 24px;

$ui-font: 'NotoSans', sans-serif;

$ui-color-black: #000;
$ui-color-white: #FFFFFF;
$ui-color-violet: #B178FF;
$ui-color-azure: #A3DEFF;
$ui-color-transparent: transparent;

$ui-fitler-blur: 20px;
$ui-border-radius: 10px;
$ui-drop-shadow: drop-shadow(0px 10px 30px rgba(1, 33, 103, 0.1));

$ui-transition-time: .2s;
$ui-transition-function: ease-in-out;
```
6. Другое
Если есть необходимость использования локальных плагинов, для них можно создать папку plugins в папках ./scr/css & ./scr/js. В нее положить нужные файлы. Все работает при запущенной разработке с флагом dev
