# Мастер создания скриншотов

Это дополнение предоставляет мастер для создания скриншотов всего экрана или отдельных областей, таких как объекты, окна и т. д. Он активируется клавишей _print screen_, которая на стандартных клавиатурах обычно является первой из группы из трёх клавиш справа от F12. Если вы предпочитаете использовать другую клавишу, её можно настроить по пути NVDA меню, параметры подменю, жесты ввода.

При вызове мастера вокруг объекта в фокусе создаётся виртуальный прямоугольник и активируется слой клавиатурных команд со следующими клавиатурными командами:

### команды

* F1 выводит справочное сообщение с основными командами; двойное нажатие открывает этот документ.

#### Информация о прямоугольнике

Клавиши с 1 по 7 предоставляют следующую информацию:

* 1: Координаты левого верхнего и правого нижнего углов.
* 2: Размеры прямоугольника, ширина на высоту.
* 3: Эталонный объект.
* 4: Доля площади прямоугольника, занимаемая эталонным объектом.
* 5: Указывает, находится ли часть эталонного объекта за пределами прямоугольника.
* 6: Указывает, выходит ли прямоугольник за пределы активного окна на переднем плане.
* 7: Доля экрана, занимаемая прямоугольником.

Клавиша пробел читает всю эту информацию подряд.

#### Выбор объекта

Эталонный объект - это объект на экране, который всё время ограничен прямоугольником. Сначала этот объект будет находиться в фокусе системы, но можно выбрать и другой с помощью следующих клавиш:

* Стрелка вверх: обрамляет контейнер текущего объекта.
* F: Обрамляет объект в фокусе.
* N: Обрамляет  объект навигатора.
* W: обрамляет активное окно.
* M: обрамляет объект под указателем мыши.
* S: обрамляет весь экран.

С помощью стрелки вниз изменения отменяются.

#### Размер прямоугольника

Размер прямоугольника можно изменить с помощью следующих клавиш:

* shift + клавиши-стрелки перемещают левый верхний угол:
* shift + стрелка вверх или вниз перемещает верхний край,
* shift + стрелка влево или вправо перемещает левый край.
* С помощью сочитания клавиш control +клавиши-стрелки + перемещается правый нижний угол:
* control + стрелка вверх или вниз перемещает нижний край,
* control + стрелка влево или вправо перемещает правый край.
* control + shift + стрелка вверх расширяет прямоугольник, перемещая все четыре края наружу.
* control + shift + стрелка вниз сжимает прямоугольник, перемещая все четыре края внутрь.

Количество пикселей для этих перемещений можно изменить в настройках дополнения или с помощью клавиш page up и page down.

При изменении размера прямоугольника эталонный объект может измениться. Он всегда будет пытаться выбрать объект, который находится по центру, на переднем плане и занимает большую площадь в прямоугольнике. Об изменении объекта будет сообщено при его появлении.

#### OCR

При нажатии кнопки R текст, включённый в прямоугольник, будет распознан. В некоторых случаях это может не сработать, например, если прямоугольник слишком мал или если установлено дополнение Bluetooth audio (хотя несовместимость встречается редко).

#### Захват изображения

Клавиша Enter создаёт снимок области экрана, ограниченной прямоугольником, сохраняет его в файл и выходит из программы.

Если вместо Enter нажать Shift+enter, появится диалоговое окно с выбором места сохранения скриншота, а не автоматическое сохранение в папку по умолчанию.

Клавиша Escape отменяет действие и приводит к выходу.

### Настройки

По пути  NVDA меню, параметры подменю, настройки, можно настроить следующее:

* Папка, в которую будут сохраняться файлы.  По умолчанию это папка документов пользователя.
* Формат файла изображения.
* Увеличивать или нет захваченное изображение. Масштаб рассчитывается в зависимости от размера прямоугольника и экрана. Маленькие изображения будут увеличены ещё больше, максимум в 4 раза, а большие - только до края экрана.
* Действие после сохранения (ничего, открыть папку или открыть файл).
* Количество пикселей для каждого движения.
