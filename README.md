# SolidWorks Open Selected Part
Открыть текущую выбранную деталь или связанную с ней сборку по одной кнопке в SolidWorks 2021 SP5.1 (и вероятно другие версии)

Одно нажатие = один уровень вниз; повторное нажатие снова опустит на уровень ниже, так как активным документом станет уже открытая подсборка.

Работает в чертежах и 3д видах.


--------


Как установить
1. Инструменты → Макрос → Создать (или Правка макроса), вставь код целиком в Module1, точка входа — Sub main().

2. Сохрани как .swp (или .swb), например OpenSelectedPart.swp.
в любой папке.

3. Инструменты → Настройка → Клавиатура (Customize → Keyboard), найди категорию макросов, назначь горячую клавишу на этот файл. 


--------


Важные нюансы

Если у SW не подключены ссылки на библиотеки типов (обычно подключаются автоматически при создании макроса), а константы вроде swDocASSEMBLY, swSelSHEETS, swDontRebuildActiveDoc не распознаются — открой в редакторе VBA Tools → References и убедись, что отмечены SldWorks 2021 Type Library и SolidWorks 2021 Constant type library.

Для виртуальных (сохранённых внутри сборки) компонентов открыть "файл" нельзя — макрос выдаст сообщение, это ограничение самого SolidWorks, не скрипта.



---------

Open the currently selected part or its associated assembly with a single click in SolidWorks 2021 SP5.1 (and likely other versions)
One click = one level down; clicking again will move down one level again, as the currently open subassembly will become the active document.
